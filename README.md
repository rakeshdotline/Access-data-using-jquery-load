# Access-data-using-jquery-load

The .load() method, unlike $.get(), allows us to specify a portion of the remote document to be inserted. This is achieved with a special syntax for the url parameter. If one or more space characters are included in the string, the portion of the string following the first space is assumed to be a jQuery selector that determines the content to be loaded.

We could modify the example above to use only part of the document that is fetched:

<!doctype html>
<html lang="en">
    <head>
        <meta charset="utf-8">
        <title>load demo</title>
        <style>
            body {
                font-size: 12px;
                font-family: Arial;
            }
        </style>
        <script src="https://code.jquery.com/jquery-1.10.2.js"></script>
    </head>
    <body>

<b>Projects:</b>
<ol id="new-projects"></ol>

<script>
    $( "#new-projects" ).load( "/resources/load.html #projects li" );
</script>

</body>
</html>