Enchanting Kata
============================

_created by [Giulio Perrone](https://github.com/pepperrone)_

## Story

Durance has found a magic book in one of his adventures and decided to learn how to enchant his weapons. Due to the unstable nature of magic, he is not sure of what kind of magical things will happen, he might even lose previous enchantments! (That happens every 1/10th of the time) Let’s try to help him.

### Description
Create an application that allows Durance to enchant his weapon.

For this version of the kata, only one enchantment is allowed. We might re-roll an existing enchantment but there is a 1/10 that we might lose all current enchantments on the weapon.

Example:

    Dagger of the Nooblet
     5 - 10 attack damage
     1.2 attack speed
After enchanting it, Durance rolled the Fire enchantment!

    Inferno Dagger of the Nooblet
     5 - 10 attack damage
     1.2 attack speed
     +5 fire damage
Not satisfied, he enchanted it again and this time he got the Agility enchantment!

    Quick Dagger of the Nooblet
     5 - 10 attack damage
     1.2 attack speed
     +5 agility
He felt confident thinking that he could get something better and tried again, sadly, he lost his enchantment!

    Dagger of the Nooblet
     5 - 10 attack damage
     1.2 attack speed
### Rules

- Only 1 enchantment should be "active" at a time
- For the simple version, the enchantment attributes have no effect on the base stats of the weapon, they are considered as extra stats
- Enchanted weapons have the prefix of the enchantment on them
- Enchantment selection should be randomized
- We can’t roll an enchantment we already have, they are always different
- 1/10 probability of losing the enchantment

### Enchantments

An enchantment adds different attributes to a weapon, for this kata, we can choose among the following:
```
{
  "ice": {
    "prefix": "Icy",
    "attribute": "+5 ice damage"
  },
  "fire": {
    "prefix": "Inferno",
    "attribute": "+5 fire damage"
  },
  "lifesteal": {
    "prefix": "Vampire",
    "attribute": "+5 lifesteal"
  },
  "agility": {
    "prefix": "Quick",
    "attribute": "+5 agility"
  },
  "strength": {
    "prefix": "Angry",
    "attribute": "+5 strength"
  }
}
```

### Starting point (Optional)

    public class Durance{
      Weapon weapon;
      MagicBook magicBook;

      public void enchant(){
    // Implement here...
      }

      public String describeWeapon(){
    // Implement here...
      }
    }

    public interface Weapon{
      String stats();
    }

## Harder version
Durance can now carry more weapons and each one can have up to 3 unique enchantments, he is also worried about dealing the most damage possible, so DPS (Damage per second) should be displayed as well.

### DPS
We take the agility attribute into account, converting it to an attack speed increase equal to: `attack speed + agility points / 10`

DPS is calculated as: `((Min Weapon Damage + Max Weapon Damage) / 2) / Weapon Speed`

### Rules
- Previous rules apply
- In case of a losing enchantment roll, only the last enchantment should be removed
