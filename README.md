# React Data Visualizer

![React](https://img.shields.io/badge/React-20232A?style=flat&logo=react&logoColor=61DAFB)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![D3.js](https://img.shields.io/badge/D3.js-F9A03C?style=flat&logo=d3.js&logoColor=white)
![Chart.js](https://img.shields.io/badge/Chart.js-FF6384?style=flat&logo=chart.js&logoColor=white)
![Plotly](https://img.shields.io/badge/Plotly-3F4F75?style=flat&logo=plotly&logoColor=white)
![License](https://img.shields.io/badge/license-MIT-blue.svg)

Dashboard interativo de visualização de dados construído com React, oferecendo gráficos dinâmicos, análise em tempo real e interface responsiva para exploração de datasets complexos.

## 🎯 Visão Geral

Aplicação React moderna para visualização de dados que combina múltiplas bibliotecas de gráficos para criar dashboards interativos e responsivos para análise de dados empresariais.

### ✨ Características Principais

- **📊 Múltiplos Tipos de Gráficos**: Line, bar, pie, scatter, heatmap
- **🔄 Dados em Tempo Real**: Atualizações automáticas e streaming
- **📱 Design Responsivo**: Otimizado para desktop e mobile
- **🎨 Temas Customizáveis**: Dark mode e temas personalizados
- **📈 Análise Interativa**: Zoom, pan, drill-down
- **💾 Export de Dados**: PNG, SVG, PDF, CSV

## 🛠️ Stack Tecnológico

### Frontend Core
- **React 18**: Framework principal com hooks
- **TypeScript**: Tipagem estática (opcional)
- **CSS Modules**: Estilos modulares
- **Styled Components**: CSS-in-JS

### Visualização de Dados
- **D3.js**: Visualizações customizadas
- **Chart.js**: Gráficos responsivos
- **Plotly.js**: Gráficos científicos interativos
- **Recharts**: Gráficos React nativos

### Estado e Dados
- **Redux Toolkit**: Gerenciamento de estado
- **React Query**: Cache e sincronização de dados
- **Axios**: Cliente HTTP
- **Socket.io**: Dados em tempo real

## 📁 Estrutura do Projeto

```
React-Data-Visualizer/
├── public/                         # Arquivos públicos
│   ├── index.html                  # HTML principal
│   └── favicon.ico                 # Ícone da aplicação
├── src/                            # Código fonte
│   ├── components/                 # Componentes React
│   │   ├── Charts/                 # Componentes de gráficos
│   │   │   ├── LineChart.js        # Gráfico de linha
│   │   │   ├── BarChart.js         # Gráfico de barras
│   │   │   ├── PieChart.js         # Gráfico de pizza
│   │   │   ├── ScatterPlot.js      # Gráfico de dispersão
│   │   │   └── Heatmap.js          # Mapa de calor
│   │   ├── Dashboard/              # Componentes do dashboard
│   │   │   ├── Sidebar.js          # Barra lateral
│   │   │   ├── Header.js           # Cabeçalho
│   │   │   ├── FilterPanel.js      # Painel de filtros
│   │   │   └── MetricsCard.js      # Cards de métricas
│   │   ├── UI/                     # Componentes de interface
│   │   │   ├── Button.js           # Botões customizados
│   │   │   ├── Modal.js            # Modais
│   │   │   ├── Tooltip.js          # Tooltips
│   │   │   └── Loading.js          # Indicadores de carregamento
│   │   └── Layout/                 # Componentes de layout
│   │       ├── Container.js        # Container principal
│   │       ├── Grid.js             # Sistema de grid
│   │       └── Responsive.js       # Componentes responsivos
│   ├── hooks/                      # Custom hooks
│   │   ├── useData.js              # Hook para dados
│   │   ├── useChart.js             # Hook para gráficos
│   │   ├── useFilters.js           # Hook para filtros
│   │   └── useTheme.js             # Hook para temas
│   ├── services/                   # Serviços e APIs
│   │   ├── api.js                  # Cliente API
│   │   ├── dataService.js          # Serviço de dados
│   │   ├── chartService.js         # Serviço de gráficos
│   │   └── websocket.js            # WebSocket para tempo real
│   ├── utils/                      # Utilitários
│   │   ├── dataProcessing.js       # Processamento de dados
│   │   ├── chartHelpers.js         # Helpers para gráficos
│   │   ├── formatters.js           # Formatadores
│   │   └── constants.js            # Constantes
│   ├── styles/                     # Estilos globais
│   │   ├── globals.css             # Estilos globais
│   │   ├── variables.css           # Variáveis CSS
│   │   └── themes.css              # Temas
│   ├── App.js                      # Componente principal
│   └── index.js                    # Ponto de entrada
├── package.json                    # Dependências
├── .gitignore                      # Arquivos ignorados
└── README.md                       # Documentação
```

## 🚀 Quick Start

### Pré-requisitos

- Node.js 16+
- npm ou yarn

### Instalação

1. **Clone o repositório:**
```bash
git clone https://github.com/galafis/React-Data-Visualizer.git
cd React-Data-Visualizer
```

2. **Instale as dependências:**
```bash
npm install
# ou
yarn install
```

3. **Execute em desenvolvimento:**
```bash
npm start
# ou
yarn start
```

4. **Acesse a aplicação:**
```
http://localhost:3000
```

## 📊 Componentes de Visualização

### Line Chart Interativo
```jsx
import { LineChart } from './components/Charts/LineChart';

function Dashboard() {
  const data = [
    { date: '2024-01', value: 100 },
    { date: '2024-02', value: 150 },
    { date: '2024-03', value: 120 }
  ];

  return (
    <LineChart
      data={data}
      xKey="date"
      yKey="value"
      title="Vendas Mensais"
      color="#3b82f6"
      interactive={true}
      showTooltip={true}
    />
  );
}
```

### Bar Chart Responsivo
```jsx
import { BarChart } from './components/Charts/BarChart';

function SalesChart() {
  const salesData = [
    { category: 'Produto A', sales: 1200 },
    { category: 'Produto B', sales: 800 },
    { category: 'Produto C', sales: 1500 }
  ];

  return (
    <BarChart
      data={salesData}
      xKey="category"
      yKey="sales"
      title="Vendas por Produto"
      orientation="vertical"
      gradient={true}
    />
  );
}
```

### Pie Chart com Animações
```jsx
import { PieChart } from './components/Charts/PieChart';

function MarketShare() {
  const marketData = [
    { segment: 'Desktop', share: 45.2 },
    { segment: 'Mobile', share: 38.7 },
    { segment: 'Tablet', share: 16.1 }
  ];

  return (
    <PieChart
      data={marketData}
      labelKey="segment"
      valueKey="share"
      title="Market Share"
      showLabels={true}
      animated={true}
      colors={['#3b82f6', '#ef4444', '#10b981']}
    />
  );
}
```

## 🔄 Dados em Tempo Real

### WebSocket Integration
```jsx
import { useEffect, useState } from 'react';
import { useWebSocket } from './hooks/useWebSocket';

function RealTimeChart() {
  const [data, setData] = useState([]);
  const { socket, isConnected } = useWebSocket('ws://localhost:8080');

  useEffect(() => {
    if (socket) {
      socket.on('data-update', (newData) => {
        setData(prevData => [...prevData.slice(-50), newData]);
      });
    }
  }, [socket]);

  return (
    <div>
      <div>Status: {isConnected ? 'Conectado' : 'Desconectado'}</div>
      <LineChart data={data} realTime={true} />
    </div>
  );
}
```

### Auto-refresh de Dados
```jsx
import { useData } from './hooks/useData';

function AutoRefreshDashboard() {
  const { data, loading, error } = useData({
    url: '/api/metrics',
    refreshInterval: 5000, // 5 segundos
    autoRefresh: true
  });

  if (loading) return <Loading />;
  if (error) return <Error message={error.message} />;

  return (
    <Dashboard data={data} />
  );
}
```

## 🎨 Temas e Customização

### Theme Provider
```jsx
import { ThemeProvider } from './contexts/ThemeContext';

const lightTheme = {
  colors: {
    primary: '#3b82f6',
    secondary: '#64748b',
    background: '#ffffff',
    surface: '#f8fafc'
  }
};

const darkTheme = {
  colors: {
    primary: '#60a5fa',
    secondary: '#94a3b8',
    background: '#0f172a',
    surface: '#1e293b'
  }
};

function App() {
  return (
    <ThemeProvider themes={{ light: lightTheme, dark: darkTheme }}>
      <Dashboard />
    </ThemeProvider>
  );
}
```

### Styled Components
```jsx
import styled from 'styled-components';

const ChartContainer = styled.div`
  background: ${props => props.theme.colors.surface};
  border-radius: 8px;
  padding: 20px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  
  @media (max-width: 768px) {
    padding: 15px;
    margin: 10px;
  }
`;

const ChartTitle = styled.h3`
  color: ${props => props.theme.colors.primary};
  font-size: 1.25rem;
  margin-bottom: 15px;
`;
```

## 📱 Design Responsivo

### Responsive Grid
```jsx
import { Grid, GridItem } from './components/Layout/Grid';

function ResponsiveDashboard() {
  return (
    <Grid
      templateColumns={{
        base: '1fr',
        md: 'repeat(2, 1fr)',
        lg: 'repeat(3, 1fr)'
      }}
      gap={6}
    >
      <GridItem colSpan={{ base: 1, lg: 2 }}>
        <LineChart data={salesData} />
      </GridItem>
      <GridItem>
        <PieChart data={categoryData} />
      </GridItem>
      <GridItem colSpan={{ base: 1, md: 2 }}>
        <BarChart data={productData} />
      </GridItem>
    </Grid>
  );
}
```

## 💾 Export e Compartilhamento

### Export de Gráficos
```jsx
import { exportChart } from './utils/chartHelpers';

function ExportableChart({ data }) {
  const handleExport = (format) => {
    exportChart({
      data,
      format, // 'png', 'svg', 'pdf'
      filename: `chart-${Date.now()}`,
      width: 800,
      height: 600
    });
  };

  return (
    <div>
      <LineChart data={data} />
      <div>
        <button onClick={() => handleExport('png')}>Export PNG</button>
        <button onClick={() => handleExport('svg')}>Export SVG</button>
        <button onClick={() => handleExport('pdf')}>Export PDF</button>
      </div>
    </div>
  );
}
```

## 🧪 Testes

### Executar Testes
```bash
# Testes unitários
npm test

# Testes com coverage
npm run test:coverage

# Testes end-to-end
npm run test:e2e
```

### Exemplo de Teste
```jsx
import { render, screen } from '@testing-library/react';
import { LineChart } from './LineChart';

test('renders line chart with data', () => {
  const mockData = [
    { x: 1, y: 10 },
    { x: 2, y: 20 }
  ];

  render(<LineChart data={mockData} />);
  
  expect(screen.getByRole('img')).toBeInTheDocument();
});
```

## 🚀 Deploy

### Build para Produção
```bash
npm run build
```

### Deploy no Netlify
```bash
# Instalar Netlify CLI
npm install -g netlify-cli

# Deploy
netlify deploy --prod --dir=build
```

## 📊 Casos de Uso

### 1. Dashboard Executivo
- KPIs em tempo real
- Métricas de performance
- Análise de tendências

### 2. Analytics de Vendas
- Funil de conversão
- Performance por região
- Análise de produtos

### 3. Monitoramento de Sistema
- Métricas de performance
- Logs em tempo real
- Alertas visuais

## 📄 Licença

Este projeto está licenciado sob a Licença MIT - veja o arquivo [LICENSE](LICENSE) para detalhes.

## 👨‍💻 Autor

**Gabriel Demetrios Lafis**

- GitHub: [@galafis](https://github.com/galafis)
- Email: gabrieldemetrios@gmail.com

---

⭐ Se este projeto foi útil, considere deixar uma estrela!

