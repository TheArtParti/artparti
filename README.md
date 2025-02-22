<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Art Parti</title>
    <style>
        body { 
            font-family: 'Poppins', sans-serif; 
            text-align: center; 
            background-color: #fff8e1; 
            color: #333; 
            margin: 0; 
            padding: 0;
        }
        .container { 
            max-width: 1000px; 
            margin: auto; 
            padding: 40px 20px;
        }
        h1 { 
            color: #ff4081; 
            font-size: 3rem;
        }
        .button { 
            background-color: #ff4081; 
            color: white; 
            padding: 12px 25px; 
            text-decoration: none; 
            border-radius: 25px; 
            font-size: 1.2rem;
            display: inline-block;
            margin-top: 15px;
        }
        .event-list, .contact-form { 
            margin-top: 40px; 
            background: white; 
            padding: 25px; 
            border-radius: 15px; 
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
        }
        input, textarea { 
            width: 100%; 
            padding: 12px; 
            margin: 10px 0; 
            border: 1px solid #ddd; 
            border-radius: 5px;
        }
        .event-item { 
            border-bottom: 2px solid #ff4081; 
            padding: 20px 0; 
        }
        .event-item:last-child {
            border-bottom: none;
        }
        .navbar {
            background: #ff4081;
            padding: 15px 0;
        }
        .navbar a {
            color: white;
            text-decoration: none;
            font-size: 1.2rem;
            padding: 15px;
        }
    </style>
</head>
<body>
    <div class="navbar">
        <a href="#events">Events</a>
        <a href="#contact">Contact</a>
    </div>
    
    <div class="container">
        <h1>Welcome to The Art Parti 🎨✨</h1>
        <p>Unleash your creativity in a fun, vibrant space!</p>
        
        <div class="event-list" id="events">
            <h2>🎭 Upcoming Events</h2>
            <div class="event-item">
                <h3>Watercolor Workshop</h3>
                <p>Date: March 15, 2025</p>
                <p>Join us for a relaxing and fun watercolor painting session!</p>
                <a class="button" href="https://venmo.com/TheArtParti">Book & Pay via Venmo</a>
            </div>
        </div>
        
        <div class="contact-form" id="contact">
            <h2>📩 Join Our Community</h2>
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
