---
title: Revisar los cambios propuestos en una solicitud de extracción
intro: 'En una solicitud de extracción, puedes revisar y opinar sobre las confirmaciones, los archivos cambiados y las diferencias (o "diff") entre los archivos de las ramas de base y comparada.'
redirect_from:
  - /github/collaborating-with-issues-and-pull-requests/reviewing-changes-in-pull-requests/reviewing-proposed-changes-in-a-pull-request
  - /articles/reviewing-proposed-changes-in-a-pull-request
  - /github/collaborating-with-issues-and-pull-requests/reviewing-proposed-changes-in-a-pull-request
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Pull requests
shortTitle: Revisar los cambios propuestos
---

## Acerca de revisar las solicitudes de extracción

Puedes revisar los cambios de una solicitud de extracción en un archivo por vez. Mientras revisas los archivos en una solicitud de extracción, puedes dejar comentarios individuales en cambios específicos. Después de que terminas de revisar cada archivo, puedes marcarlo como visto. Esto colapsa el archivo, lo cual te ayuda a identificar los archivos que aún debes revisar. Una barra de progreso en el encabezado de la solicitud de cambios muestra la cantidad de archivos que has visto. Después de revisar tantos archivos como quieras, puedes aprobar la solicitud de cambios o solicitar cambios adicionales si emites tu revisión con un comentario de resumen.

{% data reusables.search.requested_reviews_search_tip %}

## Comenzar una revisión

{% include tool-switcher %}

{% webui %}

{% data reusables.repositories.sidebar-pr %}
{% data reusables.repositories.choose-pr-review %}
{% data reusables.repositories.changed-files %}
{% data reusables.repositories.start-line-comment %}
{% data reusables.repositories.type-line-comment %}
{% data reusables.repositories.suggest-changes %}
5. Cuando estés listo, haz clic en **Start a review** (Comenzar una revisión). Si ya comenzaste una revisión, puedes hacer clic en **Add review comment** (Agregar comentario de revisión). ![Botón Start a review (Comenzar una revisión)](/assets/images/help/pull_requests/start-a-review-button.png)

Antes de enviar tu revisión, tus comentarios de líneas quedan _pendientes_, y solo tú los puedes ver. Puedes editar los comentarios pendientes en cualquier momento antes de enviar tu revisión. Para cancelar una revisión pendiente, incluidos todos sus comentarios pendientes, desplázate hasta el final de la cronología en la pestaña Conversation (Conversación) y haz clic en **Cancel review** (Cancelar revisión).

![Botón Cancel review (Cancelar revisión)](/assets/images/help/pull_requests/cancel-review-button.png)
{% endwebui %}

{% ifversion fpt or ghec %}

{% codespaces %}

Puedes utilizar los [{% data variables.product.prodname_codespaces %}](/codespaces/overview) para probar, ejecutar y revisar las solicitudes de cambios.

{% data reusables.codespaces.review-pr %}

Para obtener más información sobre revisar las solicitudes de cambios en los {% data variables.product.prodname_codespaces %}, consulta la sección "[Utilizar los Codespaces para las solicitudes de cambios](/codespaces/developing-in-codespaces/using-codespaces-for-pull-requests)".

{% endcodespaces %}
{% endif %}

{% ifversion fpt or ghes > 3.1 or ghec %}
## Revisar los cambios de las dependencias

{% data reusables.dependency-review.beta %}

Si la solicitud de cambios contiene cambios para las dependencias, puedes utilizar la revisión de dependencias para un archivo de bloqueo o de manifiesto para ver qué ha cambiado y verificar si los cambios introducen vulnerabilidades de seguridad. Para obtener más información, consulta la sección "[Revisar los cambios a las dependencias en una solicitud de cambios](/github/collaborating-with-issues-and-pull-requests/reviewing-dependency-changes-in-a-pull-request)".

{% data reusables.repositories.changed-files %}

1. A la derecha del encabezado de un archivo de bloqueo o de manifiesto, muestra la revisión de dependencias dando clic en el botón de diff enriquecido **{% octicon "file" aria-label="The rich diff icon" %}**.

   ![El botón de diff rica](/assets/images/help/pull_requests/dependency-review-rich-diff.png)

{% data reusables.repositories.return-to-source-diff %}
{% endif %}

## Marcar un archivo como visto

Después de que hayas terminado de revisar un archivo, puedes marcar el archivo como visto, y el archivo se colapsará. Si el archivo se modifica después de que lo hayas visto, dejará de estar marcado como visto.

{% data reusables.repositories.changed-files %}
2. A la derecha del encabezado del archivo que terminaste de revisar, selecciona **Viewed** (Visto). ![Casilla Viewed (Visto)](/assets/images/help/pull_requests/viewed-checkbox.png)

## Enviar tu revisión

Después de que hayas terminado de revisar todos los archivos que quieras de la solicitud de extracción, envía tu revisión.

{% data reusables.repositories.changed-files %}
{% data reusables.repositories.review-changes %}
{% data reusables.repositories.review-summary-comment %}
4. Selecciona el tipo de revisión que te gustaría proporcionar: ![Botones Radio con opciones de revisión](/assets/images/help/pull_requests/pull-request-review-statuses.png)
    - Selecciona **Comment** (Comentario) para dejar una opinión general sin aprobar de manera explícita los cambios ni solicitar cambios adicionales.
    - Selecciona **Approve** (Aprobar) para enviar tus comentarios y aprobar la fusión de los cambios propuestos en la solicitud de extracción.
    - Selecciona **Request changes** (Solicitar cambios) para enviar comentarios que se deban tener en cuenta antes de que se pueda fusionar la solicitud de extracción.
{% data reusables.repositories.submit-review %}

{% data reusables.repositories.request-changes-tips %}

## Leer más

- "[Acerca de las ramas protegidas](/github/administering-a-repository/about-protected-branches#require-pull-request-reviews-before-merging)"
- "[Filtrar solicitudes de extracción por estado de revisión](/github/managing-your-work-on-github/filtering-pull-requests-by-review-status)"
