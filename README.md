# Videoconferencia en Tiempo Real

## Descripción

Este proyecto es una aplicación de videoconferencia basada en **Flask**, **Socket.IO** y **Canvas**, que permite la transmisión de video en tiempo real entre múltiples usuarios sin necesidad de WebRTC. Se utiliza un servidor Flask para manejar conexiones y reenvío de frames de video a través de **WebSockets**.

## Características

- Permite conexiones múltiples en tiempo real.
- Uso de **Canvas** para renderizar los frames de video.
- Comunicación basada en **Socket.IO**.
- Soporte para eventos de conexión y desconexión de usuarios.
- Diseño responsive con una interfaz minimalista.

## Instalación y Configuración

### Requisitos

- **Python 3.x**
- **Flask** y **Flask-SocketIO**
- **Ngrok** (opcional para exponer el servidor a Internet)

### Instalación

1. Clonar el repositorio:
   ```bash
   git clone https://github.com/usuario/videoconferencia.git
   cd videoconferencia
   ```
2. Instalar dependencias:
   ```bash
   pip install flask flask-socketio flask-cors
   ```
3. Iniciar el servidor:
   ```bash
   python servidor.py
   ```
4. Si deseas hacer accesible la aplicación desde Internet, inicia un túnel con **Ngrok**:
   ```bash
   ngrok http 5000
   ```
   Copia la URL generada por Ngrok y configúrala en `index.html`.

## Uso

1. Abre el archivo `index.html` en un navegador.
2. Permite el acceso a la cámara.
3. Se generará un **canvas** donde se visualizará tu video.
4. Cuando otro usuario se conecte, su video aparecerá en la pantalla.

## Tecnologías Utilizadas

- **Flask** (Servidor web)
- **Socket.IO** (Comunicación en tiempo real)
- **JavaScript** (Manipulación de video y eventos)
- **HTML5 Canvas** (Renderizado de video)
- **CSS3** (Diseño responsive y atractivo)

## Funcionamiento

1. Un usuario abre la aplicación y se conecta al servidor.
2. Se solicita acceso a la cámara y se captura el video en un **canvas**.
3. Los frames del video se convierten en imágenes y se envían al servidor mediante **Socket.IO**.
4. El servidor reenvía los frames a los demás usuarios conectados.
5. Cada usuario recibe los frames y los dibuja en su propio **canvas**.
6. Cuando un usuario se desconecta, su video desaparece de la pantalla.

## Mejoras Futuras

- Implementar WebRTC para mejorar la eficiencia de la transmisión de video.
- Agregar cifrado a la comunicación para mayor seguridad.
- Incluir chat de texto en tiempo real.
- Optimizar el uso de ancho de banda con técnicas de compresión de imágenes.

