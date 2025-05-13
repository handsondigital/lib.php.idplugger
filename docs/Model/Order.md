# # Order

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** | Id do pedido | [optional]
**user_id** | **int** | Id do usuário | [optional]
**payment_id** | **string** | Id do pagamento | [optional]
**payment_gateway** | **string** | Gateway de pagamento | [optional]
**amount** | **float** | Valor total do pedido |
**coupon_id** | **int** | Id do cupom gerado pelo pedido | [optional]
**status** | **string** | Estado atual do pedido | [optional] [default to 'pending']
**created_at** | **string** | Data em que o pedido foi criado | [optional]
**updated_at** | **string** | Data em que o pedido foi atualizado | [optional]
**coupon** | [**\IdPluggerPromotion\Model\Coupon**](Coupon.md) |  | [optional]
**lucky_numbers** | [**\IdPluggerPromotion\Model\LuckyNumber[]**](LuckyNumber.md) |  | [optional]
**custom_data** | [**\IdPluggerPromotion\Model\OrderCustomDataInner[]**](OrderCustomDataInner.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
