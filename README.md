# INFO7255
# Extract transactions corresponding to approved UUIDs and calculate total balance
Post2:

{
    "objectId": "planCostShares_1234",
    "objectType": "planCostShares",
    "planCostShares": {
        "deductible": 10,
        "_org": "org",
        "copay": 5,
        "objectId": "123",
        "objectType": "planCostShares"
    },
    "linkedplanServices": [
        {
            "linkedService": {
                "_org": "MGH",
                "objectId": "123_1234",
                "objectType": "linkedService",
                "name": "MGH_Basic"
            },
            "planserviceCostShares": {
                "deductible": 10,
                "_org": "org",
                "copay": 5,
                "objectId": "123_2",
                "objectType": "planServiceCostShares"
            },
            "_org": "MGH",
            "objectId": "123_4",
            "objectType": "linkedplanService"
        }
    ],
    "_org": "Blue Cross Blue Shield",
    "planType": "Insurance",
    "creationDate": "2020-07-30T14:00:00.000-04"
}


Post:
http://localhost:8080/v1/plan/

{
  "objectId": "planCostShares_1234",
  "objectType": "planCostShares",
  "planCostShares": {
    "deductible": 10,
    "_org": "org",
    "copay": 5,
    "objectId": "123",
    "objectType": "planCostShares"
  },
  "linkedplanServices": [
    {
      "linkedService": {
        "_org": "MGH",
        "objectId": "123_1",
        "objectType": "linkedService",
        "name": "MGH_Basic"
      },
      "planserviceCostShares": {
        "deductible": 10,
        "_org": "org",
        "copay": 5,
        "objectId": "123_2",
        "objectType": "planServiceCostShares"
      },
      "_org": "MGH",
      "objectId": "123_4",
      "objectType": "linkedplanService"
    }
  ],
  "_org": "Blue Cross Blue Shield",
  "planType": "Insurance",
  "creationDate": "2020-07-30T14:00:00.000-04"
}







curl --location 'http://localhost:8080/v1/plan/' \
--header 'Content-Type: application/json' \
--header 'Cookie: JSESSIONID=709A630F8A0FB3E596F4395ABF4E1306' \
--data '{
  "objectId": "planCostShares_1234",
  "objectType": "planCostShares",
  "planCostShares": {
    "deductible": 10,
    "_org": "org",
    "copay": 5,
    "objectId": "123",
    "objectType": "planCostShares"
  },
  "linkedplanServices": [
    {
      "linkedService": {
        "_org": "MGH",
        "objectId": "123_1",
        "objectType": "linkedService",
        "name": "MGH_Basic"
      },
      "planserviceCostShares": {
        "deductible": 10,
        "_org": "org",
        "copay": 5,
        "objectId": "123_2",
        "objectType": "planServiceCostShares"
      },
      "_org": "MGH",
      "objectId": "123_4",
      "objectType": "linkedplanService"
    }
  ],
  "_org": "Blue Cross Blue Shield",
  "planType": "Insurance",
  "creationDate": "2020-07-30T14:00:00.000-04"
}'



  
    

Get:
http://localhost:8080/v1/plan/planCostShares_1

curl --location 'http://localhost:8080/v1/plan/planCostShares_1' \
--header 'Cookie: JSESSIONID=709A630F8A0FB3E596F4395ABF4E1306'
