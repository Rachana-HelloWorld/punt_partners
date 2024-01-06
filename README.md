# punt_partners
Punt Partners assignment

APIs
1. Add repeat counts to a coupon code - Set a coupon code usage limit using this API. The coupon code repeat count can be set on the following
- Global Total Repeat Count
- User Total Repeat Count
- User Daily Repeat Count
- User Weekly Repeat Count
endpoint - POST service/coupon
requestbody and responseBody:
{
"code":"skdjhf",
"globalTotalRepeatCount" : 5,
"userTotalRepeatCount": 3,
"userDailyRepeatCount" 1,
"userWeeklyRepeatCount 5"
}
  
2. Verify Coupon code validity - Validate if coupon code exists and is valid for the given user and ensure count limit is not exceeded.
endpoint - GET users/userId/coupon?code="some_coupon_code"
response {"isValid":true}

3. Apply coupon code
endpoint - POST /users/userId/coupon?code="code"
- check validity of the coupon
- if coupon is valid then decrease repeat count in db
  
   
