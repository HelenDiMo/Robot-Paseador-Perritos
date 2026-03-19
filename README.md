# 🐾 P.A.W.L-E: Personal Assistant for Walking & Leisure Entities

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![UI](https://img.shields.io/badge/Interfaz-Polimórfica-ff69b4?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Funcional-success?style=for-the-badge)

**P.A.W.L-E** es un simulador de robot autónomo de acompañamiento canino desarrollado en Python. El proyecto implementa lógica de toma de decisiones en tiempo real, gestión de recursos limitados y un sistema de memoria persistente para el reconocimiento de usuarios.

---

## 🚀 Acceso a las Aplicaciones
El proyecto cuenta con dos versiones desplegadas que comparten el mismo núcleo lógico pero ofrecen experiencias de usuario (UX) distintas:

* ⚙️ [**Versión Técnica**](https://ais-pre-zuhzshpfk53v2elx3nekk7-366529865543.europe-west2.run.app): Enfoque minimalista y robótico, orientado a datos y monitorización de sistemas.
* 🌸 [**Versión Kawaii**](https://ais-pre-dcriwrnpytpoi2i2tbx5or-366529865543.europe-west2.run.app/): Diseñada para una conexión emocional, con mensajes amigables y estética colorida.

---

## 🧠 Lógica de Funcionamiento

El robot opera bajo un **motor de estados** que evalúa variables críticas cada 5 minutos de tiempo simulado:

### ⚡ Gestión de Energía y Recursos
* **Modo Exploración:** Gasto de batería del **12%** por tramo mientras interactúa con el entorno.
* **Protocolo de Retorno (Modo Ahorro):** Si la batería cae por debajo del **40%** o se agotan las bolsas de residuos, el robot prioriza la supervivencia reduciendo el consumo al **4%**.
* **Eventos Aleatorios:**
    * **Recarga Solar (20% prob.):** El robot detecta luz solar y recupera un **10%** de energía.
    * **Evento Biológico (50% prob.):** El perro realiza sus necesidades, restando una bolsa del inventario.

### 💾 Memoria de Usuario (Persistence)
El sistema utiliza un registro global para identificar a los perros por su nombre:
* **Nuevos Usuarios:** Crea un perfil único en el primer encuentro.
* **Usuarios Recurrentes:** Reconoce al perro y contabiliza el historial de paseos realizados, personalizando el saludo inicial.

---

## 🛠️ Arquitectura Técnica

El código sigue el paradigma de **Programación Orientada a Objetos (POO)**:

1. **`RobotPaseador` (Clase):** Define el estado (batería, bolsas, felicidad) y las acciones base (saludar, pasear, autodiagnóstico).
2. **`REGISTRO_PERROS` (Data Store):** Diccionario persistente durante la sesión que almacena la frecuencia de uso.
3. **Loop de Misión:** Bucle principal que procesa la lógica de tiempo, eventos estocásticos y condiciones de parada.

---

## 📊 Reporte de Misión
Al finalizar cada simulación, el sistema genera:
* **Gráfica de Consumo:** Un historial detallado del nivel de batería frente al tiempo.
* **Índice de Felicidad:** Métrica acumulada basada en la calidad y duración del paseo.
* **Diagnóstico Final:** Estado de integridad del hardware tras la misión.

---

## 👩‍💻 Sobre este proyecto
Este simulador ha sido creado como un proyecto de aprendizaje en **Desarrollo de Software e Inteligencia Artificial**, demostrando la capacidad de separar la lógica de negocio (Backend) de la presentación visual (Frontend).
