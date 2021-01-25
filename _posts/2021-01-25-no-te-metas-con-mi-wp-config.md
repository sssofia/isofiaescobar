---
layout: post
title: No te metas con mi wp-config
---

Para empezar con los posts del lado developer, decidí por compartir una experiencia relacionada a Wordpress que me sucedió el año pasado y que resolví hasta este. Con mi blog de hace años, [Inspiración Volátil](http://www.inspiracionvolatil.com), tuve un problema algo inesperado: Me empezó a salir un error justamente en la parte de arriba del home, más que nada hablaba sobre un par de errores en las carpetas de ciertos plugins y la versión de php. Lo que fue el colmo es que al intentar loguearme no me dejaba y aparecía este otro error:

ERROR: Cookies are blocked due to unexpected output. For help, please see this documentation or try the support forums.

Literal, empecé a paniquear... no, tampoco hahahaha pero si, me preocupé y quería ver qué estaba pasando. Lo primero que pensé fue que a lo mejor era la versión de Wordpress y que tendría que actualizarlo. Considerando que no podía entrar a mi Dashboard eso significaba actualizar "a patita" dentro del FTP, lo cual me ponía un poco nerviosa porque nunca lo había hecho antes. Esto fue a principios de diciembre aproximadamente, así que un par de días después de haber visto el error admito que pensé: "¡ya va a ser Navidad! mejor lo revisaré en enero"

Y así fue. Con una mente un poco más despejada, lo primero que pensé fue retomar la búsqueda del error y dejé la actualización "a patita" como mi última opción. Después de varios foros y artículos, de revisar las carpetas de los themes uno por uno, llegué a la conclusión que el problema no era el theme. Ya un poco cansada de no encontrar nada, vi en un foro que alguien tenía un problema similar y que había hecho unas modificaciones en el archivo de wp-config.php, uno de los archivos importantes en la instalación de Wordpress; por lo que pensé que valdría la pena revisar dicho archivo, y...

¡Oh sorpresa! Encontré algo que no me esperaba. En la última línea, encontré algo que me llamó la atención:

define( €@$WP_AUTO_UPDATE_CORE$@€, true );   

(No recuerdo muy bien la secuencia de las letras pero era algo así)

Si quieren saber la importancia de unas simples comillas, pues aquí está. Este es un claro ejemplo de lo que podría pasar. Obviamente al reconocer lo que estaban haciendo los caracteres, los eliminé, coloqué las comillas donde deberían estar y ¡voilá! El error desapareció y pude entrar a mi blog como siempre lo había hecho.

El punto de esta larga historia es simple: Si tienen su blog o cualquier otro sitio en Wordpress, tomen su tiempo de darle mantenimiento, actualizarlo y asegurarlo. Por ejemplo, yo en mi blog y demás sitios de Wordpress que hago coloco plugins como [Jetpack](https://es.wordpress.org/plugins/jetpack/) para mejorar la seguridad, evitar spam y eventos así. Pero, considerando una situación parecida a la mía, la solución que encontré gracias al foro de Wordpress es colocar un código en el archivo de .htaccess para prohibir el acceso al archivo de wp-config.php y evitar cambios en el código como lo que me sucedió.

Este es el código (colocarlo hasta arriba)

```
<files wp-config.php>
order allow,deny
deny from all
</files>
```

Ya colocado, no es necesario cambiar permisos en el archivo.

Si quieren saber más sobre cómo mejorar la seguridad de sus sitios de Wordpress, aquí está la página que me ayudó: [Hardening Wordpress](https://wordpress.org/support/article/hardening-wordpress/) . Igual, si conocen más recomendaciones sobre cómo mejorar la seguridad en Wordpress, son bienvenidos 😄
