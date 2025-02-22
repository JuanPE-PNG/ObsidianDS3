# Documento de Arquitectura del Sistema de Gestión de Órdenes y Entregas

  

## 1. Introducción  

Este documento describe la arquitectura inicial del sistema de gestión de órdenes y entregas, incluyendo requisitos funcionales, requisitos de calidad y restricciones clave que deben ser consideradas en el diseño del software.

  

**Equipo:** _[9]_  

**Integrantes:** _[Juan Pablo Escobar Viveros, Edgar Andres Vargas García, Cristian David, William Alexander Franco Otero, Jhojan Stiven Castaño Jejen, David Santiago Velasco Triana]_  

**Fecha:** _[20/02/2025]_  

  

---

  

## 2. Requisitos Funcionales  

Los requisitos funcionales se presentan en forma de **historias de usuario**, especificando los **criterios de aceptación**.

  

### **Historias de Usuario**

| **ID**    | **Historia de Usuario**                                                                                                           | **Criterios de Aceptación**                                                                                                                                                                                                                                                                                            |

| --------- | --------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |

| **US-01** | Como cliente registrado, quiero iniciar sesión en la plataforma para acceder a mi historial de pedidos y realizar nuevas compras. | - El usuario debe ingresar un correo y contraseña válidos.<br>- Si las credenciales son correctas, el usuario es redirigido a su perfil.<br>- Si las credenciales son incorrectas, se muestra un mensaje de error sin revelar detalles específicos.<br>- El usuario puede solicitar un restablecimiento de contraseña. |

| **US-02** | _[Agregar historia de usuario]_                                                                                                   | _[Agregar criterios de aceptación]_                                                                                                                                                                                                                                                                                    |

| **US-03** | _[Agregar historia de usuario]_                                                                                                   | _[Agregar criterios de aceptación]_                                                                                                                                                                                                                                                                                    |

|           |                                                                                                                                   |                                                                                                                                                                                                                                                                                                                        |

|           |                                                                                                                                   |                                                                                                                                                                                                                                                                                                                        |

  

>  **Instrucciones:**  

> - Completar al menos **tres historias de usuario**.  

> - Asegurar que cada historia tenga criterios de aceptación claros y verificables.  

  

---

  

## 3. Requisitos de Calidad  

Los requisitos de calidad se presentan en forma de **historias de calidad**, siguiendo la estructura de Len Bass.

| Fuente          | Estimulo                                                                                                                                          | Artefactos                                                      | Entorno                                                                                                                                        | Respuesta esperada                                                                                                                 | Medida de respuesta                                                                                                                                                  |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Cliente         | El cliente ingresa a la página                                                                                                                    | Módulo Web                                                      | Activo                                                                                                                                         | Se ingresa el usuario a la página                                                                                                  | La página no debe tardar más de 5 segundos al menos el 95% de las veces                                                                                              |
| Soporte técnico | Se reporta que la página se cae durante horas específicas de tráfico                                                                              | Sistema de Balance de carga                                     | Activo pero no maneja los picos de tráfico                                                                                                     | Se implementa un sistema de escalado automático para manejar picos de tráfico                                                      | El sistema debe mantener una disponibilidad del 99% durante las horas pico de tráfico, sin caerse y generando réplicas del backend para manejarlo                    |
| Administrador   | Quiere actualizar el inventario de los productos que se manejan en la tienda para poder mantener una contabilidad correcta, sencilla y ajustable. | Base de datos y sección solo para administradores en la página. | La actualización se realiza con éxito no importa la acción tomada (agregar, quitar, eliminar productos) excepto en mantenimiento del servicio. | El sistema permite al administrador agregar, modificar o eliminar productos del inventario, y reflejar los cambios en tiempo real. | Los cambios realizados por el administrador en el inventario se reflejan en la tienda en línea en menos de 2 segundos después de ser guardados por el administrador. |




  

---

  

## 4. Restricciones del Sistema  

Las restricciones establecen **limitaciones** en la arquitectura del sistema, ya sean tecnológicas, de negocio, regulatorias o de infraestructura.

  

### **Lista de Restricciones**

| **Tipo de Restricción** | **Descripción** |

|------------------------|----------------|

| Tecnológica | El sistema debe desarrollarse utilizando **Spring Boot y PostgreSQL**, debido a la infraestructura actual de la empresa y su compatibilidad con otros sistemas internos. |

| _[Agregar otro tipo]_ | _[Describir la restricción]_ |

  

>  **Tipos de restricciones:**  

> - **Tecnológicas:** Lenguajes, frameworks o herramientas que deben utilizarse.  

> - **De negocio:** Normativas o estándares de la empresa.  

> - **Regulatorias:** Cumplimiento de normativas legales o de seguridad.  

> - **De infraestructura:** Limitaciones en hardware, red o almacenamiento.  

  
  

---

  

## 5. Formato de Entrega  

- **Formato:** Markdown (`.md`) en el repositorio de Codelabs, El documento debe llamarse `Arquitectura.md`.  

- **Extensión máxima:** 3 páginas.  

  

---

  

## **Tiempo estimado para completar el ejercicio: 50 minutos**  

**15 min** → Definir **3 historias de usuario con criterios de aceptación**.  

**15 min** → Definir **3 historias de calidad alineadas con atributos clave**.  

**10 min** → Identificar **2 restricciones relevantes**.  

**10 min** → Revisión y ajustes finales del documento.