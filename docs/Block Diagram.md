---
title: Block Diagram
---

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My GitHub Pages Site</title>
    <style>
        /* Basic Styling */
        body { font-family: Arial, sans-serif; text-align: center; margin: 20px; }

        /* Tab container */
        .tab {
            display: flex;
            justify-content: center;
            background: #ddd;
            padding: 10px;
        }

        /* Tab buttons */
        .tab button {
            background: none;
            border: none;
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
        }

        .tab button.active {
            background: #007BFF;
            color: white;
        }

        /* Tab content */
        .tabcontent {
            display: none;
            padding: 20px;
            border: 1px solid #ddd;
        }

        .tabcontent.active {
            display: block;
        }

        /* Image styling */
        .schematic-image {
            width: 100%;
            max-width: 800px;
        }

        /* PDF Viewer */
        iframe {
            width: 100%;
            height: 600px;
            border: none;
        }
    </style>
</head>
<body>

    <h1>My GitHub Pages Website</h1>

    <!-- Tabs -->
    <div class="tab">
        <button class="tablinks active" onclick="openTab(event, 'Home')">Home</button>
        <button class="tablinks" onclick="openTab(event, 'Schematic')">Schematic</button>
        <button class="tablinks" onclick="openTab(event, 'PDF')">PDF Viewer</button>
    </div>

    <!-- Tab Content -->
    <div id="Home" class="tabcontent active">
        <h2>Welcome to My GitHub Pages Site</h2>
        <p>This site hosts my schematic files and project details.</p>
    </div>

    <div id="Schematic" class="tabcontent">
        <h2>Schematic Diagram</h2>
        <img src="images/schematic.png" alt="Schematic Diagram" class="schematic-image">
    </div>

    <div id="PDF" class="tabcontent">
        <h2>PDF Viewer</h2>
        <iframe src="Schematic Prints.pdf"></iframe>
    </div>

    <!-- JavaScript for Tabs -->
    <script>
        function openTab(evt, tabName) {
            var i, tabcontent, tablinks;

            // Hide all tab contents
            tabcontent = document.getElementsByClassName("tabcontent");
            for (i = 0; i < tabcontent.length; i++) {
                tabcontent[i].style.display = "none";
                tabcontent[i].classList.remove("active");
            }

            // Remove active class from all buttons
            tablinks = document.getElementsByClassName("tablinks");
            for (i = 0; i < tablinks.length; i++) {
                tablinks[i].classList.remove("active");
            }

            // Show the clicked tab content and set button to active
            document.getElementById(tabName).style.display = "block";
            document.getElementById(tabName).classList.add("active");
            evt.currentTarget.classList.add("active");
        }
    </script>

</body>
</html>
