#Re-apply listeners to DOM elements

If object is dynamicaly generated we need to apply listeners again. With Foundation this is done by creating a new instance of an object (e.g. Accordion):

* Foundation.Accordion - Creates a new instance of an accordion.
* var elem = new Foundation.Accordion(element, options);

###Example
```js
$(element).on("click", function () {
	$.get(URL)
	  .done(function (data) {
		  var list = data.list;

		  $.each(list, function (i, val) {
			  $("#accordion")
				  .append('<li class="accordion-item" data-accordion-item>'
				  + '<a href="#" class="accordion-title">' + val.title + '</a>'
				  + '<div class="accordion-content" data-tab-content>' + val.body + '</div></li>');
		  });
		  var accordion = new Foundation.Accordion($('#accordion'));
	  });
});
```