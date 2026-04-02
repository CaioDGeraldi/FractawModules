# Fractaw Modules

<p align="center">
  <strong>Solução ERP Modular moderno para empresas.</strong><br>
  
</p>

<p align="center">
  <img src="https://img.shields.io/badge/status-em%20desenvolvimento-blue">
  <img src="https://img.shields.io/badge/framework-Django-green">

</p>

> Pare de lutar contra o seu software. O Fractaw Modules quebra a complexidade de um ERP comum em partes gerenciáveis, para que você foque no negócio, não no sistema.

---

# Sobre o Projeto

**Fractaw Modules** é uma coletânea de soluções em módulos para melhor e específica gestão empresarial.

Diferente dos Modules tradicionais, o Fractaw foi projetado para ser:

* Simples
* Rápido
* Acessível
* Moderno
* Integrável

Os módulos cobrem áreas como:
* **Financeira | Contabilidade**
* **Logística | Gestão de Estoque**
* **Vendas | CRM**
* **Gestão de Serviços**

---

# Problema

A maioria das soluções tradicionais apresenta três grandes problemas:

* Alto custo
* Interfaces complexas
* Dificuldade de Escalabilidade
* Implantação lenta

> A maioria dos ERPs do mercado são monólitos, o que significa que mesmo utilizando apenas um serviço, você ainda precisa do ERP inteiro. 

---

# Solução

O **Fractaw Modules** oferece:

* **Escalabilidade Granular em Módulos**

Se seu negócio cresceu, você apenas escala o setor do sistema desejado conforme seu próprio negócio, sem necessidades de aumentar a potência de um sistema inteiro.

* **Independência de Falhas** 

Ao fracionar as capacidades de um ERP tradicional em módulos, eliminamos o "ponto único de falha". Isso resulta em uma plataforma com maior índice de disponibilidade e facilidade de manutenção, sem interrupções globais de serviço.

* **Integração Rápida**

O **Fractaw Modules** transcende a limitação dos sistemas "caixa-preta". Nossa arquitetura foi projetada sob o paradigma **API-First**, garantindo que a comunicação entre módulos e softwares externos ocorra de forma fluida, segura e padronizada.

Objetivo:

> Permitir que empresas reduzam os custos operacionais e escalar o sistema conforme o próprio negócio.

---

# MVP (Minimum Viable Product)
Nesta fase inicial, o foco está na gestão de **fluxo de vendas**, **estoque** e **relatórios de logística** e na integração de API e permitir com que os módulos conversem entre si.

Projeto Base:

<details>
  <summary>Módulo de Vendas</summary>
  
- Emissão de Pedidos/Seriços: Fluxo de criação, edição e fechamento de venda.
  
- Status de Venda: Controle de etapas (Ex: Orçamento -> Aprovado -> Faturado -> Cancelado).

- Calculo de Impostos e Descontos: Regras básicas para chegar ao valor líquido e bruto.

</details>

<details>
<summary>Módulo de Gestão de Estoque</summary>
  
- Cadastro de Produtos Detalhado: SKU (identificador único), EAN (código de barras), categoria, unidade de medida (kg, un, m) e preço de custo.

- Movimentação Manual: Entradas (compras/ajustes) e Saídas (vendas/perdas/avarias).

- Controle de Saldo em Tempo Real: Visualização imediata de quanto resta de cada item.

- Alerta de Estoque Mínimo: Notificação quando um produto atinge o nível crítico para evitar ruptura (falta de produto).

</details>

<details>
<summary>Módulo de Relatórios de Logística</summary>

- Relatórios de Logística: Relatório geral de vendas, transportes, dados de parceiros, frete, prazos e feedbacks.

- Gestão de Expedição: Um fluxo simples para confirmar que os itens certos foram retirados do estoque e embalados.

- Cadastro de Transportadoras: Registro de parceiros logísticos, tipos de frete (FOB/CIF) e prazos médios.

- Código de Rastreio: Campo para anexar o link/código de rastreamento de terceiros (Correios, Jadlog, etc.) ao pedido.

- Cálculo de Frete Básico: Tabela simples de preços por região ou integração com uma API de cálculo de frete.
  
</details>

# Adicionais
Adições futuras e desejáveis para o projeto.

<details>
  <summary>Integração com WhatsApp Business</summary>
  
  <details>  
  <summary>Notificações Transacionais Automatizadas:</summary>

  - Vendas: Envio do PDF do orçamento ou confirmação de pedido.
  
  - Financeiro: Envio de lembretes de vencimento e boletos/Pix copia-e-cola.

  - Logística: Atualização automática do status de rastreamento ("Seu pedido saiu para entrega!").

  - Templates Oficiais (HSM): Gestão de modelos de mensagens aprovados pela Meta para iniciar conversas.

  - Webhook de Recebimento: Capturar mensagens do cliente e registrar no histórico do CRM.
  
  </details>

  <details>
  <summary>Integração Modular</summary>
    
  - O WhatsApp aqui funciona como um Service Consumer de todos os outros módulos:

  - Vendas → WhatsApp: O vendedor clica em "Enviar via Zap" e o módulo de WhatsApp consome a API de Vendas para gerar a mensagem.

  - Logística → WhatsApp: O gatilho de "Objeto Postado" dispara uma mensagem automática sem intervenção humana.
  
  </details>

  <details>
  <summary>Funcionalidades Avançadas</summary>
    
  - Chatbot de Autoatendimento: Menu interativo para o cliente consultar status de pedido ou segunda via de boleto sozinho.

  - Multi-agentes: Uma única conta de WhatsApp Business distribuindo conversas para vários vendedores do módulo de Vendas.

  - Interactive Messages: Botões de "Aprovar Orçamento" ou "Confirmar Recebimento" direto no chat, que atualizam o banco de dados do ERP via API.
</details>
