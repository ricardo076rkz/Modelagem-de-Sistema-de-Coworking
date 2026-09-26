# Modelagem-de-Sistema-de-Coworking
🏢 WorkSpace: Modelagem de Sistema de Coworking Este repositório contém a modelagem estrutural (Diagrama de Classes UML) de um sistema de gestão para coworking, desenvolvido como exercício prático do curso de Análise e Desenvolvimento de Sistemas (ADS).

🎯 Sobre o Projeto
O objetivo desta prática foi traduzir as regras de negócio de uma empresa fictícia ("WorkSpace") para uma arquitetura orientada a objetos. O sistema foi desenhado para gerenciar membros, planos de assinatura, reservas de salas, recursos físicos e controle de fluxo de acesso (check-in).

A partir do "mini mundo" proposto, o diagrama mapeia as principais entidades do sistema e a forma como elas interagem entre si, garantindo que as regras de negócio sejam respeitadas antes mesmo de iniciar a codificação.

🛠️ Conceitos e Tecnologias Aplicadas
Neste projeto, apliquei conceitos fundamentais de Engenharia de Software e Programação Orientada a Objetos (POO):

Abstração: Identificação de classes centrais, atributos e métodos essenciais.

Relacionamentos e Multiplicidade: Definição de regras de cardinalidade (ex: 1..*) entre as entidades (como a relação entre Membros e Reservas).

Composição: Aplicação de regras de dependência estrita (ex: a subordinação entre a Sala e seus Recursos físicos).

Diagramas como Código (DaC): Utilização da linguagem Mermaid.js para estruturar o diagrama UML visualmente através de código, facilitando o versionamento e a manutenção.

🚀 Como visualizar
O diagrama foi construído utilizando blocos de código mermaid. O próprio GitHub renderiza o gráfico nativamente, então basta abrir o arquivo contendo o código para visualizar a estrutura completa das classes gerada de forma automática.

