### Design Patterns

1. Abstract_factory design pattern: the following steps are required in building a Jungle
a. Number of animals
b. Jungle Organism Factory

the above processes can esaily be accomplished via

            jungle = Habitat.new(JungleOrganismFactory.new, number_of_animals: 2)
which gives the output:

            Tiger Animal0 eats meat
            Roar
            Tiger Animal1 eats meat
            Roar

2. Singleton design pattern: This Configuration class shows the creation of the same configuration twice in line with the Singleton method. It does not get instantiated

3. Factory method design pattern: The folloeing steps are reuired in building  a shape
a. The shape to be built
b. The imension of shape to be built
c. Calling the draw method
This can easily be accomplished by
triangle = ShapeFactory.build(:triangle, 2, 3, 4)
triangle .draw

4. Bridge design pattern: the folllowing is reuired in getting a shape to be drawn on a system
a. The name of shape
b. The name of system
this can easily be accomplished by Rectangle.new(MacOs.new)
So the rectangle.draw shows up 'drawing a rectangle upon a Mac'

6. Command design pattern: the following is required to  adding an UIButton to add an item to a cart
a. The Item
b. The cart
this can easily be accomplished by running
    item = Item.new("Book")
    cart = Cart.get_current_cart
    command = AddItemToCartCommand.new(item, cart)
    button = UIButton.new(command)
    button.press_button

7. Composite design pattern: The following steps are required for showing that objects and compositions of objects are treated uniformly
a. add_sub_task(AddDryIngredientsTask.new)
b. add_sub_task(MakeBatterTask.new)

One can see that they both have intialize methods to store the name of the task an get_time_required to store
the time left for the task to be completed.

8. Decorator method design pattern: the following steps are required for getting the price of different types of coffee
a. the type of cofffee
this can esaily be aomplished by running CoffeeWithSugar.new(Coffee.new) to get the price

9. Facade design pattern: This is the following steps required to run the SubSytemClass#{number} class
a. call a new inststance of FacadeSystem class as in facade = FacadeSystem.new
b. call facade. method_1 or facede. method_2

10. Flyweight design pattern: these are the steps required to run FlyweightFactory
a. call the flyweightFActory Class as in flyweight_factory = FlyweightFactory.new
b. call flyget_flyweight("flyweight1") to see what get returned
c.  flyweight1.operation(10) to see the return



11. Interpreter design pattern: this are the steps required for the finding of an expression in the group of letters entered.
a. Context.new("AAABBBCCCDDD")
b. The steps required for getting TernimalExpressiong and NonTerminalExpression from AbstractExpression in   

12. Chain of responsibility design pattern: The following steps are required in answering questions
a. Call the the chain _of_responsibility.process request with the asked question inside
This can be answered by running chain_of_responsibility.process_request("Who is Harry Potter's best friend?") to give Answering a Harry Potter related question

13. Iterator design pattern: This is th rfollowing steps required to call and create new Portfolio elements
a. create a new portfolio: Portfolio.new
b. create a new Portfolio element: my_portfolio.add_account(Account.new('Stocks', 100))




14. Mediator design pattern: theses are the following steps required to find a word
a.submit a array of words
b. submit a Mediator with the value of the searched text_field
This can easily be solved by running 
list = List.new(["apple", "avocado", "banana", "kiwi", "mango", "watermelon"])
text_field = TextFieldWithObserver.new
mediator = ListSearchMediator.new(text_field, list)
text_field.value = "av"
puts list.words.inspect 
Which will give ['avocado']

15. Memento design pattern: Theses are the following steps need to store something in the mememto class
a. Crate an originator
b. Create a stste for saving it to memento
c. Create a state for restoring from memento
This can be acheived by running  
    caretaker = Caretaker.new
    originator = Originator.new
    originator.state = "name:foo"
    memento = originator.save_to_memento
    caretaker.memento = memento
    originator.state = "name:bar"
    originator.restore_from_memento(caretaker.memento)

16. Observer pattern: We ahave an 

The Observer pattern allows you to notify parts of your program that some other part of your program has changed. It does this while allowing you to vary the objects you wish to keep informed ( observers ) from the object being observed ( the subject ) independently. It enables a highly decoupled but well informed system. Critically, you are able to add observers to a subject without having to modify either the observer or the subject. the 'notify_observers' method is where the magic happens. It will notify all of the observer that an update has occurred. Each observer presumably shares an Observer interface of some kind. In our case, we're sticking with the most basic and traditional method within the Observer pattern tradition: 'update'. The 'observers' must all adhere to the same interface. Multiple observer of different class types can observe the same subject with ease.
What you choose to do with the information that has been broadcast to an observer is up to you. By the Way, the subject is a publisher and an observer is a subscriber. "Publish/Subscribe" is an alias for "Subject/Observer", which is the Observer pattern through and through. We'll create two observers and our subject. Next, we'll attach the two observers to the subject. Finally, we'll notify the observers that some change has occurred.

17. Proxy design pattern: provide a surrogate / placeholder for another object to control access to it.

AccountProtectionProxy creates an account if the account name is  `bamroc`. It can deposit some money and withdraw some money.

18. Prototype design pattern: Specify the kinds of objects to create using a prototypical instance, and create new objects by copying this prototype.

PizzaPrototype is calling pizza_type to select the menu type. The _clone method recreates a clone of the pizza.


19. State design pattern: Allow an object to alter its behaviour when its internal state changes. The object will appear to change its class.

ConcreteStateA class calls handleit requires

context = Context.new(state)

then

context.request

20. Strategy design pattern: Here, we create objects which represent various strategies and a context object whose behavior varies as per its strategy object. 

In the example attached, an instance of the Car class accepts an engine strategy. There are two engine strategies defined, StraightSixEngine and V8Engine. Each encapsulates a variant of an engine algorithm. Each shares a common interface. 

21. Visitor design pattern: represent an operation to be performed on the elements of an object structure. Visitor lets you define a new operation without changing the classes of the elements on which it operates.

Order contains an array of product and exposes simple method to add new product to the list. Order contains an array of product and exposes simple method to accept a new product to the list. We can define operations in a separate classes and we can visit the order with that operation. Order will apply that operation to every product from the list. That way we don't have to expose internal representation of products and we don't have to extend Order or Product if we wan't to add new operation.


22. Template Method design pattern: Define the skeleton of an algorithm in an operation, deferring some steps to subclasses.

Template Method pattern to the #add_engine step. It is to be defined in derivatives (subclasses) of the CarBuilder class.

