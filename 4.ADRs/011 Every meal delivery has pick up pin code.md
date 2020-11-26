# Every meal delivery has pick up pin code

Date: 2020-10-28

## Status 

Accepted

## Context

Network connection might be lost, when meal delivered to a fridge and a user come to grab it. Then the fridge can't check data of the user online by card swapping, or in-app distance opening. 
But the fridge have a pin pad keyboard and still have quite sofisticated software and internal memory to process orders. 

Update 2020-11-24: 

We except that every meal has it's own unique id provided by the kitchen, because some meals might be customized from the general catalog. Let's say lactose free lasania should be addressed to a specific user. 

Then, at the purchase or production process we can update user's device with the meal unique id and generate access code based on meal ID. 

## Decision

Dispatched from a Ghost Kitchen meals, will have a special 6-8 digit code. 

## Consequences

Now the user can grab the meal even if smart-fridge is disconected from the network at the moment of picking up meal. 

Pin codes for meals should be formed upfront and delivered early to devices (smart-fridge and user-device). Possibly, there might be a mechanism to update those codes with a prepared meal delivery. The pin code should be quite long to lower chance of brute-force attempt.   

**Bonus feature:** it's easier to delegate meal grabbing to other person. 

**Risks:** Someone can be so lucky that can guess a pin code from a first attempt. 

**Arguments:** 8th long digint codes are too long to type! 