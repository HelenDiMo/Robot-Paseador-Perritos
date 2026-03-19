# 🐾 P.A.W.L-E: Protocolo Automático de Walkies y Limpieza Estándar

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![UI](https://img.shields.io/badge/Interfaz-Polimórfica-ff69b4?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Funcional-success?style=for-the-badge)

**P.A.W.L-E** es un simulador de robot autónomo diseñado para pasear perros. El proyecto utiliza lógica de programación para que el robot tome sus propias decisiones, gestione su energía y reconozca a sus "clientes" caninos.

---

## 🚀 Acceso a las Aplicaciones
He creado dos versiones del robot que comparten el mismo "cerebro" pero se ven de forma diferente:

* 🌸 [**Versión Kawaii**](https://ais-pre-zuhzshpfk53v2elx3nekk7-366529865543.europe-west2.run.app): Una interfaz amigable, con emojis y mensajes cariñosos.
* ⚙️ [**Versión Técnica (Seriota)**](https://ais-pre-dcriwrnpytpoi2i2tbx5or-366529865543.europe-west2.run.app/): Un enfoque minimalista centrado en los datos y el estado del sistema.

---

## 🗺️ Navegación y Prevención de Riesgos

P.A.W.L-E no solo camina, sino que analiza el suelo por donde pasa gracias a su **Radar de Superficie**:

* **Detección de Obstáculos:** En cada paso hay un **30% de probabilidad** de encontrar peligros como charcos, barro, cristales o asfalto caliente.
* **Esquive Automático:** Si detecta un riesgo, el robot avisa por pantalla y cambia la ruta para proteger al perro.
* **Gasto de Energía:** Maniobrar para evitar un obstáculo consume un **-2% extra de batería**, lo que obliga al robot a ser más eficiente.

---

## 🧠 Lógica de Funcionamiento

### ⚡ Gestión de Energía y Recursos
* **Modo Paseo:** Gasta un **12%** de batería mientras juega y pasea normal.
* **Protocolo de Retorno:** Si la batería baja del **40%** o se queda con **1 sola bolsa**, el robot activa el modo ahorro y vuelve directo a casa gastando solo un **4%**.
* **Eventos del Azar:** El robot puede recargar energía si sale el **Sol (+10%)** o gastar una **Bolsa (-1)** si el perro hace sus necesidades.

### 💾 Memoria de Usuarios
El robot tiene "memoria" gracias a un registro de nombres:
* **Reconocimiento:** Si un perro ya ha paseado con él, el robot lo reconoce y le da una bienvenida especial.
* **Historial:** Lleva la cuenta de cuántos paseos han compartido juntos.

---

## 📊 Reporte de Misión
Al terminar el paseo, el sistema muestra un resumen de datos:
* **Evolución de Batería:** Una lista con el nivel de energía minuto a minuto.
* **Índice de Felicidad:** Cuántos puntos de alegría ha conseguido el perro.
* **Diagnóstico Final:** Un chequeo de cómo han terminado los sistemas del robot.

---

## 👩‍💻 Sobre este proyecto

Este simulador ha sido mi proyecto práctico en el curso de **Introducción a la IA (80h)** de **[Fundación Somos F5](https://www.somosf5.org/)**. 

Al crear a P.A.W.L-E, he practicado conceptos básicos que son la base para entender cómo funcionan los programas inteligentes:

* **Programación con Clases (POO):** He organizado el código creando una "plantilla" (`RobotPaseador`) para que el robot sepa quién es, cuánta batería tiene y qué acciones puede hacer.
* **Toma de decisiones y Azar:** He programado al robot para que reaccione a cosas que pasan por sorpresa, como que aparezca un charco o que el perro necesite una bolsa.
* **Control de Energía:** He diseñado un sistema para que el robot vigile su propia batería y decida por sí mismo cuándo es hora de volver a casa para no quedarse tirado.
* **Manejo de Datos:** He aprendido a usar diccionarios para guardar los nombres de los perros y listas para registrar cómo va cambiando la energía durante la misión.

En resumen, he convertido un problema de la vida real en un **algoritmo funcional** que sabe reaccionar a su entorno.
