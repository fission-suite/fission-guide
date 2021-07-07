---
description: A abordagem da para prover e trabalhar com blocos nativos da web 
---

# Fundamentos do Processamento, Armazenamento, e Identidade 

Os alicerces de aplicações poderosas de forma geral incluem três blocos primários: processamento, armazenamento, e identidade. A abordagem escolhida pela Fission é fazer uso desses blocos, deixando-os fáceis para programadores os utilizarem, além de criar fortes atributos para essas áreas por padrão. 

O [Fission White Paper](https://whitepaper.fission.codes/) pode ser lido para uma análise mais técnica, com todas nossas especificações e metas, incluindo links para várias seções importantes:

* [WinFS File System](https://whitepaper.fission.codes/file-system)
* [DID-based identity, UCAN + JWTs](https://whitepaper.fission.codes/identity)

Leituras adicionais e apresentações também estão disponíveis:

* User Controlled Authorization Network \(UCAN\), [Auth without a Backend blog post](https://blog.fission.codes/auth-without-backend/)
* Apresentação feita no Berlin Functional Programming Meetup June 2020, [A Universal Hostless Substrate: Full Stack Web Apps Without a Backend, and More!](https://talk.fission.codes/t/berlin-functional-programming-group-a-universal-hostless-substrate-full-stack-web-apps-without-a-backend-and-more/617)

## Processamento

Web browsers rodam no seu desktop local, laptop, ou dispositivos móveis, e todos eles usam processamento local do "computer processing unit" \(CPU\) para fazer o trabalho -- para computar as coisas. Sua máquina realiza o trabalho para executar aplicações no seu browser. Páginas web simples usam os recursos de HTML e CSS próprios dos browsers. Mas muitas páginas na web possuem mais recursos interativos, com uma rica interface gráfica \(UI\). Estes são geralmente construído e executdaos em JavaScript, uma linguagem de programação que roda no seu browser, e usa seu processamento local.

Web Assembly é o quarto recurso de computação padronizado para navegadores. Ele pode processar aplicações que são escritas originalmente em outras linguagens, não só JavaScript. Nós estamos começando a ver aplicações poderosas sendo feitas em Web Assembly, como o Figma, que provê uma experiência no estilo "PhotoShop" para seu web browser. 

Fission pretende suportar Web Assembly, deixando assim mais fácil de construir, hospedar, e escalar aplicações nativas da web que incluem  Web Assembly.

## Armazenamento

Quando as pessoas pensam sobre serem donas de seus prórpios dados, isso geralmente revela que eles se sentem confortáveis quando podem ver e procurar os arquivos que um aplicativo usa ou cria, ao invés de precisarem exportar, ou não ter acesso nenhum aos seus dados.

Na Fission, nós desenvolvemos um sistema de arquivos que está disponível tanto para desenvolvedores que querem construir e hospedar aplicativos, quanto para as pessoas que usam esses aplicativos.

Nós desenvolvemos o que chamamos de **Web Native File System**, se pronuncia e se escreve como **WinFS**. É construído sobre vários protocolos abertos, incluindo o InterPlanetary File System \(IPFS\), o qual você pode [aprender mais sobre no apêndice](../../appendix/ipfs.md).

Nós pretendendos desenvolver e compartilhar as especificações do WinFS, e contribuir para isso se tornar uma padronização aberta, com implementações abertas para qualquer um utilizar.

WinFS foi feito para prover uma experiência aberta como do iCloud: disponível e sincronizado em todos os dispositivos, além de prover arquivos criptografados públicos e privados. 

## Identidade

Implementar um sistema de login, autenticação, e autorização de forma segura é um desafio, especialmente respeitando a privacidade do usuário, provendo criptografria end to end, e de outra froma balanceando a facilidade de uso tanto para desenvolvedores quando para consumidores. 

Para desenvolvedores, nós queremos prover uma solução interna para incluir logins e autenticação evitando problemas para sua implementação.

Para todos, nós queremos que seja fácil fazer login de forma segura, sem precisar que lembrar de senhas, e fazer esse login disponível em todos os outros dispositivos.

Nós construímos sobre os Identificadores Descentralizados \(DIDs\). [Rascunho do W3C standards](https://www.w3.org/TR/did-core/).

Nós então desenvolvemos o "User Controlled Authorization Network" \(UCAN\): uma forma de fazer a autorização onde os usuários possuem totalmente o controle. 

Com UCAN, nós nos baseaamos nos padrões do JSON Web Tokens \(JWTs\), e também no paper da Google sobre Macaroons para sistemas distribuídos.

Nós combinamos tudo isso no SDK webnative para desenvolvedores e usuários da plataforma da Fission. Em browsers, usamos o [Web Cryptography API, uma padronização da W3C](https://www.w3.org/TR/WebCryptoAPI/). A [Documentação da MDN incluí mais leituras »](https://developer.mozilla.org/en-US/docs/Web/API/Web_Crypto_API)

Nós pretendemos trabalhar com padrões de autorização e identiades existentes e novos que contribuirão para nosso trabalho como padronizações abertas. 

