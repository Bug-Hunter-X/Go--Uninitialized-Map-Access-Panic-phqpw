# Go: Uninitialized Map Access Panic

This repository demonstrates a common error in Go: accessing a map without checking for `nil`.  This can lead to a runtime panic, halting the program's execution.

The `bug.go` file shows the problematic code. The `bugSolution.go` file presents a corrected version that avoids the panic.

**Problem:**
Uninitialized maps in Go are `nil`. Attempting to access a key in a `nil` map will cause a runtime panic.

**Solution:**
Always check if a map is `nil` before accessing its elements, or initialize it with `make(map[KeyType]ValueType)`.  Alternatively, consider using a default value for the map.