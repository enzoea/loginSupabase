# loginSupabase

Login com Supabase
Este projeto é um exemplo simples de sistema de login com Supabase utilizando autenticação por e-mail e senha.

🚀 Tecnologias
HTML

JavaScript

Supabase (Backend-as-a-Service)

📋 Pré-requisitos
Antes de rodar o projeto, você precisa:

Criar uma conta gratuita no Supabase

Criar um novo projeto

Ir até a aba "Project Settings" > "API" para copiar:

A URL do projeto

A anon public key

🛠️ Configuração no Código
Abra o arquivo login.html (ou o arquivo onde está configurado o Supabase) e substitua os valores abaixo pelas informações do seu projeto:

javascript
Copiar
Editar
const supabase = supabase.createClient(
  "https://<SUA-URL>.supabase.co", 
  "<SUA-CHAVE-ANON>"
);
✅ Fluxo de Login
O usuário insere e-mail e senha

O Supabase autentica e gera uma sessão

Você pode implementar um sistema pós-login (como redirecionamento ou dashboard)

📦 O que fazer após o login?
Depois que o usuário estiver logado, você pode:

Redirecionar para uma área restrita

Armazenar os dados do usuário em uma tabela no Supabase

Usar a sessão atual com supabase.auth.getSession() para verificar login

Criar um CRUD conectado ao Supabase usando o ID do usuário

Exemplo de captura da sessão:

javascript
Copiar
Editar
const { data: { session } } = await supabase.auth.getSession();
console.log(session);
