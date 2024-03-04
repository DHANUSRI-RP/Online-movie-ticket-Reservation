# ONLINE-MOVIE-TICKET-RESERVATION-
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Movie Ticket Reservation</title>
<style>
</style>
</head>
<body>
<h1>Movie Ticket Reservation</h1>
<form id="reservation-form">
<label for="movie">Select Movie:</label>
<select id="movie" required>
<option value="" disabled selected>Select a movie</option>
<option value="LEO">LEO</option>
<option value="JAILER">JAILER</option>
<option value="MAAMANNAN">MAAMANNAN</option>
<option value="VIDUTHALAI">VIDUTHALAI</option>
<option value="ANEETHI">ANEETHI</option>
<option value="CAPTAIN MILLER">CAPTAIN MILLER</option>,
</select><br>
<label for="date">Select Date:</label>
<input type="date" id="date" required>
<br>
<label for="time">Select Time:</label>
<select id="time" required>
<option value="" disabled selected>Select a time</option>
<option value="9:00 AM">9:00 AM</option>
<option value="11:00 AM">11:00 AM</option>
<option value="12:00 PM">12:00 PM</option>
<option value="3:00 PM">3:00 PM</option>
<option value="6:00 PM">6:00 PM</option>
<option value="10:00 PM">10:00 PM</option>
</select><br>
<label for="seats">Select Number of Seats:</label>
<input type="number" id="seats" min="1" max="10" required>
<br>
<label for="name">Your Name:</label>
<input type="text" id="name" required>
<br>
 
<label for="email">Your Email:</label>
<input type="email" id="email" required>
<br><br>
<button type="submit">Book Tickets</button>
</form>
<div id="reservation-summary" style="display: none;">
<h2>Reservation Summary</h2>
<p><strong>Movie:</strong> <span id="summary-movie"></span></p>
<p><strong>Date:</strong> <span id="summary-date"></span></p>
<p><strong>Time:</strong> <span id="summary-time"></span></p>
<p><strong>Seats:</strong><spanid="summary-seats"></span></p>p><strong>Total Price:</strong> <span id="summary-price"></span></p>
</div>
<script>
document.getElementById('reservation-form').addEventListener('submit', function (event) { event.preventDefault();
const movie = document.getElementById('movie').value; const date = document.getElementById('date').value; const time = document.getElementById('time').value;
const seats = parseInt(document.getElementById('seats').value); const name = document.getElementById('name').value;
const email = document.getElementById('email').value;

// Calculate total price
const totalPrice = 210 * seats;

// Display reservation summary document.getElementById('summary-movie').innerText = movie; document.getElementById('summary-date').innerText = date; document.getElementById('summary-time').innerText = time; document.getElementById('summary-seats').innerText = seats;
document.getElementById('summary-price').innerText = 'Rs ' + totalPrice + '/-';

// Hide form and show summary document.getElementById('reservation-form').style.display = 'none';
document.getElementById('reservation-summary').style.display = 'block';
});
</script>
</body>
</html>
