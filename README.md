# DekaStudio.github.io

<p align="center">
  <img src="app/src/main/res/drawable/app_logo.png" alt="Dekachat Logo" width="128" height="128" />
</p>

<p align="center">
  <strong>Mensajería descentralizada entre pares (P2P), cifrada de extremo a extremo y con cero conocimiento.</strong><br>
  <em>Decentralized peer-to-peer (P2P), end-to-end encrypted and zero-knowledge private messaging for Android.</em>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Android_8.0+-3DDC84?style=for-the-badge&logo=android&logoColor=white" alt="Android Platform" />
  <img src="https://img.shields.io/badge/UI-Jetpack_Compose_M3-4285F4?style=for-the-badge&logo=jetpackcompose&logoColor=white" alt="Jetpack Compose" />
  <img src="https://img.shields.io/badge/Language-Kotlin-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white" alt="Kotlin" />
  <img src="https://img.shields.io/badge/Encryption-AES--256--GCM-00C853?style=for-the-badge" alt="AES-256-GCM" />
  <img src="https://img.shields.io/badge/Network-Direct_P2P_Sockets-FF6D00?style=for-the-badge" alt="Direct P2P Sockets" />
  <img src="https://img.shields.io/badge/Privacy-Zero--Knowledge-6200EE?style=for-the-badge" alt="Zero-Knowledge" />
</p>

---

## 🌐 Selecciona tu idioma / Select your language

- 🇪🇸 **[Español](#-español)**
  - [Visión General](#visión-general)
  - [Características Principales](#características-principales)
  - [Guía Rápida de Uso](#guía-rápida-de-uso-paso-a-paso)
  - [Arquitectura Criptográfica y de Red](#arquitectura-criptográfica-y-de-red)
  - [Permisos y Privacidad](#permisos-y-garantías-de-privacidad)
  - [Compilación y Desarrollo](#compilación-y-desarrollo)
- 🇬🇧 **[English](#-english)**
  - [Overview](#overview)
  - [Key Features](#key-features)
  - [Step-by-Step User Guide](#step-by-step-user-guide)
  - [Cryptographic & Network Architecture](#cryptographic--network-architecture)
  - [Permissions & Privacy Guarantees](#permissions--privacy-guarantees)
  - [Build and Development](#build-and-development)

---

# 🇪🇸 Español

## Visión General

**Dekachat** es una aplicación de mensajería para Android diseñada desde cero para proteger la privacidad absoluta y la soberanía de los datos del usuario. A diferencia de las plataformas de mensajería convencionales, **Dekachat no utiliza servidores centrales, servicios en la nube ni bases de datos remotas**.

Toda la comunicación ocurre directamente entre dispositivos (**Peer-to-Peer**) dentro de tu red local (Wi-Fi, punto de acceso o LAN). Cada mensaje de texto, nota de voz y archivo transferido se encripta de extremo a extremo mediante **AES-256-GCM**, asegurando que únicamente los participantes legítimos puedan descifrar el contenido.

### Principios Fundamentales
1. **Zero-Knowledge (Conocimiento Cero):** Nadie (ni los creadores ni intermediarios de red) tiene acceso a tus conversaciones o claves.
2. **Sin Registro:** No requiere número de teléfono, correo electrónico, contraseñas ni cuenta en la nube.
3. **Cero Rastreadores:** Sin analíticas, sin publicidad y sin telemetría en segundo plano.
4. **Soberanía Total:** Tus datos residen exclusivamente en el almacenamiento seguro de tu dispositivo móvil (*Sandboxed Storage*).

---

## Características Principales

* 🔒 **Cifrado Autenticado AES-256-GCM:** Cada carga útil incluye un Vector de Inicialización (IV) de 12 bytes y una etiqueta de autenticación (Auth Tag) de 128 bits para evitar ataques de manipulación o intermediarios (*Man-in-the-Middle*).
* ⚡ **Comunicación Directa P2P:** Transmisión ultrarrápida mediante sockets TCP nativos (puerto estándar `8988`), ideal para oficinas, hogares o situaciones sin conexión a Internet global.
* 📷 **Emparejamiento y Verificación por Código QR:** Comparte tu perfil y clave criptográfica en segundos utilizando el generador y escáner de códigos QR con cámara en vivo.
* 🛡️ **Verificación de Huella Criptográfica:** Compara huellas de seguridad en pantalla o escanéalas para confirmar que tu contacto no ha sido suplantado.
* 🎙️ **Notas de Voz Protegidas:** Grabación y reproducción de notas de audio con visualizador de ondas y cifrado instantáneo antes de la transmisión.
* 📁 **Compartición Segura de Archivos y Fotos:** Envío de imágenes y documentos con registro e historial de archivos compartidos.
* 🩺 **Auditoría de Seguridad en Tiempo Real:** Herramienta integrada que ejecuta pruebas criptográficas dinámicas directamente en el dispositivo y emite un informe de integridad.
* 🎨 **Diseño Moderno con Material 3:** Interfaz moderna, minimalista y reactiva creada con Jetpack Compose y soporte para tema oscuro.

---

## Guía Rápida de Uso (Paso a Paso)

### Paso 1: Configura tu Identidad
1. Abre la aplicación por primera vez.
2. Ingresa un **alias o apodo** para tu perfil (no requiere datos reales).
3. Dekachat generará automáticamente tu par de claves criptográficas y tu código de identificación seguro.

### Paso 2: Conectar con otro Dispositivo
Asegúrate de que ambos teléfonos estén conectados a la **misma red Wi-Fi o punto de acceso portátil**:
* **Método 1 (Automático con QR):** Ve a la pestaña **Contactos**, pulsa el botón **"+"** o **Escanear QR**, y apunta tu cámara al código QR que tu amigo muestra en su pantalla de perfil.
* **Método 2 (Manual):** Introduce la dirección IP local de tu amigo (mostrada en la cabecera de su app, ej. `192.168.1.45`) y su clave pública de identidad.

### Paso 3: Verificar la Huella de Seguridad
1. Abre la conversación con tu contacto.
2. Toca el icono de **Escudo / Huella de Seguridad** en la barra superior.
3. Puedes comparar visualmente el código alfanumérico o usar **Escanear Huella** para validar la firma criptográfica. Si coinciden, el contacto se marcará como **Verificado**.

### Paso 4: Chatear, Enviar Audios y Archivos
* **Texto:** Escribe en la barra inferior y presiona enviar.
* **Notas de Voz:** Mantén presionado el icono de **micrófono** para grabar. Suelta para enviar con cifrado automático.
* **Archivos y Fotos:** Presiona el botón de **adjuntar (+) o galería** para seleccionar y transferir archivos de forma directa.
* **Auditoría:** En el menú superior, pulsa **Auditoría de Seguridad** para ejecutar un chequeo del cifrado en cualquier momento.

---

## Arquitectura Criptográfica y de Red

```
┌─────────────────────────────────┐           Socket TCP Directo (Puerto 8988)         ┌─────────────────────────────────┐
│       Dispositivo A (Peer 1)    │◄──────────────────────────────────────────────────►│       Dispositivo B (Peer 2)    │
│  - Clave Identidad A            │            Carga Útil Cifrada AES-256-GCM          │  - Clave Identidad B            │
│  - IP Local: 192.168.1.X        │     [IV (12B) | Mensaje Cifrado | Tag (16B)]       │  - IP Local: 192.168.1.Y        │
│  - Base de Datos Room (Local)   │                                                    │  - Base de Datos Room (Local)   │
└────────────────┬────────────────┘                                                    └────────────────┬────────────────┘
                 │                                                                                      │
                 │                     Verificación Cruzada de Huellas QR                               │
                 └───────────────────────────────► 📷 ◄─────────────────────────────────────────────────┘
                                        (Zero-Trust Key Exchange)
```

### Derivación de Clave Compartida
Ambos dispositivos derivan una clave compartida conmutativa idéntica utilizando una función de derivación de claves basada en **SHA-256 (KDF)** sobre las claves públicas ordenadas:
$$\text{SharedKey} = \text{SHA-256}(\text{"DEKACHAT\_E2EE\_AES256\_GCM\_V1"} \parallel \text{Key}_A \parallel \text{Key}_B)$$
Esto garantiza que sin importar quién inició la conexión, ambos extremos cifran y descifran los mensajes con exactitud e integridad garantizada por el tag GCM de 128 bits.

---

## Permisos y Garantías de Privacidad

Dekachat solicita únicamente los permisos indispensables para las acciones solicitadas por el usuario:

| Permiso | Finalidad | Garantía de Privacidad |
| :--- | :--- | :--- |
| `CAMERA` | Escanear códigos QR de contactos y huellas criptográficas. | Solo se activa al abrir el escáner. Las imágenes no se guardan ni transmiten. |
| `RECORD_AUDIO` | Grabar notas de voz interactivas. | Solo se activa al mantener pulsado el botón de audio. El audio se encripta inmediatamente. |
| `INTERNET` / `ACCESS_NETWORK_STATE` | Establecer sockets TCP en la red local. | No realiza peticiones a servidores externos ni a servicios en la nube. |

---

## Compilación y Desarrollo

### Requisitos
* Android Studio Iguana / Jellyfish o superior.
* JDK 17 o JDK 21.
* Android SDK (API 26 mínima, API 35 objetivo).

### Comandos de Compilación
```bash
# Compilar el APK en modo depuración
gradle assembleDebug

# Ejecutar las pruebas unitarias y de Robolectric
gradle :app:testDebugUnitTest
```

---
---

# 🇬🇧 English

## Overview

**Dekachat** is an Android messaging application built from the ground up to protect absolute privacy and user data sovereignty. Unlike conventional messaging platforms, **Dekachat does not use central servers, cloud infrastructure, or remote databases**.

All communications occur directly between devices (**Peer-to-Peer**) across your local network (Wi-Fi, mobile hotspot, or LAN). Every text message, voice note, and shared file is end-to-end encrypted using **AES-256-GCM**, ensuring only authorized chat participants can read your data.

### Core Principles
1. **Zero-Knowledge Architecture:** No central server or third party ever sees your plaintext messages, contacts, or keys.
2. **No Registration or Accounts:** No phone number, email address, password, or cloud identity required.
3. **Zero Trackers:** No analytics SDKs, no ad networks, and no hidden telemetry.
4. **Complete Data Sovereignty:** All conversation history and cryptographic credentials remain strictly in your device's sandboxed storage.

---

## Key Features

* 🔒 **Authenticated AES-256-GCM Encryption:** Every payload carries a unique 12-byte Initialization Vector (IV) and a 128-bit authentication tag to prevent tampering and Man-in-the-Middle attacks.
* ⚡ **Direct Peer-to-Peer (P2P) Sockets:** Blazing fast message exchange over TCP sockets (default port `8988`), resilient even in offline or local-only networks.
* 📷 **QR Code Pairing & Key Exchange:** Share identity credentials and connect peers instantly with the built-in live camera QR scanner and QR code generator.
* 🛡️ **Cryptographic Fingerprint Verification:** Compare security fingerprints on screen or scan to verify cryptographic peer identity.
* 🎙️ **Protected Voice Audio Notes:** Interactive voice recording and playback with audio waveforms, encrypted directly on device before network transport.
* 📁 **Secure Media & File Transfer:** Exchange photos and documents directly with a dedicated shared files history screen.
* 🩺 **Real-Time Cryptographic Security Audit:** Integrated test suite that evaluates cipher suites, derivations, and tamper-resistance live on your phone.
* 🎨 **Material Design 3 & Jetpack Compose:** Clean, dark-mode-first aesthetic with fluid animations, intuitive typography, and adaptive layouts.

---

## Step-by-Step User Guide

### Step 1: Create your Identity
1. Launch the app for the first time.
2. Choose a **display alias** (no real personal info required).
3. Dekachat will generate your local cryptographic keys and secure identity string immediately.

### Step 2: Connect with a Peer
Ensure both devices are connected to the **same Wi-Fi network or portable mobile hotspot**:
* **Option 1 (Instant QR Scan):** In the **Contacts** tab, tap **"+"** or **Scan QR**, and point your camera at your friend's profile QR code.
* **Option 2 (Manual Input):** Enter your peer's local IP address (displayed at the top of their screen, e.g. `192.168.1.45`) and their public identity key.

### Step 3: Verify the Security Fingerprint
1. Open the chat with your contact.
2. Tap the **Shield / Fingerprint** icon in the top app bar.
3. Visually compare the fingerprint code or tap **Scan Fingerprint** with your camera. When verified, the peer is marked with a verified green badge.

### Step 4: Chat, Record Voice Notes & Send Files
* **Text Chat:** Type your message and tap Send.
* **Voice Notes:** Press and hold the **microphone button** to record audio. Release to send encrypted.
* **Files & Photos:** Tap the **attachment (+)** icon to share pictures or documents directly.
* **Security Audit:** Open the top menu and select **Security Audit** to run on-device cryptographic verification tests anytime.

---

## Cryptographic & Network Architecture

```
┌─────────────────────────────────┐             Direct TCP Socket (Port 8988)          ┌─────────────────────────────────┐
│        Device A (Peer 1)        │◄──────────────────────────────────────────────────►│        Device B (Peer 2)        │
│  - Identity Key A               │           AES-256-GCM Encrypted Payload            │  - Identity Key B               │
│  - Local IP: 192.168.1.X        │     [IV (12B) | Ciphertext | AuthTag (16B)]        │  - Local IP: 192.168.1.Y        │
│  - Local Room SQLite Database   │                                                    │  - Local Room SQLite Database   │
└────────────────┬────────────────┘                                                    └────────────────┬────────────────┘
                 │                                                                                      │
                 │                    Mutual QR Fingerprint Verification                                │
                 └───────────────────────────────► 📷 ◄─────────────────────────────────────────────────┘
                                        (Zero-Trust Key Exchange)
```

### Symmetric Shared Key Agreement
Both devices compute an identical symmetric key using a commutative **SHA-256 Key Derivation Function (KDF)** over the sorted identity keys:
$$\text{SharedKey} = \text{SHA-256}(\text{"DEKACHAT\_E2EE\_AES256\_GCM\_V1"} \parallel \text{Key}_A \parallel \text{Key}_B)$$
This deterministic derivation ensures both parties arrive at the identical 256-bit AES key with no intermediary server handshake.

---

## Permissions & Privacy Guarantees

Dekachat requests only the minimal permissions required for user-initiated actions:

| Permission | Purpose | Privacy Guarantee |
| :--- | :--- | :--- |
| `CAMERA` | Scan QR codes for peer discovery and fingerprint verification. | Active only while scanning. Camera frames are processed in memory and never stored. |
| `RECORD_AUDIO` | Record interactive voice messages. | Active only when holding the record button. Audio is encrypted with AES-256-GCM before transport. |
| `INTERNET` / `ACCESS_NETWORK_STATE` | Direct local network TCP communication. | Traffic remains inside the local network. No external server connections are made. |

---

## Build and Development

### Prerequisites
* Android Studio Iguana / Jellyfish or newer.
* JDK 17 or JDK 21.
* Android SDK (minSdk 26, targetSdk 35).

### Build Commands
```bash
# Build debug APK
gradle assembleDebug

# Run unit and Robolectric tests
gradle :app:testDebugUnitTest
```

---

<p align="center">
  Crafted with care by <strong>DekaStudio</strong> • Prioritizing privacy, digital freedom, and open technology.
</p>
