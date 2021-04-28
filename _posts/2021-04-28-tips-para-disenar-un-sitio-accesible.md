---
layout: post
title: Tips para diseñar un sitio accesible
---

Tanto tiempo escribiendo en inglés la palabra "accessibility" que por poco escribo "accessibilidad" (hahaha). Lo siento, no pude evitarlo. Dejando a un lado mi mal chiste de ortografía, hoy quiero continuar el tema de la accesibilidad en la web gracias a un artículo que me topé en el camino: [Designing with accessibility in mind]([https://uxplanet.org/designing-with-accessibility-in-mind-f25a3f70b8c0](https://uxplanet.org/designing-with-accessibility-in-mind-f25a3f70b8c0)). 

En realidad, no tengo nada en contra del artículo. Me parece que resume muy bien los aspectos que hay que tomar para que un sitio sea accesible sin abrumar a los diseñadores con los aspectos técnicos. Sin embargo, creo que el título está mal. El contenido del artículo mezcla tips tanto de código como de diseño, cuando el título habla en específico desde el punto de vista de diseño. Esto me llevó a pensar: al final, ¿cómo se puede hacer accesible un sitio web si solamente se abarca la parte del diseño? 

Es aquí donde entra mi lista. En general, sobre lo que he aprendido del tema, mi conclusión es que la esencia de un sitio accesible está en cómo está hecho. En el código y la estructura está lo más importante, ya que este es el que el lector de pantalla interpreta para la persona que lo está utilizando. Puede que el diseño esté bien, pero si una imagen no tiene un texto alternativo, no se están utilizando las etiquetas semánticas de HTML5, o peor aún, el sitio no se puede navegar por medio del teclado, ahí ya estamos en serios problemas.

Pero no nos asustemos, aquí nos enfocaremos solo en el diseño ;)

Sin más preámbulos, les comparto mis tips:

1. Contraste de color

Más que una regla básica del diseño gráfico, como el típico caso del amarillo sobre blanco, lo que hay que considerar es el tema del daltonismo y sus diferentes tipos. Por ello es muy importante simplificar el contraste entre fondo y los elementos sobre este, a manera que puedan resaltar y sean fáciles de leer. Según los lineamientos del WCAG 2.1 un sitio web accesible tiene que tener un valor mínimo de contraste, y hay sitios como [WebAIM][(https://webaim.org/resources/contrastchecker/](https://webaim.org/resources/contrastchecker/)) los cuales son muy útiles para revisar el contraste de los colores que estamos utilizando y si se encuentran entre los valores sugeridos.

2. Complementar la información proporcionada con colores

Por ejemplo, en el caso de los mensajes de error. No limitarse a diseñar mensajes de error con color rojo y dejarlos así, sino también agregar un ícono o incuso un título o texto complementario que transmita que es un mensaje de error. En este aspecto me sirve pensar que estoy armando el diseño en escala de grises, (aclaración: las personas con daltonismo no miran así, esto es solo para fines didácticos) y analizar los elementos que estoy utilizando y si estos se explican por si solos. Si regresamos al ejemplo del mensaje de error sin icono o texto complementario, si nos pasamos a la "modalidad gris", ¿estaría comunicando que es un error o se confundiría con otra cosa?

Esto aplica también a elementos como enlaces. No solamente hay que cambiar el color de ellos, sino también mantener el subrayado para que visualmente este se diferencie del texto a su alrededor.

3. Contraste de color en todos los elementos interactivos

Para cerrar el tema del color, quiero recalcar que esto aplica a todo, en especial con elementos interactivos como botones, formularios y galerías. Es importante que los controles de las galerías o sliders y el texto dentro de los campos de los formularios (placeholder de los inputs) no sea de un gris muy claro que se confunda con el fondo. Obviamente el color de estos elementos cambia cuando estan activos e inactivos, pero hay que cuidar el contraste entre estos dos estados y el fondo. Otro estado muy importante aquí es el estado :focus, el cual permite que sea visible la posición con la que nos encontramos navegando con el teclado. Es por ello que tenemos que cuidar su contraste para que el sitio se pueda navegar correctamente y no se pierda de vista.

4. Tamaño del texto

Por último, el contraste también se maneja en los tamaños de los textos. Es importante mantener una jerarquía entre título, subtítulo y el contenido, y ser constante con su uso en todo el sitio. También, hay que evitar utilizar tamaños muy pequeños. Todo esto con el fin de facilitar la lectura.

Hasta aquí llegamos, después de terminar de diseñar el sitio es hora de pasárselo al maquetador o programador. En ese caso, me tocará hacer otro post describiendo los tips o checklist para ese otro proceso. Espero que hayan sido útiles estos tips, y si tienen algo más que agregar pueden contactarme (links en la página de About ✌️)
