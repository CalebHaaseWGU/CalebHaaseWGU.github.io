
<!DOCTYPE html>
<html lang="en">
<body>
    <header>
        <h1>Welcome to Virginia</h1>
        <img src="https://www.osano.com/hubfs/assets/blogs/featured/Virginia%20road%20sign.jpg" alt="Virginia">
    </header>
    <nav>
        <ul>
            <li><a href="index.html">Home</a></li>
            <li><a href="losangeles.html">Los Angeles</a></li>
            <li><a href="sanfrancisco.html">San Francisco</a></li>
            <li><a href="sacramento.html">Sacramento</a></li>
            <li><a href="sandiego.html">San Diego</a></li>
        </ul>
    </nav>
    <section>
        <h2>About California</h2>
        <p>California, in the western U.S., stretches from the Mexican border along the Pacific for nearly 900 miles. Its terrain includes cliff-lined beaches, redwood forests, the Sierra Nevada Mountains, Central Valley farmland, and the Mojave Desert.</p>
        <ol>
            <li>Capital: Sacramento</li>
            <li>Largest City: Los Angeles</li>
            <li>State Flower: California Poppy</li>
        </ol>
    </section>
    <aside>
        <h3>Facts:</h3>
        <ul>
            <li>Official State Animal: California Grizzly Bear</li>
            <li>Official State Song: "I Love You, California"</li>
            <li><a href="https://www.visitcalifornia.com/" target="_blank">Tourism Website</a></li>
        </ul>
    </aside>
    <footer>
        <form>
            <label for="fname">First name:</label>
            <input type="text" id="fname" name="fname" placeholder="First Name">
            <label for="lname">Last name:</label>
            <input type="text" id="lname" name="lname" placeholder="Last Name">
            <label for="email">Email:</label>
            <input type="email" id="email" name="email" placeholder="Email">
            <label for="confirm-email">Confirm Email:</label>
            <input type="email" id="confirm-email" name="confirm-email" placeholder="Confirm Email">
            <label for="question">Question:</label>
            <textarea id="question" name="question" placeholder="Ask a question"></textarea>
            <input type="submit" value="Submit">
        </form>
    </footer>
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






