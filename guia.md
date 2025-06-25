# 📘 Respuestas Comentadas del Cuestionario - Repaso 3º Parcial

Este documento contiene las respuestas correctas e incorrectas del cuestionario con una breve explicación.

---

## ✅ Pregunta 1
**✔ Correcta**  
**Explicación**: Es una afirmación general válida sobre compilación o estructura en C.

---

## ✅ Pregunta 2
**✔ Correcta**  
**Explicación**: El orden de los archivos `.c` al compilar con `gcc` generalmente **no afecta** si todas las dependencias están satisfechas. `gcc` compila por separado y luego enlaza.

---

## ✅ Pregunta 3
**✔ Correcta**  
**Explicación**: Aunque es buena práctica que los archivos `.h` y `.c` tengan el mismo nombre, **no es obligatorio**.

---

## ✅ Pregunta 4
**✔ Correcta**  
**Explicación**: La afirmación técnica sobre archivos o funciones fue válida.

---

## ❌ Pregunta 5
**✘ Incorrecta**  
**Tu respuesta**: Falso  
**Correcta**: Verdadero  
**Explicación**: El uso de archivos binarios **está relacionado con estructuras** (`struct`) ya que facilitan el manejo de datos complejos en un solo bloque.

**Versión corregida**: Trabajar con archivos binarios está asociado al uso de estructuras.

---

## ✅ Pregunta 6
**✔ Correcta**  
**Explicación**: Se refiere correctamente a una función o comportamiento estándar del lenguaje.

---

## ❌ Pregunta 7
**✘ Incorrecta**  
**Tu respuesta**: Falso  
**Correcta**: Verdadero  
**Explicación**: La función `fseek()` modifica la posición del puntero en un archivo abierto. No reabre el archivo.

**Versión corregida**: `fseek()` modifica el puntero del archivo, no lo reabre.

---

## ❌ Pregunta 8
**✘ Incorrecta**  
**Tu respuesta**: Verdadero  
**Correcta**: Falso  
**Explicación**: `fread()` al llegar al final del archivo activa `feof()`, **no `ferror()`**.

**Versión corregida**: `fread()` activa `feof()` al llegar al final del archivo.

---

## ✅ Pregunta 9
**✔ Correcta**  
**Explicación**: La afirmación concuerda con la definición y uso correcto de funciones estándar.

---

## ✅ Pregunta 10
**✔ Correcta**  
**Explicación**: `fprintf()` formatea y escribe texto en un archivo, como se describe.

---

## ❌ Pregunta 11
**✘ Incorrecta**  
**Tu respuesta**: Verdadero  
**Correcta**: Falso  
**Explicación**: `feof()` **solo detecta fin de archivo tras una lectura fallida**, no antes.

**Versión corregida**: `feof()` no se activa anticipadamente, solo después de una operación fallida.

---

## ✅ Pregunta 12
**✔ Correcta**  
**Explicación**: La afirmación era precisa según el funcionamiento de buffers o estructuras.

---
