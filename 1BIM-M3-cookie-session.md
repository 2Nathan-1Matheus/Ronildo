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

### Exercício 3 — Pergunta de investigação:

Ao executar o arquivo `teste.php` pela primeira vez no navegador, apareceu a mensagem **“Cookie ainda não disponível.”**
Isso acontece porque o comando `setcookie("contador", "1", time()+3600);` apenas envia a instrução para o navegador criar o cookie, mas ele ainda não fica disponível na mesma execução do script.

Depois de atualizar a página, apareceu a mensagem **“Valor do cookie: 1”**.
Nessa etapa, o navegador já havia salvo o cookie e o enviou de volta ao servidor na nova requisição, permitindo que o PHP acessasse o valor por meio de `$_COOKIE["contador"]`.

Ao abrir as ferramentas do navegador (`F12`) e acessar a aba de cookies, foi possível visualizar o cookie chamado **contador**, com o valor **1** e tempo de expiração de aproximadamente **1 hora**.

Depois de limpar os cookies do site e atualizar novamente, a mensagem voltou a ser **“Cookie ainda não disponível.”**, pois o cookie foi apagado do navegador.
Ao atualizar mais uma vez, ele reapareceu com o valor **1**, repetindo o mesmo processo inicial.

O cookie não aparece imediatamente na primeira execução porque ele só fica disponível na **próxima requisição feita pelo navegador**.
Ou seja, primeiro o servidor envia o cookie, o navegador salva, e somente no próximo carregamento da página ele retorna esse valor ao PHP.

### Exercício 4 — Por que sessions são preferidas na autenticação

As sessions são preferidas na autenticação de usuários porque oferecem mais segurança, controle e confiabilidade em relação aos cookies.

**Segurança:**

Nas sessions, os dados ficam armazenados no servidor, e o navegador guarda apenas um ID de sessão. Assim, informações sensíveis não ficam expostas ao usuário.
Já os cookies ficam no navegador e podem ser acessados ou alterados.

**Manipulação de dados:**

Sessions permitem armazenar dados mais complexos e são facilmente controladas no servidor.
Cookies têm limitações e exigem mais cuidados para evitar alterações indevidas.

**Controle:**

Sessions podem ser encerradas com session_destroy() e expiram automaticamente após um tempo de inatividade.
Cookies podem continuar ativos mesmo após o usuário sair, dependendo da configuração.

**Riscos dos cookies:**

Usar apenas cookies pode causar problemas como:

alteração de dados pelo usuário
roubo de cookies
exposição de informações sensíveis

**Conclusão**

As sessions são mais seguras e eficientes para autenticação, pois mantêm os dados protegidos no servidor. Os cookies devem ser usados apenas como complemento ou para informações não sensíveis.

