# Admin Custom Pages Module for ProcessWire

### Create custom admin pages easily without having to build a Process Module.
 
The module does something very simple. This is a process that you can assign to any page that has the "admin" template, and renders another page inside the admin template. I chose to render the page that is children of this custom admin page.

So, how to create a new admin page?

1. Install the module

2. Create a new page under "Admin" with the "admin" template, and assign to it the "ProcessAdminCustomPages" process (there will be a new link on the admin nav)

3. Create new page as children of that one with any template that you want (This will work as any normal page, and in the template file you can use normal PW variables as $page)
 
4. Go to the new link in the admin and see what happens

### To load sccripts and styles

To load JS and CSS files for each template, create a folder with the same name as the rendered page template inside the scripts and styles folders (defaults to the folders that come by default with PW but you can change it in the module settings to suit your needs) and place inside them any number of .js and .css files (.js files in the scripts folder and .css files in the styles folder). they will all be loaded.
