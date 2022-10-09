Simple Vector
------------

Container, a simplified analogue of `std::vector`. A pointer wrapper has been written for this container. The idiom RAII is used.

Initialization
------------

- `SimpleVector(size_t size, const Type& value)` - creates a vector from size elements initialized with value
- `SimpleVector(size_t size)` - creates a vector from size elements initialized with the default value
- `SimpleVector<T>test {value1, value2.. , value-n}` -Creates a vector from std::initializer_list


Access to elements
-----------------

- `At(index)` - returns the value of the element at the index position, or throws an out_of_range exception
- `operator[index]` - returns the value of the element at the index position


Iterators
--------

Iterator type - `LegacyRandomAccessIterator `

Invalidation of the iterator - any operations with resizing, insertion into an arbitrary position (if without changing capacity, end() is disabled)
- `begin()` - returns the iterator to the first element of the array
- `end()` - returns the iterator to the position behind the last element of the array


Container
------

- `IsEmpty()` : returns true if the vector is empty
- `getSize()`: returns the number of elements
- `GetCapacity()`: returns the number of items that can be stored in the currently allocated memory


Modifiers
-----------

- `PushBack(T value)` - inserting an element at the end of the array
-`Insert(Iterator position, T value)` - inserting an element into an arbitrary position
- `Resize(t_size value)` - resizing
- `PopBack()` - deletes the last element of the array
- `Erase(Iterator position)` - deletes an element in the position position
- `swap(SimpleVector& other)` - exchange with `SimpleVector& other` data `A <-> B`


Complexity (efficiency) of general vector operations:
----------------------------------------------------

- Random access - constant `O(1)`
- Insertion or deletion of elements at the end - Amortized constant `O(1)`
- Insertion or deletion of elements - linearly by distance to the end of the vector `O(n)`

How to use
--------------

- Put the files `array_ptr.h, simple_vector in your project folder.h` from the repository.
- Connect SimpleVector to your file via the directives `#include "simple_vector.h, #include "array_ptr.h"`.
