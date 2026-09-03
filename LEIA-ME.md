# Prova da Ordem — OCPCA · projecto Android

App Android que abre, sem internet, a aplicação de estudo para o 8.º Exame Nacional de
Admissão à OCPCA (295 perguntas, resumos, formulário, plano de estudo e modo prova).

É um WebView que carrega `app/src/main/assets/index.html`. O progresso fica guardado no
telemóvel (localStorage do WebView).

## Como obter o APK sem instalar nada

1. Cria uma conta em github.com (gratuita) e um repositório novo, vazio.
2. Carrega para lá o conteúdo desta pasta (botão **Add file › Upload files**,
   arrasta tudo, incluindo a pasta `.github`).
3. Abre o separador **Actions**. A compilação arranca sozinha; demora 3 a 5 minutos.
4. Quando terminar, entra na execução e descarrega o ficheiro
   **Prova-da-Ordem-OCPCA-apk** em baixo, em *Artifacts*. Lá dentro está o `.apk`.

## Como instalar no telemóvel

Passa o `.apk` para o telemóvel e abre-o. O Android vai pedir para autorizar a
instalação de aplicações de origem desconhecida — é normal, por a app não vir da
Play Store. É um APK de depuração, assinado com a chave de depuração: instala e
funciona, mas não serve para publicar na Play Store.

## Actualizar o conteúdo

Substitui `app/src/main/assets/index.html` pela versão nova e sobe o ficheiro outra
vez; o Actions gera um APK novo. Sobe também `versionCode` e `versionName` em
`app/build.gradle` se quiseres instalar por cima da anterior.
