# Contract Summary: 

The contract allows an owner to store an amount and retrieve it.
The owner is set when the contract is first deployed.
It also allows to get the address of owner.




# Issues and Effects:

## 1
### Issue : 
The contract does not check for any authorization before storing the amount. 
### Effect :
Anyone can call the store function and overwrite the previous stored value, whether it is the owner or anyone else.

## 2
### Issue : 
No functionality for transferring the ownership. 
### Effect :
Once deployed, owner cannot be changed.

## 3
### Issue :
The contract does not have any functionality to stop or pause the contract. 
### Effect :
This means once the contract is deployed, it will always accept transactions.

## 4
### Issue :
store() function stores a variable named str in 'memory' instead of 'storage'. It also assigns the _amount and user after creation. 
### Effect
It will cause error if 'memory' is changed to 'storage'.


# Improvement Steps:

### 1
Implementation of an authorization mechanism to restrict the store function to the owner only. 'require' statements or modifiers may prove useful.
### 2
Addition of a function to transfer ownership to a new owner, if it will be required.
### 3
Implementation of a function or method to stop or pause the contract in case of an emergency.
### 4
store() function can be further simplified to avoid possible errors and improve code.