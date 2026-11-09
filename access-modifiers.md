# Who Gets the Keys? A Beginner's Guide to Access Modifiers in TypeScript

## Introduction

Imagine your home. Guests can sit in the living room, only family can enter the store room, and only you can open your personal diary. Classes in TypeScript work the same way. Access modifiers decide who can see or change the data inside a class. There are four: `public`, `private`, `protected`, and `readonly`.

## Meet the Four Rules

```ts
class Employee {
  readonly id: number;
  public name: string;
  private baseSalary: number;
  protected department: string;

  constructor(id: number, name: string, baseSalary: number, department: string) {
    this.id = id;
    this.name = name;
    this.baseSalary = baseSalary;
    this.department = department;
  }
}

class Manager extends Employee {
  getDepartment(): string {
    return this.department; 
  }
}
```

- **public** is the living room. Anyone can access it, and it is the default. Anyone can read `employee.name`.
- **private** is your diary. Only the class itself can touch `baseSalary`. Even `Manager` gets an error if it tries.
- **protected** is the family room. The class and its child classes can enter, but outsiders cannot. That is why `Manager` can read `department`.
- **readonly** is a name carved in stone. You set `id` once in the constructor, and any later change gives an error.

A small tip: these rules are checked while you write code, not when the program runs. TypeScript simply warns you early, like a friendly teammate.

## Conclusion

Start with `private` by default, open things up only when needed, and use `readonly` for values that should never change. Your classes will be safer, cleaner, and much easier to understand.

Good code is not about hiding everything, it is about sharing the right things with the right people. Once you learn to hand out the keys wisely, your code will feel as calm and organized as a well-kept home.
