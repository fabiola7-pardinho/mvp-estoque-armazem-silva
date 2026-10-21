# mvp-estoque-armazem-silva
MVP de Controle de Estoque e Giro Rápido - Armazém &amp; Utilidades Silva (Python / Flask)
# 📦 Sistema de Controle de Estoque e Giro Rápido - Armazém & Utilidades Silva (MVP)

Projeto prático de Engenharia de Software (Análise e Desenvolvimento de Sistemas) voltado para a modernização operacional do **Armazém & Utilidades Silva**, microempreendimento varejista comunitário.

## 🎯 Objetivo do MVP e Alinhamento ODS
Eliminar o descompasso entre o controle manual em caderno físico e o atendimento presencial/WhatsApp, prevenindo rupturas de estoque e perdas de vendas. 
* **ODS 8 (ONU):** Trabalho Decente e Crescimento Econômico (Meta 8.3).

## 🚀 Funcionalidades Principais (Escopo Core)
- **RF01:** Cadastro e edição simplificada de produtos (nome, categoria, preço, saldo atual e estoque mínimo).
- **RF02:** Baixa (`-1`) e entrada (`+1`) rápida de mercadorias em clique único diretamente na listagem.
- **RF03:** Consulta preditiva instantânea (< 800 ms) para resposta rápida a clientes no balcão e WhatsApp.
- **RF04:** Alerta visual multimodal (`⚠ Estoque Baixo - Repor`) para produtos que atingem o limite mínimo de segurança.

## 🛠️ Arquitetura e Tecnologias Utilizadas
- **Padrão Arquitetural:** Monolítico em Camadas (MVC/MVT) com API REST leve.
- **Backend:** Python 3.12 + Flask 3.0 + Flask-SQLAlchemy (ORM) + Flask-Login / Werkzeug (Hash PBKDF2).
- **Frontend:** HTML5, CSS3, JavaScript (Fetch API) e Bootstrap 5.3 (Acessibilidade WCAG 2.1 AA com áreas de toque de 48x48 px).
- **Banco de Dados:** SQLite (Desenvolvimento/Testes) e PostgreSQL (Produção).
- **Testes Automatizados:** Pytest.

## 📂 Estrutura do Repositório
```text
├── app/
│   ├── models.py          # Entidades Produto e MovimentacaoEstoque
│   ├── routes.py          # Endpoints e regras de negócio
│   ├── templates/         # Telas (Login, Estoque Central e Alertas)
│   └── static/            # CSS e scripts assíncronos
├── tests/
│   └── test_estoque.py    # Testes unitários e de integração
├── requirements.txt       # Dependências do projeto
└── run.py                 # Ponto de entrada da aplicação
