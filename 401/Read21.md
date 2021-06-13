# Django Models
- Django web applications could access and manage data through Python objects referred called models. 
- Models define the structure of stored data, including the field types and possibly also their maximum size, default values, selection list options, help text for documentation, label text for forms, etc


	
### Model primer
- Models are usually defined in an application's models.py file. They are implemented as subclasses of
`django.db.models.Model`, and can include fields, methods and metadata. 

The code below shows a "typical" model, named `MyModelName`:

        ```
        from django.db import models
        class MyModelName(models.Model):
            """A typical class defining a model, derived from the Model class."""
            # Fields
            my_field_name = models.CharField(max_length=20, help_text='Enter field documentation')
            ...
            # Metadata
            class Meta:
                ordering = ['-my_field_name']
            # Methods
            def get_absolute_url(self):
                """Returns the url to access a particular instance of MyModelName."""
                return reverse('model-detail-view', args=[str(self.id)])
            def __str__(self):
                """String for representing the MyModelName object (in Admin site etc.)."""
                return self.my_field_name
        ```

	
### Fields
- A model can have an arbitrary number of fields, of any type — each one represents a column of data that we want to store in one of our database tables.

    `my_field_name = models.CharField(max_length=20, help_text='Enter field documentation')`
    
- Our above example has a single field called `my_field_name`, of type `models.CharField` — which means that this field will contain strings of alphanumeric characters. 
- The field types are assigned using specific classes, which determine the type of record that is used to store the data in the database.
- The field types can also take arguments that further specify how the field is stored or can be used. In this case we are giving our field two arguments:
- `max_length=20` — States that the maximum length of a value in this field is 20 characters.
- `help_text='Enter field documentation'` — provides a text label to display to help users know what value to provide when this value is to be entered by a user via an HTML form.

# Django admin site
- The Django admin application can use your models to automatically build a site area that you can use to create, view, update, and delete records.
- This could save you a lot of time during development, making it very easy to test your models and get a feel for whether you have the right data.
- The admin application can also be useful for managing data in production, depending on the type of website.

	
## Registering models 
First, open admin.py in the catalog application (/locallibrary/catalog/admin.py)- It currently looks like this — note that it already imports

        `django.contrib.admin`:
        `from django.contrib import admin`

Register the models by copying the following text into the bottom of the file. This code imports the models and then calls `admin.site.register` to register each of them.

        ```
        from .models import Author, Genre, Book, BookInstance
        admin.site.register(Book)
        admin.site.register(Author)
        admin.site.register(Genre)
        admin.site.register(BookInstance)
        ```
