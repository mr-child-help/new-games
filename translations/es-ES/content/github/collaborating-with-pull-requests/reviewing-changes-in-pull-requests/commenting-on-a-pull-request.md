---
title: Comentar en una solicitud de extracción
redirect_from:
  - /github/collaborating-with-issues-and-pull-requests/reviewing-changes-in-pull-requests/commenting-on-a-pull-request
  - /articles/adding-commit-comments/
  - /articles/commenting-on-the-diff-of-a-pull-request/
  - /articles/commenting-on-differences-between-files/
  - /articles/commenting-on-a-pull-request
  - /github/collaborating-with-issues-and-pull-requests/commenting-on-a-pull-request
intro: 'Luego de abrir una solicitud de extracción en un repositorio, los colaboradores o miembros del equipo pueden comentar sobre la comparación de archivos entre dos ramas especificadas, o dejar comentarios generales en el proyecto en general.'
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Pull requests
shortTitle: Comentar en una solicitud de cambios
---

## Acerca de los comentarios de las solicitudes de extracción

Puedes comentar en la pestaña **Conversation** (Conversación) de una solicitud de extracción para dejar comentarios generales, preguntas o apoyos. También puedes sugerir cambios que el autor de la solicitud de extracción puede aplicar directamente desde tu comentario.

![Conversación de solicitud de extracción](/assets/images/help/pull_requests/conversation.png)

También puedes comentar sobre secciones específicas de un archivo en la pestaña **Files changed** (Archivos cambiados) de una solicitud de extracción en forma de comentarios en la línea o como parte de una [revisión de solicitud de extracción](/articles/about-pull-request-reviews). Agregar comentarios en la línea es una gran manera de debatir preguntas sobre la implementación o brindar retroalimentación al autor.

Para obtener más información sobre cómo agregar comentarios en la línea a una revisión de solicitud de extracción, consulta ["Revisar cambios propuestos en una solicitud de extracción".](/articles/reviewing-proposed-changes-in-a-pull-request)

{% note %}

**Nota:** Si respondes una solicitud de extracción por correo electrónico, tu comentario se agregará a la pestaña **Conversation** (Conversación) y no será parte de una revisión de solicitud de extracción.

{% endnote %}

Para responder un comentario en la línea que ya existe, deberás ir hasta el comentario en la pestaña **Conversation** (Conversación) o en la pestaña **Files changed** (Archivos modificados) y agregar otro comentario en la línea debajo.

{% tip %}

**Tips:**
- Los comentarios de las solicitudes de extracción soportan el mismo [ formato](/categories/writing-on-github) que los comentarios regulares en {% data variables.product.product_name %}, como @menciones, emojis y referencias.
- Puedes agregar reacciones a los comentarios de las solicitudes e cambios en la pestaña **Archivos que se cambiaron**.

{% endtip %}

## Agregar comentarios en la línea a una solicitud de extracción

{% data reusables.repositories.sidebar-pr %}
2. En la lista de solicitudes de extracción, haz clic en la solicitud de extracción en la que deseas dejar los comentarios en la línea.
{% data reusables.repositories.changed-files %}
{% data reusables.repositories.start-line-comment %}
{% data reusables.repositories.type-line-comment %}
{% data reusables.repositories.suggest-changes %}
5. Cuando hayas terminado, haz clic en **Add single comment** (Agregar comentario único). ![Ventana de comentario en línea](/assets/images/help/commits/inline-comment.png)

Cualquier persona que observe la solicitud de extracción o el repositorio recibirá una notificación de tu comentario.

{% data reusables.pull_requests.resolving-conversations %}

## Leer más

- "[Escribir en GitHub](/github/writing-on-github)"
{% ifversion fpt or ghec %}- "[Informar abuso o spam](/communities/maintaining-your-safety-on-github/reporting-abuse-or-spam)"
{% endif %}
