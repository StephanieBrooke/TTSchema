# TTSchema

Issues with Webflow character limit - 

Just follow these steps:

Make a new repository (call it whatever you like) and make it public

Choose ‘create new file’

Copy your HTML and then paste the code into the new file.

Name your file and add the extension .html (for example [repositoryname]/mycode.html)

Click ‘commit new file’

In your repository, open your file, and then click ‘raw’

Copy the URL of the RAW format, it should, look like this:

https://raw.githubusercontent.com/username/respositoryname/master/filename.html

Go back to your Webflow page where you require the HTML and add a custom code block.

Add the following code to your custom code block:
<div id="ajaxContent"></div><script> var Webflow = Webflow || []; Webflow.push(function() { $.get('YOUR COPIED LINK HERE', function(data) { $('#ajaxContent').append(data); }); }); </script>

Paste your copied RAW url into the ‘YOUR COPIED LINK HERE’ section, and then press save.

Publish your website and test.



Just to add for others who might run into problems when using this script to insert multiple HTML embeds. Make sure you use different id´s in the script, since the script is appending data into the embed (ajaxContent).

<div id="ajaxContent01"></div><script> var Webflow = Webflow || []; Webflow.push(function() { $.get('YOUR COPIED LINK HERE', function(data) { $('#ajaxContent01').append(data); }); }); </script>

<div id="ajaxContent02"></div><script> var Webflow = Webflow || []; Webflow.push(function() { $.get('YOUR COPIED LINK HERE', function(data) { $('#ajaxContent02').append(data); }); }); </script>

just make sure you name your id differently (e.g. ajaxContent01, ajaxContent02)
