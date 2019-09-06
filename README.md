# Personal-Website-Workshop

## Setup

1. Install VS Code (or your favorite text editor).
2. Recommended: Download the VS Code extension "Live Server". Click on Extensions button on side panel and search for "Live Server".
3. Create a GitHub account if you don't have one already.
4. Install GitHub desktop (or use Git CLI if you already know how).
5. Create a new repository on GitHub. Name it "(github-username).github.io". Initialize it with a README.
6. Then on the respository page, click "Clone or Download">"Open in Desktop".
7. Then launch VS Code. Click "File">"Open Folder" and open the local respository folder you just created (should be named "(github-username).github.io")
8. There should be nothing inside except a README.md file. Now, you will create a new file called "index.html" and another new filed called "style.css". (Right click > "New file" to create new files).
9. Try previewing your file by clicking the "Go Live" button on the bottom bar. You can also preview your file by double clicking the index.html file in file explorer.

        <link href="https://fonts.googleapis.com/css?family=Montserrat|Source+Sans+Pro" rel="stylesheet">
        <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css" rel="stylesheet">

        <div class="topbar">
        <div class="items">
        <a href="/resume.pdf" target="_blank"><div class="li">Resum&eacute;</div></a>
        </div>
        </div>

        <div class="content">
        <div class="name">
            <h1>Richard Guo</h1>
        </div>
        <div>
            <span class="box"><a class="s_label" href="mailto:rwguo@andrew.cmu.edu">
                <span class="fa fa-envelope-o"></span></a></span>
            <span class="box"><a class="s_label" href="http://www.github.com/richardg999">
                <span class="fa fa-github"></span></a></span>
            <span class="box"><a class="s_label" href="http://www.linkedin.com/in/rwguo/">
                <span class="fa fa-linkedin"></span></a></span>
        </div>
         </div>

         
        
        



## Creating the website

1. Add the following code into your index.html file. This creates the basic structure for the website.

        <!DOCTYPE html>
        <html>
        <head>
            
        </head>
        <body>
            
        </body>
        </html>

2. Create a title for your page. Add the following code into the `<head>`.

        <title>Richard Guo</title>

3. Add in some meta information. This just tells the browser to make some width adjustments. Add it into the `<head>`.

        <meta name="viewport" content="width=device-width, initial-scale=1.0">

4. Import your CSS stylesheet. Add it into the `<head>`.
        
        <link rel="stylesheet" type="text/css" href="style.css">

4. Now add your name to the file. Add it into the `<body>`.

        <h1>Richard Guo</h1>

5. Preview your file (through Live Server, double clicking index.html, or some other method). You should see your name.
6. Go to GitHub Desktop. Write a short description in the "Summary" text box and click "Commit to Master". Then click "Push origin" on the top right. This will push your code to GitHub. You can now see the code you added in your online GitHub repository. You should also be able to see your site at (github-username).github.io.


