# Read: 11 - EJS

* [Watch EJS tutorial from WalkThroughCode on YouTube, Videos 1-5](https://www.youtube.com/playlist?list=PL7sCSgsRZ-slYARh3YJIqPGZqtGVqZRGt)
* EJS = Embedded Javascript Templating
* In the intro getting started he requires express, body-parser, cors and path, then creates an instance of the app with express, then configure the app with app.use() with bodyParser() and cors() - though it's unclear what that does.
app.set('views',path.join(__dirname,'views')); //for the views concatenate the current working directory and a folder called views
app.set('view engine', 'ejs); //now it's set to go.
Then he creates a folder called views with an index.ejs inside it.
Then he sets the path to listen on port 8000.
then he creates a simple route for the root directory with app.get('/',(request,response) => { response.render('index')}); //dont need to specify the path for index

* Injecting values into our views with EJS
in the app.get add a second parameter to the response.render with a new object. In the index.ejs you can then refer to the property of that object using <%= foo %>

* To loop, we pass in the array of objects in response.render then in index.ejs use:

``` javascript
<ul>
<% for(var person of people) {
    <li><%= person.name %> </li>
    <% } %>
</ul>
```

* to do an if statement:

``` javascript
<ul>
    <% for(var person of people) {
        <% if (person.name === 'dave') { %>
        <li> this is definitely <%= person.name %>!!!</li>
        <% } else { %>
        <li> This is definitely not dave!!! This is <%= person.name %> </li>
        <% } %>
    <% } %>
</ul>
```

## Additional Resources

* Reference: [Google Books API Docs](https://developers.google.com/books/docs/v1/using#WorkingVolumes)
Specifically the section about working with Volumes. Review the sample request and response. Practice making requests using Postman and consider the possible properties of the response that you may want to include in your book application.
* Reference: [EJS Docs](https://ejs.co/)

Bookmark/Skim

* Skim: [EJS Tutorial](https://www.digitalocean.com/community/tutorials/how-to-use-ejs-to-template-your-node-application)
* Skim: [Source Code for the EJS Tutorial](https://github.com/scotch-io/node-ejs)
Review the code that goes along with the tutorial
