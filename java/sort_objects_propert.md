## Sort Objects by Property

**Question:** Create a function that sorts an array of objects based on a specified property of the objects.

**Solution:**
```java
import java.util.Arrays;
import java.util.Comparator;

public class SortByProperty {
    public static void main(String[] args) {
        Person[] people = {
            new Person("Alice", 30),
            new Person("Bob", 25),
            new Person("Charlie", 35)
        };

        // Sort by age
        Arrays.sort(people, Comparator.comparingInt(Person::getAge));

        // Print sorted array
        for (Person person : people) {
            System.out.println(person);
        }
    }
}

class Person {
    private String name;
    private int age;

    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    public int getAge() {
        return age;
    }

    public String getName() {
        return name;
    }

    @Override
    public String toString() {
        return "{ name: '" + name + "', age: " + age + " }";
    }
}
