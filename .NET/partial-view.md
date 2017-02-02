#Pass ViewBag to Partial View

```cs
// Index.cshtml
@{ 
    Html.RenderPartial("_PartialView", (string)ViewBag.Partner);
}

// _PartialView.cshtml

@model string

<p>String: @Model</p>
```