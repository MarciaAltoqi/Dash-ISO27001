# 📊 AltoQi · Dashboard ISO 27001

Dashboard interativo de monitoramento do projeto de certificação ISO 27001 da AltoQi.  
Meta de certificação: **março de 2027**.

---

## 🚀 Acesso rápido

> [🔗 https://marciaaltoqi.github.io/Dash-ISO27001/ ]

---

## 📋 O que é este projeto

Este repositório contém um único arquivo HTML (`index.html`) que funciona como um painel de controle completo para acompanhar a implementação dos controles da norma ISO 27001 na AltoQi. Ele foi desenvolvido para ser:

- **Autossuficiente** — um único arquivo, sem dependências de servidor ou instalação
- **Dinâmico** — conecta-se ao Google Sheets para atualização automática dos dados
- **Executivo** — foco em clareza visual e identificação rápida de pontos de atenção

---

## 🖥️ Funcionalidades

### Visão Executiva
| Componente | Descrição |
|---|---|
| **KPIs** | % de progresso, maturidade média, dias restantes até a auditoria, total de não implementados |
| **Burnup Chart** | Projeção de implementação mês a mês do kick-off até março/2027 |
| **Alertas de Risco** | Painel com os principais bloqueadores críticos para a certificação |
| **Progresso por Tópico** | Barras de progresso por categoria (Organizacional, Pessoas, Físico, Tecnológico) |

### Visão Operacional & Gargalos
| Componente | Descrição |
|---|---|
| **Mapa de Calor** | Matriz Área × Status — identifica visualmente onde estão os gargalos |
| **Donut Chart** | Distribuição proporcional por status de implementação |
| **Tabela de Plano de Ação** | Lista filtrável e ordenável de todos os controles com evidências e observações |
| **Filtros interativos** | Filtro por Área, Status, Tópico e busca livre — todos os componentes reagem juntos |

---

## 🔄 Como atualizar os dados

Os dados podem ser mantidos de duas formas:

### Opção 1 — Google Sheets (recomendado)

1. Mantenha a planilha de controles atualizada no Google Sheets
2. Publique a planilha na web:  
   **Arquivo → Compartilhar → Publicar na web → CSV → Publicar**
3. Copie o link gerado (formato `https://docs.google.com/spreadsheets/d/e/.../pub?output=csv`)
4. Abra o dashboard, cole o link na barra azul no topo e clique em **↻ Carregar dados**
5. O link fica salvo no navegador — nas próximas aberturas o dashboard atualiza automaticamente

> ⚠️ A planilha precisa estar com acesso **"Qualquer pessoa com o link pode ver"**.
---

## 🗂️ Estrutura da planilha de dados

A planilha deve conter obrigatoriamente as seguintes colunas, separadas por `;`:

| Coluna | Descrição | Exemplo |
|---|---|---|
| `ID do Controle` | Identificador do controle ISO | `5.1` |
| `Tópico` | Categoria da norma | `5.Organizacional` |
| `Descrição do Controle` | Nome curto do controle | `Políticas de segurança` |
| `Detalhes` | Descrição detalhada | `Criar e aprovar políticas...` |
| `Evidência esperada` | O que comprova a implementação | `Documentos publicados...` |
| `Maturidade` | Nível de maturidade (0 a 3) | `1.5` |
| `Área Responsável` | Equipe responsável | `CloudOps` |
| `Status de Implementação` | Status atual | `Implementado` / `Em andamento` / `Não implementado` |
| `Observações / Histórico` | Notas e contexto | `Em processo de revisão` |

### Escala de maturidade

| Valor | Significado |
|---|---|
| `0` | Inexistente / não iniciado |
| `1.5` | Em desenvolvimento / parcialmente implementado |
| `3` | Totalmente implementado e operacional |

### Status válidos

| Status | Cor no dashboard |
|---|---|
| `Implementado` | 🟢 Verde |
| `Em andamento` | 🟡 Amarelo |
| `Não implementado` | 🔴 Vermelho |

---

## 🛠️ Tecnologias utilizadas

- **HTML5 / CSS3 / JavaScript** — sem frameworks, sem dependências locais
- **[Chart.js 4.4](https://www.chartjs.org/)** — gráficos (carregado via CDN)
- **[Google Fonts](https://fonts.google.com/)** — tipografia (Space Grotesk + JetBrains Mono)
- **localStorage** — persiste o link do Google Sheets entre sessões

---

## 📅 Cronograma do projeto

| Marco | Data |
|---|---|
| Kick-off | Janeiro 2026 |
| Data atual | Maio 2026 |
| **Meta de certificação** | **Março 2027** |

---

## 👥 Áreas envolvidas

- CloudOps
- Infraestrutura
- Desenvolvimento Web
- Desenvolvimento Desktop
- People (RH)
- Legal
- Facilities
- Compras / Infra
- RevOps / CloudOps

---

## ❓ Dúvidas frequentes

**O dashboard funciona offline?**  
Sim, com os dados locais embutidos. Para carregar do Google Sheets é necessária conexão com a internet.

**Preciso instalar algo?**  
Não. Basta abrir o arquivo `index.html` em qualquer navegador moderno (Chrome, Firefox, Edge, Safari).

**Como compartilhar com a equipe?**  
Via GitHub Pages (link público) ou subindo o arquivo no SharePoint/Google Drive da empresa.

**Como restringir o acesso?**  
O GitHub Pages gratuito é público. Para acesso restrito, use o SharePoint interno ou o GitHub Pro/Team com repositório privado.

**Posso adicionar novos controles na planilha?**  
Sim. O dashboard recalcula tudo automaticamente a cada carregamento. Basta manter o formato das colunas.

---

## 📬 Contato

Projeto gerenciado pela equipe de **Segurança da Informação — AltoQi**.  
Dúvidas ou sugestões: **seguranca@altoqi.com.br**
