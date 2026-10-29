# VERIFICADOR-DE-QUEBRAS-DE-LINHA
Validador de arquivos posicionais em HTML, com detecção de linhas suspeitas, verificação de largura dos registros e visualização do contexto das ocorrências.
# Verificador de Quebras de Linha

Aplicação web desenvolvida em **HTML, CSS e JavaScript**, destinada à análise de arquivos de integração com dados posicionais. Permite identificar linhas potencialmente problemáticas, verificar inconsistências estruturais e visualizar o contexto de cada ocorrência.

O projeto funciona diretamente no navegador, sem necessidade de instalação, servidor ou dependências externas.

## Funcionalidades

- **Análise de arquivos posicionais:** permite colar o conteúdo de arquivos de integração diretamente na interface.
- **Detecção de indentação inesperada:** identifica linhas que apresentam espaços ou tabulações no início em posições diferentes das esperadas.
- **Verificação de largura dos registros:** identifica linhas com quantidades de caracteres diferentes das demais.
- **Identificação de linhas vazias:** detecta linhas vazias localizadas entre registros com conteúdo.
- **Detecção de possíveis truncamentos:** identifica linhas que podem ter sido cortadas ou apresentar estrutura inconsistente.
- **Verificação de caracteres suspeitos:** procura caracteres de substituição, caracteres de controle e ocorrências de `CR` isolado.
- **Visualização da ocorrência:** apresenta o número e o conteúdo integral da linha identificada.
- **Visualização do contexto:** exibe até três linhas anteriores e três posteriores à ocorrência, destacando a linha analisada.
- **Navegação entre ocorrências:** permite avançar e retroceder pelos problemas encontrados.
- **Critérios configuráveis:** permite ativar ou desativar individualmente os cinco critérios de validação.
- **Interface responsiva:** adapta a disposição dos elementos a diferentes tamanhos de tela.

## Interface

A interface utiliza fundo vermelho, cabeçalho em destaque, molduras azul-violeta e áreas internas brancas.

A organização é dividida em três áreas principais:

1. **Entrada dos dados posicionais:** área para colar o conteúdo do arquivo e configurar os critérios de análise.
2. **Linha identificada:** exibe o conteúdo e a numeração da ocorrência selecionada.
3. **Contexto da ocorrência:** apresenta a linha problemática e as linhas vizinhas, mantendo a numeração original.

## Como utilizar

1. Baixe ou clone este repositório.
2. Abra o arquivo HTML diretamente em um navegador moderno.
3. Cole o conteúdo do arquivo de integração na área de entrada.
4. Selecione os critérios de validação desejados.
5. Clique em **Analisar** para executar a verificação.
6. Consulte a linha identificada e seu contexto nas áreas de resultado.
7. Utilize os controles **Anterior** e **Próxima** para navegar entre as ocorrências.
8. Clique em **Limpar** para remover o conteúdo e reiniciar a análise.

## Atalhos de teclado

| Atalho | Ação |
|---|---|
| `Ctrl + Enter` | Executar a análise |
| `F3` | Avançar para a próxima ocorrência |
| `Shift + F3` | Voltar para a ocorrência anterior |
| `Ctrl + N` | Avançar para a próxima ocorrência |
| `Ctrl + Shift + N` | Voltar para a ocorrência anterior |

## Tecnologias utilizadas

- **HTML5:** estrutura da aplicação.
- **CSS3:** layout, cores, responsividade e estilos visuais.
- **JavaScript:** análise do conteúdo, identificação de ocorrências, renderização dos resultados e navegação.

Todo o código está concentrado em um único arquivo HTML, sem necessidade de frameworks ou bibliotecas externas.

## Execução e compatibilidade

A aplicação pode ser executada localmente, abrindo o arquivo HTML em um navegador moderno. A análise do texto é realizada no próprio navegador, sem necessidade de enviar o conteúdo para um servidor.

A interface foi projetada para funcionar em computadores e dispositivos com telas menores.

## Limitações

Os critérios implementados utilizam heurísticas para identificar possíveis inconsistências. Portanto, uma ocorrência sinalizada não representa necessariamente um erro no arquivo.

A verificação de largura fixa compara o comprimento das linhas com o da primeira linha não vazia. A detecção de truncamentos também utiliza padrões heurísticos. Para validar integralmente um layout posicional específico, é necessário conhecer as regras formais do arquivo, como o tamanho esperado de cada registro e a estrutura de seus campos.

O programa não deve ser considerado um validador definitivo de qualquer formato de integração sem a configuração ou adaptação dessas regras.
