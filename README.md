# TypeScript Assignment

This repository contains my TypeScript coding solutions and two short blog posts about core TypeScript concepts.

## Overview

The assignment has two parts:

1. **Coding solutions:** Functions, generics, interfaces, classes, and an async function, all written with explicit parameter and return types and no use of `any`.
2. **Blog posts:** Two beginner-friendly blogs, each with a title, introduction, body with code examples, and conclusion.

## Blog Posts
Blog: 5 (https://drive.google.com/file/d/1CzGQIxgTgYQ76fHiEb52FjllAheqn8Eb/view?usp=sharing)
- [Who Gets the Keys? A Beginner's Guide to Access Modifiers in TypeScript](./access-modifiers.md): explains `public`, `private`, `protected`, and `readonly` with a simple home analogy.
Blog: 7 (https://drive.google.com/file/d/1ya9vi7WW7V1fB23SfWCC-6D9_YA_4j3K/view?usp=sharing)
- [Tea OR Coffee, Burger AND Fries: Union and Intersection Types in TypeScript](./union-intersection-types.md): shows how `|` and `&` work together in one type.

## Coding Solutions

All solutions are in [`solutions.ts`](./solutions.ts):

| Name | What it covers |
|------|----------------|
| `multiplyValue` | Optional parameters |
| `processInput` | Union types and `typeof` narrowing |
| `formatCoordinate` | Readonly tuples and destructuring |
| `concatenateArrays` | Generics with rest parameters |
| `Course`, `getPopularCourses` | Interfaces and array filtering |
| `pluckValues` | Generics with `keyof` |
| `Employee`, `Manager`, `getDetails`, `getRoleInfo` | Classes, inheritance, and access modifiers |
| `validateAgeAsync` | `Promise<T>` and async code |

## File Structure

```
├── solutions.ts
├── access-modifiers.md
├── union-intersection-types.md
└── README.md
```
