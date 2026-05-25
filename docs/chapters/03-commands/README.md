# Comandos

O ecossistema Go provê uma ferramenta unificada de linha de comando, referenciada simplesmente como `go`, que atua como o núcleo para a gestão do ciclo de vida do desenvolvimento. Por meio dessa interface, realizam-se tarefas que englobam desde a formatação do código até a compilação final e a execução de testes automatizados.

Para o propósito educacional desta obra, o escopo restringe-se aos comandos fundamentais para o fluxo de trabalho inicial de um desenvolvedor. Ferramentas avançadas ou de uso específico em automações complexas não serão detalhadas, permitindo maior foco na consolidação das práticas diárias de programação.

A sintaxe geral para a execução de qualquer operação segue a padronização abaixo:

```bash
go <comando> [argumentos]
```

## Entendendo a Sintaxe: Comandos e Argumentos

Para a correta utilização da ferramenta, é fundamental compreender a distinção entre os elementos que compõem a instrução:

- `<comando>`: Representa a ação mandatória que a ferramenta Go deve executar. Exemplos são os que serão citados a seguir no módulo.
- `[argumentos]`: Representam os dados adicionais fornecidos para direcionar ou modificar a execução do comando. Os colchetes indicam que a sua presença é opcional ou variável, a depender do comando utilizado.

Os argumentos dividem-se geralmente em duas categorias práticas:

- **Alvos da Ação**: Indicam o arquivo ou pacote sobre o qual o comando operará. No comando `go run main.go`, por exemplo, o termo `main.go` é o argumento que específica qual arquivo deve ser compilado e executado.
- **Sinalizadores (_Flags_)**: São modificadores que alteram o comportamento padrão do comando, geralmente antecedidos por um ou dois hifens. No comando `go test -v`, o argumento `-v` (_verbose_) instrui a ferramenta a exibir o relatório detalhado de cada teste executado, em vez de apenas o resumo final.

## Comandos Principais de Desenvolvimento

Os itens listados a seguir constituem a base operacional do desenvolvimento em Go e serão observados com maior frequência na construção de aplicações.

- `run` **(Compilação e Execução Temporal)**: Realiza a compilação dos arquivos de código-fonte diretamente na memória e executa o binário resultante imediatamente. É utilizado primordialmente durante a fase de desenvolvimento e testes rápidos, pois não gera um arquivo executável permanente no diretório de trabalho.
- `build` **(Compilação de Pacotes)**: Compila os pacotes e as dependências do projeto, gerando um arquivo binário executável pronto para distribuição. Diferente do comando run, o build salva o resultado diretamente no disco rígido.
- `fmt` **(Formatação de Código-Fonte)**: Executa a ferramenta utilitária gofmt, responsável por reformatar automaticamente o estilo do código de acordo com os padrões estritos estabelecidos pela comunidade Go. Garante a uniformidade visual do código-fonte sem a necessidade de intervenção manual do programador.
- `test` **(Execução de Testes Automatizados)**: Automatiza o processo de testes do sistema, localizando e executando funções específicas de teste contidas nos pacotes para garantir a integridade das regras de negócio implementadas.
- `mod` **(Manutenção de Módulos)**: Provê o acesso às ferramentas de gerenciamento de dependências, criação e organização dos arquivos go.mod, fundamentais para o controle de versões de bibliotecas utilizadas no projeto.
- `vet` **(Análise Estática de Código)**: Examina o código-fonte em busca de erros potenciais ou construções suspeitas que, embora permitidas pelo compilador, podem resultar em comportamentos inesperados durante a execução.

## Comandos Complementares de Suporte

Para além do fluxo principal, a ferramenta disponibiliza comandos utilitários voltados à manutenção do ambiente de desenvolvimento e consulta de metadados.

- `get` **(Adição de Dependências)**: Responsável por localizar, baixar e instalar dependências externas ao módulo atual, integrando-as ao arquivo de controle de pacotes.
- `install` **(Instalação de Binários)**: Compila e instala pacotes e suas respectivas dependências diretamente no diretório de binários do sistema Go, tornando o programa disponível globalmente na máquina.
- `doc` **(Consulta de Documentação)**: Extrai e exibe diretamente no terminal a documentação de referência para pacotes, funções ou símbolos específicos, reduzindo a necessidade de consultas externas à internet.
- `env` **(Informações de Ambiente)**: Exibe as variáveis de configuração internas que orientam o comportamento do compilador e das ferramentas do Go no sistema operacional.
- `clean` **(Limpeza de Artefatos)**: Remove arquivos-objeto gerados temporariamente e limpa os caches criados por compilações anteriores, liberando espaço em disco e garantindo compilações limpas quando necessário.

## Referências

* [Comandos](https://pkg.go.dev/cmd/gol) – Documentação oficial de Go com os comandos. 
