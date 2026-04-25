# Fredo-Prompter

Teleprompter simples para **apresentações em vídeo**: o texto fica na **parte superior da tela**, para o olhar parecer mais próximo da **câmera** (webcam no topo do laptop).

Tudo roda em **um único arquivo** (`index.html`) — sem Node, sem build e sem conta em serviço externo.

## Como usar

1. Abra o arquivo `index.html` no navegador (duplo clique ou arraste para Chrome / Safari / Firefox).
2. Cole o roteiro na caixa de texto.
3. Ajuste **velocidade** (px/s) e **tamanho do texto** (px) nos campos numéricos.
4. Opcional: defina **Tempo-alvo (mm:ss)**. Se for maior que zero, ao iniciar a **velocidade é calculada** para tentar terminar o texto nesse tempo.
5. Clique em **Iniciar teleprompter**.

### Durante a leitura

- **Espaço**: pausar / continuar  
- **+** e **-**: aumentar ou diminuir a velocidade em passos de 5 px/s  
- **Decorrido** e **Restante**: contadores no rodapé (rest só aparece com tempo-alvo)  
- **Voltar ao início**: reinicia rolagem e o contador decorrido  
- **Editar texto**: volta à tela inicial (o texto colado permanece)

## Abrir pelo caminho do arquivo

No navegador, use um endereço no formato:

`file:///caminho/para/seu/projeto/index.html`

## Dica de janela

Deixe o teleprompter em **uma janela** (ou metade superior da tela) e a chamada de vídeo em outra, para alinhar leitura e câmera.

## Arquivos do repositório

| Arquivo | Descrição |
|--------|-----------|
| `index.html` | App completo (HTML, CSS, JS) |
| `FREDO-PROMPT_ER-REPLICAR.md` | Prompt para replicar o projeto em outro ambiente |
| `.gitignore` | Ignora arquivos locais do macOS (ex.: `.DS_Store`) |

## Licença

Uso interno / projeto de apoio a apresentações. Ajuste a licença conforme a política da sua organização, se for publicar de forma ampla.
