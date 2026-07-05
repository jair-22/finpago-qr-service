# Política de Seguridad

## Descripción General

Finpago QR Service es un microservicio financiero encargado de la generación, validación y procesamiento de transacciones de pago mediante códigos QR.

Dado que este servicio puede procesar información transaccional sensible, la seguridad es un principio fundamental en su diseño, desarrollo y operación.

Este documento define:

- Versiones soportadas
- Procedimiento para reportar vulnerabilidades
- Política de divulgación responsable
- Tiempos de respuesta
- Alcance de seguridad

---

## Versiones Soportadas

Solo las siguientes versiones reciben actualizaciones de seguridad:

| Versión | Soporte | Observaciones |
|----------|----------|----------------|
| 2.1.x | ✅ Sí | Versión estable actual en producción |
| 2.0.x | ✅ Sí | Soporte de mantenimiento |
| 1.x | ❌ No | Versión obsoleta – requiere actualización |

Si está utilizando una versión sin soporte, deberá actualizar antes de solicitar correcciones de seguridad.

---

## Alcance

Esta política aplica a:

- Endpoints de generación de códigos QR
- APIs de validación de transacciones
- Flujos de autenticación y autorización
- Procesamiento de tokens de pago
- Validación de entradas y parámetros
- Workflows CI/CD definidos en este repositorio
- Archivos de Infraestructura como Código (IaC)

No aplica a:

- Infraestructura de terceros
- Sistemas bancarios externos
- Sistemas de comerciantes integrados

---

## Cómo Reportar una Vulnerabilidad

Si identifica una vulnerabilidad de seguridad, **NO abra un Issue público**.

Reporte el hallazgo de manera privada a:

📧 Correo: seguridad@finpago.com 
🔐 Comunicación cifrada disponible bajo solicitud 
📦 También puede utilizar "Private Vulnerability Reporting" de GitHub si está habilitado

Incluya:

- Descripción detallada
- Endpoint o componente afectado
- Pasos para reproducir
- Evidencia técnica (si aplica)
- Evaluación de impacto estimada

---

## Tiempos de Respuesta

Seguimos prácticas de divulgación responsable.

| Severidad | Respuesta Inicial | Objetivo de Corrección |
|------------|------------------|------------------------|
| Crítica | 24–48 horas | ≤ 7 días |
| Alta | 48 horas | ≤ 14 días |
| Media | 5 días hábiles | ≤ 30 días |
| Baja | Mejor esfuerzo | Según planificación |

Los tiempos pueden variar dependiendo de la complejidad técnica.

---

## Política de Divulgación Responsable

Solicitamos a los investigadores:

- No divulgar públicamente antes de la remediación
- No explotar más allá de una prueba de concepto
- No acceder a datos reales de usuarios
- No realizar pruebas de denegación de servicio sin coordinación

Nos comprometemos a:

- Comunicación transparente
- Reconocimiento del investigador (si lo desea)
- Publicar avisos de seguridad cuando corresponda
- Emitir CVE si aplica

---

## Prácticas de Seguridad Implementadas

Este repositorio aplica:

- Revisión obligatoria de Pull Requests
- Protección de rama principal
- Escaneo de dependencias
- Análisis estático de código
- Detección de secretos expuestos
- Workflows CI/CD con validaciones de seguridad
- Commits firmados (cuando aplica)

---

## Arquitectura de Seguridad

Controles implementados:

- Autenticación basada en tokens (JWT)
- Validación estricta de entradas
- Control de tasa (rate limiting)
- Registro y trazabilidad de eventos
- Validaciones automáticas en CI/CD

Las implementaciones productivas pueden integrarse con:

- SSO corporativo
- Aprovisionamiento SCIM
- Monitoreo centralizado
- Sistemas SIEM

---

## Agradecimientos

Valoramos la investigación responsable en seguridad.

Las vulnerabilidades reportadas adecuadamente podrán ser reconocidas públicamente en notas de versión o avisos de seguridad.

---

Gracias por contribuir a mantener Finpago seguro.
