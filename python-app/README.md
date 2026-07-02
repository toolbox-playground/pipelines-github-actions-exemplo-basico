# Python App 🐍

Este reposiório trás a aplicação Python utilizada como base para implementação e validação da pipeline de CI/CD.

## Objetivo 🎯

Disponibilizar uma estrutura mínima de projeto Python para suportar a validação do fluxo de integração contínua, incluindo verificações de segurança, auditoria de dependências, testes automatizados, geração de pacote e fluxo de publicação.

## Estrutura 📋

```text
python-app/
├── src/
│   └── python_app/
├── tests/
├── pyproject.toml
├── requirements.txt
└── README.md

```

## Execução Local▶️

### Criar e ativar o ambiente virtual

```bash
python3 -m venv .venv
source .venv/bin/activate

```

### Instalar as dependências

```bash
pip install -e ".[dev]"

```

### Executar os testes

```bash
pytest

```

### Gerar o pacote

```bash
python -m build

```

## Pipeline CI/CD 🔄

A pipeline implementada para esta aplicação contempla as seguintes etapas:

-  🛡️ **Secret Scan** utilizando TruffleHog;
    
-  🔒 **Dependency Check** utilizando `pip-audit`;
    
-  🧪 **Testes automatizados** utilizando `pytest`;
    
-  📦 **Build** do pacote Python utilizando `python -m build`;
    
-  🚀 **Publicação** protegida por aprovação manual através do GitHub Environments.
    

## Observações 📝

O fluxo de publicação foi estruturado para utilizar credenciais armazenadas como **GitHub Secrets**, seguindo boas práticas de segurança.

A publicação efetiva depende da configuração de uma credencial válida e do repositório de pacotes utilizado pela empresa.