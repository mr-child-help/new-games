---
title: Cambiar la etapa de una solicitud de extracción
intro: 'Puedes marcar un borrador de solicitud de extracción como listo para revisión {% ifversion fpt or ghae or ghes or ghec %} o convertir la solicitud en borrador{% endif %}.'
permissions: People with write permissions to a repository and pull request authors can change the stage of a pull request.
product: '{% data reusables.gated-features.draft-prs %}'
redirect_from:
  - /github/collaborating-with-issues-and-pull-requests/proposing-changes-to-your-work-with-pull-requests/changing-the-stage-of-a-pull-request
  - /articles/changing-the-stage-of-a-pull-request
  - /github/collaborating-with-issues-and-pull-requests/changing-the-stage-of-a-pull-request
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Pull requests
shortTitle: Cambiar el estado
---

## Marcar una solicitud como lista para revisión

{% data reusables.pull_requests.mark-ready-review %}

{% ifversion fpt or ghae or ghes or ghec %}
{% tip %}

**Tip**: También puedes marcar una solicitud de cambios como lista para revisión utilizando el {% data variables.product.prodname_cli %}. Para obtener más información, consulta la sección "[`gh pr ready`](https://cli.github.com/manual/gh_pr_ready)" en la documentación de {% data variables.product.prodname_cli %}.

{% endtip %}
{% endif %}

{% data reusables.repositories.sidebar-pr %}
2. En la lista "Pull requests" (Solicitudes de extracción), haz clic en la solicitud de extracción que deseas marcar como disponibles para revisión.
3. En la caja de fusión, da clic en **Listo para revisión**. ![Botón Ready for review (Disponible para revisión)](/assets/images/help/pull_requests/ready-for-review-button.png)

{% ifversion fpt or ghae or ghes or ghec %}

## Convertir una solicitud de extracción en borrador

Puedes convertir una solicitud de extracción en borrador en cualquier momento. Por ejemplo, si accidentalmente abriste una solicitud de extracción en vez de un borrador, o si recibiste retroalimentación en tu solicitud de extracción, la cual necesitas atender, puedes convertirla en borrador para indicar que requiere más cambios. Nadie puede fusionar la solicitud de extracción hasta que la marques nuevamente como lista para revisión. Las personas que ya se han suscrito a las notificaciones de la solicitud de extracción no podrán darse de baja de éstas cuando la conviertas en borrador.

{% data reusables.repositories.sidebar-pr %}
2. En las lista de "Solicitudes de extracción", da clic en aquella que quieras convertir en borrador.
3. En la barra lateral derecha, debajo de "Revisores", da clic en **Convertir en borrador**. ![Enlace para convertir en borrador](/assets/images/help/pull_requests/convert-to-draft-link.png)
4. Da clic en **Convertir en borrador**. ![Confirmación de conversión a borrador](/assets/images/help/pull_requests/convert-to-draft-dialog.png)

{% endif %}

## Leer más

- "[Acerca de las solicitudes de extracción](/github/collaborating-with-issues-and-pull-requests/about-pull-requests)"
