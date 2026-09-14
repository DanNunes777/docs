---
icon: lucide/list
---

# Histórias de usuário

As histórias abaixo foram levantadas e validadas em reuniões com o cliente e representam o escopo funcional acordado para o sistema. Cada história é uma unidade de valor entregável, com critérios de aceitação próprios, e é referenciada por um identificador estável ao longo de toda a documentação, do backlog e dos testes.

---

## Convenções { #convencoes }

### Identificação

| Elemento | Formato | Exemplo | Regra |
| --- | --- | --- | --- |
| História | `US` + número sequencial | `US15` | Estável: nunca é renumerada, mesmo que a história mude de épico ou seja removida |
| Critério de aceitação | `US` + número + `-CA` + número | `US15-CA03` | Estável dentro da história; novos critérios entram no fim da lista |
| Épico | `EP` + número | `EP03` | Corresponde a um arquivo `.md` desta seção |

Identificadores removidos **não são reaproveitados**. Se `US14` for descartada, o número 14 permanece vago.

### Formato da história

Toda história segue o padrão **Connextra**:

> **Como** *&lt;perfil&gt;*, **eu quero** *&lt;ação&gt;*, **para que** *&lt;benefício&gt;*.

Os critérios de aceitação usam **Dado / Quando / Então** sempre que descrevem um comportamento observável; regras invariantes (restrições, permissões, validações) são escritas em forma afirmativa direta.

### Campos de rastreabilidade

Cada história declara dois campos de relacionamento, com significados diferentes:

- **Depende de** — histórias que precisam estar implementadas para que esta funcione. Define ordem de implementação.
- **Relaciona-se com** — histórias afetadas pela mesma regra de negócio ou que consomem/alimentam esta, sem bloqueá-la. Define impacto de mudança.

Os dois campos são consolidados na [matriz de rastreabilidade](../rastreabilidade/matriz.md), que também mostra o caminho inverso (quem referencia cada história).

### Links diretos

Cada história tem uma âncora própria e estável. Para referenciar uma história de qualquer lugar da documentação:

``` markdown
[US15](ep03-cadastro-acordos.md#us15)
```

Na navegação do site, o link resolve para `.../historias/ep03-cadastro-acordos/#us15`, apontando direto para a história — use esse endereço em issues, pull requests e commits.

### Como adicionar uma nova história

1. Escolha o épico ao qual ela pertence e abra o `.md` correspondente.
2. Use o próximo número livre da sequência global (não o próximo do épico).
3. Copie o bloco de uma história existente como modelo: título com âncora, citação Connextra, os três campos de rastreabilidade e os critérios numerados.
4. Preencha **Depende de** e **Relaciona-se com** e acrescente o link recíproco nas histórias citadas.
5. Inclua a história na tabela de resumo no topo do épico e na [matriz de rastreabilidade](../rastreabilidade/matriz.md).

---

## Épicos

| # | Épico | Histórias | Objetivo |
| --- | --- | --- | --- |
| EP01 | [Portal Institucional & Autenticação](ep01-portal-autenticacao.md) | US01–US06 | Vitrine pública e controle de acesso |
| EP02 | [Gestão de Usuários e Perfis](ep02-usuarios-perfis.md) | US07–US11 | Quem entra no sistema e com quais permissões |
| EP03 | [Cadastro de Acordos](ep03-cadastro-acordos.md) | US12–US24 | Estrutura do acordo: valores, honorários, parcelas, responsável |
| EP04 | [Acompanhamento de Parcelas](ep04-parcelas.md) | US25–US31 | Rotina mensal de baixa, atraso e auditoria |
| EP05 | [Comissões e Metas](ep05-comissoes-metas.md) | US32–US36 | Desempenho da equipe e visão financeira segmentada |
| EP06 | [Painel do Cliente](ep06-painel-cliente.md) | US37–US40 | Autonomia do síndico/administradora |
