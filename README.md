# ask-me-anything

## Preparando ambiente 

### Instalando Go

A forma mais recomendada de obter o executável `go` utilizado para criar, executar e gerenciar projetos na linguagem é através do instalador oficial da linguagem ou do binário pré-compilado para seu sistema operacional

Caso Você ja tenha a ferramenta `go` disponível no seu terminal, confira se a versão é >=1.21.
Isso pode ser feito rodando o comando `go version`.

Você terá uma saída no seu prompt como esta:

```bash
$ go version
go version go1.22.2 darwin/arm64
```

Caso a versão da sua ferramenta `go` seja menor que a versão 1.21 Siga para a etapa de instalação de acordo com o site oficial da ferramenta `Go` https://go.dev/dl/.


### Configurando o VSCode para Go!

Manual de instalação do VSCode: https://code.visualstudio.com/docs/setup/setup-overview

Para a melhor experiência de desenvolvimento na linguagem recomendamos que você utilize as seguintes extensões do VSCode e siga o passo-a-passo abaixo:

1. Comece instalando a extensão oficial de Go: 
Esta é a extensão oficial do Go para VSCode. Ela oferece funcionalidades como linting, auto-complete, debugging, formatação de código, gerenciamento de pacotes, entre outros
[Go - Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=golang.go)
    
    [Screen Recording 2024-07-05 at 16.13.10.mov](https://prod-files-secure.s3.us-west-2.amazonaws.com/08f749ff-d06d-49a8-a488-9846e081b224/68dccbe4-83b3-49f4-8a85-b7e6d8a2e358/Screen_Recording_2024-07-05_at_16.13.10.mov)
    
2. Instale agora a extensão Error Lens:
    
    Melhora a visibilidade de erros e avisos no código diretamente na linha correspondente dentro do editor, destacando-os de forma clara.
    [Error Lens - Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=usernamehw.errorlens)
    
    [Screen Recording 2024-07-05 at 16.15.03.mov](https://prod-files-secure.s3.us-west-2.amazonaws.com/08f749ff-d06d-49a8-a488-9846e081b224/e3189400-4d43-4108-b68c-288175aa00ef/Screen_Recording_2024-07-05_at_16.15.03.mov)
    

Agora que as extensões principais estão instaladas, é hora de configurar a extensão Go para ativar todas as suas funcionalidades.

A extensão Go requer algumas ferramentas adicionais para funcionar corretamente. Para abrir o menu necessário, use o atalho `Ctrl+Shift+P` no Windows/Linux e `CMD+Shift+P` no macOS.

### Instalando Docker e Docker Compose

**Instalação do Docker e Docker Compose**

#### Instalação

A forma mais fácil e recomendada de obter o Docker é instalar o Docker Desktop. O Docker Desktop inclui o Docker Compose juntamente com o Docker Engine e Docker CLI, que são pré-requisitos do Compose.

O Docker Desktop está disponível em:

- [Linux](https://docs.docker.com/desktop/install/linux-install/)
- [Mac](https://docs.docker.com/desktop/install/mac-install/)
- [Windows](https://docs.docker.com/desktop/install/windows-install/)

Se você já instalou o Docker Desktop, pode verificar qual versão do Compose possui selecionando "Sobre o Docker Desktop" no menu do Docker, o menu do ícone da baleia.

Se você já tiver o Docker Engine e o Docker CLI instalados, pode instalar o plugin Compose a partir da linha de comando, de duas maneiras:

- [Usando o repositório do Docker](https://docs.docker.com/compose/install/linux/#install-using-the-repository)
- [Fazendo o download e instalação manualmente](https://docs.docker.com/compose/install/linux/#install-the-plugin-manually)

##### Linux

1. Baixe o pacote correto para a sua distribuição Linux e instale-o usando o gerenciador de pacotes correspondente.
    - [Install on Debian](https://docs.docker.com/desktop/install/debian/)
    - [Install on Fedora](https://docs.docker.com/desktop/install/fedora/)
    - [Install on Ubuntu](https://docs.docker.com/desktop/install/ubuntu/)
    - [Install on Arch](https://docs.docker.com/desktop/install/archlinux/)
2. Abra o seu menu de Applications no ambiente de trabalho procure por Docker Desktop.

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/08f749ff-d06d-49a8-a488-9846e081b224/578ba4dd-b43a-4d93-a10b-bc85c638cd2f/Untitled.png)

1. Selecione Docker Desktop para iniciar o Docker.
O menu do Docker (menu da baleia) exibe o Acordo de Serviço de Assinatura do Docker.
2. Selecione Aceitar para continuar. O Docker Desktop iniciará após você aceitar os termos.
    
    Observe que o Docker Desktop não será executado se você não concordar com os termos. Você pode optar por aceitar os termos em uma data posterior abrindo o Docker Desktop.
    

Para mais dúvidas, acesse: https://docs.docker.com/desktop/install/linux-install/

##### Windows

1. Verifique se o seu sistema está com a virtualização ativada: https://docs.docker.com/desktop/troubleshoot/topics/#virtualization
2. Faça o download do instalador na página: https://docs.docker.com/desktop/install/windows-install/
3. Duplo clique em Docker Desktop Installer.exe para executar o instalador.
4. Quando solicitado, certifique-se de que a opção "Use o WSL 2 em vez do Hyper-V" na página de Configuração está selecionada ou não, dependendo da sua escolha de back-end.
5. Se o seu sistema suportar apenas uma das duas opções, você não poderá selecionar qual backend usar.
6. Siga as instruções no assistente de instalação para autorizar o instalador e prosseguir com a instalação.
7. Quando a instalação for bem-sucedida, selecione Fechar para completar o processo de instalação.

Busque por Docker e selecione Docker Desktop nos resultados da busca.

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/08f749ff-d06d-49a8-a488-9846e081b224/e9f7a565-b5c6-4739-a53e-41716df3fc1a/Untitled.png)

Busque pelo aplicativo Docker.
O menu do Docker (menu da baleia) exibe o Acordo de Serviço de Assinatura do Docker.

Aqui está um resumo dos pontos-chave:

O Docker Desktop é gratuito para pequenas empresas (menos de 250 funcionários E menos de $10 milhões em receita anual), uso pessoal, educação e projetos de código aberto não comerciais.
Caso contrário, é necessário uma assinatura paga para uso profissional.
Assinaturas pagas também são necessárias para entidades governamentais.
As assinaturas Docker Pro, Team e Business incluem o uso comercial do Docker Desktop.
Selecione Aceitar para continuar. O Docker Desktop iniciará após você aceitar os termos.

Observe que o Docker Desktop não será executado se você não concordar com os termos. Você pode optar por aceitar os termos em uma data posterior abrindo o Docker Desktop.
Se tiver dúvidas, acesse: https://docs.docker.com/desktop/install/windows-install/

##### macOS

1. Faça o download na página: https://docs.docker.com/desktop/install/mac-install/
2. Dê um duplo clique no arquivo Docker.dmg para abrir o instalador e, em seguida, arraste o ícone do Docker para a pasta Applications.
3. Dê um duplo clique no Docker.app na pasta Applications para iniciar o Docker.
4. O menu do Docker exibirá o Acordo de Serviço de Assinatura do Docker. Aqui está um resumo dos pontos-chave:
    - O Docker Desktop é gratuito para pequenas empresas (com menos de 250 funcionários E menos de $10 milhões em receita anual), uso pessoal, educação e projetos de código aberto não comerciais.
    - Caso contrário, é necessária uma assinatura paga para uso profissional.
    - Assinaturas pagas também são necessárias para entidades governamentais.
    - As assinaturas Docker Pro, Team e Business incluem o uso comercial do Docker Desktop.
    
    Selecione Aceitar para continuar.
    
5. Observe que o Docker Desktop não será executado se você não concordar com os termos. Você pode optar por aceitar os termos em uma data posterior abrindo o Docker Desktop.
6. No a janela de instalação, selecione uma das opções:
    - Use as configurações recomendadas (Requer senha). Isso permite que o Docker Desktop defina automaticamente as configurações necessárias.
    - Use configurações avançadas. Você poderá então configurar o local das ferramentas CLI do Docker no diretório do sistema ou do usuário, habilitar o socket padrão do Docker e permitir mapeamento de porta privilegiada. Consulte as Configurações para mais informações e como definir o local das ferramentas CLI do Docker.
7. Selecione Concluir. Se você aplicou alguma das configurações acima que exijam uma senha no passo 5, insira sua senha para confirmar sua escolha.