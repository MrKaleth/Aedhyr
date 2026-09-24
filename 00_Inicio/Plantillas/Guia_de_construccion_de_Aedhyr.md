# Guía de construcción de la bóveda de Aedhyr

> Manual de referencia para decidir **qué escribir, dónde escribirlo y cómo estructurarlo** dentro de la bóveda de Obsidian de Aedhyr.
>
> Esta guía está diseñada para trabajar de forma deliberada desde una estructura ya preparada: primero se decide **dónde vive una idea** y después se desarrolla el contenido.

---

# 0. Filosofía general de la bóveda

La bóveda no debe funcionar como una enciclopedia escrita de una sola vez. Debe funcionar como un **sistema de worldbuilding conectado**.

La estructura de carpetas responde principalmente a:

- **Qué clase de cosa es.**
- **Qué función cumple dentro del setting.**
- **Qué conjunto conceptual pertenece a qué área.**

Los enlaces de Obsidian responden a:

- con qué se relaciona una cosa;
- quién depende de ella;
- dónde apareció;
- qué la causó;
- quién la adora;
- quién la habita;
- qué acontecimientos la afectan.

Por tanto, la regla principal es:

> **Las carpetas organizan. Las notas explican. Los enlaces relacionan.**

No intentes resolver todas las relaciones del mundo mediante carpetas.

---

# 1. Regla fundamental: una entidad tiene un hogar principal

Cuando algo pueda convertirse en una entidad propia del mundo, debe tener un lugar principal dentro de la bóveda.

Ejemplos:

- una ciudad vive en `02_Atlas/Asentamientos/Ciudades/`;
- una deidad vive en `04_Mitología y Religión/Mitología/Divinidades/`;
- una criatura vive en `07_Bestiario/Tipos de Criaturas/...`;
- un personaje vive en `09_Personajes y Npcs/`;
- una facción vive en `08_Facciones y Organizaciones/`;
- un acontecimiento histórico vive en `03_Historia/`;
- un conjuro vive en `06_Magia/Conjuros/...`.

Después se relaciona con los demás elementos mediante enlaces.

### Ejemplo

Una ciudad pertenece a un reino y está habitada mayoritariamente por Qirathi.

La ciudad sigue viviendo en:

```text
02_Atlas/Asentamientos/Ciudades/Ciudad X.md
```

No hace falta colocarla físicamente dentro de la carpeta del reino ni dentro de Qirathi.

En la nota de la ciudad:

```markdown
Pertenece a [[Reino X]].

Su población está formada principalmente por [[Qirathi]].

En la ciudad tiene presencia [[Los Vaelirr]].
```

En la nota del reino:

```markdown
## Ciudades relevantes

- [[Ciudad X]]
```

La ubicación física del archivo y las relaciones narrativas son cosas distintas.

---

# 2. Regla de las notas con el mismo nombre que la carpeta

En esta bóveda, las notas que llevan el mismo nombre que una carpeta son **nodos de navegación (MOC)**.

Ejemplo:

```text
Atlas/
    Atlas.md
    Continentes/
        Continentes.md
```

`Atlas.md` no debe convertirse en una copia completa de todo el contenido de Atlas.

Debe servir como una puerta de entrada.

### Una nota nodo debe responder:

1. ¿Qué contiene esta sección?
2. ¿Qué conceptos son los más importantes?
3. ¿Dónde puedo seguir navegando?
4. ¿Qué relaciones generales debo conocer antes de entrar en detalles?

### Formato recomendado para un nodo

```markdown
# Atlas

> Mapa general de los lugares, regiones, territorios y accidentes geográficos de Aedhyr.

## Continentes
- [[Continentes]]

## Geografía
- [[Accidentes Geográficos]]

## Asentamientos
- [[Asentamientos]]

## Política territorial
- [[Reinos y Naciones]]

## Lugares especiales
- [[Lugares Especiales]]
```

El nodo debe ser **corto, navegable y útil**.

No necesita desarrollar todo el lore que enlaza.

---

# 3. Cómo decidir si algo merece una nota propia

Crea una nota independiente cuando el concepto:

- tenga nombre propio;
- tenga suficiente información para desarrollarse;
- tenga varias relaciones con otras partes del mundo;
- pueda crecer con el tiempo;
- sea algo que quieras encontrar directamente desde la búsqueda de Obsidian;
- o tenga importancia suficiente para aparecer enlazado desde varias páginas.

No hace falta crear una nota independiente para cada detalle mínimo.

### Ejemplo

Una ciudad llamada **Ael-Tar** merece una nota.

El nombre de una de sus plazas puede quedarse dentro de `Ael-Tar.md` mientras no tenga importancia propia.

Si después la plaza tiene historia, culto, conflicto, personajes asociados y acontecimientos propios, entonces puede convertirse en:

```text
Plaza del Alba.md
```

### Regla práctica

> **Una nota debe justificar su existencia por el contenido o por las relaciones que puede generar.**

---

# 4. Cómo escribir el contenido de Aedhyr

Aedhyr debe escribirse como un mundo ficticio coherente, no como una lista de datos aislados.

Siempre que sea posible, intenta que cada nota contenga cuatro capas:

### 4.1. Identidad

¿Qué es?

### 4.2. Descripción

¿Cómo es?

### 4.3. Contexto

¿Por qué existe o cómo llegó a ser así?

### 4.4. Relaciones

¿Qué otras cosas del mundo están conectadas con esto?

No todas las notas necesitan las cuatro capas con la misma profundidad, pero esta estructura mental ayuda mucho.

---

# 5. Estilo de escritura recomendado

## 5.1. Escribe de general a particular

Primero define el concepto y después sus detalles.

Malo:

> Tiene tres ceremonias anuales. Se utilizan campanas. La ceremonia principal dura seis horas. El sumo sacerdote lleva una capa azul.

Mejor:

> La festividad principal de los Qirathi es una celebración religiosa anual dedicada a X. Se caracteriza por ceremonias públicas, música ritual y la participación de las comunidades costeras.

> La ceremonia central dura aproximadamente seis horas y está dirigida por el sacerdote principal, que viste la capa tradicional azul.

Así primero sabemos **qué es**, y después **cómo funciona**.

## 5.2. No rellenes por rellenar

Una nota vacía no es un problema.

Una nota llena de texto genérico sí.

Es preferible:

```markdown
# Primera Era

## Estado

Pendiente de desarrollo.

## Ideas

- Origen de las primeras civilizaciones.
- Primer contacto con X.
- Desarrollo inicial de la magia.
```

que inventar diez párrafos sólo para que la nota parezca terminada.

## 5.3. Diferencia canon de ideas

Durante el worldbuilding vas a cambiar cosas.

Conviene distinguir mentalmente entre:

- **Canon:** decidido y válido dentro de Aedhyr.
- **Borrador:** idea suficientemente formada, pero todavía modificable.
- **Idea:** posibilidad que aún no forma parte del mundo.
- **Pendiente:** concepto que existe pero todavía necesita desarrollo.

Puedes usar propiedades si quieres:

```yaml
estado: canon
```

```yaml
estado: borrador
```

```yaml
estado: idea
```

No es obligatorio poner propiedades en todo desde el principio, pero sí es útil mantener una convención cuando la bóveda crezca.

---

# 6. Cómo usar los enlaces

Los enlaces son una de las partes más importantes de Aedhyr.

Cuando nombres algo que ya tenga una nota propia, enlázalo.

En lugar de:

```markdown
La ciudad pertenece al Reino de Aster.
```

usa:

```markdown
La ciudad pertenece al [[Reino de Aster]].
```

Esto permite que el grafo tenga valor real.

### Evita enlazar absolutamente cada palabra

No conviertas el texto en esto:

```markdown
Los [[Qirathi]] viven en [[Ciudades]] y practican la [[Religión]].
```

si `Ciudades` o `Religión` están siendo usadas sólo como conceptos genéricos.

Enlaza especialmente:

- nombres propios;
- conceptos propios de Aedhyr;
- instituciones;
- lugares;
- personas;
- criaturas;
- dioses;
- acontecimientos;
- términos que tengan una nota propia.

---

# 7. 00_Inicio

```text
00_Inicio/
├── Inicio.md
└── Plantillas/
    ├── Plantillas.md
    ├── Plantilla - Criatura.md
    ├── Plantilla - Deidad.md
    ├── Plantilla - Facción.md
    ├── Plantilla - Lugar.md
    └── Plantilla - Personaje.md
```

Esta sección no es lore. Es la **interfaz de trabajo de la bóveda**.

---

## 7.1. Inicio.md

Debe ser la página desde la que puedas entrar a prácticamente cualquier gran área de Aedhyr.

No debería contener un ensayo sobre el mundo.

Debe funcionar como portada.

### Contenido recomendado

```markdown
# Aedhyr

> Setting de fantasía para D&D.

## El mundo

- [[Astronomía y Tiempo]]
- [[Atlas]]
- [[Historia]]

## Cosmología y sociedad

- [[Mitología y Religión]]
- [[Cultura y Sociedad]]
- [[Magia]]

## Seres y poderes

- [[Bestiario]]
- [[Facciones y Organizaciones]]
- [[Personajes y NPCs]]

## Campañas

- [[Campañas]]

## Herramientas

- [[Plantillas]]
```

Puedes añadir una pequeña sección de “estado del mundo”, pero sin convertir `Inicio.md` en una página de lore general.

---

## 7.2. Plantillas/Plantillas.md

Debe explicar qué plantillas existen y cuándo utilizar cada una.

Ejemplo:

```markdown
# Plantillas

## Entidades
- [[Plantilla - Criatura]]
- [[Plantilla - Deidad]]
- [[Plantilla - Facción]]
- [[Plantilla - Lugar]]
- [[Plantilla - Personaje]]
```

Las plantillas no deben contener lore específico de Aedhyr salvo ejemplos claramente marcados como ejemplos.

---

# 8. 01_Astronomía y Tiempo

```text
01_Astronomía y Tiempo/
├── Astronomía/
└── Calendario/
```

Esta sección responde a:

> **¿Cómo funciona el cielo y cómo experimentan el paso del tiempo los habitantes de Aedhyr?**

No es sólo astronomía realista. Incluye también la forma cultural y práctica en que el mundo entiende el tiempo.

---

## 8.1. Astronomía y Tiempo.md

Es el nodo general.

Debe explicar brevemente:

- qué caracteriza al cielo de Aedhyr;
- qué elementos astronómicos existen;
- cómo se relacionan con el calendario;
- si la astronomía tiene importancia religiosa, mágica o cultural.

Enlaza a:

- [[Astronomía]];
- [[Calendario]].

---

## 8.2. Astronomía/Astronomía.md

Es el nodo de toda la estructura celeste.

Debe servir de mapa a:

- [[Las Estrellas]];
- [[Las Lunas]];
- [[Los Soles]].

También puede contener una explicación general del sistema astronómico.

Debe responder preguntas como:

- ¿Cuántos cuerpos celestes principales se reconocen?
- ¿Cómo se mueven?
- ¿Son entendidos igual por todas las culturas?
- ¿Tienen efectos físicos, mágicos o religiosos?
- ¿Qué fenómenos son importantes?

No repitas aquí las fichas completas de Oren, Riah, Ezkira, etc.

---

## 8.3. Las Estrellas/Las Estrellas.md

Nodo dedicado a las estrellas.

Aquí debes explicar el concepto general:

- constelaciones;
- nombres tradicionales;
- navegación;
- significado religioso;
- astrología, si existe;
- estrellas especiales;
- fenómenos relevantes.

Si una estrella concreta tiene suficiente importancia, crea una nota propia.

---

## 8.4. Las Lunas/Las Lunas.md

Esta nota presenta el sistema lunar completo.

Debe incluir, como mínimo:

- cuántas lunas existen;
- cómo se distinguen;
- ciclos generales;
- relación entre ellas;
- efectos sobre el mundo;
- interpretación cultural/religiosa;
- relación con el calendario.

Después enlaza a:

- [[Ezkira, la Luna Menor]];
- [[Lysuun, la Luna Mediana]];
- [[Naëthra, la Luna Mayor]].

---

## 8.5. Notas individuales de las lunas

Cada luna debe responder principalmente a:

- qué es;
- aspecto;
- tamaño relativo;
- órbita o comportamiento;
- ciclo;
- fenómenos;
- efectos sobre Aedhyr;
- importancia cultural;
- importancia religiosa;
- importancia mágica;
- nombres alternativos.

No inventes todos estos apartados si no aplican. La plantilla debe adaptarse al concepto.

---

## 8.6. Los Soles/Los Soles.md

Es la visión general del sistema solar de Aedhyr.

Debe explicar:

- cuántos soles existen;
- cómo se relacionan;
- cómo afecta su presencia al día y al clima;
- qué importancia tienen para el calendario;
- qué interpretación tienen dentro de la cosmología.

Después enlaza a Oren y Riah.

---

## 8.7. Notas individuales de los soles

Cada sol debe tratarse como una entidad astronómica propia.

Incluye lo relevante sobre:

- características;
- comportamiento;
- ciclo;
- posición;
- efectos físicos;
- simbología;
- mitología;
- influencia cultural.

---

## 8.8. Calendario/Calendario.md

Debe explicar **cómo mide el tiempo la civilización o civilizaciones de referencia de Aedhyr**.

Debe incluir, según corresponda:

- unidades de tiempo;
- días;
- semanas;
- meses;
- años;
- comienzo del año;
- relación con los ciclos astronómicos;
- sistemas de datación;
- festividades principales;
- diferencias regionales, si existen.

Si tienes un sistema de eras, enlázalo con [[Eras de Aedhyr]].

---

## 8.9. Las Estaciones/Las Estaciones.md

Debe explicar el sistema estacional como un todo.

Incluye:

- número de estaciones;
- orden;
- duración;
- condiciones generales;
- cambios ambientales;
- impacto social;
- impacto agrícola;
- festividades;
- relación con soles y lunas.

Las notas de `Invierno`, `Primavera`, `Verano`, `Otoño`, `Nebluvia` y `Ventoseco` deben explicar cada estación individualmente.

Importante: no asumas que “las estaciones” tienen que corresponder exactamente a las cuatro estaciones terrestres. En Aedhyr deben describir el sistema que hayas definido.

---

# 9. 02_Atlas

```text
02_Atlas/
├── Accidentes Geográficos/
├── Asentamientos/
├── Continentes/
├── Lugares Especiales/
└── Reinos y Naciones/
```

Esta sección responde a:

> **¿Dónde ocurren las cosas?**

El Atlas debe ser espacial, no histórico.

La historia de una ciudad puede aparecer en su nota, pero los acontecimientos importantes también deben enlazarse desde `03_Historia`.

---

## 9.1. Atlas.md

Debe ser el mapa general.

Enlaces principales:

```markdown
- [[Accidentes Geográficos]]
- [[Asentamientos]]
- [[Continentes]]
- [[Lugares Especiales]]
- [[Reinos y Naciones]]
```

Puede contener una descripción muy breve de la geografía global.

---

## 9.2. Accidentes Geográficos/Accidentes Geográficos.md

Nodo de toda la geografía física.

Debe explicar qué se considera accidente geográfico dentro del setting y enlazar a:

- [[Bosques]];
- [[Mares]];
- [[Montañas]];
- [[Océanos]];
- [[Ríos]].

---

## 9.3. Bosques, Mares, Montañas, Océanos y Ríos

Estas notas son **índices de categoría**, no listas enciclopédicas completas.

Por ejemplo, `Montañas.md` puede contener:

```markdown
# Montañas

## Cordilleras
- [[Cordillera X]]
- [[Cordillera Y]]

## Montañas destacadas
- [[Monte Z]]
```

Una cadena montañosa importante merece su propia nota si tiene identidad y relaciones suficientes.

---

## 9.4. Asentamientos/Asentamientos.md

Nodo general de asentamientos.

Enlaces a:

- [[Ciudades]];
- [[Fortalezas]];
- [[Pueblos]].

Debe explicar las principales categorías de asentamiento de Aedhyr y, si existe, qué las diferencia.

---

## 9.5. Ciudades, Fortalezas y Pueblos

Las notas de estas carpetas son índices por tipo.

Una ciudad concreta debe tener su propia nota dentro de `Ciudades`.

### Una ficha de ciudad debería responder

- ¿Dónde está?
- ¿Quién la fundó?
- ¿A qué reino o territorio pertenece?
- ¿Quién la gobierna?
- ¿Cuánta población tiene aproximadamente?
- ¿Qué pueblos viven allí?
- ¿Qué recursos tiene?
- ¿Qué lugares importantes contiene?
- ¿Qué facciones tienen presencia?
- ¿Qué conflictos existen?
- ¿Qué importancia histórica tiene?
- ¿Qué rumores o secretos puede conocer un aventurero?

No conviertas una ciudad en una lista de nombres. Dale una identidad.

---

## 9.6. Continentes/Continentes.md

Debe explicar el mapa continental de Aedhyr y enlazar a los cinco continentes que ya existen en la estructura:

- [[Continente Central]];
- [[Continente Este]];
- [[Continente Norte]];
- [[Continente Oeste]];
- [[Continente Sur]].

---

## 9.7. Notas individuales de cada continente

No tienen que ser completamente geográficas.

Deben dar una visión panorámica:

- posición;
- tamaño aproximado;
- grandes regiones;
- clima;
- pueblos predominantes;
- reinos importantes;
- grandes rasgos geográficos;
- historia resumida;
- características culturales;
- peligros relevantes.

La nota del continente es una vista de conjunto. Las regiones, reinos y ciudades se explican en sus respectivas notas.

---

## 9.8. Reinos y Naciones/Reinos y Naciones.md

Nodo general de la geopolítica.

Debe explicar:

- qué entidades se consideran reinos, naciones, imperios, ciudades-estado, etc.;
- cómo se organiza políticamente Aedhyr;
- cuáles son los territorios relevantes.

Cada reino importante debe tener su propia nota.

### Ficha de un reino/nación

Puede incluir:

- nombre;
- capital;
- territorio;
- régimen;
- gobernante;
- población;
- pueblos predominantes;
- economía;
- ejército;
- religión;
- relaciones diplomáticas;
- aliados y enemigos;
- conflictos internos;
- historia;
- símbolos;
- ciudades relevantes.

---

## 9.9. Lugares Especiales/Lugares Especiales.md

Es la categoría para lugares que no encajan naturalmente como ciudad, pueblo, fortaleza, continente o accidente geográfico convencional.

Ejemplos posibles:

- ruinas;
- monumentos;
- estructuras imposibles;
- templos aislados;
- lugares malditos;
- puertas;
- enclaves sobrenaturales;
- lugares únicos.

No debe convertirse en “todo lo que no sé dónde meter”.

Si algo merece una categoría propia y esa categoría se vuelve importante, entonces la estructura podrá evolucionar.

---

# 10. 03_Historia

```text
03_Historia/
├── Cronología/
│   └── Eras de Aedhyr/
└── Grandes Eventos/
```

Esta sección responde a:

> **¿Qué ocurrió y cuándo?**

La historia debe narrar cambios en el mundo.

---

## 10.1. Historia.md

Debe ser una introducción a la historia general de Aedhyr.

Puede incluir:

- grandes periodos;
- resumen de la evolución del mundo;
- principales puntos de ruptura;
- enlaces a la cronología;
- enlaces a grandes eventos.

No debería convertirse en una copia detallada de todas las eras.

---

## 10.2. Cronología/Cronología.md

Es la puerta de entrada temporal.

Debe explicar cómo se ordena la historia.

Por ejemplo:

```markdown
# Cronología

## Eras
- [[Eras de Aedhyr]]

## Grandes acontecimientos
- [[Gran Evento X]]
- [[Gran Evento Y]]
```

Si el mundo utiliza diferentes calendarios o sistemas de datación, este es también un buen lugar para explicar cómo se relacionan.

---

## 10.3. Eras de Aedhyr/Eras de Aedhyr.md

Debe explicar qué son las eras y qué criterio define el comienzo y final de cada una.

Enlaza a:

- [[Era Prehistórica]];
- [[Primera Era]];
- [[Segunda Era]];
- [[Tercera Era]];
- [[Cuarta Era]];
- [[Quinta Era]].

### Importante

Cada Era debe ser tratada como un **periodo histórico**, no sólo como una página con una fecha.

Una nota de era puede incluir:

- duración;
- evento que la inicia;
- evento que la termina;
- civilizaciones dominantes;
- acontecimientos principales;
- transformaciones mágicas;
- cambios religiosos;
- cambios geográficos;
- legado.

---

## 10.4. Era Prehistórica y las cinco Eras

La estructura permite que cada era tenga contenido propio.

La nota de una era debe ser un resumen histórico amplio.

Los acontecimientos concretos deben vivir en `Grandes Eventos` cuando tengan entidad suficiente.

### Ejemplo

En `Primera Era.md`:

```markdown
Durante la Primera Era surgieron las primeras grandes civilizaciones de Aedhyr...

## Acontecimientos
- [[La Guerra X]]
- [[La Fundación de Y]]

## Figuras relevantes
- [[Personaje X]]

## Lugares relevantes
- [[Ciudad Y]]
```

Así la nota de la era se convierte en un centro de navegación temporal.

---

## 10.5. Grandes Eventos/Grandes Eventos.md

Debe ser el índice de acontecimientos que hayan cambiado el mundo o tengan peso suficiente para merecer una nota propia.

Un gran evento puede ser:

- una guerra;
- una catástrofe;
- una revolución;
- una fundación;
- una caída de civilización;
- una gran batalla;
- una transformación mágica;
- un acontecimiento cósmico.

### Ficha de evento

```markdown
# Nombre del evento

## Resumen

## Fecha / Era

## Lugar

## Actores

## Qué ocurrió

## Consecuencias

## Relación con otros acontecimientos

## Enlaces
```

La parte más importante de un evento no es la anécdota: son **sus consecuencias**.

---

# 11. 04_Mitología y Religión

```text
04_Mitología y Religión/
├── Mitología/
└── Religión/
```

Esta división debe mantenerse muy clara.

## Mitología

Responde:

> ¿Qué cuentan los mitos que ocurrió? ¿Qué entidades existen? ¿Cómo se entiende el cosmos?

## Religión

Responde:

> ¿Cómo viven, interpretan y practican esas creencias los mortales?

Un mito puede existir aunque nadie lo siga como religión.

Una religión puede interpretar un mismo mito de una manera distinta a otra.

---

# 12. Mitología

## 12.1. Mitología/Mitología.md

Nodo general.

Debe explicar:

- qué entiende el mundo por mitología;
- cómo se organiza la cosmología;
- qué grandes grupos de entidades existen;
- cuáles son los principales relatos.

Enlaza a:

- [[Divinidades]];
- [[Los Dominios]];
- [[Mitos y Leyendas]].

---

## 12.2. Divinidades/Divinidades.md

Es el nodo general del panteón.

Debe explicar la estructura del sistema divino y enlazar a:

- [[Las Tres Entidades]];
- [[Primera Generación de Dioses]];
- [[Segunda Generación de Dioses]].

No debe contener una ficha completa de todos los dioses. Su función principal es dar contexto y navegar.

---

## 12.3. Las Tres Entidades

Debe explicar qué hace especial a este grupo.

`Las Tres Entidades.md` puede contener:

- explicación del grupo;
- relaciones entre ellas;
- posición cosmológica;
- importancia en el origen del universo;
- enlaces a sus tres fichas individuales.

---

## 12.4. Notas de Omhyr, Ori y Ridah

Cada entidad debe tener una ficha individual.

Puede incluir:

- identidad;
- naturaleza;
- títulos;
- aspecto;
- funciones;
- relación con otras entidades;
- papel en la creación;
- símbolos;
- culto o interpretación mortal;
- mitos relacionados;
- dominios, si aplica;
- lugares o fenómenos asociados.

No confundas la entidad con las doctrinas que las religiones mortales han construido sobre ella.

---

## 12.5. Primera Generación de Dioses

`Primera Generación de Dioses.md` debe explicar qué caracteriza a esta generación como grupo.

Las fichas individuales —Ezkadra, Lyssba, Naëmer, etc.— deben desarrollar a cada dios.

`La Tríada.md` puede funcionar como una nota específica de relación entre los miembros de esa estructura.

---

## 12.6. Segunda Generación de Dioses

`Segunda Generación de Dioses.md` es el nodo de la generación.

`Los 12 Patrones.md` debe explicar el conjunto de los doce dioses como estructura.

Las doce divinidades —Corvion, Dovharen, Eiran, Eshari, Haldris, Kaëlion, Lethari, Malvior, Thyria, Vaëlor, Ysvarel y Zailyn— deben tener fichas individuales.

### Ficha de una deidad

Recomendación de estructura:

```markdown
# Nombre de la deidad

## Identidad

## Títulos y epítetos

## Naturaleza

## Aspecto / representación

## Dominios

## Símbolos

## Personalidad o carácter mítico

## Relaciones

## Mitos principales

## Culto entre los mortales

## Ritos y festividades

## Templos / lugares asociados

## Seguidores

## Interpretaciones y variantes

## Enlaces relacionados
```

No todos estos apartados necesitan existir desde el primer día.

---

# 13. Los Dominios

Esta categoría debe explicar exactamente qué significa “Dominio” dentro de Aedhyr.

No asumas que necesariamente significa “dominio de una deidad” al estilo tradicional de D&D.

Primero define el concepto.

Puede tratarse de:

- ámbitos metafísicos;
- territorios divinos;
- conceptos cosmológicos;
- planos;
- regiones espirituales;
- u otra cosa propia del setting.

La nota `Los Dominios.md` debe ser el índice de esa estructura.

Si un Dominio concreto tiene identidad suficiente, tendrá su propia nota.

---

# 14. Mitos y Leyendas

`Mitos y Leyendas.md` debe ser el nodo de los relatos míticos del mundo.

Aquí conviene distinguir:

- hechos históricos conocidos;
- relatos míticos;
- versiones religiosas;
- leyendas populares;
- cuentos tradicionales.

Un mismo acontecimiento puede tener una nota histórica y, aparte, una interpretación legendaria.

---

## 14.1. El Origen.md

Debe contener el relato del origen del universo tal como está definido en Aedhyr.

No es necesario que el lector pueda determinar inmediatamente qué partes son “objetivamente ciertas” dentro del mundo.

Puedes escribir:

- versión mítica;
- versiones contradictorias;
- elementos conocidos;
- interpretaciones posteriores;
- secretos que sólo conoce el DM, si quieres introducirlos.

Es importante distinguir entre:

> lo que realmente ocurrió;

> lo que los habitantes creen que ocurrió.

Esa diferencia puede ser una fuente enorme de profundidad para Aedhyr.

---

# 15. Religión

`Religión.md` debe explicar la religión como fenómeno social y espiritual.

No debe repetir la cosmología completa.

Debe enlazar a:

- [[Cultos y Sectas]];
- [[Iglesias y Órdenes Mayores]];
- [[Ritos y Liturgia]];
- [[Teología y Dogma]];
- [[Textos Sagrados]].

---

## 15.1. Cultos y Sectas

Aquí van grupos religiosos que no funcionen como las grandes instituciones religiosas.

Puede incluir:

- cultos secretos;
- movimientos religiosos;
- sectas;
- ramas heréticas;
- congregaciones marginales.

Una organización concreta que tenga peso suficiente puede tener su propia nota.

---

## 15.2. Iglesias y Órdenes Mayores

Aquí van instituciones religiosas grandes o establecidas.

Una nota de una iglesia/orden debe explicar:

- deidad o principio al que sirve;
- origen;
- estructura;
- autoridad;
- dogmas;
- ritos;
- símbolos;
- distribución geográfica;
- influencia política;
- relación con otras religiones.

---

## 15.3. Ritos y Liturgia

Describe **qué hace una religión**.

Incluye:

- plegarias;
- ceremonias;
- iniciaciones;
- funerales;
- bodas;
- sacrificios;
- peregrinaciones;
- festividades;
- objetos rituales.

Una práctica exclusiva de una religión concreta puede enlazarse desde esta sección o mantenerse en la ficha de la propia religión dependiendo de su importancia.

---

## 15.4. Teología y Dogma

Explica lo que una religión **afirma que es verdad**.

Ejemplos:

- naturaleza de los dioses;
- creación;
- muerte;
- alma;
- pecado;
- destino;
- magia;
- vida después de la muerte;
- relación entre dioses y mortales.

Aquí es especialmente importante distinguir doctrina de hechos reales de Aedhyr.

---

## 15.5. Textos Sagrados

Debe funcionar como índice de los textos reconocidos como sagrados.

`Los Libros de Lin-Tan.md` debe explicar el conjunto de obras, no convertirse necesariamente en el texto íntegro de cada libro.

`La Leyenda de Ori.md` puede ser un texto concreto, relato concreto o parte concreta del corpus.

Si escribes literatura diegética completa, puedes tratarla como documento dentro del mundo, pero conviene indicar claramente quién la escribió, cuándo y qué estatus tiene.

---

# 16. 05_Cultura y Sociedad

```text
05_Cultura y Sociedad/
├── Arte y Saber/
├── Lenguas y Terminología/
├── Pueblos y Culturas/
├── Razas Inteligentes/
└── Vida Cotidiana/
```

Esta sección responde a:

> **¿Cómo viven, piensan, hablan y se organizan las sociedades de Aedhyr?**

---

# 17. Arte y Saber

`Arte y Saber.md` es el nodo del conocimiento cultural.

Enlaces:

- [[Literatura]];
- [[Crónicas y Tratados]];
- [[Poesía y Teatro]].

---

## 17.1. Literatura.md

Debe explicar la literatura como fenómeno cultural.

Puede incluir:

- géneros;
- autores famosos;
- obras importantes;
- tradiciones literarias;
- censura;
- alfabetización;
- regiones con tradiciones distintivas.

Una obra concreta que tenga relevancia puede tener su propia nota.

---

## 17.2. Crónicas y Tratados

Esta carpeta puede albergar documentos históricos, científicos, filosóficos o jurídicos escritos dentro del mundo.

Cada documento importante debería responder:

- autor;
- fecha;
- lugar;
- propósito;
- tema;
- destinatarios;
- estado de conservación;
- fiabilidad;
- relevancia histórica.

La fiabilidad es importante: un tratado puede estar equivocado.

---

## 17.3. Poesía y Teatro

Contiene tradiciones escénicas y poéticas.

Incluye:

- formas poéticas;
- tradiciones teatrales;
- compañías;
- autores;
- obras importantes;
- estilos regionales;
- relación con religión o política.

---

# 18. Lenguas y Terminología

```text
Lenguas y Terminología/
├── Glosario.md
├── Idiomas del Mundo.md
├── Lenguas y Terminología.md
└── Unidades de Medida.md
```

## Lenguas y Terminología.md

Es el nodo.

Debe enlazar a:

- [[Idiomas del Mundo]];
- [[Glosario]];
- [[Unidades de Medida]].

## Idiomas del Mundo.md

Debe presentar los idiomas existentes.

Puede incluir:

- familias lingüísticas;
- idiomas principales;
- escritura;
- distribución geográfica;
- dialectos;
- préstamos lingüísticos;
- relación entre idiomas;
- lenguas muertas;
- lenguas secretas o rituales.

Una lengua importante puede tener su propia nota si necesita desarrollo.

## Glosario.md

Es la referencia de términos propios del setting.

Puede incluir palabras, conceptos o expresiones que el lector necesita comprender.

No debe duplicar páginas completas de lore.

## Unidades de Medida.md

Explica las unidades utilizadas en Aedhyr.

Puede contener:

- distancia;
- peso;
- volumen;
- tiempo cuando no corresponda al calendario;
- monedas, si son unidades de valor y no un sistema económico completo.

Siempre que haya medidas alternativas por cultura o región, enlázalas.

---

# 19. Pueblos y Culturas

`Pueblos y Culturas.md` debe ser el nodo de grupos culturales y sociales que no tengan por qué equivaler a una raza.

Esta distinción es importante.

Una raza puede tener muchas culturas.

Una cultura puede contener miembros de varias razas.

### Una nota de pueblo/cultura puede incluir

- origen;
- región;
- población;
- valores;
- costumbres;
- estructura social;
- relaciones con otras culturas;
- lengua;
- religión predominante;
- vestimenta;
- alimentación;
- tradiciones;
- arte;
- tabúes;
- conflictos.

---

# 20. Razas Inteligentes

```text
Razas Inteligentes/
├── Razas/
│   └── Qirathi/
│       └── Subrazas/
└── Razas Inteligentes.md
```

Esta sección se centra en qué es una raza o especie inteligente dentro de Aedhyr.

No utilices esta sección para describir toda la cultura de un pueblo concreto.

---

## 20.1. Razas Inteligentes.md

Debe explicar qué significa “raza inteligente” en Aedhyr y cuáles son las categorías generales.

Puede incluir:

- qué rasgos definen una raza;
- diferencias respecto a pueblos o culturas;
- historia general de las especies inteligentes;
- conceptos de origen.

---

## 20.2. Razas/Razas.md

Es el índice de todas las razas.

Debe enlazar a cada raza importante.

No es una página completa sobre cada una.

---

## 20.3. Qirathi/Qirathi.md

Debe ser la ficha general de los Qirathi.

Recomendación:

```markdown
# Qirathi

## Resumen

## Origen

## Naturaleza / biología

## Apariencia

## Longevidad

## Capacidades naturales

## Distribución

## Subrazas

- [[Qirathi Abisales]]
- [[Qirathi de Agua Dulce]]
- [[Qirathi Oceánicos]]

## Sociedad

## Costumbres

## Idioma

## Religión

## Relaciones con otros pueblos

## Cultura
```

Si `Sociedad Qirathi`, `Costumbres Qirathi` o `Idioma Qirathi` necesitan páginas propias, puedes crearlas dentro de esta misma carpeta cuando exista suficiente contenido. No hace falta separar desde el principio cada apartado de la ficha.

---

## 20.4. Subrazas

Cada subraza debe explicar principalmente qué la diferencia del tronco Qirathi.

No repitas toda la ficha de Qirathi.

Incluye:

- origen;
- características físicas;
- capacidades;
- hábitat;
- diferencias culturales, si las hay;
- relaciones con otras subrazas;
- distribución.

---

# 21. Vida Cotidiana

Esta carpeta responde a:

> **¿Cómo es vivir un día normal en Aedhyr?**

`Vida Cotidiana.md` debe funcionar como índice y visión general.

---

## 21.1. Comida.md

Incluye:

- alimentos habituales;
- platos regionales;
- métodos de conservación;
- bebidas;
- tabúes alimentarios;
- comida de lujo;
- comida de viaje;
- ingredientes ligados a magia o religión.

---

## 21.2. Jerga y Expresiones.md

Aquí pueden ir:

- insultos;
- frases hechas;
- expresiones comunes;
- saludos;
- juramentos;
- proverbios;
- expresiones regionales.

Cuando una expresión tenga una historia importante, puede enlazar a su origen histórico, cultural o religioso.

---

## 21.3. Sistemas Monetarios.md

Debe explicar:

- monedas;
- equivalencias;
- materiales;
- valor aproximado;
- acuñación;
- regiones;
- monedas históricas;
- trueque u otros sistemas.

No hace falta construir una economía completa si no la necesitas para el juego.

---

## 21.4. Títulos y Rangos.md

Aquí van:

- títulos nobiliarios;
- rangos militares;
- cargos religiosos;
- cargos políticos;
- formas de tratamiento;
- jerarquías relevantes.

No conviertas esto en una lista sin contexto: explica qué significa cada rango.

---

## 21.5. Vestimenta.md

Incluye:

- ropa cotidiana;
- ropa regional;
- ropa ceremonial;
- materiales;
- símbolos;
- diferencias de clase;
- ropa militar o religiosa.

---

# 22. 06_Magia

```text
06_Magia/
├── Conjuros/
├── Escuelas y Tradiciones/
├── Grimorios y Tomos/
├── Leyes de la Magia/
└── Objetos Mágicos/
```

Esta estructura se conserva como parte importante del sistema de Aedhyr.

La magia debe tratarse como un sistema del mundo, no sólo como una lista de efectos de juego.

---

# 23. Magia.md

Debe explicar:

- qué es la magia;
- de dónde procede;
- cómo funciona a grandes rasgos;
- quién puede utilizarla;
- qué límites tiene;
- qué relación tiene con la cosmología;
- qué relación tiene con religión y sociedad.

No debería contener todas las reglas detalladas.

---

# 24. Leyes de la Magia

Debe explicar las reglas fundamentales que no deberían cambiar arbitrariamente.

Preguntas útiles:

- ¿Qué puede hacer la magia?
- ¿Qué no puede hacer?
- ¿Cuál es su coste?
- ¿Qué fuentes existen?
- ¿Puede romperse una ley?
- ¿Qué ocurre cuando se abusa de ella?
- ¿Quién conoce realmente estas leyes?

Esta es una de las notas más importantes de toda la sección de Magia.

---

# 25. Escuelas y Tradiciones

Aquí describes formas de entender o practicar la magia.

Una escuela puede ser:

- académica;
- filosófica;
- técnica;
- cultural;
- religiosa;
- regional;
- histórica.

Una tradición no tiene por qué ser lo mismo que una escuela formal.

Define claramente los términos en `Escuelas y Tradiciones.md`.

---

# 26. Conjuros

`Conjuros.md` es el índice general.

Las carpetas `Nivel 1` a `Nivel 12` son categorías de organización.

Cada nivel debe tener su nota nodo:

```markdown
# Nivel 3

## Conjuros
- [[Conjuro A]]
- [[Conjuro B]]
```

Una ficha individual de conjuro puede incluir:

```markdown
# Nombre

## Descripción

## Nivel

## Escuela / tradición

## Tiempo de lanzamiento

## Alcance

## Componentes

## Duración

## Efecto

## Coste o riesgos

## Historia

## Usuarios conocidos

## Enlaces
```

Si Aedhyr utiliza niveles del 1 al 12, la nota debe reflejar el sistema propio del setting.

No hace falta adaptar todo automáticamente al D&D oficial si tu sistema modifica los conceptos.

---

# 27. Objetos Mágicos

`Objetos Mágicos.md` es el nodo general.

Las categorías `Común`, `Poco Común`, `Raro`, `Muy Raro`, `Legendario` y `Artefactos` son clasificaciones de organización.

Una ficha de objeto mágico puede contener:

```markdown
# Nombre

## Descripción

## Tipo

## Rareza

## Apariencia

## Poderes

## Limitaciones

## Requisitos

## Historia

## Creador

## Localización

## Propietarios conocidos

## Riesgos

## Enlaces
```

Los artefactos deberían recibir un tratamiento especialmente profundo cuando sean piezas relevantes del mundo.

---

# 28. Grimorios y Tomos

Aquí van libros, códices, grimorios y documentos mágicos.

Una ficha puede incluir:

- autor;
- fecha;
- origen;
- contenido;
- escuela o tradición;
- importancia;
- propiedades mágicas;
- propietarios;
- localización;
- reputación;
- estado actual.

Un libro puede existir como objeto físico y como obra intelectual. Enlaza ambas dimensiones cuando sea necesario.

---

# 29. 07_Bestiario

```text
07_Bestiario/
├── Ecología y Flora/
│   ├── Criaturas Vegetales/
│   └── Herbolario/
└── Tipos de Criaturas/
```

Esta estructura se conserva deliberadamente.

El Bestiario debe responder a:

> **¿Qué seres viven en Aedhyr y cómo encajan dentro de sus ecosistemas?**

---

# 30. Bestiario.md

Debe ser la entrada general.

Enlaza a:

- [[Ecología y Flora]];
- [[Tipos de Criaturas]].

Puede explicar brevemente cómo se clasifica la vida sobrenatural y natural.

---

# 31. Ecología y Flora

`Ecología y Flora.md` es el nodo general.

Debe conectar el bestiario con:

- ecosistemas;
- biomas;
- plantas;
- criaturas vegetales;
- recursos naturales;
- relaciones depredador/presa;
- efectos mágicos del entorno.

---

## 31.1. Criaturas Vegetales

Aquí entran seres vegetales que funcionen como criaturas y no simplemente como plantas.

Una criatura vegetal debe recibir una ficha propia si tiene identidad suficiente.

---

## 31.2. Herbolario

Puede contener plantas, hierbas, hongos y recursos botánicos.

Una ficha de planta puede incluir:

- aspecto;
- hábitat;
- ciclo;
- propiedades;
- usos culinarios;
- usos medicinales;
- usos mágicos;
- peligros;
- rareza;
- criaturas asociadas.

---

# 32. Tipos de Criaturas

Las carpetas de:

- Aberraciones;
- Bestias;
- Celestiales;
- Cienos;
- Constructos;
- Dragones;
- Elementales;
- Feéricos;
- Gigantes;
- Humanoides;
- Infernales;
- Monstruosidades;
- No Muertos;

son categorías de clasificación.

Cada nota nodo de tipo debe ser un índice y una definición breve del tipo.

Ejemplo:

```markdown
# Bestias

## Concepto

## Características generales

## Criaturas
- [[Alaini]]
- [[Noctarra]]
```

---

# 33. Ficha de criatura

La plantilla de criatura debe ser flexible.

Puede incluir:

```markdown
# Nombre

## Identidad

## Clasificación

## Apariencia

## Hábitat

## Comportamiento

## Alimentación

## Reproducción / ciclo vital

## Capacidades

## Debilidades

## Inteligencia

## Sociedad

## Relación con otras criaturas

## Relación con pueblos

## Importancia cultural o mítica

## Encuentros / uso en partida

## Datos de juego
```

No todo tiene que estar completado.

Para una criatura puramente natural, por ejemplo, puede no existir importancia religiosa.

---

# 34. 08_Facciones y Organizaciones

Esta sección debe permanecer preparada para albergar estructuras jerárquicas.

`Facciones y Organizaciones.md` es el nodo general.

Cuando una organización contiene suborganizaciones reales, la jerarquía de carpetas puede representarlo.

Por ejemplo:

```text
Los Vaelirr/
├── El Velo de Alabastro/
├── Los Argentarios/
├── Los Cantos de Plata/
├── Los Karn-Dur/
├── Los Nyr’vossai/
├── Los Orum-Hein/
├── Los Runaforjados/
├── Los Vaelendir/
├── Los Vhal'Shai/
└── Renata/
```

No hace falta eliminar esta profundidad: aquí la jerarquía puede formar parte del propio lore.

---

# 35. Cómo escribir una organización

Una nota de organización debe responder:

- ¿Qué es?
- ¿Por qué existe?
- ¿Qué quiere conseguir?
- ¿Cómo se organiza?
- ¿Quién manda?
- ¿Quiénes son sus miembros importantes?
- ¿Dónde opera?
- ¿Qué recursos posee?
- ¿Qué métodos utiliza?
- ¿Qué relaciones tiene?
- ¿Qué reputación tiene?
- ¿Qué secretos esconde?

### Estructura recomendada

```markdown
# Nombre

## Resumen

## Origen

## Propósito

## Estructura

## Liderazgo

## Miembros relevantes

## Territorio / presencia

## Recursos

## Relaciones

## Enemigos

## Historia

## Secretos

## Enlaces
```

---

# 36. Los miembros de una facción

Si un personaje todavía es pequeño, puede permanecer físicamente dentro de la carpeta de la organización si así se ha decidido para la estructura de trabajo.

Ejemplo:

```text
Los Argentarios/
    Los Argentarios.md
    Teryn Volsharr.md
```

Pero debe existir un enlace desde la organización:

```markdown
## Miembros relevantes

- [[Teryn Volsharr]]
```

Y el personaje debería enlazar de vuelta:

```markdown
## Afiliaciones

- [[Los Argentarios]]
```

Si un personaje crece hasta tener una historia independiente muy grande, puede trasladarse posteriormente a `09_Personajes y NPCs` sin perder sus enlaces.

---

# 37. 09_Personajes y NPCs

```text
09_Personajes y Npcs/
├── Npcs/
└── Personajes/
```

La separación sirve para distinguir **función** dentro de la experiencia de juego, no para marcar si alguien está vivo o muerto.

No crear carpetas `Activos` e `Históricos`.

El estado puede ser una propiedad:

```yaml
estado: activo
```

```yaml
estado: histórico
```

---

# 38. Personajes/Personajes.md

Debe explicar qué se considera un personaje relevante y servir de índice.

Puede agrupar por:

- personajes importantes;
- protagonistas;
- líderes;
- figuras históricas;
- etc.

No necesitas crear todas estas carpetas ahora. Los enlaces son suficientes.

---

# 39. NPCs/Npcs.md

Es el nodo de NPCs.

Un NPC puede ser:

- comerciante;
- guardia;
- líder;
- aliado;
- enemigo;
- informante;
- habitante local;
- personaje secundario.

La importancia narrativa de un NPC puede aumentar con el tiempo sin obligarte a cambiar de categoría.

---

# 40. Ficha de personaje

Recomendación:

```markdown
# Nombre

## Identidad

## Apariencia

## Personalidad

## Historia

## Motivaciones

## Miedos

## Relaciones

## Afiliaciones

## Lugar de origen

## Ubicación actual

## Creencias

## Capacidades

## Secretos

## Estado

## Papel en la historia

## Enlaces
```

En personajes importantes, evita llenar la ficha sólo de adjetivos.

“Es inteligente, carismático y misterioso” dice poco.

Es mejor explicar:

> qué decisiones toma;
> qué quiere;
> cómo trata a los demás;
> qué está dispuesto a sacrificar;
> qué considera imperdonable.

Eso genera personalidad real.

---

# 41. 10_Campañas

```text
10_Campañas/
    Campañas.md
```

Esta sección debe mantenerse separada del lore general.

El objetivo es poder distinguir:

> **Lo que es Aedhyr**

de:

> **Lo que ocurrió en una campaña concreta.**

`Campañas.md` debe ser el índice general.

Cuando aparezca una campaña real, puedes crear:

```text
10_Campañas/
└── Campaña 01/
    ├── Campaña 01.md
    ├── Sesiones/
    ├── Aventuras/
    ├── PNJ de campaña/
    ├── Lugares de campaña/
    └── Diario de campaña/
```

No es obligatorio crear esas carpetas hasta que la campaña lo necesite.

### Regla importante

Un acontecimiento de campaña puede acabar convertido en canon de Aedhyr.

Cuando eso ocurra, **duplica o resume el hecho en la sección canónica correspondiente**, en vez de asumir que la nota de campaña es automáticamente parte del setting.

---

# 42. 99_Archivos

Esta carpeta contiene material auxiliar:

```text
99_Archivos/
    Alaini.png
    Noctarra.png
    Qirathi.png
```

No debe contener notas de lore.

Su función es almacenar imágenes u otros archivos auxiliares que alimentan las notas de Aedhyr.

Cuando una imagen forme parte importante de una entrada, incrústala desde su nota correspondiente.

---

# 43. Convenciones de nombres

Para que la bóveda permanezca fácil de buscar:

## Nombres de carpetas

Usa nombres descriptivos, estables y consistentes.

## Nombres de entidades

Utiliza el nombre canónico de la entidad.

No cambies el nombre del archivo sólo porque aparezca una variante ortográfica en un texto diegético.

## Acrónimos

Mantén el estilo actual de Aedhyr cuando un nombre propio sea deliberadamente especial.

## Mayúsculas

Mantén una política consistente en nombres de carpetas y notas.

---

# 44. Cómo escribir notas nodo vs. notas de contenido

Esta distinción es crucial.

## Nota nodo

Ejemplo:

```text
Atlas.md
```

Debe:

- orientar;
- categorizar;
- enlazar;
- resumir.

## Nota de entidad

Ejemplo:

```text
Qirathi.md
Ciudad X.md
Oren.md
Teryn Volsharr.md
```

Debe:

- explicar la entidad;
- darle identidad;
- mostrar contexto;
- relacionarla con otras entidades.

No mezcles las dos funciones.

---

# 45. Cómo evitar contradicciones

Cuando escribas una nueva nota, comprueba tres cosas:

### 1. ¿Qué notas menciona?

Enlázalas.

### 2. ¿Qué notas deberían mencionarla?

Cuando tengas tiempo, añade el enlace recíproco desde los nodos pertinentes.

### 3. ¿Qué información podría contradecir?

Antes de crear una verdad nueva, revisa las notas centrales relacionadas.

Por ejemplo, si vas a escribir una nueva fecha histórica, comprueba:

- calendario;
- era correspondiente;
- eventos próximos;
- edad de personajes;
- fundación de ciudades;
- genealogías.

La consistencia temporal se rompe muy fácilmente en worldbuilding.

---

# 46. Cómo tratar la información desconocida

No necesitas decidirlo todo.

Puedes escribir:

```markdown
## Lo que se sabe

...

## Lo que se cree

...

## Desconocido

...
```

Esto es especialmente útil para:

- mitología;
- historia antigua;
- origen del universo;
- dioses;
- civilizaciones desaparecidas;
- magia.

La ausencia de una respuesta puede ser parte del mundo.

---

# 47. Cómo tratar diferentes perspectivas

No todo el mundo de Aedhyr debe creer lo mismo.

Cuando existan versiones distintas, no las fusiones artificialmente.

Ejemplo:

```markdown
## Versión oficial

La Iglesia de X sostiene que...

## Tradición Qirathi

Los Qirathi cuentan que...

## Interpretación académica

Los historiadores creen que...

## Lo que realmente ocurrió

[Información de canon / DM]
```

Esto permite que Aedhyr tenga historia, propaganda, religión y memoria cultural sin confundirlas.

---

# 48. Cómo escribir el worldbuilding sin caer en el exceso de exposición

Una ficha no tiene que explicar absolutamente todo.

Prioriza aquello que permita comprender el concepto.

Por ejemplo, una ciudad necesita identidad, función y contexto antes que diez páginas de nombres de calles.

Un dios necesita cosmología, carácter, símbolos y relaciones antes que una lista interminable de festividades.

Una criatura necesita comportamiento y nicho ecológico antes que una mitología completa si no la tiene.

### Principio

> **Profundiza donde haya consecuencias.**

Una idea es interesante cuando afecta a algo más.

---

# 49. Relaciones que conviene enlazar siempre

Cuando existan las notas correspondientes, intenta relacionar:

### Lugares

- continente;
- región;
- reino;
- ciudad;
- habitantes;
- facciones;
- acontecimientos.

### Personajes

- familia;
- facciones;
- lugares;
- dioses/religión;
- acontecimientos.

### Dioses

- otros dioses;
- dominios;
- religión;
- cultos;
- mitos;
- lugares;
- festividades.

### Facciones

- líderes;
- miembros;
- lugares;
- aliados;
- enemigos;
- recursos;
- eventos.

### Criaturas

- hábitat;
- flora/fauna asociada;
- pueblos;
- mitos;
- depredadores;
- recursos.

Esto hará que el grafo de Obsidian se convierta en una representación útil del mundo.

---

# 50. Qué debe aparecer en las notas nodo de las carpetas

Como regla general:

```markdown
# Nombre

> Una o dos frases explicando qué contiene esta sección.

## Categorías
- [[Categoría 1]]
- [[Categoría 2]]
- [[Categoría 3]]

## Conceptos clave
- [[Entidad importante]]
- [[Otra entidad]]
```

Si la sección ya tiene suficiente contenido, añade una pequeña introducción contextual antes de los enlaces.

---

# 51. Qué NO hacer

## No duplicar lore

Si `Oren.md` explica a Oren, no copies toda la información de Oren dentro de `Los Soles.md`.

`Los Soles.md` debe enlazar a Oren y resumirlo si hace falta.

## No colocar un personaje en diez carpetas

Su lugar principal debe ser único.

## No crear una carpeta porque parezca bonita

Crea una carpeta cuando represente una distinción real dentro de tu modelo mental.

## No convertir los nodos en ensayos

Son puertas de entrada.

## No inventar información sólo para completar una plantilla

Una sección vacía puede esperar.

## No mezclar canon y borradores sin indicarlo

Una hipótesis no debe parecer una verdad establecida.

---

# 52. Cómo trabajar cada vez que tengas una idea nueva

Utiliza este proceso:

### Paso 1 — Identifica qué es

¿Es un:

- lugar;
- personaje;
- criatura;
- deidad;
- facción;
- evento;
- concepto mágico;
- elemento cultural;
- etc.?

### Paso 2 — Busca su hogar

Ve a la carpeta correspondiente.

### Paso 3 — Comprueba si ya existe

Antes de crear la nota, busca el nombre en toda la bóveda.

### Paso 4 — Crea la nota

Utiliza la plantilla correspondiente si existe.

### Paso 5 — Escribe primero el núcleo

¿Qué es?

¿Por qué importa?

### Paso 6 — Enlaza

Añade enlaces a las entidades relacionadas.

### Paso 7 — Amplía

Después desarrolla historia, detalles, cultura, conflictos, secretos, etc.

### Paso 8 — Comprueba contradicciones

Revisa las notas principales afectadas.

---

# 53. Cómo expandir la estructura en el futuro

No cambies la arquitectura porque una nota individual sea compleja.

Sólo crea una nueva categoría cuando varias notas empiecen a necesitarla.

Ejemplo:

Si dentro de `Ciudades` aparecen veinte ciudades marítimas y empiezas a necesitar navegar por puertos, entonces puedes crear una clasificación específica.

No la crees por adelantado sólo porque “algún día quizá haya puertos”.

La estructura actual ya es suficientemente completa para crecer.

---

# 54. El principio más importante de todo el sistema

> **La estructura debe ayudarte a pensar sobre Aedhyr, no hacerte pensar sobre Obsidian.**

Si estás escribiendo una idea y pasas más tiempo pensando “¿en qué carpeta va?” que desarrollándola, probablemente existe una distinción estructural que debe revisarse.

Pero mientras una carpeta responda a una diferencia conceptual que realmente utilices, mantenerla es completamente válido.

---

# 55. Checklist rápida antes de dar una nota por buena

```markdown
- [ ] Sé qué es esta cosa.
- [ ] Sé por qué importa.
- [ ] Está en la carpeta adecuada.
- [ ] No estoy duplicando otra nota.
- [ ] He enlazado las entidades importantes.
- [ ] He separado hechos de creencias o rumores cuando corresponde.
- [ ] No he rellenado información sólo por completar una plantilla.
- [ ] La información es coherente con el resto de Aedhyr.
- [ ] He dejado claro qué está decidido y qué sigue abierto.
```

---

# 56. Checklist específica para cada tipo de entidad

## Lugar

```markdown
- [ ] Ubicación
- [ ] Naturaleza del lugar
- [ ] Habitantes
- [ ] Gobierno / control
- [ ] Recursos
- [ ] Lugares relevantes
- [ ] Facciones
- [ ] Historia
- [ ] Conflictos
- [ ] Enlaces
```

## Personaje

```markdown
- [ ] Identidad
- [ ] Apariencia
- [ ] Personalidad
- [ ] Motivaciones
- [ ] Historia
- [ ] Relaciones
- [ ] Afiliaciones
- [ ] Lugar
- [ ] Secretos
- [ ] Estado
```

## Deidad

```markdown
- [ ] Naturaleza
- [ ] Generación / posición
- [ ] Dominios
- [ ] Símbolos
- [ ] Relaciones
- [ ] Mitos
- [ ] Culto
- [ ] Ritos
- [ ] Lugares
```

## Facción

```markdown
- [ ] Propósito
- [ ] Origen
- [ ] Organización
- [ ] Liderazgo
- [ ] Miembros
- [ ] Recursos
- [ ] Territorio
- [ ] Aliados
- [ ] Enemigos
- [ ] Secretos
```

## Criatura

```markdown
- [ ] Clasificación
- [ ] Aspecto
- [ ] Hábitat
- [ ] Comportamiento
- [ ] Alimentación
- [ ] Ciclo vital
- [ ] Capacidades
- [ ] Debilidades
- [ ] Relaciones ecológicas
- [ ] Relaciones culturales
```

---

# 57. Plantillas: filosofía

Las plantillas deben ser **andamios, no formularios obligatorios**.

Nunca debes sentir que una nota está incompleta porque le falten diez encabezados.

Una plantilla sirve para recordar qué preguntas merece la pena hacerse.

### Regla de uso

> **Si un apartado no aporta información, elimínalo de esa ficha.**

No escribas:

```markdown
## Alimentación

No aplicable.
```

simplemente elimina el apartado, salvo que quieras dejar constancia deliberada de que esa ausencia tiene sentido.

---

# 58. Qué significa que una nota esté “terminada”

Una nota no necesita estar completa al 100 % para ser útil.

Una nota está suficientemente desarrollada cuando:

1. define claramente el concepto;
2. establece su identidad dentro de Aedhyr;
3. explica las relaciones más importantes;
4. no contradice el canon conocido;
5. deja claro qué partes siguen sin decidirse.

El worldbuilding puede seguir creciendo indefinidamente.

---

# 59. Principio de canon interno

Cuando una nueva idea contradiga una vieja, no decidas automáticamente que la vieja es la correcta.

Primero determina si:

- la nueva idea es mejor;
- la vieja era un borrador;
- ambas pueden coexistir como perspectivas diferentes;
- una puede convertirse en información falsa dentro del mundo;
- o realmente hay que retconear.

Después actualiza los enlaces y las notas afectadas.

---

# 60. El objetivo final de la bóveda

La bóveda no debe ser sólo un almacén de información.

Debe permitirte pasar rápidamente de:

```text
Mundo
→ continente
→ reino
→ ciudad
→ facción
→ personaje
→ acontecimiento
→ mito
→ dios
→ religión
→ criatura
→ magia
```

y también recorrer el camino inverso.

Cuando el sistema esté maduro, podrás abrir una nota de cualquier entidad y navegar por las relaciones que la conectan con el resto de Aedhyr.

Ese es el verdadero propósito de la estructura.

---

# 61. Nota sobre el árbol actual

La estructura utilizada para esta guía corresponde al árbol proporcionado para la bóveda.

Hay un detalle ortográfico en el árbol actual:

```text
Era Perhistórica/
    Era Prehistórica.md
```

La carpeta parece estar pensada como `Era Prehistórica/`. Se recomienda corregir el nombre para que coincida con la nota.

Asimismo, se recomienda mantener una convención homogénea para `NPCs` en lugar de `Npcs` cuando se normalicen los nombres.

---

# 62. Resumen en una sola página

Cuando tengas dudas sobre dónde poner algo, utiliza esta tabla mental:

| Pregunta | Lugar principal |
|---|---|
| ¿Cuándo ocurrió? | [[Historia]] |
| ¿Dónde está? | [[Atlas]] |
| ¿Qué hay en el cielo? | [[Astronomía y Tiempo]] |
| ¿En qué creen? | [[Mitología y Religión]] |
| ¿Cómo viven? | [[Cultura y Sociedad]] |
| ¿Cómo funciona la magia? | [[Magia]] |
| ¿Qué criaturas existen? | [[Bestiario]] |
| ¿Quién tiene poder organizado? | [[Facciones y Organizaciones]] |
| ¿Quién es esa persona? | [[Personajes y NPCs]] |
| ¿Qué ocurrió durante la partida? | [[Campañas]] |

Y después:

> **Una entidad tiene un hogar. Sus relaciones viven en los enlaces. Sus atributos pueden vivir en propiedades.**

---

# 63. Regla de oro de Aedhyr

> ## Construye el mundo como si fuera una red, no una pila de documentos.
>
> La carpeta te dice dónde empezar.
>
> La nota te dice qué es.
>
> Los enlaces te dicen con qué se conecta.
>
> La historia te dice qué cambió.
>
> La cultura te dice cómo lo viven los mortales.
>
> La mitología te dice cómo lo interpretan.
>
> Y la campaña te dice qué ocurrió cuando los jugadores entraron en él.

