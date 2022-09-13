# Object Oriented Programming

## The idea is to marry state and behavior

```vb
Dim myName as String
Set myName = "Jeff"

myName = UCase(myName)

```



```csharp
var myName = "Jeff";

myName = myName.ToUpper();



```

## Objects have:

### State
variables that the object "owns"

In .NET state is in class level variables, we use the term `Fields` for these.


### Behavior
code that can be invoked that has something to do with the data (state) owned by that object.

In .Net, the behavior is methods.

Constructors

Properties

Events


## Example

I have an object that represents a bank account.

### State 
Bank Accounts have a current balance.
```csharp
public class BankAccount 
{
    private decimal _currentBalance = 0;

}

```

### Behaviors

We can make a deposit, and make a withdraw, and we can retreive our balance.

```csharp
public class BankAccount 
{
    private decimal _currentBalance = 0;

    public void Deposit(decimal amount) 
    {
        _currentBalance += amount;
    }

    public void Withdraw(decimal amount)
    {
        _currentBalance -= amount;
    }

    public decimal GetBalance()
    {
        return _currentBalance;
    }

}

```

