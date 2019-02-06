# Mapping-Function-In-solidity


Mapping Function in solidity
 
 here the code ###
 
 
 
pragma solidity 0.5.1;

contract MyContract {


    uint256 peopleCount = 0;
    
    mapping(uint => person) public people; 

    struct Person {
         uint _id;
        string _firstName;
        string _lastName;
    }

    function addPerson(string memory _firstName, string memory _lastName) public {
         peopleCount + = 1;
         people[peopleCount] = person(peopleCount,_firstName,_lastName);
        //people.push(Person(_firstName, _lastName));
       
    }
}



We all know that , we run solidity code in online i.e Remix ide::::::
0.5.1 is the version of that ide to run in safe manner
here we introduced the struct person having two strngs 

mapping(uint => Person) public people;


This will be a mapping where we store person structs. 
It will replace the people array.
The key will be an unsigned integer, and the value will be a person struct. We'll treat the key like a database id

his uses the peopleCount counter cache to create an id for the person. 
Then it instantiates a new person struct with the id and the passed in attributes. 
