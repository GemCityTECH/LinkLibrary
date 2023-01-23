# Razor Methods - IsSectionDefined()  

## IsSectiondDefined() 
You can use this method to inspect whether a section has been defined in the referring view and act accordingly.

**_Layout.cshtml**
~~~
@Scripts.Render("~/bundles/jquery")
@* @RenderSection("scripts", required: false) *@
@if (IsSectionDefined("scripts"))
{
  @RenderSection("scripts")
}
@
~~~

**_LayoutWithSidebar.cshtml**
~~~
@section Featured {
  @RenderSection("Featured", required: false)
}

@section Scripts {
  @RenderSection("Scripts", required: false)
}

<div class="sidebar">
  @RenderSection("sidebar")
</div>

<div class="content">
  @RenderBody()
</div>


~~~

**Index.cshtml**  
~~~
@section Featured {
  <section class="Featured">
    <div class="content-wrapper">
      This is some featured content!
    </div>
  </section>
}

@section Scripts {
  <!-- This content will be rendered in the Scripts section -->
}
~~~
