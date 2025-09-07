# Laboratorio 3 – Respuesta ante Incidentes de Seguridad

## Paso 1: Identificar el Vector de Ataque Inicial

### 1.1 Revisión de Indicadores Iniciales

**Actividad:**  
Reunir la primera información que indique que existe un posible incidente:

- Mensajes de correo extraños o sospechosos.  
- Fallos en sistemas específicos o aplicaciones críticas.  
- Alertas inusuales en antivirus, IDS/IPS o firewall.  
- Accesos de usuarios desconocidos o desde ubicaciones no habituales.  

**Posibles vectores de ataque:**
- **Phishing** (correos falsos que contienen enlaces o archivos maliciosos).  
- **Explotación de vulnerabilidad** (aprovechamiento de fallas en el software).  
- **Acceso no autorizado** (uso indebido de credenciales legítimas o suplantación de identidad).  

---

### 1.2 Evaluación de la Evidencia

**Actividad:**  
Determinar cuál es el vector de ataque más probable, según las pruebas recolectadas.  

- **Si el phishing es identificado:**  
  - Revisar encabezados de correos electrónicos.  
  - Analizar enlaces sospechosos y adjuntos maliciosos.  
  - Verificar conexiones hacia dominios desconocidos.  

- **Si una vulnerabilidad es sospechosa:**  
  - Identificar software o servicios sin parches.  
  - Revisar logs de explotación o intentos de intrusión.  
  - Correlacionar con exploits conocidos.  

- **Si se detecta acceso no autorizado:**  
  - Analizar logs de inicio de sesión (fallidos y exitosos).  
  - Identificar accesos desde direcciones IP extrañas.  
  - Revisar el uso de credenciales privilegiadas fuera de horario.  

**Resultado esperado:**  
Parámetros claros que confirmen el vector de ataque inicial (ejemplo: phishing con archivo adjunto malicioso que ejecutó malware).  

---

## Paso 2: Analizar los Logs del Sistema para Encontrar Evidencias de Actividad Maliciosa

### 2.1 Recolección de Logs

**Actividad:** Identificar los principales logs que se deben revisar.  

- **Logs del servidor de correo electrónico:**  
  - Correos con remitentes sospechosos.  
  - Archivos adjuntos no solicitados.  
  - Usuarios que hicieron clic en enlaces.  

- **Logs del sistema de bases de datos:**  
  - Consultas inusuales o no autorizadas.  
  - Intentos de acceso desde cuentas desconocidas.  
  - Cambios no registrados en tablas críticas.  

- **Logs de seguridad (SO, firewall, IDS/IPS):**  
  - Intentos de intrusión o fuerza bruta.  
  - Accesos desde IPs no habituales.  
  - Alertas de antivirus o sistemas de monitoreo.  

---

### 2.2 Análisis de la Actividad Maliciosa

**Actividad:**  
Analizar los logs para buscar patrones anómalos o repetitivos.  

Ejemplos de patrones:  
- Accesos múltiples desde una misma IP en poco tiempo.  
- Intentos repetidos de autenticación fallida.  
- Ejecución de procesos o comandos no habituales.  

**Herramientas recomendadas:**  
- **SIEM (Security Information and Event Management):** Splunk, ELK Stack, Wazuh.  
- **Comandos básicos:** grep, awk, less, journalctl.  
- **Análisis de tráfico:** Wireshark, tcpdump.  

---

## Paso 3: Determinar el Alcance del Compromiso y los Sistemas Afectados

### 3.1 Identificación de Sistemas Comprometidos

**Actividad:**  
- Revisar qué sistemas presentan actividad anómala.  
- Evaluar si otros equipos interconectados también fueron afectados.  
- Validar conexiones entre servidores críticos y segmentados.  

---

### 3.2 Evaluación del Impacto

**Actividad:**  
Analizar cómo afecta el ataque a los pilares de la seguridad:  

- **Disponibilidad:** ¿El sistema sigue funcionando o fue interrumpido?  
- **Integridad:** ¿Se alteraron los datos sin autorización?  
- **Confidencialidad:** ¿Hubo fuga de información sensible?  

**Resultado esperado:**  
Mapa del compromiso indicando qué sistemas fueron afectados y qué nivel de impacto tuvieron.  

---

## Paso 4: Proponer Medidas de Contención Inmediatas

### 4.1 Medidas de Contención Inmediatas

**Actividad:**  
Aplicar acciones rápidas para evitar la propagación del ataque.  

- **Desconectar sistemas comprometidos** de la red.  
- **Actualizar sistemas y aplicar parches** de seguridad.  
- **Cambiar credenciales comprometidas** y reforzar autenticación (ej. MFA).  

---

### 4.2 Plan de Recuperación

**Actividad:**  
Restaurar los sistemas afectados y volver a la operación normal.  

- **Restauración desde copias de seguridad confiables.**  
- **Monitoreo y validación** posterior para asegurar que la amenaza fue eliminada.  
- **Evaluación post-incidente** para identificar mejoras en los procesos de seguridad.  

---

### 4.3 Comunicación

**Actividad:**  
Definir cómo y a quién comunicar el incidente.  

- **A la dirección y responsables de TI:** para coordinar medidas.  
- **A los usuarios afectados:** transparencia sobre qué ocurrió y cómo se solucionó.  
- **A las autoridades (si aplica):** en caso de fuga de datos sensibles o normativas legales.  

**Transparencia:**  
Informar de manera clara, sin ocultar datos relevantes, manteniendo la confianza.  

---
