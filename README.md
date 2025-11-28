## Multi-Counter App with LazyColumn

Yetunde Abdulazeez-Ado
Mobile Technology and Programming  

## 1. Introduction

This assignment required the development of an Android application using **Jetpack Compose** that displays a scrollable list of counters. Each counter should be independently adjustable with increment and decrement buttons. The counters are labeled sequentially as `Counter_#`. An optional enhancement was to allow users to dynamically add or remove counter items during runtime. The goal was to practice state management, UI composition, and dynamic list handling in Compose.

## 2. Implementation

### 2.1 Project Setup

- **Package name:** `com.example.counter`  
- **Main activity:** `MainActivity.kt`  
- **UI framework:** Jetpack Compose  
- **State management:** `mutableStateListOf` for dynamic counter values  

### 2.2 Counter List with LazyColumn

- A `LazyColumn` was used to display a scrollable list of counter items.
- Each item in the list was rendered using a custom composable `CounterItem`.
- The list was initialized with five counters using:
  ```kotlin
  val counters = remember { mutableStateListOf(0, 0, 0, 0, 0) }

### 2.3 Independent Counter Control

- Each counter was passed its current value and two lambda functions:
  - `onIncrease` → increments the counter.
  - `onDecrease` → decrements the counter.
- These functions directly modify the corresponding index in the `counters` list.

### 2.4 CounterItem Composable

- Displays the current counter value.
- Includes two buttons:
  - **Increase** → pink background (`Color(0xFFFF4081)`), white text.
  - **Decrease** → same styling.
- Layout uses `Column` and `Row` with spacing and alignment for clean UI.

### 2.5 Optional Feature: Add/Remove Counters

> *Note: This feature was not implemented in the submitted version but is planned for future enhancement.*

To support dynamic counter management:
- Add button → `counters.add(0)`
- Remove button → `counters.removeLast()`

This would allow users to customize the number of counters during runtime.

## 3. Results

The application successfully:
- Displays a scrollable list of counters using `LazyColumn`.
- Allows each counter to be incremented or decremented independently.
- Uses clean UI layout with consistent styling.
- Demonstrates effective use of Compose state and recomposition.

## 4. Discussion

This exercise reinforced key concepts in **Jetpack Compose**:
- **State management** with `remember` and `mutableStateListOf`.
- **Composable architecture** for reusable UI components.
- **LazyColumn** for efficient rendering of scrollable lists.
- **Dynamic UI updates** based on user interaction.



