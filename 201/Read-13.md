## Local storgae 

Before HTML5, data used to be stored in cookies, even in every HTTP request.you can store large data locally using web storage since it's secure and doesn't affect performance which is a way for web pages to store data locally even after uou exit your website or close your browser. Almost every up to date version of browser support web stotage.   

you can use web storage and store data using ` window.localStorage ` , but firstly you have to check if your browser supports it. 
    `
        if (Modernizr.localstorage) {
        // window.localStorage is available!
        } else {
        // no native support for HTML5 storage :(
        // maybe try dojox.storage or a third-party solution
        }
    `

Then using this object you can apply Setitem and assign any value you want as a string only or you may use the bracket notation without any methods. if you wish to retrieve numbers you may use methods such as parseInt. After saving data , you can track them using the storage event

Note: saved data will be as key/pair  and their unit is per origin and the default storag per origin is 5MB. 
