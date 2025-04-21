html

<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Well-Structured HTML5 Document</title>
    <link rel="stylesheet" href="styles.css">
</head>

<body>

    <header>
        <h1>Welcome to My Website</h1>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>
    <main>
        <section id="about">
            <h2>About Us</h2>
            <p>We ensure to offer the safest accomodations that is well secured and has security for 24/7.</p>
        </section>

        <section id="services">
            <h2>Our rooms</h2>
            <ul>
                <li>bachelor room</li>
                <li>Sharing of 3 students</li>
                <li>sharing of 6 students</li>
            </ul>
        </section>

        <section id="contact">
            <h2>Contact Us</h2>
            <form action="/submit" method="post">
                <label for="name">Name:</label>
                <input type="text" id="name" name="name" required>
                
                <label for="email">Email:</label>
                <input type="email" id="email" name="email" required>

                <label for="message">Message:</label>
                <textarea id="message" name="message" required></textarea>

                <button type="submit">Send Message</button>
            </form>
        </section>
    </main>

    <footer>
        <p>&copy; 2025 My Website. All rights reserved.</p>
    </footer>

</body>
</html>

js.

// Function to change the text content dynamically
document.getElementById('change-text-btn').addEventListener('click', function() {
    const welcomeMessage = document.getElementById('welcome-message');
    welcomeMessage.textContent = 'The text has been changed!';
    welcomeMessage.style.color = 'blue'; // Modify CSS style
});

// Function to add a new list item
document.getElementById('add-element-btn').addEventListener('click', function() {
    const dynamicList = document.getElementById('dynamic-list');
    const newListItem = document.createElement('li');
    newListItem.textContent = 'New item added to the list!';
    dynamicList.appendChild(newListItem);
});

// Function to remove the last list item
document.getElementById('remove-element-btn').addEventListener('click', function() {
    const dynamicList = document.getElementById('dynamic-list');
    if (dynamicList.lastChild) {
        dynamicList.removeChild(dynamicList.lastChild);
    } else {
        alert('No more items to remove!');
    }
});
