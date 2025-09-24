# handsondigital/lib.php.idplugger



# Introdução

Bem-vindo à documentação oficial da API da Plataforma de Promoção IdPlugger! Esta API foi desenvolvida para oferecer acesso seguro e eficiente aos recursos e serviços essenciais da Plataforma.

# Sobre a API

Esta API é baseada em REST, proporcionando uma arquitetura flexível e de fácil integração para desenvolvedores e empresas.

Esta documentação foi elaborada com o intuito de fornecer uma referência abrangente e detalhada para desenvolvedores, parceiros e clientes que desejam utilizar a API da Plataforma de Promoção IdPlugger em seus próprios aplicativos, sistemas e plataformas. Aqui, você encontrará informações sobre os endpoints disponíveis, parâmetros de solicitação, respostas esperadas, autenticação, webhooks, exemplos de uso e muito mais.

# Começando

Para começar a explorar e utilizar a API da Plataforma de Promoção IdPlugger, recomendamos que você siga os seguintes passos:

1. **Autenticação**: Obtenha suas credenciais de autenticação ('username' e 'password'), junto ao nosso time comercial, para acessar a API.

2. **Explorar Endpoints**: Navegue pela lista de endpoints disponíveis e suas respectivas funcionalidades.

3. **Experimentar**: Utilize os exemplos de solicitação fornecidos para testar os endpoints e compreender melhor seu funcionamento.

4. **Integrar**: Integre a API da Plataforma de Promoção IdPlugger em seus próprios projetos e sistemas para aproveitar ao máximo suas capacidades.

# Autenticação

Todos os endpoints requerem token de autenticação válido, que pode ser obtido através de requisição à API enviando as credenciais obtidas junto a equipe da Plataforma de Promoção.

Este token é do tipo JWT e deve ser enviado no header da requisição no seguinte formato:

| Header | Valor |
  | - | - |
  | Authorization | bearer `{token}` |

Substitua `{token}` pelo token obtido na autenticação.

IMPORTANTE: O token JWT tem um tempo de validade, o ideal é armazenar o token JWT e solicitar um novo token apenas quando o seu token expirar. A validade do token é enviada junto com o token na resposta do endpoint de autenticação.

# Webhooks

Ao cadastrar um usuário ou um cupom, a API irá armazenar os dados informados para processar em segundo plano. Por tanto, para obter a informação de cadastro com sucesso ou falha no cadastro de um usuário ou um cupom, é necessário ter um webhook cadastrado na API.

Para cadastrar o webhook da promoção na API, utilize o endpoint <a href=\"#/Settings/config.webhook\">`/webhook`</a>.

# Ambiente de testes

Atualmente a Plataforma de Promoção IdPlugger não possui ambiente de homologação para testes de integração do cliente. Todos as validações devem ser realizadas em produção, **sem ônus à pessoa desenvolvedora**. Todos os dados de testes serão excluídos da Plataforma antes do início oficial da Promoção.

Estamos empolgados por você ter escolhido a API de Promoção da IdPlugger para impulsionar suas iniciativas promocionais. Se surgirem dúvidas ou precisar de suporte, não hesite em contatar nossa equipe de suporte técnico.

Vamos começar a promover o sucesso juntos!

# Postman Collection

[<img src=\"https://run.pstmn.io/button.svg\" alt=\"Run In \" style=\"width: 128px; height: 32px;\">](https://god.gw.postman.com/run-collection/13619232-20687020-3c58-488d-bd15-9f9d1a8164b1?action=collection%2Ffork&source=rip_markdown&collection-url=entityId%3D13619232-20687020-3c58-488d-bd15-9f9d1a8164b1%26entityType%3Dcollection%26workspaceId%3Df86d7ea0-5224-4351-bf69-54ada2ca328d)


## Installation & Usage

### Requirements

PHP 8.1 and later.

### Composer

To install the bindings via [Composer](https://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/GIT_USER_ID/GIT_REPO_ID.git"
    }
  ],
  "require": {
    "GIT_USER_ID/GIT_REPO_ID": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/handsondigital/lib.php.idplugger/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\ArticlesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$article = array(new \IdpluggerPromotion\Model\Article()); // \IdpluggerPromotion\Model\Article[]

try {
    $result = $apiInstance->articlesCreate($promotion_id, $article);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ArticlesApi->articlesCreate: ', $e->getMessage(), PHP_EOL;
}

```

## API Endpoints

All URIs are relative to *http://localhost*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*ArticlesApi* | [**articlesCreate**](docs/Api/ArticlesApi.md#articlescreate) | **POST** /v3/promotion/{promotion_id}/cms/articles | Cadastra publicações na promoção
*ArticlesApi* | [**articlesDelete**](docs/Api/ArticlesApi.md#articlesdelete) | **DELETE** /v3/promotion/{promotion_id}/cms/articles/{id} | Exclui uma publicação da promoção
*ArticlesApi* | [**articlesIndex**](docs/Api/ArticlesApi.md#articlesindex) | **GET** /v3/promotion/{promotion_id}/cms/articles | Lista as publicações cadastradas na promoção
*ArticlesApi* | [**articlesUpdate**](docs/Api/ArticlesApi.md#articlesupdate) | **PATCH** /v3/promotion/{promotion_id}/cms/articles | Cadastra ou atualiza publicações na promoção
*AuthApi* | [**authLoginByToken**](docs/Api/AuthApi.md#authloginbytoken) | **POST** /v3/auth/login | Login na API via e-mail e token
*AuthApi* | [**authRefreshToken**](docs/Api/AuthApi.md#authrefreshtoken) | **POST** /v3/auth/refresh | Renova o do token de autenticação
*AuthApi* | [**authRequestToken**](docs/Api/AuthApi.md#authrequesttoken) | **POST** /v3/auth/request-token | Solicita envio de token de login por email
*AuthApi* | [**login**](docs/Api/AuthApi.md#login) | **POST** /v3/login | Login na API
*AuthApi* | [**me**](docs/Api/AuthApi.md#me) | **GET** /v3/me | Dados na API
*AwardedsApi* | [**awardedsSearch**](docs/Api/AwardedsApi.md#awardedssearch) | **GET** /v3/promotion/{promotion_id}/awardeds | Busca por usuários cadastrados na promoção ganhadores de sorteios
*AwardedsApi* | [**awardedsStates**](docs/Api/AwardedsApi.md#awardedsstates) | **GET** /v3/promotion/{promotion_id}/awardeds/states | Lista os status de ganhador existentes na promoção
*AwardedsApi* | [**awardedsUpdate**](docs/Api/AwardedsApi.md#awardedsupdate) | **PATCH** /v3/promotion/{promotion_id}/awardeds | Atualiza informações referentes aos ganhadores de sorteios da promoção
*AwardsApi* | [**awardsCreate**](docs/Api/AwardsApi.md#awardscreate) | **POST** /v3/promotion/{promotion_id}/awards | Cadastra um prêmio na promoção
*AwardsApi* | [**awardsDelete**](docs/Api/AwardsApi.md#awardsdelete) | **DELETE** /v3/promotion/{promotion_id}/awards/{id} | Deleta um prêmio da promoção
*AwardsApi* | [**awardsIndex**](docs/Api/AwardsApi.md#awardsindex) | **GET** /v3/promotion/{promotion_id}/awards | Pesquisa por prêmios na promoção
*AwardsApi* | [**awardsUpdate**](docs/Api/AwardsApi.md#awardsupdate) | **PATCH** /v3/promotion/{promotion_id}/awards | Cadastra ou atualiza um prêmio na promoção
*BlockedUsersApi* | [**blacklistCreate**](docs/Api/BlockedUsersApi.md#blacklistcreate) | **POST** /v3/promotion/{promotion_id}/users/blacklist | Cadastra um CPF na lista de CPFs bloqueados na promoção
*BlockedUsersApi* | [**blacklistDelete**](docs/Api/BlockedUsersApi.md#blacklistdelete) | **DELETE** /v3/promotion/{promotion_id}/users/blacklist/{id} | Exclui um CPF da lista de CPFs bloqueados da promoção
*BlockedUsersApi* | [**blacklistIndex**](docs/Api/BlockedUsersApi.md#blacklistindex) | **GET** /v3/promotion/{promotion_id}/users/blacklist | Pesquisa por CPFs bloqueados na promoção
*BrandingApi* | [**brandingIndex**](docs/Api/BrandingApi.md#brandingindex) | **GET** /v3/promotion/{promotion_id}/cms/branding | Dados referentes a identidade visual da marca da promoção
*BrandingApi* | [**brandingUpdate**](docs/Api/BrandingApi.md#brandingupdate) | **POST** /v3/promotion/{promotion_id}/cms/branding | Altera os dados referentes a identidade visual da marca da promoção
*ContentApi* | [**contentCreate**](docs/Api/ContentApi.md#contentcreate) | **POST** /v3/promotion/{promotion_id}/cms/content | Cria um novo conteúdo para a promoção
*ContentApi* | [**contentIndex**](docs/Api/ContentApi.md#contentindex) | **GET** /v3/promotion/{promotion_id}/cms/content | Dados referentes aos conteúdos (que não são artigos de blog) da promoção
*CouponsApi* | [**couponsCreate**](docs/Api/CouponsApi.md#couponscreate) | **POST** /v3/promotion/{promotion_id}/users/{user_id}/coupons | Cadastra um cupom para um usuário cadastrado na promoção
*CouponsApi* | [**couponsDelete**](docs/Api/CouponsApi.md#couponsdelete) | **DELETE** /v3/promotion/{promotion_id}/users/{user_id}/coupons/{coupon_id} | Exclui um cupom de um usuário cadastrado na promoção
*CouponsApi* | [**couponsIndex**](docs/Api/CouponsApi.md#couponsindex) | **GET** /v3/promotion/{promotion_id}/users/{user_id}/coupons | Busca por cupons de um usuário cadastrado na promoção
*CouponsApi* | [**couponsUpdate**](docs/Api/CouponsApi.md#couponsupdate) | **PATCH** /v3/promotion/{promotion_id}/users/{user_id}/coupons | Cadastra ou atualiza um cupom para um usuário cadastrado na promoção
*CouponsApi* | [**cuponsWebhook**](docs/Api/CouponsApi.md#cuponswebhook) | **POST** /webhook-do-cupom | Webhook de resposta ao registro de cupons
*DefaultApi* | [**v3PromotionPromotionIdCouponsGet**](docs/Api/DefaultApi.md#v3promotionpromotionidcouponsget) | **GET** /v3/promotion/{promotion_id}/coupons | Buscar cupons de uma promoção
*DocumentRulesApi* | [**documentRulesIndex**](docs/Api/DocumentRulesApi.md#documentrulesindex) | **GET** /v3/promotion/{promotion_id}/cms/document_rules | Termos de uso, regulamentos e política de privacidade da promoção
*DocumentRulesApi* | [**documentRulesRegulationDelete**](docs/Api/DocumentRulesApi.md#documentrulesregulationdelete) | **DELETE** /v3/promotion/{promotion_id}/cms/document_rules/regulation/{regulation_id} | Exclui um regulamento da promoção
*DocumentRulesApi* | [**documentRulesUpdate**](docs/Api/DocumentRulesApi.md#documentrulesupdate) | **POST** /v3/promotion/{promotion_id}/cms/document_rules | Atualiza os termos de uso e regulamento da promoção
*FAQApi* | [**faqCreate**](docs/Api/FAQApi.md#faqcreate) | **POST** /v3/promotion/{promotion_id}/cms/faq | Cadastra perguntas frequentes na promoção
*FAQApi* | [**faqDelete**](docs/Api/FAQApi.md#faqdelete) | **DELETE** /v3/promotion/{promotion_id}/cms/faq | Esclui perguntas frequentes na promoção
*FAQApi* | [**faqIndex**](docs/Api/FAQApi.md#faqindex) | **GET** /v3/promotion/{promotion_id}/cms/faq | Lista as perguntas frequentes cadastradas na promoção
*FAQApi* | [**faqUpdate**](docs/Api/FAQApi.md#faqupdate) | **PATCH** /v3/promotion/{promotion_id}/cms/faq | Cadastra ou atualiza perguntas frequentes na promoção
*FilesApi* | [**filesShow**](docs/Api/FilesApi.md#filesshow) | **GET** /v3/promotion/{promotion_id}/files/{filename} | Faz o download de um arquivo
*LuckyNumbersApi* | [**luckyNumbersAddCustom**](docs/Api/LuckyNumbersApi.md#luckynumbersaddcustom) | **POST** /v3/promotion/{promotion_id}/lucky_numbers | Cadastra Números da Sorte no repositório da promoção
*LuckyNumbersApi* | [**luckyNumbersRemove**](docs/Api/LuckyNumbersApi.md#luckynumbersremove) | **POST** /v3/promotion/{promotion_id}/users/{user_id}/lucky_numbers/remove | Inativa e remove Números da Sorte cadastrados na promoção
*LuckyNumbersApi* | [**luckyNumbersSearch**](docs/Api/LuckyNumbersApi.md#luckynumberssearch) | **GET** /v3/promotion/{promotion_id}/users/{user_id}/lucky_numbers | Busca por Números da Sorte de um usuário cadastrado na promoção
*MetricsApi* | [**metrics**](docs/Api/MetricsApi.md#metrics) | **GET** /v3/promotion/{promotion_id}/metrics | Devolve as métricas da promoção
*OrdersApi* | [**ordersCreate**](docs/Api/OrdersApi.md#orderscreate) | **POST** /v3/promotion/{promotion_id}/users/{user_id}/orders | Cadastra um pedido para um usuário na promoção
*OrdersApi* | [**ordersIndex**](docs/Api/OrdersApi.md#ordersindex) | **GET** /v3/promotion/{promotion_id}/users/{user_id}/orders | Pesquisa por pedidos na promoção
*OrdersApi* | [**ordersUpdate**](docs/Api/OrdersApi.md#ordersupdate) | **PATCH** /v3/promotion/{promotion_id}/users/{user_id}/orders | Cadastra ou atualiza um pedido de um usuário na promoção
*ProductsApi* | [**productsCreate**](docs/Api/ProductsApi.md#productscreate) | **POST** /v3/promotion/{promotion_id}/products | Cadastra um produto na promoção
*ProductsApi* | [**productsDelete**](docs/Api/ProductsApi.md#productsdelete) | **DELETE** /v3/promotion/{promotion_id}/products/{product_id} | Exclui um produto cadastrado na promoção
*ProductsApi* | [**productsIndex**](docs/Api/ProductsApi.md#productsindex) | **GET** /v3/promotion/{promotion_id}/products | Busca por produtos cadastrados na promoção
*ProductsApi* | [**productsUpdate**](docs/Api/ProductsApi.md#productsupdate) | **PATCH** /v3/promotion/{promotion_id}/products | Cadastra ou atualiza produtos na promoção
*PromotionDataApi* | [**configsIndex**](docs/Api/PromotionDataApi.md#configsindex) | **GET** /v3/promotion/{promotion_id} | Retorna dados da promoção
*RafflesApi* | [**rafflesCreate**](docs/Api/RafflesApi.md#rafflescreate) | **POST** /v3/promotion/{promotion_id}/raffles | Cadastra um sorteio na promoção
*RafflesApi* | [**rafflesDelete**](docs/Api/RafflesApi.md#rafflesdelete) | **DELETE** /v3/promotion/{promotion_id}/raffles/{id} | Exclui um sorteio da promoção
*RafflesApi* | [**rafflesIndex**](docs/Api/RafflesApi.md#rafflesindex) | **GET** /v3/promotion/{promotion_id}/raffles | Pesquisa por sorteios na promoção
*RafflesApi* | [**rafflesReport**](docs/Api/RafflesApi.md#rafflesreport) | **POST** /v3/promotion/{promotion_id}/raffles/{id}/report | Envia por e-mail o relatório de cupons participantes de um sorteio
*RafflesApi* | [**rafflesUpdate**](docs/Api/RafflesApi.md#rafflesupdate) | **PATCH** /v3/promotion/{promotion_id}/raffles | Cadastra ou atualiza um sorteio na promoção
*SettingsApi* | [**configWebhook**](docs/Api/SettingsApi.md#configwebhook) | **POST** /v3/promotion/{promotion_id}/webhook | Configura o webhook da promoção
*StoresApi* | [**storesCreate**](docs/Api/StoresApi.md#storescreate) | **POST** /v3/promotion/{promotion_id}/stores | Cadastra uma loja na promoção
*StoresApi* | [**storesDelete**](docs/Api/StoresApi.md#storesdelete) | **DELETE** /v3/promotion/{promotion_id}/stores/{store_id} | Exclui um produto cadastrado na promoção
*StoresApi* | [**storesIndex**](docs/Api/StoresApi.md#storesindex) | **GET** /v3/promotion/{promotion_id}/stores | Busca por lojas cadastradas na promoção
*StoresApi* | [**storesUpdate**](docs/Api/StoresApi.md#storesupdate) | **PATCH** /v3/promotion/{promotion_id}/stores | Cadastra ou atualiza lojas na promoção
*TicketsApi* | [**ticketsCreate**](docs/Api/TicketsApi.md#ticketscreate) | **POST** /v3/promotion/{promotion_id}/tickets | Cadastra um ticket de suporte na promoção
*TicketsApi* | [**ticketsDelete**](docs/Api/TicketsApi.md#ticketsdelete) | **DELETE** /v3/promotion/{promotion_id}/tickets/{id} | Exclui um ticket de suporte da promoção
*TicketsApi* | [**ticketsIndex**](docs/Api/TicketsApi.md#ticketsindex) | **GET** /v3/promotion/{promotion_id}/tickets | Busca por tickets de suporte cadastrados na promoção
*TicketsApi* | [**ticketsUpdate**](docs/Api/TicketsApi.md#ticketsupdate) | **PATCH** /v3/promotion/{promotion_id}/tickets | Cadastra ou atualiza um ticket de suporte na promoção
*UsersApi* | [**usersCreate**](docs/Api/UsersApi.md#userscreate) | **POST** /v3/promotion/{promotion_id}/users | Cadastra um usuário na promoção
*UsersApi* | [**usersDelete**](docs/Api/UsersApi.md#usersdelete) | **DELETE** /v3/promotion/{promotion_id}/users/{user_id} | Exclui um usuário da promoção
*UsersApi* | [**usersIndex**](docs/Api/UsersApi.md#usersindex) | **GET** /v3/promotion/{promotion_id}/users | Busca por um usuário cadastrado na promoção
*UsersApi* | [**usersUpdate**](docs/Api/UsersApi.md#usersupdate) | **PATCH** /v3/promotion/{promotion_id}/users | Cadastra ou atualiza um usuário na promoção
*UsersApi* | [**usersWebhook**](docs/Api/UsersApi.md#userswebhook) | **POST** /webhook-do-usuario | Webhook de resposta ao registro de usuário

## Models

- [AddLuckyNumberCustom](docs/Model/AddLuckyNumberCustom.md)
- [Article](docs/Model/Article.md)
- [ArticleCustomDataInner](docs/Model/ArticleCustomDataInner.md)
- [ArticlesCreate200Response](docs/Model/ArticlesCreate200Response.md)
- [ArticlesCreate400Response](docs/Model/ArticlesCreate400Response.md)
- [ArticlesCreate401Response](docs/Model/ArticlesCreate401Response.md)
- [ArticlesDelete200Response](docs/Model/ArticlesDelete200Response.md)
- [ArticlesDelete400Response](docs/Model/ArticlesDelete400Response.md)
- [ArticlesDelete401Response](docs/Model/ArticlesDelete401Response.md)
- [ArticlesIndex200Response](docs/Model/ArticlesIndex200Response.md)
- [ArticlesIndex400Response](docs/Model/ArticlesIndex400Response.md)
- [ArticlesIndex401Response](docs/Model/ArticlesIndex401Response.md)
- [ArticlesUpdate200Response](docs/Model/ArticlesUpdate200Response.md)
- [ArticlesUpdate400Response](docs/Model/ArticlesUpdate400Response.md)
- [ArticlesUpdate401Response](docs/Model/ArticlesUpdate401Response.md)
- [AuthLoginByToken200Response](docs/Model/AuthLoginByToken200Response.md)
- [AuthLoginByTokenRequest](docs/Model/AuthLoginByTokenRequest.md)
- [AuthRefreshTokenRequest](docs/Model/AuthRefreshTokenRequest.md)
- [AuthRequestToken200Response](docs/Model/AuthRequestToken200Response.md)
- [AuthRequestTokenRequest](docs/Model/AuthRequestTokenRequest.md)
- [Award](docs/Model/Award.md)
- [Awarded](docs/Model/Awarded.md)
- [AwardedsSearch200Response](docs/Model/AwardedsSearch200Response.md)
- [AwardedsSearch400Response](docs/Model/AwardedsSearch400Response.md)
- [AwardedsSearch401Response](docs/Model/AwardedsSearch401Response.md)
- [AwardedsStates200Response](docs/Model/AwardedsStates200Response.md)
- [AwardedsStates200ResponseContentInner](docs/Model/AwardedsStates200ResponseContentInner.md)
- [AwardedsUpdate200Response](docs/Model/AwardedsUpdate200Response.md)
- [AwardedsUpdate400Response](docs/Model/AwardedsUpdate400Response.md)
- [AwardedsUpdate401Response](docs/Model/AwardedsUpdate401Response.md)
- [AwardsCreate200Response](docs/Model/AwardsCreate200Response.md)
- [AwardsCreate400Response](docs/Model/AwardsCreate400Response.md)
- [AwardsCreate401Response](docs/Model/AwardsCreate401Response.md)
- [AwardsDelete200Response](docs/Model/AwardsDelete200Response.md)
- [AwardsDelete400Response](docs/Model/AwardsDelete400Response.md)
- [AwardsDelete401Response](docs/Model/AwardsDelete401Response.md)
- [AwardsIndex200Response](docs/Model/AwardsIndex200Response.md)
- [AwardsIndex400Response](docs/Model/AwardsIndex400Response.md)
- [AwardsIndex401Response](docs/Model/AwardsIndex401Response.md)
- [AwardsUpdate200Response](docs/Model/AwardsUpdate200Response.md)
- [AwardsUpdate400Response](docs/Model/AwardsUpdate400Response.md)
- [AwardsUpdate401Response](docs/Model/AwardsUpdate401Response.md)
- [BlacklistCreate200Response](docs/Model/BlacklistCreate200Response.md)
- [BlacklistCreate200ResponseContentInner](docs/Model/BlacklistCreate200ResponseContentInner.md)
- [BlacklistCreate400Response](docs/Model/BlacklistCreate400Response.md)
- [BlacklistCreate401Response](docs/Model/BlacklistCreate401Response.md)
- [BlacklistCreateRequest](docs/Model/BlacklistCreateRequest.md)
- [BlacklistDelete200Response](docs/Model/BlacklistDelete200Response.md)
- [BlacklistDelete400Response](docs/Model/BlacklistDelete400Response.md)
- [BlacklistDelete401Response](docs/Model/BlacklistDelete401Response.md)
- [BlacklistIndex200Response](docs/Model/BlacklistIndex200Response.md)
- [BlacklistIndex200ResponseContentInner](docs/Model/BlacklistIndex200ResponseContentInner.md)
- [BlacklistIndex400Response](docs/Model/BlacklistIndex400Response.md)
- [Branding](docs/Model/Branding.md)
- [BrandingIndex200Response](docs/Model/BrandingIndex200Response.md)
- [BrandingIndex400Response](docs/Model/BrandingIndex400Response.md)
- [BrandingIndex401Response](docs/Model/BrandingIndex401Response.md)
- [BrandingMenuInner](docs/Model/BrandingMenuInner.md)
- [BrandingSocial](docs/Model/BrandingSocial.md)
- [BrandingUpdate200Response](docs/Model/BrandingUpdate200Response.md)
- [BrandingUpdate400Response](docs/Model/BrandingUpdate400Response.md)
- [BrandingUpdate401Response](docs/Model/BrandingUpdate401Response.md)
- [ConfigWebhook200Response](docs/Model/ConfigWebhook200Response.md)
- [ConfigWebhook400Response](docs/Model/ConfigWebhook400Response.md)
- [ConfigWebhook401Response](docs/Model/ConfigWebhook401Response.md)
- [ConfigWebhookRequest](docs/Model/ConfigWebhookRequest.md)
- [ConfigsIndex200Response](docs/Model/ConfigsIndex200Response.md)
- [ConfigsIndex400Response](docs/Model/ConfigsIndex400Response.md)
- [ConfigsIndex401Response](docs/Model/ConfigsIndex401Response.md)
- [Content](docs/Model/Content.md)
- [ContentCreate200Response](docs/Model/ContentCreate200Response.md)
- [ContentCreate400Response](docs/Model/ContentCreate400Response.md)
- [ContentCreate401Response](docs/Model/ContentCreate401Response.md)
- [ContentIndex200Response](docs/Model/ContentIndex200Response.md)
- [ContentIndex400Response](docs/Model/ContentIndex400Response.md)
- [ContentIndex401Response](docs/Model/ContentIndex401Response.md)
- [Coupon](docs/Model/Coupon.md)
- [CouponProductsInner](docs/Model/CouponProductsInner.md)
- [CouponWebhookError](docs/Model/CouponWebhookError.md)
- [CouponWebhookErrorContent](docs/Model/CouponWebhookErrorContent.md)
- [CouponWebhookErrorContentAllOfErrors](docs/Model/CouponWebhookErrorContentAllOfErrors.md)
- [CouponWebhookSuccess](docs/Model/CouponWebhookSuccess.md)
- [CouponsCreate200Response](docs/Model/CouponsCreate200Response.md)
- [CouponsCreate401Response](docs/Model/CouponsCreate401Response.md)
- [CouponsCreate409Response](docs/Model/CouponsCreate409Response.md)
- [CouponsCreateRequest](docs/Model/CouponsCreateRequest.md)
- [CouponsDelete200Response](docs/Model/CouponsDelete200Response.md)
- [CouponsDelete400Response](docs/Model/CouponsDelete400Response.md)
- [CouponsDelete401Response](docs/Model/CouponsDelete401Response.md)
- [CouponsUpdate201Response](docs/Model/CouponsUpdate201Response.md)
- [CouponsUpdate401Response](docs/Model/CouponsUpdate401Response.md)
- [CouponsUpdate409Response](docs/Model/CouponsUpdate409Response.md)
- [CuponsWebhookRequest](docs/Model/CuponsWebhookRequest.md)
- [DocumentRulesIndex200Response](docs/Model/DocumentRulesIndex200Response.md)
- [DocumentRulesIndex200ResponseContent](docs/Model/DocumentRulesIndex200ResponseContent.md)
- [DocumentRulesIndex200ResponseContentRegulationsInner](docs/Model/DocumentRulesIndex200ResponseContentRegulationsInner.md)
- [DocumentRulesIndex400Response](docs/Model/DocumentRulesIndex400Response.md)
- [DocumentRulesIndex401Response](docs/Model/DocumentRulesIndex401Response.md)
- [DocumentRulesRegulationDelete200Response](docs/Model/DocumentRulesRegulationDelete200Response.md)
- [DocumentRulesRegulationDelete400Response](docs/Model/DocumentRulesRegulationDelete400Response.md)
- [DocumentRulesRegulationDelete401Response](docs/Model/DocumentRulesRegulationDelete401Response.md)
- [DocumentRulesUpdate200Response](docs/Model/DocumentRulesUpdate200Response.md)
- [DocumentRulesUpdate400Response](docs/Model/DocumentRulesUpdate400Response.md)
- [DocumentRulesUpdate401Response](docs/Model/DocumentRulesUpdate401Response.md)
- [DocumentRulesUpdateRequest](docs/Model/DocumentRulesUpdateRequest.md)
- [DocumentRulesUpdateRequestRegulationsInner](docs/Model/DocumentRulesUpdateRequestRegulationsInner.md)
- [FaqCreate200Response](docs/Model/FaqCreate200Response.md)
- [FaqCreate400Response](docs/Model/FaqCreate400Response.md)
- [FaqCreate401Response](docs/Model/FaqCreate401Response.md)
- [FaqCreateRequestInner](docs/Model/FaqCreateRequestInner.md)
- [FaqDelete200Response](docs/Model/FaqDelete200Response.md)
- [FaqDelete400Response](docs/Model/FaqDelete400Response.md)
- [FaqDelete401Response](docs/Model/FaqDelete401Response.md)
- [FaqIndex200Response](docs/Model/FaqIndex200Response.md)
- [FaqIndex200ResponseContentInner](docs/Model/FaqIndex200ResponseContentInner.md)
- [FaqIndex400Response](docs/Model/FaqIndex400Response.md)
- [FaqIndex401Response](docs/Model/FaqIndex401Response.md)
- [FaqUpdate200Response](docs/Model/FaqUpdate200Response.md)
- [FaqUpdate400Response](docs/Model/FaqUpdate400Response.md)
- [FaqUpdate401Response](docs/Model/FaqUpdate401Response.md)
- [FilesShow200Response](docs/Model/FilesShow200Response.md)
- [FilesShow400Response](docs/Model/FilesShow400Response.md)
- [FilesShow401Response](docs/Model/FilesShow401Response.md)
- [Login200Response](docs/Model/Login200Response.md)
- [Login401Response](docs/Model/Login401Response.md)
- [LoginRequest](docs/Model/LoginRequest.md)
- [LuckyNumber](docs/Model/LuckyNumber.md)
- [LuckyNumbersAddCustom200Response](docs/Model/LuckyNumbersAddCustom200Response.md)
- [LuckyNumbersAddCustom400Response](docs/Model/LuckyNumbersAddCustom400Response.md)
- [LuckyNumbersAddCustom401Response](docs/Model/LuckyNumbersAddCustom401Response.md)
- [LuckyNumbersRemove200Response](docs/Model/LuckyNumbersRemove200Response.md)
- [LuckyNumbersRemove400Response](docs/Model/LuckyNumbersRemove400Response.md)
- [LuckyNumbersRemove401Response](docs/Model/LuckyNumbersRemove401Response.md)
- [LuckyNumbersRemoveRequest](docs/Model/LuckyNumbersRemoveRequest.md)
- [LuckyNumbersRemoveRequestLuckyNumbersInner](docs/Model/LuckyNumbersRemoveRequestLuckyNumbersInner.md)
- [LuckyNumbersSearch200Response](docs/Model/LuckyNumbersSearch200Response.md)
- [LuckyNumbersSearch400Response](docs/Model/LuckyNumbersSearch400Response.md)
- [LuckyNumbersSearch401Response](docs/Model/LuckyNumbersSearch401Response.md)
- [Me200Response](docs/Model/Me200Response.md)
- [Me200ResponsePromotionsInner](docs/Model/Me200ResponsePromotionsInner.md)
- [Metrics200Response](docs/Model/Metrics200Response.md)
- [Metrics200ResponseContent](docs/Model/Metrics200ResponseContent.md)
- [Metrics200ResponseContentUsersInner](docs/Model/Metrics200ResponseContentUsersInner.md)
- [Metrics400Response](docs/Model/Metrics400Response.md)
- [Order](docs/Model/Order.md)
- [OrderCustomDataInner](docs/Model/OrderCustomDataInner.md)
- [OrdersCreate200Response](docs/Model/OrdersCreate200Response.md)
- [OrdersCreate400Response](docs/Model/OrdersCreate400Response.md)
- [OrdersCreate401Response](docs/Model/OrdersCreate401Response.md)
- [OrdersCreateRequest](docs/Model/OrdersCreateRequest.md)
- [OrdersIndex200Response](docs/Model/OrdersIndex200Response.md)
- [OrdersIndex400Response](docs/Model/OrdersIndex400Response.md)
- [OrdersIndex401Response](docs/Model/OrdersIndex401Response.md)
- [OrdersUpdate200Response](docs/Model/OrdersUpdate200Response.md)
- [OrdersUpdate400Response](docs/Model/OrdersUpdate400Response.md)
- [OrdersUpdate401Response](docs/Model/OrdersUpdate401Response.md)
- [Pagination](docs/Model/Pagination.md)
- [PaginationLinksInner](docs/Model/PaginationLinksInner.md)
- [Product](docs/Model/Product.md)
- [ProductsCreate200Response](docs/Model/ProductsCreate200Response.md)
- [ProductsCreate401Response](docs/Model/ProductsCreate401Response.md)
- [ProductsCreate409Response](docs/Model/ProductsCreate409Response.md)
- [ProductsCreateRequest](docs/Model/ProductsCreateRequest.md)
- [ProductsDelete200Response](docs/Model/ProductsDelete200Response.md)
- [ProductsDelete400Response](docs/Model/ProductsDelete400Response.md)
- [ProductsDelete401Response](docs/Model/ProductsDelete401Response.md)
- [ProductsIndex200Response](docs/Model/ProductsIndex200Response.md)
- [ProductsIndex400Response](docs/Model/ProductsIndex400Response.md)
- [ProductsIndex401Response](docs/Model/ProductsIndex401Response.md)
- [ProductsUpdate201Response](docs/Model/ProductsUpdate201Response.md)
- [ProductsUpdate401Response](docs/Model/ProductsUpdate401Response.md)
- [ProductsUpdate409Response](docs/Model/ProductsUpdate409Response.md)
- [Promotion](docs/Model/Promotion.md)
- [PromotionDatetime](docs/Model/PromotionDatetime.md)
- [PromotionDatetimeActive](docs/Model/PromotionDatetimeActive.md)
- [PromotionDatetimeDelivery](docs/Model/PromotionDatetimeDelivery.md)
- [PromotionDatetimeParticipate](docs/Model/PromotionDatetimeParticipate.md)
- [PromotionDatetimeShowAwardeds](docs/Model/PromotionDatetimeShowAwardeds.md)
- [Raffle](docs/Model/Raffle.md)
- [RafflesCreate200Response](docs/Model/RafflesCreate200Response.md)
- [RafflesCreate400Response](docs/Model/RafflesCreate400Response.md)
- [RafflesCreate401Response](docs/Model/RafflesCreate401Response.md)
- [RafflesCreateRequestInner](docs/Model/RafflesCreateRequestInner.md)
- [RafflesDelete200Response](docs/Model/RafflesDelete200Response.md)
- [RafflesDelete400Response](docs/Model/RafflesDelete400Response.md)
- [RafflesDelete401Response](docs/Model/RafflesDelete401Response.md)
- [RafflesIndex200Response](docs/Model/RafflesIndex200Response.md)
- [RafflesIndex400Response](docs/Model/RafflesIndex400Response.md)
- [RafflesIndex401Response](docs/Model/RafflesIndex401Response.md)
- [RafflesReportRequest](docs/Model/RafflesReportRequest.md)
- [RafflesUpdate200Response](docs/Model/RafflesUpdate200Response.md)
- [RafflesUpdate400Response](docs/Model/RafflesUpdate400Response.md)
- [RafflesUpdate401Response](docs/Model/RafflesUpdate401Response.md)
- [RafflesUpdateRequestInner](docs/Model/RafflesUpdateRequestInner.md)
- [SerieNumber](docs/Model/SerieNumber.md)
- [Store](docs/Model/Store.md)
- [StoresCreate200Response](docs/Model/StoresCreate200Response.md)
- [StoresCreate401Response](docs/Model/StoresCreate401Response.md)
- [StoresCreate409Response](docs/Model/StoresCreate409Response.md)
- [StoresCreateRequest](docs/Model/StoresCreateRequest.md)
- [StoresDelete200Response](docs/Model/StoresDelete200Response.md)
- [StoresDelete400Response](docs/Model/StoresDelete400Response.md)
- [StoresDelete401Response](docs/Model/StoresDelete401Response.md)
- [StoresIndex200Response](docs/Model/StoresIndex200Response.md)
- [StoresIndex400Response](docs/Model/StoresIndex400Response.md)
- [StoresIndex401Response](docs/Model/StoresIndex401Response.md)
- [StoresUpdate201Response](docs/Model/StoresUpdate201Response.md)
- [StoresUpdate401Response](docs/Model/StoresUpdate401Response.md)
- [StoresUpdate409Response](docs/Model/StoresUpdate409Response.md)
- [Ticket](docs/Model/Ticket.md)
- [TicketsCreate200Response](docs/Model/TicketsCreate200Response.md)
- [TicketsCreate400Response](docs/Model/TicketsCreate400Response.md)
- [TicketsCreate401Response](docs/Model/TicketsCreate401Response.md)
- [TicketsDelete200Response](docs/Model/TicketsDelete200Response.md)
- [TicketsDelete400Response](docs/Model/TicketsDelete400Response.md)
- [TicketsDelete401Response](docs/Model/TicketsDelete401Response.md)
- [TicketsIndex200Response](docs/Model/TicketsIndex200Response.md)
- [TicketsIndex400Response](docs/Model/TicketsIndex400Response.md)
- [TicketsIndex401Response](docs/Model/TicketsIndex401Response.md)
- [TicketsUpdate200Response](docs/Model/TicketsUpdate200Response.md)
- [TicketsUpdate400Response](docs/Model/TicketsUpdate400Response.md)
- [User](docs/Model/User.md)
- [UserWebhookError](docs/Model/UserWebhookError.md)
- [UserWebhookErrorContent](docs/Model/UserWebhookErrorContent.md)
- [UserWebhookErrorContentAllOfErrors](docs/Model/UserWebhookErrorContentAllOfErrors.md)
- [UserWebhookSuccess](docs/Model/UserWebhookSuccess.md)
- [UsersCreate201Response](docs/Model/UsersCreate201Response.md)
- [UsersCreate401Response](docs/Model/UsersCreate401Response.md)
- [UsersCreate409Response](docs/Model/UsersCreate409Response.md)
- [UsersCreateRequest](docs/Model/UsersCreateRequest.md)
- [UsersDelete200Response](docs/Model/UsersDelete200Response.md)
- [UsersDelete400Response](docs/Model/UsersDelete400Response.md)
- [UsersDelete401Response](docs/Model/UsersDelete401Response.md)
- [UsersIndex200Response](docs/Model/UsersIndex200Response.md)
- [UsersUpdate201Response](docs/Model/UsersUpdate201Response.md)
- [UsersWebhook200Response](docs/Model/UsersWebhook200Response.md)
- [UsersWebhookRequest](docs/Model/UsersWebhookRequest.md)
- [V3PromotionPromotionIdCouponsGet200Response](docs/Model/V3PromotionPromotionIdCouponsGet200Response.md)
- [V3PromotionPromotionIdCouponsGet200ResponseContentInner](docs/Model/V3PromotionPromotionIdCouponsGet200ResponseContentInner.md)
- [V3PromotionPromotionIdCouponsGet400Response](docs/Model/V3PromotionPromotionIdCouponsGet400Response.md)
- [V3PromotionPromotionIdCouponsGet401Response](docs/Model/V3PromotionPromotionIdCouponsGet401Response.md)

## Authorization

Authentication schemes defined for the API:
### bearerAuth

- **Type**: Bearer authentication (JWT)

## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Author



## About this package

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `3.3.0`
    - Generator version: `7.13.0`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`
