------------------------------------------------------INSTRUCTIONS-------------------------------------------------------------------------------
Name: Carlos Gonzalo Villas Velazquez
Date: Nov 11, 2020

Homework Assignment #12: Object Oriented Programming

Details:
    What is object oriented programming, and why would you use it? As you may already know, many javascript projects are written using a functional, or event-driven design pattern. In which cases would an OOP pattern be a better choice?
    For this task, write a few paragraphs describing a project that would benefit greatly from an OOP structure. (This could be any kind of application, running on any type of system). Describe the application flow from the user's point of view (user stories). What is the application's purpose, and how would people use it? What information would they enter, and what would be received? Try to mention all the "stories" in which the user performs any kind of CRUD operation.
    Next, using pseudocode (or any other notation-technique or diagramming tool you wish), map out what the main objects of the system would look like, how they would be constructed, and how they would relate to each other. 
    Save your writeup in a Readme.md file, and push it to Github.

------------------------------------------------------HOMEWORK------------------------------------------------------------------------------------

What is object oriented programming, and why would you use it?

In object oriented programming:
    In object oriented programming, program is divided into small parts called objects.
    Object oriented programming follows bottom up approach.
    Object oriented programming have access specifiers like private, public, protected etc.
    Adding new data and function is easy.
    Object oriented programming provides data hiding so it is more secure.
    Overloading is possible in object oriented programming.
    In object oriented programming, data is more important than function.
    Object oriented programming is based on real world.
    Some languages that use this type of programming: C++, Java, Python, C# etc.

OOP is often the best use when:
    You have multiple programmers who don’t need to understand each component.
    There is a lot of code that could be shared and reused.
    The project is anticipated to change often and be added to over time.
    Different sections can benefit from different resources like datasource or hardware.

Standard game that could benefit greatly with OOP:

If you are creating a game where you have 5 different kinds of enemies and they all share the following abilities: Move, Seek Player, Attack, Flinch, Die. Also you have different animations, graphics, sounds associated for all those abilities, and for all 5 kinds of those enemies.
You can represent your problem as a whole if you just think of the enemies as one type: Enemy. Also you can define the definition for those abilities inside this class. When it’s time to define the enemies themselves, you’d inherit from this Enemy class.
Since you inherit from the Enemy class, you got those 5 abilities already defined for you. You can specialize their behavior. Anytime you ask an enemy to use an ability, regardless of their type, all you have to do is say: MyMonster.Attack() or MyMonster.Move(). 

class Monster {
    constructor(move, seek, attack, flinch, die){
    this.move = move;
    this.seek = seek;
    this.attack = attack;
    this.flinch = flinch;
    this.die = die;
    }

    attack {
        console.log(attack);
        attack += 1;
    }

    move {
        console.log(move);
    }
}

myMonster1 = new Monster("forward",true,1,false,10);
myMonster2 = new Monster("backwards",true,1,false,8);
myMonsterBoss = new Monster("everywhere",1,true,true,100);

myMonster1.Attack();
myMonsterBoss.Move();