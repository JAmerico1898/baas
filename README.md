# 🏦 Banking as a Service (BaaS) - Aplicação Pedagógica

Uma aplicação interativa desenvolvida em **Streamlit** para ensino de Banking as a Service (BaaS) em cursos de MBA, baseada na **Consulta Pública do Banco Central do Brasil nº 108/2024** e **115/2025**, além de pesquisa internacional sobre o tema.

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Streamlit](https://img.shields.io/badge/Streamlit-1.28+-red.svg)
![License](https://img.shields.io/badge/License-Educational-green.svg)

---

## 📋 Sumário

- [Sobre o Projeto](#-sobre-o-projeto)
- [Funcionalidades](#-funcionalidades)
- [Instalação](#-instalação)
- [Como Executar](#-como-executar)
- [Estrutura da Aplicação](#-estrutura-da-aplicação)
- [Conteúdo Pedagógico](#-conteúdo-pedagógico)
- [Tecnologias Utilizadas](#-tecnologias-utilizadas)
- [Referências Regulatórias](#-referências-regulatórias)
- [Autor](#-autor)

---

## 📖 Sobre o Projeto

Esta aplicação foi desenvolvida como ferramenta pedagógica para o ensino de **Banking as a Service (BaaS)** no contexto do sistema financeiro brasileiro. O BaaS é um modelo de negócio onde instituições financeiras autorizadas pelo Banco Central disponibilizam sua infraestrutura regulamentada para que entidades terceiras (fintechs, varejistas, plataformas digitais) possam oferecer produtos e serviços financeiros aos seus clientes.

### Contexto Regulatório

Em outubro de 2024, o Banco Central do Brasil publicou a **Consulta Pública nº 108/2024**, propondo a regulamentação do modelo BaaS no país. Em janeiro de 2025, o prazo para contribuições foi prorrogado até 28 de fevereiro de 2025 através do **Edital nº 115/2025**.

---

## ✨ Funcionalidades

A aplicação conta com **10 módulos interativos**:

| Módulo | Descrição |
|--------|-----------|
| 🏠 **Introdução** | Conceitos fundamentais de BaaS e motivação regulatória |
| 🔄 **Ecossistema** | Diagrama interativo dos participantes e fluxos |
| 💼 **Modelos de Negócio** | Estruturas operacionais e modelos de monetização |
| ⚙️ **Serviços** | Escopo de serviços conforme proposta do BCB |
| 📋 **Regulação BCB** | Timeline e princípios da regulação proposta |
| ⚠️ **Riscos** | Mapeamento de riscos e caso Synapse |
| 🚀 **Oportunidades** | Benefícios e tendências (Embedded Finance) |
| 🌍 **Cenário Global** | Comparativo internacional de mercados BaaS |
| 📊 **Simulador** | Ferramenta interativa para análise de cenários |
| 📝 **Quiz** | Avaliação de conhecimentos com feedback |

### Destaques Técnicos

- **Visualizações Interativas**: Gráficos Plotly (radar, barras, timeline, fluxo)
- **Design Premium**: Interface dark theme estilo consultoria/Figma
- **Responsivo**: Layout adaptável para diferentes tamanhos de tela
- **Simulador de Cenários**: Cálculos dinâmicos de custos, receitas e riscos

---

## 🚀 Instalação

### Pré-requisitos

- Python 3.8 ou superior
- pip (gerenciador de pacotes Python)

### Dependências

```bash
pip install streamlit plotly
```

Ou usando requirements.txt:

```bash
pip install -r requirements.txt
```

**requirements.txt:**
```
streamlit>=1.28.0
plotly>=5.18.0
```

---

## ▶️ Como Executar

1. **Clone ou baixe** os arquivos do projeto

2. **Navegue** até o diretório do projeto:
   ```bash
   cd caminho/para/o/projeto
   ```

3. **Execute** a aplicação:
   ```bash
   streamlit run baas_app.py
   ```

4. **Acesse** no navegador:
   ```
   http://localhost:8501
   ```

### Configurações Opcionais

Para alterar a porta padrão:
```bash
streamlit run baas_app.py --server.port 8080
```

Para permitir acesso externo:
```bash
streamlit run baas_app.py --server.address 0.0.0.0
```

---

## 📁 Estrutura da Aplicação

```
baas-app/
├── baas_app.py          # Aplicação principal
├── README.md            # Este arquivo
└── requirements.txt     # Dependências (opcional)
```

### Arquitetura do Código

```
baas_app.py
│
├── Configuração & CSS
│   ├── st.set_page_config()
│   └── Estilos customizados (dark theme)
│
├── Funções Auxiliares
│   ├── create_metric_card()      # Cards de métricas
│   ├── create_participant_card() # Cards de participantes
│   ├── create_flow_diagram()     # Diagrama de fluxo Plotly
│   ├── create_risk_radar()       # Gráfico radar de riscos
│   ├── create_global_comparison()# Gráfico comparativo
│   └── create_timeline()         # Timeline regulatória
│
├── Sidebar (Navegação)
│   └── st.radio() com 10 opções
│
├── Páginas (condicionais por seleção)
│   ├── Introdução
│   ├── Ecossistema BaaS
│   ├── Modelos de Negócio
│   ├── Serviços
│   ├── Regulação BCB
│   ├── Riscos
│   ├── Oportunidades
│   ├── Cenário Global
│   ├── Simulador
│   └── Quiz
│
└── Footer
```

---

## 📚 Conteúdo Pedagógico

### 1. Conceitos Fundamentais

- **Definição de BaaS**: Modelo onde IFs autorizadas disponibilizam infraestrutura regulamentada
- **Participantes**: Instituição Prestadora, Tomador de Serviços, Middleware, Cliente Final
- **Analogia**: BaaS como o "SaaS" do setor bancário

### 2. Modelos de Negócio

| Estrutura | Características |
|-----------|-----------------|
| Parceria Direta | Maior controle, maior complexidade |
| Via Middleware | Integração simplificada, dependência |
| Banco Nativo API | Alta performance, poucos players |

| Modelo de Receita | Descrição |
|-------------------|-----------|
| Intercâmbio | Receita por transação de cartão |
| Depósitos | Compartilhamento de NIM |
| Crédito | Originação e venda de empréstimos |
| Plataforma | Taxas fixas ou variáveis |

### 3. Serviços Propostos pelo BCB

- **Previstos**: Contas de Pagamento, Pix, Cartões, TED/TEF
- **Em Discussão**: Crédito, Credenciamento/Subcredenciamento
- **Em Avaliação**: ITP (Open Finance), eFX (Câmbio)
- **Futuro**: Investimentos

### 4. Riscos Mapeados

- Regulatório (PLD/FT, True Lender)
- Operacional (Cibersegurança, Reconciliação)
- Reputacional (Confiança do cliente)
- Econômico (Modelo de receita, Compliance)

### 5. Caso Synapse (2024)

Estudo de caso sobre a falência do middleware americano Synapse e lições para o mercado brasileiro:
- Falhas de reconciliação em contas FBO
- Supervisão inadequada por bancos parceiros
- Complexidade de resolução em múltiplas camadas

---

## 🛠️ Tecnologias Utilizadas

| Tecnologia | Uso |
|------------|-----|
| **Python 3.8+** | Linguagem base |
| **Streamlit** | Framework de aplicação web |
| **Plotly** | Visualizações interativas |
| **HTML/CSS** | Estilização customizada |

### Paleta de Cores

| Cor | Hex | Uso |
|-----|-----|-----|
| Cyan | `#0ea5e9` | Destaque primário |
| Violet | `#8b5cf6` | Destaque secundário |
| Emerald | `#10b981` | Sucesso/Positivo |
| Amber | `#f59e0b` | Alerta/Atenção |
| Rose | `#f43f5e` | Erro/Negativo |
| Slate | `#0f172a` | Background |

---

## 📜 Referências Regulatórias

### Documentos do Banco Central do Brasil

1. **Consulta Pública BCB nº 108/2024**
   - Publicação: 31 de outubro de 2024
   - Tema: Proposta de regulamentação de BaaS
   - [Link para o documento](https://www.bcb.gov.br)

2. **Edital de Consulta Pública nº 115/2025**
   - Publicação: Janeiro de 2025
   - Tema: Prorrogação do prazo até 28/02/2025

### Literatura Complementar

- Pesquisas internacionais sobre BaaS
- Análise do mercado americano (Emenda Durbin)
- Caso Synapse e lições regulatórias
- Embedded Finance e tendências globais

---

## 👨‍🏫 Autor

**Prof. José Américo**  
COPPEAD/UFRJ - Instituto de Pós-Graduação e Pesquisa em Administração  
Universidade Federal do Rio de Janeiro

### Disciplinas Relacionadas

- Regulação do Sistema Financeiro
- Inovações em Serviços Financeiros
- Derivativos e Produtos Estruturados
- Finanças Digitais

---

## 📄 Licença

Este material foi desenvolvido para fins **educacionais** no âmbito do programa de MBA da COPPEAD/UFRJ.

---

## 🤝 Contribuições

Sugestões e melhorias são bem-vindas. Para contribuir:

1. Faça um fork do projeto
2. Crie uma branch para sua feature (`git checkout -b feature/nova-funcionalidade`)
3. Commit suas mudanças (`git commit -m 'Adiciona nova funcionalidade'`)
4. Push para a branch (`git push origin feature/nova-funcionalidade`)
5. Abra um Pull Request

---

<div align="center">

**Banking as a Service - Aplicação Pedagógica para MBA**

*Transformando a educação em finanças através de tecnologia interativa*

🏦 COPPEAD/UFRJ • 2024-2025

</div>
