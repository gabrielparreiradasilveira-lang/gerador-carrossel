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

## Limitações
- Não tem imagem nem foto no slide, só texto e formas.
- Não tem negrito ou destaque dentro do parágrafo.
- "Baixar todos" dispara vários downloads seguidos, e o navegador pode pedir permissão. Se isso incomodar, use o .zip.
