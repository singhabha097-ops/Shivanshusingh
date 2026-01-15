# Shivanshusingh
Book tickets 
// Seat selection
function toggleSeat(id) {
  let seat = document.getElementById('seat'+id);
  seat.classList.toggle('selected');
}

// User signup
function signup() {
  localStorage.setItem(document.getElementById('su').value, document.getElementById('sp').value);
  alert('Signup successful');
}

// User/Admin login
function login() {
  let u = document.getElementById('user').value;
  let p = document.getElementById('pass').value;

  if (u === 'admin' && p === '1234') {
    window.location = 'admin.html';
  } else if (localStorage.getItem(u) === p) {
    alert('User login successful');
  } else {
    alert('Invalid login');
    body { font-family: Arial; margin: 0; background: #f4f6f8; text-align: center; }
header { background: #0b5ed7; color: white; padding: 20px; }
nav a { color: white; margin: 0 10px; text-decoration: none; font-weight: bold; }
.search input, button { padding: 10px; margin: 5px; }
button { background: #198754; color: white; border: none; cursor: pointer; }
.seat-grid { display: grid; grid-template-columns: repeat(4, 50px); justify-content: center; gap: 5px; margin: 20px 0; }
.seat { background: #e0e0e0; padding: 10px; cursor: pointer; }
.seat.selected { background: #198754; color: white; }
footer { background: #222; color: white; padding: 10px; position: fixed; bottom: 0; width: 100%; }
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ATS Bus Booking</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <h1>ATS</h1>
    <p>Easy, Fast & Reliable Bus Ticket Booking</p>
    <nav>
      <a href="index.html">Home</a>
      <a href="about.html">About</a>
      <a href="services.html">Routes</a>
      <a href="gallery.html">Gallery</a>
      <a href="contact.html">Contact</a>
      <a href="login.html">Login</a>
      <a href="signup.html">Signup</a>
    </nav>
  </header>

  <section class="search">
    <input type="text" placeholder="From" />
    <input type="text" placeholder="To" />
    <input type="date" />
    <button onclick="window.location='payment.html'">Search & Book</button>
  </section>

  <section class="seats">
    <h2>Select Seats (40 seats)</h2>
    <div class="seat-grid">
      <!-- 40 seats -->
      <script>
        for(let i=1;i<=40;i++){
          document.write('<div class="seat" id="seat'+i+'" onclick="toggleSeat('+i+')">'+i+'</div>');
        }
      </script>
    </div>
  </section>

  <footer>
    <p>📞 7654884845 | 📧 singhabha097@gmail.com | Bhabua</p>
  </footer>
  <script src="script.js"></script>
</body>
</html>
  }
}

// Payment demo
function pay(method) {
  alert(method + " payment successful!\nTicket booked.");
  window.location = 'success.html';
}
