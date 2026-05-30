# 🏭 Sentinel Factory — Motor de Agentes Trabajadores Digitales

SaaS multi-tenant para agencias de marketing. Permite crear, gestionar y revender agentes de IA personalizados a PYMEs sin tocar una sola línea de código.

[Demo en vivo](#)

##  ¿Qué es Sentinel Factory?

Sentinel Factory es un motor donde la agencia entra, ingresa la URL de un cliente, y en 30 segundos tiene un agente listo: con los servicios, precios, horarios y personalidad de ese negocio específico.

* **Multi-tenant:** Administra docenas de agentes independientes desde un solo dashboard.
* **White-label total:** El cliente final solo ve su marca, sus colores y su personalidad. Sentinel Factory es invisible.
* **Agente, no chatbot:** No es un árbol de decisiones rígido. Es IA real que responde, agenda y captura leads.

### 📐 Arquitectura de Flujo de Datos

Transparencia total: en la demo, cada mensaje permite ver la latencia en milisegundos de cada capa del motor:

```text
Usuario 
   │
   ▼
[AI Shield (Filtro de Seguridad)]
   │
   ▼
[Clasificador de Intención]
   │
   ▼
[RAG: Ingesta de pgvector + Búsqueda Semántica]
   │
   ▼
[LLM (Claude / OpenAI) + Integración API Calendar]
   │
   ▼
[PII Sanitizer / Privacy Shield]
   │
   ▼
Respuesta Segura
```
 El "Autopilot Engine": Tu motor de ventas
La plataforma no solo crea bots, los vende por ti:

Prospección Masiva: Escanea 100 negocios diarios en Google Maps (categoría a elección).

Generación Automática: Crea un bot de demo para cada prospecto usando su propia web.

Prueba Social Instantánea: Genera un GIF mostrando el bot respondiendo preguntas reales del negocio.

Cold Emailing: Envía un email al dueño con el GIF incrustado. El dueño ve su propio bot funcionando en 10 segundos.

 Lo que hace el agente
RAG Estricto: Responde basándose en los documentos (PDFs, FAQs) del negocio. Si no sabe, no inventa.

Agendamiento: Conectado a Google Calendar. Gestiona disponibilidad y confirma citas en la conversación.

Captura de Leads: Extrae nombre, teléfono, email e interés; notifica al dueño por correo al instante.

Escala a Humano: Si el cliente lo pide, despliega un botón directo al WhatsApp del negocio.

Auto-aprendizaje: Registra las preguntas donde el bot falló. La agencia enseña la respuesta correcta y el bot la guarda para siempre.

Calidad Técnica y Stack
Engine: Python 3.13 + FastAPI async.

Base de Datos: PostgreSQL con pgvector para búsqueda semántica.

Automatización: Playwright para scraping, Resend para correos transaccionales, Stripe para pagos.

Deploy: Docker-Compose probado en Railway.

 Modelo de Negocio para la Agencia
Costo: Plan Professional (20 agentes) = $299/mes.

Venta sugerida: $150–$300 USD/mes por cliente.

Resultado: Con solo 10 clientes, la agencia genera $2.000 USD de ingresos y un margen neto de $1.700 USD.

 Instalación Rápida
```
Bash
git clone [https://github.com/dannisk9/sentinel](https://github.com/dannisk9/sentinel)
cd sentinel
cp .env.example .env
# Edita .env con tus keys
docker-compose up --build
```


App en http://localhost:8000

Dashboard en http://localhost:8000/dashboard.html

Licencia y Compra (Acquire.com)
Producto propietario, pago único. Desde $5.500 USD.

Incluye código fuente completo, 30 días de soporte, llamada de onboarding y documentación técnica.

¿Necesitas integraciones a medida (WhatsApp API, voz con ElevenLabs, apps móviles)? Consulta por tarifas de desarrollo post-venta.
