# Admin Custom Pages Module for ProcessWire

### Create custom admin pages easily without having to build a Process Module.
 
The new version of this module works better with the current DEV version of PW, 
but also works with the stable version. Differences are explained bellow.


### To prepare the module:

1. Install the module by placing the module file in /site/modules/
2. Replace the /site/templates/admin.php that comes with your pw install, by the provided file with the same name.
3. Create a new textarea field named "ACP_scripts_and_styles"

### To create the pages:

*In the current PW stable version*

1. Create a new template **without** a file (name it whatever you wish)
2. In the advanced settings insert "admin" as the Alternate Template Filename
3. Create a new page under "Admin" and give it the newly created template
4. create a page as children and give it any template (this is the template that will be rendered in the admin page)
5. In this template file you can use PW variables as in any normal template
  
--

*In the current PW DEV version*

1. Create a new template **with** a file (name it whatever you wish)
2. In the advanced settings insert "admin" as the Alternate Template Filename
3. Create a new page under "Admin" and give it the newly created template
4. Doesn't exist ;)
5. In the template file you can use PW variables as in any normal template (yes, pretend you didn't change the file in the settings)

### To add custom script and style files to the page:

1. Add the "ACP_scripts_and_styles" to the page template (the one created on point 1. of the previous instructions)
2. Add the .js and .css URLs in this field textarea, one in each line
  

--

That's it! Hope you enjoy the module :)
