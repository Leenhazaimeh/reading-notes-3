# IMAGES 

images are an essential part of any website, you can include your images easily using ` <img> ` tag specifying the path for the image withing `src` attribute, Most of images have width and height attributes to specify the dimension for the image,you should also include your `alt` attribute to help SEO identify your website as we will discuss later on in the SEO sction. 

you can add images not only using HTML tags, but using CSS as well, any box in your HTML can be given a ` background-image  ` property in CSS that refers to it, then include the value of the image by url path. since that can be done, there are many properties are used to control this image which will set as a background for that element such as: ` background-repeat ` that will help you repeating the image over your element if it's has an extra space , you can also repeat it over only x-axis or y-axis. 

Another property like ` background-position ` lets you make the image as cover to fill all space in the box , or you can specify the side that you will be showing if it's not fitting in , maybe you'll include them as pixels of the photo or top right , left bottom to specify the part than you want to emphasize. The `background-attachment` property specifies whether a background image should stay in one position or move as the user scrolls up and down the page. It can have one of two values fixed pr scroll.

you can use a shorthand for the background property that will make your life easier and include allof these values inside it. 


# Practical Information 

we will divide these ection into 3 , the first is about SEO (search engine optimization) which is a huge topic on its own but we will include the basics for it , the second about how to collect and analyze info about your site visitors and finally we will discuss the basics of getting your website online. 

### SEO 

SEO is a way for letting your site appear on the top ofsearch engines, before dig into that we have to know how they collect info from your site.

we will start by the order of their importance, which is the 
1. **title** included in your HEAD for that page, it should be a strong keyword that relevant to what your website is all about and the service or products you offer. 
2. your **HEADINGS** especially h1,h2 all the way to h6.
3. your main **text** should include keyword relevant to your website 
4. **text inside anchor ` <a> ` tags** 
5. **text in alt attribute for images**  
6. your **description for the page in your meta tag in the <HEAD>**

Once you know that these mentioned above are the most critical things for you SEO, you start searching for the most keywords to your site, eitehr by searching the web or whatever you see most relevant to you. the idea from researching is to know the most keywords in your market and to avoid as much as you can the most competitive keywords, after you do ,organize your list and try to include them in your page as mentioned above without over-repeating them to make it human readable and not to look dumb and vague. your a tags also should include meanningful text rather than using click here or go here texts!

## Collection info about your site

this is almsot done using third-party tools like google analytics by signing up a new account and they will track these imortant info about your visitor by the links they provided you with in the HEAD of the page. 

Using the interface they gave to you, you can now track the most visited pages , number of visitors , where they came from if it's a direct link or from a specific site, most kickoff pages and many more that will help you improve your website. you are most likely have to take a tutorial to demonstarate this skill and use it to your advantage. 

## Getting the website online

to get your site online you need a domain name that will direct to your site and you get this by usually paying annual fee to these domain names providers , after you achieve this you need a server which is a computer that always connected to interent to stroe your files on, barrign some exceptions for huge tech companies this can be achieved by purchasing one from web hosting companies like : AWS or digital ocean. they will charge you depending on the bandwith you use, the storage they provide and many others features such as: 24/7 support, backups, emails domain etc. 

Remeber to do your researches and check reviews about companies you want to deal with to make sure that you get what you need without extra cost, you should also specify type of hosting you wish to get because there are multiple types you may need regarding the use of your website. 

When you reserve that web server , it comes wih FTP which is a client side progarm with username and passowrd that lets you download and upload files easily from and to your local machine to that hosted web server. 

________ 

# Flash 

it's an old way that still used in web world to add animations, videos,audios to your website. by the way it's considered obsolete now and has been replaced with ` <audio > ` and ` <video> ` tags that released on 2010 

The most popular way of adding flash into a web page is using JavaScript. it will be sth like this: 

``` 
            <!DOCTYPE html>
        <html>
        <head>
        <title>Adding a Flash Movie</title>
        <script type="text/javascript"
        src="http://ajax.googleapis.com/ajax/libs/
        swfobject/2.2/swfobject.js"></script>
        <script type="text/javascript">
        swfobject.embedSWF("flash/bird.swf",
        "bird", "400", "300", "8.0.0");</script>
        </head>
        <body>
        <div id="bird"><p>An animation of a bird taking
        a shower</p></div>
        </body>
        </html>

``` 

