# Descrição

## Introdução

Este caderno Jupyter tem como objetivo criar uma base de dados sintética relacionada a **benefícios do INSS**, incorporando cenários de **fraudes** para fins didáticos e de análise. A base permite a exploração de padrões suspeitos e a aplicação de técnicas de identificação de irregularidades em concessão de benefícios.

O caso foi inspirado em uma ocorrência real descrita da seguinte forma:

> "A fraude foi detectada a partir de uma análise encaminhada pelo INSS. A PF disse também que o servidor investigado reativou temporariamente benefícios cessados por morte, alterando tanto o motivo da interrupção quanto os dados do titular, para receber os valores das aposentadorias na conta dele."  
> Fonte: [G1 - Notícia](https://g1.globo.com/pe/pernambuco/noticia/2023/07/04/servidor-do-inss-e-investigado-por-ressuscitar-beneficiarios-mortos-e-desviar-dinheiro-de-aposentadorias.ghtml)

## Estrutura da Base Sintética

A base sintética é composta por duas tabelas principais: **servidores** e **benefícios**, contendo atributos relevantes para análise e identificação de possíveis fraudes.

### **Tabela: Servidores**
| Coluna       | Descrição |
|-------------|------------|
| `id_servidor` | Matrícula do servidor concedente (0,1,2,...) |
| `uf_servidor` | Unidade da Federação do servidor concedente (AC, AL, AP, ...) |

### **Tabela: Benefícios**
| Coluna       | Descrição |
|-------------|------------|
| `id_beneficio` | Número do benefício (0,1,2,...) |
| `uf_beneficiario` | Unidade da Federação do beneficiário (AC, AL, AP, ...) |
| `id_servidor` | Matrícula do servidor concedente |
| `uf_servidor` | Unidade da Federação do servidor concedente (AC, AL, AP, ...) |
| `uf_coincidente` | Indica se a UF do servidor e do beneficiário é igual (`true/false`) |
| `reativado` | Indica se o benefício foi reativado (`true/false`) |
| `valor_beneficio` | Valor do benefício concedido |
| `tempo_analise` | Tempo de análise do benefício |

## Objetivo

Esta base permite o desenvolvimento de estudos, simulações e aplicações de **métodos de detecção de fraudes**, como:
- Identificação de padrões suspeitos em reativação de benefícios;
- Análise da relação entre servidores e concessão de benefícios;
- Detecção de inconsistências nos valores concedidos;
- Correlação entre tempo de análise e aprovação de benefícios suspeitos.

## Aviso

Os dados aqui apresentados são **fictícios** e foram gerados para fins **didáticos** e de **pesquisa**. 
O uso deste material deve se restringir a propósitos acadêmicos e de treinamento.

