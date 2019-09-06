# Personal-Website-Workshop

This is what the finished website will look like: https://richardg999.github.io.
This is what the finished code should look like: https://github.com/richardg999/richardg999.github.io.

## Setup

1. Install VS Code (or your favorite text editor).
2. Recommended: Download the VS Code extension "Live Server". Click on Extensions button on side panel and search for "Live Server". Live Server automatically refreshes the webpage in the browser every time you save in VS Code. It also provides a handy button at the bottom to launch HTML files.
3. Create a GitHub account if you don't have one already.
4. Install GitHub desktop (or use Git CLI if you already know how).
5. Create a new repository on GitHub. Name it "(github-username).github.io". Initialize it with a README.
6. Then on the respository page, click "Clone or Download">"Open in Desktop".
7. Then launch VS Code. Click "File">"Open Folder" and open the local respository folder you just created (should be named "(github-username).github.io")
8. There should be nothing inside except a README.md file. Now, you will create a new file called "index.html" and another new filed called "style.css". (Right click > "New file" to create new files).
9. Try previewing your file by clicking the "Go Live" button on the bottom bar. You can also preview your file by double clicking the index.html file in file explorer.


## Creating the website

### Adding the basics

1. Add the following code into your index.html file. This creates the basic structure for the website.

        <!DOCTYPE html>
        <html>
        <head>
            
        </head>
        <body>
            
        </body>
        </html>

2. Add the following code into your style.css file. All it does is remove an extra margin that would otherwise appear on your page.

        body {
            margin: 0;
        }

2. Create a title for your page. This title will appear in your browser tab. Add the following code into the `<head>`.

        <title>Richard Guo</title>

3. Add in some meta information. This just tells the browser to make some width adjustments. Add it into the `<head>`.

        <meta name="viewport" content="width=device-width, initial-scale=1.0">

4. Import your CSS stylesheet. Add it into the `<head>`.
        
        <link rel="stylesheet" type="text/css" href="style.css">

4. Now add your name to the file. Add it into the `<body>`.

        <h1>Richard Guo</h1>

5. Preview your file (through Live Server, double clicking index.html, or some other method). You should see your name.
6. Go to GitHub Desktop. Write a short description in the "Summary" text box and click "Commit to Master". Then click "Push origin" on the top right. This will push your code to GitHub. You can now see the code you added in your online GitHub repository. You should also be able to see your site at (github-username).github.io.

### Stylizing your name

1. Now stylize your name. First, we will import a font that we want to use (Montserrat) into the head. Add this code into the `<head>`.

        <link href="https://fonts.googleapis.com/css?family=Montserrat|Source+Sans+Pro" rel="stylesheet">

2. Now put a div element around your heading with the attribute class="name". Then put another div element around that with class="content". In other words, replace `<h1>Richard Guo</h1>` with

        <div class="content">
            <div class="name">
                <h1>Richard Guo</h1>
            </div>
         </div>
    

3. Now in your style.css file, add this code. This stylizes all of the text within the content div.

        .content {
            margin: 18% 20% 0% 20%;
            font-size: 2em;
            text-align: center;
            line-height: 2em;
        }

4. Now in your style.css file, add this code. This stylizes elements with class="name" with the font, font size, color, etc.

        .name {
            font-family: Montserrat;
            text-transform: uppercase;
            font-size: 1.1em;
            line-height: 2em;
            color: #222;
        }

### Adding a resume button

1. Add the following html at the top of the `<body>`, before your name. What this does is it has the word Resum&eacute; in a class called li, which is in a link to "/resume.pdf", which is in a class called "items", and which is in a class called "topbar".

        <div class="topbar">
            <div class="items">
                <a href="/resume.pdf" target="_blank"><div class="li">Resum&eacute;</div></a>
            </div>
        </div>

2. Add the styling. Copy and paste the following code to style.css.

        .topbar {
            display: flex;
            font-family: Source Sans Pro;
            font-size: 1em;
            width: 100%;
            height: 5em;
            line-height: 5em;
            float: top;
            overflow: hidden;
            top: 0;
            position: fixed;
        }

        .items {
            margin: 0 2em;
            width: 100%;
            float: right;
            color: #222;
        }

        .items a {
            text-decoration: none;
            color: inherit;
        }

        .li {
            float: right;
            text-transform: uppercase;
            font-weight: bold;
            text-align: center;
            margin: 0 0.5em;
            display: block;
            letter-spacing: 0.05em;
        }

3. Add a fancy hover effect to the Resume button. This CSS effect will only trigger when the mouse is hovered over the li element.

        .li:hover {
            color: #666;
            transition: color 0.2s ease;
        }

4. Add your resume. Name it resume.pdf and place it into your local respository folder. The Resume button should now work.

### Adding the buttons

1. Import Font Awesome. We will be using Font Awesome for their Mail, GitHub, and LinkedIn icons. Add this to the `<head>`.

        <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css" rel="stylesheet">

2. Add the following html into the content div (`<div class="content">`). This is the html for the buttons. Starting from the inside, it creates a class labeled "fa fa-envelope-o". This class will be replaced by Font Awesome with the appropriate icon (the envelope in this case). Encapsulating that is a link to "mailto:rwguo@andrew.cmu.edu", which is just the link for the button. Around that is a class called "box" will soon stylize the look for each icon.

        <div>
            <span class="box"><a class="s_label" href="mailto:rwguo@andrew.cmu.edu">
                <span class="fa fa-envelope-o"></span></a></span>
            <span class="box"><a class="s_label" href="http://www.github.com/richardg999">
                <span class="fa fa-github"></span></a></span>
            <span class="box"><a class="s_label" href="http://www.linkedin.com/in/rwguo/">
                <span class="fa fa-linkedin"></span></a></span>
        </div>

3. Add the following CSS to style.css. This stylizes the box and the s_label.

        .box {
            margin: 0 0.1em;
            display: inline-block;
            height: 2.7em;
            width: 2.7em;
            line-height: 2.7em;
        }

        .s_label {
            height: 2.2em;
            width: 2.2em;
            line-height: 2.2em;
            display: inline-block;
            border-radius: 50%;
            border-color: #222;
            border-style: solid;
            border-width: 0.04em;
        }

        .box a {
            text-decoration: none;
            color: inherit;
        }


4. Now we will add CSS animations to the buttons. Add the following code within the .s_label block in style.css. This will ease in the button when it appears.

        transition: 0.4s ease;

5. Now add this following code into style.css. This creates a hover effect.

        .s_label:hover {
            height: 2.55em;
            width: 2.55em;
            line-height: 2.55em;
            background-color: #222;
            color: #fff;
            transition: 0.2s ease;
        }

### Adding size adjustments for mobile devices

1. Paste the following code into style.css. This code detects the width of the device screen and adjusts the font size of the name class accordingly. This will optimize the screen for mobile devices.

        @media screen and (max-width: 768px) {
            .name {
                font-size: 1em;
                margin-bottom: 1.5em;
            }
        }

        @media screen and (max-width: 528px) {
            .name {
                font-size: .75em;
                margin-top: 3em;
                margin-bottom: 2em;
            }
        }

### Test it out!

1. Preview your file (through Live Server, double clicking index.html, or some other method). You should see your name.
2. Go to GitHub Desktop. Write a short description in the "Summary" text box and click "Commit to Master". Then click "Push origin" on the top right. This will push your code to GitHub. You can now see the code you added in your online GitHub repository. You should also be able to see your site at (github-username).github.io.
3. You have now finished creating your personal website! Feel free to personalize it however you wish (changing the color, font, adding additional buttons, additional text, etc.).