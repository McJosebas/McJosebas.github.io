---
title: "Sistema de Báscula Industrial y Dosificación con Node-RED"
description: "Sistema de pesaje industrial integrado con PLC Siemens S7 y base de datos SQL, desarrollado con Node-RED para la gestión de órdenes, lotes, fórmulas e incidencias en tiempo real."
publishDate: 2026-01-15
isFeatured: true
seo:
  image:
    src: "../../assets/images/Project3/Project3_1.png"
---

![Project preview](../../assets/images/Project3/Project3_1.png)

**Nota:** Este caso de estudio muestra un proyecto real de automatización industrial enfocado a sistemas de pesaje, dosificación, trazabilidad y supervisión de procesos mediante tecnologías abiertas.

**Descripción general del proyecto:**  
Diseño e implementación de un **sistema de báscula industrial** basado en **Node-RED**, encargado de la supervisión del pesaje de ingredientes asociados a órdenes de producción.  
El sistema permite visualizar pesos, consignas, porcentajes, lotes y recetas en tiempo real, además de gestionar incidencias y acciones manuales desde una **HMI web** integrada con PLC Siemens S7 y base de datos SQL Server.

---

## 🛠️ Tecnologías

<div style="display: flex; gap: 10px; align-items: center; flex-wrap: wrap;">
  <img src="https://img.shields.io/badge/PLC-Siemens%201200-brightgreen" alt="Siemens PLC">
  <img src="https://img.shields.io/badge/HMI-Node--RED%20Dashboard-blue" alt="Node-RED Dashboard">
  <img src="https://img.shields.io/badge/SCADA-Node--RED-red" alt="Node-RED">
  <img src="https://img.shields.io/badge/Database-SQL%20Server-black" alt="SQL Server">
  <img src="https://img.shields.io/badge/Protocol-ISO--on--TCP%20%7C%20TCP%2FIP-orange" alt="Network">
</div>

- **PLC:** Siemens SIMATIC S7 1200
- **HMI / SCADA:** Node-RED + Node-RED Dashboard  
- **Base de Datos:** Microsoft SQL Server  
- **Comunicaciones:** ISO-on-TCP, TCP/IP  
- **Software:** Node-RED, Tia Portal, Movicon, MySQL
---

## 🔄 Workflow del Proyecto

### 1. Análisis del Proceso y Requisitos 🎯
- Identificación de las necesidades del proceso de pesaje:
  - Visualización de **peso bruto, neto y consigna**
  - Gestión de **órdenes de producción**
  - Control de **lotes**
  - Consulta de **recetas y fórmulas**
  - Detección y gestión de **incidencias**
- Definición de una solución flexible y escalable basada en Node-RED.

---

### 2. Diseño de la Arquitectura del Sistema 🖌️
- Arquitectura basada en:
  - **PLC Siemens** como controlador del proceso
  - **Node-RED** como sistema de supervisión
  - **Base de datos SQL** para gestión de recetas y órdenes
  - **HMI web** accesible desde navegador
- Separación clara entre:
  - Control de proceso
  - Visualización
  - Gestión de datos
  - Acciones manuales

---

### 3. Integración PLC – Node-RED 🛜
- Comunicación directa con el PLC mediante **ISO-on-TCP**
- Lectura cíclica de variables críticas:
  - Pesos
  - Identificadores de orden y artículo
  - Estado del proceso
  - Señales de incidencia
- Escritura de comandos desde la HMI:
  - Reintentar pesaje
  - Continuar proceso
  - Avanzar al siguiente producto

---

### 4. Gestión del Pesaje y Cálculos ⚖️
- Visualización en tiempo real de:
  - Peso bruto
  - Peso neto
  - Peso consigna
- Cálculo automático del **porcentaje de llenado**
- Representación gráfica del estado del pesaje mediante indicadores dinámicos.

---

### 5. Gestión de Órdenes, Artículos y Fórmulas 📦
- Detección automática de nuevas órdenes de producción
- Consulta a SQL Server para obtener:
  - Artículos a dosificar
  - Cantidades objetivo
  - Tolerancias permitidas
- Visualización del:
  - Producto actual
  - Lista completa de ingredientes
  - Cantidades y tolerancias asociadas

---

### 6. Gestión de Lotes 🔢
- Control del proceso mediante:
  - Lote actual
  - Número total de lotes
- Visualización clara del progreso de la producción para el operario.

---

### 7. Gestión de Incidencias 🚨
- Detección automática de incidencias:
  - Falta de producto
  - Pesaje fuera de tolerancia
- Visualización clara de alarmas en la HMI
- Habilitación dinámica de controles manuales según el estado del proceso.

---

### 8. Desarrollo de la Interfaz HMI 📺
- HMI desarrollada con **Node-RED Dashboard**
- Interfaz orientada al operario:
  - Información clara y en tiempo real
  - Acciones manuales accesibles
  - Gestión visual de incidencias
- Control dinámico de la visibilidad de secciones según el estado del proceso.

---

### 9. Pruebas y Puesta en Marcha 🔩
- Pruebas de:
  - Comunicación PLC – Node-RED
  - Lectura y escritura de variables
  - Consultas a base de datos
  - Gestión de incidencias
- Validación del sistema en entorno industrial real.

---

### 10. Resultados Obtenidos ✅
- Supervisión completa del proceso de pesaje
- Reducción de errores operativos
- Mejora de la trazabilidad del proceso
- Alternativa flexible y escalable a sistemas SCADA tradicionales
- Integración efectiva entre PLC, base de datos y HMI web

---

### 11. Diagrama de Arquitectura

[![Diagrama de Arquitectura](/images/Project2/Project2_2.png)](/images/Project2/Project2_2.png)

