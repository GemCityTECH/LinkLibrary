# ASP.NET / MVC

## MVC Rules
  - Controllers are the only component that should ever create an instance of a model  
  - ASP.NET MVC is a stateless architecture, that means it does not generally transmit any information other than form post values in between requests.
---
## [ViewData VS ViewBag Vs TempData in MVC](https://www.c-sharpcorner.com/blogs/viewdata-vs-viewbag-vs-tempdata-in-mvc1)

- **TempData**
  - TempData is a dictionary which is derived from TempDataDictionary class. TempData is stored data just like live session for short time. TempData keeps data for the time of HTTP Request, which means that it holds data between two consecutive requests. TempData helps us to transfer data between controllers or between actions. TempData internally use Session variables. Note that TempData is only work during the current and subsequent request. It is generally used to store one time messages. With the help of the TempData.Keep() method we can keep value in TempData object after request completion.  
  
- **ViewData** / **ViewBag**  
  - ViewData and ViewBag are used for the same purpose --  to transfer data from controller to view.  ViewData is nothing but a dictionary of objects and it is accessible by string as key. ViewData is a property of controller that exposes an instance of the ViewDataDictionary class. ViewBag is very similar to ViewData. ViewBag is a dynamic property (dynamic keyword which is introduced in .net framework 4.0). ViewBag is able to set and get value dynamically and able to add any number of additional fields without converting it to strongly typed. ViewBag is just a wrapper around the ViewData.  
---

## [Tutorial: Read related data with EF in an ASP.NET MVC app](https://docs.microsoft.com/en-us/aspnet/mvc/overview/getting-started/getting-started-with-ef-using-mvc/reading-related-data-with-the-entity-framework-in-an-asp-net-mvc-application)  
  posted on January 21, 2019  

## [Grouping data with LINQ and MVC](https://ole.michelsen.dk/blog/grouping-data-with-linq-and-mvc.html)  
  Article by Ole Michelsen posted on November 20, 2011  
  
  Create a list in a controller:  
  
  ```
  using System.Collections.Generic;
  using System.Linq;
  using System.Web.Mvc;
  using LinqGrouping.Models;
  
  namespace LinqGrouping.Controllers
  {
      public class GroupingController : Controller
      {
          public ActionResult Index()
          {
              var books = new List<Book>();
  
              // Add test data
              books.Add(new Book { Author = "Douglas Adams", Title = "The Hitchhiker's Guide to the Galaxy", Genre = "Fiction", Price = 159.95M });
              books.Add(new Book { Author = "Scott Adams", Title = "The Dilbert Principle", Genre = "Fiction", Price = 23.95M });
              books.Add(new Book { Author = "Douglas Coupland", Title = "Generation X", Genre = "Fiction", Price = 300.00M });
              books.Add(new Book { Author = "Walter Isaacson", Title = "Steve Jobs", Genre = "Biography", Price = 219.25M });
              books.Add(new Book { Author = "Michael Freeman", Title = "The Photographer's Eye", Genre = "Photography", Price = 195.50M });
  
              // Group the books by Genre
              var booksGrouped = from b in books
                                 group b by b.Genre into g
                                 select new Group<string, Book> { Key = g.Key, Values = g };
  
              return View(booksGrouped.ToList());
          }
      }
  }
  ```  
  
  
  The grouping is handled with the LINQ group by statement, and here we choose the Genre field as our key to group by. Now we select our subsets into the Group object, which will consist of a key and a collection of each book which matches this key. The end result is a List<Group<string, Book>>, which makes it easy for us to output as HTML:  
  ```
  @using LinqGrouping.Models
  @model List<Group<string, Book>>
  
  @{
      ViewBag.Title = "LINQ Grouping";
  }
  
  <h2>Grouping books by Genre</h2>
  
  <table>
  <thead><tr><th>Author</th><th>Title</th><th>Price</th></tr></thead>
  <tbody>
  @foreach (var group in Model)
  {
      <tr><th colspan="3">@group.Key</th></tr>
      foreach (var book in group.Values)
      {
          <tr><td>@book.Author</td><td>@book.Title</td><td>@book.Price.ToString("c")</td></tr>
      }
  }
  </tbody>
  </table>
  ```  
  
