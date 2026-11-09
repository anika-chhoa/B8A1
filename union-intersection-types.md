# Tea OR Coffee, Burger AND Fries: Union and Intersection Types in TypeScript

## Introduction

When you order food, you sometimes say "tea or coffee" and sometimes say "burger and fries". TypeScript lets you do the same with types. The `|` symbol means "this or that", and the `&` symbol means "this and that". The real fun starts when you use both in one type.

## Body

```ts
type Student = { name: string; studentId: number };
type Teacher = { name: string; subject: string };
type Contact = { email: string };

type ContactablePerson = (Student | Teacher) & Contact;

function introduce(person: ContactablePerson): string {
  if ("subject" in person) {
    return `${person.name} teaches ${person.subject}. Email: ${person.email}`;
  }
  return `${person.name} has ID ${person.studentId}. Email: ${person.email}`;
}

const student: ContactablePerson = { name: "Rahim", studentId: 101, email: "rahim@school.com" };
const teacher: ContactablePerson = { name: "Mitu", subject: "Math", email: "mitu@school.com" };
```

Let's read `(Student | Teacher) & Contact` slowly. The part inside the brackets is a union, so a person is either a student or a teacher. The `& Contact` part is an intersection, so every person must also have an email.

That means `student` needs `name`, `studentId`, and `email`. In the same way, `teacher` needs `name`, `subject`, and `email`. If any required property is missing, TypeScript shows an error immediately.

Inside `introduce`, TypeScript only trusts the shared properties, like `name` and `email`. So we check `"subject" in person` first. After that check, it knows exactly which shape we are holding.

## Conclusion

Use `|` when a value can be one of several shapes. Use `&` when you want to add extra requirements to those shapes. Combine them, and you get flexible types that are still strict where it matters.
