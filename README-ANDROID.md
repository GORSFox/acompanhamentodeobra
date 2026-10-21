# RPR+ — preparação Android

Esta branch é uma preparação isolada para avaliar a conversão do RPR+ em aplicativo Android com Capacitor. A branch `main` e o arquivo original não foram alterados.

## Estrutura
- `www/index.html`: cópia do HTML existente, para servir de ponto de partida do app.
- `capacitor.config.json`: configuração inicial do Capacitor.
- `package.json`: dependências e comandos de preparação.
- `www/manifest.webmanifest` e `www/sw.js`: arquivos web referenciados pelo HTML.

## Próximos passos (ambiente com Node.js, npm e Android Studio)
1. Instalar Node.js LTS e Android Studio.
2. Nesta pasta, executar `npm install`.
3. Executar `npx cap add android` (apenas uma vez).
4. Executar `npm run android:sync`.
5. Abrir com `npm run android:open`, testar em emulador/aparelho e corrigir eventuais problemas.
6. Só depois de testes funcionais e de persistência, gerar o Android App Bundle (.aab).

## Atenção antes de publicar
- O identificador `br.com.rprplus.orcamentos` é provisório e deve ser confirmado antes da primeira publicação; não é recomendável alterá-lo depois.
- O HTML usa `localStorage`. Os dados ficam locais ao ambiente do app e podem não ser preservados se o app for desinstalado, se os dados forem apagados ou se o armazenamento mudar. Faça backup/exportação antes de testar.
- A existência destes arquivos não significa que o app foi compilado, testado ou aprovado pela Google Play.
- Verificar o comportamento de impressão/compartilhamento, importação/exportação JSON e todos os fluxos em Android real.
- Não guardar dados reais importantes em versões de teste sem backup.
