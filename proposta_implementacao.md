# Proposta de Implementação

## Uso das Tecnologias
Cada tecnologia será usada para garantir a segurança do sistema:
- **bcrypt**: Hash de senhas para evitar armazenamento de credenciais em texto puro.
- **JWT**: Autenticação baseada em tokens para sessões seguras.
- **AES (CBC)**: Criptografia simétrica para proteger as mensagens enviadas.
- **RSA**: Proteção da chave AES para garantir que apenas o destinatário correto possa descriptografar a mensagem.

## Principais Etapas de Implementação
1. **Cadastro de Usuário**:
   - O sistema receberá uma senha e a armazenará de forma segura utilizando bcrypt.
2. **Login**:
   - O sistema validará a senha usando bcrypt e, se correta, gerará um token JWT.
3. **Criptografia de Mensagens**:
   - A mensagem será criptografada utilizando AES (CBC) antes de ser salva.
4. **Proteção da Chave AES**:
   - A chave AES será criptografada com RSA antes de ser armazenada, garantindo que apenas o destinatário correto consiga descriptografá-la.

## Armazenamento Seguro de Dados
- As senhas serão armazenadas apenas como hashes.
- As chaves privadas RSA dos usuários serão protegidas e não serão armazenadas no banco de dados.
- Tokens JWT terão um tempo de expiração e serão validados a cada requisição.
