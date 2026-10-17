# Proyecto-23-Chatbot-Asistente-en-la-Nube-para-Atencion-Automatizada
Chatbot asistente en la nube con Dialogflow CX e integracion a WhatsApp y Google Sheets para Centro de Servicios Digitales Cuidadanos CSDC

# Chatbot Asistente en la Nube para Atención Ciudadana (CSDC)

Repositorio profesional para el proyecto **Chatbot Asistente en la Nube para Atención Automatizada (Lite)** desarrollado para el **Centro de Servicios Digitales Ciudadanos (CSDC)** de la Secretaría de Innovación de El Salvador (ESIT).

---
hatbot asistente en la nube con Dialogflow CX e integracion a WhatsApp y Google Sheets para Centro de Servicios Digitales Cuidadanos CSDC

markdown Chatbot Asistente en la Nube - CSDC (Versión Lite)

Fase correspondiente: FASE 0: Onboarding y planificacion

FASE 1: Analisis de casos de uso e intenciones del Chatbot

Nombre del equipo:

Integrante y rol:

katerin yamileth serrano majano - Lider del proyecto Jr., diseñadora y desarrolladora tecnico del proyecto.

Fecha de entrega: FASE 0: Onboarding y planificacion: del 23 de septiembre al 4 de octubre FASE 1: Analisis de casos de uso e intenciones del chatbot : del 05 al 18 de octubre

Resumen ejecutivo.

Qué se realizó: Este repositorio contiene la documentación, flujos y scripts de integración para el chatbot automatizado del *Centro de Servicios Digitales Ciudadanos (CSDC). El sistema está diseñado para reducir los tiempos de respuesta y mitigar la sobrecarga de atención manual mediante el uso de **Dialogflow CX, *WhatsApp y Google Sheets.

Estado actual del proyecto: Actualmente dicho proyecto esta en proceso de desarrollo.

## 1. Asignación de Roles del Equipo
* **Líder de Proyecto Jr.:** Coordinación de backlog, cumplimiento de fases y enlace con tutoría.
* **Diseñador/a de Conversaciones Jr. (CX/UX):** Definición de intenciones, árbol de diálogo, tono y mensajes.
* **Ingeniero/a de Integración Cloud Jr.:** Configuración de Dialogflow CX y canales (Telegram/Web).
* **Desarrollador/a de Automatización Jr.:** Implementación de webhooks, almacenamiento en Google Sheets y notificaciones.
* **QA / Documentador Técnico Jr.:** Matriz de pruebas conversacionales, bitácora semanal e informe final.

---

## 2. Inventario de Recursos Cloud y Herramientas

| Recurso | Plataforma / Proveedor | Responsable | Uso Previsto | Límites y Observaciones |
| :--- | :--- | :--- | :--- | :--- |
| **Plataforma Conversacional** | Dialogflow CX / | Ing. Integración Cloud Jr. | Motor NLP, manejo de intenciones, entidades y rutas de páginas. | Free Tier de GCP / Créditos educativos. |
| **Plataforma Automatización** | / Self-hosted | Dev Automatización Jr. | Orquestación de flujos, webhook middleware y conexiones HTTP. | Instancia de prueba controlada. |
| **Canal de Mensajería** |  / Telegram API | Diseñador CX / Ing. Integración | Interfaz conversacional con el ciudadano. | Sandbox con datos simulados. |
| **Almacenamiento Backend** | Google Sheets API | Dev Automatización Jr. | Registro estandarizado de solicitudes e incidencias. | Sin datos personales reales. |
| **Control de Versiones** | GitHub | Líder de Proyecto Jr. | Repositorio centralizado de código, flujos JSON y documentación `/docs`. | Repositorio público/privado con `.gitignore`. |
| **Herramientas de Testing** | cURL / Postman | QA / Documentador Jr. | Validación de payloads JSON y endpoints de fulfillment. | Pruebas de integración asincrónicas. |

---

## 3. Acuerdos de Trabajo Asincrónico
* **Canales de Comunicación:** Discord / WhatsApp para avisos rápidos; GitHub Issues para asignación de tareas.
* **Control de Commits:** Commits descriptivos con prefijos (`feat:`, `docs:`, `fix:`, `test:`).
* **Protección de Datos:** Estrictamente prohibido incluir tokens, llaves privadas o claves API en el código fuente (uso de `.env.example`).



# Plan de Recursos Tecnológicos (Fase 0)
**Proyecto:** Chatbot Asistente en la Nube para Atención Ciudadana (CSDC)  
**Cliente:** Centro de Servicios Digitales Ciudadanos (CSDC) - Secretaría de Innovación  
**Unidad Ejecutora:** Unidad de Proyectos ESIT (Célula Conversacional Cloud)  


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




# Bitácora de Trabajo Semanal (Semanas 1 a 10)
**Proyecto:** Chatbot Asistente en la Nube para Atención Ciudadana (CSDC)  

---

## Control Semanal de Actividades (Plan de 10 Semanas)

### Semana 1 - Fase 0: Onboarding y Planificación
* **Actividades:** Lectura del requerimiento institucional del CSDC, constitución de la célula conversacional, asignación de roles y elaboración del Plan de Recursos Tecnológicos.
* **Entregables:** `Plan_de_Recursos_Tecnologicos.md` y estructura de repositorio GitHub creada.

### Semanas 2 y 3 - Fase 1: Análisis y Definición de Contenido
* **Actividades:** Levantamiento de casos de uso prioritarios (Simple.sv, Identidad Digital, SAC, ESIT). Redacción de las frases de entrenamiento y respuestas institucionales.
* **Entregables:** `Documento_de_Analisis_Casos_de_Uso.md` y `Catalogo_de_Intenciones_y_Respuestas.md`.

### Semanas 4 y 5 - Fase 2: Diseño y Configuración Base
* **Actividades:** Elaboración de diagramas de flujo conversacional y diseño de arquitectura cloud. Configuración inicial del agente en Dialogflow CX y exportación del borrador JSON.
* **Entregables:** `Documento_de_Diseno_y_Arquitectura.md` y `flows/dialogflow_cx_agent.json`.

### Semanas 6, 7 y 8 - Fase 3: Implementación, Webhooks y Pruebas
* **Actividades:** Desarrollo del webhook backend en Python (`src/main.py`), conexión con Google Sheets API y ejecución de la matriz de pruebas conversacionales (QA).
* **Entregables:** `src/main.py`, `flows/n8n_workflow_csdc.json` y `Matriz_de_Pruebas_Conversacionales.md`.

### Semanas 9 y 10 - Fase 4: Cierre Técnico y Entrega Profesional
* **Actividades:** Redacción del informe final, revisión de limitaciones y empaquetado del repositorio completo para entrega institucional y publicación en GitHub.
* **Entregables:** `Informe_Profesional_Final.md` y `README.md` principal.

# Catálogo de Intenciones y Respuestas (Fase 1 y 2)
**Proyecto:** Chatbot Asistente en la Nube para Atención Ciudadana (CSDC)  

---

## 1. Intent: `welcome_intent`
* **Descripción:** Saludo inicial y presentación del menú principal.
* **Frases de Entrenamiento (*Training Phrases*):**
  * "Hola", "Buenas tardes", "Inicio", "Necesito ayuda con trámites", "¿Qué consultas puedo hacer?"
* **Respuesta Base:**
  > "¡Hola! 👋 Bienvenido al Asistente Virtual del Centro de Servicios Digitales Ciudadanos (CSDC). Estoy para orientarte las 24/7.\n\nPor favor, selecciona o escribe la opción que necesitas:\n1. 📄 Consultar Trámites en Simple.sv\n2. 🆔 Crear Identidad Digital / Login.gob.sv\n3. 📝 Registrar Caso o Denuncia (SAC)\n4. 🎓 Cursos Gratuitos de la ESIT\n5. 📞 Soporte y Atención Humana"

---

## 2. Intent: `consultar_tramite_simplesv`
* **Entidades Extraídas:** `$tipo_tramite` (penales, policiales, pasaporte, apostilla, DUI).
* **Frases de Entrenamiento:**
  * "¿Cuánto valen los antecedentes penales?"
  * "Requisitos para solvencia de la policía"
  * "Precio del pasaporte en Centroamérica y Estados Unidos"
  * "¿Cómo apostillar una partida de nacimiento?"
* **Respuestas Mapeadas:**
  * **Antecedentes Penales:** Costo $3.00 USD en Simple.sv.
  * **Antecedentes Policiales:** Costo $3.50 USD en Simple.sv.
  * **Pasaporte Exterior:** $40.00 USD Centroamérica; $60.00 USD resto del mundo.
  * **Apostilla Electrónica / DUI:** Trámites 100% gratuitos en línea.

---

## 3. Intent: `crear_identidad_digital`
* **Frases de Entrenamiento:**
  * "¿Cómo creo mi perfil digital?"
  * "Pasos para registrar mi cuenta en login.gob.sv"
  * "No me llega el código SMS para mi Identidad Digital"
* **Respuesta Base:**
  > "Para crear tu Identidad Digital:\n1. Ingresa a simple.sv o login.gob.sv y haz clic en 'Crear cuenta'.\n2. Digita tu número de DUI y acepta términos.\n3. Ingresa el número de folio de tu DUI.\n4. Verifica tu correo electrónico con el código enviado.\n5. Verifica tu número telefónico vía SMS.\n6. Asigna tu contraseña segura."

---

## 4. Intent: `registrar_denuncia_sac`
* **Parámetros Requeridos:** `$nombre_ciudadano`, `$correo_contacto`, `$telefono_contacto`, `$sector`, `$detalle_caso`.
* **Frases de Entrenamiento:**
  * "Quiero poner un reclamo sobre un centro de salud"
  * "Denuncia anónima en el SAC para educación"
  * "Registrar solicitud de información pública"
* **Acción Fulfillment:** Ejecuta Webhook Backend para guardar los datos en Google Sheets.

---

## 5. Intent: `sys.no-match-default` (Fallback)
* **Respuesta Base:**
  > "Disculpa, no logré comprender tu consulta. Por favor, intenta redactar tu pregunta de forma distinta o selecciona una de nuestras opciones principales: Trámites Simple.sv, Identidad Digital, SAC o Cursos ESIT."

# Documento de Análisis y Casos de Uso (Fase 1)
**Proyecto:** Chatbot Asistente en la Nube para Atención Ciudadana (CSDC)  

---

## 1. Contexto Institucional y Problemática Detectada
El **Centro de Servicios Digitales Ciudadanos (CSDC)** opera como primer punto de contacto entre la población y las instituciones públicas de El Salvador. 
Actualmente, la atención se realiza de forma manual mediante agentes humanos, generando:
1. **Tiempos de respuesta elevados:** Colas de mensajes en horas pico.
2. **Sobrecarga del personal:** Redundancia al responder preguntas frecuentes (FAQ) repetitivas sobre trámites en **Simple.sv**, **Identidad Digital** o **SAC**.
3. **Falta de trazabilidad:** Dificultad para construir estadísticas consolidadas sobre las inquietudes ciudadanas.

---

## 2. Definición de Usuarios Finales
* **Ciudadano General:** Requiere información rápida 24/7 sobre trámites en Simple.sv (costos, requisitos, tiempos).
* **Diáspora Salvadoreña:** Consulta sobre pasaportes en el exterior y apostillado de partidas de nacimiento.
* **Estudiante / Profesional:** Interesado en capacitaciones continuas gratuitas de la ESIT.
* **Usuario Interno CSDC:** Recibe solicitudes estandarizadas y registradas en Google Sheets.

---

## 3. Matriz de Casos de Uso Prioritarios

| ID Caso de Uso | Nombre del Caso de Uso | Actor Principal | Descripción Breve | Resultado Esperado |
| :--- | :--- | :--- | :--- | :--- |
| **CU-01** | Consultar Requisitos y Costos de Trámites | Ciudadano / Diáspora | Obtener información inmediata de antecedentes penales, policiales, pasaporte y apostilla. | Respuesta clara con montos en USD y enlace a Simple.sv. |
| **CU-02** | Guía de Registro de Identidad Digital | Ciudadano | Recibir la guía paso a paso para crear cuenta en `login.gob.sv` / Simple.sv. | Instrucciones de los 6 pasos con verificación DUI/SMS. |
| **CU-03** | Registro de Incidencia / Denuncia SAC | Ciudadano | Capturar datos del sector (Salud/Educación), departamento, institución y descripción. | Fila agregada en Google Sheets y confirmación al usuario. |
| **CU-04** | Consulta de Oferta Académica ESIT | Estudiante / Servidor | Informar sobre diplomados y cursos asincrónicos gratuitos de la ESIT. | Catálogo de cursos (Scrum, MySQL, Gobernanza) y link. |
| **CU-05** | Canal de Soporte Humano | Ciudadano | Proporcionar correos y números telefónicos de atención oficial. | Directorio de contacto (`contacto@simple.sv`, WhatsApp SAC). |

 Documento de Diseño y Arquitectura (Fase 2)
**Proyecto:** Chatbot Asistente en la Nube para Atención Ciudadana (CSDC)  

---

## 1. Arquitectura General del Sistema
El prototipo conversacional se estructura en cuatro capas desacopladas:

```
[ Ciudadano / Usuario ] 
        │
        ▼ (Mensajes / Telegram / Webchat)
[ Canal de Mensajería ]
        │
        ▼ (Webhook HTTP / JSON API)
[ Dialogflow CX / n8n NLP Engine ] ──(Fulfillment Request)──► [ Webhook Backend / Cloud Function ]
                                                                       │
                                                                       ▼
                                                             [ Google Sheets API ]
```

---

## 2. Diagrama de Flujo Conversacional (Árbol de Diálogo)

```
                       [ Inicio / Welcome ]
                               │
       ┌───────────────────────┼───────────────────────┐
       ▼                       ▼                       ▼
[ Simple.sv ]          [ Identidad Digital ]        [ SAC / Denuncias ]
   │                       │                           │
   ├── Antecedentes        └── Paso a paso DUI         ├── Captura Sector/Institución
   ├── Pasaportes              SMS & Email             ├── Captura Datos Contacto
   └── Apostillas                                      └── Webhook -> Google Sheets
```

---

## 3. Especificación de Interfaces e Integraciones
* **Interfaz de Entrada:** Payload de Dialogflow CX en formato JSON conteniendo `sessionInfo.parameters`.
* **Procesamiento Middleware:** Servicio en Python (GCP Cloud Functions / Cloud Run) que valida la firma del request y procesa la lógica.
* **Interfaz de Salida (Almacenamiento):** Inserción mediante API OAuth2 en la hoja de cálculo `Registro_Solicitudes_CSDC` con columnas: `[Fecha, Nombre, Correo, Teléfono, Sector, Detalle, Estado]`.

 


## 2. Objetivos Alcanzados
1. **Automatización de FAQ (24/7):** Resolución inmediata sobre costos y requisitos de más de 90 trámites en Simple.sv, pasaportes y certificados.
2. **Estandarización de Registros:** Captura estructurada de solicitudes para el Sistema de Atención Ciudadana (SAC).
3. **Despliegue Multi-Canal:** Soporte para interacción vía Bot de Telegram y widget web.
4. **Documentación Completa:** Publicación de especificaciones de arquitectura, flujos JSON y bitácoras de trabajo en GitHub.

---

## 3. Demostración del Flujo Operativo
* **Paso 1:** El ciudadano inicia conversación en Telegram/Web y recibe menú principal.
* **Paso 2:** Selecciona la consulta de un trámite o el registro de una incidencia SAC.
* **Paso 3:** En caso de denuncia SAC, la plataforma recopila parámetros (nombre, correo, teléfono, sector).
* **Paso 4:** El webhook procesa los parámetros en milisegundos y almacena la información en la hoja de cálculo institucional de Google Sheets.

---

## 4. Limitaciones Actuales y Recomendaciones Futuras
* **Limitación:** El prototipo no consulta directamente APIs de bases de datos gubernamentales en tiempo real para verificar el estado interno de expedientes institucionales.
* **Recomendación Futura:** Integrar autenticación OAuth2 directa con la plataforma de Identidad Digital (`login.gob.sv`) para autenticación avanzada y habilitar módulos de inteligencia artificial generativa (Vertex AI / Gemini) para manejar consultas complejas no estructuradas.

  # Matriz de Pruebas Conversacionales (Fase 3)
**Proyecto:** Chatbot Asistente en la Nube para Atención Ciudadana (CSDC)  

---

## Resultados del Protocolo de Pruebas (QA Conversacional)

| ID Test | Categoría / Escenario | Entrada del Usuario | Intención Detectada | Resultado Esperado en Respuesta | Estado |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **TC-01** | Camino Feliz - Antecedentes | "¿Cuánto cuestan los antecedentes penales?" | `consultar_tramite_simplesv` | Informa precio de $3.00 USD y enlace a Simple.sv. | **PASS** |
| **TC-02** | Variación Lenguaje - Policiales | "Quiero mi papel de la policía" | `consultar_tramite_simplesv` | Detecta trámite de solvencia policial ($3.50 USD). | **PASS** |
| **TC-03** | Tolerancia a Tipeo - Registro | "como ago para crear mi cuuenta en login.gob" | `crear_identidad_digital` | Muestra guía de 6 pasos de registro DUI/SMS. | **PASS** |
| **TC-04** | Consulta Gratuita - Apostilla | "¿Es gratis la apostilla de partida de nacimiento?" | `consultar_tramite_simplesv` | Confirma que el apostillado electrónico es $0.00 USD. | **PASS** |
| **TC-05** | Flujo Completo SAC - Webhook | "Quiero reportar un problema en un hospital de San Salvador" | `registrar_denuncia_sac` | Solicita datos, ejecuta webhook y guarda fila en Google Sheets. | **PASS** |
| **TC-06** | Fallback - Fuera de Ámbito | "¿A qué hora juega la selección de fútbol?" | `sys.no-match-default` | Mensaje de fallback orientando a opciones institucionales. | **PASS** |
| **TC-07** | Inyección / Basura | "asdfghjkl 12345" | `sys.no-match-default` | Mantiene estabilidad de sesión y despliega menú principal. | **PASS** |
| **TC-08** | Prueba de Carga Webhook | Petición HTTP POST simultánea (10 req/s) | `registrar_denuncia_sac` | HTTP 200 OK en <500ms; escrituras exitosas en Sheets. | **PASS** |


nombre: "CSDC_Chatbot_Atencion_Ciudadana_CX",
  "defaultLanguageCode": "es",
 "America/El_Salvador",

  "description": "Prototipo Lite de Chatbot Asistente en la Nube para el Centro de Servicios Digitales Ciudadanos (CSDC)",
  "intents": 
    
      "displayName": "welcome_intent",

        "Hola", "Buenas tardes", "Inicio", "Necesito información sobre trámites", "¿Qué consultas puedo hacer?"
      
      "responses":
        "¡Hola! 👋 Bienvenido al Asistente Virtual del Centro de Servicios Digitales Ciudadanos (CSDC). ¿En qué puedo ayudarte hoy?\n1. Trámites en Simple.sv\n2. Crear Identidad Digital\n3. Registrar Caso / Denuncia (SAC)\n4. Cursos ESIT\n5. Soporte Técnico"
      
   consultor: "consultar_tramite_simplesv",
        "¿Cuánto cuestan los antecedentes penales?",
        "Requisitos para solvencia policial",
        "Pasaporte en el exterior",
        "Apostillado electrónico",
        "Trámites disponibles en Simple.sv"
      
    
   "crear_identidad_digital",
        "¿Cómo creo mi cuenta en Simple.sv?",
        "No puedo iniciar sesión en login.gob.sv",
        "Pasos para registrar mi Identidad Digital",
        "¿Qué necesito para registrarme con DUI?"
  
  
  
"registrar_denuncia_sac",
    
"Quiero poner un reclamo sobre un hospital",
"Denuncia anónima en el SAC",
"Registrar caso para educación o salud",
 "Consultar estado de expediente SAC"
  
  
   "informacion_esit",
        "Cursos de la ESIT",
        "Capacitación en Scrum o MySQL",
        "Escuela Superior de Innovación y Tecnología",
        "Cursos gratuitos de gobernanza digital"
      
      "contacto_soporte",
      "trainingPhrases":
        "Hablar con un operador humano",
        "Correo de ayuda Simple.sv",
        "Teléfono del SAC",
        "Atención al cliente"


  "CSDC_Chatbot_Atencion_Ciudadana_CX",
"es",
 "America/El_Salvador",
  "description": "Prototipo Lite de Chatbot Asistente en la Nube para el Centro de Servicios Digitales Ciudadanos (CSDC)",
  "intents":
    
      "displayName": "welcome_intent",
      "trainingPhrases": 
        "Hola", "Buenas tardes", "Inicio", "Necesito información sobre trámites", "¿Qué consultas puedo hacer?"
    
      "responses": 
        "¡Hola! 👋 Bienvenido al Asistente Virtual del Centro de Servicios Digitales Ciudadanos (CSDC). ¿En qué puedo ayudarte hoy?\n1. Trámites en Simple.sv\n2. Crear Identidad Digital\n3. Registrar Caso / Denuncia (SAC)\n4. Cursos ESIT\n5. Soporte Técnico"
  
      "displayName": "consultar_tramite_simplesv",
      "trainingPhrases": [
        "¿Cuánto cuestan los antecedentes penales?",
        "Requisitos para solvencia policial",
        "Pasaporte en el exterior",
        "Apostillado electrónico",
    
      "displayName": "crear_identidad_digital",
      "trainingPhrases": 
        "¿Cómo creo mi cuenta en Simple.sv?",
        "No puedo iniciar sesión en login.gob.sv",
        "Pasos para registrar mi Identidad Digital",
        "¿Qué necesito para registrarme con DUI?"
    
      "displayName": "registrar_denuncia_sac",
      "trainingPhrases": 
        "Quiero poner un reclamo sobre un hospital",
        "Denuncia anónima en el SAC",
        "Registrar caso para educación o salud",
        "Consultar estado de expediente SAC"
    
      "displayName": "informacion_esit",
      "trainingPhrases": 
        "Cursos de la ESIT",
        "Capacitación en Scrum o MySQL",
        "Escuela Superior de Innovación y Tecnología",
        "Cursos gratuitos de gobernanza digital"
    
      "displayName": "contacto_soporte",
      "trainingPhrases": 
        "Hablar con un operador humano",
        "Correo de ayuda Simple.sv",
        "Teléfono del SAC",
        "Atención al cliente"

import os
import json

def handle_webhook_request(req_data):
    """
    Procesador de Webhook para Dialogflow CX / n8n
    """
    session_info = req_data.get("sessionInfo", {})
    parameters = session_info.get("parameters", {})

    nombre = parameters.get("nombre_ciudadano", "Anónimo")
    correo = parameters.get("correo_contacto", "N/A")
    sector = parameters.get("sector", "General")

    response_text = f"Solicitud registrada para {nombre} ({sector}). Contacto: {correo}"

    return {
        "fulfillment_response": {
            "messages": [
                {
                    "text": {
                        "text": [response_text]
                    }
                }
            ]
        }
    }

curl -X POST "$WEBHOOK_URL" \
     -H "Content-Type: application/json" \
     -d @tests/test_webhook_payload.json

echo -e "\n=== Prueba Finalizada ==="


