# miniguia-estudos-notebooklm
Miniguia de Estudos para Analista SOC usando NotebookLM e IA.
# 🛡️ Miniguia de Estudos: Análise de Logs e Detecção de Ameaças em SOC

> **Projeto de Caderno Temático desenvolvido para o Bootcamp DIO / Bradesco - GenAI, Dados & Cyber, utilizando o Google NotebookLM como ferramenta de aprendizagem ativa.**

---

## 📌 Contexto e Objetivos

Com o crescimento exponencial do volume de dados em ambientes corporativos, a atuação do **Analista SOC (Security Operations Center)** exige capacidade de processar, filtrar e identificar anomalias em logs de sistemas de forma rápida e precisa.

Este projeto tem como objetivo construir uma base de conhecimento interativa no **NotebookLM** para acelerar os estudos sobre:
- Fundamentos de monitoramento de segurança e estrutura de logs (Syslog, Web, Autenticação).
- Uso de **Python (Pandas)** para automação de análise e detecção de anomalias em tempo real.
- Consultas estratégicas em **SQL** para investigação de incidentes e varreduras.

---

## 📚 Curadoria de Fontes

Para alimentar a base de conhecimento do NotebookLM, foram selecionadas e carregadas as seguintes fontes abertas e documentações técnicas:

1. **NIST SP 800-92 - Guide to Computer Security Log Management**
   - *Descrição:* Guia oficial do NIST com boas práticas para gerenciamento, análise e retenção de logs de segurança.
2. **Documentação Oficial do Python Pandas para Análise de Dados**
   - *Descrição:* Referência técnica sobre manipulação de DataFrames, filtragem de dados e análise de séries temporais aplicadas a logs.
3. **Cheat Sheet de Consultas SQL para Cibersegurança e Forense**
   - *Descrição:* Guia com comandos SQL para agrupamento (`GROUP BY`), identificação de eventos atípicos e correlação de dados.

---

## 🛠️ Engenharia de Prompts e Solução de Problemas (Troubleshooting)

Nesta etapa, documentei a evolução das perguntas enviadas ao NotebookLM para extrair análises mais precisas do material fornecido.

### 🧪 Teste 1: Solicitação Genérica vs. Prompt Estruturado

- **Prompt Inicial (Simples):** 
  > *"Como analisar logs de acesso com Python?"*
- **Resultado:** Resposta genérica listando apenas bibliotecas básicas sem contexto de segurança ou código aplicável.
- **Prompt Refinado (Engenharia de Prompt):**
  > *"Atuando como um Analista SOC Sênior, utilize as fontes fornecidas para explicar como o Python (Pandas) pode ser usado para detectar tentativas de ataque de força bruta em logs de login. Apresente a lógica e um exemplo de código funcional com comentários."*
- **Resultado Obtido:** A IA utilizou os trechos do guia do NIST e a documentação de Python para construir uma lógica clara baseada em contagem de falhas por endereço IP em janelas de tempo.

### 💡 "Cicatrizes" e Dificuldades Encontradas:
- **Desafio:** Inicialmente, ao perguntar sobre SQL, o NotebookLM trouxe sintaxes específicas de bancos NoSQL que não estavam no escopo.
- **Ajuste:** Foi necessário restringir o contexto no prompt usando a instrução: *"Responda utilizando estritamente a sintaxe do MySQL citada nos documentos anexados."*

---

## 📖 Miniguia de Estudo (Entrega Final)

### 📝 Resumo Estruturado do Assunto

1. **Estrutura e Tipos de Logs:**
   - Logs de Webserver (Apache/Nginx): Registram requisições HTTP, status codes (ex: 401/403 para falhas de acesso) e IPs de origem.
   - Logs de Autenticação (Syslog/Windows Event Log): Registram eventos de login, elevação de privilégios e falhas de senha.
2. **Identificação de Anomalias:**
   - **Força Bruta:** Alta frequência de falhas (status 401) vindas de um mesmo IP em um curto intervalo de tempo.
   - **Varredura (Port Scanning / Reconnaissance):** Múltiplas requisições sequenciais buscando caminhos inexistentes (status 404).

---

### 🔤 Glossário de Conceitos Aprendidos

| Termo | Definição |
| :--- | :--- |
| **SOC (Security Operations Center)** | Central responsável por monitorar, detectar e responder a incidentes de cibersegurança. |
| **SIEM** | Ferramenta que centraliza a coleta e análise de logs de múltiplos sistemas. |
| **Outlier / Anomalia** | Dado que se desvia significativamente do padrão normal de tráfego ou comportamento. |
| **Parsing de Logs** | Processo de ler e estruturar arquivos de texto não formatados em tabelas de dados. |

---

### 🔄 Prompts Reutilizáveis para Revisões Futuras

Guarde estes prompts para usar no NotebookLM ao estudar novos temas:

* **Prompt 1 (Síntese de Conceitos):**
  > *"Crie um resumo executivo com os 5 principais indicadores de comprometimento (IoCs) citados nos textos, organizando em uma tabela com 'Ameaça', 'Sinal de Log' e 'Ação Recomendada'."*
* **Prompt 2 (Gerador de Casos Práticos):**
  > *"Elabore um cenário fictício de incidente de segurança baseado nas fontes e me faça 3 perguntas técnicas para testar minha capacidade de resposta como Analista SOC."*
* **Prompt 3 (Refatoração de Consultas SQL):**
  > *"Com base no guia de SQL fornecido, monte uma consulta capaz de agrupar requisições por IP e filtrar apenas aqueles com mais de 50 tentativas de acesso no mesmo minuto."*

---

## 👤 Autor

**Teyrone Korol Vidal**  
- 💼 [LinkedIn](https://www.linkedin.com/in/teyrone-korol-vidal-/)  
- 🐙 [GitHub](https://github.com/Teyrone)
