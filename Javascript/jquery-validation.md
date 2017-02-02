#jQuery Validation
[jQUery Validation Documentation](https://jqueryvalidation.org/documentation/)

##Extend jquery range validator to work for required checkboxes

* Asp.Net Core, Tag helpers, jquery Validation, Data Annotations
* [See more: ASP.NET MVC - Required Checkbox with Data Annotations](http://jasonwatmore.com/post/2013/10/16/aspnet-mvc-required-checkbox-with-data-annotations)

```html
<!-- Index.cshtml -->
<div class="small-12 medium-12 column">
    <div class="form-group">
        <input asp-for="Checkbox" />
        <label asp-for="Checkbox">This checkbox has to be ticked!</label>
    </div>
</div>

<!-- Html outcome -->
<div class="small-12 medium-12 column">
	<div class="form-group">
		<input  data-val="true" 
		        data-val-range="This field is required" 
                data-val-range-max="True" 
                data-val-range-min="True" 
                data-val-required="The Terms Accepted field is required." 
                id="Checkbox" 
                name="Checkbox" 
                type="checkbox" 
                value="true">
		<label class="fw-normal" for="TermsAccepted">This checkbox has to be ticked!</label>
		<span class="field-validation-valid" data-valmsg-for="Checkbox" data-valmsg-replace="true"></span>
	</div>
</div>
```

```cs
// FormViewModel.cs
[Display(Name = "Checkbox")]
[Range(typeof(bool), "true", "true", ErrorMessage = "Required")]
public bool Checkbox { get; set; }

```

```js
// Extend jquery range validator to work for required checkboxes
var defaultRangeValidator = $.validator.methods.range;
    $.validator.methods.range = function (value, element, param) {
        if (element.type === 'checkbox') {
            // if it's a checkbox return true if it is checked
            return element.checked;
        } else {
            // otherwise run the default validation function
            return defaultRangeValidator.call(this, value, element, param);
        }
    }
});
```