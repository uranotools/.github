<div align="center">

# 🌌 Urano Tools

### *The Open-Source Autonomous AI Agents & Cyber Defense Ecosystem*

[![Website](https://img.shields.io/badge/Official_Site-uranoai.com-00D4FF?style=for-the-badge&logo=googlechrome&logoColor=white)](https://uranoai.com)
[![NPM Urano Guard](https://img.shields.io/npm/v/@uranotools/urano-guard?style=for-the-badge&color=cb0000&logo=npm&label=urano-guard)](https://www.npmjs.com/package/@uranotools/urano-guard)
[![GitHub Org](https://img.shields.io/badge/Organization-uranotools-black?style=for-the-badge&logo=github)](https://github.com/uranotools)
[![Medium](https://img.shields.io/badge/Blog-Medium-12100E?style=for-the-badge&logo=medium)](https://uranoproject.medium.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)](https://opensource.org/licenses/MIT)

<p align="center">
  <b>Construyendo el futuro de la Inteligencia Artificial Autónoma, Agentes Locales Soberanos y Ciberdefensa Perimetral de Alta Resiliencia.</b>
</p>

</div>

---

## ⚡ Nuestra Visión

**Urano Tools** es la división Open Source de **Urano Project**. Desarrollamos y liberamos herramientas de grado de ingeniería para desarrolladores, investigadores y empresas que construyen con **agentes de IA autónomos**.

Creemos firmemente que:
> *"La Inteligencia Artificial no debe ser un servicio cerrado que consumes. Debe ser una tecnología soberana que posees, controlas y proteges."*

---

## 🛡️ Arquitectura del Ecosistema

```mermaid
flowchart LR
    classDef cyber fill:#1e1b4b,stroke:#818cf8,stroke-width:2px,color:#fff;
    classDef agent fill:#0f172a,stroke:#38bdf8,stroke-width:2px,color:#fff;
    classDef proto fill:#064e3b,stroke:#34d399,stroke-width:2px,color:#fff;

    EXTERNAL([🌐 Tráfico / Webhooks / Prompts]) --> GUARD[🛡️ Urano Guard<br/>AI WAF & Perimeter Shield]:::cyber
    
    GUARD -- "Tráfico Sanitizado (<1ms)" --> DESKTOP[🖥️ Urano Desktop<br/>Laboratorio Multi-Agente Local]:::agent
    
    DESKTOP <--> ACP[📐 ACP-Urano Protocol<br/>Control Anti-Alucinación]:::proto
    DESKTOP <--> MCP[🧩 MCP Plugins Ecosystem<br/>Tools / FS / Shell / Vision]:::agent
```

---

## 🚀 Proyectos Principales

### 1. 🛡️ [`urano-guard`](https://github.com/uranotools/urano-guard) *(NUEVO)*
> **High-Resilience Security Gateway & AI WAF Middleware** para APIs, Webhooks y Aplicaciones con LLMs.

Diseñado para proteger infraestructuras críticas contra **agentes atacantes autónomos, inyecciones de prompts (Jailbreaks), evasiones por padding, ataques de repetición (Replay Attacks) y filtración de datos (PII)** con latencia sub-milisegundo (<1ms cache) y cero dependencias pesadas.

* 📦 **Instalación NPM:** `pnpm add @uranotools/urano-guard`
* 🔌 **Adaptadores:** Express, Fastify, Edge (Cloudflare/Vercel) y Node.js HTTP nativo.
* 🛑 **Resiliencia:** Circuit Breaker adaptativo con garantía *Fail-Open* y defensa activa (Tarpit + Honey-Tokens).

---

### 2. 🖥️ [`UranoDesktop`](https://github.com/uranotools/UranoDesktop)
> **Tu laboratorio personal y autónomo de Inteligencia Artificial.**

Entorno de ejecución de agentes locales con soporte nativo para **Model Context Protocol (MCP)**, visión por computadora, automatización de flujos de trabajo en segundo plano, sistema de memoria persistente y notificaciones del sistema.

* 🤖 Orquestación multi-agente en tiempo real.
* 🧩 Arquitectura modular extensible mediante plugins.
* 🔒 Soberanía de datos: tus herramientas y modelos corren en tu entorno.

---

### 3. 📐 [`ACP-Urano`](https://github.com/uranotools/ACP-Urano)
> **Agent Context Protocol — Protocolo determinista anti-alucinaciones.**

Estándar de comunicación y estructuración de contexto diseñado para forzar a los agentes de IA a actuar de manera verificable, reduciendo drásticamente las alucinaciones en tareas operativas complejas.

---

## 🗂️ Matriz de Repositorios

| Repositorio | Descripción | Tipo | Estado |
|---|---|:---:|:---:|
| **[urano-guard](https://github.com/uranotools/urano-guard)** | Security Gateway & AI WAF Middleware (TypeScript / NPM) | `Cybersecurity / SDK` | 🚀 **Activo (v1.0.0)** |
| **[UranoDesktop](https://github.com/uranotools/UranoDesktop)** | Aplicación principal y runtime multi-agente MCP | `Core / Runtime` | 🚀 **Activo** |
| **[ACP-Urano](https://github.com/uranotools/ACP-Urano)** | Protocolo de contexto y control de alucinaciones | `Protocol / Spec` | 🚀 **Activo** |
| **[my-ainewsletter-template](https://github.com/uranotools/my-ainewsletter-template)** | Plantilla para crear newsletters de IA 100% autónomas | `Template / Workflow` | 🟢 **Activo** |
| **[my-ainewsletter-plugin](https://github.com/uranotools/my-ainewsletter-plugin)** | Plugin MCP para publicación y curación automatizada | `MCP Plugin` | 🟢 **Activo** |

---

## 🚀 Inicio Rápido con Urano Guard

Protege tu API o agente de IA en 3 líneas de código:

```ts
import express from 'express';
import { createUranoGuard } from '@uranotools/urano-guard';

const app = express();
app.use(express.json());

// Activa el escudo de ciberdefensa perimetral
const guard = createUranoGuard({
    securityMode: 'block_threats',
    inspectors: { promptInjection: true, paddingEvasion: true, piiDataMasking: true }
});

app.use(guard.express());

app.post('/api/agent', (req, res) => {
    res.json({ message: 'Request seguro y libre de amenazas' });
});

app.listen(3000);
```

---

## 🤝 Comunidad & Contribuciones

Construimos en público y damos la bienvenida a desarrolladores, investigadores de seguridad y entusiastas de los agentes autónomos:

* 💡 **Reporta vulnerabilidades o reglas de bypass:** [Política de Seguridad (SECURITY.md)](https://github.com/uranotools/urano-guard/blob/main/SECURITY.md)
* 🧩 **Crea nuevos Plugins MCP:** Revisa la documentación en [UranoDesktop Docs](https://github.com/uranotools/UranoDesktop)
* 📖 **Tutoriales y Casos de Uso:** [Blog en Medium](https://uranoproject.medium.com)
* 🐦 **Síguenos en X (Twitter):** [@uranoproject](https://x.com/uranoproject)

---

<div align="center">

**Hecho con pasión por Andy E. Gómez y la comunidad Urano Project.**  
🇬🇹 *Guatemala al mundo.*

</div>
