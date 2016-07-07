# Minha visão sobre ADRs

Volte para o [índice](README.md).

## Contexto

Várias vezes eu olhei para um sistema ou código e vi decisões que não
faziam sentido ou que tinham alternativas melhores, e isso teve dois
efeitos:

- xinguei muito no twitter
- trabalhei em volta do problema ao invés de considerar se devia arrumar

Quando encontramos algo que não entendemos no código, podemos **aceitar
cegamente** e trabalhar do jeito que está, ou **negar cegamente** e
reescrever do zero. No primeiro caso ficamos com uma solução ruim que
atrapalha a evolução, e no segundo caso podemos cair na falácia de "eu
com certeza faço melhor".

Mas depois de um tempo, aprendi uma coisa muito importante: toda decisão
tomada durante um projeto tem uma explicação, que pode inclusive ser
falta de conhecimento. Até mesmo decisões atuais podem ser ruins no
futuro quando o sistema evolui.

Aprendi sobre
[ADRs](http://thinkrelevance.com/blog/2011/11/15/documenting-architecture-decisions)
(**A**rchitecture **D**ecision **R**ecords) durante o meu último
projeto, e passamos a usá-lo para registrar nossas decisões de
arquiteturas.

## Decisão

Os ADRs serão utilizados para registrar todas as decisões de arquitetura
que o time considerar importantes.

Os ADRs serão armazenados num repositório git, em formato markdown.
Muitas plataformas de hospedagem renderizam markdown muito bem, tipo
github, gitlab, bitbucket, etc.

Os ADRs serão numerados sequenciamente. Ex.: `ADR-001-descricao.md`

Os ADRs não são muito longos, pois a idéia é seja simples de ler e
entender as decisões de arquitetura.

Os ADRS tem as seções **título**, **contexto**, **decisão**, **status**
e **consequências**.

O contexto deve descrever o problema de maneira objetiva. É legal
explicar quais são as forças em conflito, tipo **tempo disponível** vs.
**complexidade**, ou **familiaridade** vs. **adequação**. A decisão
descreve qual foi a solução escolhida. O status descreve se a ADR foi
proposta, aceita ou se foi tornada obsoleta por outra ADR. Nas
consequências, deve-se descrever as consequências positivas e negativas,
que podem afetar o projeto no futuro.

## Status

Aceita

## Consequências

Agora é mais fácil para pessoas novas entenderem o estado atual do
projeto, sendo um ótimo jeito de fazer onboarding de pessoas. Além
disso, o time pode tomar decisões mais informadas sobre seguir ou não
com uma determinada solução, pois toda a lógica para a escolha está
descrita. A contrapartida é manter o repositório atual, pois uma vez que
existe a dúvida se ele é usado, as pessoas passam a ignorar o que está
escrito nele.
