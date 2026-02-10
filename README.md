# Projeto: Análise Automática de Pull Requests com Prompt Engineering

Nome: Leandro Luccas  
Curso/Turma: ____________________  
Disciplina: ____________________  
Data: ____ / ____ / 2026  

---

## 1. Objetivo

Este projeto tem como objetivo demonstrar a aplicação de técnicas de
Prompt Engineering para análise automática de Pull Requests (PRs)
de Infraestrutura como Código (IaC), utilizando modelos de linguagem.

O foco da análise é identificar riscos relacionados a:

- Segurança
- Custo
- Compliance
- Boas práticas

Foram desenvolvidas três versões progressivas de prompts (v1, v2 e v3),
onde cada versão representa uma evolução da anterior.

---

## 2. Estrutura do Projeto

A estrutura de diretórios do projeto é organizada da seguinte forma:

Analise-Automatizada-de-Pull-Requests
├── exemplos-terraform/
│ ├── PR1-add-S3-bucket.md
│ ├── PR2-open-ssh.md
│ ├── PR3-increase-rds.md
│ ├── PR4-add-tag.md
│ ├── PR5-lambda-timeout.md
│ └── PR6-injection.md
|
|── prompts/
│ ├── v1-baseline.md
│ ├── v2-structured.md
│ └── v3-schema.md
│
├── resultados/
│ ├── v1-PR1.jpg
│ ├── v2-PR1.jpg
│ ├── v3-PR1.jpg
│ └── ...
│
└── README.md


Cada pasta possui uma função específica:

- `prompts/`: contém as versões dos prompts.
- `exemplos-terraform/`: contém os PRs simulados.
- `resultados/`: contém as evidências dos testes.
- `README.md`: documentação do projeto.

---

## 3. Metodologia

O projeto foi desenvolvido seguindo as etapas abaixo:

1. Criação de exemplos de Pull Requests em Terraform e CloudFormation.
2. Desenvolvimento progressivo dos prompts (v1, v2 e v3).
3. Execução de cada prompt em todos os exemplos.
4. Registro dos resultados por meio de screenshots.
5. Análise comparativa entre as versões.

Cada combinação de prompt e PR foi testada individualmente,
totalizando 18 execuções.

---

## 4. Evolução dos Prompts

### 4.1 Versão 1 — Baseline

A versão inicial utiliza linguagem natural sem restrições rígidas.

Características:

- Análise básica dos recursos.
- Identificação simples de problemas.
- Resposta em texto livre.
- Ausência de validações.

Limitações:

- Vulnerável a prompt injection.
- Sem controle de formato.
- Baixa confiabilidade.

Objetivo:
Avaliar o comportamento inicial do modelo.

---

### 4.2 Versão 2 — Structured

A segunda versão introduz regras e estrutura.

Características:

- Formato de resposta padronizado.
- Regras iniciais de segurança.
- Detecção básica de padrões suspeitos.

Limitações:

- Proteção parcial contra injeção.
- Ainda dependente de texto natural.

Objetivo:
Aumentar a consistência das respostas.

---

### 4.3 Versão 3 — Schema + Segurança

A terceira versão implementa um modelo estruturado em JSON
com regras rígidas de segurança.

Características:

- Saída em formato JSON.
- Isolamento do conteúdo do PR.
- Regras explícitas contra prompt injection.
- Campo de detecção de injeção.

Benefícios:

- Alta confiabilidade.
- Possibilidade de automação.
- Integração com pipelines.
- Redução de riscos.

Objetivo:
Criar um prompt adequado para uso em ambiente produtivo.

---

## 5. Exemplos de Teste

Foram utilizados seis Pull Requests simulados:

| PR  | Descrição                              | Categoria Principal |
|-----|----------------------------------------|---------------------|
| PR1 | Criação de bucket S3                   | Boas práticas       |
| PR2 | Abertura de porta SSH pública          | Segurança           |
| PR3 | Escalonamento de banco de dados         | Custo               |
| PR4 | Inclusão de tags de custo              | Compliance          |
| PR5 | Lambda sem timeout configurado         | Boas práticas       |
| PR6 | Tentativa de prompt injection          | Segurança           |

Esses exemplos permitem avaliar diferentes tipos de riscos.

---

## 6. Resultados

Os resultados demonstram a evolução progressiva dos prompts:

- V1: Alta vulnerabilidade a ataques.
- V2: Melhora na padronização.
- V3: Proteção efetiva contra injeção.

De forma geral:

| Versão | Padronização | Segurança | Automação |
|--------|-------------|-----------|-----------|
| V1     | Baixa        | Baixa     | Não       |
| V2     | Média        | Média     | Parcial   |
| V3     | Alta         | Alta      | Sim       |

---

## 7. Ferramentas Utilizadas

- ChatGPT (Web)
- Editor de texto (VS Code)
- Sistema operacional Windows

---

## 8. Conclusão

Este projeto demonstrou como a evolução do prompt impacta diretamente
na qualidade, segurança e confiabilidade das análises.

A versão V3 apresentou os melhores resultados, sendo a mais adequada
para utilização em ambientes corporativos e pipelines CI/CD.

A aplicação de técnicas de prompt engineering é fundamental para
o uso seguro de modelos de linguagem em processos críticos.

---

## 9. Considerações Finais

O projeto permitiu compreender, na prática:

- Riscos de prompt injection
- Importância da estruturação
- Validação de saídas
- Governança de IA

Esses conceitos são essenciais para ambientes modernos de cloud computing.

---
