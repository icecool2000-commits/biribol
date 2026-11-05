# Biribol Oficial Mococa – app de presença

- App estático (PWA) publicado no GitHub Pages a partir da branch main: index.html, config.js, sw.js, manifest.webmanifest, ícones.
- Treinos: terça e quinta 19:00, domingo 10:00.
- Dados no Firebase Firestore, projeto `biribol-mococa` (plano Spark, grátis), coleções: treinos / presencas / config.
- Biribol e Basquete dividem o mesmo projeto Firebase: `firestore.rules` vale para os dois e é publicado à mão no console (Firestore → Regras). Mudou aqui, publique lá.
- Organizador: icecool2000@gmail.com (em `config.js` e em `firestore.rules`, sempre os dois juntos).
- Cada presença: id = nome normalizado, campos { nome, em (timestamp ou ms), uid }.
- A cada mudança de arquivo, subir a versão do cache em `sw.js` (const C) para todos receberem a atualização.
- Não usar mensagens automáticas no WhatsApp (não há API gratuita para grupos); o app usa link wa.me para compartilhar.
- Não reduzir as regras de segurança: qualquer um cria o próprio nome, só o dono tira o próprio, só o organizador edita tudo.
