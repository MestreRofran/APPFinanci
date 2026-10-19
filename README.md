# Financi

Financi é um aplicativo web progressivo (PWA) para organização financeira pessoal.
Ele foi pensado para uso direto no navegador ou instalado no Android, com foco em praticidade no dia a dia.

## O que o app faz

O Financi reúne, em uma única aplicação:

- controle de despesas mensais;
- organização de compras e devoluções;
- histórico de movimentações;
- gráficos e tabelas de gastos;
- acompanhamento de pessoas que devem ou para quem você deve;
- cadastros de pessoas, categorias, meios de pagamento e contas;
- salvamento local, por arquivo e por login em nuvem;
- funcionamento como PWA, com suporte offline básico.

## Como o projeto foi estruturado

O projeto foi feito em **HTML + CSS + JavaScript puro**, sem depender de framework.
A proposta é manter tudo simples de publicar e atualizar no GitHub Pages.

Arquivos principais:

- `index.html` → aplicativo principal publicado no GitHub Pages;
- `manifest.json` → configura a instalação PWA;
- `sw.js` → Service Worker para cache e funcionamento offline básico;
- `financi-192.png`, `financi-512.png`, `financi-maskable-512.png` → ícones do app;
- `favicon.ico`, `favicon-16x16.png`, `favicon-32x32.png` → miniaturas do navegador;
- `apple-touch-icon.png` → atalho para dispositivos Apple;
- `financi-social-1200x630.png` → imagem de compartilhamento/apresentação.

## Funcionalidades principais

### 1. Tela Inicial
- visão resumida das contas, compras, valores recebidos, gastos e pessoas;
- indicadores rápidos e atalhos para detalhes.

### 2. Despesas Mensais
- acompanhamento das faturas e contas do mês;
- marcação de pagamento, recebimento e pagamentos parciais;
- filtros específicos por situação e tipo.

### 3. Minhas Compras
- lista do que deseja comprar;
- compras aguardando entrega;
- itens recebidos com prazo de devolução;
- fluxo de devolução e reembolso com campos completos;
- cópia de itens e edição detalhada.

### 4. Busca Histórico
- consulta de lançamentos anteriores;
- filtros por período;
- exibição de observações, rateios, pagadores e devedores.

### 5. Pessoas Devem
- controle de quem deve para você e de quem você deve;
- filtros e detalhamento dos valores de origem.

### 6. Tabela de Gastos
- gráficos de faturas e compras;
- filtros por período, pessoa e forma de pagamento;
- exibição em formatos diferentes conforme a necessidade.

### 7. Configurações
- tema visual;
- gerenciamento de armazenamento;
- login e nuvem;
- filtros da tela inicial;
- ajustes gerais do app.

## Armazenamento

O app suporta diferentes formas de persistência:

- cache/local do navegador;
- arquivo JSON em pasta conectada;
- login com sincronização em nuvem.

Quando houver divergência entre cópias, a lógica atual prioriza a **informação mais recente**.

## Login e nuvem

O app foi preparado para uso com Firebase Authentication e Firestore.
Quando o login estiver ativo, cada usuário utiliza seu próprio espaço isolado na nuvem.

## Como publicar no GitHub Pages

1. Envie os arquivos deste pacote para a raiz do repositório.
2. Garanta que o arquivo principal publicado seja `index.html`.
3. Ative o GitHub Pages na branch desejada.
4. Após publicar, faça um recarregamento completo do navegador para atualizar o cache do Service Worker.

## Versão deste pacote

**Financi 5.2**

### Ajustes desta versão
- corrigido o problema em que iniciar uma devolução e fechar sem confirmar criava um clone do produto;
- o botão **Manter dados apenas por Login** agora usa azul quando desligado e verde quando ativo;
- pacote GitHub atualizado com PWA, Service Worker, README, favicon, ícones Android e miniaturas do navegador baseados na identidade visual atual do Financi.
