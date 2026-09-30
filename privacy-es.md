---
layout: default
title: Política de Privacidad
permalink: /privacy-es.html
---

*Esta es una traducción. En caso de discrepancia, prevalece la [versión en inglés](privacy-en.html).*

# Política de Privacidad de Margino

**Fecha de entrada en vigor:** 8 de mayo de 2026
**Última actualización:** 29 de septiembre de 2026

Esta Política de Privacidad explica cómo Margino ("la Aplicación", "el Servicio") recopila, utiliza, almacena y protege sus datos personales. Se proporciona en cumplimiento del Reglamento General de Protección de Datos de la Unión Europea (GDPR) y de la Ley de Protección de Datos Personales de Turquía (KVKK).

## 1. Responsable del Tratamiento

**Cemal Yılmaz**, empresario individual registrado en Turquía.

Contacto: [cemalyilmazsmmm@gmail.com](mailto:cemalyilmazsmmm@gmail.com)

No hemos designado un Delegado de Protección de Datos (DPO): el volumen y el perfil de riesgo del tratamiento de datos de Margino no alcanzan los umbrales del Artículo 37 del GDPR. El Responsable del Tratamiento indicado arriba es el punto de contacto para todas las solicitudes de los titulares de los datos.

## 2. Datos Personales que Recopilamos

Cuando usa la Aplicación, procesamos los siguientes datos:

| Categoría | Contenido | Origen |
|---|---|---|
| Identidad | ID de cuenta de Google (sub), nombre, foto de perfil | Google OAuth |
| Contacto | Correo electrónico asociado a su cuenta de Google | Google OAuth |
| Uso del Servicio | Imágenes de recibos/facturas que sube (transitorias), líneas de artículo extraídas (proveedor, artículos, precios, totales, impuestos), su lista de productos (nombres de productos, proveedores, tamaños de paquete, costo unitario más reciente y anterior), su margen de ganancia objetivo y sus preferencias de comisión de apps de reparto, el ID de su Google Sheet si conecta uno | Uso de la Aplicación |
| Técnico / Dispositivo | Dirección IP, marca de tiempo de la solicitud | Registros de acceso de Cloudflare |
| Notificaciones (opcional) | Token de notificaciones push e idioma de la app, solo si permite las notificaciones — se usa para el aviso semanal de costos de proveedores | Aplicación (iOS) |
| Facturación (futuro) | Estado de suscripción de RevenueCat | App Store / Play Store |

## 3. Finalidades y Bases Legales (Artículo 6 del GDPR)

| Finalidad | Base Legal |
|---|---|
| Lectura OCR de su recibo, mantenimiento de su lista de productos y precios sugeridos en la Aplicación y — solo si lo conecta — su escritura en su propio Google Sheet | Ejecución de un contrato (Art. 6(1)(b)) |
| Autenticación de cuenta y gestión de sesión | Ejecución de un contrato (Art. 6(1)(b)) |
| Prevención del uso indebido del servicio (límite de tasa, registros de errores) | Interés legítimo (Art. 6(1)(f)) |
| Comparación anónima de precios regionales | Interés legítimo (Art. 6(1)(f)) — sin identificador de usuario asociado |
| Analítica de producto (PostHog — métricas de uso) | Consentimiento (Art. 6(1)(a)) — recopilado mediante consentimiento dentro de la aplicación |
| Medir qué anuncios nuestros generan instalaciones, registros y suscripciones (Meta App Events) | Interés legítimo (Art. 6(1)(f)) |

## 4. Flujo de Datos y Destinatarios Externos

Compartimos sus datos con los siguientes proveedores de servicios únicamente para operar Margino. No vendemos ni compartimos datos con fines de marketing.

| Destinatario | Ubicación | Finalidad | Tipo de Dato |
|---|---|---|---|
| Anthropic, PBC | EE. UU. | Lectura de recibos mediante IA (API de Claude) | Imágenes de recibos (transitorias, eliminadas tras la lectura) |
| Google LLC | Global | Google OAuth, API de Sheets (escritura en su propio sheet), metadatos de Drive | Perfil de Google, token de actualización cifrado |
| Cloudflare, Inc. | EE. UU. (los puntos de presencia son globales) | Backend de la Aplicación (Workers), procesamiento de colas, registros de acceso | Todas las cargas de solicitud (transitorias en RAM, sin almacenamiento persistente) |
| Supabase, Inc. | EE. UU. (us-east-1) | Base de datos Postgres (registros de usuario, recibos procesados, su lista de productos, token de actualización cifrado), Vault (gestión de claves) | Identidad, contacto, contenido de recibos procesados, lista de productos, token de actualización cifrado |
| PostHog, Inc. | EE. UU. | Analítica de producto; visitas anónimas al sitio web y clics al App Store (sin cookies) | Eventos anónimos |
| RevenueCat, Inc. | EE. UU. | Gestión de suscripciones (tras la aprobación de Apple) | Estado de suscripción anónimo |
| Meta Platforms, Inc. | EE. UU. | Medición de los anuncios de Margino (SDK Meta App Events) | Eventos de la app (instalación, primer inicio de sesión, primer recibo, suscripción con precio y moneda), información del dispositivo y de la app (modelo, versión del sistema y de la app, idioma, zona horaria), dirección IP. Nunca su nombre, correo, recibos ni su lista de productos. |

**Transferencias internacionales:** Los datos se transfieren a EE. UU. y a otras regiones fuera del EEE / Turquía. Estas transferencias están protegidas por Cláusulas Contractuales Tipo (SCC) en virtud del Acuerdo de Tratamiento de Datos (DPA) de cada proveedor. Cuando nos basamos en el consentimiento para la transferencia (p. ej., Artículo 9 de la KVKK), este se recopila al comenzar a usar la Aplicación.

Margino no le rastrea en apps ni sitios web de otras empresas. No pedimos el permiso de Transparencia de Seguimiento de Apps ni recopilamos el identificador publicitario de su dispositivo (IDFA/AAID). En iOS, SKAdNetwork de Apple le indica a Meta que una instalación vino de un anuncio sin identificarle.

## 5. Períodos de Conservación

| Dato | Conservación |
|---|---|
| Imágenes de recibos | Hasta su lectura (segundos); nunca se almacenan de forma persistente |
| Contenido de recibos procesados y su lista de productos | Mientras su cuenta esté activa; se eliminan en cascada al eliminar la cuenta. Si conecta Google Sheets, también queda una copia en su propio Sheet, del cual usted es propietario |
| Token de actualización cifrado (Supabase) | Mientras la cuenta esté activa; se elimina de inmediato al eliminar la cuenta |
| Registro de usuario (tabla users de Supabase) | Mientras la cuenta esté activa; se elimina en cascada al eliminar la cuenta |
| Registro de recibos (marca de tiempo, éxito/fallo) | Mientras la cuenta esté activa; se elimina en cascada al eliminar la cuenta |
| Registros de acceso de Cloudflare | 30 días por defecto de Cloudflare |
| Comparaciones regionales anónimas | Indefinidamente (sin identificador de usuario; no se puede rastrear) |

## 6. Sus Derechos (Artículos 15 a 22 del GDPR)

Usted tiene los siguientes derechos respecto a sus datos personales:

- **Derecho de acceso** (Art. 15): solicitar una copia de los datos que tenemos sobre usted
- **Derecho de rectificación** (Art. 16): corregir datos inexactos
- **Derecho de supresión** (Art. 17): eliminar sus datos — disponible al instante desde **Ajustes → Eliminar cuenta** en la Aplicación
- **Derecho a la limitación del tratamiento** (Art. 18): limitar cómo procesamos sus datos
- **Derecho a la portabilidad de los datos** (Art. 20): exportar sus productos y precios a su propio Google Sheet desde **Ajustes → Exportar a Google Sheets**, o escribirnos por correo para obtener una copia
- **Derecho de oposición** (Art. 21): oponerse al tratamiento basado en interés legítimo
- **Derecho a retirar el consentimiento** (Art. 7(3)): para cualquier tratamiento basado en consentimiento
- **Derecho a presentar una reclamación**: ante la Autoridad KVKK de Turquía (kvkk.gov.tr) o ante su Autoridad de Protección de Datos local en la UE

Para ejercer cualquiera de estos derechos, escriba a [cemalyilmazsmmm@gmail.com](mailto:cemalyilmazsmmm@gmail.com). Respondemos en un plazo de 30 días (Artículo 12(3) del GDPR).

## 7. Datos de Menores

Margino no está destinado a usuarios menores de 13 años. Si descubrimos que se han recopilado datos de un usuario menor de 13 años, eliminaremos la cuenta de inmediato.

## 8. Seguridad

- Todo el tráfico cliente-servidor está cifrado con TLS 1.3
- Los tokens de actualización se almacenan en Supabase Vault, cifrados con claves gestionadas por KMS
- Los JWT de sesión se firman con HMAC-SHA256: token de acceso de 1 hora + token de actualización que vence tras 180 días sin uso; cada actualización lo rota y un token reutilizado cierra la sesión
- Todos los proveedores externos cuentan con certificación SOC 2 Type II o ISO 27001

## 9. Cambios en esta Política

Cuando actualicemos esta política, la fecha de "Última actualización" cambiará y se lo notificaremos dentro de la aplicación. Los cambios sustanciales requieren obtener de nuevo el consentimiento de los usuarios existentes.

## 10. Contacto

Puede contactar al Responsable del Tratamiento (Cemal Yılmaz) en:

📧 [cemalyilmazsmmm@gmail.com](mailto:cemalyilmazsmmm@gmail.com)
