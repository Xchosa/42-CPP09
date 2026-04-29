C++ - Module 09: Standard Template Library (STL)

📌 Project Overview

This module is the final step in the 42 C++ journey, focusing on the effective use of **STL Containers** and  **Algorithms** . The primary challenge is not just solving the problems, but selecting the most appropriate container for each specific task while complying with the strict constraint: **Once a container is used, it cannot be used again in subsequent exercises.**

🛠️ General Rules

* **Language Standard:** **C++98.**
* **Compilation:** `c++ -Wall -Wextra -Werror -std=c++98`.
* **Design:** **All classes must follow the**  **Orthodox Canonical Form** **.**
* **STL Restriction:** **Containers and algorithms are strictly limited to Modules 08 and 09.**

---

🚀 Exercises

(Ex00) Bitcoin Exchange

**Program Name:** `btc`

* **Goal:** **Calculate the value of a specific amount of Bitcoin on a given date using a CSV database.**
* **Logic:** **If a specific date is not found in the database, the program must use the closest** **lower** **date.**
* **Input Format:** `date | value` **(e.g.,** `2011-01-03 | 3`).
* **Constraint:** **Use at least one STL container.**

(Ex01) Reverse Polish Notation (RPN)

**Program Name:** `RPN`

* **Goal:** **Evaluate a mathematical expression provided in Reverse Polish Notation.**
* **Logic:** **Handles operations:** `+`, `-`, `/`, `*`. All numbers passed as initial arguments are less than 10.
* **Constraint:** **Use an STL container**  **not used in Ex00** **.**

(Ex02) PmergeMe

**Program Name:** `PmergeMe`

* **Goal:** **Implement the** **Ford-Johnson algorithm** **(merge-insert sort) to sort a sequence of positive integers.**
* **Logic:** **Compare the performance of the algorithm using two different containers.**
* **Constraint:** **Use at least two different STL containers**  **not used in Ex00 or Ex01** **.**
* **Output:** **Must display the time taken for each container with high precision.**

---

📋 Summary of Container Usage

| Exercise       | Container(s) Used                | Why?                                                                                       |
| -------------- | -------------------------------- | ------------------------------------------------------------------------------------------ |
| **Ex00** | `std::map`                     | Efficient for key-value (date-price) storage and finding closest lower bounds.             |
| **Ex01** | `std::stack`                   | Ideal for the LIFO nature of RPN calculations.                                             |
| **Ex02** | `std::vector` & `std::deque` | To compare contiguous vs. non-contiguous memory performance in the Ford-Johnson algorithm. |

> (!IMPORTANT)
> Change the containers in the table above to match your actual implementation!

---

💻 Usage

Each directory (`ex00/`, `ex01/`, `ex02/`) contains its own `Makefile`.

bash

```
# Example for Ex00
cd ex00
make
./btc input.txt
```
