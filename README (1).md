# 📂 Manejo de Archivos en C

Este repositorio contiene ejemplos prácticos del uso de archivos en lenguaje C, incluyendo lectura y escritura en archivos binarios y de texto, manipulación del indicador de posición y uso de punteros.

## 📁 Contenido

- `src/`: Código fuente en C
- `ejemplos/`: Archivos de ejemplo (`.dat`)
- `README.md`: Documentación general

## ✅ Temas Cubiertos

- Archivos binarios y de texto
- Funciones: `fopen()`, `fclose()`, `fread()`, `fwrite()`, `fprintf()`, `fscanf()`, `fseek()`, `ftell()`, `feof()`
- Uso de punteros `FILE *`
- Manejo de estructuras en archivos

## 🚀 Ejecución

Compilar con:
```bash
gcc src/escribir_binario.c -o escribir_binario
```

Ejecutar con:
```bash
./escribir_binario
```

---

## 📌 Ejemplos incluidos

### 🔸 Escritura binaria
Guarda estructuras en un archivo binario.

```c
FILE *archivo;
struct Persona persona = {"Pedro", 28};
archivo = fopen("ejemplos/bin.dat", "wb");
fwrite(&persona, sizeof(persona), 1, archivo);
fclose(archivo);
```

---

### 🔸 Lectura binaria
Lee estructuras desde un archivo binario.

```c
FILE *archivo;
struct Persona persona;
archivo = fopen("ejemplos/bin.dat", "rb");
while (fread(&persona, sizeof(persona), 1, archivo) == 1) {
    printf("%s %d\n", persona.nombre, persona.edad);
}
fclose(archivo);
```

---

### 🔸 Obtener tamaño de archivo
Utiliza `fseek` y `ftell` para obtener el tamaño.

```c
FILE *archivo = fopen("ejemplos/bin.dat", "rb");
fseek(archivo, 0L, SEEK_END);
long tamaño = ftell(archivo);
fclose(archivo);
printf("El archivo tiene %ld bytes\n", tamaño);
```

---

## 📌 Requisitos

- GCC o cualquier compilador de C
- Entorno compatible con línea de comandos
- Sistema de archivos que permita escritura de archivos `.dat`

---

## 🔒 Licencia

Este proyecto se distribuye bajo la licencia MIT. Libre para usar y modificar.
