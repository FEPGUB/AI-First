# PRD-001: Orgenicemos — Aplicacion para la gestion de eventos

## Contexto y Problema

Se requiere desarrollar una aplicación web/móvil para la gestión de eventos que automatice las invitaciones, la confirmación de asistencia y seguimiento del mismo.
La solución busca optimizar la comunicación entre organizadores e invitados mediante recordatorios automáticos y herramientas de retroalimentación posterior (encuestas y observaciones).

## Objetivos

Poder generar eventos para distintas fechas, invitar gente.
Ademas, para cada evento poder agregar encuestas con información de la misma

## Requerimientos Funcionales

- RF-01: Crear eventos: Permite definir detalles clave de estos (fecha, hora, ubicación física, descripción, invitados).
- RF-02: Se poder listar todos los eventos propios y a los que soy invitado.
- RF-03: Se deben generar las invitaciones individuales por correo electrónico o notificaciones dentro de la app.
- RF-04: El invitado debe poder confirmar asistencia.
- RF-05: El organizador debe poder visualizar las respuestas de los invitados.
- RF-06: El organizador debe poder crear encuestas y observaciones.
- RF-07: El sistema debe enviar invitaciones automaticas recordando a los invitados que no emitieron una respuesta.
- RF-08: El sistema enviar un recordatorio el dia del evento.

## Requerimientos No Funcionales

- RNF-01: Los eventos deben ingresarse con al menos 4 dias de anticipación.
- RNF-02: La respuesta del invitado no puede ser posterior al dia anterior al evento.
- RNF-03: Las encuestas puede no ser respondidas.

## Criterios de Aceptación

- AC-01 (RF-01, RF-02, RF-04): Dado un invitado recibe la invitación debe poder responder Asistiré/No asistire.
- AC-02 (RF-07): Dado que falta 1 día para el evento y existen invitados en estado Pendiente, entonces se enviará una notificación (email) automática únicamente a la lista de personas que aún no han respondido.
- AC-03 (RF-07): Dado que falta 1 día para el evento, entonces se enviará una notificación (email) automática a la lista de personas respondieron que asistirán.

## Fuera de Alcance

No se implementará el modulo de envio de notificaciones Push

## Riesgos y Dependencias

- Riesgo: Baja entregabilidad de emails (los correos pueden ir a la carpeta de Spam).
- Dependencia: SQLite.
