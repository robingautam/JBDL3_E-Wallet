# JBDL3_E-Wallet

User Onboarding
curl --location 'localhost:8081/user-service/create/user' \
--header 'Content-Type: application/json' \
--header 'Cookie: JSESSIONID=4A20CC60622CE78215600E91324B2D11' \
--data-raw '{
    "name": "Sagar",
    "email": "sagar@gmail.com",
    "mobileNo": "8756789789",
    "password": "123456",
    "userIdentifier": "AADHAR",
    "userIdentifierValue": "787456087633"
}'

Transaction Initiate
curl --location --request POST 'localhost:8083/txn-service/initiate/transaction?amount=10&receiver=8756789789&purpose=sample%20txn' \
--header 'Authorization: Basic OTcxNzY3MzQ1NjoxMjM0NTY=' \
--header 'Cookie: JSESSIONID=4A20CC60622CE78215600E91324B2D11'
