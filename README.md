# Thanks Coffee & Sangas Webapp
## Link: https://ligmaleng.pythonanywhere.com
## Description:
The python app runs a webpapp for my regular local sandwich shop(Thanks Coffee and Sangas) with the flask framework. The pages include a home page and layout extension(about, menu, and info) pages described below. The html pages were also designed with viewport reactivity in mind, having different css styles for when the viewport width changes. The design theme remains consistent with the shop design which reflects the 90s vibe that the owners grew up with.
## Video Demo:  https://www.youtube.com/watch?v=zsQ6iCIi9Z4
# Page Description
## [HOME](templates/index.html):
Contains a large main logo for Thanks with a collapsable navbar made using bootstrap with custom javascript to tweak the [ SELECT ] button to disable itself while the navbar opens and closes in sync with the collapsing animation time, and change it's text to [ CLOSE ] simultaneously. This was implemented because without the button disabling the text might change without the collapsing animation completing so it might show the wrong collapse state.
The rest of the navbar contains a dropdown list to navigate to the remaining web pages: About, Menu, Info.\
The footer of the page contains the address of the shop and a button linking to their instagram page. It is contained in a css flex container the changes its flex direction from row to column to stack the child elements on top of each other if the viewport width is too small.
## [LAYOUT](templates/layout):
HTML template for the non-home pages that contain the same navbar as the homepage but re-positioned and logo resized. The layout has jinja blocks that will plug in the html head title, re-arrange the navbar listing to remove the current pages selection, and the body of the page.
## [ABOUT](templates/about.html):
Extends the layout template and contains some information about the shop in a scrollable division styled in a retro desktop window. The desktop window concept is used as the background in multiple colours following the shop design theme, with an image of the sibling co-owners Gus and Giselle in fron of their store to introduce them in a shifting image animation that changes from a bright daylight image to the same image edited to show a neon backgroumd, the transition form one image to the other is achieved with some css.
## [MENU](templates/menu.html):
Extends the layout template and displays the menu of the shop on a pink wall. The menus are made with tables for easy positional formatting and is in the style of a letter board with contrasting shadows applied to both the table and the font to achieve a depth effect.
## [INFO](templates/info.html):
Extends the layout template and contains a division with an embedded google map marked at the shops location, below the map it displays the shops address and their opening hours . The bottom on the page also contains a button to their instagram page.
# app.py:
Python code that imports a few packages from the flask library, and uses flask decorators to route requests for the pages to render the relative html templates and html files.
