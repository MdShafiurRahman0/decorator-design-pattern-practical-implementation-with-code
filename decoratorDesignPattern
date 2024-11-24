// Step 1: Component Interface
interface Pizza {
    String getDescription();
    double getCost();
}

// Step 2: Concrete Component
class PlainPizza implements Pizza {
    @Override
    public String getDescription() {
        return "Plain Pizza";
    }

    @Override
    public double getCost() {
        return 200.0; // Base price
    }
}

// Step 3: Decorator Abstract Class
abstract class PizzaDecorator implements Pizza {
    protected Pizza pizza; // Composition

    public PizzaDecorator(Pizza pizza) {
        this.pizza = pizza;
    }

    @Override
    public String getDescription() {
        return pizza.getDescription();
    }

    @Override
    public double getCost() {
        return pizza.getCost();
    }
}

// Step 4: Concrete Decorators
class CheeseDecorator extends PizzaDecorator {
    public CheeseDecorator(Pizza pizza) {
        super(pizza);
    }

    @Override
    public String getDescription() {
        return pizza.getDescription() + ", Cheese";
    }

    @Override
    public double getCost() {
        return pizza.getCost() + 50.0; // Adding cheese costs 50
    }
}

class OliveDecorator extends PizzaDecorator {
    public OliveDecorator(Pizza pizza) {
        super(pizza);
    }

    @Override
    public String getDescription() {
        return pizza.getDescription() + ", Olives";
    }

    @Override
    public double getCost() {
        return pizza.getCost() + 30.0; // Adding olives costs 30
    }
}

class PepperoniDecorator extends PizzaDecorator {
    public PepperoniDecorator(Pizza pizza) {
        super(pizza);
    }

    @Override
    public String getDescription() {
        return pizza.getDescription() + ", Pepperoni";
    }

    @Override
    public double getCost() {
        return pizza.getCost() + 70.0; // Adding pepperoni costs 70
    }
}

// Step 5: Client Code
public class DecoratorPatternPizzaExample {
    public static void main(String[] args) {
        // Basic pizza
        Pizza plainPizza = new PlainPizza();
        System.out.println(plainPizza.getDescription() + " | Cost: " + plainPizza.getCost());

        // Pizza with cheese
        Pizza cheesePizza = new CheeseDecorator(plainPizza);
        System.out.println(cheesePizza.getDescription() + " | Cost: " + cheesePizza.getCost());

        // Pizza with cheese and olives
        Pizza cheeseOlivePizza = new OliveDecorator(cheesePizza);
        System.out.println(cheeseOlivePizza.getDescription() + " | Cost: " + cheeseOlivePizza.getCost());

        // Pizza with cheese, olives, and pepperoni
        Pizza deluxePizza = new PepperoniDecorator(cheeseOlivePizza);
        System.out.println(deluxePizza.getDescription() + " | Cost: " + deluxePizza.getCost());
    }
}
