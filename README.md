bootpag - dynamic pagination
============================

This jQuery plugin helps you create dynamic pagination with [Bootstrap](http://getbootstrap.com/) or in any other html pages.

#Example

Snippet that dynamic loads number of pages.
More examples can be found on [project homepage](http://botmonster.com/jquery-bootpag/)

```html
<p id="content">Dynamic page content</p>
<p id="pagination-here"></p>
```

```javascript
$('#pagination-here').bootpag({
    pageSize: 10,      // items per page, default: 1
    total: 7,          // total items
    page: 1,            // default page
    maxVisible: 5,     // visible pagination
    leaps: true,         // next/prev leaps through maxVisible
    boundaryLeaps: true   // whether disable next/prev button when page is in the first/last set of pages
}).on("page", function(event, num){
    $("#content").html("Page " + num); // or some ajax content loading...
    // ... after content load -> change total to 10
    $(this).bootpag({total: 10, maxVisible: 10});
});

```
#License

Plugin available under MIT license (See LICENSE file)

Copyright (c) 2013-2015 botmonster.com
