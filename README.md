# Web Security Auditor v5.0

Auditor de seguridad web **100% pasivo y no invasivo** desarrollado en Python.  
Analiza sitios web públicos, detecta vulnerabilidades y genera informes profesionales automáticamente.

---

## ¿Qué hace?

Evalúa 11 áreas de seguridad sin realizar ningún ataque ni modificación al sitio:

- **Cabeceras HTTP** — HSTS, CSP, X-Frame-Options, y más
- **SSL/TLS** — protocolo, cifrado, vencimiento del certificado
- **Puertos y WAF** — servicios expuestos, banner grabbing, detección de Cloudflare
- **DNS y Email** — SPF, DKIM, DMARC, DNSSEC, subdominios
- **Tecnologías y CVEs** — stack detectado, versiones expuestas
- **Archivos públicos** — 38+ rutas sensibles (.env, .git, backups, etc.)
- **Secretos en JavaScript** — credenciales o API keys expuestas
- **Integridad de scripts externos (SRI)**
- **Contenido y formularios** — mixed content, open redirect, CSRF
- **Reputación** — listas negras DNSBL, URLScan, antigüedad del dominio
- **Formulario de login** — CSRF, autocomplete, rate limiting, enumeración de usuarios

---

## Informes generados

Por cada auditoría se generan automáticamente 4 archivos:

| Archivo | Descripción |
|---|---|
| `informe.pdf` | Informe técnico completo — 27 páginas, mapeo OWASP, referencias CWE |
| `informe_ejecutivo.pdf` | Resumen ejecutivo — 2 páginas en lenguaje no técnico para el dueño del negocio |
| `informe.html` | Versión web interactiva del informe completo |
| `informe.json` | Datos crudos para integración con otros sistemas |

---

---

## Ejemplo de informe

Los archivos en este repositorio corresponden a un análisis de **example.com** realizado el 17 de mayo de 2026.

**Resultado:** B — 80/100 | 1 crítico · 8 advertencias · 15 correctos

Para ver cómo trabaja el sistema sin descargar archivos, puede revisar la demostración online o abrir los archivos directamente desde el repositorio:

* 🖥️ **[VER REPORTE INTERACTIVO EN VIVO (Recomendado)](https://ignacio-ledesma.github.io/web-security-auditor/)**
* 📄 **[Ver Resumen Ejecutivo en PDF](./example_com_20260517_193646_v5_ejecutivo.pdf)** *(Ideal para el dueño del negocio)*
* 🗂️ **[Ver Informe Técnico Completo PDF](./example_com_20260517_193646_v5.pdf)** *(27 páginas de análisis profundo)*
* ⚙️ **[Ver Estructura de Datos JSON](./example_com_20260517_193646_v5.json)**

---

## Servicio de auditoría

Ofrezco auditorías de seguridad web para empresas y negocios con presencia online.

**Precio: USD 100 por sitio**

Incluye informe técnico completo + informe ejecutivo listo para compartir con dirección o clientes.

Ideal para PYMEs, estudios profesionales, clínicas, e-commerce y cualquier negocio con sitio web que quiera conocer su postura de seguridad sin contratar un equipo de IT.

📩 Contacto: [LinkedIn — Ignacio Ledesma](https://www.linkedin.com/in/ignacio-ledesma-3a2523324/)

---

## Tecnologías

Python · ReportLab · dnspython · cryptography · ThreadPoolExecutor · requests

---

*Análisis pasivo — sin ataques, sin modificaciones, sin riesgo para el sitio auditado.*
