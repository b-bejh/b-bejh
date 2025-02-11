<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>B&J Home - Costa Smeralda</title>
    <style>
        body { font-family: Arial, sans-serif; margin: 0; padding: 0; background-color: #f5f5f5; }
        header { background-color: #2c3e50; color: white; padding: 20px; text-align: center; }
        .container { max-width: 1200px; margin: auto; padding: 20px; }
        .gallery img { width: 100%; height: auto; border-radius: 10px; }
        .calendar, .booking-form { margin-top: 20px; }
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
    
    <div class="container">
        <section class="gallery">
            <h2>Galería</h2>
            <p>Próximamente imágenes</p>
        </section>
        
        <section class="calendar">
            <h2>Disponibilidad</h2>
            <div id="calendar"></div>
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

