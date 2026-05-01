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

3. Google Sheets

https://docs.google.com/spreadsheets/d/1K7gr_Ku96HSebKSQFKaTWTzRHsyw8sJVKBY-HnJOFDs/edit?usp=sharing

🚀 Cómo importar el flujo en n8n

Abre tu cuenta en n8n.cloud
Crea un nuevo flujo
Haz clic en el menú ... (arriba a la derecha)
Selecciona Import from file
Sube el archivo flujo_inasistencias.json


🔐 Cómo configurar las credenciales
Una vez importado el flujo debes reemplazar las credenciales con las tuyas:

Telegram

Abre el nodo Telegram Trigger
En Credential agrega el token de tu bot
Repite para todos los nodos de Send a text message


📁 Estructura del repositorio
📦 sistema-inasistencias
 ┣ 📄 JSON_N8N.md
 ┣ 📄 STYLES
 ┗ 📄 index.html
 ┗📄 README.md


⚠️ Riesgos y limitaciones

La IA puede cometer errores en casos ambiguos
No detecta documentos falsificados automáticamente
Depende de servicios externos (Google, Telegram, n8n)
Requiere supervisión humana en casos de confianza media


👤 Autor
Desarrollado como proyecto académico para la automatización de procesos administrativos educativos.


Screenshot del Flujo:

<img width="1919" height="929" alt="image" src="https://github.com/user-attachments/assets/c9f70d88-eb54-4458-9a34-6bd4710656b4" />


