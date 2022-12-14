---
title: Repository löschen
intro: 'Du kannst ein Repository oder einen Fork löschen, wenn Du Organisationsinhaber bist oder über Administratorberechtigungen für das Repository oder den Fork verfügst. Durch das Löschen eines geforkten Repositorys wird das vorgelagerte Repository nicht gelöscht.'
redirect_from:
  - /delete-a-repo/
  - /deleting-a-repo/
  - /articles/deleting-a-repository
  - /github/administering-a-repository/deleting-a-repository
  - /github/administering-a-repository/managing-repository-settings/deleting-a-repository
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Repositories
---

{% data reusables.organizations.owners-and-admins-can %} ein Organisations-Repository löschen. Wenn **Allow members to delete or transfer repositories for this organization** (Mitgliedern das Löschen oder Übertragen von Repositorys für diese Organisation erlauben) deaktiviert wurde, können nur Organisationsinhaber Repositorys der Organisation löschen. {% data reusables.organizations.new-repo-permissions-more-info %}

{% ifversion not ghae %}Deleting a public repository will not delete any forks of the repository.{% endif %}

{% warning %}

**Warnings**:

- Deleting a repository will **permanently** delete release attachments and team permissions. Diese Aktion **kann nicht** rückgängig gemacht werden.
- Deleting a private or internal repository will delete all forks of the repository.

{% endwarning %}

Some deleted repositories can be restored within 90 days of deletion. {% ifversion ghes or ghae %}Your site administrator may be able to restore a deleted repository for you. Weitere Informationen findest Du unter „[Ein gelöschtes Repository wiederherstellen](/admin/user-management/managing-repositories-in-your-enterprise/restoring-a-deleted-repository).“ {% else %}For more information, see "[Restoring a deleted repository](/articles/restoring-a-deleted-repository)."{% endif %}

{% data reusables.repositories.navigate-to-repo %}
{% data reusables.repositories.sidebar-settings %}
2. Klicke unter „Danger Zone“ (Gefahrenzone) auf **Delete this repository** (Dieses Repository löschen). ![Schaltfläche „Repository deletion" (Repository Löschung)](/assets/images/help/repository/repo-delete.png)
3. **Lies die Warnungen.**.
4. Um sicherzustellen, dass Du das richtige Repository löschst, gib den Namen des Repositorys ein, das Du löschen möchtest. ![Lösch-Kennzeichnung](/assets/images/help/repository/repo-delete-confirmation.png)
5. Klicke auf **I understand the consequences, delete this repository** (Mir sind die Folgen bekannt, lösche dieses Repository).
