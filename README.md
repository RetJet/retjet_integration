# Integration with Retjet

The Retjet platform enables integration with numerous sales platforms available on the market. However, if your store is built using custom software, you can carry out the integration using our default connector.

To do this, you need to prepare the appropriate set of methods and authorization using a token.

Note! If your platform already has a built-in authorization system other than API Token and you would like to authorize access to your API using the aforementioned mechanism, please contact us.

## Required methods:

1. Searching for orders using the customer's email address and order number. Sample request:

```
curl -X POST 'https://your-shop.com/api/get.orders.json' \
--header 'Authorization: ••••••' \
--data-urlencode 'email=customer@email.ltd' \
--data-urlencode 'orderNo=order-ref-id'
```


The JSON response is specified in the [get.orders.json](https://github.com/RetJet/custom-rest/blob/main/get.orders.json) file.


2. Full list of orders statuses
```
curl -X GET 'https://your-shop.com/api/get.statuses.json' \
--header 'Authorization: ••••••'
```

The JSON response is specified in the [get.statuses.json](https://github.com/RetJet/custom-rest/blob/main/get.statuses.json) file.
