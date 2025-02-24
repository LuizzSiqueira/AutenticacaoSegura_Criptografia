## Objetivo do Projeto
Garantir a segurança da comunicação entre funcionários, protegendo mensagens sensíveis contra acessos não autorizados. Isso será feito por meio de hashing seguro de senhas, autenticação via tokens JWT e criptografia assimétrica e simétrica.

## Tecnologias Utilizadas

- **bcrypt**: Para hashing seguro de senhas. Usaremos a versão 4.2.1. 
- **PyJWT**: Para geração e verificação de tokens JWT. Usaremos a versão 2.10.1.
- **cryptography**: Para implementação da criptografia AES e RSA. Usaremos a versão 39.0.1
=======
- **bcrypt**: Para hashing seguro de senhas.
- **PyJWT**: Para geração e verificação de tokens JWT.
- **cryptography**: Para implementação da criptografia AES e RSA.
- **hashlib, base64, os**: Para suporte auxiliar à criptografia e manipulação de dados.

## Fluxo Básico do Sistema
1. **Cadastro de Usuário**: Senha armazenada de forma segura utilizando bcrypt.
2. **Login**: Autenticação via JWT para acesso ao sistema.
3. **Envio de Mensagem**: Mensagem criptografada com AES antes de ser armazenada.
4. **Recebimento de Mensagem**: O destinatário descriptografa a chave AES com sua chave RSA privada para acessar a mensagem.
