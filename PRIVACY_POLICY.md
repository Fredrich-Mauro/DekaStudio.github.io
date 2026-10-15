# Política de Privacidad de Dekachat

**Última actualización:** Octubre de 2026  
**Desarrollador:** DekaStudio  
**Aplicación:** Dekachat (`com.dekastudio.dekachat.jicwsi`)  
**Contacto:** fredrichmauro@gmail.com

---

## 1. Introducción y Compromiso de Privacidad

En **DekaStudio**, creemos firmemente que la privacidad es un derecho fundamental. **Dekachat** es una aplicación de mensajería privada descentralizada y cifrada diseñada desde sus cimientos bajo el principio de **Zero-Knowledge** (conocimiento cero) y **comunicación entre pares (Peer-to-Peer - P2P)**.

Nuestra arquitectura garantiza que ninguna información personal, mensaje de texto, nota de voz, archivo o metadato sea recopilado, procesado o almacenado en servidores externos o de terceros.

---

## 2. Principio de No Recopilación de Datos ("Zero-Data Collection")

Dekachat opera sin bases de datos remotas, cuentas en la nube ni servidores centrales:

- **Sin registro ni cuentas personales:** No requerimos números de teléfono, correos electrónicos, nombres reales, perfiles ni contraseñas.
- **Sin recopilación de datos:** DekaStudio **NO recopila, rastrea, monitorea ni almacena** su actividad, historial de chats, lista de contactos ni hábitos de uso.
- **Sin publicidad ni rastreadores:** Dekachat no contiene SDKs de analíticas (como Google Analytics o Firebase Analytics), redes publicitarias ni librerías de seguimiento conductual.
- **Sin telemetría oculta:** La aplicación no realiza conexiones ocultas de diagnóstico o reporte de fallos en segundo plano.

---

## 3. Cifrado de Extremo a Extremo (AES-256-GCM)

Toda comunicación a través de Dekachat está protegida con estándares criptográficos de grado militar:

- **Algoritmo de cifrado:** Cada mensaje y archivo multimedia se encripta mediante **AES-256-GCM** (Galois/Counter Mode).
- **Integridad y autenticidad:** Cada carga útil incluye un vector de inicialización único (IV) y una etiqueta de autenticación (Auth Tag) que previene ataques de manipulación o intermediarios (*Man-in-the-Middle*).
- **Control de claves:** Las claves criptográficas se generan y derivan localmente en los dispositivos de los usuarios. DekaStudio no tiene acceso a sus claves ni la capacidad técnica de descifrar sus comunicaciones.

---

## 4. Uso Estricto de Permisos del Dispositivo

Dekachat solicita únicamente los permisos indispensables del sistema operativo Android para habilitar funciones operativas solicitadas activamente por el usuario:

### A. Cámara (`android.permission.CAMERA`)
- **Propósito:** Utilizada de forma puntual y exclusiva para escanear el código QR que contiene la clave pública o huella de seguridad de otro usuario al añadir un contacto.
- **Garantía:** No se capturan fotos, no se graban vídeos y la imagen de la cámara se procesa localmente en la memoria volátil del dispositivo en tiempo real sin guardarse en disco.

### B. Micrófono (`android.permission.RECORD_AUDIO`)
- **Propósito:** Permitir al usuario grabar notas de voz únicamente cuando pulsa y mantiene presionado de manera activa el botón de grabación en una conversación.
- **Garantía:** El micrófono nunca se activa en segundo plano. El archivo de audio resultante se encripta inmediatamente con AES-256-GCM antes de ser transmitido de par a par y almacenado localmente.

### C. Red y Conectividad (`android.permission.INTERNET`, `ACCESS_NETWORK_STATE`, `ACCESS_WIFI_STATE`)
- **Propósito:** Establecer sockets directos de red local (Wi-Fi o LAN) para transferir los paquetes criptográficos directamente entre los dos dispositivos involucrados en el chat.
- **Garantía:** No se transmite tráfico hacia servidores centralizados de DekaStudio ni de proveedores externos.

---

## 5. Almacenamiento Local y Soberanía del Usuario

- **Ubicación de los datos:** Todos los mensajes recibidos y enviados, así como la configuración de la app, se almacenan exclusivamente en la base de datos local y aislada de su propio dispositivo (*Android Sandboxed Storage*).
- **Eliminación y borrado completo:** El usuario tiene soberanía absoluta sobre sus datos. Al seleccionar la opción de vaciar chat, borrar datos de la aplicación desde los ajustes de Android, o desinstalar la app, toda la información y claves asociadas se destruyen de forma inmediata e irrecuperable.

---

## 6. Transferencia y Divulgación a Terceros

DekaStudio **no comparte, no vende, no alquila ni divulga** ningún tipo de dato con terceros, empresas comerciales, entidades gubernamentales ni proveedores de servicios, por la sencilla razón técnica de que **no poseemos ni almacenamos dato alguno**.

---

## 7. Privacidad de Menores

Dekachat no recopila intencionalmente datos de ninguna persona, incluidos niños y menores de edad. Cumple plenamente con las directrices de la Ley de Protección de la Privacidad Infantil en Línea (COPPA) y el Reglamento General de Protección de Datos (GDPR).

---

## 8. Cumplimiento de la Declaración de Seguridad de Datos (Google Play Data Safety)

En el marco de las Políticas para Desarrolladores de Google Play Console, declaramos que para Dekachat:
- **Datos recopilados:** **0** (Ningún dato se recopila).
- **Datos compartidos:** **0** (Ningún dato se comparte con terceros).
- **Cifrado en tránsito:** Los datos compartidos entre dispositivos pares están cifrados de extremo a extremo (E2EE) con AES-256-GCM.
- **Mecanismo de eliminación:** Los datos pueden eliminarse en cualquier momento desinstalando la aplicación o borrando su almacenamiento local.

---

## 9. Modificaciones a esta Política

Podemos actualizar nuestra Política de Privacidad periódicamente si se incorporan nuevas funcionalidades que así lo requieran. Cualquier actualización se publicará con su respectiva fecha de vigencia en este mismo documento.

---

## 10. Información de Contacto

Para cualquier consulta o inquietud técnica respecto a esta Política de Privacidad o la seguridad de Dekachat:

- **Desarrollador Responsable:** DekaStudio  
- **Aplicación:** Dekachat para Android (`com.dekastudio.dekachat.jicwsi`)  
- **Correo Electrónico:** fredrichmauro@gmail.com  
