PROJETO HIPERTROFIA — VERSÃO COM LOGIN GOOGLE

IMPORTANTE: antes de usar a sincronização, configure o banco seguindo estes passos.

1. No Supabase, abra SQL Editor.
2. Clique em New query.
3. Abra CONFIGURAR_SUPABASE.sql, copie todo o conteúdo, cole no editor SQL e clique em Run.
4. No Supabase > Authentication > URL Configuration, Site URL deve ser https://arthurcsc1914.github.io/projeto-hipertrofia/ e Redirect URLs deve incluir esse mesmo endereço.
5. Em Google Cloud > OAuth client, Authorized JavaScript origins deve ser https://arthurcsc1914.github.io (sem barra final). Authorized redirect URI deve ser o Callback URL exibido no Supabase, normalmente https://SEU-PROJETO.supabase.co/auth/v1/callback.
6. Substitua os arquivos index.html, manifest.json e sw.js do repositório GitHub pelos arquivos desta pasta. Inclua CONFIGURAR_SUPABASE.sql no repositório se desejar, mas ele não é necessário para o site público.
7. Aguarde o GitHub Pages atualizar e abra o site. Clique Entrar com Google.

A chave sb_publishable é uma chave pública apropriada para frontend. Nunca coloque chaves sb_secret ou service_role no site. A proteção dos dados depende da tabela e das políticas RLS do SQL acima.

NOTA: os registros antigos que estavam apenas no navegador não são migrados automaticamente para a nuvem. Guarde o aparelho/navegador antigo até confirmar que não precisa dos registros antigos.
