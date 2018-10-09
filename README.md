
# Design Patterns

  

1. ### Abstract_factory
 ### Abstract_factory
 The following steps are required in building a Jungle
		

    a. Number of animals
    b. Jungle Organism Factory

  the above processes can easily be accomplished via
`jungle = Habitat.new(JungleOrganismFactory.new, number_of_animals: 2)`

which gives the output:

    Tiger Animal0 eats meat
    Roar
    Tiger Animal1 eats meat
    Roar

2. ### Singleton design pattern: 
This Configuration class shows the creation of the same configuration twice in line with the Singleton method. It does not get instantiated


4. ### Factory method 
 The following steps are required in building a shape

a. The shape to be built

b. The dimensions of shape to be built

c. Calling the draw method

This can easily be accomplished by

    triangle = ShapeFactory.build(:triangle, 2, 3, 4)
    
    triangle .draw

  

4. ### Bridge design pattern
The following is required in getting a shape to be drawn on a system

    a. The name of shape
    
    b. The name of system

this can easily be accomplished by `Rectangle.new(MacOs.new)`

So the rectangle#draw shows up 'drawing a rectangle upon a Mac'

  

6. ### Command design pattern
 The following is required to adding an UIButton to add an item to a cart

		a. The Item

		b. The cart

this can easily be accomplished by running

    item = Item.new("Book") 
    cart = cart.get_current_cart
    command = AddItemToCartCommand.new(item, cart)
    button = UIButton.new(command)
    button.press_button

 
7. ### Composite 
The following steps are required for showing that objects and compositions of objects are treated uniformly

    a. add_sub_task(AddDryIngredientsTask.new)
    
    b. add_sub_task(MakeBatterTask.new)

One can see that they both have initialize methods to store the name of the task and get_time_required to store the time left for the task to be completed.

8. #### Decorator method : 
†he following steps are required for getting the price of different types of coffee

a. the type of coffee

this can easily be accomplished by running `CoffeeWithSugar.new(Coffee.new)` to get the price

9. ### Facade  
 This is the following steps required to run the SubSytemClass#{number} class

a. call a new instance of FacadeSystem class as in `facade = FacadeSystem.new`
 call facade. method_1 or facade. method_2

  
10. #### Flyweight design pattern:
These are the steps required to run FlyweightFactory



    a. call the flyweightFActory Class as in flyweight_factory = FlyweightFactory.new
    b. call flyweight_factory.get_flyweight("flyweight1") to see what get returned
    c. flyweight1.operation(10) to see the return

  

11. ### Interpreter
These are the steps required for the finding of an expression in the group of letters entered.

a. Context.new("AAABBBCCCDDD")

b. The steps required for getting TernimalExpression and NonTerminalExpression from AbstractExpression in the array zit it fetching from.

  

12. ### Chain of responsibility 
For this  we have a QuestionhHandler. The following steps are required in answering questions

a. Call the the chain _of_responsibility.process request with the asked question inside

This can be answered by running `chain_of_responsibility.process_request("Who is Harry Potter's best friend?")` to give `Answering a Harry Potter related question`

  

13. #### Iterator 
This is the following steps required to call and create new Portfolio elements
 
    a. create a new portfolio: Portfolio.new
    
    b. create a new Portfolio element: my_portfolio.add_account(Account.new('Stocks', 100))

and the result can be gained by

    my_portfolio.each { |account| puts "#{account.name}: #{account.balance}" }

to get the elements added

  

14. ### Mediator
These are the following steps required to find a word

    a. Submit a array of words
    
    b. Submit a Mediator with the value of the searched text_field

This can easily be solved by running

    list = List.new(["apple", "avocado", "banana", "kiwi", "mango", "watermelon"])
    
    text_field = TextFieldWithObserver.new
    
    mediator = ListSearchMediator.new(text_field, list)
    
    text_field.value = "av"
    
    puts list.words.inspect

Which will give ['avocado']

  

15. ### Memento design pattern
Theses are the following steps need to store something in the memento class

    a. Crate an originator
    
    b. Create a state for saving it to memento
    
    c. Create a state for restoring from memento

This can be acheived by running

    caretaker = Caretaker.new
    
    originator = Originator.new
    
    originator.state = "name:foo"
    
    memento = originator.save_to_memento
    
    caretaker.memento = memento
    
    originator.state = "name:bar"
    
    originator.restore_from_memento(caretaker.memento)

  

16. ### Observer design pattern
 The are the steps required to edit an observer

    a. Create an observer
    
    b. Change the observer
    
    c. Notify about the change in observers

This can be achieved by running the following

    observer_a = Observer.new
    
    observer_b = Observer.new
    
    subject = Subject.new
    
    subject.name = "Anakin Skywalker"
    
    subject.add_observer(observer_a)
    
    subject.add_observer(observer_b)
    
    subject.name = "Obi Wan Kenobi"
    
    subject.notify_observers

  
17. ### Proxy 
This provide a way for a protected account to be created unlike An ordinary aacount.

    proxy = AccountProtectionProxy.new(account, 'bamroc')
    
    proxy.deposit(20)
    
    proxy.withdraw(40)
    
    puts proxy.balance

This is the AccountProtection Proxy class which is used to protect Account class.

19. ### State design pattern
These are the the requirements for changing the internal state of ConcreteStateA which runs

	    state = ConcreteStateA.new
        
        context = Context.new(state)
        
        context.request
        
        context.request

  

20. ### Strategy design pattern
Here are the steps to install an engine on a car

    a. Declare the car
    
    b. Declare the engine type on the car

this can be easily run off

    car_a = Car.new(StraightSixEngine.new)
    
    car_b = Car.new(V8Engine.new)
    
    car_a.start
    
    car_a.stop
    
    car_b.start

  
21. ### Visitor design pattern
For this we have an Order and product. These are the steps to print a receipt from the Order.

    p1 = Product.new(name: 'Laptop', price: 1000)
    
    p2 = Product.new(name: 'Beer', price: 5)
    
    order = Order.new
    
    order.add_product(p1)
    
    order.add_product(p2)
    
    order.accept(ProductsPrinterVisitor.new)
    
    order.accept(HalfPriceSimulatorVisitor.new)

  
22. ### Template Method design pattern
For this we have a car builder. These steps to required to build a car include

a. `declare the car builder: car = OmegaCarBuilder.new`

b. the steps required to start the engine of the car can be done by

    car.add_engine
    
    car.start_engine

  

23. ### Adaptor design pattern
For this, we had a GuitarBuilder class which helps reduce the complexity involved in building a guitar. The following are the steps required in building a guitar:

a. Add a string

b. Craft the guitar body

c. Paint the guitar body

The following processes can easily be accomplished via:

    - guitar_builder = GuitarBuilder.new
    
    - guitar_builder.add_strings(6)
    
    - guitar_builder.craft_body
    
    - guitar_builder.paint_body


