<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Art Parti</title>
    <style>
        body { font-family: Arial, sans-serif; text-align: center; background-color: #fdf6e3; color: #333; }
        .container { max-width: 800px; margin: auto; padding: 20px; }
        h1 { color: #ff6347; }
        .button { background-color: #ff6347; color: white; padding: 10px 20px; text-decoration: none; border-radius: 5px; display: inline-block; }
        .event-list, .contact-form { margin-top: 20px; }
        input, textarea { width: 100%; padding: 10px; margin: 5px 0; }
        .event-item { border: 1px solid #ddd; padding: 10px; margin: 10px 0; }
    </style>
</head>
<body>
    <div class="container">
        <h1>Welcome to The Art Parti</h1>
        <p>A creative space to explore your artistic side!</p>
        
        <div class="event-list">
            <h2>Upcoming Events</h2>
            <div class="event-item">
                <h3>Watercolor Workshop</h3>
                <p>Date: March 15, 2025</p>
                <p>Join us for a fun watercolor painting session!</p>
                <a class="button" href="https://venmo.com/TheArtParti">Book & Pay via Venmo</a>
            </div>
        </div>
        
        <div class="contact-form">
            <h2>Join Our Community</h2>
            <form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
                <input type="text" name="name" placeholder="Your Name" required>
                <input type="email" name="email" placeholder="Your Email" required>
                <textarea name="message" placeholder="Your Message"></textarea>
                <button class="button" type="submit">Submit</button>
            </form>
        </div>
    </div>
</body>
</html>
