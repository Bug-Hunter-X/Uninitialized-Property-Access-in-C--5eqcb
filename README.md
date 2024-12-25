# Uninitialized Property Access in C#

This repository demonstrates a common, yet often subtle, bug in C#: accessing a property that hasn't been explicitly initialized.  While C# provides default values for properties (0 for integers, null for reference types, etc.), relying on these defaults can lead to unexpected behavior and difficult-to-debug issues.

**The bug:** The `ExampleClass` attempts to access the `MyProperty` without first assigning a value.  Depending on the context, this might result in 0, null, or other default values.

**The solution:** Explicitly initialize the `MyProperty` in the constructor or before it is used to avoid potential issues.