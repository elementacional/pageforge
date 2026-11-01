# PageForge Studio

**Versão:** 1.2  
**Idioma:** Português (Brasil)  
**Plataforma:** Navegadores modernos de desktop  
**Tipo:** Aplicativo local em arquivo HTML, sem instalação

## Visão geral

O **PageForge Studio** é um aplicativo para organizar e unir imagens de páginas digitalizadas de livros e documentos. Permite importar arquivos por arrastar e soltar, conferir a sequência, reorganizar páginas e exportar o resultado em imagem única ou PDF com páginas de tamanho padronizado.

O processamento ocorre no navegador do próprio computador. Não exige cadastro nem envio dos arquivos a um servidor.

## Requisitos

- Computador com navegador moderno, como Google Chrome ou Microsoft Edge.
- Arquivo `PageForge_Studio_v1.2.html` salvo no computador.
- Memória disponível compatível com a quantidade e a resolução das imagens.

Não é necessária instalação de dependências nem conexão à internet para as funções locais do arquivo HTML.

## Como iniciar

1. Baixe e salve `PageForge_Studio_v1.2.html`.
2. Dê um duplo clique no arquivo ou abra-o no navegador.
3. Arraste as imagens para a área de upload ou clique nela para selecionar arquivos.
4. Confira a lista e ajuste a ordem conforme necessário.
5. Escolha o formato e as opções de composição.
6. Clique em **Exportar composição** para salvar o resultado.

## Formatos de entrada

- **JPG/JPEG**
- **PNG**
- **WEBP**
- **BMP**
- **SVG**
- **TIFF/TIF:** suporte a variantes comuns; determinadas compressões, profundidades de cor e organizações do arquivo podem ser incompatíveis.

A leitura de alguns tipos depende também das capacidades do navegador.

## Organização das imagens

Ao importar arquivos, o aplicativo apresenta uma **ordem alfabética inicial**. É possível:

- Arrastar os itens pelo ícone de movimentação para personalizar a sequência.
- Usar **A → Z** para ordenar novamente.
- Usar **Inverter** para reverter a ordem atual.
- Remover imagens individualmente ou usar **Limpar** para começar outra sequência.

A exportação respeita a ordem exibida na lista.

## Modos de composição

| Modo | Resultado |
| --- | --- |
| Sequência vertical | Une as imagens de cima para baixo em uma imagem única. |
| Sequência horizontal | Une as imagens lado a lado em uma imagem única. |
| Uma imagem por página em PDF | Cria um PDF multipáginas, seguindo a ordem da lista. |

## Formatos de saída

| Formato | Características |
| --- | --- |
| **PNG** | Imagem única; compressão sem perda. |
| **JPG/JPEG** | Imagem única; qualidade ajustável, com compressão com perda. |
| **WEBP** | Imagem única; qualidade ajustável e arquivo geralmente mais compacto. |
| **PDF** | Um documento multipáginas, com uma imagem por página e tamanho uniforme de página. |

**Importante:** a saída PDF reúne imagens. Não aplica OCR e não transforma o texto digitalizado em texto pesquisável ou editável.

## Padronização das páginas do PDF (corrigida na versão 1.2)

Na exportação para PDF, **todas as páginas recebem o mesmo tamanho físico**, mesmo que os arquivos originais tenham dimensões diferentes. A imagem é ajustada proporcionalmente à área disponível e centralizada, sem ser deformada.

**Tamanhos de página disponíveis:**

- A4 — 210 × 297 mm
- A5 — 148 × 210 mm
- Carta — aproximadamente 216 × 279 mm
- Ofício — aproximadamente 216 × 356 mm
- Igual à maior imagem (com proporção definida pela primeira imagem)

**Margens configuráveis:** 0, 5, 10, 15 ou 20 mm.

Se as imagens tiverem proporções distintas, poderão aparecer áreas em branco; isso é esperado para **preservar a imagem inteira sem cortes**.

A opção **Uniformizar largura/altura** é destinada à composição em JPG/PNG/WEBP, e não substitui a escolha do tamanho de página do PDF.

## Resolução e qualidade

O aplicativo permite selecionar escalas de **100%, 150%, 200%, 300%**, além de escala personalizada entre **25% e 400%**. Para JPG e WEBP, a qualidade de compressão é configurável.

A classificação de qualidade exibida pelo aplicativo é **indicativa**, com base nas dimensões da imagem. Aumentar a escala amplia o arquivo de saída, mas **não recupera detalhes ausentes no original**. Para melhores resultados, utilize imagens de origem nítidas e com boa resolução.

## Configuração sugerida para páginas digitalizadas

Para gerar um documento com páginas homogêneas:

1. Importe as imagens e ajuste a ordem.
2. Escolha **Uma imagem por página em PDF**.
3. Selecione **PDF** como formato.
4. Defina **A4** (ou o tamanho real pretendido).
5. Ajuste as margens para **5 mm**, conforme necessário.
6. Escolha a escala de saída considerando nitidez, tamanho do arquivo e memória disponível.
7. Confira a prévia e exporte.

A pré-visualização do PDF mostra a **primeira página**; confira o documento final para verificar o enquadramento das demais.

## Privacidade e funcionamento local

Os arquivos são processados no próprio navegador e o resultado é salvo por download local. O aplicativo não solicita conta nem contém uma rotina de upload dos documentos para um serviço remoto.

## Limitações conhecidas

- **TIFF:** algumas variantes não são compatíveis.
- **Memória e tamanho:** conjuntos muito grandes ou resoluções extremas podem exceder os limites de canvas/memória do navegador; reduza a escala ou divida o lote.
- **PDF:** as imagens são incorporadas como páginas rasterizadas; não há OCR.
- **Enquadramento:** proporções diferentes geram margens visuais diferentes dentro da página fixa; o conteúdo não é cortado intencionalmente.
- **Prévia:** no modo PDF, é exibida uma prévia da primeira página, não de todas.
- **Tratamento de imagem:** a versão 1.2 não oferece correção automática de perspectiva, remoção automática de bordas ou alinhamento por OCR.

## Solução de problemas

**As páginas do PDF saíram com tamanhos diferentes.**  
Confirme que está usando a versão **1.2** e que selecionou **PDF** com formato de página fixo, por exemplo, A4. Se o problema for somente o tamanho visual do conteúdo, isso ocorre porque a proporção das imagens originais é diferente: a página A4 continua com tamanho fixo.

**Uma imagem TIFF não abriu.**  
Converta-a previamente para PNG ou JPG e importe novamente.

**A exportação falhou ou o navegador ficou lento.**  
Diminua a escala, reduza o número de imagens por lote ou exporte em PDF paginado em vez de gerar uma imagem única muito longa.

**A qualidade não melhorou ao selecionar 300%.**  
A escala amplia dimensões em pixels; ela não substitui uma digitalização de alta qualidade.

## Histórico de versões

| Versão | Principais recursos |
| --- | --- |
| 1.0 | Importação, ordenação, composição, prévia e exportação. |
| 1.1 | Opção PDF destacada entre os formatos de exportação. |
| **1.2** | **Correção da padronização do tamanho físico das páginas PDF**, seleção de papel e margens. |

## Arquivo do aplicativo

`PageForge_Studio_v1.2.html`

O aplicativo é distribuído como um único arquivo HTML. Este README descreve os recursos e as limitações identificáveis na versão 1.2; não constitui certificação de testes completos em todos os navegadores e formatos.
