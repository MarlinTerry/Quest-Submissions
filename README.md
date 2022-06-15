# Quest-Submissions

# Chapter 1 Day 1

1. The Blockchain is an open, decentralized database where anyone can store data.
2. A Smart Contract is like a rulebook that allows users to make transactions on the Blockchain.
3. A transaction is a paid function that changes data on the Blockchain. A script is a free transaction that allows you to view data, but does not change the data.


# Chapter 1 Day 2

1. The Five Cadence Programming Language Pillars: Safety and Security, Clarity, Approachability, Developer Experience, and Resource Oriented Programming.
2. Flow was developed largely in response to the faults of the Ethereum blockchain, and the five pillars represent the biggest improvements Flow seeks to make. So keeping these five items top of mind and at the forefront of Cadence is essential.

 
# Chapter 2 Day 1

1. pub contract JacobTucker {
  pub let is: String

  init() {
    self.is = "the best"

  }

}

2. import JacobTucker from 0x03

pub fun main(): String  {
  return JacobTucker.is
  
}

# Chapter 2 Day 2 

1. changeGreeting would be used to make changes on the blockchain. Scripts are only for viewing data, so you couldn't use changeGreeting in a script.
2. AuthAccount means an account (or user) on Flow.
3. Prepare access the data in your account. Execute changes data on the blockchain.
4. Contract 
pub contract HelloWorld {

    pub var greeting: String
    
    pub var myNumber: Int

    pub fun changeGreeting(newGreeting: String) {
    self.greeting = newGreeting
    }

    pub fun updateMyNumber(newNumber: Int) {
        self.myNumber = newNumber
        }

    init() {
        self.greeting = "Hello, World!"
        self.myNumber = 0
    }
    
}


Transaction 

import HelloWorld from 0x01

transaction(myNewNumber: Int) {

  prepare(signer: AuthAccount) {}

  execute {
    HelloWorld.updateMyNumber(newNumber: myNewNumber)
    }
}

Script

import HelloWorld from 0x01

pub fun main(): Int {
    return HelloWorld.myNumber
}

# Chapter 2 Day 3











