---
title: "Sistema de Etiquetado Automático 4 Caras con Visión Artificial"
description: "Estación automática para etiquetado secuencial de cajas en cuatro caras, con verificación mediante visión artificial y control de movimiento de alta precisión."
publishDate: 2026-01-07
isFeatured: true
seo:
  image:
    src: "../../assets/images/Project2/Project2.jpeg"
---

![Project preview](../../assets/images/Project2/Project2.jpeg)

**Nota:** Este caso de estudio muestra un proyecto real de automatización industrial orientado a trazabilidad, control de calidad y etiquetado automático en línea de producción.

**Descripción general del proyecto:**  
Diseño e implementación de una **estación automática de etiquetado 4 caras** para cajas industriales. El sistema gestiona el posicionamiento preciso del producto, la impresión y aplicación de etiquetas, y la **verificación del código QR mediante visión artificial**, garantizando que ningún producto salga de la estación sin una identificación válida y legible.

---

## 🛠️ Tecnologías

<div style="display: flex; gap: 10px; align-items: center; flex-wrap: wrap;">
  <img src="https://img.shields.io/badge/x2%20PLC-Siemens%20S7--1200-brightgreen" alt="Siemens PLC">
  <img src="https://img.shields.io/badge/HMI1-KTP700-blue" alt="HMI1">
  <img src="https://img.shields.io/badge/HMI2-NB3Q%20TW00B-blue" alt="HMI1">  
  <img src="https://img.shields.io/badge/Motion-Panasonic%20MINAS%20LIQI-purple" alt="Motion Control">
  <img src="https://img.shields.io/badge/Vision-Cognex%20In--Sight-red" alt="Vision">
  <img src="https://img.shields.io/badge/Printer-Zebra%20ZE500-black" alt="Zebra">
  <img src="https://img.shields.io/badge/Network-Profinet%20%7C%20TCP%2FIP-orange" alt="Network">
</div>

- **PLC:** 2x Siemens SIMATIC S7-1200 (Arquitectura Maestro–Esclavo)  
- **HMI:** Siemens KTP700 Basic y NB3Q-TW00B-V1
- **Motion Control:** Servomotor Panasonic MINAS LIQI (Control PTO)  
- **Visión Artificial:** Cámara Cognex In-Sight 8000  
- **Impresión:** Zebra ZE500 (motor de impresión industrial)  
- **Comunicaciones:** Profinet, TCP/IP, FTP  
- **Neumática:** Vacío y soplado para transferencia de etiquetas  
- **Software:** TIA Portal V17 + Maewin (Etiquetas) + NB-Designer + In‑Sight Explorer + PANATERM (driver)

---

## 🎯 Objetivos

1. Automatizar el **etiquetado completo de cajas en sus cuatro caras** sin intervención manual.  
2. Garantizar **trazabilidad total del producto** mediante códigos QR verificados por visión artificial.  
3. Implementar una lógica de control **robusta, segura y estandarizada** siguiendo la Guía GEMMA.  
4. Reducir errores de impresión y lectura a **cero productos defectuosos** en salida de estación.  

---

## ⚡ Características

### 1. Control y Posicionamiento de Alta Precisión
- Uso de **servomotores** para el posicionamiento exacto de la caja durante el proceso de etiquetado.  
- Sincronización precisa entre movimiento, impresión y aplicación de etiquetas.  

### 2. Arquitectura de Control Industrial
- Red **Profinet** para comunicación rápida y fiable entre PLCs, HMI y periféricos.  
- Programación desarrollada en **TIA Portal V17**, combinando:
  - **KOP:** Secuenciación principal del proceso.
  - **SCL:** Gestión de datos, validaciones y cálculos.

### 3. Gestión de Estados – Guía GEMMA
- Modos de funcionamiento claramente definidos:
  - **Producción automática**
  - **Modo preparación (F2)**
  - **Parada en estado inicial (A1)**
- Gestión segura de arranques, paradas y rearme tras fallo.  
- Integración de **paradas de emergencia** y condiciones de seguridad.

### 4. Sistema de Verificación por Visión Artificial
- La cámara **Cognex In-Sight** valida:
  - Presencia de etiqueta  
  - Calidad del código QR  
  - Legibilidad del contenido  
- En caso de fallo:
  - Bloqueo del avance de la caja  
  - Solicitud automática de **reimpresión de etiqueta**  
- Garantía de **calidad 100% verificada** antes de salida.

### 5. Gestión de Errores y Reintentos
- Reintento automático de impresión ante errores de lectura.  
- Registro de estados y fallos para diagnóstico rápido por mantenimiento.  


### 6. Diagrama de Arquitectura

[![Diagrama de Arquitectura](/images/Project2/Project2_2.png)](/images/Project2/Project2_2.png)

---

## 📂 Documentación del Proyecto

- **Manual de Usuario:** Operación, seguridad y prevención de riesgos.<br>
[⬇️ Descargar Manual de Usuario (PDF)](/pdf/MANUAL_USUARIO.pdf)

- **Manual de Funcionamiento:** Lógica de control, secuencias y estados GEMMA.<br>
[⬇️ Descargar Manual de Usuario (PDF)](/pdf/MANUAL_USUARIO.pdf)

- **Manual de Comunicaciones:** Red, direcciones IP y protocolos de datos.<br>
[⬇️ Descargar Manual de Comunicaciones (PDF)](/pdf/MANUAL_USUARIO.pdf)

- **Manual de HMI:** Guia para el operario.<br>
[⬇️ Descargar Manual de HMI (PDF)](/pdf/MANUAL_USUARIO.pdf)

- **Manual de Grafet y Programa:** Construccion del programa de manera interna.<br>
[⬇️ Descargar Manual de Grafet y Programa (PDF)](/pdf/MANUAL_USUARIO.pdf)

---

