# Studio — testes de sites 3D

Cada teste vive na sua própria pasta e é servido em `/<pasta>`.

| Pasta | Teste |
|---|---|
| `kimi/` | Kimi Antonelli — GRIDO1 Racing Systems (three.js + Lenis, arquivo único) |
| `soda/` | Diet Soda — Pure Zero (GSAP + model-viewer, arquivo único) |

A raiz (`index.html`) lista os testes. O repositório está ligado ao projeto
`studio-impacto-soda` na Vercel: cada push no `main` publica em
https://studio-impacto-soda.vercel.app.

Os assets do `kimi/` passam pelo próprio domínio através do rewrite em `vercel.json`
(`/assets/kimi-04a9449ab2/*` → `storage.getlayers.ai`), então texturas, o modelo do
capacete e as máscaras CSS carregam sem depender dos cabeçalhos CORS do bucket.
Aberto direto do disco, o `index.html` fica sem assets — use a URL da Vercel.
