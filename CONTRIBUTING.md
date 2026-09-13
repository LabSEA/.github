# Como contribuir com o LabSEA

Este documento apresenta as formas mais comuns de contribuir com os projetos do LabSEA e como organizar o desenvolvimento de trabalhos relacionados a projetos de extensão, iniciação científica, disciplinas e pesquisas individuais.

## Visão geral

Existem três situações principais:

1. uma pessoa desenvolve um projeto pessoal e, posteriormente, ele passa a ser associado ao LabSEA.
2. uma pessoa contribui com um projeto que já pertence ao LabSEA;
3. um membro do laboratório desenvolve uma nova funcionalidade em um projeto do LabSEA;

Cada situação pode utilizar um fluxo diferente de GitHub.


## 1. Fork de um repositório pessoal para a organização

É possível que um integrante desenvolva inicialmente um projeto em seu próprio repositório e, posteriormente, associe esse projeto ao LabSEA.

Essa situação pode ocorrer em projetos de:

- iniciação científica;
- extensão;
- trabalhos acadêmicos;
- disciplinas;
- pesquisas individuais;
- protótipos desenvolvidos antes da formação de uma equipe.

Quando fizer sentido manter o repositório pessoal original, a organização LabSEA pode fazer um fork desse projeto para sua conta. Assim, o projeto passa a ter uma cópia vinculada à organização, mantendo também a relação com o membro que iniciou o desenvolvimento.

Esse modelo facilita a identificação da origem e da autoria do trabalho, especialmente quando o projeto começou como uma iniciativa individual e depois passou a fazer parte das atividades do laboratório.

Antes de criar o fork, é importante alinhar com o integrante:

- o nome e a descrição do projeto;
- quais pessoas terão acesso ao repositório;
- se o projeto continuará recebendo alterações no repositório pessoal;
- qual repositório será considerado a fonte principal;
- como serão reconhecidos os autores e colaboradores.

O fork não substitui a definição de responsabilidades. É importante deixar claro se o repositório principal será o pessoal ou o da organização e como as alterações serão sincronizadas entre eles.

Se a intenção for transferir definitivamente a propriedade e o desenvolvimento para o LabSEA, a transferência do repositório pode ser mais apropriada do que um fork. O fork é especialmente útil quando se deseja preservar o repositório original do autor e, ao mesmo tempo, disponibilizar uma versão vinculada à organização.


## 2. Fork de um repositório do LabSEA

O fork é uma cópia de um repositório em outra conta ou organização. Ele é útil quando a pessoa não possui permissão de escrita no repositório original.

Nesse fluxo, o colaborador:

1. conversa com um administrador do GitHub para confirmar o acesso e a forma de contribuição;
2. faz um fork do repositório do LabSEA para sua conta pessoal;
3. clona o fork para o computador;
4. desenvolve a alteração e cria os commits;
5. envia os commits para o próprio fork;
6. abre um Pull Request para o repositório oficial do LabSEA.

O Pull Request permite que os responsáveis pelo projeto revisem o código, façam comentários, solicitem ajustes e aprovem a integração das alterações.

Esse fluxo é adequado para colaboradores externos ou para contribuições pontuais. Porém, para uma equipe interna trabalhando continuamente no mesmo projeto, branches no repositório oficial costumam ser mais simples de acompanhar.

## 2. Desenvolvimento por branches (mais recomendado)

Quando o colaborador possui permissão de escrita no repositório do LabSEA, a forma recomendada é criar uma branch para cada funcionalidade, correção ou experimento.

A branch `main` deve representar a versão mais estável do projeto. Por isso, o desenvolvimento não deve ser feito diretamente nela.

Exemplo:

```bash
git checkout main
git pull origin main
git checkout -b feature/create-engine
```

O colaborador pode desenvolver e testar livremente nessa branch. Ao terminar, envia a branch para o GitHub:

```bash
git push origin feature/create-engine
```

Depois disso, deve ser aberto um Pull Request da branch para a `main`.

O Pull Request serve para:

- revisar o código;
- discutir decisões técnicas;
- verificar testes e documentação;
- solicitar correções;
- registrar quem participou da alteração;
- aprovar a integração com a versão estável.

Sempre que possível, o ideal é que outro integrante revise e aprove o Pull Request. Dependendo das permissões do projeto, o próprio autor pode realizar o merge, mas a revisão por outra pessoa ajuda a manter a qualidade e a segurança do código.

Fluxo resumido:

```text
main estável
    ↓
criação de uma branch
    ↓
desenvolvimento e testes
    ↓
Pull Request
    ↓
revisão
    ↓
merge na main
```

Esse é um fluxo utilizado em equipes profissionais e ajuda os integrantes a desenvolverem boas práticas para futuros projetos, estágios e oportunidades de trabalho.


## Boas práticas

- Mantenha a `main` estável.
- Crie uma branch para cada tarefa.
- Use nomes descritivos, como `feature/navegacao-aruco` ou `fix/correcao-lidar`.
- Faça commits pequenos e objetivos.
- Explique claramente o que foi alterado no Pull Request.
- Atualize a documentação quando necessário.
- Teste as alterações antes de solicitar o merge.
- Preserve os créditos de autores, orientadores, bolsistas e colaboradores.
<!-- - Defina a licença e a origem do projeto antes de publicar o código. -->

## Resumo

O fork é uma boa opção para contribuições externas e também pode ser usado para vincular à organização um projeto que começou em um repositório pessoal.

Para o desenvolvimento cotidiano dos projetos mantidos diretamente pelo LabSEA, o fluxo recomendado é criar branches, abrir Pull Requests e manter a `main` como a versão estável do código.

O mais importante é que o histórico do projeto, a autoria e as responsabilidades fiquem claros para todos os envolvidos.
