# DevTools  

## Table of contents  
- [Chrome DevTools](#chrome-devtools---google-developers)  
- [Umar Hansa - "Dev Tools" Newsletter](#umar-hansa---dev-tools-newsletter)  
- [Other](#other)  
- [Snippets](#Snippets)  

## [Chrome DevTools](https://developers.google.com/web/tools/chrome-devtools/) - Google Developers  
- [Local Overrides](https://developers.google.com/web/updates/2018/01/devtools#overrides)  

## [Umar Hansa](https://umaar.com/) - "Dev Tools" Newsletter  
- [Copy and extract all the CSS for an element on the page](https://umaar.com/dev-tips/201-extract-element-styles/) - (8/11/2019)
- [Quickly clear all the data from a website](https://umaar.com/dev-tips/197-clear-site-data/) - (4/9/2019)  
- [The five most popular DevTools tips from 2018](https://umaar.com/dev-tips/190-five-popular-2018-tips/) - (1/8/2019)  


## Other  

- [Getting creative with the Console API!](https://areknawo.com/getting-creative-with-the-console-api/)  
  by [Areknawo](https://areknawo.com/) (4/6/2019)  
- [A list of cool Chrome DevTools Tips and Tricks](https://flaviocopes.com/chrome-devtools-tips/#drag-and-drop-in-the-elements-panel)  
  by [Flavio Copes](https://flaviocopes.com/) (3/20/2018)  

- [Improve Your Debugging Skills with Chrome DevTools](https://www.telerik.com/blogs/improve-your-debugging-skills-with-chrome-devtools)  
  by [Telerik](https://www.telerik.com/) (3/21/2018)  

- [Console cheat sheet for JavaScript developers](https://levelup.gitconnected.com/console-cheat-sheet-for-javascript-developers-21f0c49604d4) by [Javascript Jeep](https://levelup.gitconnected.com/@jagathishsaravanan) (11/2019)

## Snippets
---
    // LIST SELECT VALUES
    $("select").each(function(){
        console.log($(this).attr('value'));
    });

    // LIST SELECT ID's
    $("select").each(function(){
        console.log($(this).attr('id'));
    });

    // LIST TEXT FROM SELECTED OPTIONS 
    $("select option:selected").each(function(){
        console.log($(this).text());
    });

    //LIST ID/VALUE/TEXT OF ALL SELECT ELEMENTS
    $("select").each(function(){
        console.log($(this).attr('id') + ' = ' + $('option:selected',this).val() + " = " +$('option:selected',this).text());
    });

    // LIST ID/VALUE OF ALL SELECT ELEMENTS
    $("select option:selected").each(function(){
        console.log($(this).attr('id') + ' = ' + $(this).val() );
    });

    // LIST HREF LINK WITH THE TITLE OF THE SPAN
    $("a").each(function(){
        console.log($(this).attr('href') + ' = ' + $("span",this).attr("title") );
    });


    // 7/22/2019
    // LIST SELECTED PARAMETERS - COPY FRIENDLY
    item = "";
    $("select").each(function(){
        item = item + $(this).attr('id') + ' = ' + $('option:selected',this).val() + " = " +$('option:selected',this).text()+"\n";
    });
    console.log(item);

    // 7/22/2019
    // LIST SELECTED PARAMETERS - COPY FRIENDLY
    item = "R: " + $('h2').text() + "\nPARAMETERS USED TO RUN R:\n";
    $("select").each(function(){
        item = item + "\t"+$(this).attr('id') + ": " +$('option:selected',this).text()+"\n";
    });
    item = item.replace('PId','Product');
    item = item.replace('RPSystems_0__IpmPSystemId','P System');
    item = item.replace('RType','R Type');
    item = item.replace('RPStartDate','R P Start Date');
    item = item.replace('RPEndMonth','R P End Month');
    item = item.replace('RPEndYear','R P End Year');
    item = item.replace('RRunMonth','R P');
    item = item.replace('RRunYear','R Year');
    item = item.replace('HRunOut','HC Run Out');
    item = item.replace('HMMYear','HM Year');
    console.log(item);

    // 7/23/2019
    // GET ALL CONFIG
    item = "R: " + $('h2').text() + "\nPARAMETERS USED TO RUN R:\n";
    $("div.inputGroup div select").each(function(){
        item = item + "\t"+$(this).attr('id') + ": " +$('option:selected',this).text()+"\n";
    });
    // item = item.replace('PId','Product');
    // item = item.replace('RPSystems_0__IpmPSystemId','P System');
    // item = item.replace('RType','R Type');
    // item = item.replace('RPStartDate','R P Start Date');
    // item = item.replace('RPEndMonth','R P End Month');
    // item = item.replace('RPEndYear','R P End Year');
    // item = item.replace('RRunMonth','R P');
    // item = item.replace('RRunYear','R Year');
    // item = item.replace('HRunOut','H C Run Out');
    // item = item.replace('HMYear','H M Year');
    console.log(item);



    $("form input:checkbox").each(function(){
        console.log($(this).attr('value'));
        });
---
    // PLUS ONE MINUS ONE QUALITY REPORT
    $("#ProductId option[value='100000']").attr("selected","selected").change();

    $("#ReportProviderSystems_0__IpmProviderSystemId option[value='100000']").attr("selected","selected").change();

    $("#ReportType option[value='1']").attr("selected","selected").change();

    $("#ReportRunMonth option[value='3']").attr("selected","selected").change();

    $("#ReportRunYear option[value='2017']").attr("selected","selected").change();

    // UNCHECK ALL CHECKBOXES
    $("input").prop('checked', false); 

---

    // jQuery REMOVE ERROR
    $("div").removeClass("has-error");

    // RUN CDP Incentive Reports
    $('#frmReport').submit();  

-------


