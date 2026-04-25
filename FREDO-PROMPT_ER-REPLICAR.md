# Prompt para replicar o teleprompter no Cursor

Copie o bloco abaixo (tudo entre as linhas `---`) e cole em um **novo chat do Cursor** na pasta do projeto onde quiser gerar o arquivo. Uma pasta vazia ou um projeto novo serve.

---

## Prompt (copiar daqui)

Crie um **teleprompter como site estático** em um único arquivo `index.html` (HTML + CSS + JavaScript, sem frameworks e sem servidor obrigatório — deve abrir com duplo clique no navegador).

### Objetivo de uso

- Uso em **apresentações em vídeo**: o texto deve ficar na **parte superior da tela** (~22% da altura com uma linha guia horizontal discreta), para quem lê parecer estar olhando para a **câmera** em laptops com webcam no topo.
- Pode ficar em **janela separada** do restante do trabalho (segunda janela do navegador).

### Tela inicial (configuração)

- Título e texto de ajuda em **português (pt-BR)**.
- **Área grande para colar o roteiro** (textarea).
- **Velocidade de rolagem**: campo numérico **digitável** (não slider), rótulo tipo “Velocidade de rolagem (px/s)”, valores inteiros entre **5** e **120**, padrão **40**. Unidade: pixels por segundo.
- **Tamanho do texto**: campo numérico **digitável**, entre **16** e **56** px, padrão **28**.
- Botão **Iniciar teleprompter** (só faz sentido se houver texto; se vazio, focar no textarea).
- Se o usuário deixar número inválido ou vazio nos campos, ao sair do campo (**change**), restaurar o **último valor válido**.

### Modo teleprompter (tela cheia da página)

- Fundo escuro, texto claro, texto **centralizado horizontalmente**, margens laterais confortáveis (ex.: padding horizontal em vw).
- **Rolagem automática** para cima: o conteúdo se move com `requestAnimationFrame` e velocidade em **px/s**.
- **Linha de leitura** horizontal na altura **~22%** do viewport (cor suave, sem atrapalhar a leitura).
- **Padding superior** no bloco de texto para que a **primeira linha** comece alinhada à zona da linha de leitura; **padding inferior** grande para o final do texto não “cortar” seco.
- **Limite do fim da rolagem**: quando o texto acabar, não ultrapassar o fim do conteúdo (cálculo com `offsetHeight` e altura da janela).
- **Barra de controles** fixa na parte inferior (HUD): botões **Pausar / Continuar**, **Voltar ao início**, **Editar texto** (volta à tela inicial sem perder o texto colado).
- No HUD: **mesmo campo numérico de velocidade** (px/s), sincronizado com a tela inicial.
- **Teclado** (com o teleprompter ativo): **Espaço** pausa/continua; **+** e **-** ajustam a velocidade em passos de **5** (respeitando min/max).
- **Redimensionar a janela**: recalcular padding da linha de leitura e limites de rolagem sem quebrar a posição de forma estranha.

### Implementação

- Um arquivo só: `index.html`.
- `lang="pt-BR"`, meta viewport, estilos coerentes (campos com foco visível, botão primário destacado).
- Campos numéricos: `type="number"` com `inputmode="numeric"`; pode esconder os spinners nativos via CSS para parecer mais “caixa de texto”.
- Texto do roteiro: quebrar por linhas (`\n`) em parágrafos; preservar linhas vazias de forma razoável.

Gere o `index.html` completo e funcional.

---

## Prompt (copiar até aqui)

### Como usar em outro terminal / máquina

1. Abra uma pasta no Cursor (nova ou existente).
2. Cole o prompt acima no chat do agente e peça para criar o arquivo (por exemplo: “Implemente isso criando `index.html` na raiz”).
3. Abra `index.html` no navegador (duplo clique ou “Open with Live Server”, se usar extensão).

Não é necessário Node, npm nem conta em serviço externo para usar o teleprompter.
