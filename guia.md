# Respuestas del Cuestionario Repaso - 3º Parcial (Explicadas)

---

### En la mayoría de los casos, NO afecta el orden, porque:
- gcc main.c input.c operaciones.c -o programa es igual que gcc operaciones.c input.c main.c -o programa
- Siempre que todas las dependencias estén satisfechas, el programa va a compilar igual.
- Porque gcc primero compila todos los .c por separado, y luego los enlaza juntos en el ejecutable.

**Respuesta correcta:** Todas las opciones  
**Explicación:** El orden de compilación no afecta si todas las dependencias se resuelven correctamente.

---

### En C, el archivo .h (header) y el archivo .c (implementación) suelen tener el mismo nombre.
**Respuesta correcta:** Verdadero  
**Explicación:** No es obligatorio, pero es buena práctica mantener coherencia en el nombre de archivo de cabecera y de implementación.

---

### Trabajar con archivos binarios está asociado con el uso de estructuras.
**Respuesta correcta:** Verdadero  
**Explicación:** Las estructuras permiten almacenar registros completos de forma eficiente, y se usan habitualmente en archivos binarios.

---

### En C todas las operaciones que se realizan sobre archivos son hechas a través de funciones.
**Respuesta correcta:** Verdadero  
**Explicación:** Existen funciones estándar en C para el manejo de archivos que acceden directamente mediante punteros FILE*.

---

### Las listas doblemente encadenadas tienen dos punteros, uno que apunta al primer elemento y otro al último.
**Respuesta correcta:** Verdadero  
**Explicación:** Esto permite recorrido en ambas direcciones de la lista.

---

### Modos de apertura de archivo (r+, rb, a) corresponden a modos válidos.
**Respuesta correcta:** Todas las opciones son verdaderas  
**Explicación:** Son modos válidos para abrir archivos en C según se desee lectura, escritura o binario.

---

### Cuando el buffer se llena o se vacía, se actualizan los datos desde y hacia el archivo.
**Respuesta correcta:** Verdadero  
**Explicación:** El buffer intermedio permite realizar operaciones más eficientes al agrupar lecturas o escrituras.

---

### Definición de archivo como estructura de registros y campos.
**Respuesta correcta:** Archivo  
**Explicación:** Un archivo se compone de registros (entidades iguales) con campos (atributos).

---

### Modularización: dividir el programa en partes más pequeñas.
**Respuesta correcta:** Verdadero  
**Explicación:** Mejora la organización, el trabajo en equipo, y el mantenimiento del código.

---

### El uso de buffer significa acceso indirecto al archivo.
**Respuesta correcta:** Falso  
**Explicación:** Se accede al buffer, y no directamente al archivo.

---

### Beneficios de la modularidad: orden, reutilización, trabajo en equipo y mantenimiento.
**Respuesta correcta:** Todas las opciones  
**Explicación:** Estos beneficios están directamente asociados al uso de módulos.

---

### Métodos de acceso: secuencial no implica acceso directo al registro.
**Respuesta correcta:** Falso  
**Explicación:** En acceso secuencial se recorren los registros uno a uno hasta llegar al deseado.

---

### Eliminación del primer nodo en lista simplemente encadenada:
```c
t := prim;
prim := *t.proximo;
disponer(t);
```
**Respuesta correcta:** Eliminar el primer elemento de la lista  
**Explicación:** Se guarda el nodo inicial, se pasa al siguiente y se libera el primero.

---

### Pila: primero en entrar, primero en salir (FIFO)
**Respuesta correcta:** Verdadero  
**Explicación:** Es el principio básico de funcionamiento de las pilas.

---

### Clasificación del archivo según tipo de datos:
**Respuesta correcta:** Archivo binario y de texto  
**Explicación:** Es una clasificación común según el tipo de contenido del archivo.

---

### Función recursiva:
```c
function Recursiva(int x, int y) {
  if(y == 0) return x;
  else return Recursiva(x + 1, y - 1);
}
```
**Respuesta correcta:** La función recursiva permite que cualquier número natural sumado a otro sea la suma del primero +1 y el segundo decrementado en 1.

---

### Separación de módulos:
- .h → declaraciones
- .c → implementación
- main.c → programa principal

**Respuesta correcta:** Verdadero  
**Explicación:** Es una convención común en programación modular en C.

---

### Modos de apertura de archivo:
- `t` → texto (por defecto)
- `b` → binario

**Respuesta correcta:** Verdadero  
**Explicación:** Son los modificadores estándar para el modo de archivo en C.
