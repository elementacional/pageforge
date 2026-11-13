# PageForge Studio

**Versão 1.6 · Composição, organização e exportação de imagens**

O **PageForge Studio** é um aplicativo web desenvolvido em HTML, CSS e JavaScript para importar, organizar, compor e exportar imagens de páginas de livros, documentos e outros materiais gráficos. Funciona diretamente no navegador, com uma interface escura e compacta, sem exigir instalação, cadastro ou servidor para o processamento dos arquivos locais.

## Funcionalidades

- Importação de múltiplas imagens do computador por seleção ou arrastar e soltar.
- Importação por endereços URL diretos de imagens, com botão **+** para acrescentar campos.
- Organização alfabética inicial, reordenação por arrastar, inversão da ordem e remoção de itens.
- Miniaturas, dimensões, tamanho dos arquivos e indicação aproximada de resolução.
- Pré-visualização antes da exportação.
- Composição vertical, horizontal ou exportação de imagens individuais (modo padrão).
- Geração de PDF com uma imagem por página e dimensões padronizadas.
- Ajuste de resolução (100%, 150%, 200%, 300% ou personalizada de 25% a 400%).
- Opções de fundo branco, normalização de dimensões e espaçamento entre imagens.
- Exportação de várias imagens individuais em um único arquivo ZIP.
- Layout adaptado ao espaço da janela, com rolagem interna nos painéis quando necessário.

## Formatos

### Entrada

São reconhecidas extensões como **JPG/JPEG, PNG, TIFF/TIF, BMP, SVG, WEBP, GIF, AVIF e ICO**, além de algumas variantes. A leitura efetiva depende dos recursos de decodificação do navegador. TIFF possui decodificação local para formatos comuns, mas algumas compressões ou variações não são suportadas. Arquivos HEIC/HEIF também dependem do navegador.

### Saída

| Formato | Uso e observações |
| --- | --- |
| **PNG** (`.png`) | Imagem sem perda na codificação. |
| **JPEG** (`.jpg`) | Imagem compactada com controle de qualidade. |
| **WEBP** (`.webp`) | Formato de imagem otimizado com controle de qualidade. |
| **ICO** (`.ico`) | Ícone com versões de **16, 32, 48, 64, 128 e 256 px** no mesmo arquivo. |
| **SVG** (`.svg`) | Contêiner SVG com a imagem PNG incorporada em Base64; **não vetoriza** automaticamente imagens rasterizadas. |
| **PDF** (`.pdf`) | PDF multipáginas, com uma imagem por página. |

> **Importante:** a extensão correta para ícones do Windows e favicons é `.ico`, não `.icon`.

## Como usar

1. Abra o arquivo `index.html` no navegador.
2. Arraste imagens para a área de importação ou clique para selecionar os arquivos.
3. Opcionalmente, cole uma URL direta de imagem e use **+** para adicionar mais URLs; depois, clique em **Importar imagens das URLs**.
4. Organize as imagens por ordem alfabética, usando o ícone de arraste ou os comandos **A → Z** e **Inverter**.
5. Escolha o **Modo de composição**: imagens individuais, sequência vertical, sequência horizontal ou uma imagem por página em PDF.
6. Selecione o **Formato de exportação**, ajuste a escala e as demais preferências.
7. Confira a prévia e clique em **Exportar composição**.

**Saída individual:** um arquivo de imagem é baixado diretamente; quando houver várias imagens, elas são agrupadas em um `.zip`. Em composições vertical ou horizontal, o resultado é um arquivo de imagem, exceto quando o formato PDF é selecionado.

## Instalação local

Não é necessário executar comandos, instalar pacotes ou configurar um ambiente de desenvolvimento.

```text
PageForge-Studio/
├── index.html
└── README.md
```

Basta abrir `index.html` em um navegador atualizado (como Chrome, Edge ou Firefox). O processamento das imagens locais ocorre no próprio dispositivo.

## Publicação no GitHub Pages

1. Crie um repositório no GitHub.
2. Envie o aplicativo com o nome **`index.html`** e este documento com o nome **`README.md`** para a raiz do repositório.
3. Acesse **Settings → Pages**.
4. Em **Build and deployment**, selecione **Deploy from a branch**.
5. Escolha a branch principal (geralmente `main`) e a pasta **`/ (root)`**; salve.
6. Após a publicação, abra o endereço disponibilizado pelo GitHub Pages.

O aplicativo é estático: não requer backend ou chave de API para suas funções locais.

## Observações e limitações

- **URLs externas:** a importação usa `fetch` e depende de o servidor remoto permitir acesso entre origens (**CORS**). Nem todo link de página ou rede social é um link direto para um arquivo de imagem.
- **SVG:** a exportação gera um documento SVG válido com uma imagem raster incorporada, não um arquivo vetorial editável por caminhos.
- **ICO:** a exportação gera um pacote multirresolução; conteúdos retangulares são ajustados proporcionalmente e centralizados em telas quadradas.
- **PDF:** as imagens são ajustadas para caber nas páginas, mantendo suas proporções. O documento permite os tamanhos A4, A5, Carta, Ofício e um modo baseado nas dimensões das imagens.
- **Nitidez:** ampliar a resolução de exportação não recupera detalhes inexistentes no original.
- **Limites do navegador:** composições muito grandes podem exceder os limites de tamanho ou memória do Canvas; reduza a escala ou prefira a exportação paginada em PDF.
- **Privacidade:** arquivos importados localmente são processados no navegador. A importação por URL consulta o servidor que hospeda a imagem.
- **Uso offline:** os recursos locais funcionam sem conexão após o arquivo HTML estar disponível; a importação por URL requer acesso à internet.

## Tecnologias

- HTML5 e CSS3
- JavaScript sem bibliotecas externas obrigatórias
- Canvas API, File API e Blob API
- Exportação ZIP implementada no próprio código
- Geração de PDF diretamente no navegador

## Histórico resumido

- **v1.5:** inclusão da importação de imagens por múltiplas URLs, com campos adicionais sob demanda, modo individual padrão e ajustes de layout.
- **v1.6:** inclusão das saídas **ICO** e **SVG**, preservando PNG, JPEG, WEBP e PDF.

## Licença

Nenhuma licença de código aberto foi definida neste documento. O titular do projeto poderá acrescentar um arquivo `LICENSE` ao repositório para especificar as condições de uso, modificação e distribuição.
