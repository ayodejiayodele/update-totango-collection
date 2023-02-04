# update-totango-collection
Custom action to create or update collection records in Totango.


This action creates or updates Totango collection records. To make use of this action, you must have a Totango account and have configured a collection in your Totango instance. It makes use of the [Totango Integration Hub API](https://int-hub.totango.com/#tag/collections).

### Inputs
You will need the following information to use this action:
 - The internal name of the collection to create/update e.g. 'leads'. This is the value of the 'collection-type' input and should not have spaces.
 - The service ID of your Totango instance, usually in the format of '123456789'. To learn how to find your Totango service ID, visit [how to find Totango token](https://support.totango.com/hc/en-us/articles/203036939-Where-can-I-find-my-Totango-Token#h_01FTE6NV9XXJNXKTEVZ6557CZD).
 - The Totango API token. To learn how to find your Totango API key, visit [how to find Service ID](https://support.totango.com/hc/en-us/articles/203036939-Where-can-I-find-my-Totango-Token#h_01FTE6M3BNN50ESP177HPNXRJ4).
 - The path to the JSON payload to send to Totango e.g. documents/accounts/new-leads.json.
 ## Sample Payload
```json
{
    "collections": [
        {
            "id": 8182,
            "customer_id": "01d0Q3ul7AANB",
            "attributes": {
                "Customer Name": "Integrity Plus",
                "Type": "SMB",
                "ContactDate": "2022-11-30T20:29:19Z",
                "Sales Officer": "info@intolu.com",
                "Product Interest": "Tier 4,Shampoo, Conditioner"
            }
        },
        {
            "id": 8183,
            "customer_id": "01d073ul7AANB",
            "attributes": {
                "Customer Name": "Long Shanks",
                "Type": "Enterprise",
                "ContactDate": "2022-10-30T20:29:19Z",
                "Sales Officer": "info@longshanks.com",
                "Product Interest": "Retainer Conditioner"
            }
        }
    ]
}
```
 For more information about Totango, see https://www.totango.com/