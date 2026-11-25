# Controle de Equipamentos Diário — Edição Timão (v30.3)

Aplicação web autônoma (arquivo único `index.html`) para controle diário de instalação, entrega e logística reversa de equipamentos de telecomunicações (ONT, EMTA, Decoder, Smartcard, Chip e Mesh Wi-Fi), com suporte a funcionamento **100% offline** via armazenamento local (`localStorage`).

---

## Principais Melhorias da Versão 30.3

- **Escudo S.C. Corinthians Paulista 100% Offline:** O escudo no cabeçalho foi incorporado diretamente em formato vetorial (`data:image/svg+xml`) no atributo `src` da tag `<img>`, eliminando o ícone de imagem quebrada quando o arquivo é aberto localmente no Android (`content://` ou `file://`) ou sem conexão com a internet.
- **Correção de Sintaxe no Parser:** Corrigidas as expressões regulares `.split(/\r?\n/)` que impediam a execução do JavaScript em navegadores móveis.
- **Indicador de Status de Rede:** Exibe em tempo real no cabeçalho se o dispositivo está **Online** ou **Offline**, confirmando que o salvamento local permanece ativo.

---

## Funcionalidades

- **Cadastro Rápido:** Registro de Contrato/OS, Destino (`Cliente` ou `Reversa`), Tipo de Equipamento e código (`MAC`, `CA ID` ou `Serial`).
- **Detecção Automática de Equipamento:** Identifica automaticamente ONT, EMTA, Decoder, Smartcard, Chip (ICCID) e Mesh ao digitar, colar ou escanear o código.
- **Leitor Híbrido por Câmera:** Combina `Html5Qrcode`, `BarcodeDetector` nativo e OCR (`Tesseract.js`) com mira de precisão, controle de foco, lanterna e botão **Forçar Leitura** (quando conectado ou em cache).
- **Controle de Reversa:** Permite marcar a data/hora exata da entrega/devolução de equipamentos retirados.
- **Busca e Filtros Instantâneos:** Pesquisa por MAC, CA ID, número de contrato ou data.
- **Exportação e Backup:**
  - **CSV (Excel):** Gera planilha compatível com Microsoft Excel e Google Sheets (offline).
  - **JSON (Exportar / Importar):** Backup completo com opção de mesclar sem duplicar ou substituir registros (offline).
  - **PDF:** Relatório paisagem formatado com o escudo do Corinthians no cabeçalho.

---

## Como Usar

1. Extraia os arquivos do pacote ZIP (`index.html` e `README.md`).
2. Abra o arquivo `index.html` diretamente no navegador (Chrome, Edge, Safari ou visualizador HTML).
3. Todos os registros ficam armazenados localmente no navegador (`localStorage`), funcionando mesmo sem internet.
