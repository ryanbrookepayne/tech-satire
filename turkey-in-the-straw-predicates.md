# 🦃 Turkey in the Straw Predicates

Filter your [straw for turkeys](https://youtu.be/VsnZxfkkoKQ) with Java Predicates.

## Animal Representations

### Animal Interface

```java
public interface Animal {
}
```

### Turkey, Cow, and Pig Implementations

```java
public class Turkey implements Animal {
}
```

```java
public class Cow implements Animal {
}
```

```java
public class Pig implements Animal {
}
```

## Adding Animals to the Straw

```java
Animal Herb = new Turkey();
Animal Ned = new Turkey();
Animal Ferdinand = new Cow();
Animal Johnson = new Pig();

List<Animal> animalsInTheStraw = new ArrayList<>();
animalsInTheStraw.add(Herb);
animalsInTheStraw.add(Ned);
animalsInTheStraw.add(Ferdinand);
animalsInTheStraw.add(Johnson);
```

## isTurkey Predicate

We'll use the following predicate to filter the straw for turkeys.

```java
Predicate<Animal> isTurkey = animal -> animal instanceof Turkey;
```

## Counting the Turkeys

```java
long turkeysInTheStraw = animalsInTheStraw.stream()
    .filter(isTurkey)
    .count();

if (turkeysInStraw < 1) {
    // Your straw is devoid of turkeys. Consider an alterative career to farming.
} else if (turkeysInStraw == 1)
    // Hooray! You have one turkey in the straw. But don't get ahead of yourself.
    // Turkeys can die of loneliness. Continue adding turkeys to your straw.
} else if (turkeysInStraw > 1 || turkeysInStraw <= 100) {
    // Congratulations! You've have the optimal amount of turkeys in your straw.
} else {
    // WARNING! You have too many turkeys in the straw. You have violated your
    // “free range organic” certification agreement. Eat some turkeys to free up space.
}
```

## Determining the Purity of the Straw

```java
boolean onlyTurkeysInStraw = animalsInTheStraw.stream().allMatch(isTurkey);

if (!onlyTurkeysInTheStraw) {
    // The straw has been polluted with non-turkeys. Remove the turkeys from the straw,
    // burn the barn down, and start over.
}

// Watch the turkeys gleefully hop and dance in the straw.
```

## Bonus: isThanksgiving Predicate

Add a `fearOfBeingEaten` field.

```java
public interface Animal {
    private String fearOfBeingEaten;

    public String getFearOfBeingEaten() {
        return fearOfBeingEaten;
    }

    public void setFearOfBeingEaten(String fearOfBeingEaten) {
        this.fearOfBeingEaten = fearOfBeingEaten;
    }
}
```

Test the field.

```java
Predicate<Animal> isThanksgiving = animal -> "Extremely High".equals(animal.getFearOfBeingEaten());
```
