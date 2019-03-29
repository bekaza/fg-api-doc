# Api Doc (Version - Beta)

## **Signature Algorithm** <span style="color:red">(update coming soon)</span>

***

## API : Create Order
Link : "https://fgproduction.paiduayapp.com/order/create"

Headers: 
```json
{
    "Content-Type": "application/json"
}
```

Method: POST

Request Parameter:

```json
{
    "sign": xxxxx, // update coming soon
    "status": 1,
    "purchase_channel": 2,
    "customer_id": 410486,
    "customer": {
        "tag": "",
        "name": "ff",
        "phone_number": "0855555555",
        "address": "หกหกห",
        "phone_number_sec": "",
        "sub_district": "แหลมสัก",
        "district": "อ่าวลึก",
        "province": "กระบี่",
        "zipcode": "81110",
        "customer_id": 410486,
        "shop_id": 154,
        "email": null,
    },
    "products": [
        {
            "product_id": 33354,
            "name": "ทดสอบ",
            "sku": "#015433354",
            "price": 1,
            "weight": 25,
            "shop_id": 154,
            "quantity": 1,
            "discount": 0,
            "total": 0
        }
    ],
    "note": "",
    "courier_id": 2,
    "courier_account_id": 9,
    "payment_type": 2,
    "delivery_cost": 0,
    "additional_discount": 0,
    "shop_id": 154
}
```

Response(JSON Form):
- success (bool)=> true, false
- data (JSON object)
- message(string) => error message when return success = false

```json
{
    "order_id":60464608,
    "order_number":"13662815",
    "tracking_number": "FGOOD13662815",
    "success":true
}
```

## API : Create Shipment
Link : "https://fgproduction.paiduayapp.com/order/create"

Headers:
```json
{
    "Content-Type": "application/json"
}
```

Method: GET

Request Parameter: tracking_number (query_string)

Request URL Example:
https://fgproduction.paiduayapp.com/courier/scg/create-shipment?tracking_number=111533498440

Response(JSON Form): 
- success (bool)=> true, false
- data (JSON object)
- message(string) => error message when return success = false


```json
{
   "data": {
       "CODAmount": "0",
       "ContactName": "สมบูรณ์  เมฆจรัสแสง",
       "DeliveryAddress": "10  ราฎอุทิศ  25  ตำบล/แขวง แสนแสบ อำเภอ/เขต มีนบุรี จังหวัดกรุงเทพมหานคร",
       "Note": "ถ้าติดต่อปลายทางไม่ได้ ให้ติดต่อต้นทางทุกกรณี",
       "OrderCode": "FGOOD48810884",
       "ShipperAddress": "322 ซ.อัมฤทธิ์ ตำบล/แขวง บางแค อำเภอ/เขต บางแค จังหวัดกรุงเทพมหานคร",
       "ShipperCode": "10038902",
       "ShipperName": "เอกสถาพร",
       "ShipperTel": "0972580015",
       "ShipperZipcode": "10160",
       "Tel": "0953284703",
       "TotalBoxs": "1",
       "TrackingNumber": "A121488108840A",
       "WeightKgs": "0.4",
       "Zipcode": "10510"
   },
   "success": true
}
```

## API : Get Tracking Status
Link : "https://fgproduction.paiduayapp.com/order/create"

Headers: 
```json
{
    "Content-Type": "application/json"
}
```

Method: POST

Request Parameter:

```json
{
    "order_number": "13662815",
    "sign": xxxxx // update coming soon
}
```

Response(JSON Form):
- success (bool)=> true, false
- data (JSON object)
- message(string) => error message when return success = false

```json
{
    "status": "พร้อมจัดส่ง",
    "success":true
}
```