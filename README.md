<div align="center">

#  Interfaz Calculadora de IMC

[![Java](https://img.shields.io/badge/Java-21%2B-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)](https://www.oracle.com/java/)
[![Swing](https://img.shields.io/badge/GUI-Java%20Swing-007396?style=for-the-badge&logo=java&logoColor=white)](https://docs.oracle.com/javase/tutorial/uiswing/)
[![Architecture](https://img.shields.io/badge/Architecture-MVC-informational?style=for-the-badge)](#arquitectura)


<p align="center">
  Aplicación para <strong>Java Swing</strong> diseñada para el cálculo y categorización del Índice de Masa Corporal (IMC) según los datos de la OMS, implementando el patrón <strong>Modelo-Vista-Controlador (MVC)</strong>.
</p>


</div>

---

## Características

- **Cálculo instantáneo:** Evalúa el índice de masa corporal normalizando las entradas numéricas (manejo de comas y puntos decimales).
- **Clasificación clínica:** Categoriza el resultado en tiempo real (*Bajo Peso*, *Peso Normal*, *Sobrepeso*, *Obesidad*).
- **Validación robusta:** Control de excepciones (`NumberFormatException`) frente a entradas incorrectas.
- **Desacoplamiento total:** Separación estricta de responsabilidades mediante MVC.

---

##  Tecnologías y Arquitectura

### Stack
- **Lenguaje:** Java 21+ / Ant Build System
- **GUI:** Java Swing & NetBeans GUI Builder (AWT/Swing Layouts)

### Arquitectura (MVC)
El proyecto desacopla deliberadamente la capa visual de la lógica matemática para garantizar testabilidad y mantenibilidad:

```text
src/com/calculadoraPeso/imc/
├── model/        # CalculadoraIMC: Reglas de cálculo y rangos OMS
├── view/         # IMCVista: Componentes Swing e interfaz gráfica
├── controller/   # IMCController: Manejo de eventos (Listeners) y validaciones
└── main/         # Main: Inicialización y bootstrap del JFrame
```

---

##  Instalación y Ejecución

### Prerrequisitos
- JDK 17 o superior instalado (`java -version`).
- Git instalado (o descargar el archivo `.zip`).

### Pasos rápidos

1. **Clonar el repositorio:**
   ```bash
   git clone https://github.com/https://github.com/geuguis/Interfaz-Calculadora-IMC.git
   cd Interfaz-Calculadora-IMC
   ```

2. **Compilar y ejecutar:**
   - **Desde terminal:**
     ```bash
     javac -d build/classes src/com/calculadoraPeso/imc/*/*.java
     java -cp build/classes com.calculadoraPeso.imc.main.Main
     ```
   - **Desde IDE:**  
     Abre el proyecto directamente en **NetBeans**, **IntelliJ IDEA** o **Eclipse** y ejecuta `Main.java`.

---

##  Autor

Desarrollado por **Guillermo Eugui Sánchez**  
- **GitHub:** [@geuguis](https://github.com/geuguis)  
- **LinkedIn:** [Guillermo Eugui Sánchez](https://es.linkedin.com/in/guillermoeuguisanchez)  
*(Desarrollo de Aplicaciones Multiplataforma - Módulo DI)*