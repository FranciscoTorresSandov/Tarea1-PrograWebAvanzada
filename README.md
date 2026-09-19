# Tarea 1 - Construcción de interfaces web adaptables con HTML y CSS

## Información del estudiante

- **Nombre:** Francisco Jose Torres Sandoval
- **Curso:** SOFT-12 - Programación Web Avanzada
- **Sección:** SCV2
- **Docente:** Álvaro Cordero Peña
- **Periodo:** III Cuatrimestre 2026
- **Fecha de entrega:** 2026-09-20

---

## Descripción general

Este repositorio contiene el desarrollo de la Tarea 1 del curso
Programación Web Avanzada.

El proyecto está compuesto por dos interfaces web independientes,
desarrolladas exclusivamente mediante HTML5 y CSS3.

El objetivo principal fue construir interfaces adaptables aplicando
HTML semántico, CSS Grid, Flexbox, modelo de caja, posicionamiento,
variables CSS, unidades relativas, accesibilidad básica y una estrategia
mobile-first.

No se utilizaron JavaScript, Bootstrap, Tailwind, frameworks CSS
ni plantillas externas.

Los dos casos fueron desarrollados como soluciones visualmente
diferentes, de acuerdo con el contexto y las necesidades particulares
de cada interfaz.

---

# Caso 1 - Centro de control de una expedición científica

## Descripción del problema

El Caso 1 representa un centro de control utilizado para supervisar
las operaciones de una expedición científica realizada en Monteverde,
Costa Rica.

La interfaz permite consultar rápidamente el estado general de la
expedición, las misiones científicas, los equipos de trabajo, las
alertas operativas y las próximas actividades.

## Contenido desarrollado

La interfaz incluye:

- Nombre y ubicación de la expedición.
- Día de operación y estado general.
- Navegación entre las principales secciones.
- Cuatro indicadores de resumen.
- Cinco misiones científicas.
- Cuatro equipos científicos.
- Cuatro alertas con diferentes niveles de importancia.
- Cinco próximas actividades organizadas cronológicamente.

Los equipos representados son:

- Biología.
- Hidrología.
- Meteorología.
- Geología.

Los estados de las misiones y alertas no dependen únicamente del color.
También se utilizan textos y símbolos para facilitar su identificación.

---

# Caso 2 - Panel público de información de un festival

## Descripción del problema

El Caso 2 representa un panel público de información para asistentes
al Festival Raíces y Cultura 2026.

A diferencia del primer caso, esta interfaz fue diseñada pensando
principalmente en usuarios que consultan información desde un teléfono
mientras se encuentran dentro del festival.

Por este motivo, la sección **Está ocurriendo ahora** posee una
jerarquía visual especialmente importante.

## Contenido desarrollado

La interfaz incluye:

- Nombre del festival.
- Fecha.
- Ubicación.
- Horario general.
- Navegación principal.
- Tres actividades que están ocurriendo actualmente.
- Seis próximas actividades.
- Programación de cuatro escenarios.
- Cuatro tipos de cambios importantes.
- Ocho servicios para los visitantes.
- Información general del evento.

Los escenarios incluidos son:

- Escenario Central.
- Teatro.
- Zona Cultural.
- Zona Familiar.

Los servicios disponibles incluyen:

- Alimentación.
- Baños.
- Primeros auxilios.
- Hidratación.
- Información.
- Accesibilidad.
- Estacionamiento.
- Objetos perdidos.

---

# Estructura del repositorio

```text
Tarea1/
├── README.md
│
├── caso1/
│   ├── index.html
│   ├── css/
│   │   └── estilos.css
│   └── img/
│       └── .gitkeep
│
└── caso2/
    ├── index.html
    ├── css/
    │   └── estilos.css
    └── img/
        └── .gitkeep
```

Los archivos `.gitkeep` permiten conservar las carpetas `img`
dentro del repositorio aunque actualmente los diseños no necesiten
imágenes.

Ambas hojas de estilo incluyen una regla general para que cualquier
imagen que se incorpore sea adaptable:

```css
img {
    display: block;
    max-width: 100%;
    height: auto;
}
```

De esta forma una imagen no supera el ancho de su contenedor y conserva
su proporción original.

---

# Instrucciones para abrir el proyecto

El proyecto no necesita instalación de dependencias ni un servidor
especial.

## Caso 1

Abrir directamente:

```text
caso1/index.html
```

## Caso 2

Abrir directamente:

```text
caso2/index.html
```

Los archivos pueden abrirse en un navegador moderno como:

- Google Chrome.
- Mozilla Firefox.
- Microsoft Edge.
- Safari.

Cada caso funciona de manera independiente.

---

# Decisiones de diseño y desarrollo

## 1. ¿Por qué se utilizaron etiquetas semánticas?

Se utilizaron etiquetas como:

```text
header
nav
main
section
article
aside
footer
```

porque permiten representar correctamente el significado y propósito
de las diferentes partes de cada página.

`header` contiene información introductoria.

`nav` representa los enlaces de navegación.

`main` identifica el contenido principal.

`section` agrupa contenido relacionado.

`article` se utiliza para componentes independientes como misiones,
actividades, escenarios, alertas y servicios.

`aside` se utiliza para información complementaria que necesita
especial atención.

En el Caso 1 se utiliza `aside` para las alertas.

En el Caso 2 se utiliza `aside` para los cambios importantes.

Esta estructura hace que el documento sea más comprensible para los
desarrolladores, navegadores y tecnologías de asistencia.

---

## 2. ¿Cómo se organizó la jerarquía de encabezados?

Cada página contiene un único `h1`.

En el Caso 1:

```text
Expedición Bosque Nuboso 2026
```

En el Caso 2:

```text
Festival Raíces y Cultura
```

Los elementos `h2` representan las principales secciones de la página.

Los elementos `h3` representan componentes dentro de esas secciones,
por ejemplo:

- Misiones.
- Equipos.
- Actividades.
- Alertas.
- Escenarios.
- Servicios.

La jerarquía se definió según el significado del contenido y no
únicamente por razones visuales.

---

## 3. ¿Qué decisiones de accesibilidad se implementaron?

Ambos documentos utilizan:

```html
<html lang="es">
```

También se agregó un enlace:

```text
Saltar al contenido principal
```

que permite a una persona que utiliza el teclado evitar recorrer toda
la navegación antes de llegar al contenido principal.

Los enlaces de navegación poseen estilos visibles mediante
`:focus-visible`.

Los estados tampoco dependen únicamente del color.

Por ejemplo, en el Caso 1 se utilizan elementos como:

```text
▶ Estado: En progreso
✓ Estado: Completada
◷ Estado: Pendiente
■ Estado: Suspendida
```

En el Caso 2 se utilizan textos explícitos como:

```text
● En este momento
Actividad trasladada
Cambio de horario
Actividad cancelada
Cambio de escenario
```

También se utilizaron elementos `time` para representar horarios
semánticamente.

---

## 4. ¿Cómo se aplicó el modelo de caja?

En ambos archivos CSS se utiliza:

```css
*,
*::before,
*::after {
    box-sizing: border-box;
}
```

La propiedad `border-box` permite que el `padding` y los bordes formen
parte del tamaño total del elemento.

Esto facilita el control de tarjetas, secciones y columnas y ayuda a
evitar problemas de desbordamiento.

---

## 5. ¿Dónde se utilizó position y por qué?

### Caso 1

Las tarjetas de misión utilizan:

```css
.tarjeta-mision {
    position: relative;
}
```

Las etiquetas de prioridad utilizan:

```css
.prioridad {
    position: absolute;
}
```

Esto permite colocar etiquetas como:

```text
Prioridad: Alta
Prioridad: Media
Prioridad: Crítica
```

en la parte superior de cada tarjeta.

La tarjeta funciona como contexto de posicionamiento, por lo que la
etiqueta permanece asociada únicamente a su misión.

`position` no se utilizó para construir el layout general.

### Caso 2

Las actividades que se están desarrollando utilizan:

```css
.actividad-actual {
    position: relative;
}
```

La etiqueta:

```text
● En este momento
```

utiliza:

```css
.actividad-pie {
    position: absolute;
}
```

Esto permite superponer visualmente la etiqueta dentro de la tarjeta
correspondiente.

El layout general continúa siendo responsabilidad de CSS Grid y
Flexbox.

---

## 6. ¿Cómo se controló la cascada y la especificidad?

Los estilos generales se definieron primero.

Posteriormente se utilizaron clases específicas para modificar
únicamente los componentes que lo requieren.

Por ejemplo:

```css
.alerta {
    /* estilos comunes */
}

.alerta-critica {
    /* variaciones de una alerta crítica */
}
```

Otro ejemplo es:

```css
.servicio {
    /* estilos comunes */
}

.servicio-prioritario {
    /* variación específica */
}
```

Esta estrategia permite reutilizar estilos y reducir duplicación.

No se utilizó:

```css
!important
```

porque la cascada y la especificidad se controlaron mediante clases
simples y reutilizables.

---

## 7. ¿Dónde se utilizó Flexbox y por qué?

Flexbox se utilizó principalmente para distribuciones
unidimensionales.

### Caso 1

Se utiliza para:

- Navegación.
- Datos operativos del encabezado.
- Indicadores.
- Encabezados de tarjetas.
- Estados.
- Equipos.
- Alertas.
- Agenda.

### Caso 2

Se utiliza para:

- Navegación.
- Datos generales del festival.
- Actividades que están ocurriendo.
- Próximas actividades.
- Encabezados de escenarios.
- Programación interna de escenarios.
- Cambios importantes.
- Encabezados de servicios.
- Pie de página.

Flexbox resulta apropiado cuando se necesita organizar elementos
principalmente en una fila o una columna.

---

## 8. ¿Dónde se utilizó CSS Grid y por qué?

CSS Grid se utilizó para estructuras que requieren controlar filas y
columnas simultáneamente.

### Caso 1

El elemento principal del centro de control utiliza CSS Grid.

Las áreas principales son:

```text
resumen
misiones
equipos
alertas
agenda
```

En teléfono se muestran en una sola columna.

En tableta se reorganizan en dos columnas.

En escritorio se utiliza una cuadrícula de doce columnas.

### Caso 2

CSS Grid se utiliza para:

- Layout general del festival.
- Programación por escenarios.
- Servicios.

Los cuatro escenarios pueden compararse simultáneamente en escritorio:

```text
Escenario Central | Teatro | Zona Cultural | Zona Familiar
```

Grid es apropiado para estas estructuras porque permite controlar
distribuciones bidimensionales.

---

## 9. ¿Qué cambia entre teléfono, tableta y escritorio?

### Caso 1

#### Teléfono

La interfaz utiliza principalmente una columna.

Las secciones aparecen en este orden:

```text
Resumen
Misiones
Alertas
Equipos
Agenda
```

Las alertas permanecen en una posición fácilmente localizable.

#### Tableta

La estructura se reorganiza aproximadamente así:

```text
Resumen
Misiones | Alertas
Equipos  | Agenda
```

#### Escritorio

Se utiliza una cuadrícula de doce columnas.

La distribución principal es:

```text
Resumen: 12 columnas

Misiones: 7 columnas
Alertas: 5 columnas

Equipos: 7 columnas
Agenda: 5 columnas
```

---

### Caso 2

#### Teléfono

La información se prioriza de esta manera:

```text
Ahora
Cambios importantes
Programación
Escenarios
Servicios
Información
```

Esto permite que un visitante vea primero qué está ocurriendo y si
existe alguna modificación importante.

#### Tableta

La interfaz comienza a utilizar dos columnas.

Los escenarios se presentan en una cuadrícula de:

```text
2 x 2
```

Los servicios también utilizan dos columnas.

#### Escritorio

La interfaz aprovecha una cuadrícula principal de doce columnas.

Las tres actividades actuales aparecen simultáneamente.

Programación y cambios importantes comparten una fila.

Los cuatro escenarios aparecen uno junto al otro:

```text
Central | Teatro | Cultural | Familiar
```

Los servicios se distribuyen cuatro por fila.

---

## 10. ¿Qué media queries y breakpoints se utilizaron?

El proyecto utiliza una estrategia **mobile-first**.

Los estilos iniciales corresponden a pantalla pequeña.

Posteriormente se utilizan media queries con `min-width`.

### Caso 1

Primer breakpoint:

```css
@media (min-width: 40rem)
```

Equivale aproximadamente a:

```text
640 px
```

En este punto existe espacio suficiente para comenzar a utilizar dos
columnas.

Segundo breakpoint:

```css
@media (min-width: 64rem)
```

Equivale aproximadamente a:

```text
1024 px
```

En este punto la interfaz puede convertirse en un dashboard de
escritorio con varias zonas simultáneas.

---

### Caso 2

Primer breakpoint:

```css
@media (min-width: 37.5625rem)
```

Equivale aproximadamente a:

```text
601 px
```

Se utiliza para comenzar la distribución correspondiente a tableta.

Segundo breakpoint:

```css
@media (min-width: 64rem)
```

Equivale aproximadamente a:

```text
1024 px
```

Se utiliza para la composición completa de escritorio.

También se implementa:

```css
@media (prefers-reduced-motion: reduce)
```

para respetar configuraciones del usuario relacionadas con reducción
de movimiento.

---

## 11. ¿Qué unidades relativas se utilizaron?

Se utilizaron principalmente:

```text
rem
%
fr
vw
```

Por ejemplo:

```css
width: 92%;
```

```css
gap: 1.5rem;
```

```css
grid-template-columns:
    repeat(12, minmax(0, 1fr));
```

También se utilizó `clamp()` para adaptar tamaños tipográficos:

```css
font-size:
    clamp(2rem, 6vw, 3.2rem);
```

Estas unidades permiten que la interfaz responda al espacio disponible
sin depender exclusivamente de tamaños fijos en píxeles.

---

## 12. ¿Cómo se utilizaron las variables CSS?

Ambos casos contienen variables definidas en:

```css
:root {
    /* variables */
}
```

Se utilizaron variables para:

- Colores principales.
- Colores de fondo.
- Colores de texto.
- Estados.
- Bordes.
- Espaciados.
- Radios.
- Sombras.
- Ancho máximo.

Ejemplo:

```css
:root {
    --color-primario: #502070;
    --color-fondo: #fff8f2;
    --color-texto: #2c2230;
    --espacio-md: 1rem;
    --radio-md: 0.9rem;
}
```

Esto facilita mantener una apariencia consistente y modificar valores
reutilizados desde un único lugar.

---

# Prevención de desbordamiento horizontal

No se utilizó:

```css
overflow-x: hidden;
```

como método para ocultar errores de maquetación.

En su lugar se utilizaron técnicas como:

```css
min-width: 0;
```

```css
minmax(0, 1fr);
```

```css
flex-wrap: wrap;
```

```css
overflow-wrap: anywhere;
```

```css
max-width: 100%;
```

El objetivo fue prevenir el desbordamiento desde la estructura del
layout en lugar de simplemente ocultarlo.

---

# Diferenciación visual de los casos

Los dos casos fueron diseñados de manera independiente y no representan
la misma plantilla con contenido diferente.

## Caso 1

Utiliza principalmente tonos verdes relacionados con un entorno
científico y natural.

Su estructura se comporta como un centro de mando que presenta varias
zonas de información operativa.

## Caso 2

Utiliza principalmente tonos morados, naranja y amarillo.

Su estructura se enfoca en la consulta rápida por parte de visitantes
de un festival, especialmente desde dispositivos móviles.

La sección **Ahora** posee una jerarquía visual especialmente fuerte.

---

# Historial de commits

La siguiente tabla fue construida utilizando el historial real de Git.

| # | Fecha | Hash | Mensaje | Caso | Cambio realizado |
|---:|---|---|---|---|---|
| 1 | 2026-09-17 | `7e1155d` | Creacion de estructura semantica inicial del centro de control | Caso 1 | Creación de la estructura HTML semántica inicial del centro de control. |
| 2 | 2026-09-17 | `14207b1` | Incorpora navegacion e indicadores del centro de control | Caso 1 | Incorporación de navegación e indicadores operativos. |
| 3 | 2026-09-17 | `0f75f58` | Agrega misiones y equipos cientificos | Caso 1 | Incorporación de las misiones y los cuatro equipos científicos. |
| 4 | 2026-09-17 | `2c63137` | Incorpora alertas y agenda de la expedicion | Caso 1 | Incorporación de alertas y agenda cronológica de actividades. |
| 5 | 2026-09-18 | `2eaa381` | Implementa Grid Flexbox y posicionamiento del caso 1 | Caso 1 | Implementación de CSS Grid, Flexbox y posicionamiento de las prioridades. |
| 6 | 2026-09-18 | `616ebe3` | Completa adaptabilidad y accesibilidad del caso 1 y cierre del mismo | Caso 1 | Implementación responsive, accesibilidad y cierre del Caso 1. |
| 7 | 2026-09-18 | `fc1876a` | Inicio de Caso 2 y Creacion de estructura mobile first del panel de festival | Caso 2 | Creación de la estructura inicial mobile-first y sección Ahora. |
| 8 | 2026-09-18 | `8b69709` | Agrega actividades y programacion por escenarios caso 2 | Caso 2 | Incorporación de próximas actividades y programación de escenarios. |
| 9 | 2026-09-19 | `12a86f7` | Incorpora cambios importantes y servicios del festival para el caso 2 | Caso 2 | Incorporación de cambios importantes y servicios para visitantes. |
| 10 | 2026-09-19 | `323c2d9` | Implementa Grid Flexbox y posicionamiento del caso 2 | Caso 2 | Implementación del Grid principal, Flexbox y posicionamiento en actividades actuales. |
| 11 | 2026-09-19 | `245c796` | Completa adaptabilidad y accesibilidad del caso 2 y conclusion del mismo | Caso 2 | Adaptación responsive, accesibilidad y cierre del Caso 2. |

El commit final corresponde a la creación de esta documentación y al
cierre de la entrega.

Debido a que el hash de un commit depende de su propio contenido, el
hash del commit que contiene este README se consulta directamente desde
el historial después de realizar el commit final.

---

# Distribución temporal del desarrollo

El historial demuestra trabajo realizado en diferentes días:

```text
2026-09-17
2026-09-18
2026-09-19
```

Por lo tanto, el desarrollo previo al cierre se encuentra distribuido
en tres días distintos.

El commit final de documentación se realiza posteriormente como cierre
formal de la entrega.

---

# Verificación del historial

Para consultar el historial con fecha, hash y mensaje:

```bash
git log --date=short --pretty=format:"| %ad | %h | %s |"
```

Para mostrar los commits desde el primero hasta el más reciente:

```bash
git log --reverse --date=short --pretty=format:"| %ad | %h | %s |"
```

---

# Estado final del proyecto

El proyecto contiene dos interfaces web independientes desarrolladas
exclusivamente mediante HTML5 y CSS3.

Ambos casos implementan:

- HTML semántico.
- Jerarquía correcta de encabezados.
- CSS Grid.
- Flexbox.
- Modelo de caja.
- Posicionamiento justificado.
- Variables CSS.
- Unidades relativas.
- Estrategia mobile-first.
- Media queries.
- Adaptación para teléfono, tableta y escritorio.
- Accesibilidad básica.
- Estados que no dependen únicamente del color.
- Prevención de desbordamiento horizontal.
- Organización visual diferenciada entre ambos casos.

El proyecto puede ejecutarse directamente desde los archivos
`index.html` de cada caso y queda preparado para su revisión desde el
repositorio público.