# ARQUITECTURA GEORGE ↔ MAIA — Documento fundacional
**Fecha:** 2026-07-13
**Autor:** José Luis Espinosa (visión) · refinado con análisis estratégico

---

## PRINCIPIO RECTOR
Dos asistentes con el mismo motor de inteligencia, separación TOTAL de datos, contexto y propósito:
- **GEORGE** = cerebro personal privado. No se vende. Lo sabe todo de José Luis.
- **MAIA** = producto comercial. Cada cliente tiene el suyo. No sabe NADA de José Luis ni de otros clientes.

Regla de oro irrompible: **ningún dato personal de José Luis o de un cliente puede cruzar al otro lado.** George puede diseñar MAIA; MAIA jamás accede al contexto de George.

---

## 1. GEORGE — Asistente personal (privado)
**Misión:** director ejecutivo personal de José Luis.
**Rol respecto a MAIA:** arquitecto. George diseña, desarrolla y mejora MAIA. Recibe las órdenes .md de desarrollo.
**Requisitos técnicos:** memoria persistente propia (NUNCA en infraestructura de MAIA), acceso a servidores/repos como herramienta, credenciales y contexto separados del producto.

## 2. MAIA — Producto comercial (SaaS)
**Misión:** el empleado digital de un negocio — no chatbot, sistema que conoce la empresa y opera su gestión.
**Visión completa (largo plazo):** chat IA con memoria, gestión documental OCR, CRM, incidencias, mantenimiento preventivo, ERP ligero, agenda, facturación, informes, automatizaciones, WhatsApp/Telegram/Email, API, roles/permisos, multiempresa.

## 3. ANÁLISIS ESTRATÉGICO
**Riesgo evitado:** "automatizar todo para cualquier empresa" compite contra Salesforce/Holded/Odoo sin equipo ni foco.
**Ventaja real:** MAIA hoy es un GMAO móvil con IA para mantenimiento funcionando en un hospital real (Cas Serres) — OTs, preventivos automáticos, OCR contadores, checklists, fichajes GPS, alertas. Nadie lo tiene bien resuelto para pymes de mantenimiento/facility services, y José Luis conoce el sector desde dentro (EULEN, Cas Serres).
**Posicionamiento v1:** "El empleado digital de las empresas de mantenimiento" (GMAO + IA, vertical). Clientes tipo: mantenimiento, facility services, instaladoras, property managers de hoteles (Ibiza). El catálogo grande (CRM, facturación, ERP) se añade DESPUÉS, tirado por demanda real.

## 4. PLAN POR FASES
- **P0** — Terminar MAIA de Cas Serres al 100% (producto piloto + caso de éxito + banco de pruebas)
- **P1** — Productizar: multi-tenant real (instancia por cliente, aprovisionamiento automatizado), separar config específica de Cas Serres, onboarding (alta/CSV/QRs), marca/landing/precios (por técnico/mes), legal (RGPD, contrato, DPA)
- **P2** — 2-3 pilotos de pago en Ibiza/Baleares, precio reducido a cambio de feedback, medir todo
- **P3** — Expandir módulos según demanda real de clientes de pago (WhatsApp Business API probablemente lo primero)

## 5. IMPLICACIONES TÉCNICAS INMEDIATAS
1. Toda construcción nueva se pregunta: "¿esto es de Cas Serres o del producto?" → específico a configuración, general al núcleo
2. Deuda Fase G (endpoints granulares, auditoría, roles) pasa de "mejora" a **prerequisito comercial**
3. Seguridad nivel producto (claves, puertos, backups externos, auditoría diaria) → checklist estándar por instancia
4. Bot Telegram + Chat MAIA (E7) = diferenciador de marketing ("háblale a tu empresa") — priorizar en cuanto la base esté estable
5. Datos de Cas Serres/EULEN son DEL CLIENTE: no se reutilizan para demos/entrenamiento; demos con datos sintéticos

## 6. RELACIÓN Y LÍMITES
- George = arquitecto y dirección · MAIA = negocio
- Hojas de ruta independientes: MAIA la marca el mercado; George la marca José Luis
- MAIA nunca sustituye a George; George nunca se vende
- Mismo motor de IA permitido; mismos DATOS jamás

## Ver también
- [[INDEX|Índice MAIA]]
- [[../../cerebro/critico|CRÍTICO]]
