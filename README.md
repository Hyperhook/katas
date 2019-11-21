# Story

Durance has found a magic book in one of his adventures and decided to learn how to enchant his weapons. Due to the unstable nature of magic, he is not sure of what kind of magical things will happen, he might even lose previous enchantments! (That happens every 1/10th of the time) Let’s try to help him.


# Description
Create an application that allows Durance to enchant his weapons.

For this version of the kata, only one enchantment is allowed. We might re-roll an existing enchantment but there is a 1/10 that we might lose all current enchantments on the weapon.

Example:

```
Dagger of Durance
 5 attack
 1.0 attack speed
 
 “He has no idea on how to use it”
```
After enchanting it, we rolled the Fire enchantment!

```
Inferno Dagger of Durance
 5 attack
 1.0 attack speed
 +5 fire damage
	
 “He has no idea on how to use it”
```

# Rules

- Only 1 enchantment should be "active" at a time
- Enchanted weapons have the prefix of the enchantment on them
- Enchantment selection should be randomized
- We can’t re-roll into an existing enchantment
- 1/10 probability of losing the enchantment

# Enchantments

An enchantment adds different attributes to a weapon, for this kata, we can choose among the following:

| Enchantment | Prefix   | Attributes         |
|-------------|----------|--------------------|
| Ice         | Icy      | +5 ice damage      |
| Fire        | Inferno  | +5 fire damage     |
| Lifesteal   | Vampire  | +5 lifesteal       |
| Agility     | Quick    | + 0.5 attack speed |
| Strength    | Angry    | +5 strength        |

# Starting point

```
public class Durance{
  Weapon weapon;
  MagicBook magicBook;
  
  public void enchant(){}
}

public class MagicBook{
  List<Enchant> enchants;

  public void randomEnchant(){}
}

public interface Weapon{
  String name;
  int attackPower;
  float attackSpeed;
  String description;
}
```
