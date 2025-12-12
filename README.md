# Dashboard de Operações

Dashboard interativo desenvolvido com Google Apps Script para monitoramento de métricas operacionais em tempo real.

## 📊 Funcionalidades

- **Visão Geral**: Dashboard consolidado com todas as métricas principais
- **Chargeback**: Análise detalhada de chargebacks com gráficos e indicadores
- **Garantia**: Monitoramento de garantias com histórico mensal
- **BadDebt**: Acompanhamento de dívidas incobráveis
- **Credenciamento**: Análise de credenciamentos realizados
- **Prevenção**: Métricas de ações preventivas

## 🎨 Características

- ✅ Design responsivo e moderno
- ✅ Integração com Google Sheets
- ✅ Gráficos interativos com Chart.js
- ✅ Navegação intuitiva com menu lateral
- ✅ Indicadores de performance com variação percentual
- ✅ Interface em português brasileiro

## 🚀 Como Implementar

### 1. Criar um novo projeto Google Apps Script

1. Acesse [Google Apps Script](https://script.google.com/)
2. Clique em "Novo Projeto"
3. Nomeie o projeto como "Dashboard de Operações"

### 2. Adicionar os arquivos

1. **Code.gs**: Copie o conteúdo do arquivo `Code.gs` para o editor
2. **index.html**: Clique em "+" ao lado de "Arquivos" > "HTML" > Nomeie como "index" > Cole o conteúdo
3. **appsscript.json**: Clique no ícone de configurações (⚙️) > Cole o conteúdo do arquivo `appsscript.json`

### 3. Configurar a planilha Google Sheets

1. Crie uma nova planilha no Google Sheets
2. Copie o ID da planilha (encontrado na URL: `https://docs.google.com/spreadsheets/d/ID_DA_PLANILHA/edit`)
3. No arquivo `Code.gs`, atualize a constante `SPREADSHEET_ID` com o ID da sua planilha

### 4. Estrutura da planilha

Crie as seguintes abas na planilha com a estrutura:

#### Aba "Chargeback"
```
A1: Métrica          B1: Valor
A2: Total            B2: 15234
A3: Mês Atual        B3: 2340
A4: Variação (%)     B4: -12.5
A5: (vazio)          B5: (vazio)
A6: Jan              B6: 2500
A7: Fev              B7: 2300
... (continuar para outros meses)
```

Repita a mesma estrutura para as abas:
- "Garantia"
- "BadDebt"
- "Credenciamento"
- "Prevencao"

### 5. Implantar como aplicativo web

1. No editor do Apps Script, clique em "Implantar" > "Nova implantação"
2. Clique no ícone de engrenagem e selecione "Aplicativo da Web"
3. Configure:
   - **Descrição**: Dashboard de Operações v1.0
   - **Executar como**: Eu (seu email)
   - **Quem tem acesso**: Qualquer pessoa (ou conforme sua necessidade)
4. Clique em "Implantar"
5. Copie o URL do aplicativo web

### 6. Acessar o dashboard

Abra o URL copiado no navegador para visualizar o dashboard.

## 📱 Interface

O dashboard possui as seguintes seções:

### Navegação Principal
- 📈 Visão Geral
- 💳 Chargeback
- 🛡️ Garantia
- ⚠️ BadDebt
- ✅ Credenciamento
- 🔒 Prevenção

### Cada seção contém:
- **Cards de métricas**: Total acumulado, mês atual e variação percentual
- **Gráficos**: Visualização da evolução mensal dos dados
- **Indicadores visuais**: Cores e ícones para facilitar a interpretação

## 🔧 Personalização

### Alterar cores
As cores dos cartões podem ser personalizadas no arquivo `index.html`, nas classes CSS:
```css
.color-chargeback
.color-garantia
.color-baddebt
.color-credenciamento
.color-prevencao
```

### Adicionar novas métricas
1. Crie uma nova função em `Code.gs` seguindo o padrão das existentes
2. Adicione a nova aba na planilha
3. Crie uma nova seção no `index.html`
4. Adicione o link de navegação no menu lateral

## 📊 Dados de Exemplo

O sistema possui dados de exemplo (fallback) que são exibidos caso:
- A planilha não esteja acessível
- O ID da planilha esteja incorreto
- As abas não existam

Isso permite testar o dashboard antes de configurar a planilha completa.

## 🛠️ Tecnologias Utilizadas

- **Google Apps Script**: Backend e integração com Google Sheets
- **HTML5/CSS3**: Interface do usuário
- **JavaScript**: Lógica de interação
- **Chart.js 3.9.1**: Biblioteca para gráficos interativos

## 📝 Notas Importantes

1. O ID da planilha deve ser atualizado no arquivo `Code.gs`
2. A conta que executa o script precisa ter acesso à planilha
3. Para uso em produção, considere ajustar as permissões de acesso
4. Os dados são carregados ao abrir o dashboard
5. O design é totalmente responsivo para dispositivos móveis

## 🐛 Solução de Problemas

### Dashboard não carrega dados
- Verifique se o SPREADSHEET_ID está correto
- Confirme que a conta tem acesso à planilha
- Verifique se as abas estão nomeadas corretamente

### Gráficos não aparecem
- Verifique a conexão com a internet (Chart.js é carregado via CDN)
- Abra o console do navegador (F12) para ver erros

### Erro de permissão
- Reimplante o aplicativo web
- Verifique as configurações de compartilhamento da planilha

## 📄 Licença

Este projeto é de código aberto e está disponível para uso livre.

## 👨‍💻 Autor

Dashboard desenvolvido para monitoramento de operações empresariais.
