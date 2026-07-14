# ShelfCheck

Aplicacao web para registrar e acompanhar conferencias diarias de produtos em lojas de varejo.

## Visao Geral

O ShelfCheck centraliza o processo de conferencia de produtos em um unico lugar, substituindo registros manuais e mensagens soltas.

No MVP, a aplicacao permite:

- visualizar a conferencia do dia;
- abrir produtos da lista;
- registrar status da verificacao;
- adicionar observacao e foto;
- acompanhar o progresso da conferencia;
- salvar os dados localmente no navegador.

## Problema Resolvido

Hoje a conferencia costuma ser feita de forma manual: percorrer corredores, verificar area de venda, buscar no estoque, tirar fotos e comunicar pendencias. O ShelfCheck organiza esse fluxo em uma rotina unica e rastreavel.

## Publico-Alvo

- funcionarios responsaveis pela conferencia de produtos;
- evolucao futura para lideres, supervisores e gerentes.

## Fluxo Principal

1. Selecionar conferencia.
2. Selecionar produto.
3. Verificar area de venda.
4. Se encontrado, organizar gondola, registrar foto e finalizar.
5. Se nao encontrado, buscar no estoque.
6. Se encontrado no estoque, abastecer, organizar, registrar foto e finalizar.
7. Se nao encontrado no estoque, registrar observacao, notificar superior e finalizar.

## Status de Produto

- Pendente: produto ainda nao conferido.
- Conferido: produto ja estava na area de venda.
- Abastecido: produto foi encontrado no estoque e reposto.
- Nao encontrado: produto nao foi localizado.

## Requisitos do MVP

### Funcionais

- Exibir conferencia do dia.
- Exibir lista de produtos da conferencia.
- Permitir selecao de produto.
- Permitir informar se encontrou na area de venda.
- Permitir informar se encontrou no estoque.
- Permitir registrar observacao.
- Permitir anexar foto.
- Salvar conferencia do produto.
- Atualizar progresso automaticamente apos salvar.
- Retornar para lista apos salvar.

### Nao Funcionais

- Mobile First.
- Interface responsiva.
- Compatibilidade com navegadores modernos.
- Persistencia local via LocalStorage.
- Uso com uma mao em dispositivos moveis.
- Interface simples e intuitiva.
- Progresso mantido mesmo apos fechar navegador.

## Tecnologias

MVP planejado com:

- HTML5
- CSS3
- JavaScript
- LocalStorage

## Estrutura Atual do Projeto

- index.html
- doc/01-PRD.md
- doc/02-requesitos.md

## Como Executar Localmente

Como o projeto esta em estrutura simples de frontend, voce pode abrir o arquivo index.html diretamente no navegador.

Opcao recomendada:

1. Usar uma extensao de servidor local (ex.: Live Server no VS Code).
2. Abrir a pasta do projeto.
3. Iniciar o servidor e acessar a URL local gerada.

## Roadmap

- MVP: dashboard, conferencia, produtos, status, foto, observacao, LocalStorage.
- v2: historico.
- v3: React.
- v4: API REST.
- v5: banco de dados.
- v6: login.
- v7: dashboard administrativo.

## Status do Projeto

Fase atual: discovery e definicao de requisitos.
