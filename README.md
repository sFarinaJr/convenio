# Convênio — Demonstrativo de Repasse Odontológico

Ferramenta web que lê o **PDF do demonstrativo de pagamento** de operadoras de
convênios odontológicos e gera um **relatório sintético por profissional**,
calculando bruto, imposto, líquido e glosas para facilitar o repasse aos
dentistas pelos gestores de clínica.

**Acesse:** https://sfarinajr.github.io/convenio/

## Como usar

1. Abra a URL acima em qualquer computador.
2. Defina a alíquota de imposto (padrão 11%).
3. Arraste o PDF do demonstrativo (ou clique para selecionar).
4. Veja o resumo, a tabela por profissional e o detalhamento por paciente.
5. Exporte em **CSV** ou baixe o **relatório em PDF**.

Operadoras com leitura mapeada: **Unimed** e **Odontoprev** (detecção
automática). Outras operadoras são reconhecidas no título, mas a extração de
valores pode precisar de ajuste.

## Privacidade

Processamento **100% local no navegador** (PDF.js). O conteúdo do
demonstrativo **não é enviado a nenhum servidor** — o GitHub Pages apenas
entrega os arquivos estáticos.

## Estrutura

| Arquivo       | Função                                                                 |
|---------------|------------------------------------------------------------------------|
| `index.html`  | Aplicação completa (UI + leitura de PDF + relatórios). É o que o Pages serve. |
| `Code.gs`     | Alternativa de hospedagem via **Google Apps Script** (não usado pelo GitHub Pages). |

### Sobre o `Code.gs`

É o invólucro para servir o app como Web App do Google Apps Script. No Apps
Script o arquivo HTML deve se chamar `Index` (sem extensão), como referenciado
em `createTemplateFromFile('Index')`. Mantido apenas como referência — a
hospedagem oficial é o GitHub Pages.

## Tecnologias (via CDN)

PDF.js · Chart.js · html2pdf.js · Lucide Icons · Google Fonts (Inter)
