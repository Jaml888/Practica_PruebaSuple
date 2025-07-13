# Practica_PruebaSuple
Este es un repositorio para una prueba practica para mi prueba supletorio

# Universidad Tecnica de Ambato 
## Facultad de Sistemas, Electronica e Industrial 
### Carrera de Ingeniería en Software  

**Asignatura:** Manejo y Configuración de Software  
**Nombre del Estudiante:** Jaim Mariño 
**Fecha:** 12/7/2025

---

# Evaluación Práctica de Git y GitHub

## Instrucciones Generales

- Cada pregunta debe ser respondida directamente en este archivo **(README.md)** debajo del enunciado correspondiente.
- Cada respuesta debe ir acompañada de uno o más **commits**, según se indique en cada pregunta.
- Cuando se indique, deberán realizarse acciones prácticas dentro del repositorio (como creación de archivos, ramas, resolución de conflictos, etc.).
- Cada pregunta debe estar **etiquetada con un tag**, únicamente en el commit final correspondiente, con el formato: `"Pregunta 1"`, `"Pregunta 2"`, etc.

---

## Pregunta 1 (1 punto)

**Explicar la diferencia entre los siguientes conceptos/comandos en Git y GitHub:**

- `git clone`  
- `fork`  
- `git pull`

### Parte práctica:

- Realizar un **fork** de este repositorio en la cuenta personal de GitHub del estudiante.
- Luego, realizar un **clone** del fork en el equipo local.
- En este README, describir el proceso seguido:
  - ¿Cómo se realizó el fork?
  - ¿Cómo se realizó el clone del fork?
  - ¿Cómo se verificó que se estaba trabajando sobre el fork y no sobre el repositorio original?

**📝 Respuesta:**

### Diferencias entre `git clone`, `fork` y `git pull`:

#### `git clone`
- **Definición**: Es un comando de Git que permite crear una copia local completa de un repositorio remoto.
- **Propósito**: Descargar todo el historial de commits, ramas y archivos de un repositorio desde un servidor remoto (como GitHub) a tu máquina local.
- **Cuándo usar**: Cuando quieres trabajar con un repositorio existente en tu computadora local.
- **Ejemplo**: `git clone https://github.com/usuario/repositorio.git`

#### `fork`
- **Definición**: Es una funcionalidad específica de GitHub (y otras plataformas similares) que permite crear una copia independiente de un repositorio en tu cuenta personal.
- **Propósito**: Crear tu propia versión del repositorio original para poder hacer cambios sin afectar el proyecto original.
- **Cuándo usar**: Cuando quieres contribuir a un proyecto de código abierto o trabajar en tu propia versión de un proyecto.
- **Características**: 
  - El fork mantiene una conexión con el repositorio original
  - Puedes sincronizar tu fork con los cambios del repositorio original
  - Permite crear Pull Requests hacia el repositorio original

#### `git pull`
- **Definición**: Es un comando de Git que combina `git fetch` (descargar cambios) y `git merge` (integrar cambios).
- **Propósito**: Actualizar tu rama local con los cambios más recientes del repositorio remoto.
- **Cuándo usar**: Cuando quieres obtener y integrar los últimos cambios del repositorio remoto a tu rama local actual.
- **Ejemplo**: `git pull origin main`

### Relación entre los conceptos:
1. **Fork** → Crea una copia independiente del repositorio en tu cuenta de GitHub
2. **Clone** → Descarga el repositorio (original o fork) a tu máquina local
3. **Pull** → Mantiene tu repositorio local actualizado con los cambios del remoto

### Proceso práctico realizado:

#### ¿Cómo se realizó el fork?

1. **Acceso al repositorio original**: Se navegó al repositorio original en GitHub usando la URL proporcionada por el docente.
2. **Botón de Fork**: Se localizó y se hizo clic en el botón "Fork" ubicado en la esquina superior derecha de la página del repositorio.
3. **Selección de cuenta**: Se seleccionó la cuenta personal de GitHub donde se deseaba crear el fork.
4. **Confirmación**: Se confirmó la creación del fork, lo que generó una copia independiente del repositorio en la cuenta personal.
5. **Verificación**: Se verificó que el fork se creó correctamente navegando a la nueva URL del repositorio fork.

#### ¿Cómo se realizó el clone del fork?

1. **Obtención de la URL**: Se copió la URL del repositorio fork desde la barra de direcciones del navegador o desde el botón "Code" en GitHub.
2. **Comando de clonación**: Se ejecutó el comando `git clone` en la terminal:
   ```bash
   git clone https://github.com/mi-usuario/Practica_PruebaSuple.git
   ```
3. **Descarga del repositorio**: Git descargó automáticamente todos los archivos, historial de commits y ramas del fork.
4. **Navegación al directorio**: Se cambió al directorio del repositorio clonado:
   ```bash
   cd Practica_PruebaSuple
   ```

#### ¿Cómo se verificó que se estaba trabajando sobre el fork y no sobre el repositorio original?

1. **Verificación del origen remoto**: Se ejecutó el comando para verificar la URL del repositorio remoto:
   ```bash
   git remote -v
   ```
   La salida mostró que el origen apuntaba a la URL del fork personal, no al repositorio original.

2. **Verificación en GitHub**: Se navegó al repositorio en GitHub y se confirmó que la URL en la barra de direcciones correspondía al fork personal.

3. **Verificación del propietario**: Se verificó que el propietario del repositorio en GitHub era la cuenta personal, no la cuenta del docente o del repositorio original.

4. **Prueba de escritura**: Se realizó una pequeña modificación de prueba para confirmar que se tenían permisos de escritura en el fork.

**Resultado**: Se confirmó exitosamente que se estaba trabajando sobre el fork personal y no sobre el repositorio original, lo que permite realizar cambios de forma segura sin afectar el proyecto original.

---

## Pregunta 2 (1 punto)

**Configurar un archivo `.gitignore` para que ignore:**

- Todos los archivos con extensión `.log`.
- Una carpeta llamada `temp/`.

### Requisitos:

1. Realizar un **primer commit** que incluya únicamente el archivo `.gitignore` con las reglas de exclusión definidas.
2. Realizar un **segundo commit** donde se explique en este README la función del archivo `.gitignore` y se muestre evidencia de que los archivos y carpetas indicadas no están siendo rastreadas por Git.

**Importante:**  
- Solo el **segundo commit** debe llevar el **tag `"Pregunta 2"`**.

**📝 Respuesta:**

### Función del archivo `.gitignore`

El archivo `.gitignore` es un archivo de configuración especial que le dice a Git qué archivos y carpetas debe **ignorar** y no rastrear en el control de versiones. Esto es útil para excluir:

- **Archivos temporales** generados por el sistema o editores
- **Archivos de configuración local** que no deben compartirse
- **Archivos de compilación** y binarios
- **Archivos de logs** que pueden ser muy grandes
- **Carpetas de dependencias** que se pueden regenerar
- **Archivos sensibles** como contraseñas o claves

### Reglas configuradas en este proyecto:

```gitignore
# Ignorar todos los archivos con extensión .log
*.log

# Ignorar la carpeta llamada temp/ y todo su contenido
temp/
```

**Explicación de las reglas:**
- `*.log`: El asterisco es un comodín que coincide con cualquier nombre de archivo, y `.log` especifica la extensión. Esta regla ignora todos los archivos que terminen en `.log`.
- `temp/`: La barra al final indica que es una carpeta. Esta regla ignora toda la carpeta `temp` y todo su contenido, sin importar qué archivos contenga.

### Evidencia de que los archivos y carpetas no están siendo rastreadas por Git

Para demostrar que las reglas del `.gitignore` funcionan correctamente, se realizaron las siguientes pruebas:

#### 1. Creación de archivos de prueba

Se crearon archivos y carpetas que deberían ser ignorados:

```bash
# Crear archivos .log
echo "Este es un archivo de log" > archivo1.log
echo "Otro archivo de log" > debug.log

# Crear carpeta temp con archivos
mkdir temp
echo "Archivo temporal 1" > temp/archivo_temp1.txt
echo "Archivo temporal 2" > temp/archivo_temp2.txt
```

#### 2. Verificación del estado de Git

Al ejecutar `git status`, se puede observar que estos archivos **NO aparecen** en la lista de archivos no rastreados:

```bash
git status
```

**Resultado esperado:**
- Los archivos `archivo1.log`, `debug.log` y la carpeta `temp/` no aparecen en la salida de `git status`
- Solo se muestran los archivos que SÍ deben ser rastreados por Git

#### 3. Verificación con `git check-ignore`

Para confirmar que Git está aplicando correctamente las reglas, se puede usar:

```bash
git check-ignore archivo1.log
git check-ignore temp/archivo_temp1.txt
```

**Resultado:** Estos comandos devuelven el nombre del archivo, confirmando que están siendo ignorados.

#### 4. Verificación de archivos rastreados

Para contrastar, se creó un archivo que SÍ debe ser rastreado:

```bash
echo "Este archivo SÍ debe ser rastreado" > archivo_normal.txt
git status
```

**Resultado:** El archivo `archivo_normal.txt` SÍ aparece en la lista de archivos no rastreados, confirmando que Git funciona correctamente y solo ignora lo especificado en `.gitignore`.

### Beneficios de usar `.gitignore`

1. **Mantiene el repositorio limpio** al excluir archivos innecesarios
2. **Evita conflictos** al no incluir archivos de configuración personal
3. **Reduce el tamaño del repositorio** al no versionar archivos temporales
4. **Mejora la seguridad** al evitar subir accidentalmente archivos sensibles
5. **Facilita la colaboración** al mantener un estándar de archivos a versionar

---

## Pregunta 3 (2 puntos)

**Utilizar Git Flow para desarrollar una nueva funcionalidad llamada `ingresar-encabezado`.**

### Requisitos:

- Inicializar el repositorio con Git Flow, utilizando las ramas por defecto: `main` y `develop`.
- Crear una rama de tipo `feature` con el nombre `ingresar-encabezado`.
- En dicha rama, **completar con los datos personales del estudiante** el encabezado que ya se encuentra al inicio de este archivo `README.md`.
- Realizar al menos un commit durante el desarrollo.
- Finalizar la feature siguiendo el flujo de trabajo establecido por Git Flow.

### En este README, se debe incluir:

- Los **comandos exactos** utilizados desde la inicialización de Git Flow hasta el cierre de la feature.
- Una descripción del **proceso seguido**, indicando el propósito de cada paso.
- Una reflexión sobre las **ventajas de aplicar Git Flow**, especialmente en contextos colaborativos o proyectos de larga duración.

**Importante:**

- Deben realizarse varios commits durante esta pregunta.
- **Solo el commit final** debe llevar el **tag `"Pregunta 3"`**.
- El flujo debe respetar la estructura de Git Flow con las ramas `develop` y `main`.

**📝 Respuesta:**

### Comandos exactos utilizados desde la inicialización de Git Flow hasta el cierre de la feature:

#### 1. Verificación de la versión de Git Flow
```bash
git flow version
```
**Salida:** `1.12.3 (AVH Edition)`

#### 2. Inicialización de Git Flow
```bash
git flow init
```
**Configuración realizada:**
- Branch para producción: `main`
- Branch para desarrollo: `develop`
- Prefijos de ramas: `feature/`, `bugfix/`, `release/`, `hotfix/`, `support/`
- Prefijo de versiones: (vacío)
- Directorio de hooks: `C:/Users/User/Practica_PruebaSuple/.git/hooks`

#### 3. Verificación de las ramas creadas
```bash
git branch -a
```
**Salida:**
```
* develop
  main
  remotes/origin/HEAD -> origin/main
  remotes/origin/main
```

#### 4. Creación de la rama feature
```bash
git flow feature start ingresar-encabezado
```
**Salida:**
```
Switched to a new branch 'feature/ingresar-encabezado'

Summary of actions:
- A new branch 'feature/ingresar-encabezado' was created, based on 'develop'
- You are now on branch 'feature/ingresar-encabezado'

Now, start committing on your feature. When done, use:
     git flow feature finish ingresar-encabezado
```

#### 5. Verificación del estado de trabajo
```bash
git status
```
**Salida:**
```
On branch feature/ingresar-encabezado
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
```

#### 6. Agregar cambios al staging area
```bash
git add .
```

#### 7. Realizar commit con los datos personales
```bash
git commit -m "Datos Personales del estudiante"
```
**Salida:**
```
[feature/ingresar-encabezado 1c5333a] Datos Personales del estudiante
 1 file changed, 4 insertions(+), 4 deletions(-)
```

#### 8. Finalizar la feature
```bash
git flow feature finish ingresar-encabezado
```
**Salida:**
```
Switched to branch 'develop'
Updating 5434209..1c5333a
Fast-forward
 README.md | 8 ++++----
 1 file changed, 4 insertions(+), 4 deletions(-)
Deleted branch feature/ingresar-encabezado (was 1c5333a).

Summary of actions:
- The feature branch 'feature/ingresar-encabezado' was merged into 'develop'
- Feature branch 'feature/ingresar-encabezado' has been locally deleted
- You are now on branch 'develop'
```

#### 9. Verificación final del estado
```bash
git status
git log --oneline
```

### Descripción del proceso seguido:

#### **Fase 1: Inicialización**
- **Propósito**: Configurar Git Flow en el repositorio para establecer un flujo de trabajo estructurado
- **Acción**: Se inicializó Git Flow con las ramas por defecto `main` (producción) y `develop` (desarrollo)
- **Resultado**: Se creó automáticamente la rama `develop` a partir de `main`

#### **Fase 2: Creación de Feature**
- **Propósito**: Crear un entorno aislado para desarrollar la funcionalidad "ingresar-encabezado"
- **Acción**: Se creó la rama `feature/ingresar-encabezado` basada en `develop`
- **Resultado**: Se cambió automáticamente a la nueva rama de feature

#### **Fase 3: Desarrollo**
- **Propósito**: Completar los datos personales del estudiante en el encabezado del README.md
- **Acción**: Se modificó el archivo README.md con los datos:
  - Universidad: Universidad Técnica de Ambato
  - Facultad: Facultad de Sistemas, Electrónica e Industrial
  - Nombre: Jaim Mariño
  - Fecha: 12/7/2025
- **Resultado**: Se realizó un commit con los cambios

#### **Fase 4: Finalización**
- **Propósito**: Integrar la feature completada de vuelta a la rama de desarrollo
- **Acción**: Se ejecutó `git flow feature finish` que:
  - Fusionó la feature en `develop`
  - Eliminó la rama de feature local
  - Cambió de vuelta a la rama `develop`
- **Resultado**: Los cambios están ahora integrados en `develop` y listos para futuras releases

### Reflexión sobre las ventajas de aplicar Git Flow:

#### **En contextos colaborativos:**

1. **Separación clara de responsabilidades**:
   - `main`: Código en producción, siempre estable
   - `develop`: Código en desarrollo, integrando features
   - `feature/*`: Desarrollo aislado de funcionalidades específicas

2. **Prevención de conflictos**:
   - Cada desarrollador trabaja en su propia rama de feature
   - Los cambios se integran de forma controlada a través de `develop`
   - Se evita que cambios incompletos lleguen a producción

3. **Trazabilidad mejorada**:
   - Cada feature tiene su propia rama con commits específicos
   - Es fácil identificar qué cambios pertenecen a cada funcionalidad
   - Facilita la revisión de código y debugging

#### **En proyectos de larga duración:**

1. **Gestión de releases**:
   - Permite crear ramas `release/*` para preparar versiones
   - Facilita la corrección de bugs críticos con `hotfix/*`
   - Mantiene un historial limpio de versiones

2. **Escalabilidad**:
   - El flujo se mantiene consistente independientemente del tamaño del equipo
   - Permite trabajar en múltiples features simultáneamente
   - Facilita la integración continua

3. **Mantenimiento a largo plazo**:
   - Estructura clara para nuevos desarrolladores
   - Facilita la identificación de problemas en versiones específicas
   - Permite rollbacks controlados si es necesario

#### **Beneficios generales:**

- **Calidad del código**: El flujo estructurado promueve mejores prácticas
- **Documentación implícita**: La estructura de ramas documenta el proceso de desarrollo
- **Flexibilidad**: Permite adaptar el flujo según las necesidades del proyecto
- **Automatización**: Facilita la implementación de CI/CD pipelines

---

## Pregunta 4 (2 puntos)

**Trabajo con Issues y Pull Requests**

### Parte teórica:

- Explicar qué es un **issue** en GitHub.
- Explicar qué es un **pull request** y cuál es su finalidad.
- Indicar la diferencia entre ambos y cómo se relacionan en un entorno de trabajo colaborativo.

### Parte práctica:

- Trabajar en la rama `develop`, ya existente desde la configuración de Git Flow.
- Crear un **issue** titulado `"Respuesta a la Pregunta 4"`, en el que se indique que su objetivo es documentar esta pregunta.
- Realizar los cambios necesarios en este archivo `README.md` para responder esta pregunta.
- Realizar un **commit** con los cambios y subirlo a la rama `develop` del repositorio remoto.
- Crear un **pull request** desde `develop` hacia `develop` en GitHub.
- **Vincular el pull request con el issue creado**, de manera que al ser aprobado y fusionado, el issue se cierre automáticamente.
- El repositorio debe estar **configurado para requerir una revisión previa al merge**, la cual **debe ser aprobada por el docente**.

### En este README, se debe incluir:

- Un resumen del procedimiento realizado.
- El número del issue creado.
- El enlace al pull request.
- Una explicación de cómo se comprobó que el repositorio requería revisión antes de aceptar el pull request (por ejemplo, a través del mensaje mostrado por GitHub).

**📝 Respuesta:**

## Parte Teórica: Explicaciones Clave

### 1. ¿Qué es un Issue en GitHub?

Un **issue** (o incidencia) es una herramienta de seguimiento que se usa para registrar tareas, mejoras, ideas o errores (bugs) relacionados con un proyecto. Funciona como un foro de discusión para un tema específico.

**Características principales:**
- **No contiene código**. Es el lugar donde se discute qué se debe hacer o por qué algo no funciona.
- **Permite la colaboración**: El equipo puede comentar, asignar responsables y etiquetar los issues para organizar el trabajo.
- **Facilita el seguimiento**: Permite rastrear el progreso de tareas y problemas desde su identificación hasta su resolución.

**Ejemplos de uso:**
- "El botón de login no funciona en Firefox"
- "Sugerencia: Añadir un modo oscuro a la aplicación"
- "Bug: La aplicación se cuelga al cargar archivos grandes"
- "Mejora: Optimizar el tiempo de carga de la página principal"

### 2. ¿Qué es un Pull Request (PR) y cuál es su finalidad?

Un **pull request** (o solicitud de extracción) es una propuesta formal para fusionar (merge) una serie de commits desde una rama hacia otra (generalmente de una rama de feature a develop, o de develop a main).

**Finalidad principal:**
- **Revisión de código**: Es el momento en que le dices al equipo: "He terminado mi trabajo, aquí está el código. Por favor, revísenlo antes de que se integre al proyecto principal".
- **Contiene los cambios de código** y permite una discusión línea por línea sobre las modificaciones propuestas.
- **Permite la integración continua**: Se pueden ejecutar pruebas automáticas sobre el código del PR antes de fusionarlo.

**Características clave:**
- Muestra las diferencias (diffs) entre las ramas
- Permite comentarios específicos en líneas de código
- Facilita la revisión colaborativa
- Integra con sistemas de CI/CD para validaciones automáticas

### 3. Diferencia y Relación entre Issues y Pull Requests

| **Característica** | **Issue** | **Pull Request (PR)** |
|-------------------|-----------|----------------------|
| **Propósito** | Discutir y rastrear una tarea o problema. (El qué y el porqué). | Proponer y revisar una solución en código. (El cómo). |
| **Contenido** | Principalmente texto, imágenes, discusiones. | Commits, diferencias de código (diffs), discusiones sobre el código. |
| **Estado** | Se abre para iniciar una discusión. Se cierra cuando la tarea está resuelta. | Se abre para proponer cambios. Se cierra (fusiona) cuando el código es aprobado. |

### Relación entre Issues y Pull Requests

Se complementan perfectamente en un flujo de trabajo colaborativo:

1. **Se crea un Issue** para describir un problema (ej: "Issue #42: El logo se ve borroso").
2. **Un desarrollador crea una rama** para trabajar en ese problema.
3. **Una vez que tiene la solución**, abre un Pull Request y en la descripción escribe "Cierra el Issue #42" o "Soluciona #42".
4. **Al fusionar el Pull Request**, GitHub automáticamente cierra el Issue vinculado.

**Beneficios de esta relación:**
- **Trazabilidad completa**: Se puede seguir el ciclo completo desde la identificación del problema hasta su solución
- **Documentación automática**: Los issues cerrados automáticamente quedan documentados con su solución
- **Colaboración mejorada**: Facilita la comunicación entre desarrolladores y stakeholders
- **Gestión de proyectos**: Permite estimar tiempos y asignar recursos de manera más eficiente

### Parte Práctica:

<!-- Aquí se debe documentar el proceso práctico realizado -->

---

## Pregunta 5 (2 puntos)

**Resolver conflictos entre ramas y realizar un Pull Request controlado**

### Requisitos:

- Crear dos ramas llamadas `ramaA` y `ramaB`, ambas a partir de la rama `main`.
- En `ramaA`, crear un archivo llamado `archivoA.txt` con el contenido:  
  `Contenido A`
- En `ramaB`, crear un archivo con el mismo nombre (`archivoA.txt`), pero con el contenido:  
  `Contenido B`
- Intentar fusionar `ramaB` sobre `ramaA`, lo cual debe generar un conflicto.
- Resolver el conflicto combinando ambos contenidos (por ejemplo: `Contenido combinado A+B`).
- Realizar el merge de `ramaA` hacia `develop`.
- Crear un **pull request** desde `ramaA` hacia `develop`.
- El pull request debe estar **configurado para requerir revisión y ser aprobado por el docente**.
- Una vez completado el merge, eliminar las ramas `ramaA` y `ramaB` tanto local como remotamente.

### En este README, se debe incluir:

- El procedimiento completo:
  - Cómo se crearon las ramas.
  - Cómo se generó y resolvió el conflicto.
  - Cómo se realizó el merge hacia `develop`.
  - Cómo se creó y vinculó el pull request.
  - Cómo se verificó que la revisión fue requerida y aprobada.
  - Cómo se eliminaron las ramas al finalizar.
- El enlace al pull request.
- Una breve explicación de qué es un conflicto en Git y por qué ocurrió en este caso.

**📝 Respuesta:**

<!-- Escribe aquí tu respuesta completa a la Pregunta 5 -->

---

## Pregunta 6 (2 puntos)

**Realizar limpieza, explicar versionamiento semántico y enviar cambios al repositorio original**

### Requisitos:

- Trabajar en la rama `develop` del fork del repositorio.
- Eliminar los archivos `archivoA.txt` y `archivoB.txt` creados en preguntas anteriores.
- Realizar un merge desde `develop` hacia `main` en el repositorio local.
- Enviar los cambios de la rama `main` local a la rama `develop` del repositorio remoto (fork).
- Finalmente, crear un **pull request** desde la rama `develop` del fork hacia la rama `main` del repositorio original (del cual se realizó el fork en la Pregunta 1), en la descripción colocar el link de su repositorio de GitHub.

### En este README, se debe incluir:

- Una explicación del proceso realizado paso a paso.
- Una explicación del **versionamiento semántico**, indicando:
  - En qué consiste.
  - Sus tres componentes (MAJOR, MINOR, PATCH).
  - Ejemplos de aplicación en un proyecto real.
- El enlace al pull request creado hacia el repositorio original.
- Una reflexión sobre la importancia del versionamiento semántico y del uso de forks y pull requests en equipos de trabajo.

**📝 Respuesta:**

<!-- Escribe aquí tu respuesta completa a la Pregunta 6 -->
