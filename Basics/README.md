
---

# **Ruby Basics**

This guide introduces fundamental and intermediate Ruby concepts through hands-on exercises. Topics range from basic syntax to complex problem-solving like creating Sudoku solvers and working with multidimensional arrays.

---

## **Index**

### **Day 1: Basics - Introduction to Ruby**
1. [`Abuelita_sordita.rb`](#abuelita_sordita)
2. [`Dale_estilo_al_codigo.rb`](#dale_estilo_al_codigo)
3. [`Diccionario.rb`](#diccionario)
4. [`Lee_el_error.rb`](#lee_el_error)
5. [`Utilizando_irb.rb`](#utilizando_irb)

---

### **Day 2: Enumerables and String Manipulations**
1. [`Los_enumerables_cobran_vida.rb`](#los_enumerables_cobran_vida)
2. [`Metodos_destructivos.rb`](#metodos_destructivos)
3. [`Pig_latin.rb`](#pig_latin)

---

### **Day 3: Algorithms and Iteration**
1. [`Algoritmo_linear_search.rb`](#algoritmo_linear_search)
2. [`Factorial.rb`](#factorial)

---

### **Day 4: Multidimensional Arrays and Grid Challenges**
1. [`Ajedrez.rb`](#ajedrez)
2. [`Tabla_de_datos.rb`](#tabla_de_datos)
3. [`Nested_arrays_2.rb`](#nested_arrays_2)
4. [`Sopa_de_letras.rb`](#sopa_de_letras)

---

### **Day 5: Sudoku Solver**
1. **Input and Grid Representation**
2. **Extracting Boxes**
3. **Finding Missing Digits**
4. **Identifying Empty Positions**
5. **Validating Missing Numbers**
6. **General Board Analysis**

---

---

## **Day 1: Basics - Introduction to Ruby**

### **`Abuelita_sordita.rb`**
- **Objective**: Practice conditionals and loops.
- **Description**: Simulate a conversation with a "deaf grandma" where her responses depend on your input:
  - Shouting (`all uppercase`) → "NO, NO DESDE 1983."
  - Normal speaking → "HUH?! NO TE ESCUCHO, HIJO!"
  - Say `"BYE TQM"` three times to exit.
- **Key Concepts**:
  - Loops (`loop do`), conditionals (`if`, `elsif`), and string methods (`upcase`).

---

### **`Dale_estilo_al_codigo.rb`**
- **Objective**: Learn to define and use classes, constants, and methods.
- **Description**: Create a `Person` class with attributes like `name` and `age`. Add methods to:
  - Determine "life stage" (child, teenager, adult, elder).
  - Check legal age.
- **Key Concepts**:
  - Classes, constants, and attribute readers (`attr_reader`).

---

### **`Diccionario.rb`**
- **Objective**: Work with nested arrays and loops.
- **Description**: Extract names of students with perfect grades from nested data.
- **Key Concepts**:
  - Nested arrays, loops, and array methods like `push`.

---

### **`Lee_el_error.rb`**
- **Objective**: Debug and validate a prewritten class.
- **Description**: Fix a `Person` class to ensure correct results for methods like `life_stage`.
- **Key Concepts**:
  - Debugging classes and writing test cases.

---

### **`Utilizando_irb.rb`**
- **Objective**: Experiment with Ruby in IRB.
- **Description**: Use IRB for quick coding experiments like defining methods, assigning variables, and handling errors.
- **Key Concepts**:
  - Syntax experimentation in an interactive environment.

---

---

## **Day 2: Enumerables and String Manipulations**

### **`Los_enumerables_cobran_vida.rb`**
- **Objective**: Use Ruby's `Enumerable` module to manipulate arrays.
- **Key Methods**:
  - `each_with_index`, `select`, `find`, `map`, and `reduce`.

---

### **`Metodos_destructivos.rb`**
- **Objective**: Differentiate between destructive and non-destructive methods.
- **Example**:
  ```ruby
  city = "afganistan"
  puts city.delete("a")    # Non-destructive
  puts city.delete!("a")   # Destructive
  ```

---

### **`Pig_latin.rb`**
- **Objective**: Create a Pig Latin translator.
- **Key Concepts**:
  - String manipulation and helper methods for modularity.

---

---

## **Day 3: Algorithms and Iteration**

### **`Algoritmo_linear_search.rb`**
- **Objective**: Implement single and global linear searches to find elements in arrays.

---

### **`Factorial.rb`**
- **Objective**: Calculate factorials using iterative and functional approaches.

---

---

## **Day 4: Multidimensional Arrays and Grid Challenges**

### **`Ajedrez.rb`**
- **Objective**: Generate a chessboard representation using Unicode symbols.

---

### **`Tabla_de_datos.rb`**
- **Objective**: Access and transform 2D arrays into readable formats like hashes.

---

### **`Nested_arrays_2.rb`**
- **Objective**: Validate Tic-tac-toe grids and convert tables into hashes.

---

### **`Sopa_de_letras.rb`**
- **Objective**: Build a word search solver capable of finding words in multiple directions.

---

## **Day 5: Sudoku Solver**

### **1. Input and Grid Representation**
- **Description**: Convert a 1D string of 81 digits into a 2D array representing the Sudoku board.

### **2. Extracting Boxes**
- **Description**: Extract and analyze the top-left 3x3 box (`box_1`) to identify its contents.

### **3. Finding Missing Digits**
- **Description**: Determine which numbers (1-9) are absent from a specific 3x3 box.

### **4. Identifying Empty Positions**
- **Description**: Locate positions of empty cells (zeros) in a grid.

### **5. Validating Missing Numbers**
- **Description**: Check if missing numbers can fit into empty positions according to Sudoku rules.

### **6. General Board Analysis**
- **Description**: Analyze the entire board to prepare for implementing a full Sudoku solver.

---

### **Key Learning Objectives for Day 5**
- Manipulate 2D arrays and nested structures.
- Implement logical validations for rows, columns, and boxes.
- Lay the foundation for advanced Sudoku-solving algorithms, including recursion and backtracking.

---

## **What’s Next?**
1. **Solve the Sudoku puzzle**: Extend the program to complete the board using recursion.
2. **Optimize logic**: Add efficient validation for constraints in rows, columns, and boxes.
3. **Visualize progress**: Create a graphical representation of the Sudoku board.

---
