1. 🛡️ Terminal de Alta Segurança - Cyber-SENAI
Este projeto é um sistema de autenticação simulado, desenvolvido para fins educacionais. Ele demonstra a implementação de lógica de validação de usuários, controle de tentativas de acesso e bloqueio de interface via JavaScript.

2. 🚀 Funcionalidades
Validação de Credenciais: Compara o input do usuário com uma base de dados local (Array de objetos).

Controle de Acesso: Permite até 3 tentativas de login.

Sistema de Bloqueio: Após a terceira falha, os campos de entrada e o botão são desabilitados, impedindo novas tentativas.

Feedback Visual: Mensagens coloridas indicando sucesso (verde), erro (laranja) ou bloqueio total (vermelho).

3. 🛠️ Tecnologias Utilizadas
HTML5: Estruturação da página e campos de formulário.

CSS3: Estilização básica e gerenciamento de estados visuais.

JavaScript (ES6): Lógica de autenticação, manipulação do DOM e controle de fluxo.

4. 📂 Como utilizar
Clone o repositório ou baixe o arquivo .html.

Abra o arquivo em qualquer navegador moderno.

Utilize uma das credenciais padrão da base de dados (ex: Usuário: user1 | Senha: pass1).

Teste o sistema de bloqueio inserindo credenciais incorretas três vezes consecutivas.

5. 🔍 Trecho de Código Relevante: Lógica de Bloqueio
O sistema utiliza um contador global para monitorar o estado do terminal:

JavaScript
if (tentativas > 0) {
    resDiv.innerText = `Login ou Senha incorretos! Restam ${tentativas} tentativas.`;
    resDiv.style.color = "orange";
} else {
    resDiv.innerText = "SISTEMA BLOQUEADO - Procure o Suporte";
    resDiv.style.color = "red";
    document.getElementById("username").disabled = true;
    document.getElementById("password").disabled = true;
}
