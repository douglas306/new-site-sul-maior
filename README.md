Site Sul Maior Corretora (React + Vite)
```
npm install
npm run dev       # desenvolvimento
npm test          # testes (Vitest + Testing Library)
npm run build     # gera a pasta dist/ para publicar
```
Publique a pasta `dist/` (Netlify, Cloudflare Pages etc.). Domínio configurado: https://www.sulmaiorseguros.com.br
Textos e cartões: `src/data/content.ts`
Contatos e mensagens de WhatsApp: `src/lib/whatsapp.ts`
Estilos e imagens dos cartões (classes `.i-truck`, `.i-ware`...): `src/styles.css`. Para usar fotos, troque o `background-image` de cada classe por `url(/images/foto.jpg)` e coloque os arquivos em `public/images/`.
Publicar na Vercel
O projeto já vem com `vercel.json` (Vite, saída em `dist/`, cache e cabeçalhos de segurança).
Pelo CLI
```
npm install -g vercel
vercel login
vercel --prod
```
Pelo GitHub: envie esta pasta para um repositório, importe em vercel.com/new e clique em Deploy. As configurações são detectadas automaticamente.
Domínio: em Settings > Domains, adicione `www.sulmaiorseguros.com.br` e crie no DNS apenas o registro indicado pela Vercel (A ou CNAME). Não troque os nameservers sem antes anotar os registros MX do e-mail.
Foto do topo
A foto fica em `public/images/hero-caminhao.jpg`. Para trocar, substitua o arquivo mantendo o nome. Se ele não existir, o site mostra a ilustração.
