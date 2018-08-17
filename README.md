# cellprofiler.github.com

## development
1. Ensure `ruby` is installed on your system. For OS X, use `homebrew`:
    ```sh
    brew install ruby
    ```

1. Install project dependencies:
    ```sh
    bundle install
    ```

1. Start the local server
    ```sh
    bundle exec jekyll serve
    ```

## documentation
1. How to create a new page
  - To create a new page on the website, you must first render the website locally and then open the website through your preferred text editor (e.g. Atom, Visual Studio, etc.).
  - Then create a new folder and name the folder whatever you want the path name of the web page to be.
  - Then create a file inside the folder called “index.md” (this creates the file in markdown but you can also call it “index.html” if you want in html).
  - If there will be more than one file in the folder, the base file that will have the introduction to the topic of the new page will always be called “index.(file type)” and other sub pages about it can be called anything you want, generally having something to do with what they are about but in only up to a few words long.

1. How to edit a current page
  - To edit a page that already exists, repeat the same first step from the instructions above and then simply edit and save (using command+S) the file(s) you want.
  - It is also useful to know that in order for changes to show up on the locally rendered website, the file in the text editor must be saved, you must reload the page on the local render, and you must make sure that there are no errors occuring in the saving of the file by checking the command line which is running the locally rendered website.

1. How and when to create a template/include
  - An include should be used if a page has a structure which has a repeating layout of text/image/links (e.g. look at /examples page) or a page which has a very unique structure which would benefit from being segmented (e.g. look at /supportplan page).
  - To create an include, you must first create two new files; one new .yml file in the /\_data folder and a .html file in the /\_includes folder and name them in relation to the file they will be used for (e.g. if an include is only going to be used for a page called /information, name the include file information.html and the data file information.yml) or their formatting purpose (e.g. if an include file is only for creating a table, name it something about what kind of table it makes such as striped_table.html and .yml).
  - First, to call an include in the file you want, you type in '{% include file_name.html %}' where 'file_name.html' is the name of the file in the /\_includes folder you want to correspond to the current page.
  - The include file (.html) is the file where all of the structure of the repetition/segmentation is and the data file (.yml) is where all of the actual information being shown on the page is.
  - The data file (.yml) works in a basic yml file way where you define variables and then put the corresponding information to that variable after it. The format for the first row is '- variable: information' with all of the latter variables in the same group being the same except replacing the - with another space to create a normal indentation. In yml files, the - signifies one group of data with every variable until the next - to be grouped together for one iteration of the for loop being used in the include file (.html). The include file (.html) works in a normal html file way, however, there will be a for loop inside of it for calling the data file (.yml). (__Note:__ If your 'information' in the data file has one or more colons (:) in it, you need to put a greater than sign (>) after the variable and then put the information on a new line underneath the variable with one more indentation. Look at /\_data/citations for an example on this website)
  - The for loop is written similar to the include line written in the corresponding .md file: '{% for variable_name in site.data.file_name %}' where 'variable_name' is some random variable name you come up with which will be used in this include file (.html) for calling the variables in the data file (.yml).
  - To call a variable from the data file (.yml) in the include file (.html), the format is '{{variable_name.variable}}' where 'variable_name' is the random name you came up with in the for loop in this include file (.html) and 'variable' is the name of the variable you created in the data file (.yml) which corresponds to the data you want to have in the location you entered '{{variable_name.variable}}'. If you want to create an include of which the only purpose is a formatting style, such as a striped table, in the include file's (.html) for loop, instead of typing 'site.data.file_name', you write 'include.style_name' where 'style_name' is a random variable you create which would then be given a value in the actual calling of the include in the .md file (e.g. {% include information.html table=site.data.information %} with the for loop in 'information.html' being {% for info in include.table %}. To see an example of this on this website, go to the /previous_releases/index and /\_includes/previous_releases files).
  - https://getbootstrap.com/docs/4.0/layout/grid/ for information on grid layout for text/image formatting (e.g. making columns and centering text).
  - https://jekyllrb.com/docs/includes/ for information on includes. The very bottom of the page has the information you need when trying to use one include for different pages (e.g. when you want two pages have two different tables and you want one include that you can call on each page that can take from two different data sources and make two different tables without having to manually write the html table with the corresponding data on both pages. Refer to /previous_releases/index and /\_includes/previous_releases for an example of how to do this on this website).

1. How to edit/add css styling
  - The page currently being used as the css styling database for this website is /css/app.css. To add a new entry/styling to the file, you enter '.style_name {}' where 'style_name' is the random name you create to correspond to this style when calling it in the future. Then, you press enter in between the curly braces which should put the end curly brace two lines below the open curly brace which you then enter the css styling code in between them with one indentation. To call the css styling on a page, you have to use html code and enter the 'style_name' in a class definition (e.g. <div class="style_name"></div>). (__Note:__ The 'style_name' referred to in this paragraph is not related to the 'style_name' used in the above paragraph about templates/includes)
