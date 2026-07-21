# Mohammad-Abu-ALhaija-BinX-Backend-Internship

# BinX Tech — Backend Development Internship (.NET)

## 📅 Week 1 — Day 1: Program Orientation & .NET Development Environment Setup

### Overview
The internship started on Day 1 with its Phase 1 (Onboarding & Foundations). The emphasis was on gaining an overview of the program and establishing a working, professional .NET development environment before writing any code or using a web framework.

### What I Learned
- **Program Orientation**: Covered the four phases of the program, the weekly schedule, the mentor check-in schedule, and an example of a successful Phase 3 capstone project.
- **.NET SDK Installation**: Installed the current .NET LTS SDK, which includes the runtime, compiler, and the `dotnet` CLI. Tested with:
  ```bash
  dotnet --version
  dotnet --list-sdks
  ```
- **The `dotnet` CLI**: Learned the basic commands used throughout the program:
  - `dotnet new console` — scaffold a new console application
  - `dotnet run` — build and run the project in one step
  - `dotnet build` — compile without executing
- **IDE Setup**: Installed and configured Visual Studio Code (using the C# Dev Kit extension), enabling IntelliSense and the debugger — both essential for the coming weeks.

### Hands-On Lab
1. Installed the .NET LTS SDK and confirmed it with `dotnet --version`.
2. Configured the IDE with debugging enabled.
3. Created a new console app:
   ```bash
   dotnet new console -o HelloBinX
   dotnet run
   ```
4. Modified the program to print my name and today's date, then rebuilt and reran it.
5. Created this GitHub repository to track the internship's progress.

### Tools Used
`.NET SDK` • `Visual Studio Code (C# Dev Kit)` • `Terminal` • `GitHub`

### Resources
- [Environment Setup Video](https://www.youtube.com/watch?v=ZVGutgqBMUM)

### Status
✅ .NET SDK installed and verified
✅ IDE configured with debugging
✅ First console app ("Hello World") built and run successfully
✅ GitHub repository created

# Day 2 — C# Fundamentals I: Types, Variables & Control Flow

## Overview
Day 2 of Week 1 (BinX Tech Backend .NET Internship) focused on C# fundamentals: value types vs. reference types, variable declaration and type inference, control flow (switch expressions), and nullable reference types. Below is a summary of the hands-on lab tasks completed, with the corresponding code.

## Tasks Completed

- [x] Declared at least 3 value-type and 3 reference-type variables, printing each one's type using `GetType()`
- [x] Demonstrated value-vs-reference copy behavior, printing state before and after mutation
- [x] Implemented a grade-classifier method using a `switch` expression covering multiple score ranges
- [x] Read user input and handled a possibly-null value safely with nullable reference types enabled
- [x] Committed the day's work to GitHub with a clear commit message

## 1. Value Types vs. Reference Types

Declared value types (`int`, `double`, `bool`) and reference types (`string`, array, `List<string>`), and printed each one's runtime type using `GetType()`.

```csharp
int age = 22;
string MyName = "Mohammad";
Console.WriteLine($"age type: {age.GetType()}");
Console.WriteLine($"MyName type: {MyName.GetType()}");
```

## 2. Copy Behavior (Value vs. Reference)

Demonstrated the core distinction between the two:
- Copying an `int` (value type) creates an independent copy — changing `y` does not affect `x`.
- Copying a `List<string>` (reference type) copies the reference — changing `list2` also changes `list1`, since both point to the same object in memory.

```csharp
int x = 10;
int y = x;
y = 20; // x is still 10

List<string> list1 = new List<string> { "Apple", "Banana" };
List<string> list2 = list1;
list2[0] = "Orange"; // list1[0] is "Orange" too
```

## 3. Grade Classification (Switch Expression)

Used a `switch` expression with range patterns to map a numeric score to a letter grade (A–F), with `_` as the default/fallback case.

```csharp
string grade = score switch
{
    >= 90 => "A",
    >= 80 => "B",
    _ => "F"
};
```

## 4. Nullable Reference Types

Read console input into a `string? name` variable and used an `if (name is not null)` check to safely handle the case where no input was provided, avoiding a possible null-reference exception at compile time.

```csharp
string? name = Console.ReadLine();
if (name is not null)
{
    Console.WriteLine($"Hello, {name}!");
}
```

## Tools Used
.NET SDK • VS Code / Visual Studio • Git
