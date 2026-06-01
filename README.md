# OPL Digital - Utilidades

App desktop da OPL Digital para centralizar ferramentas usadas no dia a dia.

## Ferramentas

- Central de PDF: comprimir, unir, extrair paginas, reordenar, rotacionar, editar texto, assinar, adicionar marca d'agua, extrair texto, converter paginas em imagens, gerar PDF a partir de imagens e converter PDF/Word.
- Redimensionador de imagens: preview, dimensoes finais, modos de encaixe, alinhamento, qualidade e suporte a GIF animado.
- Validador de criativos: analisa imagens, pastas e ZIPs; informa formato, dimensoes, peso e todos os motivos de reprovacao.
- Correcao individual: converte criativos corrigiveis para JPG e comprime arquivos acima do peso permitido sem alterar suas dimensoes.

## Atualizacoes

O app consulta gratuitamente o manifesto publico `latest.json`. Quando existe uma versao nova, uma notificacao discreta aparece no canto do programa com um botao para baixar o instalador diretamente do GitHub.

O download do Windows usa o instalador `.exe` diretamente, sem arquivo compactado e sem senha.

## Tecnologia

- Electron para o app desktop.
- Node.js com Sharp para processamento de imagens.
- Helper standalone em Python/PyMuPDF empacotado com PyInstaller para processamento de PDFs.

## Requisitos de desenvolvimento

- Node.js 20 ou superior.
- Python 3 com `PyMuPDF` instalado apenas se precisar reconstruir o helper de PDF.
- Opcional: LibreOffice para preservar melhor o layout ao converter Word para PDF.

## Rodar

```bash
npm install
npm start
```

## Gerar instalador

```bash
npm run build
npm run package:public
```

O instalador publico sera criado em `release/` com o nome `OPL-Digital-Utilidades-Setup-<versao>.exe`.
