# Accesibilidad

## Qué es?

Es la posibilidad de que un producto o servicio web pueda ser accedido o usado de manera sencilla y directa.

## Limitaciones

- Visuales: Baja visión - ceguera total
- Motrices: Dificultad a la hora de moverse:
- Auditivas: Deficiencias auditivas
- Cognitivas: Dificultades de aprendizaje y/o cognitivas.

## Accesibilidad WEB (WAI)

El estándar es W3C, donde podremos encontrar la documentación

> La accesibilidad está **legislada** por las autoridades, por ello es importante tenerla en cuenta a la hora de construir aplicaciones web

### Actividades

- Guías para la **calificación** desarrollando pautas
- Mejora las herramientas para la evaluación y reparación
- Campaña educativa y de concienciación, difundiendo la importancia de la accesibilidad
- Abre nuevos campos, en través de la investigación

### Niveles de Accesibilidad

- Prioridad 1: Se tienen que cumplir obligatoriamente, porque si no, cierto grupo de usuarios **no podrían acceder** a la información de la web
- Prioridad 2: El usuario tendrá dificultades a la hora de acceder a la información
- Prioridad 3: El usuario tendrá mínimas complicaciones a la hora de navegar por tu web

### Pautas

**WCAG** cuenta con 14 pautas que proporcionan soluciones de diseño para ser utilizadas como ejemplo ante situaciones realistas.

#### Versión 2.0

Fue un cambio sustancial en su filosofía, el más importante fue el enfoque en principios en vez de las técnicas. Además, fueron diseñadas para que la adecuación se pueda verificar de forma fiable. Estos principios son:

##### Perceptible

1. Proporcionar alternativas textuales para todo contenido _no textual_ y así se pueda convertir a otros formatos.
2. Alternativas para los medios tempo-dependientes, los _sliders_ por ejemplo.
3. Crear contenido que se pueda presentar de una forma más simple, sin perder estructura e información. Un ejemplo de ello son las _webs responsive_.
4. Facilitar a los usuarios ver y/u oír el contenido, incluyendo la separación entre el primer plano y el fondo. La semántica de HTML es un ejemplo, en especial el encabezado, ya que tiene que estar bien colocado.

##### Operable

1. Proporcionar acceso a toda la funcionalidad mediante el teclado, esto puede ser el uso de la tecla **Enter** a la hora de interactuar con tu web.
2. Proporcionar a los usuarios el tiempo suficiente para leer y usar el contenido.
3. No diseñar contenido de un modo que se sepa podría provocar espasmos o convulsiones, es por ello que la etiqueta `<blink>` se prohibió.
4. Proporcionar medios para ayudar a los usuarios a navegar dentro de la página, como puede ser la presencia de un menú, botones de retorno, etc.

##### Comprensible

1. Contenidos textuales legibles y comprensibles, el contraste entre color de texto y color de fondo es un ejemplo de ello.
2. Realizar que las páginas que conforman tu sitio aparezcan y operen de manera predecible, que cada elemento tenga lógica y una razón de ser. A veces la excesiva creatividad es contraproducente.
3. Ayudar a los usuarios a evitar y corregir errores, el _feedback_ al usuario es **importante**, en especial en la validación de formularios. UX toca también la validación en el front, y seguridad es la validación del back.

##### Robusto

1. Maximizar la compatibilidad con las aplicaciones de usuario actuales y futuras, incluyendo las ayudas técnicas.

### Beneficios

- Aumenta el número de potenciales visitantes.
- Incrementa la satisfacción de los usuarios.
- Disminuye los costes de desarrollo y mantenimiento
- Reduce el tiempo de carga de la web y la carga del servidor.

### Tecnologías inclusivas (assistive technologies)

Son componentes tecnológicos que fueron creados para proporcionar asistencia a la personas que cuentan con ciertas particularidades. Es por ello que tenemos que pensar que nuestro proyecto debe de ser **soportado** por alguno de los siguientes ejemplos a continuación:

- Screen readers
- Teclados alternativos
- Switches
- Scanning software

SEO es el parámetro que mide la sinergia que tiene nuestro proyecto con estas tecnologías.

### Elementos HTML de accesibilidad

- El <!DOCTYPE> (histórico)
- Identificar el idioma (<html lang="idioma_a_seleccionar">)
- Título significativo para tu página (<title>Tu título</title>)
- Utilizar HTML con una semántica válida
  - Encabezados y su orden dentro del documento
- Ayudas adicionales a la navegación (<nav>). Lo máximo en un nav puede ser 8 elementos, lo que se busca es ser ordenado con la información que desees gestionar. Existe el atributo **"rel"**, que nos ayuda a la hora de cargar el link donde esta inicializado.
  - Propósito de los enlaces (<a>)
  - Añadir títulos a los vínculos
- Presentar inicialmente el contenido principal (_above the fold_)
- Contraste de color
- Utilizar colores de manera segura en los vínculos y siempre que tengan un valor informativo
- Definir abreviaturas y acrónimos
- Que tu web sea **Responsive**
  - 'Saltar' de links
- Texto Alternativo (_alt_) en las imágenes. Podemos prescindir del _alt_ cuando la imagen es poco importante o decorativa.
  - Proveer texto equivalente para los mapas de imágenes/svg interactivos
- ¿No abrir ventanas nuevas?
- Marcar correctamente las cabeceras de las tablas (<th>). Recordar que la tabla solo se usa con datos tabulares
- Usar tamaños de fuentes relativos (rem, em) esto es para respetar los cambios de configuración del usuario.
  - Font Size al 200%
- Elementos de los formularios definidos correctamente
  - Formularios y sus relaciones: <label> -> <input>, mediante el atributo _for_
  - Placeholders como un extra
  - La importancia del _focus_, perceptible y no solo con colores (atributo _tabindex_, si le das un 0 no le agrega prioridad). Con respecto al color tenemos la propiedad _outline_ que no agrega pixeles a la página, por ende, no se moverán los elementos que están al lado del elemento donde colocaste el outline
  - Navegación a través del teclado.
  - Componentes complejos, establecen relaciones y otorgan un feedback.
  - Enlaces vs Botones. Los enlaces se usan para navegar, los botones para subir información, es por ello que sale una _manita_ a la hora de estar encima de un _link_
- Definir accesos directos desde el teclado
- ¿Evitar la dependencia de los scripts?
  - Progressive enhancement: La web son capas progresivas de funcionalidad
- Animaciones: uso y abuso

### Accesibilidad en CSS

- `prefers-reduced-motion`

  > 2️⃣0️⃣2️⃣0️⃣🔥🧨☀️😎 nueva _característica de medios_ que se utiliza para detectar si el usuario ha solicitado que el sistema minimice la cantidad de movimiento no esencial que utiliza.

  ```css
  @media (prefers-reduced-motion) {
    .animation {
      animation: none;
    }
  }
  ```

- `prefers-color-scheme`

  > 2️⃣0️⃣2️⃣0️⃣🔥🧨☀️😎 nueva _característica de medios_ que se utiliza para detectar si el usuario ha solicitado un tema de color claro u oscuro.

  ```css
  @media (prefers-color-scheme: dark) {
    .foo {
      background: #333;
      color: white;
    }
  }
  ```

- `prefers-reduced-data`

  > 2️⃣0️⃣2️⃣1️⃣🔥🧨☀️😎 nueva _característica de medios_ que se utiliza para detectar si el usuario ha solicitado contenido web que consuma menos tráfico de internet.

  ```css
  @media (prefers-reduced-data: reduce) {
    body {
      font-family: system-ui;
    }
  }
  ```

- `color-scheme`

  > 2️⃣0️⃣2️⃣1️⃣🔥🧨☀️😎 nueva _propiedad CSS_ que permite a un elemento indicar en qué esquemas de color puede renderizado cómodamente.

  ```css
  .html {
    color-scheme: light dark;
  }
  ```

- `prefers-contrast`

  > 2️⃣0️⃣2️⃣2️⃣🔥🧨☀️ nueva _característica de medios_ que se utiliza para detectar si el usuario ha solicitado contenido web que cumpla con ciertos niveles de contraste.

  ```css
  @media (prefers-contrast: more) {
    .contrast {
      outline: 2px solid black;
    }
  }
  ```

- `forced-colors`

  > 2️⃣0️⃣2️⃣2️⃣🔥🧨☀️ nueva _característica de medios_ que se utiliza para detectar si el usuario ha solicitado contenido web que cumpla con ciertos niveles de color.

  ```css
  @media (forced-colors: active) {
    .button {
      border: 2px green solid;
    }
  }
  ```

- `color-contrast()`

  > 2️⃣0️⃣2️⃣1️⃣🧨☀️😎 nueva _notación funcional_ que toma un valor de color y lo compara con una lista de otros valores de color, seleccionando el que tenga el mayor contraste de la lista.

- `:focus-visible`

  > 2️⃣0️⃣2️⃣2️⃣🔥🧨☀️ nueva _pseudo-clase_ que se aplica a un elemento que recibe el enfoque del teclado, pero solo si el enfoque no se realiza con un mouse u otro dispositivo de puntero.

  ```css
  .focus-visible-only:focus-visible {
    outline: 2px dashed darkorange;
  }
  ```

- `:focus-within`

  > _pseudo-clase_ que se aplica a un elemento que contiene un elemento que recibe el enfoque del teclado.

- `light-dark()`

  > 2️⃣0️⃣2️⃣4️⃣🔥 nueva _función de CSS_ que selecciona un valor de una lista de valores basándose en si el usuario ha solicitado un tema de color claro u oscuro.

  ```css
  code {
    color: light-dark(var(--light-code), var(--dark-code));
  }
  ```
