## Funcionalidades do Sistema

1. **Cadastro de Usuário**:
   - O usuário fornecerá nome, e-mail e senha.
   - A senha será armazenada de forma segura com bcrypt.

2. **Login**:
   - O sistema validará a senha com bcrypt.
   - Se correta, gerará um token JWT para autenticação.

3. **Envio de Mensagem**:
   - O remetente escreverá uma mensagem.
   - A mensagem será criptografada com AES antes de ser salva.
   - A chave AES será criptografada com RSA usando a chave pública do destinatário.

4. **Recebimento de Mensagem**:
   - O destinatário receberá a mensagem criptografada.
   - Ele descriptografará a chave AES usando sua chave privada RSA.
   - A mensagem será finalmente descriptografada com AES e exibida ao usuário.
