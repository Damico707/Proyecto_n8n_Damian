📋 Sistema de Gestión de Inasistencias
Sistema automatizado para registrar, analizar y gestionar solicitudes de justificación de inasistencias, integrando inteligencia artificial, Google Sheets y notificaciones vía Telegram.

🧠 ¿Cómo funciona?
Formulario HTML
      ↓
   Webhook (n8n)
      ↓
  Agente IA (Gemini) → Clasifica la justificación
      ↓
  Google Sheets → Guarda el registro completo
      ↓
  Bot de Telegram → Notifica al estudiante
El bot de Telegram también permite consultar el estado de una solicitud escribiendo /estado @ID.

🛠️ Tecnologías utilizadas
TecnologíaUson8n.cloudMotor de automatización y orquestaciónGoogle Gemini APIAnálisis y clasificación de justificacionesGoogle SheetsAlmacenamiento de registrosTelegram Bot APINotificaciones y consultasHTML + CSSFormulario web de solicitudes

✅ Requisitos previos
Antes de importar el flujo necesitas tener listo lo siguiente:
1. Cuenta en n8n.cloud

Regístrate en n8n.cloud

2. Bot de Telegram

Abre Telegram y busca @BotFather
Escribe /newbot y sigue las instrucciones
Copia el Token que te genera

3. API Key de Google Gemini

Ve a Google AI Studio
Crea una API Key
Cópiala para usarla en n8n

4. Google Sheets

Crea una hoja de cálculo en Google Drive
Agrega las siguientes columnas en la fila 1:

nombre | id | correo | curso | motivo | clasificacion | confianza | razon

🚀 Cómo importar el flujo en n8n

Abre tu cuenta en n8n.cloud
Crea un nuevo flujo
Haz clic en el menú ... (arriba a la derecha)
Selecciona Import from file
Sube el archivo flujo_inasistencias.json


🔐 Cómo configurar las credenciales
Una vez importado el flujo debes reemplazar las credenciales con las tuyas:
Google Sheets

Abre el nodo Google Sheets
En Credential conecta tu cuenta de Google
Selecciona tu hoja de cálculo en Document

Google Gemini

Abre el nodo Google Gemini Chat Model
En Credential agrega tu API Key de Gemini

Telegram

Abre el nodo Telegram Trigger
En Credential agrega el token de tu bot
Repite para todos los nodos de Send a text message


📁 Estructura del repositorio
📦 sistema-inasistencias
 ┣ 📄 README.md
 ┣ 📄 flujo_inasistencias.json
 ┗ 📄 index.html

📸 Screenshot del flujo n8n
Flujo principal (Formulario → IA → Sheets)

(Agregar screenshot aquí)

Flujo del bot de Telegram

(Agregar screenshot aquí)


⚠️ Riesgos y limitaciones

La IA puede cometer errores en casos ambiguos
No detecta documentos falsificados automáticamente
Depende de servicios externos (Google, Telegram, n8n)
Requiere supervisión humana en casos de confianza media


👤 Autor
Desarrollado como proyecto académico para la automatización de procesos administrativos educativos.
