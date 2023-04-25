%dw 2.0
output application/json
---
//in this i used mapobject to change key and values after that i used map for all the key and values for the given indexes after i need to remove count key value pair from the given input so used the '-' operator to remove the specified values in the input
payload mapObject ((value, key, index) -> 
 (key): value map ((item, index1) ->
 item -"count"
 )
)
