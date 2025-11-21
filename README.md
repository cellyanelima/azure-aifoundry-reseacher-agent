# 🛒 Agente "Researcher" de Pesquisa de Preços de Supermercado (Nova Zelândia)  

## 📘 Introdução

Este repositório contém minha participação no Azure Frontier Girls – AI Foundry Challenge: Build Your First Copilot (Foundry Edition), um programa oficial da Microsoft voltado para capacitação técnica em IA generativa, Copilots e Azure AI.
O desafio propõe a criação de um agente funcional utilizando o Microsoft Azure AI Foundry, explorando desde conceitos fundamentais até a construção prática de soluções com ações, grounding e automações.

Ao longo das etapas, as participantes são avaliadas em presença, desempenho em quizzes, entrega técnica e qualidade da documentação — requisitos essenciais para a elegibilidade ao voucher de certificação Microsoft AZ-900.
Este projeto cumpre os critérios oficiais, apresentando a solução desenvolvida, registros do processo, prints das configurações e explicações do fluxo de execução do agente.

## 🎯 Descrição e objetivo do Agente

**Assinatura: Azure subscription 1**  
**Resource Group: rg-foundry-challenge**
**Modelo utilizado: gpt-4o-mini**  
**Nome do agente: Researcher**
**Integrações: Grounding com Bing Search + Ação de Envio de E-mail**

Este projeto demonstra a criação de um agente especializado em pesquisar preços de produtos de supermercados na **Nova Zelândia**, utilizando o **Azure AI Foundry**, o modelo **gpt-4o-mini**, integração com **Bing Search**, e uma ação personalizada de envio de e-mail contendo os resultados.

| Nome                                           | Tipo              | Região   |
|------------------------------------------------|-------------------|----------|
| products-price-project                         | Foundry           | East US  |
| bing-afg-challenge                             | Bing Resource     | Global   |
| get-prices                                     | Logic app         | East US  |
| products-price-project/products-price-project  | Foundry project   | East US  |

- Pesquisar preços em fontes confiáveis da Nova Zelândia:
  - **Woolworths/Countdown**
  - **New World**
  - **PAK'nSAVE**
- Retornar resultados em **JSON estruturado**.
- Garantir precisão, correspondência exata do produto e escolha do **menor preço**.
- Indicar claramente quando um item estiver fora do escopo ou não for encontrado.
- Permitir o envio do resultado completo via **Action** de e-mail configurada no AI Foundry.

---

## 🧠 Arquitetura Geral

O projeto foi criado no Azure AI Foundry portal, antes de configurar o agente,onde foi necessário provisionar o ambiente base no Azure AI Foundry.
Com o *Resource Group* já criado (`rg-foundry-challenge`), iniciamos a criação do recurso Foundry que servirá como hub central para projetos e experimentos, informando o nome do projeto (`products-price-project`), adicionei a assinatura, resource group e região, então revisei e criei. Com isto foi iniciada a criacao do Agente Researcher.

![Criação do Projeto](./images/1-criacao-projeto.png)

![Criação do Projeto](./images/2-product-price-project.png)

![Criação do Agente](./images/3-criacao-agente.png)

![Criação do Agente](./images/4-criacao-escolha-modelo.png)

![Criação do Agente](./images/5-criacao-resumo-deploy.png)

---
