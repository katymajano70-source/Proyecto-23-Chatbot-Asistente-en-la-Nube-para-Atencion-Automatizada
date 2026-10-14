# Proyecto-23-Chatbot-Asistente-en-la-Nube-para-Atencion-Automatizada
Chatbot asistente en la nube con Dialogflow CX e integracion a WhatsApp y Google Sheets para Centro de Servicios Digitales Cuidadanos CSDC

# Chatbot Asistente en la Nube para Atención Ciudadana (CSDC)

Repositorio profesional para el proyecto **Chatbot Asistente en la Nube para Atención Automatizada (Lite)** desarrollado para el **Centro de Servicios Digitales Ciudadanos (CSDC)** de la Secretaría de Innovación de El Salvador (ESIT).

---

## 📌 Descripción del Proyecto
El objetivo del proyecto es reducir la sobrecarga del personal y los tiempos de espera en la atención ciudadana digital mediante la implementación de un bot asistente capaz de:
1. Responder preguntas frecuentes (FAQ) las 24 horas sobre más de 90 trámites en Simple.sv, Identidad Digital, programas de la ESIT y servicios del SAC.
2. Capturar y registrar solicitudes o denuncias de forma estandarizada en Google Sheets a través de un webhook middleware en Python.
3. Operar de forma integrada en canales digitales como Telegram Bot o Webchat Widgets.

---

## 📂 Estructura del Repositorio

```text
csdc-chatbot-repo/
├── README.md                           # Documentación principal del repositorio
├── .env.example                        # Plantilla de variables de entorno
├── .gitignore                          # Reglas de exclusión para Git y credenciales
├── flows/                              # Definiciones de flujos e intenciones en JSON
│   ├── dialogflow_cx_agent.json        # Exportación del agente de Dialogflow CX
│   └── n8n_workflow_csdc.json          # Flujo de trabajo exportado de n8n
├── src/                                # Código fuente del Webhook Backend
│   ├── main.py                         # Servidor/Handler Webhook en Python
│   ├── requirements.txt                # Dependencias de Python
│   └── service_account.json.example    # Plantilla de credenciales GCP / Google Sheets
├── docs/                               # Documentación de las 5 Fases del Proyecto
│   ├── Plan_de_Recursos_Tecnologicos.md
│   ├── Documento_de_Analisis_Casos_de_Uso.md
│   ├── Catalogo_de_Intenciones_y_Respuestas.md
│   ├── Documento_de_Diseno_y_Arquitectura.md
│   ├── Matriz_de_Pruebas_Conversacionales.md
│   ├── Informe_Profesional_Final.md
│   └── Bitacora_de_Trabajo_Semanal.md
└── tests/                              # Scripts y payloads de prueba (QA)
    ├── test_webhook_payload.json       # Payload de prueba en formato Dialogflow CX
    └── test_webhook.sh                 # Script bash para cURL testing
```

---

## 🚀 Guía de Uso e Importación en GitHub
1. Descomprimir el archivo ZIP descargado desde este repositorio.
2. Inicializar Git en la carpeta del proyecto y publicar en tu cuenta de GitHub.
3. Importar los archivos JSON de la carpeta `flows/` en Dialogflow CX o n8n.
4. Ejecutar el webhook de `src/main.py` para procesar los registros de usuarios.

# Configuración del Entorno - CSDC Chatbot Cloud
GOOGLE_APPLICATION_CREDENTIALS=service_account.json
SPREADSHEET_NAME=Registro_Solicitudes_CSDC
TELEGRAM_BOT_TOKEN=tu_telegram_bot_token_aqui
GMAIL_SENDER_USER=notificaciones@csdc.gob.sv
PORT=8080

# Environment variables
.env
*.env

# Python
__pycache__/
*.py[cod]
*$py.class
venv/
ENV/

# Credentials & Service Accounts
service_account.json
*.json
!flows/*.json
!tests/*.json

# IDEs & System
.vscode/
.idea/
.DS_Store

