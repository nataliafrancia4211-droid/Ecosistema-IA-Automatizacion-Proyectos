# 🚀 Entrega Final: Ecosistema de Automatización IA Autónomo para Negocios

**Curso / Comisión:** Coderhouse #102325  
**Estudiante:** Natalia Francia Rodriguez  
**Proyecto:** Flujo de Gestión y Generación de Propuestas Comerciales con IA  

---

## 📹 Demostración en Video
🎬 **[Haz clic aquí para ver la Demostración en Video de la Automatización](https://drive.google.com/file/d/1sN4I5I_mU-uYGZN-6vQ-lX8aTgW2hSsT/view?usp=sharing)**

---

## 🛠️ Tecnologías Integradas
* **Orquestador:** n8n (Arquitectura de doble trigger)
* **Base de Datos / Memoria:** Notion (`Ecosistema_IA_Proyectos`)
* **Procesamiento IA:** Google Gemini API (`models/gemini-flash-lite-latest`)
* **Canales de Salida:** Gmail API & WhatsApp Business

---

## 🔗 Enlaces Importantes
* 📊 **Base de Datos en Notion (Modo Lectura):** [Ver Tabla Ecosistema_IA_Proyectos](https://app.notion.com/p/3de6e76a050c80b58518fa8b1bceac6c)
* 📄 **Documentación Completa en PDF:** Revisa el archivo `Ecosistema de Automatización IA.pdf` adjunto en este repositorio para ver el desglose técnico y las capturas de pantalla de evidencia.

---

## 📁 Archivos en este Repositorio
* `Ecosistema de Automatización IA.pdf`: Reporte de arquitectura, matriz de casos de prueba y capturas de evidencia.
* `Ecosistema_IA_Proyectos.json`: Blueprint/Workflow exportado de n8n listo para importar.

---

## 💡 Arquitectura y Lógica del Sistema (HITL)
Se diseñó una arquitectura de doble trigger desacoplada a través de la base de datos (Notion) para implementar de manera estricta el patrón **Human-In-The-Loop (HITL)**:
1. **Generación con IA:** El primer trigger procesa la solicitud del cliente mediante Google Gemini y persiste la propuesta en la DB en estado *"En revisión"*.
2. **Validación Humana:** El sistema se detiene en el nodo `Filter` evitando envíos no autorizados.
3. **Envío Multicanal:** Tras la aprobación manual en Notion (cambio de estado a *"Aprobado"*), el segundo trigger ejecuta el envío simultáneo por **Gmail** y **WhatsApp**.
4. **Optimización de Costos:** Se seleccionó Google Gemini por sobre OpenAI/Claude para garantizar una ejecución eficiente, de baja latencia y sin costos operativos en las pruebas de estrés.# Ecosistema-IA-Automatizacion-Proyectos
Entrega Final Coderhouse - Ecosistema de Automatización IA Autónomo con n8n, Notion, Gemini API, Gmail y WhatsApp.
