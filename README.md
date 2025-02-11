<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>B&J Home - Costa Smeralda</title>
    <style>
        body { font-family: Arial, sans-serif; margin: 0; padding: 0; background-color: #f5f5f5; }
        header { background-color: #2c3e50; color: white; padding: 20px; text-align: center; }
        nav { background-color: #34495e; padding: 10px; text-align: center; }
        nav a { color: white; text-decoration: none; margin: 0 15px; font-size: 18px; }
        .container { max-width: 1200px; margin: auto; padding: 20px; }
        .gallery img { width: 100%; height: auto; border-radius: 10px; }
        .calendar, .booking-form, .info-section { margin-top: 20px; }
        footer { background-color: #2c3e50; color: white; text-align: center; padding: 10px; margin-top: 20px; }
    </style>
    <script src="https://cdn.jsdelivr.net/npm/fullcalendar@5.11.3/main.min.js"></script>
    <link href="https://cdn.jsdelivr.net/npm/fullcalendar@5.11.3/main.min.css" rel="stylesheet">
    <script>
        document.addEventListener('DOMContentLoaded', function() {
            var calendarEl = document.getElementById('calendar');
            var calendar = new FullCalendar.Calendar(calendarEl, {
                initialView: 'dayGridMonth',
                selectable: true,
                dateClick: function(info) {
                    alert('Fecha seleccionada: ' + info.dateStr);
                }
            });
            calendar.render();
        });
    </script>
</head>
<body>
    <header>
        <h1>B&J Home - Costa Smeralda</h1>
        <p>Un paraíso en Cerdeña</p>
    </header>
    
    <nav>
        <a href="#about">Quiénes Somos</a>
        <a href="#availability">Disponibilidad</a>
        <a href="#activities">Actividades</a>
        <a href="#faq">Preguntas Frecuentes</a>
        <a href="#legal">Aviso Legal</a>
    </nav>
    
    <div class="container">
        <section class="gallery">
            <h2>Bienvenidos a B&J Home</h2>
            <p>Un refugio de lujo en la hermosa Costa Esmeralda, ideal para unas vacaciones inolvidables.</p>
            <p>Próximamente imágenes</p>
        </section>
        
        <section id="availability" class="calendar">
            <h2>Disponibilidad</h2>
            <div id="calendar"></div>
        </section>
        
        <section id="about" class="info-section">
            <h2>Quiénes Somos</h2>
            <p>B&J Home es un alojamiento exclusivo diseñado para quienes buscan comodidad y tranquilidad en la Costa Smeralda.</p>
        </section>
        
        <section id="activities" class="info-section">
            <h2>Actividades en la Zona</h2>
            <p>Desde playas paradisíacas hasta rutas de senderismo, descubre todo lo que puedes hacer en la Costa Smeralda.</p>
        </section>
        
        <section id="faq" class="info-section">
            <h2>Preguntas Frecuentes</h2>
            <p>Encuentra respuestas a las preguntas más comunes sobre tu estancia en B&J Home.</p>
        </section>
        
        <section id="legal" class="info-section">
            <h2>Aviso Legal</h2>
            <p>Consulta nuestras políticas de privacidad y términos de uso.</p>
        </section>
        
        <section class="booking-form">
            <h2>Reserva ahora</h2>
            <form action="payment.php" method="post">
                <label for="name">Nombre:</label>
                <input type="text" id="name" name="name" required><br>
                <label for="email">Email:</label>
                <input type="email" id="email" name="email" required><br>
                <label for="dates">Fechas:</label>
                <input type="date" id="dates" name="dates" required><br>
                <input type="hidden" name="payment_method" value="stripe_paypal">
                <p>El pago se realizará en su totalidad al momento de la reserva. En caso de cancelación con al menos 15 días de antelación, se reembolsará el importe completo.</p>
                <button type="submit">Reservar y pagar</button>
            </form>
        </section>
    </div>
    
    <footer>
        <p>&copy; 2025 B&J Home - Todos los derechos reservados</p>
    </footer>
</body>
</html>
