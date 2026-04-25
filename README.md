# Fredo-Prompter

Teleprompter simples para **apresentações em vídeo**: o texto fica na **parte superior da tela**, para o olhar parecer mais próximo da **câmera** (webcam no topo do laptop).

Tudo roda em **um único arquivo** (`index.html`) — sem Node, sem build e sem conta em serviço externo.

## Abrir na internet (GitHub Pages)

Este repositório pode ser usado pelo endereço público:

**[https://elizignacio.github.io/Fredo-Prompter/](https://elizignacio.github.io/Fredo-Prompter/)**

A primeira publicação pode levar **1 a 2 minutos**. Se a página ainda não abrir, atualize o navegador ou confira em **Settings → Pages** se o *build* terminou sem erro.

### Como ativar GitHub Pages em outro repositório (passo a passo)

1. No GitHub, abra o repositório → **Settings** (Configurações).
2. No menu lateral, clique em **Pages**.
3. Em **Build and deployment** → **Source**, escolha **Deploy from a branch**.
4. Em **Branch**, selecione **`main`** (ou `master`, se for o caso) e pasta **`/ (root)`** → **Save**.
5. O site ficará em `https://SEU_USUARIO.github.io/NOME_DO_REPO/` (o GitHub mostra o link na mesma página de Settings → Pages).

O `index.html` precisa estar na **raiz** do branch escolhido (como neste projeto).

## Como usar

1. Abra o arquivo `index.html` no navegador (duplo clique ou arraste para Chrome / Safari / Firefox), **ou** use o link do GitHub Pages acima.
2. Cole o roteiro na caixa de texto.
3. Ajuste **velocidade** (px/s) e **tamanho do texto** (px) nos campos numéricos.
4. Opcional: defina **Tempo-alvo (mm:ss)**. Se for maior que zero, ao iniciar a **velocidade é calculada** para tentar terminar o texto nesse tempo.
5. Clique em **Iniciar Fredo-Prompter**.

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
