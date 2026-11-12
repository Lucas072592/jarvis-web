JARVIS WEB 1.0 — GUIA RÁPIDO

O que funciona nesta versão:
- Interface futurista adaptada para celular.
- Reconhecimento de voz do navegador (Web Speech API, quando suportada).
- Resposta falada usando as vozes instaladas no aparelho.
- Entrada por texto.
- Respostas locais simples para data, hora e comandos básicos.
- Campo preparado para conectar um backend de IA.

IMPORTANTE:
1. O reconhecimento de voz varia conforme navegador, aparelho e conexão. Use Chrome atualizado.
2. A voz masculina depende das vozes instaladas no Android. O app permite escolher uma voz pt-BR disponível; tom mais grave não garante uma voz masculina.
3. Para uma IA completa, configure um servidor HTTPS seu no campo "Endpoint de IA".
4. NUNCA coloque uma chave privada da OpenAI ou de outro provedor dentro do index.html. O código do navegador é público.
5. Para instalar como PWA, publique em HTTPS e abra no Chrome do Android.

PUBLICAR GRATUITAMENTE NO GITHUB PAGES:
1. Crie ou entre em https://github.com
2. Clique em New repository.
3. Nome: jarvis-web
4. Marque Public e clique em Create repository.
5. Envie todos os arquivos do projeto: index.html, manifest.webmanifest, sw.js, icon-192.png e icon-512.png (README opcional) pelo botão Add file > Upload files.
6. Clique em Commit changes.
7. Abra Settings > Pages.
8. Em Build and deployment, escolha Deploy from a branch.
9. Branch: main; folder: / (root); clique Save.
10. Aguarde a publicação. O endereço será https://SEU-USUARIO.github.io/jarvis-web/

ABRIR NO POCO X5 PRO:
1. Abra o endereço HTTPS no Google Chrome.
2. Permita o acesso ao microfone quando solicitado.
3. Toque no menu ⋮ do Chrome.
4. Escolha "Adicionar à tela inicial" ou "Instalar app", se aparecer.
5. Abra o JARVIS pelo ícone criado.
6. Toque em "Falar com JARVIS" e teste "Olá, JARVIS", "Que horas são?" ou "Qual é a data de hoje?".

TESTE LOCAL:
Abra index.html no Chrome do computador. Algumas funções de microfone podem exigir HTTPS ou localhost; para testar no celular, prefira publicar em HTTPS.

FORMATO DO BACKEND:
O endpoint configurado recebe POST JSON:
{ "message": "texto do usuário" }

E deve responder JSON:
{ "reply": "resposta do assistente" }

O backend deve chamar o provedor de IA mantendo a chave de API no servidor, nunca no navegador.
