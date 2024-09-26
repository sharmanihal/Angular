### `?` (Optional Property/Parameter)
- The `?` symbol is used to mark a property or parameter as optional. This means that the property or parameter may or may not be present.
- When used in a class or interface, it indicates that the property is optional.
- When used in a function parameter, it indicates that the parameter is optional.

**Example**:
```typescript
interface User {
  id: number;
  name?: string; // name is optional
}

function greet(user: { name?: string }) {
  console.log(`Hello, ${user.name || 'Guest'}`);
}
```

### `!` (Non-Null Assertion Operator)
- The `!` symbol is known as the non-null assertion operator. It tells the TypeScript compiler that a value that could be `null` or `undefined` is actually neither.
- This is useful when you are certain that a value is not `null` or `undefined`, but TypeScript's type system cannot infer that.

**Example**:
```typescript
let userName: string | undefined;
userName = "Alice";
console.log(userName!.toUpperCase()); // Asserts that userName is not undefined
```

### `|` (Union Type)
- The `|` symbol is used to define a union type, which allows a variable to hold one of several types.
- This is useful when a value can be of multiple types.

**Example**:
```typescript
let value: string | number;
value = "Hello";
value = 42; // Both assignments are valid
```

### Summary
- **`?`**: Marks a property or parameter as optional.
- **`!`**: Asserts that a value is not `null` or `undefined`.
- **`|`**: Defines a union type, allowing a variable to hold one of several types.

These operators help make TypeScript more flexible and powerful by allowing you to handle optional values, assert non-null values, and define variables that can hold multiple types.


###  Custome Type 
In TypeScript, you can define custom types using either the `type` keyword or the `interface` keyword. Both serve to describe the shape of an object, but they have some differences in their usage and capabilities.

### Using `type` Keyword:
```typescript
type User = {
  id: string;
  name: string;
  avatar: string;
};
```

### Using `interface` Keyword:
```typescript
interface User {
  id: string;
  name: string;
  avatar: string;
}
```

### Key Difference
**Complex Types**:
   - `type` can represent more complex types like unions, tuples, and mapped types.
   - `interface` is primarily used for object shapes.

Both are powerful tools, and the choice between them often comes down to personal preference and specific use cases. Do you have a preference for one over the other?
