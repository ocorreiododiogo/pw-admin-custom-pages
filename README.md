# Admin Custom Pages Module for ProcessWire 
###((dev version))

((IMPORTANT))  
For upgrading to this version you need to replace, both, the module file and the admin.php file in the templates folder.

### Create custom admin pages easily without having to build a Process Module.
 
The new version of this module works better with the current DEV version of PW, 
but also works with the stable version. Differences are explained bellow.

Since cersion 1.0.4 the installation process automaticaly replaces the default admin.php file in the templates folder by the provided one and creates a new field called "ACP_scripts_and_styles". This functionality was added by [Pete](https://github.com/Notanotherdotcom)

**Note:** If you (or a module) already customised the admin.php file before, make a backup of that file, and add the custom code to the newly created admin.php. 

### To prepare the module:

1. Place the module folder in /site/modules/
2. Install the module in the modules page from the admin

### To create the pages:

*In the current PW stable version*

1. Create a new template **without** a file (name it whatever you wish)
2. In the advanced settings insert "admin" as the Alternate Template Filename
3. Create a new page under "Admin" and give it the newly created template
4. create a page as children and give it any template (this is the template that will be rendered in the admin page. For use with a theme that uses dropdown menus, set this page to "hidden" in the settings tab)
5. In this template file you can use PW variables as in any normal template
  
--

*In the current PW DEV version*

1. Create a new template **with a file** (name it whatever you wish)
2. In the advanced settings insert "admin" as the Alternate Template Filename
3. Create a new page under "Admin" and give it the newly created template
4. Doesn't exist ;)
5. In the template file you can use PW variables as in any normal template (yes, pretend you didn't change the file in the settings)

### To add custom script and style files to the page:

1. Add the "ACP_scripts_and_styles" to the page template (the field that was created automaticaly on instalation)
2. Add the .js and .css URLs in this field textarea, one in each line. can be absolute or relative (relative is assumed from the site root on eg: site/templates/styles/my.css)

--

#### ((NEW))
### To create a tab in the admin for editing a page – example: a "settings" page:

1. Create a template **without a file**
2. In the advanced settings insert "admin" as the Alternate Template Filename
3. Create a new page under "Admin" and give it the newly created template
4. Don't create children pages from that page

In short: if there isn't a file with the name of the template and the page has no children, it's assumed that this is an "edit page"

--

### Troubleshooting:

> This page has no Process assigned.

If you are greeted with this message after creating a custom admin page, verify that the /site/templates/admin.php file was modified during the installation process.
If the file in your template folder is not similar to the one packed with the module, replacing it should solve the problem.

The particular lines to look for are from:

    // code inside the condition added for the Custom Admin Pages Module
   
to:
   
    // end of code for the Custom Admin Pages Module



--

Module home: http://modules.processwire.com/modules/process-admin-custom-pages/

Support forum: http://processwire.com/talk/topic/3474-admin-custom-pages-module/

--

That's it! Hope you enjoy the module :)
