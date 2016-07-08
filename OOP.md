##The 4 pillars of object oriented programming.

###Inheritance

-Inheritance is where you create a base class with generic methods and then a subclass 'inherits' those parent class's methods

-i.e if you have create a person class with method movement_speed you could create a subclass called runningperson where runningperson has the same method movement_speed


###Polymorphism

-Polymorphism is where you use one interface for mupltiple different functions.

-Using the above example of person and runningperson, the person has a base movement speed set to 3m/s. So in this case runningperson would also have 3m/s but since we want runningperson to actually be running we would use polymorphism to change runningpersons speed to 9m/s in the movement_speed method

-This is where you use the ```abstract``` or the ```virtual``` class modifier to declare a class that is 'incomplete'

-virtual methods have an implementation (contain code) and derived class have the option to ```override``` them however abstract forces the derived classes to use ```override``` and provide a custom implementation.


###Abstraction 

-Abstraction is a process to abstract or hide the functionality and provide users or other programmers to use it only.

-i.e Console.WriteLine we call this method and pass in arguments but you cannot see what is happening behind the function calling

###Encapsulation 

-Encapsulation means to put all relevant methods into one class


####Example of abstration and Encapsulation

<pre><code>
class User{
    public bool AddUser(string name, string email, string phone){
        if (ValidateUser(name, email, phone)){
            if (AddtoDb(name, email, phone) > 0){
                return true;
            }
        }
        return false;
    }

    private bool ValidateUser(string name, string email, string phone){
        // do your validation
        return true;
    }

    private int AddtoDb(string name, string email, string phone){
      // Write the Db code to insert the data
        return 1;
    }
}
</code></pre>

Then to call the adduser method

<pre><code>

class Program{
    static void Main(string[] args){
        User objUser = new User();
        bool f = objUser.AddUser("Arka", "ark@g.com", "1234567890");
    }
}

</code></pre>


We are hide the procedure of adding data into database from other users, //Abstraction. And putting all the three methods into one User class and providing other users to use it.//Encapsulation.

References:

http://www.codeproject.com/Articles/1037139/Difference-between-Encapsulation-and-Abstraction-i
http://stackoverflow.com/questions/14728761/difference-between-virtual-and-abstract-methods
