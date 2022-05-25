A criação de branches e commits seguem seus respectivos padrões, mas para explicá-los melhor precisamos primeiro entender os tipos.

## Types

- **CHORE:**  Mudanças de ferramentas, mudanças de configuração e bibliotecas.
    - ***Exemplo:***
        - *Tudo que alterar o package.json*
        - *Adicionar o commitlint e o husky ao projeto.*
        - *Adicionar o eslint ao projeto.*
        - *Dependências de desenvolvimento.*
        - *Alterar o arquivo de configurações de arquivos de teste (Jest, Jasmin...).*
    
- **FEAT:** Para adicionar novas funcionalidades e/ou recursos ao projeto. Assim como adicionar alterações e melhorias.
    - ***Exemplo:***
        - *Criar um novo componente.*
            - *Criar o componente de formulário.*
        - *Criar uma nova funcionalidade.*
            - *Criar um serviço de scroll suave.*
            - *Criar um serviço de tradução da página.*
        - *Adicionar melhorias de design ou recursos.*

- **FIX:** Tudo que não segue o que foi predefinido e necessita de correção.
    - ***Exemplo:***
        - *Corrigir uma margem que não está com o tamanho correto no componente exibido na tela.*
        - *Corrigir um erro de responsividade.*
        - *Alinhar corretamente o elemento na tela.*
        - *Adicionar um padding que faltava ao componente.*
        - *Ajustar a cor que não está correta em um componente.*
        - *Corrigir o bug do scroll que não faz a rolagem para o elemento correto.*
        - *Corrigir o bug da lambda que não envia o email para o destinatário correto.*
        
- **REFACTOR:** Para qualquer mudança de código que não altere a funcionalidade final desse código que sofreu refatoração.
    - ***Exemplo:***
        - *Retirar o acoplamento de um serviço.*
        - *Remover as mil linhas de if/else por uma lógica melhor.*
        - *Apagar código que não está sendo utilizado.*
        - *Mudança de nome de variáveis.*
    
- **DOCS:** Inclusão ou alteração somente de arquivos de documentação.
    - ***Exemplo:***
        - *Criação ou edição do README.*
        
- **PERF:** Para alterações de código que melhoram o desempenho.
    - ***Exemplo:***
        - *Remover bibliotecas que reduzem o desempenho do site.*
        - *Adicionar um arquivo de robots.txt ao projeto.*

- **TEST:** Adicionar testes ausentes, corrigir ou apagar testes.
    - ***Exemplo:***
        - *Criação de testes de integração, testes unitários...*
        
- **DEVOPS:** Mexer com CI/CD.
- *Exemplos:*
    - *CodeBuild*
    - *CloudFormation*
    - *CircleCI*
    
- **MERGE:** Para descrever correções de conflitos ao fazer o merge.

- **ENV:** Alteração realizadas nas variáveis de ambiente.

## Branch

> A branch deve ser criada informando o tipo e o nome do recurso que será afetado ou criado.
> 
> 
> 
> **Padrão:** `[JIRA-TASK-ID]` 
> 
> - *Exemplos:*
>     - [ST-92]
>     - [ST-145]
>     - [ST-2627]
>     

## Commits

> Os commits devem ser criados passando o tipo, o código da task do jira e uma breve mensagem descrevendo o commit.
> 
> 
> 
> **Padrão:** `TYPE(scope): [ST-XX] message`
> 
> - O `TYPE` corresponde aos tipos apresentados no início do tópico de Branches e Commits.
> - O `scope` serve para indicar um contexto para o commit **(OPCIONAL).**
>     - Digamos que você tem um projeto muito grande e realizou a alteração, ou incremento, de alguma funcionalidade em alguma feature. Tendo em vista isso, você pode colocar o escopo para especificar onde as mudanças estão sendo realizadas.
>     - O escopo deve ser escrio em letras minúsculas e deve fazer referências aos locais do projeto que a modificação, ou a criação, de algum recurso afeta ou atua.
>         - *Exemplos:*
>             - *Digamos que vc está criando um card que será utilizado na página home `FEAT(home): create photo card`.*
>             - *Digamos que você está criando o serviço de scroll que permite o redirecionamento da página para o `/home` e, assim que o usuário clicar* no link que está no menu, *a tela irá rolar para um determinado componente da página home que está sendo exibido para o usuário*.
>                 - `FEAT(menu/home) create scroll`
>                 - *O menu será o local responsável por chamar o serviço de scroll, por exemplo e a home é o local para o qual o serviço redireciona e faz a rolagem da tela.*
>                 - *Os locais podem ser separador por `/`*
> - O `[ST-XX]` corresponde ao código da task no jira.
>     - No caso do projeto, todas as tasks começam com `ST-` e possuem alguma numeração após as letras.
> 
> - **Exemplo:**
>     - **FEAT:** **[ST-135]** ***create home component***
>     - **FEAT(lang):** **[ST-128]** ***add portuguese language***
