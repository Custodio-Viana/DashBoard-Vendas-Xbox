# Xbox Game Pass Subscriptions Dashboard

Este projeto consiste em um dashboard interativo desenvolvido em Excel para análise de vendas e assinaturas do **Xbox Game Pass**. O objetivo principal é responder a perguntas de negócio cruciais e fornecer uma visualização clara do faturamento, tipos de planos e adesão a pacotes adicionais.

---

## 📂 Estrutura do Projeto

O arquivo Excel foi cuidadosamente estruturado utilizando as melhores práticas de modelagem e organização de planilhas. A pasta de trabalho está dividida nas seguintes abas:

1. **`A̳ssets`**: Contém a identidade visual do projeto, armazenando a paleta de cores (ex: Xbox Color `#9BC848` e `#22C55E`, cores negativas) e outras referências de design utilizadas no Dashboard.
2. **`B̳ases`**: A fonte de dados bruta (dataset). Contém todos os registros de assinantes, planos e valores.
3. **`C̳álculos`**: O motor do dashboard. Aba dedicada a responder as perguntas de negócio (ex: *"Qual faturamento Total de vendas de planos anuais"*), provavelmente utilizando Tabelas Dinâmicas (Pivot Tables) ou fórmulas agregadoras ligadas à base.
4. **`D̳ashboard`**: A camada de visualização final. Apresenta os gráficos, indicadores e segmentações de dados interagindo com a aba de cálculos.

---

## 📊 Dados Utilizados

A base de dados conta com **295 registros de assinaturas**. Cada linha representa um cliente e os detalhes do seu plano contratado. As principais variáveis (colunas) analisadas incluem:

* **Identificação do Cliente**: `Subscriber ID`, `Name`.
* **Detalhes da Assinatura**: 
  * `Plan` (Ultimate, Core, Standard).
  * `Start Date` (Data de início).
  * `Auto Renewal` (Renovação automática - Yes/No).
  * `Subscription Type` (Monthly, Annual, Quarterly).
  * `Subscription Price` (Preço base do plano).
* **Pacotes Adicionais (Add-ons)**: 
  * Adesão e valores do `EA Play Season Pass`.
  * Adesão e valores do `Minecraft Season Pass`.
* **Métricas Financeiras**: `Coupon Value` (Descontos aplicados) e `Total Value` (Valor total faturado).

---

## 🚀 Instruções para Reprodução e Uso

Para utilizar, atualizar e reproduzir os resultados deste dashboard, siga as instruções abaixo:

### 1. Requisitos
* Microsoft Excel 2016 ou superior (recomenda-se o Microsoft 365 para total compatibilidade funcional de gráficos modernos e segmentações de dados).

### 2. Como interagir com o Dashboard
1. Abra o arquivo `Projeto  Dashboard Finalizado.xlsx`.
2. Navegue até a aba **`D̳ashboard`**.
3. Utilize os filtros (Segmentações de Dados / *Slicers*) presentes na tela para filtrar a visualização por **Plano** (Ultimate, Core, etc.) ou **Tipo de Assinatura** (Anual, Mensal, etc.). Os gráficos responderão dinamicamente.

### 3. Como atualizar os dados
Caso novos clientes assinem o serviço ou ocorra o fechamento de um novo mês:
1. Vá até a aba **`B̳ases`**.
2. Adicione os novos dados na próxima linha vazia logo abaixo do último registro (garanta que a tabela do Excel se expanda automaticamente para englobar as novas linhas).
3. Preencha todas as colunas numéricas de receita corretamente.
4. Vá até a guia **Dados** (*Data*) na faixa de opções do Excel e clique em **Atualizar Tudo** (*Refresh All*).
5. O Excel irá recalcular a aba `C̳álculos` e atualizar automaticamente os visuais na aba `D̳ashboard`.

> ⚠️ **Nota Importante:** Evite alterar manualmente qualquer célula na aba `C̳álculos` ou apagar colunas na aba `B̳ases`, pois isso pode quebrar o vínculo das Tabelas Dinâmicas e as dependências do Dashboard.
