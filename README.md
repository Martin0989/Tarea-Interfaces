# Tarea-Interfaces
Actividad: Optimización de la Aplicación de Gestión de Contactos 
# GUÍA DE USUARIO
## Sistema de Gestión de Contactos Optimizado

---

## 📋 ÍNDICE

1. Introducción
2. Instalación y Configuración
3. Funcionalidades Principales
4. Atajos de Teclado
5. Solución de Problemas
6. Preguntas Frecuentes

---

## 1. INTRODUCCIÓN

El Sistema de Gestión de Contactos es una aplicación de escritorio desarrollada en Java que permite administrar información de contactos de manera eficiente, con funciones de búsqueda, filtrado, ordenamiento y exportación.

### Características Principales
- ✅ Gestión completa de contactos (Agregar, Modificar, Eliminar)
- ✅ Búsqueda en tiempo real
- ✅ Ordenamiento por cualquier columna
- ✅ Exportación a formato CSV
- ✅ Estadísticas automáticas
- ✅ Interfaz intuitiva con pestañas
- ✅ Atajos de teclado para mayor productividad

---

## 2. INSTALACIÓN Y CONFIGURACIÓN

### Requisitos Previos
- **Java JDK:** Versión 8 o superior
- **Sistema Operativo:** Windows, Linux o macOS
- **Espacio en Disco:** Mínimo 50 MB

### Pasos de Instalación

1. **Descargar el código fuente**
   ```
   Descargar los archivos del proyecto
   ```

2. **Compilar el proyecto**
   ```bash
   javac -d bin src/**/*.java
   ```

3. **Ejecutar la aplicación**
   ```bash
   java -cp bin main.AplicacionContactos
   ```

### Primera Ejecución

Al ejecutar por primera vez:
- Se creará automáticamente la carpeta `c:/gestionContactos/`
- Se generará el archivo `datosContactos.csv` para almacenar los contactos
- La aplicación estará lista para usar

---

## 3. FUNCIONALIDADES PRINCIPALES

### 3.1 Pestaña "Contactos"

#### Agregar un Nuevo Contacto

1. Completar los campos del formulario:
   - **Nombres:** Nombre completo del contacto
   - **Teléfono:** Número de teléfono
   - **Email:** Correo electrónico
   
2. Seleccionar una **Categoría** (Familia, Amigos, Trabajo)

3. Marcar como **Favorito** (opcional)

4. Hacer clic en el botón **AGREGAR** o presionar `Ctrl + S`

5. El contacto aparecerá en la tabla automáticamente

**Validaciones:**
- Todos los campos son obligatorios
- Debe seleccionar una categoría válida
- Se mostrará un mensaje de confirmación al guardar

#### Modificar un Contacto Existente

**Opción 1: Usando botones**
1. Seleccionar el contacto en la tabla
2. Los datos se cargarán automáticamente en el formulario
3. Modificar los campos deseados
4. Hacer clic en **MODIFICAR**

**Opción 2: Usando menú contextual**
1. Clic derecho sobre el contacto en la tabla
2. Seleccionar "Editar"
3. Modificar los datos
4. Guardar cambios

#### Eliminar un Contacto

**Opción 1: Usando botón**
1. Seleccionar el contacto en la tabla
2. Hacer clic en **ELIMINAR** o presionar `Ctrl + E`
3. Confirmar la eliminación en el diálogo

**Opción 2: Usando menú contextual**
1. Clic derecho sobre el contacto
2. Seleccionar "Eliminar"
3. Confirmar la acción

#### Buscar Contactos

1. Escribir en el campo **BUSCAR** en la parte inferior
2. La tabla se filtrará automáticamente mientras escribe
3. La búsqueda aplica a todos los campos (nombre, teléfono, email, categoría)
4. Para ver todos los contactos nuevamente, borrar el texto de búsqueda

#### Ordenar Contactos

1. Hacer clic en el encabezado de cualquier columna
2. **Primer clic:** Ordena ascendentemente
3. **Segundo clic:** Ordena descendentemente
4. Se puede ordenar por: Nombre, Teléfono, Email, Categoría o Favorito

#### Exportar Contactos a CSV

1. Hacer clic en el botón **EXPORTAR CSV**
2. Seleccionar la ubicación y nombre del archivo
3. Hacer clic en "Guardar"
4. El archivo CSV se generará con todos los contactos

**Formato del archivo exportado:**
```
NOMBRE,TELEFONO,EMAIL,CATEGORIA,FAVORITO
Juan Pérez,0991234567,juan@email.com,Familia,true
María López,0987654321,maria@email.com,Amigos,false
```

### 3.2 Pestaña "Estadísticas"

Muestra información resumida sobre los contactos:

- **Total de Contactos:** Cantidad total de contactos registrados
- **Contactos Favoritos:** Cantidad de contactos marcados como favoritos
- **Por Categoría:**
  - Familia
  - Amigos
  - Trabajo

Las estadísticas se actualizan automáticamente al:
- Agregar un nuevo contacto
- Modificar un contacto existente
- Eliminar un contacto

---

## 4. ATAJOS DE TECLADO

| Atajo | Acción | Descripción |
|-------|--------|-------------|
| `Ctrl + N` | Nuevo Contacto | Limpia el formulario para agregar un nuevo contacto |
| `Ctrl + S` | Guardar | Guarda el contacto actual (equivalente a AGREGAR) |
| `Ctrl + E` | Eliminar | Elimina el contacto seleccionado |
| `Clic Derecho` | Menú Contextual | Muestra opciones rápidas (Editar, Eliminar, Limpiar) |

**Consejo:** Los atajos de teclado aumentan significativamente la productividad al trabajar con muchos contactos.

---

## 5. SOLUCIÓN DE PROBLEMAS

### Problema: "Error al cargar contactos"

**Posibles causas:**
- El archivo CSV está corrupto
- No hay permisos de lectura en la carpeta

**Solución:**
1. Verificar que existe la carpeta `c:/gestionContactos/`
2. Verificar permisos de lectura/escritura
3. Si el problema persiste, eliminar el archivo CSV y la aplicación lo recreará

### Problema: "No se puede guardar el contacto"

**Posibles causas:**
- Campos vacíos en el formulario
- No se seleccionó una categoría válida
- No hay permisos de escritura

**Solución:**
1. Verificar que todos los campos estén llenos
2. Asegurarse de seleccionar una categoría (Familia, Amigos o Trabajo)
3. Verificar permisos de escritura en `c:/gestionContactos/`

### Problema: "La búsqueda no funciona correctamente"

**Solución:**
1. Asegurarse de escribir en el campo de búsqueda correcto (parte inferior)
2. La búsqueda es sensible a acentos
3. Probar borrando el texto y escribiendo nuevamente

### Problema: "La tabla no muestra los contactos"

**Solución:**
1. Reiniciar la aplicación
2. Verificar que el archivo CSV contiene datos
3. Revisar la pestaña de Estadísticas para confirmar que hay contactos

### Problema: "No puedo exportar a CSV"

**Solución:**
1. Verificar que hay contactos para exportar
2. Asegurarse de tener permisos de escritura en la carpeta destino
3. Cerrar el archivo CSV si está abierto en otra aplicación

---

## 6. PREGUNTAS FRECUENTES

### ¿Dónde se almacenan los contactos?

Los contactos se almacenan en el archivo CSV ubicado en:
```
c:/gestionContactos/datosContactos.csv
```

### ¿Puedo cambiar la ubicación del archivo?

Sí, pero requiere modificar el código en la clase `PersonaDAO.java`:
```java
archivo = new File("c:/gestionContactos"); // Cambiar esta ruta
```

### ¿Cuántos contactos puedo almacenar?

No hay límite definido, pero el rendimiento puede verse afectado con más de 10,000 contactos.

### ¿Puedo importar contactos desde otro archivo CSV?

Actualmente la aplicación no tiene función de importación directa, pero puedes:
1. Copiar el contenido de otro CSV
2. Pegarlo en el archivo `datosContactos.csv`
3. Reiniciar la aplicación

**Formato requerido:**
```
nombre;telefono;email;categoria;favorito
```

### ¿Qué pasa si elimino el archivo CSV accidentalmente?

La aplicación lo recreará automáticamente al iniciarse, pero perderás todos los contactos. Se recomienda hacer respaldos periódicos.

### ¿Puedo usar la aplicación en Linux o macOS?

Sí, pero debes cambiar la ruta del archivo en el código:
- **Linux/macOS:** `/home/usuario/gestionContactos/`
- **Windows:** `c:/gestionContactos/`

### ¿Cómo hago un respaldo de mis contactos?

**Opción 1: Exportar a CSV**
1. Usar el botón "EXPORTAR CSV"
2. Guardar en una ubicación segura

**Opción 2: Copiar el archivo**
1. Ir a `c:/gestionContactos/`
2. Copiar el archivo `datosContactos.csv`
3. Guardarlo en otra ubicación

### ¿Puedo tener múltiples listas de contactos?

Actualmente no, pero se puede implementar creando diferentes instancias con rutas distintas.

---

## 7. CONSEJOS Y MEJORES PRÁCTICAS

### Para Mayor Productividad

1. **Usa atajos de teclado** para operaciones frecuentes
2. **Ordena la tabla** por la columna que más uses (ej: nombre)
3. **Marca como favoritos** los contactos más importantes
4. **Usa categorías** consistentemente para mejor organización

### Para Seguridad de Datos

1. **Exporta regularmente** tus contactos a CSV
2. **Haz respaldos semanales** del archivo CSV
3. **No abras el CSV** con Excel mientras la aplicación está ejecutándose
4. **Verifica los datos** antes de eliminar un contacto

### Para Búsquedas Efectivas

1. Usa **palabras clave cortas** para búsquedas más rápidas
2. La búsqueda funciona en **todos los campos simultáneamente**
3. Puedes buscar por **parte del nombre, teléfono o email**
4. Borra el campo de búsqueda para ver todos los contactos

---

## 8. CARACTERÍSTICAS AVANZADAS

### Menú Contextual

El menú contextual (clic derecho) ofrece acceso rápido a:
- **Editar:** Carga los datos en el formulario
- **Eliminar:** Elimina el contacto seleccionado
- **Limpiar formulario:** Limpia todos los campos

### Indicador de Progreso

La barra de progreso aparece durante:
- Carga inicial de contactos
- Operaciones de lectura/escritura extensas

Esto evita que la aplicación parezca congelada durante operaciones largas.

### Ordenamiento Multi-nivel

Puedes ordenar por múltiples criterios:
1. Ordenar primero por una columna
2. Mantener `Shift` y hacer clic en otra columna
3. Se aplicará ordenamiento secundario

### Validación en Tiempo Real

La aplicación valida:
- ✅ Campos no vacíos
- ✅ Categoría seleccionada
- ✅ Formato básico de datos

---

## 9. GLOSARIO

- **CSV:** Comma-Separated Values (Valores Separados por Comas)
- **DAO:** Data Access Object (Objeto de Acceso a Datos)
- **MVC:** Model-View-Controller (Modelo-Vista-Controlador)
- **Favorito:** Contacto marcado como importante
- **Categoría:** Clasificación del contacto (Familia, Amigos, Trabajo)
- **JTable:** Componente de Java Swing para mostrar datos tabulares
- **JTabbedPane:** Componente de pestañas para organizar la interfaz

---

## 10. SOPORTE Y CONTACTO

### Reportar Errores

Si encuentras un error:
1. Anota los pasos para reproducirlo
2. Captura de pantalla (si es posible)
3. Mensaje de error completo
4. Contactar al desarrollador

### Solicitar Funcionalidades

Para solicitar nuevas funcionalidades:
- Describir claramente la funcionalidad deseada
- Explicar el caso de uso
- Proporcionar ejemplos si es posible

---

## 11. ACTUALIZACIONES Y VERSIONES

### Versión Actual: 2.0

**Nuevas características:**
- ✅ JTabbedPane con pestañas
- ✅ JTable con ordenamiento
- ✅ Barra de progreso
- ✅ Exportación a CSV
- ✅ Búsqueda en tiempo real
- ✅ Menú contextual
- ✅ Atajos de teclado
- ✅ Estadísticas automáticas

### Versión Anterior: 1.0

**Características originales:**
- Agregar, modificar y eliminar contactos
- Lista simple de contactos
- Almacenamiento en CSV
- Categorización básica

---

## 12. CASOS DE USO COMUNES

### Caso 1: Agregar Contacto Rápidamente

1. Presionar `Ctrl + N` para limpiar formulario
2. Llenar los datos
3. Seleccionar categoría
4. Presionar `Ctrl + S` para guardar

**Tiempo estimado:** 30 segundos

### Caso 2: Buscar y Editar un Contacto

1. Escribir el nombre en el campo de búsqueda
2. Seleccionar el contacto en la tabla
3. Modificar los datos necesarios
4. Hacer clic en MODIFICAR

**Tiempo estimado:** 1 minuto

### Caso 3: Exportar Contactos de una Categoría

1. Hacer clic en el encabezado "Categoría" para ordenar
2. Identificar visualmente los contactos deseados
3. Exportar todo a CSV
4. Abrir el CSV y filtrar manualmente en Excel

**Tiempo estimado:** 2 minutos

### Caso 4: Eliminar Múltiples Contactos

1. Buscar el primer contacto
2. Eliminar con `Ctrl + E`
3. Repetir para cada contacto
4. Verificar estadísticas actualizadas

**Tiempo estimado:** Variable según cantidad

---

## 13. SEGURIDAD Y PRIVACIDAD

### Almacenamiento Local

- Los datos se almacenan **únicamente en tu computadora**
- No hay conexión a internet ni sincronización en la nube
- **Tú tienes control total** sobre tus datos

### Recomendaciones de Seguridad

1. **No compartas** el archivo CSV con personas no autorizadas
2. **Encripta** la carpeta si contiene información sensible
3. **Haz respaldos** en dispositivos seguros
4. **Usa contraseñas** en tu sistema operativo

---

## 14. LIMITACIONES CONOCIDAS

### Limitaciones Actuales

- ❌ No soporta importación directa de CSV
- ❌ No tiene sincronización en la nube
- ❌ No permite adjuntar fotos a los contactos
- ❌ No soporta campos personalizados
- ❌ No tiene función de respaldo automático
- ❌ No valida formato de email o teléfono

### Mejoras Planificadas

- ⏳ Importación de CSV/Excel
- ⏳ Validación de formato de datos
- ⏳ Campos personalizables
- ⏳ Respaldo automático
- ⏳ Búsqueda avanzada con filtros
- ⏳ Integración con base de datos

---

## 15. CONCLUSIÓN

El Sistema de Gestión de Contactos Optimizado es una herramienta potente y fácil de usar para administrar información de contactos. Con sus múltiples funcionalidades, atajos de teclado y interfaz intuitiva, permite gestionar contactos de manera eficiente y productiva.

### Recursos Adicionales

- **Documentación de Java Swing:** https://docs.oracle.com/javase/tutorial/uiswing/
- **Tutorial de CSV:** https://en.wikipedia.org/wiki/Comma-separated_values
- **Patrón MVC:** https://en.wikipedia.org/wiki/Model–view–controller

---

**Última actualización:** Octubre 2025  
**Versión del documento:** 1.0  
**Desarrollado para:** Universidad Politécnica Salesiana  
**Asignatura:** Programación de Interfaces Gráficas

---

## NOTAS FINALES

Gracias por usar el Sistema de Gestión de Contactos. Para cualquier pregunta, sugerencia o reporte de errores, no dudes en contactar al equipo de desarrollo.

**¡Esperamos que esta herramienta facilite tu trabajo diario!** 
