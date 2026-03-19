# 🐾 P.A.W.L-E: Personal Assistant for Walking & Leisure Entities

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![UI](https://img.shields.io/badge/Interfaz-Polimórfica-ff69b4?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Funcional-success?style=for-the-badge)

**P.A.W.L-E** es un simulador de robot autónomo para el acompañamiento canino. El proyecto implementa una arquitectura basada en **Programación Orientada a Objetos (POO)** que gestiona la supervivencia del hardware y el bienestar del animal mediante un motor de estados dinámico.

---

## 🚀 Acceso a las Aplicaciones

El proyecto dispone de dos despliegues con el mismo núcleo lógico pero distintos enfoques de experiencia de usuario (UX):

* ⚙️ [**Versión Técnica**](https://ais-pre-zuhzshpfk53v2elx3nekk7-366529865543.europe-west2.run.app): Enfoque minimalista y robótico, orientado a datos y monitorización de sistemas.
* 🌸 [**Versión Kawaii**](https://ais-pre-dcriwrnpytpoi2i2tbx5or-366529865543.europe-west2.run.app/): Diseñada para una conexión emocional, con mensajes amigables y estética colorida.

---
## 🗺️ Navegación y Prevención de Riesgos

A diferencia de los simuladores lineales, P.A.W.L-E incorpora un **Sistema de Escaneo de Ruta** (`escanear_ruta`) activo durante toda la misión:

* **Radar de Superficie (30% prob.):** Detecta peligros en tiempo real como charcos, barro, cristales o asfalto caliente.
* **Recalculado de Ruta:** Al detectar un obstáculo, el robot ejecuta una maniobra evasiva automática para proteger la integridad física del perro.
* **Coste de Maniobra:** Cada evasión consume un **-2% adicional de batería**, simulando el esfuerzo mecánico de los servomotores al cambiar de trayectoria.
  
## 🧠 Lógica de Funcionamiento

El robot opera bajo un **motor de estados** que evalúa variables críticas cada 5 minutos de tiempo simulado:

### ⚡ Gestión de Energía y Recursos
* **Consumo Estándar:** -12% de batería por tramo de actividad.
* **Protocolo de Retorno:** Se activa automáticamente si la `Batería < 40%` o `Bolsas <= 1`. El robot entra en modo ahorro reduciendo el consumo a un **-4%**.
* **Autorecarga Solar (`autorecarga`):** Probabilidad del 20% de detectar luz solar, recuperando un **+10%** de energía.
* **Gestión de Residuos:** Probabilidad del 50% de deposiciones caninas, consumiendo **1 bolsa** por evento.

### 💾 Memoria de Usuario (Persistence)
El sistema utiliza un registro global para identificar a los perros por su nombre, permitiendo:
* Reconocimiento de usuarios recurrentes.
* Seguimiento del historial de paseos acumulados por cada perfil.
---

## 🛠️ Arquitectura Técnica

El código está organizado para facilitar su escalabilidad:

1. **Clase `RobotPaseador`**: Encapsula todos los métodos de acción (`saludar`, `pasear`, `autorecarga`, `escanear_ruta`).
2. **Bucle de Misión**: Motor estocástico que procesa el tiempo y los eventos aleatorios.
3. **Métricas**: Generación de un historial de batería y tiempo para su posterior análisis gráfico.

---

## 📊 Reporte de Misión
Al finalizar cada simulación, el sistema genera:
* **Gráfica de Consumo:** Un historial detallado del nivel de batería frente al tiempo.
* **Índice de Felicidad:** Métrica acumulada basada en la calidad y duración del paseo.
* **Diagnóstico Final:** Estado de integridad del hardware tras la misión.

---

## 👩‍💻 Sobre este proyecto
Este simulador ha sido creado como un proyecto de aprendizaje en **Desarrollo de Software e Inteligencia Artificial**, demostrando la capacidad de separar la lógica de negocio (Backend) de la presentación visual (Frontend).

Desarrollado como proyecto final de aprendizaje en **Desarrollo de Software e IA**, centrando el foco en la resiliencia de sistemas autónomos y la creación de interfaces adaptativas.
