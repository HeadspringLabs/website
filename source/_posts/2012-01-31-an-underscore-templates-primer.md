---
layout: post
title: An Underscore Templates Primer
categories:
- Developer Deep Dive
- javascript
- json
- underscore
status: publish
type: post
published: true
author: tim
---
<p>In April 2011, the jQuery team <a href="http://api.jquery.com/category/plugins/templates/">announced</a> development on the popular jQuery Templates plugin would be delayed indefinitely. In need of a replacement, I began investigating alternatives and soon discovered <a href="http://documentcloud.github.com/underscore/">Underscore</a>, the "utility belt" library behind the awesome <a href="http://documentcloud.github.com/backbone/">Backbone.js</a> framework. The Underscore library includes an easy-to-use templating feature that easily integrates with any JSON data source, so read on to learn how easy it is to create JSON-backed templates.</p>
<p>Sending JSON data to a browser is outside the scope of this blog post, but, for reference, take a look at this collection of books:</p>
    [
      {
        "title":"Myst: The Book of Atrus",
        "author":"Rand Miller"
      },
      {
        "title":"The Hobbit",
        "author":"J.R.R. Tolkien"
      },
      {
        "title":"Stardust",
        "author":"Neil Gaiman"
      }
    ]

<p>In this example, we'll display this collection of books as a simple unordered list, but don't let that stop you from experimenting!</p>
<h2>The Template</h2>
<p>First, we need to define our Underscore template, which we'll do in a <code>&lt;script&gt;</code> block (meaning browsers will ignore it while rendering the page, but we can still reference it by its client ID) with the type of <code>text/template</code> (so your fellow developers will know it's a template versus a standard bit of JavaScript).</p>

    <script id="tmpl-books" type="text/template">
      <ul>
        <% for (var i = 0; i < books.length; i++) { %>
          <% var book = books[i]; %>
          <li>
          <em><%= book.title %></em> by <%= book.author %>
          </li>
        <% } %>
      </ul>
    </script>

<p>If you've worked with tools like ASP.NET "WebForms" or Rails, you may recognize the "bee sting" operators (<code>&lt;%</code> and <code>%&gt;</code>), which Underscore uses to both output data to the rendered template and encapsulate behavior (as JavaScript). In this template, we first loop through the "books" collection (which we'll define in the next section), pluck out each book as the loop progresses, and print out the<br />
title and author of each as an unordered list item.</p>
<p>You're free to inject as much JavaScript as you wish into your templates, but I find they're most maintainable when the script is kept to a minimum (for me, this means mostly just loops and ternary operators, like the one below).</p>

    <% book.published ? print('(' + book.published + ')') : '' %>

<p>(The <code>print()</code> function is a handy alternative to the <code>&lt;%= %&gt;</code> syntax for outputting values inside other functions, like we're doing here.)</p>
<h2>The Result</h2>
<p>Now that we've defined our JSON source and the template for displaying our data, we need simply to tell Underscore to render the template and give us back the output HTML (using Underscore's <code>template()</code> function).</p>
<p>In our example, <code>data</code> represents our JSON collection of books, but keep in mind your JSON data source may be named something different. We'll tell Underscore to put this data inside the <code>books</code> collection, which we've referenced in our template.</p>

    // Get the template's markup...
    var tmplMarkup = $('#tmpl-books').html();
    // ...tell Underscore to render the template...
    var compiledTmpl = _.template(tmplMarkup, { books : data });
    // ...and update part of your page:
    $('#target').html(compiledTmpl);

<p>Underscore kindly compiles the template with our well-formed data and produces the following output, ready for injection into our HTML page:</p>

    <ul>
      <li><em>Myst: The Book of Atrus</em> by Rand Miller</li>
      <li><em>The Hobbit</em> by J.R.R. Tolkien</li>
      <li><em>Stardust</em> by Neil Gaiman</li>
    </ul>

<p>Underscore's templating feature quickly made its way onto my list of must-have tools for client-side Web development. Try your hand at a few JSON-backed templates using this versatile framework and it may appear on yours, as well.</p>
