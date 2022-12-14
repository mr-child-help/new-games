---
title: Fechar uma pull request
intro: 'Você pode optar por *fechar* uma pull request sem [fazer merge dela no branch upstream](/articles/merging-a-pull-request). Isso poderá ser útil se as alterações propostas no branch não forem mais necessárias ou se outra solução tiver sido proposta em outro branch.'
redirect_from:
  - /github/collaborating-with-issues-and-pull-requests/incorporating-changes-from-a-pull-request/closing-a-pull-request
  - /articles/closing-a-pull-request
  - /github/collaborating-with-issues-and-pull-requests/closing-a-pull-request
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Pull requests
---

{% tip %}

**Dica**: se você abriu uma pull request com o branch base errado, em vez de fechá-la e abrir outra, é possível alterar o branch base. Para obter mais informações, consulte "[Alterar o branch base de uma pull request](/articles/changing-the-base-branch-of-a-pull-request)".

{% endtip %}

{% data reusables.repositories.sidebar-pr %}
2. Na lista "Pull Requests", clique na pull request da qual deseja fechar.
3. Na parte inferior, abaixo da caixa de comentários da pull request, clique em **Close pull request** (Fechar pull request). ![O botão para fechar a pull request](/assets/images/help/pull_requests/pullrequest-closebutton.png)
4. Opcionalmente, [exclua o branch](/articles/deleting-unused-branches). Assim, a lista de branches do repositório ficará limpa.
