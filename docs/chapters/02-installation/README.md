# Instalação

O processo de preparação do ambiente de desenvolvimento visa disponibilizar as ferramentas essenciais para a compilação e execução de programas em Go de forma célere. Para o escopo deste material, o foco restringe-se ao método de instalação rápida e padrão, ideal para quem está iniciando na linguagem.

Dessa forma, os procedimentos detalhados a seguir cobrem a abordagem convencional por meio dos instaladores e pacotes oficiais da plataforma. Não serão abordados tópicos avançados como a compilação da linguagem a partir do código-fonte (_custom build_) ou a utilização de gerenciadores de múltiplas versões do Go (_version managers_). Caso haja necessidade futura de alternar entre diferentes versões do ecossistema ou customizar os binários da linguagem, recomenda-se a consulta à documentação oficial do projeto.

Os passos para a configuração rápida nos principais sistemas operacionais encontram-se descritos na sequência.

## Windows

O processo de instalação no sistema operacional Windows é simplificado por meio do assistente executável fornecido pela plataforma oficial. Os procedimentos para a configuração e validação do ambiente constam a seguir.

1. **Execução do Instalador**: O arquivo com extensão `.msi` baixado deve ser executado. O assistente de instalação guiará o procedimento. Por padrão, os arquivos da linguagem são armazenados no diretório `Program Files` ou `Program Files (x86)`, sendo possível alterar o destino caso necessário. 
2. **Atualização do Terminal**: Após a conclusão da instalação, torna-se obrigatório fechar e reabrir quaisquer janelas de prompt de comando ou terminais ativos. Esta ação assegura que as novas variáveis de ambiente configuradas pelo instalador sejam recarregadas pelo sistema operacional.
3. **Abertura do Prompt de Comando**: Para verificar a integridade da instalação, deve-se acessar o menu Iniciar do Windows, digitar `cmd` no campo de busca e pressionar a tecla Enter para abrir a janela do Prompt de Comando.
4. **Verificação da Versão**: Na linha de comando, deve ser executada a seguinte instrução: 
    ```cmd
    go version
    ```
    A instalação terá sido concluída com sucesso se o terminal retornar o número correspondente à versão do Go que foi instalada.

## Linux

A instalação em ambientes baseados em Linux é realizada via terminal, envolvendo a extração dos binários oficiais e a configuração manual das variáveis de ambiente do sistema.

**Aviso Crítico:** Nunca se deve extrair o arquivo compactado sobre uma instalação preexistente do Go, pois isso gera conflitos e resulta em um ambiente defeituoso. Instalações anteriores contidas em `/usr/local/go` devem ser integralmente removidas antes de qualquer nova extração.

Os procedimentos para a configuração do ambiente seguem a ordem metodológica abaixo:

1. **Remoção e Extração**: Para eliminar resquícios de versões anteriores e implantar os novos arquivos no diretório padrão `/usr/local/go`, executa-se o seguinte comando combinado (utilizando privilégios de administrador via `sudo` se necessário):
    ```bash
    rm -rf /usr/local/go && tar -C /usr/local -xzf go1.26.3.linux-amd64.tar.gz
    ```
2. **Configuração do PATH**: Para garantir que o sistema localize o executável do Go, o caminho `/usr/local/go/bin` deve ser adicionado à variável de ambiente `PATH`. Essa inclusão é feita inserindo a linha abaixo no arquivo de configuração do usuário (`$HOME/.profile`) ou em âmbito global (`/etc/profile`):
    ```bash
    export PATH=$PATH:/usr/local/go/bin
    ```
3. **Atualização da Sessão**: As modificações nos arquivos de perfil normalmente exigem uma nova sessão de usuário para entrar em vigor. Para aplicar as alterações imediatamente na sessão atual do terminal, executa-se a instrução de carregamento:
    ```bash
    source $HOME/.profile
    ```
4. **Validação do Ambiente**: A confirmação do sucesso da instalação é realizada executando o utilitário de versão no terminal:
    ```bash
    go version
    ```
    O ambiente estará pronto para uso quando o terminal exibir corretamente a versão instalada.

## MacOS

O procedimento de instalação no sistema operacional da Apple é automatizado por meio de um pacote oficial, reduzindo a necessidade de configurações manuais complexas. Os passos para a integração da linguagem ao sistema constam a seguir.

1. **Execução do Assistente**: O arquivo de pacote com extensão `.pkg` baixado deve ser executado. O assistente gráfico de instalação guiará todo o procedimento. Por padrão, os arquivos da linguagem são implantados no diretório `/usr/local/go`.
2. **Atualização Automática do PATH**: O próprio instalador do macOS é projetado para realizar a inclusão do diretório `/usr/local/go/bin` à variável de ambiente PATH. Para garantir que o sistema operacional recarregue essa modificação, torna-se necessário reiniciar quaisquer sessões ou janelas ativas do Terminal. 
3. **Abertura do Terminal**: Para realizar o teste de integridade do ambiente, deve-se abrir o aplicativo Terminal nativo do macOS (localizado na pasta de Utilitários).
4. **Verificação da Versão**: Na linha de comando do Terminal, executa-se a instrução de checagem:
    ```bash
    go version
    ```
    O ambiente estará pronto para uso quando o terminal exibir corretamente a versão instalada.
