---
Title: '.insert()'
Description: 'Inserts an element at a specified position in the deque.'
Subjects:
  - 'Computer Science'
  - 'Game Development'
Tags:
  - 'Containers'
  - 'OOP'
  - 'Classes'
  - 'Deques'
CatalogContent:
  - 'learn-c-plus-plus'
  - 'paths/computer-science'
---

The **`.insert()`** method inserts an element at a specified position in the `deque`.

## Syntax

The `.insert()` method is called on a `deque` using the following syntax:

```pseudo
dequeName.insert(position, value);
```

- `position`: An iterator pointing to the **location** where the new element should be inserted.
- `value`: The element to be added to the deque. It can be of any [data type](https://www.codecademy.com/resources/docs/cpp/data-types) that the `dequeName` holds.

## Example

The example below showcases the use of the `.insert()` method:

```cpp
#include <iostream>
#include <deque>

int main() {
    // Create a deque of integers
    std::deque<int> numbers;

    // Use insert() to add elements to the deque
    numbers.push_back(10);
    numbers.push_back(30);
    numbers.insert(numbers.begin() + 1, 20); // Insert 20 at index 1

    // Display the elements of the deque
    std::cout << "Deque contents: ";
    for (int num : numbers) {
        std::cout << num << " ";
    }
    std::cout << std::endl;

    return 0;
}
```

The above code generates the following output:

```shell
Deque contents: 10 20 30
```

## Codebyte Example

The following codebyte inserts several values into `myDeque` at specified positions using the `.insert()` method:

```cpp
#include <iostream>
#include <deque>
#include <string>

int main() {
    std::deque<std::string> myDeque;

    myDeque.push_back("A");
    myDeque.push_back("C");
    myDeque.insert(myDeque.begin() + 1, "B"); // Insert "B" at index 1
    myDeque.push_back("D");

    for (const auto& value : myDeque) {
        std::cout << ' ' << value;
    }
}
```
