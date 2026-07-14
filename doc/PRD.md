# PRD — ShelfCheck

> Versão: 1.1
>
> Status: Discovery
>
> Autor: Alexandre Ramos
>
> Curso: Engenharia de Software — Descomplica

## 1. Visão Geral

**Nome:** ShelfCheck

**Objetivo:** desenvolver uma aplicação web para registrar e acompanhar conferências diárias de produtos em lojas de varejo.

Cada conferência representa uma rotina de trabalho composta por diversos produtos que precisam ser verificados.

O sistema centraliza todas as informações da conferência em um único local.

## 2. Problema

Atualmente, a conferência é realizada manualmente.

O funcionário precisa:

- percorrer diversos corredores;
- localizar produtos específicos;
- verificar disponibilidade na área de venda;
- procurar o produto no estoque quando necessário;
- abastecer a gôndola;
- registrar fotos;
- comunicar produtos não encontrados ao superior.

Esse processo depende de memória, mensagens e fotos enviadas separadamente.

## 3. Objetivo do Produto

Centralizar toda a conferência diária em uma única aplicação.

## 4. Público-alvo

O público principal é composto por funcionários responsáveis pela conferência de produtos.

No futuro, o sistema também poderá ser usado por:

- líderes;
- supervisores;
- gerentes.

## 5. Conceitos do Sistema

### Conferência

Representa uma rotina diária de verificação.

Exemplo:

- Conferência
- Data: 15/07/2026
- Marca Própria
- Produtos

### Produto

Cada produto pertence a uma conferência.

Cada produto possui seu próprio resultado.

## 6. Fluxo Principal

```text
Selecionar conferência
↓
Selecionar produto
↓
Ir até a área de venda
↓
Produto encontrado?
├── SIM
│   ├── Organizar gôndola
│   ├── Registrar foto
│   └── Finalizar
└── NÃO
	↓
	Procurar no estoque
	↓
	Encontrou?
	├── SIM
	│   ├── Abastecer
	│   ├── Organizar
	│   ├── Registrar foto
	│   └── Finalizar
	└── NÃO
		↓
		Registrar observação
		↓
		Notificar superior
		↓
		Finalizar
```

## 7. Funcionalidades do MVP

### Conferência

- visualizar a conferência do dia;
- acompanhar o progresso;
- visualizar a quantidade restante.

### Produto

- abrir produto;
- informar se estava na área de venda;
- informar se foi encontrado no estoque;
- adicionar observação;
- adicionar foto;
- salvar resultado.

## 8. Status

| Status         | Significado                        |
| -------------- | ---------------------------------- |
| Pendente       | Produto ainda não conferido        |
| Conferido      | Produto já estava na área de venda |
| Abastecido     | Produto foi encontrado no estoque  |
| Não encontrado | Produto não localizado             |

## 9. Dados da Conferência

| Campo                | Descrição                            |
| -------------------- | ------------------------------------ |
| id                   | Identificador da conferência         |
| data                 | Data da conferência                  |
| responsável          | Usuário responsável pela conferência |
| total de produtos    | Quantidade total de produtos         |
| quantidade conferida | Quantidade já finalizada             |

## 10. Dados do Produto

| Campo                 | Descrição                                     |
| --------------------- | --------------------------------------------- |
| id                    | Identificador do produto                      |
| nome                  | Nome do produto                               |
| categoria             | Categoria do produto                          |
| corredor              | Corredor onde o produto está localizado       |
| status                | Situação atual do produto                     |
| área de venda         | Indica se o produto estava na área de venda   |
| encontrado no estoque | Indica se o produto foi localizado no estoque |
| observação            | Observação registrada pelo usuário            |
| foto                  | Foto associada ao produto                     |
| data da conferência   | Data em que o item foi conferido              |
| hora                  | Hora do registro                              |

## 11. Dashboard

O sistema deverá apresentar:

- Conferência de Hoje;
- 32 / 48 produtos;
- 67%;
- Conferidos;
- Abastecidos;
- Não encontrados;
- Pendentes.

## 12. Tecnologias

### MVP

- HTML5;
- CSS3;
- JavaScript;
- LocalStorage.

## 13. Funcionalidades Futuras

- Login;
- API;
- Banco de dados;
- Histórico de conferências;
- Pesquisa;
- Filtros;
- Dashboard gerencial;
- Relatórios;
- Exportar PDF;
- Aplicativo mobile.

## 14. Critérios de Sucesso

O MVP será considerado concluído quando permitir:

- criar uma conferência;
- registrar todos os produtos;
- acompanhar o progresso;
- salvar localmente;
- consultar os resultados.

## 15. Roadmap

| Versão | Entregas                                                                 |
| ------ | ------------------------------------------------------------------------ |
| MVP    | Dashboard, conferência, produtos, status, foto, observação, LocalStorage |
| v2     | Histórico                                                                |
| v3     | React                                                                    |
| v4     | API REST                                                                 |
| v5     | Banco de dados                                                           |
| v6     | Login                                                                    |
| v7     | Dashboard administrativo                                                 |
