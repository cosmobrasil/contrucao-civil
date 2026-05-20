# Status do Processo

Data: 2026-05-20

## Estágio atual

Fase de integração concluída: frontend Netlify publicado, backend Railway + PostgreSQL ativo e fluxo de consulta de CNPJ funcionando com fallback público quando a fonte principal não responde.

## Fase registrada

- Estruturação do frontend exclusivo em `frontend/`.
- Publicação automática via GitHub + Netlify.
- Criação do backend com cálculo de IGC, PCM, total e média de pontos.
- Integração com a EmpresaAqui preparada no backend.
- Fallback de consulta de CNPJ ativado no frontend para garantir operação contínua.
- Relatório final com gráfico doughnut do IGC validado no fluxo real.

## O que já foi feito

- Inserção do logo da Cosmob no cabeçalho.
- Criação da etapa de cadastro da empresa antes do questionário.
- Preparação do formulário para preenchimento manual e integração com a API da EmpresaAqui via backend.
- Ajuste do fluxo de navegação do questionário.
- Criação de `index.html` para entrada do deploy.
- Criação de `netlify.toml` para publicação estática.
- Criação do backend com cálculo de IGC, PCM, total e média de pontos.
- Criação da base para persistência em PostgreSQL.
- Geração do relatório final com gráfico doughnut do IGC.
- Publicação do repositório no GitHub para automação do deploy.
- Ajuste do fluxo de consulta de CNPJ para manter o preenchimento automático mesmo quando a API principal falhar.

## Próximo passo

- Monitorar a estabilidade do deploy na Netlify e na Railway.
- Refinar a origem oficial da consulta de CNPJ assim que a documentação completa da EmpresaAqui estiver disponível.
- Manter o relatório e as métricas alinhados com a regra de negócio final do projeto.
