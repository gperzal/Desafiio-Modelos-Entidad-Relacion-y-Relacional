# Diagrama Entidad-Relación

## Descripción General

Este documento describe el modelo de datos para el sistema de gestión de salud, centrándose en las entidades principales del sistema, como `Paciente`, `Médico`, `Consulta`, `Licencia` y `Especialidad`, así como sus relaciones. se implementa un Modelo Lógico y Modelo Físico

## Entidades y Relaciones 

### Paciente

- **Descripción**: Representa a los individuos que reciben atención médica.
- **Relaciones**:
  - **Consultas**: Un paciente puede tener múltiples consultas (1..N).
  - **Licencias**: Un paciente puede tener múltiples licencias médicas (0..N).

### Médico

- **Descripción**: Profesionales de la salud que brindan consultas y pueden emitir licencias médicas.
- **Relaciones**:
  - **Especialidades**: Un médico puede tener múltiples especialidades (0..N).
  - **Consultas**: Un médico puede realizar múltiples consultas (1..N).
  - **Licencias**: Un médico puede emitir múltiples licencias médicas (0..N).

### Consulta

- **Descripción**: Encuentros médicos entre un paciente y un médico.
- **Relaciones**:
  - **Licencia**: Una consulta puede resultar en la emisión de una licencia médica (0..1).

### Licencia

- **Descripción**: Documento oficial emitido por un médico que justifica la ausencia del paciente del trabajo o de otras actividades debido a razones médicas.
- **Relaciones**:
  - **Consulta**: Una licencia puede estar asociada a una consulta específica (opcional).

### Especialidad

- **Descripción**: Áreas de especialización médica de los médicos.
- **Relaciones**:
  - No tiene relaciones directas con otras entidades, pero se asocia con `Médico` a través de una tabla de relación.


## Notas Adicionales

- Este modelo es una simplificación y se basa en el requerimiento de un desafio latam.

