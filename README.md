# IdPluggerPromotion



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

Para cadastrar o webhook da promoção na API, utilize o endpoint <a href=\"#/Configurações/promotion.config.webhook\">`/webhook`</a>.

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
require_once('/path/to/IdPluggerPromotion/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');




$apiInstance = new IdPluggerPromotion\Api\AutenticaoApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$app_http_controllers_admin_admin_controller_login_request = new \IdPluggerPromotion\Model\AppHttpControllersAdminAdminControllerLoginRequest(); // \IdPluggerPromotion\Model\AppHttpControllersAdminAdminControllerLoginRequest

try {
    $result = $apiInstance->appHttpControllersAdminAdminControllerLogin($app_http_controllers_admin_admin_controller_login_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AutenticaoApi->appHttpControllersAdminAdminControllerLogin: ', $e->getMessage(), PHP_EOL;
}

```

## API Endpoints

All URIs are relative to *http://localhost*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AutenticaoApi* | [**appHttpControllersAdminAdminControllerLogin**](docs/Api/AutenticaoApi.md#apphttpcontrollersadminadmincontrollerlogin) | **POST** /v3/login | Login na API
*AutenticaoApi* | [**appHttpControllersAdminAdminControllerMe**](docs/Api/AutenticaoApi.md#apphttpcontrollersadminadmincontrollerme) | **GET** /v3/me | Dados na API
*CPFsBloqueadosApi* | [**promotionBlacklistCreate**](docs/Api/CPFsBloqueadosApi.md#promotionblacklistcreate) | **POST** /v3/promotion/{promotion_id}/users/blacklist | Cadastra um CPF na lista de CPFs bloqueados na promoção
*CPFsBloqueadosApi* | [**promotionBlacklistDelete**](docs/Api/CPFsBloqueadosApi.md#promotionblacklistdelete) | **DELETE** /v3/promotion/{promotion_id}/users/blacklist/{id} | Exclui um CPF da lista de CPFs bloqueados da promoção
*CPFsBloqueadosApi* | [**promotionBlacklistIndex**](docs/Api/CPFsBloqueadosApi.md#promotionblacklistindex) | **GET** /v3/promotion/{promotion_id}/users/blacklist | Pesquisa por CPFs bloqueados na promoção
*ConfiguraesApi* | [**promotionConfigWebhook**](docs/Api/ConfiguraesApi.md#promotionconfigwebhook) | **POST** /v3/promotion/{promotion_id}/webhook | Configura o webhook da promoção
*ContedoApi* | [**promotionContentCreate**](docs/Api/ContedoApi.md#promotioncontentcreate) | **POST** /v3/promotion/{promotion_id}/cms/content | Cria um novo conteúdo para a promoção
*ContedoApi* | [**promotionContentIndex**](docs/Api/ContedoApi.md#promotioncontentindex) | **GET** /v3/promotion/{promotion_id}/cms/content | Dados referentes aos conteúdos (que não são artigos de blog) da promoção
*CuponsApi* | [**promotionCouponsCreate**](docs/Api/CuponsApi.md#promotioncouponscreate) | **POST** /v3/promotion/{promotion_id}/users/{user_id}/coupons | Cadastra um cupom para um usuário cadastrado na promoção
*CuponsApi* | [**promotionCouponsDelete**](docs/Api/CuponsApi.md#promotioncouponsdelete) | **DELETE** /v3/promotion/{promotion_id}/users/{user_id}/coupons/{coupon_id} | Exclui um cupom de um usuário cadastrado na promoção
*CuponsApi* | [**promotionCouponsIndex**](docs/Api/CuponsApi.md#promotioncouponsindex) | **GET** /v3/promotion/{promotion_id}/users/{user_id}/coupons | Busca por cupons de um usuário cadastrado na promoção
*CuponsApi* | [**promotionCouponsUpdate**](docs/Api/CuponsApi.md#promotioncouponsupdate) | **PATCH** /v3/promotion/{promotion_id}/users/{user_id}/coupons | Cadastra ou atualiza um cupom para um usuário cadastrado na promoção
*CuponsApi* | [**promotionCuponsWebhook**](docs/Api/CuponsApi.md#promotioncuponswebhook) | **POST** /webhook-do-cupom | Webhook de resposta ao registro de cupons
*DadosDaPromooApi* | [**promotionConfigsIndex**](docs/Api/DadosDaPromooApi.md#promotionconfigsindex) | **GET** /v3/promotion/{promotion_id} | Retorna dados da promoção
*FAQApi* | [**promotionFaqCreate**](docs/Api/FAQApi.md#promotionfaqcreate) | **POST** /v3/promotion/{promotion_id}/cms/faq | Cadastra perguntas frequentes na promoção
*FAQApi* | [**promotionFaqDelete**](docs/Api/FAQApi.md#promotionfaqdelete) | **DELETE** /v3/promotion/{promotion_id}/cms/faq | Esclui perguntas frequentes na promoção
*FAQApi* | [**promotionFaqIndex**](docs/Api/FAQApi.md#promotionfaqindex) | **GET** /v3/promotion/{promotion_id}/cms/faq | Lista as perguntas frequentes cadastradas na promoção
*FAQApi* | [**promotionFaqUpdate**](docs/Api/FAQApi.md#promotionfaqupdate) | **PATCH** /v3/promotion/{promotion_id}/cms/faq | Cadastra ou atualiza perguntas frequentes na promoção
*GanhadoresApi* | [**promotionAwardedsSearch**](docs/Api/GanhadoresApi.md#promotionawardedssearch) | **GET** /v3/promotion/{promotion_id}/awardeds | Busca por usuários cadastrados na promoção ganhadores de sorteios
*GanhadoresApi* | [**promotionAwardedsStates**](docs/Api/GanhadoresApi.md#promotionawardedsstates) | **GET** /v3/promotion/{promotion_id}/awardeds/states | Lista os status de ganhador existentes na promoção
*GanhadoresApi* | [**promotionAwardedsUpdate**](docs/Api/GanhadoresApi.md#promotionawardedsupdate) | **PATCH** /v3/promotion/{promotion_id}/awardeds | Atualiza informações referentes aos ganhadores de sorteios da promoção
*IdentidadeVisualApi* | [**promotionBrandingIndex**](docs/Api/IdentidadeVisualApi.md#promotionbrandingindex) | **GET** /v3/promotion/{promotion_id}/cms/branding | Dados referentes a identidade visual da marca da promoção
*IdentidadeVisualApi* | [**promotionBrandingUpdate**](docs/Api/IdentidadeVisualApi.md#promotionbrandingupdate) | **POST** /v3/promotion/{promotion_id}/cms/branding | Altera os dados referentes a identidade visual da marca da promoção
*LojasApi* | [**promotionStoresCreate**](docs/Api/LojasApi.md#promotionstorescreate) | **POST** /v3/promotion/{promotion_id}/stores | Cadastra uma loja na promoção
*LojasApi* | [**promotionStoresIndex**](docs/Api/LojasApi.md#promotionstoresindex) | **GET** /v3/promotion/{promotion_id}/stores | Busca por lojas cadastradas na promoção
*LojasApi* | [**promotionStoresUpdate**](docs/Api/LojasApi.md#promotionstoresupdate) | **PATCH** /v3/promotion/{promotion_id}/stores | Cadastra ou atualiza lojas na promoção
*NmerosDaSorteApi* | [**promotionLuckyNumbersAddCustom**](docs/Api/NmerosDaSorteApi.md#promotionluckynumbersaddcustom) | **POST** /v3/promotion/{promotion_id}/lucky_numbers | Cadastra Números da Sorte no repositório da promoção
*NmerosDaSorteApi* | [**promotionLuckyNumbersRemove**](docs/Api/NmerosDaSorteApi.md#promotionluckynumbersremove) | **POST** /v3/promotion/{promotion_id}/users/{user_id}/lucky_numbers/remove | Inativa e remove Números da Sorte cadastrados na promoção
*NmerosDaSorteApi* | [**promotionLuckyNumbersSearch**](docs/Api/NmerosDaSorteApi.md#promotionluckynumberssearch) | **GET** /v3/promotion/{promotion_id}/users/{user_id}/lucky_numbers | Busca por Números da Sorte de um usuário cadastrado na promoção
*PedidosApi* | [**promotionOrdersCreate**](docs/Api/PedidosApi.md#promotionorderscreate) | **POST** /v3/promotion/{promotion_id}/users/{user_id}/orders | Cadastra um pedido para um usuário na promoção
*PedidosApi* | [**promotionOrdersIndex**](docs/Api/PedidosApi.md#promotionordersindex) | **GET** /v3/promotion/{promotion_id}/users/{user_id}/orders | Pesquisa por pedidos na promoção
*PedidosApi* | [**promotionOrdersUpdate**](docs/Api/PedidosApi.md#promotionordersupdate) | **PATCH** /v3/promotion/{promotion_id}/users/{user_id}/orders | Cadastra ou atualiza um pedido de um usuário na promoção
*PrmiosApi* | [**promotionAwardsCreate**](docs/Api/PrmiosApi.md#promotionawardscreate) | **POST** /v3/promotion/{promotion_id}/awards | Cadastra um prêmio na promoção
*PrmiosApi* | [**promotionAwardsDelete**](docs/Api/PrmiosApi.md#promotionawardsdelete) | **DELETE** /v3/promotion/{promotion_id}/awards/{id} | Deleta um prêmio da promoção
*PrmiosApi* | [**promotionAwardsIndex**](docs/Api/PrmiosApi.md#promotionawardsindex) | **GET** /v3/promotion/{promotion_id}/awards | Pesquisa por prêmios na promoção
*PrmiosApi* | [**promotionAwardsUpdate**](docs/Api/PrmiosApi.md#promotionawardsupdate) | **PATCH** /v3/promotion/{promotion_id}/awards | Cadastra ou atualiza um prêmio na promoção
*ProdutosApi* | [**promotionProductsCreate**](docs/Api/ProdutosApi.md#promotionproductscreate) | **POST** /v3/promotion/{promotion_id}/products | Cadastra um produto na promoção
*ProdutosApi* | [**promotionProductsDelete**](docs/Api/ProdutosApi.md#promotionproductsdelete) | **DELETE** /v3/promotion/{promotion_id}/products/{product_id} | Exclui um produto cadastrado na promoção
*ProdutosApi* | [**promotionProductsIndex**](docs/Api/ProdutosApi.md#promotionproductsindex) | **GET** /v3/promotion/{promotion_id}/products | Busca por produtos cadastrados na promoção
*ProdutosApi* | [**promotionProductsUpdate**](docs/Api/ProdutosApi.md#promotionproductsupdate) | **PATCH** /v3/promotion/{promotion_id}/products | Cadastra ou atualiza produtos na promoção
*ProdutosApi* | [**promotionStoresDelete**](docs/Api/ProdutosApi.md#promotionstoresdelete) | **DELETE** /v3/promotion/{promotion_id}/stores/{store_id} | Exclui um produto cadastrado na promoção
*PublicaesApi* | [**promotionArticlesCreate**](docs/Api/PublicaesApi.md#promotionarticlescreate) | **POST** /v3/promotion/{promotion_id}/cms/articles | Cadastra publicações na promoção
*PublicaesApi* | [**promotionArticlesDelete**](docs/Api/PublicaesApi.md#promotionarticlesdelete) | **DELETE** /v3/promotion/{promotion_id}/cms/articles/{id} | Exclui uma publicação da promoção
*PublicaesApi* | [**promotionArticlesIndex**](docs/Api/PublicaesApi.md#promotionarticlesindex) | **GET** /v3/promotion/{promotion_id}/cms/articles | Lista as publicações cadastradas na promoção
*PublicaesApi* | [**promotionArticlesUpdate**](docs/Api/PublicaesApi.md#promotionarticlesupdate) | **PATCH** /v3/promotion/{promotion_id}/cms/articles | Cadastra ou atualiza publicações na promoção
*SorteiosApi* | [**promotionRafflesCreate**](docs/Api/SorteiosApi.md#promotionrafflescreate) | **POST** /v3/promotion/{promotion_id}/raffles | Cadastra um sorteio na promoção
*SorteiosApi* | [**promotionRafflesDelete**](docs/Api/SorteiosApi.md#promotionrafflesdelete) | **DELETE** /v3/promotion/{promotion_id}/raffles/{id} | Exclui um sorteio da promoção
*SorteiosApi* | [**promotionRafflesIndex**](docs/Api/SorteiosApi.md#promotionrafflesindex) | **GET** /v3/promotion/{promotion_id}/raffles | Pesquisa por sorteios na promoção
*SorteiosApi* | [**promotionRafflesReport**](docs/Api/SorteiosApi.md#promotionrafflesreport) | **POST** /v3/promotion/{promotion_id}/raffles/{id}/report | Envia por e-mail o relatório de cupons participantes de um sorteio
*SorteiosApi* | [**promotionRafflesUpdate**](docs/Api/SorteiosApi.md#promotionrafflesupdate) | **PATCH** /v3/promotion/{promotion_id}/raffles | Cadastra ou atualiza um sorteio na promoção
*SuporteDaPromooApi* | [**promotionTicketsCreate**](docs/Api/SuporteDaPromooApi.md#promotionticketscreate) | **POST** /v3/promotion/{promotion_id}/tickets | Cadastra um ticket de suporte na promoção
*SuporteDaPromooApi* | [**promotionTicketsDelete**](docs/Api/SuporteDaPromooApi.md#promotionticketsdelete) | **DELETE** /v3/promotion/{promotion_id}/tickets/{id} | Exclui um ticket de suporte da promoção
*SuporteDaPromooApi* | [**promotionTicketsIndex**](docs/Api/SuporteDaPromooApi.md#promotionticketsindex) | **GET** /v3/promotion/{promotion_id}/tickets | Busca por tickets de suporte cadastrados na promoção
*SuporteDaPromooApi* | [**promotionTicketsUpdate**](docs/Api/SuporteDaPromooApi.md#promotionticketsupdate) | **PATCH** /v3/promotion/{promotion_id}/tickets | Cadastra ou atualiza um ticket de suporte na promoção
*TermosRegulamentosEPolticaDePrivacidadeApi* | [**promotionDocumentRulesIndex**](docs/Api/TermosRegulamentosEPolticaDePrivacidadeApi.md#promotiondocumentrulesindex) | **GET** /v3/promotion/{promotion_id}/cms/document_rules | Termos de uso, regulamentos e política de privacidade da promoção
*TermosRegulamentosEPolticaDePrivacidadeApi* | [**promotionDocumentRulesRegulationDelete**](docs/Api/TermosRegulamentosEPolticaDePrivacidadeApi.md#promotiondocumentrulesregulationdelete) | **DELETE** /v3/promotion/{promotion_id}/cms/document_rules/regulation/{regulation_id} | Exclui um regulamento da promoção
*TermosRegulamentosEPolticaDePrivacidadeApi* | [**promotionDocumentRulesUpdate**](docs/Api/TermosRegulamentosEPolticaDePrivacidadeApi.md#promotiondocumentrulesupdate) | **POST** /v3/promotion/{promotion_id}/cms/document_rules | Atualiza os termos de uso e regulamento da promoção
*UsuriosNaPromooApi* | [**promotionUsersCreate**](docs/Api/UsuriosNaPromooApi.md#promotionuserscreate) | **POST** /v3/promotion/{promotion_id}/users | Cadastra um usuário na promoção
*UsuriosNaPromooApi* | [**promotionUsersDelete**](docs/Api/UsuriosNaPromooApi.md#promotionusersdelete) | **DELETE** /v3/promotion/{promotion_id}/users/{user_id} | Exclui um usuário da promoção
*UsuriosNaPromooApi* | [**promotionUsersIndex**](docs/Api/UsuriosNaPromooApi.md#promotionusersindex) | **GET** /v3/promotion/{promotion_id}/users | Busca por um usuário cadastrado na promoção
*UsuriosNaPromooApi* | [**promotionUsersUpdate**](docs/Api/UsuriosNaPromooApi.md#promotionusersupdate) | **PATCH** /v3/promotion/{promotion_id}/users | Cadastra ou atualiza um usuário na promoção
*UsuriosNaPromooApi* | [**promotionUsersWebhook**](docs/Api/UsuriosNaPromooApi.md#promotionuserswebhook) | **POST** /webhook-do-usuario | Webhook de resposta ao registro de usuário

## Models

- [AddLuckyNumberCustom](docs/Model/AddLuckyNumberCustom.md)
- [AppHttpControllersAdminAdminControllerLogin200Response](docs/Model/AppHttpControllersAdminAdminControllerLogin200Response.md)
- [AppHttpControllersAdminAdminControllerLogin401Response](docs/Model/AppHttpControllersAdminAdminControllerLogin401Response.md)
- [AppHttpControllersAdminAdminControllerLoginRequest](docs/Model/AppHttpControllersAdminAdminControllerLoginRequest.md)
- [AppHttpControllersAdminAdminControllerMe200Response](docs/Model/AppHttpControllersAdminAdminControllerMe200Response.md)
- [AppHttpControllersAdminAdminControllerMe200ResponsePromotionsInner](docs/Model/AppHttpControllersAdminAdminControllerMe200ResponsePromotionsInner.md)
- [Article](docs/Model/Article.md)
- [ArticleCustomDataInner](docs/Model/ArticleCustomDataInner.md)
- [Award](docs/Model/Award.md)
- [Awarded](docs/Model/Awarded.md)
- [Branding](docs/Model/Branding.md)
- [BrandingMenuInner](docs/Model/BrandingMenuInner.md)
- [BrandingSocial](docs/Model/BrandingSocial.md)
- [Content](docs/Model/Content.md)
- [Coupon](docs/Model/Coupon.md)
- [CouponProductsInner](docs/Model/CouponProductsInner.md)
- [CouponWebhookError](docs/Model/CouponWebhookError.md)
- [CouponWebhookErrorContent](docs/Model/CouponWebhookErrorContent.md)
- [CouponWebhookErrorContentAllOfErrors](docs/Model/CouponWebhookErrorContentAllOfErrors.md)
- [CouponWebhookSuccess](docs/Model/CouponWebhookSuccess.md)
- [LuckyNumber](docs/Model/LuckyNumber.md)
- [Order](docs/Model/Order.md)
- [OrderCustomDataInner](docs/Model/OrderCustomDataInner.md)
- [Pagination](docs/Model/Pagination.md)
- [PaginationLinksInner](docs/Model/PaginationLinksInner.md)
- [Product](docs/Model/Product.md)
- [Promotion](docs/Model/Promotion.md)
- [PromotionArticlesCreate200Response](docs/Model/PromotionArticlesCreate200Response.md)
- [PromotionArticlesCreate400Response](docs/Model/PromotionArticlesCreate400Response.md)
- [PromotionArticlesCreate401Response](docs/Model/PromotionArticlesCreate401Response.md)
- [PromotionArticlesDelete200Response](docs/Model/PromotionArticlesDelete200Response.md)
- [PromotionArticlesDelete400Response](docs/Model/PromotionArticlesDelete400Response.md)
- [PromotionArticlesDelete401Response](docs/Model/PromotionArticlesDelete401Response.md)
- [PromotionArticlesIndex200Response](docs/Model/PromotionArticlesIndex200Response.md)
- [PromotionArticlesIndex400Response](docs/Model/PromotionArticlesIndex400Response.md)
- [PromotionArticlesIndex401Response](docs/Model/PromotionArticlesIndex401Response.md)
- [PromotionArticlesUpdate200Response](docs/Model/PromotionArticlesUpdate200Response.md)
- [PromotionArticlesUpdate400Response](docs/Model/PromotionArticlesUpdate400Response.md)
- [PromotionArticlesUpdate401Response](docs/Model/PromotionArticlesUpdate401Response.md)
- [PromotionAwardedsSearch200Response](docs/Model/PromotionAwardedsSearch200Response.md)
- [PromotionAwardedsSearch400Response](docs/Model/PromotionAwardedsSearch400Response.md)
- [PromotionAwardedsSearch401Response](docs/Model/PromotionAwardedsSearch401Response.md)
- [PromotionAwardedsStates200Response](docs/Model/PromotionAwardedsStates200Response.md)
- [PromotionAwardedsStates200ResponseContentInner](docs/Model/PromotionAwardedsStates200ResponseContentInner.md)
- [PromotionAwardedsUpdate200Response](docs/Model/PromotionAwardedsUpdate200Response.md)
- [PromotionAwardedsUpdate400Response](docs/Model/PromotionAwardedsUpdate400Response.md)
- [PromotionAwardedsUpdate401Response](docs/Model/PromotionAwardedsUpdate401Response.md)
- [PromotionAwardsCreate200Response](docs/Model/PromotionAwardsCreate200Response.md)
- [PromotionAwardsCreate400Response](docs/Model/PromotionAwardsCreate400Response.md)
- [PromotionAwardsCreate401Response](docs/Model/PromotionAwardsCreate401Response.md)
- [PromotionAwardsDelete200Response](docs/Model/PromotionAwardsDelete200Response.md)
- [PromotionAwardsDelete400Response](docs/Model/PromotionAwardsDelete400Response.md)
- [PromotionAwardsDelete401Response](docs/Model/PromotionAwardsDelete401Response.md)
- [PromotionAwardsIndex200Response](docs/Model/PromotionAwardsIndex200Response.md)
- [PromotionAwardsIndex400Response](docs/Model/PromotionAwardsIndex400Response.md)
- [PromotionAwardsIndex401Response](docs/Model/PromotionAwardsIndex401Response.md)
- [PromotionAwardsUpdate200Response](docs/Model/PromotionAwardsUpdate200Response.md)
- [PromotionAwardsUpdate400Response](docs/Model/PromotionAwardsUpdate400Response.md)
- [PromotionAwardsUpdate401Response](docs/Model/PromotionAwardsUpdate401Response.md)
- [PromotionBlacklistCreate200Response](docs/Model/PromotionBlacklistCreate200Response.md)
- [PromotionBlacklistCreate200ResponseContentInner](docs/Model/PromotionBlacklistCreate200ResponseContentInner.md)
- [PromotionBlacklistCreate400Response](docs/Model/PromotionBlacklistCreate400Response.md)
- [PromotionBlacklistCreate401Response](docs/Model/PromotionBlacklistCreate401Response.md)
- [PromotionBlacklistCreateRequest](docs/Model/PromotionBlacklistCreateRequest.md)
- [PromotionBlacklistDelete200Response](docs/Model/PromotionBlacklistDelete200Response.md)
- [PromotionBlacklistDelete400Response](docs/Model/PromotionBlacklistDelete400Response.md)
- [PromotionBlacklistDelete401Response](docs/Model/PromotionBlacklistDelete401Response.md)
- [PromotionBlacklistIndex200Response](docs/Model/PromotionBlacklistIndex200Response.md)
- [PromotionBlacklistIndex200ResponseContentInner](docs/Model/PromotionBlacklistIndex200ResponseContentInner.md)
- [PromotionBlacklistIndex400Response](docs/Model/PromotionBlacklistIndex400Response.md)
- [PromotionBrandingIndex200Response](docs/Model/PromotionBrandingIndex200Response.md)
- [PromotionBrandingIndex400Response](docs/Model/PromotionBrandingIndex400Response.md)
- [PromotionBrandingIndex401Response](docs/Model/PromotionBrandingIndex401Response.md)
- [PromotionBrandingUpdate200Response](docs/Model/PromotionBrandingUpdate200Response.md)
- [PromotionBrandingUpdate400Response](docs/Model/PromotionBrandingUpdate400Response.md)
- [PromotionBrandingUpdate401Response](docs/Model/PromotionBrandingUpdate401Response.md)
- [PromotionConfigWebhook200Response](docs/Model/PromotionConfigWebhook200Response.md)
- [PromotionConfigWebhook400Response](docs/Model/PromotionConfigWebhook400Response.md)
- [PromotionConfigWebhook401Response](docs/Model/PromotionConfigWebhook401Response.md)
- [PromotionConfigWebhookRequest](docs/Model/PromotionConfigWebhookRequest.md)
- [PromotionConfigsIndex200Response](docs/Model/PromotionConfigsIndex200Response.md)
- [PromotionConfigsIndex400Response](docs/Model/PromotionConfigsIndex400Response.md)
- [PromotionConfigsIndex401Response](docs/Model/PromotionConfigsIndex401Response.md)
- [PromotionContentCreate200Response](docs/Model/PromotionContentCreate200Response.md)
- [PromotionContentCreate400Response](docs/Model/PromotionContentCreate400Response.md)
- [PromotionContentCreate401Response](docs/Model/PromotionContentCreate401Response.md)
- [PromotionContentIndex200Response](docs/Model/PromotionContentIndex200Response.md)
- [PromotionContentIndex400Response](docs/Model/PromotionContentIndex400Response.md)
- [PromotionContentIndex401Response](docs/Model/PromotionContentIndex401Response.md)
- [PromotionCouponsCreate200Response](docs/Model/PromotionCouponsCreate200Response.md)
- [PromotionCouponsCreate401Response](docs/Model/PromotionCouponsCreate401Response.md)
- [PromotionCouponsCreate409Response](docs/Model/PromotionCouponsCreate409Response.md)
- [PromotionCouponsCreateRequest](docs/Model/PromotionCouponsCreateRequest.md)
- [PromotionCouponsDelete200Response](docs/Model/PromotionCouponsDelete200Response.md)
- [PromotionCouponsDelete400Response](docs/Model/PromotionCouponsDelete400Response.md)
- [PromotionCouponsDelete401Response](docs/Model/PromotionCouponsDelete401Response.md)
- [PromotionCouponsIndex200Response](docs/Model/PromotionCouponsIndex200Response.md)
- [PromotionCouponsIndex200ResponseContentInner](docs/Model/PromotionCouponsIndex200ResponseContentInner.md)
- [PromotionCouponsIndex400Response](docs/Model/PromotionCouponsIndex400Response.md)
- [PromotionCouponsIndex401Response](docs/Model/PromotionCouponsIndex401Response.md)
- [PromotionCouponsUpdate201Response](docs/Model/PromotionCouponsUpdate201Response.md)
- [PromotionCouponsUpdate401Response](docs/Model/PromotionCouponsUpdate401Response.md)
- [PromotionCouponsUpdate409Response](docs/Model/PromotionCouponsUpdate409Response.md)
- [PromotionCuponsWebhookRequest](docs/Model/PromotionCuponsWebhookRequest.md)
- [PromotionDatetime](docs/Model/PromotionDatetime.md)
- [PromotionDatetimeActive](docs/Model/PromotionDatetimeActive.md)
- [PromotionDatetimeDelivery](docs/Model/PromotionDatetimeDelivery.md)
- [PromotionDatetimeParticipate](docs/Model/PromotionDatetimeParticipate.md)
- [PromotionDatetimeShowAwardeds](docs/Model/PromotionDatetimeShowAwardeds.md)
- [PromotionDocumentRulesIndex200Response](docs/Model/PromotionDocumentRulesIndex200Response.md)
- [PromotionDocumentRulesIndex200ResponseContent](docs/Model/PromotionDocumentRulesIndex200ResponseContent.md)
- [PromotionDocumentRulesIndex200ResponseContentRegulationsInner](docs/Model/PromotionDocumentRulesIndex200ResponseContentRegulationsInner.md)
- [PromotionDocumentRulesIndex400Response](docs/Model/PromotionDocumentRulesIndex400Response.md)
- [PromotionDocumentRulesIndex401Response](docs/Model/PromotionDocumentRulesIndex401Response.md)
- [PromotionDocumentRulesRegulationDelete200Response](docs/Model/PromotionDocumentRulesRegulationDelete200Response.md)
- [PromotionDocumentRulesRegulationDelete400Response](docs/Model/PromotionDocumentRulesRegulationDelete400Response.md)
- [PromotionDocumentRulesRegulationDelete401Response](docs/Model/PromotionDocumentRulesRegulationDelete401Response.md)
- [PromotionDocumentRulesUpdate200Response](docs/Model/PromotionDocumentRulesUpdate200Response.md)
- [PromotionDocumentRulesUpdate400Response](docs/Model/PromotionDocumentRulesUpdate400Response.md)
- [PromotionDocumentRulesUpdate401Response](docs/Model/PromotionDocumentRulesUpdate401Response.md)
- [PromotionDocumentRulesUpdateRequest](docs/Model/PromotionDocumentRulesUpdateRequest.md)
- [PromotionDocumentRulesUpdateRequestRegulationsInner](docs/Model/PromotionDocumentRulesUpdateRequestRegulationsInner.md)
- [PromotionFaqCreate200Response](docs/Model/PromotionFaqCreate200Response.md)
- [PromotionFaqCreate400Response](docs/Model/PromotionFaqCreate400Response.md)
- [PromotionFaqCreate401Response](docs/Model/PromotionFaqCreate401Response.md)
- [PromotionFaqCreateRequestInner](docs/Model/PromotionFaqCreateRequestInner.md)
- [PromotionFaqDelete200Response](docs/Model/PromotionFaqDelete200Response.md)
- [PromotionFaqDelete400Response](docs/Model/PromotionFaqDelete400Response.md)
- [PromotionFaqDelete401Response](docs/Model/PromotionFaqDelete401Response.md)
- [PromotionFaqIndex200Response](docs/Model/PromotionFaqIndex200Response.md)
- [PromotionFaqIndex200ResponseContentInner](docs/Model/PromotionFaqIndex200ResponseContentInner.md)
- [PromotionFaqIndex400Response](docs/Model/PromotionFaqIndex400Response.md)
- [PromotionFaqIndex401Response](docs/Model/PromotionFaqIndex401Response.md)
- [PromotionFaqUpdate200Response](docs/Model/PromotionFaqUpdate200Response.md)
- [PromotionFaqUpdate400Response](docs/Model/PromotionFaqUpdate400Response.md)
- [PromotionFaqUpdate401Response](docs/Model/PromotionFaqUpdate401Response.md)
- [PromotionLuckyNumbersAddCustom200Response](docs/Model/PromotionLuckyNumbersAddCustom200Response.md)
- [PromotionLuckyNumbersAddCustom400Response](docs/Model/PromotionLuckyNumbersAddCustom400Response.md)
- [PromotionLuckyNumbersAddCustom401Response](docs/Model/PromotionLuckyNumbersAddCustom401Response.md)
- [PromotionLuckyNumbersRemove200Response](docs/Model/PromotionLuckyNumbersRemove200Response.md)
- [PromotionLuckyNumbersRemove400Response](docs/Model/PromotionLuckyNumbersRemove400Response.md)
- [PromotionLuckyNumbersRemove401Response](docs/Model/PromotionLuckyNumbersRemove401Response.md)
- [PromotionLuckyNumbersRemoveRequest](docs/Model/PromotionLuckyNumbersRemoveRequest.md)
- [PromotionLuckyNumbersRemoveRequestLuckyNumbersInner](docs/Model/PromotionLuckyNumbersRemoveRequestLuckyNumbersInner.md)
- [PromotionLuckyNumbersSearch200Response](docs/Model/PromotionLuckyNumbersSearch200Response.md)
- [PromotionLuckyNumbersSearch400Response](docs/Model/PromotionLuckyNumbersSearch400Response.md)
- [PromotionLuckyNumbersSearch401Response](docs/Model/PromotionLuckyNumbersSearch401Response.md)
- [PromotionOrdersCreate200Response](docs/Model/PromotionOrdersCreate200Response.md)
- [PromotionOrdersCreate400Response](docs/Model/PromotionOrdersCreate400Response.md)
- [PromotionOrdersCreate401Response](docs/Model/PromotionOrdersCreate401Response.md)
- [PromotionOrdersCreateRequest](docs/Model/PromotionOrdersCreateRequest.md)
- [PromotionOrdersIndex200Response](docs/Model/PromotionOrdersIndex200Response.md)
- [PromotionOrdersIndex400Response](docs/Model/PromotionOrdersIndex400Response.md)
- [PromotionOrdersIndex401Response](docs/Model/PromotionOrdersIndex401Response.md)
- [PromotionOrdersUpdate200Response](docs/Model/PromotionOrdersUpdate200Response.md)
- [PromotionOrdersUpdate400Response](docs/Model/PromotionOrdersUpdate400Response.md)
- [PromotionOrdersUpdate401Response](docs/Model/PromotionOrdersUpdate401Response.md)
- [PromotionProductsCreate200Response](docs/Model/PromotionProductsCreate200Response.md)
- [PromotionProductsCreate401Response](docs/Model/PromotionProductsCreate401Response.md)
- [PromotionProductsCreate409Response](docs/Model/PromotionProductsCreate409Response.md)
- [PromotionProductsCreateRequest](docs/Model/PromotionProductsCreateRequest.md)
- [PromotionProductsDelete200Response](docs/Model/PromotionProductsDelete200Response.md)
- [PromotionProductsDelete400Response](docs/Model/PromotionProductsDelete400Response.md)
- [PromotionProductsDelete401Response](docs/Model/PromotionProductsDelete401Response.md)
- [PromotionProductsIndex200Response](docs/Model/PromotionProductsIndex200Response.md)
- [PromotionProductsIndex400Response](docs/Model/PromotionProductsIndex400Response.md)
- [PromotionProductsIndex401Response](docs/Model/PromotionProductsIndex401Response.md)
- [PromotionProductsUpdate201Response](docs/Model/PromotionProductsUpdate201Response.md)
- [PromotionProductsUpdate401Response](docs/Model/PromotionProductsUpdate401Response.md)
- [PromotionProductsUpdate409Response](docs/Model/PromotionProductsUpdate409Response.md)
- [PromotionRafflesCreate200Response](docs/Model/PromotionRafflesCreate200Response.md)
- [PromotionRafflesCreate400Response](docs/Model/PromotionRafflesCreate400Response.md)
- [PromotionRafflesCreate401Response](docs/Model/PromotionRafflesCreate401Response.md)
- [PromotionRafflesCreateRequestInner](docs/Model/PromotionRafflesCreateRequestInner.md)
- [PromotionRafflesDelete200Response](docs/Model/PromotionRafflesDelete200Response.md)
- [PromotionRafflesDelete400Response](docs/Model/PromotionRafflesDelete400Response.md)
- [PromotionRafflesDelete401Response](docs/Model/PromotionRafflesDelete401Response.md)
- [PromotionRafflesIndex200Response](docs/Model/PromotionRafflesIndex200Response.md)
- [PromotionRafflesIndex400Response](docs/Model/PromotionRafflesIndex400Response.md)
- [PromotionRafflesIndex401Response](docs/Model/PromotionRafflesIndex401Response.md)
- [PromotionRafflesReportRequest](docs/Model/PromotionRafflesReportRequest.md)
- [PromotionRafflesUpdate200Response](docs/Model/PromotionRafflesUpdate200Response.md)
- [PromotionRafflesUpdate400Response](docs/Model/PromotionRafflesUpdate400Response.md)
- [PromotionRafflesUpdate401Response](docs/Model/PromotionRafflesUpdate401Response.md)
- [PromotionRafflesUpdateRequestInner](docs/Model/PromotionRafflesUpdateRequestInner.md)
- [PromotionStoresCreate200Response](docs/Model/PromotionStoresCreate200Response.md)
- [PromotionStoresCreate401Response](docs/Model/PromotionStoresCreate401Response.md)
- [PromotionStoresCreate409Response](docs/Model/PromotionStoresCreate409Response.md)
- [PromotionStoresCreateRequest](docs/Model/PromotionStoresCreateRequest.md)
- [PromotionStoresDelete200Response](docs/Model/PromotionStoresDelete200Response.md)
- [PromotionStoresDelete400Response](docs/Model/PromotionStoresDelete400Response.md)
- [PromotionStoresDelete401Response](docs/Model/PromotionStoresDelete401Response.md)
- [PromotionStoresIndex200Response](docs/Model/PromotionStoresIndex200Response.md)
- [PromotionStoresIndex400Response](docs/Model/PromotionStoresIndex400Response.md)
- [PromotionStoresIndex401Response](docs/Model/PromotionStoresIndex401Response.md)
- [PromotionStoresUpdate201Response](docs/Model/PromotionStoresUpdate201Response.md)
- [PromotionStoresUpdate401Response](docs/Model/PromotionStoresUpdate401Response.md)
- [PromotionStoresUpdate409Response](docs/Model/PromotionStoresUpdate409Response.md)
- [PromotionTicketsCreate200Response](docs/Model/PromotionTicketsCreate200Response.md)
- [PromotionTicketsCreate400Response](docs/Model/PromotionTicketsCreate400Response.md)
- [PromotionTicketsCreate401Response](docs/Model/PromotionTicketsCreate401Response.md)
- [PromotionTicketsDelete200Response](docs/Model/PromotionTicketsDelete200Response.md)
- [PromotionTicketsDelete400Response](docs/Model/PromotionTicketsDelete400Response.md)
- [PromotionTicketsDelete401Response](docs/Model/PromotionTicketsDelete401Response.md)
- [PromotionTicketsIndex200Response](docs/Model/PromotionTicketsIndex200Response.md)
- [PromotionTicketsIndex400Response](docs/Model/PromotionTicketsIndex400Response.md)
- [PromotionTicketsIndex401Response](docs/Model/PromotionTicketsIndex401Response.md)
- [PromotionTicketsUpdate200Response](docs/Model/PromotionTicketsUpdate200Response.md)
- [PromotionTicketsUpdate400Response](docs/Model/PromotionTicketsUpdate400Response.md)
- [PromotionUsersCreate201Response](docs/Model/PromotionUsersCreate201Response.md)
- [PromotionUsersCreate401Response](docs/Model/PromotionUsersCreate401Response.md)
- [PromotionUsersCreate409Response](docs/Model/PromotionUsersCreate409Response.md)
- [PromotionUsersCreateRequest](docs/Model/PromotionUsersCreateRequest.md)
- [PromotionUsersDelete200Response](docs/Model/PromotionUsersDelete200Response.md)
- [PromotionUsersDelete400Response](docs/Model/PromotionUsersDelete400Response.md)
- [PromotionUsersDelete401Response](docs/Model/PromotionUsersDelete401Response.md)
- [PromotionUsersIndex200Response](docs/Model/PromotionUsersIndex200Response.md)
- [PromotionUsersUpdate201Response](docs/Model/PromotionUsersUpdate201Response.md)
- [PromotionUsersWebhook200Response](docs/Model/PromotionUsersWebhook200Response.md)
- [PromotionUsersWebhookRequest](docs/Model/PromotionUsersWebhookRequest.md)
- [Raffle](docs/Model/Raffle.md)
- [SerieNumber](docs/Model/SerieNumber.md)
- [Store](docs/Model/Store.md)
- [Ticket](docs/Model/Ticket.md)
- [User](docs/Model/User.md)
- [UserCustomData](docs/Model/UserCustomData.md)
- [UserWebhookError](docs/Model/UserWebhookError.md)
- [UserWebhookErrorContent](docs/Model/UserWebhookErrorContent.md)
- [UserWebhookErrorContentAllOfErrors](docs/Model/UserWebhookErrorContentAllOfErrors.md)
- [UserWebhookSuccess](docs/Model/UserWebhookSuccess.md)

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
