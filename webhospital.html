<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bioconect - Inicio de Sesión</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background: linear-gradient(to right, #002f4b, #005c97);
            color: white;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }
        .container {
            background-color: rgba(255, 255, 255, 0.2);
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
            max-width: 400px;
            width: 100%;
            margin: 10px;
            max-height: 80vh; /* Limitar la altura máxima para permitir el desplazamiento */
            overflow-y: auto; /* Habilitar desplazamiento vertical */
        }
        h1 {
            text-align: center;
            margin-bottom: 20px;
        }
        input[type="text"], input[type="password"], input[type="date"], textarea, input[type="file"] {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: none;
            border-radius: 5px;
        }
        button {
            width: 100%;
            padding: 10px;
            background-color: #005c97;
            border: none;
            border-radius: 5px;
            color: white;
            font-size: 16px;
            cursor: pointer;
            margin: 10px 0;
        }
        button:hover {
            background-color: #004080;
        }
        .area-buttons, .equipos-buttons, .marcas-buttons {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin: 10px 0;
        }
        .area-buttons button, .equipos-buttons button, .marcas-buttons button {
            flex: 1 1 30%;
        }
        .back-button {
            background-color: #004080;
            margin-top: 10px;
        }
        #imagen-container {
            text-align: center;
            margin-top: 20px;
        }
        #imagen-preview {
            max-width: 200px;
            max-height: 200px;
            display: none;
        }
    </style>
</head>
<body>
    <div class="container" id="login-container">
        <h1>Bioconect</h1>
        <input type="text" id="username" placeholder="Usuario">
        <input type="password" id="password" placeholder="Contraseña">
        <button onclick="iniciarSesion()">Iniciar Sesión</button>
    </div>

    <div class="container" id="area-container">
        <h1>Áreas del Hospital</h1>
        <div class="area-buttons" id="area-buttons">
            <button onclick="mostrarEquipos('Emergencia')">Emergencia</button>
            <button onclick="mostrarEquipos('UCI')">UCI</button>
            <button onclick="mostrarEquipos('Ginecología')">Ginecología</button>
            <button onclick="mostrarEquipos('Diálisis')">Diálisis</button>
            <!-- Añadir más áreas según sea necesario -->
        </div>
        <button class="back-button" onclick="volverLogin()">Volver al inicio</button>
        <button class="back-button" onclick="agregarArea()">Agregar Área</button>
        <button class="back-button" onclick="eliminarArea()">Eliminar Área</button>
    </div>

    <div class="container" id="equipos-container">
        <h1 id="equipos-titulo"></h1>
        <div class="equipos-buttons" id="equipos-buttons">
            <!-- Aquí se agregarán los botones de los equipos dinámicamente -->
        </div>
        <button class="back-button" onclick="volverArea()">Volver a Áreas</button>
        <button class="back-button" onclick="agregarEquipo()">Agregar Equipo</button>
        <button class="back-button" onclick="eliminarEquipo()">Eliminar Equipo</button>
    </div>

    <div class="container" id="detalles-container">
        <h1 id="detalles-titulo"></h1>
        <div id="detalles-info" style="margin-top: 20px;">
            <!-- Aquí se mostrarán los detalles del equipo seleccionado -->
        </div>
        <div id="imagen-container">
            <img id="imagen-preview" src="#" alt="Vista previa de la imagen">
        </div>
        <button class="back-button" onclick="volverEquipos()">Volver a Equipos</button>
    </div>

    <script>
        const containers = {
            login: document.getElementById('login-container'),
            area: document.getElementById('area-container'),
            equipos: document.getElementById('equipos-container'),
            detalles: document.getElementById('detalles-container')
        };

        function showContainer(containerName) {
            Object.values(containers).forEach(container => container.style.display = 'none');
            containers[containerName].style.display = 'block';
            localStorage.setItem('currentContainer', containerName);
        }

        function iniciarSesion() {
            const username = document.getElementById('username').value;
            const password = document.getElementById('password').value;
            // Aquí agregar lógica de autenticación
            if (username && password) {
                showContainer('area');
            } else {
                alert('Por favor, ingrese usuario y contraseña');
            }
        }

        function mostrarEquipos(area) {
            document.getElementById('equipos-titulo').textContent = area;
            showContainer('equipos');
            localStorage.setItem('areaActual', area);
            cargarEquipos(area);
        }

        function mostrarMarcas(equipo) {
            const area = localStorage.getItem('areaActual');
            document.getElementById('detalles-titulo').textContent = `${area} - ${equipo}`;
            showContainer('detalles');
            localStorage.setItem('equipoActual', equipo);
            mostrarDetalles();
        }

        function mostrarDetalles() {
            const area = localStorage.getItem('areaActual');
            const equipo = localStorage.getItem('equipoActual');
            const detallesKey = `${area}-${equipo}`;
            const detalles = JSON.parse(localStorage.getItem(detallesKey)) || {
                modelo: '',
                numeroSerie: '',
                marca: '',
                fechaAdquisicion: '',
                vidaUtil: '',
                inicioOperaciones: '',
                ultimaCalibracion: '',
                responsable: '',
                comentarios: ''
            };
            const detallesInfo = `
                <label>Modelo:</label>
                <input type="text" id="modelo" value="${detalles.modelo}">
                <label>Número de Serie:</label>
                <input type="text" id="numeroSerie" value="${detalles.numeroSerie}">
                <label>Marca:</label>
                <input type="text" id="marca" value="${detalles.marca}">
                <label>Fecha de Adquisición:</label>
                <input type="date" id="fechaAdquisicion" value="${detalles.fechaAdquisicion}">
                <label>Vida Útil:</label>
                <input type="text" id="vidaUtil" value="${detalles.vidaUtil}">
                <label>Fecha de Inicio de Operaciones:</label>
                <input type="date" id="inicioOperaciones" value="${detalles.inicioOperaciones}">
                <label>Última Fecha de Calibración:</label>
                <input type="date" id="ultimaCalibracion" value="${detalles.ultimaCalibracion}">
                <label>Responsable del Mantenimiento:</label>
                <input type="text" id="responsable" value="${detalles.responsable}">
                <label>Foto del Equipo:</label><br>
                <input type="file" accept="image/*" onchange="cargarImagen(event)"><br>
                <label>Comentarios:</label><br>
                <textarea rows="4" id="comentarios" placeholder="Ingrese sus comentarios aquí">${detalles.comentarios || ''}</textarea>
                <button onclick="guardarDetalles()">Guardar</button>
            `;
            document.getElementById('detalles-info').innerHTML = detallesInfo;
            cargarImagenGuardada(detallesKey);
        }

        function cargarImagen(event) {
            const input = event.target;
            const reader = new FileReader();
            reader.onload = function() {
                const dataURL = reader.result;
                const imagenPreview = document.getElementById('imagen-preview');
                imagenPreview.src = dataURL;
                imagenPreview.style.display = 'block';
                const area = localStorage.getItem('areaActual');
                const equipo = localStorage.getItem('equipoActual');
                const detallesKey = `${area}-${equipo}`;
                localStorage.setItem(`imagen-${detallesKey}`, dataURL);
            };
            reader.readAsDataURL(input.files[0]);
        }

        function cargarImagenGuardada(detallesKey) {
            const imagen = localStorage.getItem(`imagen-${detallesKey}`);
            if (imagen) {
                const imagenPreview = document.getElementById('imagen-preview');
                imagenPreview.src = imagen;
                imagenPreview.style.display = 'block';
            }
        }

        function guardarDetalles() {
            const area = localStorage.getItem('areaActual');
            const equipo = localStorage.getItem('equipoActual');
            const detallesKey = `${area}-${equipo}`;
            const detalles = {
                modelo: document.getElementById('modelo').value,
                numeroSerie: document.getElementById('numeroSerie').value,
                marca: document.getElementById('marca').value,
                fechaAdquisicion: document.getElementById('fechaAdquisicion').value,
                vidaUtil: document.getElementById('vidaUtil').value,
                inicioOperaciones: document.getElementById('inicioOperaciones').value,
                ultimaCalibracion: document.getElementById('ultimaCalibracion').value,
                responsable: document.getElementById('responsable').value,
                comentarios: document.getElementById('comentarios').value
            };
            localStorage.setItem(detallesKey, JSON.stringify(detalles));
            alert('Detalles guardados exitosamente');
        }

        function volverLogin() {
            showContainer('login');
            localStorage.removeItem('areaActual');
            localStorage.removeItem('equipoActual');
        }

        function volverArea() {
            showContainer('area');
        }

        function volverEquipos() {
            showContainer('equipos');
        }

        function agregarArea() {
            const nuevaArea = prompt('Ingrese el nombre de la nueva área:');
            if (nuevaArea) {
                const areaButtons = document.getElementById('area-buttons');
                const button = document.createElement('button');
                button.textContent = nuevaArea;
                button.onclick = () => mostrarEquipos(nuevaArea);
                areaButtons.appendChild(button);
            }
        }

        function eliminarArea() {
            const areaAEliminar = prompt('Ingrese el nombre de la área a eliminar:');
            if (areaAEliminar) {
                const areaButtons = document.getElementById('area-buttons');
                const buttons = areaButtons.getElementsByTagName('button');
                for (let i = 0; i < buttons.length; i++) {
                    if (buttons[i].textContent === areaAEliminar) {
                        areaButtons.removeChild(buttons[i]);
                        break;
                    }
                }
            }
        }

        function cargarEquipos(area) {
            const equiposButtons = document.getElementById('equipos-buttons');
            equiposButtons.innerHTML = ''; // Limpiar botones existentes
            for (let i = 0; i < localStorage.length; i++) {
                const key = localStorage.key(i);
                if (key.startsWith(`${area}-`) && !key.startsWith(`imagen-`)) {
                    const equipo = key.split('-')[1];
                    const button = document.createElement('button');
                    button.textContent = equipo;
                    button.onclick = () => mostrarMarcas(equipo);
                    equiposButtons.appendChild(button);
                }
            }
        }

        function agregarEquipo() {
            const nuevoEquipo = prompt('Ingrese el nombre del nuevo equipo:');
            if (nuevoEquipo) {
                const area = localStorage.getItem('areaActual');
                const equiposButtons = document.getElementById('equipos-buttons');
                const button = document.createElement('button');
                button.textContent = nuevoEquipo;
                button.onclick = () => mostrarMarcas(nuevoEquipo);
                equiposButtons.appendChild(button);
                // Crear una entrada vacía en localStorage para el nuevo equipo
                const detallesKey = `${area}-${nuevoEquipo}`;
                localStorage.setItem(detallesKey, JSON.stringify({
                    modelo: '',
                    numeroSerie: '',
                    marca: '',
                    fechaAdquisicion: '',
                    vidaUtil: '',
                    inicioOperaciones: '',
                    ultimaCalibracion: '',
                    responsable: '',
                    comentarios: ''
                }));
            }
        }

        function eliminarEquipo() {
            const equipoAEliminar = prompt('Ingrese el nombre del equipo a eliminar:');
            if (equipoAEliminar) {
                const area = localStorage.getItem('areaActual');
                const equiposButtons = document.getElementById('equipos-buttons');
                const buttons = equiposButtons.getElementsByTagName('button');
                for (let i = 0; i < buttons.length; i++) {
                    if (buttons[i].textContent === equipoAEliminar) {
                        equiposButtons.removeChild(buttons[i]);
                        const detallesKey = `${area}-${equipoAEliminar}`;
                        localStorage.removeItem(detallesKey);
                        localStorage.removeItem(`imagen-${detallesKey}`);
                        break;
                    }
                }
            }
        }

        window.onload = function() {
            const currentContainer = localStorage.getItem('currentContainer') || 'login';
            showContainer(currentContainer);
        };
    </script>
</body>
</html>
