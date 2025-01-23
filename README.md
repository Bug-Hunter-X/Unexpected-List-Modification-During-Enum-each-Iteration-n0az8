# Elixir List Modification During Enum.each
This example demonstrates an unexpected behavior when attempting to modify a list while iterating over it using `Enum.each`. The core issue lies in the immutability of Elixir data structures; `List.delete` creates a *new* list, leaving the original list unchanged.

The provided `bug.exs` file illustrates this problem.  The intended behavior is to remove the element `3` from the list; however, due to the immutability and the way `Enum.each` works, the original list remains unaffected.

The solution demonstrates the correct approach using `Enum.filter` to create a new list excluding the specified element.