<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Art Parti</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap');
        
        body { 
            font-family: 'Poppins', sans-serif; 
            text-align: center; 
            background-color: #fff3e0; 
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
            color: #d81b60; 
            font-size: 3.5rem;
            font-weight: 600;
            margin-bottom: 10px;
        }
        .subheading {
            font-size: 1.4rem;
            color: #444;
            margin-bottom: 30px;
        }
        .button { 
            background-color: #d81b60; 
            color: white; 
            padding: 14px 30px; 
            text-decoration: none; 
            border-radius: 30px; 
            font-size: 1.2rem;
            display: inline-block;
            transition: 0.3s;
            margin-top: 15px;
        }
        .button:hover {
            background-color: #ad1457;
        }
        .event-list, .contact-form, .banner, .calendar { 
            margin-top: 40px; 
            background: white; 
            padding: 30px; 
            border-radius: 15px; 
            box-shadow: 0 6px 15px rgba(0, 0, 0, 0.1);
            transition: 0.3s;
        }
        .event-list:hover, .contact-form:hover, .banner:hover, .calendar:hover {
            transform: scale(1.02);
        }
        input, textarea { 
            width: 100%; 
            padding: 12px; 
            margin: 10px 0; 
            border: 1px solid #ddd; 
            border-radius: 5px;
            font-size: 1rem;
        }
        .event-item { 
            border-bottom: 2px solid #d81b60; 
            padding: 20px 0; 
        }
        .event-item:last-child {
            border-bottom: none;
        }
        .navbar {
            background: #d81b60;
            padding: 15px 0;
            position: fixed;
            width: 100%;
            top: 0;
            left: 0;
            z-index: 1000;
            box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
        }
        .navbar a {
            color: white;
            text-decoration: none;
            font-size: 1.2rem;
            padding: 15px 20px;
            font-weight: 500;
        }
        .navbar a:hover {
            text-decoration: underline;
        }
        .spacer {
            height: 70px;
        }
        .banner img {
            width: 100%;
            border-radius: 15px;
            margin-top: 20px;
        }
        .calendar-container {
            display: flex;
            justify-content: center;
            margin-top: 20px;
        }
        .calendar select {
            padding: 10px;
            font-size: 1.2rem;
            border-radius: 5px;
            border: 1px solid #d81b60;
        }
    </style>
</head>
<body>
    <div class="navbar">
        <a href="#events">Events</a>
        <a href="#contact">Contact</a>
    </div>
    
    <div class="spacer"></div>
    
    <div class="container">
        <h1>Welcome to The Art Parti 🎨✨</h1>
        <p class="subheading">Unleash your creativity in a fun, vibrant space!</p>
        
        <div class="banner">
            <img src="https://tse3.mm.bing.net/th?id=OIP.YAnPrhv-gp00kGpJukR50wHaE8&pid=Api" alt="People having fun creating art together">
            <img src="https://tse4.mm.bing.net/th?id=OIP.vsDvnseWKis9jdjxLEPnxQHaFX&pid=Api" alt="A group enjoying an art session">
        </div>

        <div class="event-list" id="event-list">
            <h2>🎭 Upcoming Events</h2>
        </div>

        <div class="calendar">
            <h2>📅 Select a Date to Book</h2>
            <div class="calendar-container">
                <select id="eventDates"></select>
            </div>
            <a class="button" id="bookButton" href="https://venmo.com/TheArtParti">Book Now</a>
        </div>
    </div>

    <script>
        document.addEventListener("DOMContentLoaded", function() {
            const eventDates = document.getElementById("eventDates");
            const bookButton = document.getElementById("bookButton");
            const today = new Date();

            for (let i = 0; i < 30; i++) {
                let friday = new Date(today);
                let saturday = new Date(today);
                friday.setDate(today.getDate() + (i * 7) + (5 - today.getDay()));
                saturday.setDate(today.getDate() + (i * 7) + (6 - today.getDay()));
                
                let fridayOption = document.createElement("option");
                fridayOption.value = friday.toDateString();
                fridayOption.textContent = friday.toDateString();
                eventDates.appendChild(fridayOption);
                
                let saturdayOption = document.createElement("option");
                saturdayOption.value = saturday.toDateString();
                saturdayOption.textContent = saturday.toDateString();
                eventDates.appendChild(saturdayOption);
            }
            
            eventDates.addEventListener("change", function() {
                bookButton.href = "https://venmo.com/TheArtParti?date=" + encodeURIComponent(eventDates.value);
            });
        });
    </script>
</body>
</html>
