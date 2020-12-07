# cm popular issues fixes

### check withdrawls disabled
- <code>select withdrawals_disabled from tbl_user where user_phone = '8750052131'</code>;
- steps to check withdrawls not working
- <code>select withdrawals_disabled, user_id from tbl_user where user_phone = '8750052131';</code>
- <code>select balance from wallet_balances where user_id = $$user_id;</code>


## How to check delivered GMV for a leader. If delivered GMV >= 5000, then he can get his commission, otherwise commission shows as processsing in Gullak.
- <code>select sum(total_after_discount) from order_items oi join orders o on o.order_id = oi.order_id and team_leader like '%9312074461' and processing_at > '2020-11-01' and order_item_status = 'DELIVERED';</code>
- check if processing
- <code> select amount, status, type from wallet_transactions_view where team_leader_phone_number = '7532857297' and created_at >= '2020-11-01' and created_at < '2020-12-01' and status = 'processing';</code>
## How to check if a leader was already a Cx before. We disallow him to become CL again. This can be removed via "mark undiscarded from admin" on team leaders page.
- <code>select already_a_cx, already_a_cx_wo_order from team_leaders where phone_number = '7761915827';</code>


## How to check if pincode is serviceable.
- <code>select * from pincodes where pincode = '123412';</code>


## How to change Leader
- [![alt text](https://i.ibb.co/Wz01Txy/Whats-App-Image-2020-11-27-at-1-55-15-PM.jpg)](https://i.ibb.co/Wz01Txy/Whats-App-Image-2020-11-27-at-1-55-15-PM.jpg)
