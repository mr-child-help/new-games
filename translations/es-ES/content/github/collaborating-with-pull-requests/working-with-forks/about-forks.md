---
title: Acerca de las bifurcaciones
intro: Una bifurcación es una copia de un repositorio que administras. Las bifurcaciones te permiten realizar cambios a un proyecto sin afectar el repositorio original. Puedes recuperar actualizaciones o enviar cambios al repositorio original con solicitudes de extracción.
redirect_from:
  - /github/collaborating-with-issues-and-pull-requests/working-with-forks/about-forks
  - /articles/about-forks
  - /github/collaborating-with-issues-and-pull-requests/about-forks
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Pull requests
---

Bifurcar un repositorio es similar a copiar un repositorio, con dos diferencias principales:

* Puedes utilizar una solicitud de extracción para sugerir cambios desde las bifurcaciones de las cuales sea dueño tu usuario hacia el repositorio original, también conocido como el repositorio *ascendente*.
* Puedes llevar cambios desde tu repositorio ascendente a tu bifurcación local sincronizando tu bifurcación con el repositorio ascendente.

{% data reusables.repositories.you-can-fork %}

{% ifversion fpt or ghec %}

Si eres un miembro de una {% data variables.product.prodname_emu_enterprise %}, hay más restricciones sobre los repositorios que puedes bifurcar. {% data reusables.enterprise-accounts.emu-forks %} For more information, see "[About {% data variables.product.prodname_emus %}](/enterprise-cloud@latest/admin/authentication/managing-your-enterprise-users-with-your-identity-provider/about-enterprise-managed-users){% ifversion fpt %}" in the {% data variables.product.prodname_ghe_cloud %} documentation.{% else %}."{% endif %}

{% endif %}

{% data reusables.repositories.desktop-fork %}

Eliminar una bifurcación no eliminará el repositorio ascendente original. Puedes hacer tantos cambios como quieras a tu bifurcación—añadir colaboradores, renombrar archivos, generar {% data variables.product.prodname_pages %}—sin que esto afecte el repositorio original.{% ifversion fpt or ghec %} no puedes restablecer un repositorio bifurcado previamente eliminado. Para obtener más información, consulta "[Restaurar un repositorio eliminado](/articles/restoring-a-deleted-repository)".{% endif %}

En proyectos de código abierto, las bifurcaciones suelen iterar en ideas o cambios antes de que se presenten al repositorio ascendente. Cuando realizas cambios en la bifurcación que es propiedad de tu usuario y abres una solicitud de extracción que compara tu trabajo con el repositorio ascendente, puedes dar permiso a cualquiera con permiso de escritura en el repositorio ascendente para subir cambios a tu rama de solicitudes de extracción. Esto agiliza la colaboración permitiendo que los mantenedores del repositorio puedan hacer confirmaciones de cambios o ejecutar pruebas locales a tu rama de solicitud de extracción desde una bifurcación propiedad de un usuario antes de fusionarlas. No puedes otorgar permisos de escritura a una bifurcación que sea propiedad de una organización.

{% data reusables.repositories.private_forks_inherit_permissions %}

Si quieres crear un repositorio nuevo desde el contenido de uno existente pero no quieres fusionar tus cambios ascendentemente en ocasiones futuras, puedes duplicar el repositorio o, si éste es una plantilla, utilizarlo como plantilla. Para obtener más información, consulta la sección "[Duplicar un repositorio](/articles/duplicating-a-repository)" y "[Crear un repositorio desde una plantilla](/articles/creating-a-repository-from-a-template)".

## Leer más

- "[Acerca de los modelos de desarrollo colaborativo](/articles/about-collaborative-development-models)"
- "[Crear una solicitud de extracción desde una bifurcación](/articles/creating-a-pull-request-from-a-fork)"
- [Guías de código abierto](https://opensource.guide/){% ifversion fpt or ghec %}
- [{% data variables.product.prodname_learning %}]({% data variables.product.prodname_learning_link %}){% endif %}
