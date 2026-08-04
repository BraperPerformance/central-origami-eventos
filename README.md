[LEIA-ME-DEPLOY.txt](https://github.com/user-attachments/files/30686116/LEIA-ME-DEPLOY.txt)
CENTRAL DO CLIENTE BMX — INSTRUÇÕES DE DEPLOY (v1.5)
====================================================

A RAIZ do repositório central-bmx deve ficar EXATAMENTE assim:

  index.html          <- o portal (com tela de login)
  assets/             <- logos + favicon
  docs/               <- os 5 documentos publicados
  LEIA-ME-DEPLOY.txt  <- este arquivo (opcional manter)

PASSO A PASSO
1) Descompacte este ZIP. Os arquivos já saem SOLTOS (sem pasta embrulhando).
2) No GitHub (repo central-bmx), a raiz do repositório deve conter index.html.
   IMPORTANTE: se existir na raiz QUALQUER outro arquivo .html antigo
   (ex.: bmx_status_*.html, dashboard, index antigo), APAGUE antes do commit.
   O Vercel serve o index.html da raiz — se houver outro, é ele que abre.
3) No Vercel, o projeto deve apontar para a RAIZ do repo
   (Settings > Root Directory = ./ , Framework Preset = Other).
4) Após o deploy, abra a URL e force atualização: Ctrl+Shift+R
   (o Vercel/navegador guarda cache da versão anterior).
5) Confira os arquivos publicados contra o checksums.txt:
   a URL /index.html deve bater com o md5 da lista.

TESTE DE ACEITE (30 segundos)
- Abrir https://central-bmx.vercel.app/  -> deve aparecer a TELA DE LOGIN
  (logo BMX + campos Nome e Senha).
- Entrar com um nome do grupo + senha -> abre o Início com os cards.
- Se abrir qualquer relatório direto, há um HTML antigo na raiz do repo
  ou o Root Directory do Vercel aponta para a pasta errada.

Suporte: equipe Braper
