# Escopo do Projeto

## Objetivo do Projeto
Garantir a segurança da comunicação entre funcionários, protegendo mensagens sensíveis contra acessos não autorizados. Isso será feito por meio de hashing seguro de senhas, autenticação via tokens JWT e criptografia assimétrica e simétrica.

## Tecnologias Utilizadas
- bcrypt: Para hashing seguro de senhas.
- PyJWT: Para geração e verificação de tokens JWT.
- cryptography: Para implementação da criptografia AES e RSA.
- hashlib, base64, os: Para suporte auxiliar à criptografia e manipulação de dados.

## Fluxo Básico do Sistema
- Cadastro de Usuário: Senha armazenada de forma segura utilizando bcrypt.
- Login: Autenticação via JWT para acesso ao sistema.
- Envio de Mensagem: Mensagem criptografada com AES antes de ser armazenada.
- Recebimento de Mensagem: O destinatário descriptografa a chave AES com sua chave RSA privada para acessar a mensagem.
