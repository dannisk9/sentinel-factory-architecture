# 🏭 Sentinel Factory — Motor de Agentes Trabajadores Digitales

> **SaaS multi-tenant para agencias de marketing.** Permite crear, gestionar y revender agentes de IA personalizados a PYMEs sin tocar una sola línea de código.

---

## 🤖 ¿Qué es Sentinel Factory?
Sentinel Factory es un motor donde la agencia ingresa la URL de un cliente y, **en solo 30 segundos**, genera un agente listo con los servicios, precios, horarios y personalidad de ese negocio específico.

*   👥 **Multi-tenant:** Administra docenas de agentes independientes desde un solo dashboard.
*   🎭 **White-label total:** El cliente final solo ve su marca, sus colores y su personalidad. Sentinel Factory es invisible.
*   🧠 **Agente, no chatbot:** No es un árbol de decisiones rígido. Es IA real que responde, agenda y captura leads.

---

## 📐 Arquitectura de Flujo de Datos
*Transparencia total: en la demo, cada mensaje permite ver la latencia en milisegundos de cada capa del motor.*

```mermaid
graph TD
    A[👤 Usuario] --> B[🛡️ AI Shield - Filtro de Seguridad]
    B --> C[🎯 Clasificador de Intención]
    C --> D[📚 RAG: Ingesta de pgvector + Búsqueda Semántica]
    D --> E[🤖 LLM Claude / OpenAI + API Calendar]
    E --> F[🔒 PII Sanitizer / Privacy Shield]
    F --> G[🚀 Respuesta Segura]
```

---

## 🚀 El "Autopilot Engine": Tu Motor de Ventas
La plataforma no solo crea bots, los vende por ti de forma automatizada:

1.  🔍 **Prospección Masiva:** Escanea 100 negocios diarios en Google Maps (categoría a elección).
2.  ⚙️ **Generación Automática:** Crea un bot de demo para cada prospecto usando su propia web.
3.  📸 **Prueba Social Instantánea:** Genera un GIF mostrando el bot respondiendo preguntas reales del negocio.
4.  📧 **Cold Emailing:** Envía un email al dueño con el GIF incrustado. ¡El dueño ve su propio bot funcionando en 10 segundos!

---

## ✨ Características del Agente

*   🎯 **RAG Estricto:** Responde basándose en los documentos (PDFs, FAQs) del negocio. Si no sabe, no inventa.
*   📅 **Agendamiento:** Conectado a Google Calendar. Gestiona disponibilidad y confirma citas en la conversación.
*   📥 **Captura de Leads:** Extrae nombre, teléfono, email e interés; notifica al dueño por correo al instante.
*   📞 **Escala a Humano:** Si el cliente lo pide, despliega un botón directo al WhatsApp del negocio.
*   📈 **Auto-aprendizaje:** Registra las preguntas donde el bot falló. La agencia enseña la respuesta correcta y el bot la guarda para siempre.

---

## 🧪 Calidad Técnica y Stack Engine

*   🐍 **Backend:** Python 3.13 + FastAPI (async).
*   🗄️ **Base de Datos:** PostgreSQL con `pgvector` para búsqueda semántica.
*   🤖 **Automatización:** Playwright (scraping), Resend (correos transaccionales), Stripe (pagos).
*   🐋 **Deploy:** Docker-Compose probado en Railway.

---

## 💰 Modelo de Negocio para la Agencia


| Concepto | Detalle |
| :--- | :--- |
| **Costo Plataforma** | Plan Professional (20 agentes) = **$299/mes** |
| **Venta Sugerida** | $150 – $300 USD/mes por cliente |
| **Rentabilidad** | Con solo 10 clientes, la agencia genera **$2,000 USD** de ingresos con un margen neto de **$1,700 USD**. |

---

## 💻 Instalación Rápida

```bash
# Clonar el repositorio
git clone https://github.com/dannisk9/sentinel
cd sentinel

# Configurar variables de entorno
cp .env.example .env
# Nota: Edita el archivo .env con tus respectivas API keys

# Levantar servicios
docker-compose up --build
```

---

## 💳 Licencia y Compra (Acquire.com)

Producto propietario, pago único desde **$5,500 USD**. 

**¿Qué incluye?**
*   📦 Código fuente completo.
*   🛠️ 30 días de soporte garantizado.
*   📞 Llamada de onboarding + Documentación técnica.

*¿Necesitas integraciones a medida (WhatsApp API, voz con ElevenLabs, apps móviles)? Consulta por nuestras tarifas de desarrollo post-venta.*

