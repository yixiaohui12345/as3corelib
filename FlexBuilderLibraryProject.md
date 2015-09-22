# Introduction #

The following steps will guide you in checking out the soruce code for this project and using it in a new FlexBuilder library project.

# Details #

In order to complete these steps, you must have Subclipse installed.

## Add an SVN Repository location for this project ##

  * In the Window menu, select Show View -> Other
  * Expand SVN and select SVN Repository, then click OK
  * Right click in the SVN Repository view and select New -> Repository location...
  * Enter the SVN Repository for this project: http://as3corelib.googlecode.com/svn/trunk/
  * Click Finish

## Check out the code from the project into the Flex Library Project ##

  * Right click on the repository location you added in the previous step, and select Checkout...
  * Select "Check out as a project configured using the New Project Wizard" and click Finish
  * Expand the Flex folder, select Flex Library Project, and click Next
  * Name the project after this library (in this case, as3corelib), and select the directory where the source code will be placed (or, you can just use the default directory there, under the current workspace).  Click Finish.

## Configure the project to include the proper classes in the .swc output file ##

After the code is checked out from the previous step, you need to modify the project so that it knows what classes to include in the output .swc file.

  * Right click on the project that you just created in FlexBuilder and select Properties
  * Select Flex Library Build Path
  * In the "Main Source Folder" field, type in "src"
  * Under the Classes tab, select the "src" folder to include everything.  Alternatively, you can pick and choose what classes you want.
  * Click OK

When the dialog closes, the project will be built and you'll have the projects .swc file placed in the default "bin" output directory.

Note that if the project has any dependencies, the compilation might fail after selecting which classes to include.  After resolving the dependencies or changing which classes are included, a successful compilation will produce the .swc file.

In the case of as3corelib, you'll need FlexUnit to compile because of the unit tests.  An alternative is to simply uncheck all of the "tests" packages in the Flex Library Build Path options.  In the future, we'll be moving "tests" into their own separate source folder to avoid this hassle.

## Updating the project code ##

To get the latest code from SVN, right click on the project, and select Team -> Update


