# Gerador de Carrossel (protótipo)

> **CONTEÚDO DE EXEMPLO — revisar.** Os textos que aparecem entre [colchetes] são guias para você escrever. Não são conteúdo pronto nem informação técnica.

Abra `gerador-carrossel.html` com dois cliques. Funciona offline: as fontes estão embutidas no arquivo.

1. Preencha **Tema**, **Certificação** (CPA, C-Pro R, C-Pro I), **Nº de slides** (5 a 10) e o **Perfil** (vem `@gparreiraaa`).
2. **Preencher estrutura** monta gancho → problema → conceito → exemplo → pegadinha de prova → resumo → CTA. Com 5 ou 6 slides, o resumo e o exemplo saem primeiro. Com 8 a 10, entram slides de "conteúdo extra".
3. Edite o título e o texto de cada slide no painel da esquerda. No texto, cada linha que começa com `- ` vira um item com marcador.
4. Visual: 3 paletas prontas, cores livres (fundo, texto, destaque) e tamanho da fonte entre 80% e 130%. Se o texto não couber, a fonte daquele slide diminui sozinha e aparece um aviso.
5. Exportar: **Baixar PNG deste slide**, **Baixar todos (PNGs)** ou **Baixar .zip** com todos os slides. Cada PNG sai em 1080×1350.

O trabalho fica salvo no próprio navegador (localStorage).

Para mudar a estrutura, os textos-guia ou as paletas, edite o bloco `<script id="modelo-carrossel" type="application/json">` no começo do HTML.

`src/index.html` é o código-fonte sem as fontes embutidas. O `../build.py` gera o HTML final.

## Textos com IA (a partir do título)

1. Abra **Configurar IA**, escolha o provedor (xAI/Grok, OpenAI, Anthropic/Claude ou Google Gemini), confira o modelo e cole a sua chave de API. Clique em **Salvar chave**.
2. Escreva o título, escolha certificação e nº de slides e clique em **Gerar textos com IA a partir do título**.
3. Escolha uma das **3 opções de gancho**. Use **↻ refazer** num slide para pedir outro texto só para ele, sem mexer nos outros.
4. Confira tudo o que ficou **em vermelho** (números, %, R$, anos, Lei, Resolução, Instrução, CVM, Bacen, art. e `[DADO A CONFERIR]`). Depois marque **Conferi os dados deste carrossel**. Sem essa marca, a exportação pede confirmação.

A IA segue um roteiro fixo: tom técnico ANBIMA e didático, estrutura gancho → problema → conceito → exemplo → pegadinha de prova → CTA, textos curtos, nenhuma menção a FGV ou a certificações descontinuadas. Ela não deve escrever números, leis ou normas que não estejam no seu título; no lugar, aparece `[DADO A CONFERIR]`. Mesmo assim, **a IA pode errar: revise antes de publicar.**

Sem chave, o botão **Preencher estrutura** continua funcionando como antes, offline.

### Onde fica a chave e quais são os riscos
- A chave fica **só no navegador em que você colou** (localStorage), separada por provedor. Ela **não está** neste repositório, no HTML, no .zip nem nos PNGs. O navegador manda a chave direto para o provedor escolhido.
- Quem usar o mesmo navegador/perfil, ou uma extensão com acesso à página, pode ler a chave.
- Use uma chave criada só para isto, com **limite de gasto** no painel do provedor. Em computador compartilhado, clique em **Esquecer chave** ao terminar. Se suspeitar de vazamento, revogue a chave no painel do provedor.
- Cada geração é cobrada pelo provedor na sua conta.

## Limitações
- Não tem imagem nem foto no slide, só texto e formas.
- Não tem negrito ou destaque dentro do parágrafo.
- "Baixar todos" dispara vários downloads seguidos, e o navegador pode pedir permissão. Se isso incomodar, use o .zip.
