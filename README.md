# Controle de Equipamentos Diário — Edição Timão

Aplicação web mobile em arquivo único (`index.html`) com identidade visual temática do **Sport Club Corinthians Paulista** (preto, branco e detalhes em vermelho), voltada ao registro diário de equipamentos, leitura por câmera com mira, reconhecimento automático de tipo, controle de reversa e exportação de dados.

## Funcionalidades

- **Tema Alvinegro:** Interface escura em preto e branco com listras verticais discretas, destaques em vermelho e símbolo do Corinthians renderizado no cabeçalho e incorporado ao relatório em PDF.
- **Registro de Equipamentos:** Cadastro por **Número do Contrato / OS** (com colagem automática a partir da área de transferência ao focar/clicar no campo), **Destino / Movimentação** (`Cliente` ou `Reversa`), **Tipo de Equipamento** (`ONT`, `EMTA`, `DECODER`, `SMARTCARD`, `CHIP`, `MESH`) e **MAC / CA ID / Serial**.
- **Leitura por Câmera com Mira:**
  - Suporte a códigos de barras (`Code 128`, `Code 39`, `Code 93`, `ITF`, `Codabar`) via `html5-qrcode` e `BarcodeDetector`, além de leitura de rótulos via `Tesseract.js` (OCR).
  - Toque na área da câmera ou use os botões **Ler Mira Agora**, **Forçar Leitura**, **Focar** e **Luz** (lanterna, quando suportada pelo dispositivo).
  - Filtro automático de identificação para priorizar códigos válidos e detecção inteligente do tipo de equipamento.
- **Gestão e Reversa:** Busca instantânea por MAC, CA ID, contrato ou data/hora, exclusão de registros e registro de data/hora de entrega para itens em **Reversa**.
- **Persistência e Exportação/Importação:**
  - Armazenamento local automático no navegador (`localStorage`, chave `claro_equipamentos_v1`).
  - Exportação em **CSV** (`relatorio_equipamentos_timao.csv`), **PDF** (`relatorio_equipamentos_timao.pdf`) e **JSON** (`backup_equipamentos_timao.json`), além de **Importação JSON** com opção de mesclar sem duplicatas ou substituir a lista atual.

## Como Usar

1. Extraia os arquivos do pacote `.zip`.
2. Abra o `index.html` em um navegador moderno (de preferência em **HTTPS** ou `localhost` para que o navegador permita o acesso à câmera do celular).
3. Preencha ou escaneie os dados do equipamento e clique em **Salvar Equipamento**.

## Autor e Versão

- **Criado por:** Fernando Sato
- **Versão:** 30.2 (Edição Timão)
- **Data de revisão:** 24/11/2026 21:50
