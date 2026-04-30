# sql-security-analysis
📌 Descripción del proyecto  

En este proyecto utilicé consultas SQL para analizar datos relacionados con intentos de inicio de sesión y empleados dentro de una organización. A través del uso de filtros, identifiqué actividad sospechosa y obtuve información clave para la seguridad del sistema.  

Este proyecto fue realizado como parte de mi formación en ciberseguridad (Google Cybersecurity Certificate).  

---

## 🔎 Intentos fallidos fuera de horario  

sql

SELECT *

FROM log_in_attempts

WHERE login_time > '18:00' AND success = FALSE;

Permite identificar intentos de acceso fallidos fuera del horario laboral.

📅 Intentos en fechas específicas

SELECT *

FROM log_in_attempts

WHERE login_date = '2022-05-09' OR login_date = '2022-05-08';

Permite analizar actividad en días específicos relacionados con incidentes.

🌎 Intentos fuera de México

SELECT *

FROM log_in_attempts

WHERE NOT country LIKE 'MEX%';

Filtra accesos que no provienen de México, útil para detectar actividad sospechosa.

🏢 Empleados de Marketing en East

SELECT *

FROM employees

WHERE department = 'Marketing' AND office LIKE 'East%';

Identifica empleados específicos para aplicar actualizaciones de seguridad.

👥 Empleados de Finanzas o Ventas

SELECT *

FROM employees

WHERE department = 'Finance' OR department = 'Sales';

Permite obtener empleados de múltiples departamentos.

🚫 Empleados que no son de IT

SELECT *

FROM employees

WHERE NOT department = 'Information Technology';

Filtra todos los empleados excepto los de IT.

🧠 Lo que aprendí

Uso de filtros en SQL (WHERE)

Operadores lógicos (AND, OR, NOT)

Uso de LIKE para patrones

Análisis de datos para detectar actividad sospechosa

🚀 Objetivo

Seguir desarrollando habilidades en SQL y análisis de datos aplicados a la ciberseguridad.
