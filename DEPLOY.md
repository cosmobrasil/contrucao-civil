# Deploy Railway + Netlify

## Backend no Railway

1. Crie um serviço Node.js apontando para este diretório.
2. Adicione um banco PostgreSQL no Railway.
3. Configure as variáveis de ambiente:
   - `DATABASE_URL`
   - `EMPRESAQUI_API_URL`
   - `EMPRESAQUI_TOKEN`
   - `EMPRESAQUI_TOKEN_HEADER=Authorization`
   - `CORS_ORIGIN=https://seu-site.netlify.app`
   - `PGSSLMODE=require`
4. Inicie o serviço com `npm start`.
5. Valide:
   - `GET /health`
   - `GET /api/health`
   - `GET /api/questions`
   - `GET /api/company/lookup?documento=...`
   - `POST /api/assessments`

## Frontend na Netlify

1. Mantenha `publish = "frontend"` no `netlify.toml`.
2. Publique o site normalmente.
3. A página principal do deploy fica em `frontend/index.html`.
4. O questionário fica em `frontend/questionario_circularidade/index.html` e é servido em `/questionario_circularidade/`.
5. Edite `frontend/questionario_circularidade/config.js` e defina:
   - `window.COSMOBRASIL_API_BASE_URL = "https://backend-production-5b5cc.up.railway.app";`
4. Teste o fluxo completo:
   - cadastro da empresa
   - preenchimento automático via EmpresaAqui
   - respostas do questionário
   - relatório final com IGC e PCM

## Observações

- O frontend usa `config.js` para apontar para o backend.
- O backend usa `EMPRESAQUI_TOKEN` apenas no servidor.
- Não coloque o token dentro do HTML público.
