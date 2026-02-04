## Autenticação

Todas as requisições devem conter um cabeçalho de autenticação do tipo **Bearer Token**.

### Exemplo de cabeçalho:



O token é obtido através de uma requisição ao endpoint `/Token`. Necessário solicitar o username e password via email: desenvolvimento@versatilis.com.br.

### Gerar Token de Acesso

+ **Método:** `POST`
+ **URL:** `https://<link_do_cliente>/Token`
+ **Headers:**
    + `Content-Type: Content-Type: text/plain`
+ **Body:**

        username={{SOLCIITAR-USERNAME}}&password={{SOLICITAR-PASSWORD}}&grant_type=password

A resposta dessa requisição conterá o token necessário para autenticação das chamadas subsequentes.