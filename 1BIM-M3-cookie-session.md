## Instituição
Etec Vasco Antônio Venchiarutti.

## Curso
Desenvolvimento de Sistemas
## Turma
2°C¹
## Autores
Nathan Nabas, Matheus e Nathan Gabriel

### Exercício 1 — Pergunta conceitual

Cookies e sessions são mecanismos utilizados no PHP para armazenar informações entre diferentes requisições feitas pelo usuário ao acessar um site. Isso é necessário porque, por padrão, o protocolo HTTP não mantém memória entre uma ação e outra. Os cookies são armazenados diretamente no navegador do usuário, permitindo que certas informações permaneçam mesmo após fechar o site. Já as sessions armazenam os dados no servidor, mantendo no navegador apenas um identificador da sessão. Em termos de segurança, as sessions são mais confiáveis, pois os dados não ficam expostos ao usuário. Dessa forma, cookies são mais usados para dados simples e persistentes, enquanto sessions são indicadas para informações mais importantes e sensíveis.

### Exercício 2 — Pergunta de aplicação

#### Manter o usuário logado:
 - Para manter o usuário logado, o mais adequado é utilizar sessions, pois os dados de autenticação ficam armazenados no servidor, o que garante mais segurança. A cada requisição, o sistema identifica o usuário por meio do ID da sessão, evitando que informações importantes fiquem expostas. Em alguns casos, pode-se usar cookies como complemento, como na função “lembrar de mim”.

#### Armazenar itens temporários no carrinho:
- Os itens do carrinho devem ser armazenados em sessions, já que são dados que mudam com frequência e precisam ser protegidos contra alterações indevidas. Como ficam no servidor, o usuário não consegue manipular diretamente essas informações, o que ajuda a manter a integridade dos dados, como quantidade e valores dos produtos.

#### Registrar preferências do usuário:
- Para registrar preferências, como idioma ou tema do site, o ideal é utilizar cookies, pois são dados simples e não sensíveis. Além disso, os cookies permitem que essas informações continuem salvas mesmo após o usuário fechar o navegador, melhorando a experiência ao retornar ao site.

#### Justificativa:
 - O uso combinado de cookies e sessions é importante porque cada um resolve um tipo de problema dentro do sistema. As sessions garantem mais segurança, já que armazenam os dados no servidor, sendo ideais para informações sensíveis como login e carrinho de compras. Por outro lado, os cookies oferecem praticidade, pois ficam no navegador e permitem manter preferências do usuário mesmo após ele sair do site. Assim, utilizar os dois de forma adequada melhora tanto a proteção dos dados quanto a experiência do usuário, tornando o sistema mais eficiente e confiável.
