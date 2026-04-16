# 🐾 WildLife Tracker

A lightweight JavaScript utility library for tracking and managing wildlife animal profiles. Built with simple, functional JavaScript — no dependencies required.

---

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Animal Schema](#animal-schema)
- [Functions](#functions)
- [Usage](#usage)
- [Example Output](#example-output)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)

---

## Overview

**WildLife Tracker** is a beginner-friendly JavaScript module that lets you create, read, update, and manage animal data objects. It's ideal for conservation databases, educational tools, or wildlife monitoring apps.

---

## ✨ Features

- 🔍 Retrieve animal species and age
- 🏕️ Add habitat information dynamically
- ✏️ Update animal age records
- ❌ Remove conservation status flags
- ✅ Check for optional property presence
- 🔑 Access any property via dynamic lookup

---

## 🐘 Animal Schema

Each animal is represented as a plain JavaScript object:

```js
const animal = {
  species: "Tiger",       // string  — species name
  age: 5,                 // number  — age in years
  isEndangered: true,     // boolean — conservation status (optional)
  habitat: "Rainforest"   // string  — habitat type (optional)
};
```

---

## 🛠️ Functions

| Function | Parameters | Returns | Description |
|---|---|---|---|
| `getSpecies(animal)` | `animal` | `string` | Returns the species name |
| `getAge(animal)` | `animal` | `number` | Returns the animal's age |
| `addHabitat(animal, habitat)` | `animal`, `habitat: string` | `animal` | Adds a habitat field to the animal |
| `updateAge(animal, newAge)` | `animal`, `newAge: number` | `animal` | Updates the animal's age |
| `removeEndangeredStatus(animal)` | `animal` | `animal` | Deletes the `isEndangered` property |
| `hasHabitat(animal)` | `animal` | `boolean` | Checks if habitat property exists |
| `getProperty(animal, propertyName)` | `animal`, `propertyName: string` | `any` | Dynamically accesses any property |

---

## 🚀 Usage

```js
// Define animals
const tiger = { species: "Tiger", age: 5, isEndangered: true };
const elephant = { species: "Elephant", age: 10, isEndangered: true };

// Get species
getSpecies(tiger);              // "Tiger"

// Get age
getAge(tiger);                  // 5

// Add habitat
addHabitat(tiger, "Rainforest");
// { species: "Tiger", age: 5, isEndangered: true, habitat: "Rainforest" }

// Update age
updateAge(elephant, 12);
// { species: "Elephant", age: 12, isEndangered: true }

// Remove endangered status
removeEndangeredStatus(tiger);
// { species: "Tiger", age: 5, habitat: "Rainforest" }

// Check for habitat
hasHabitat(tiger);              // true
hasHabitat(elephant);           // false

// Dynamic property access
getProperty(tiger, "species");  // "Tiger"
getProperty(elephant, "age");   // 12
```

---

## 📤 Example Output

```
Tiger
5
{ species: 'Tiger', age: 5, isEndangered: true, habitat: 'Rainforest' }
{ species: 'Elephant', age: 12, isEndangered: true }
{ species: 'Tiger', age: 5, habitat: 'Rainforest' }
true
false
Tiger
12
```

---

## 📁 Project Structure

```
wildlife-tracker/
├── main.js        # Core tracker functions and animal definitions
└── README.md       # Project documentation
```

---

## 🤝 Contributing

Contributions are welcome! To get started:

1. Fork the repository
2. Create a new branch: `git checkout -b feature/your-feature-name`
3. Commit your changes: `git commit -m "Add your feature"`
4. Push to the branch: `git push origin feature/your-feature-name`
5. Open a Pull Request

---

> *"The wildlife and its habitat cannot speak, so we must and we will."* — Theodore Roosevelt
