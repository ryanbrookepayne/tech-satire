# 👪 Parental Control Predicates

Control your children with these simple and strict Java predicates.

> Does your life feel like a bumpy roller coaster ride? Are your children doing whatever they please with no regard for decency?

Take control with **Parental Control Predicates**: _The programmatic way to control your family._

## Video Games and Movies

Determines whether or not your child can play video games or watch TV.

> Has he/she read a book for at least thirty minutes today?

```java
package time.management;

import java.util.function.Predicate;

public class ChildCanPlayVideoGamesOrWatchMoviesPredicate implements Predicate<int> {

	@Override
	public boolean test(int minutesSpentReadingToday) {
		return minutesSpentReadingToday >= 30;
	}
}
```

## Candy and Sweets

Determines whether or not your child can eat a sweet treat.

> Has he/she eaten a sweet already today?

```java
package diet.nutrition;

import java.util.function.Predicate;

public class ChildCanHavePieceOfCandyOrDonut implements Predicate<int> {

	@Override
	public boolean test(int sweetsEatenToday) {
		return sweetsEatenToday < 0;
	}
}
```
