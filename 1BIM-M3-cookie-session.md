## Instituição
Etec Vasco Antônio Venchiarutti.

## Curso
Desenvolvimento de Sistemas
## Turma
2°C¹
## Autores
Nathan Nabas e Matheus

### Exercício 1 — Pergunta conceitual

Cookies e sessions são usados para armazenar dados entre requisições no PHP.
Os cookies ficam armazenados no navegador do usuário, enquanto as sessions ficam no servidor.
Em termos de segurança, sessions são mais seguras, pois os dados não ficam expostos ao usuário. Já os cookies são menos seguros, podendo ser acessados ou alterados.
Assim, cookies são mais indicados para dados simples e não sensíveis, enquanto sessions são usadas para informações importantes, como autenticação.

### Exercício 2 — Pergunta de aplicação
- Manter o usuário logado
O uso de sessions é o mais adequado, pois os dados de autenticação ficam armazenados no servidor, garantindo maior segurança e evitando manipulação pelo usuário.

- Armazenar itens temporários no carrinho
Também é recomendado o uso de sessions, já que o carrinho envolve dados que mudam com frequência e precisam ser protegidos contra alterações indevidas.

- Registrar preferências do usuário
Nesse caso, o ideal é utilizar cookies, pois são dados simples e não sensíveis, além de permanecerem armazenados mesmo após o usuário fechar o navegador.

- Justificativa
O uso combinado de cookies e sessions permite equilibrar segurança e praticidade, utilizando sessions para dados críticos e cookies para melhorar a experiência do usuário.
