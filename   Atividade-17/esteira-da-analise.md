# Esteira da Análise — BiblioTech

**Estudante:** Kauê Mendes

## Funcionalidade 1: ____Renovar empréstimo_____

- **1.1 Fala do cliente:** "Os alunos vivem pedindo para aumentar o prazo do livro quando não terminaram de ler, aí eu tenho que ir no caderno e rasurar a data antiga pra colocar uma nova."
- **1.2 História de usuário:** Como ___Leitor___, quero __Renovar o prazo do emprestimo de um livro____, para ter mais tempo para terminar a leitura sem gerar pendências ou multas.__.
- **1.3. Requisito:** RF01 — O sistema deve permitir que o leitor renovar o prazo de um empréstimo ativo.
- **1.4 Caso de uso (RF01):** Ator leitor → "renovar empréstimo " (verbo + objeto)

## Funcionalidade 2: Reservar livro

- **1. Fala do cliente:** "Os alunos pedem muito pra guardar um livro que está emprestado com outra pessoa, pra ninguém pegar na frente quando ele for devolvido"
- **2. História de usuário:** Como leitor, quero reservar um livro que está atualmente emprestado, para garantir minha prioridade de retirada assim que ele for devolvido.
- **3. Requisito:** RF02 —O sistema deve permitir que o leitor solicite a reserva de um livro que esteja emprestado.
- **4. Caso de uso (RF02):** Ator Leitor → "Reservar livro" (verbo + objeto)

## Rastreabilidade

| Elipse no diagrama | Veio do requisito | Que veio da fala |
|---|---|---|
| | RF01 | ".Os alunos vivem pedindo para aumentar o prazo do livro.." |
| | RF02 | ".Os alunos pedem muito pra guardar um livro que está emprestado.." |

Renovar empréstimo: A necessidade surgiu quando a bibliotecária comentou que precisava rasurar as datas no caderno sempre que um leitor pedia mais tempo para devolver um livro. Essa situação mostrou um problema real: o leitor precisava renovar o empréstimo para evitar multas. A partir disso, foi criada uma História de Usuário, depois sintetizada no RF01 - "permitir a renovação do prazo" - e, finalmente, representada pelo caso de uso "Renovar empréstimo", realizado pelo Leitor ou pelo Bibliotecário, quando o atendimento ocorre no balcão.
Reservar livro: A ideia nasceu da fala sobre a necessidade de "guardar" um livro que já estava emprestado. Por trás desse pedido estava o desejo do leitor de garantir sua posição na fila de espera e ter prioridade assim que o exemplar fosse devolvido. Essa necessidade deu origem a uma História de Usuário, que foi resumida no RF02 e representada no diagrama pelo caso de uso "Reservar livro", associado ao ator Leitor.

## Relacionamento entre casos de uso (nível A)

- Tipo: «include»
- Entre: `Reservar livro` (caso base) e `Consultar acervo` (caso incluído)
- Por que é esse e não o outro: É um «include» porque o sistema **SEMPRE** precisa consultar o acervo para verificar o status atual e a existência do livro antes de confirmar a reserva. Não é opcional (o que seria um «extend»), mas sim um passo obrigatório para que o processo de reserva seja concluído.

## Autoavaliação

**Conceito pretendido:** _A__ (A / B / C)

- Conversei sobre esta atividade com: ninguem_ (ou "ninguém")
- Esteira da análise: __As duas funcionalidades percorrem todas as 4 estações em ordem exata, partindo da fala do cliente entre aspas até o caso de uso em verbo + objeto._ 
- Diagrama e notação: O diagrama possui a fronteira `BiblioTech`, atores externos, associações contínuas sem seta e relacionamento de «include» tracejado com direção correta.
- Rastreabilidade: Mapeada tanto na tabela quanto no detalhamento em texto conectando fala, história, código RF e caso de uso.
- Organização da entrega: asta `Atividade-17` criada com  os 4 arquivos  (`README.md`, `esteira-da-analise.md`, `diagrama-casos-de-uso.png` e `diagrama-casos-de-uso.drawio`).