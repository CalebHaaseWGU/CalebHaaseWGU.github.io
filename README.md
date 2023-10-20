<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>State Website</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <!-- Your header content, like the logo, state name, etc. -->
        <h1>State of California</h1>
    </header>

    <!-- Navigation Section -->
    <nav>
        <ul>
            <li><a href="#" onclick="generatePage('Home')">Home</a></li>
            <li><a href="#" onclick="generatePage('Los Angeles')">Los Angeles</a></li>
            <li><a href="#" onclick="generatePage('San Francisco')">San Francisco</a></li>
            <li><a href="#" onclick="generatePage('Sacramento')">Sacramento</a></li>
            <li><a href="#" onclick="generatePage('San Diego')">San Diego</a></li>
        </ul>
    </nav>

    <!-- Main Content Area -->
    <section id="content">
        <!-- Content will be loaded here dynamically -->
    </section>

    <aside>
        <!-- Your aside content. This can be news, updates, etc. -->
    </aside>

    <footer>
        <!-- Your footer content. This can be copyrights, disclaimers, etc. -->
        <p>Copyright © 2023 State of California</p>
    </footer>

    <!-- Linking the JavaScript File -->
    <script src="script.js" defer></script>
</body>
</html>


function generatePage(city) {
    const contentArea = document.getElementById('content');
    let content = '';

    switch (city) {
        case 'Home':
            content = `
                <h2>Welcome to California</h2>
                <p>California is known for its golden beaches and sunny weather...</p>
            `;
            break;
        case 'Los Angeles':
            content = `
                <h2>Los Angeles</h2>
                <p>Los Angeles is known for Hollywood and much more...</p>
            `;
            break;
        case 'San Francisco':
            content = `
                <h2>San Francisco</h2>
                <p>San Francisco is known for the Golden Gate Bridge...</p>
            `;
            break;
        case 'Sacramento':
            content = `
                <h2>Sacramento</h2>
                <p>Sacramento is the capital of California...</p>
            `;
            break;
        case 'San Diego':
            content = `
                <h2>San Diego</h2>
                <p>San Diego is known for its lovely beaches and parks...</p>
            `;
            break;
        default:
            content = '<p>Sorry, the content for this city is not available at the moment.</p>';
    }

    contentArea.innerHTML = content;
}


body {
    font-family: Arial, sans-serif;
}

header, nav, section, aside, footer {
    padding: 20px;
    margin: 10px;
    border: 1px solid #ddd;
}

nav ul {
    list-style-type: none;
}

nav ul li {
    display: inline-block;
    margin-right: 10px;
}

nav ul li a {
    text-decoration: none;
    color: blue;
    padding: 5px 10px;
    border: 1px solid blue;
    border-radius: 5px;
    transition: background-color 0.3s;
}

nav ul li a:hover {
    background-color: blue;
    color: white;
}
