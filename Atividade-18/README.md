# Atividade 18 — Diagrama de Classes do BiblioTech

**Nome:** Kauan  
**Turma:** 2º ano — Técnico em Informática Integrado  

## Diagrama
![Diagrama de Classes do BiblioTech](diagrama-classes.png)

## Por que estes números (associação Bibliotecario — Emprestimo)
- Perto de Emprestimo eu coloquei **`0..*`** porque um bibliotecário pode registrar zero ou vários empréstimos ao longo de sua rotina.
- Perto de Bibliotecario eu coloquei **`1`** porque cada empréstimo individual é registrado no balcão por exatamente um bibliotecário.

## Rastreabilidade (nível B)
- A operação `calcularDevolucao()` da classe `Emprestimo` atende ao caso de uso **`Emprestar Livro`**.

## Enxugamento do Diagrama (nível A)
- **O que foi mantido enxuto:** Evitou-se duplicar dados como `nome` ou `titulo` dentro de `Emprestimo` ou `Bibliotecario`. Os dados de usuário são herdados de `Usuario` e as referências de livro/leitor são obtidas pelas associações, evitando atributos redundantes.

## Defesa da Estrutura (nível A — Objeção)
- **Resposta à objeção do atributo `bibliotecario: String`:** O colega não está certo. Usar apenas um texto simples impede que o bibliotecário seja tratado como um `Usuario` do sistema (perdendo o reuso de `entrar()`), não guarda a `matriculaFuncional` para auditoria e permite erros de digitação. Uma classe própria garante integridade e rastreabilidade real.

## Autoavaliação
- **Conceito que pretendo:** A
- **Onde isso se prova no diagrama:**
  - **Classes e Herança:** 5 classes base + classe `Reserva`, com `Leitor` e `Bibliotecario` herdando de `Usuario` (triângulo oco apontando para a classe mãe).
  - **Ligação Bibliotecario - Emprestimo:** Linha contínua com rótulo `registra`, multiplicidade `1` em `Bibliotecario` e `0..*` em `Emprestimo`.
  - **Atividade extra e defesa:** Inclusão da classe `Reserva` associada ao `Leitor`, mapeamento de rastreabilidade e resposta fundamentada à objeção.