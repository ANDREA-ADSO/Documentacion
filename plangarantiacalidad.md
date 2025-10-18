Plan de Garantía de Calidad 

MEGALAVADO SAS

Versión: 1.0

Fecha: 18 de Octubre 2025

Responsable QA: Andrea Osorio
Stakeholders: Andrea osorio
Gerente de Operaciones
Equipo de Lavado
Yeison  Gonzalez, Andrea Osorio
Desarrolladores
Clientes finales
Yeison  Gonzalez

2. Objetivos de Calidad
 1: Garantizar disponibilidad del sistema 99.5% para permitir reservas 24/7
 2: Lograr tasa de conversión > 75% en completitud de reservas online
 3: Mantener tiempo de respuesta < 3 segundos en páginas críticas
 4: Reducir tasa de errores en reservas a < 0.5%
 5: Asegurar compatibilidad móvil para > 95% de dispositivos

3. Estándares y Referencias
 ISO 25010 para calidad de producto software
 WCAG 2.1 Nivel AA para accesibilidad web
 OWASP Top 10 para seguridad web
 Google Core Web Vitals para performance
 CMMI Nivel 2 para procesos repetibles

4. Métricas de Calidad
Métrica	Objetivo	Frecuencia	Responsable	Herramienta
Tasa de defectos en producción	< 0.5%	Semanal	QA Lead	Jira/Bugzilla
Code coverage	> 80%	Por release	Dev Lead	Jest/Jacoco
Tiempo de respuesta promedio	< 2 seg	Continuo	DevOps	New Relic
Tasa de conversión reservas	> 75%	Diaria	Product Owner	Google Analytics
Disponibilidad sistema	> 99.5%	Mensual	DevOps	Pingdom
Satisfacción cliente (CSAT)	> 4.5/5	Mensual	QA Manager	Encuestas
Tasa de abandono carrito	< 25%	Semanal	Product Owner	Hotjar
Vulnerabilidades seguridad	0 críticas	Mensual	Security Lead	OWASP ZAP

5. Procesos de Verificación
5.1. Revisiones de Código
Frecuencia: Semanal / Por cada pull request
Herramienta: GitHub/GitLab
Checklist: [Incluir checklist de revisión técnica]
Participantes: 2 desarrolladores + Tech Lead
Criterios de Aprobación:
0 comentarios críticos
Tests unitarios pasando
Coverage mantenido o mejorado

5.2. Testing
Unit Testing
Coverage esperado: > 80% código crítico
Frameworks: Jest (Frontend), JUnit (Backend)
Responsable: Desarrolladores
Criterio: Todas las funciones de negocio deben tener tests
Integration Testing
Enfoque: Pruebas de APIs y base de datos
Coverage: 100% de integraciones críticas
Herramientas: Supertest, Postman

Escenarios:
Integración pasarela de pagos
Notificaciones SMS/Email
Calendar sync
System Testing

Criterios:

Flujo completo de reserva funcional
Performance bajo carga (100 usuarios simultáneos)
Seguridad de datos validada
Entorno: Staging idéntico a producción
Acceptance Testing 

Proceso:
Pruebas con usuarios reales (beta testers)
Validación con equipo de lavado
Aprobación final del Product Owner
Criterio: 100% de casos de uso críticos aprobados

6. Roles y Responsabilidades
Rol	Responsabilidades	Persona Asignada
QA Manager	Definir estrategia QA, reportar métricas, gestionar riesgos	[Andrea Osoario, Yeison Gonzalez]
QA Engineer	Ejecutar pruebas, reportar bugs, crear casos de prueba	[Andrea Osoario, Yeison Gonzalez]
Dev Lead	Garantizar calidad código, revisiones, métricas técnicas	[Andrea Osoario, Yeison Gonzalez]
Product Owner	Validar funcionalidad, criterios aceptación, UX	[Andrea Osoario, Yeison Gonzalez]
DevOps	Monitoreo, performance, disponibilidad, despliegues	[Andrea Osoario, Yeison Gonzalez]

7. Cronograma de Actividades

Actividad	Fecha Inicio	Fecha Fin	Estado	Responsable
Definición métricas calidad	[Fecha]	[Fecha]	Completo	QA Manager
Implementación testing automatizado	[Fecha]	[Fecha]	En progreso	Dev Lead
Revisiones código semanales	[Fecha]	[Fecha]	Pendiente	Tech Lead
Pruebas integración pasarela pago	[Fecha]	[Fecha]	Pendiente	QA Engineer
Pruebas performance y carga	[Fecha]	[Fecha]	Pendiente	DevOps
Pruebas aceptación con usuarios	[Fecha]	[Fecha]	Pendiente	Product Owner
Auditoría seguridad OWASP	[Fecha]	[Fecha]	Pendiente	Security Lead


8. Gestión de Riesgos
Riesgo	Probabilidad	Impacto	Mitigación	Responsable
Caída pasarela de pagos	Media	Alto	Integración múltiples proveedores, modo offline	DevOps
Picos de tráfico inesperados	Media	Alto	Auto-scaling, CDN, cache agresivo	DevOps
Errores en asignación de citas	Baja	Alto	Validación doble, notificaciones confirmación	Dev Lead
Vulnerabilidades seguridad	Media	Alto	Scans automáticos, pentesting regular	Security Lead
Incompatibilidad dispositivos	Alta	Medio	Testing multi-dispositivo, progressive enhancement	QA Engineer
Pérdida datos reservas	Baja	Crítico	Backup automático, replicación en tiempo real	DevOps
Plan de Contingencia
Monitoreo 24/7 con alertas automáticas

Modo offline para tomar reservas telefónicas

Backup manual de sistema de citas

Comunicación proactiva con clientes afectados

Rollback automático en despliegues problemáticos

Indicadores de Alerta Temprana
Tiempo de respuesta > 3 segundos
Tasa de error > 1%
Disponibilidad < 99%
Coverage tests < 75%