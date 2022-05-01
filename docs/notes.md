# Notes

-   Prefix *always* has precedence over infix
-   Type def of `x + y + z`:
    
    ```Haskell
    Int -> Int -> Int -> Int
    ```

    Can be thought of as:

    ```Haskell
    Int -> (Int -> (Int -> Int))
    ```
    
    AKA a function that takes an `Int` and returns a function that takes an `Int` and returns a function that takes an `Int` and returns an `Int`. You can see the 4 `Int`'s in the previous sentence.

    Python equivalent:

    ```Python
    def add_three(x):
        def add_two_to_x(y):
            def add_one_to_x_plus_y(z):
                return x + y + z
            return add_one
        return add_two
    
    result = add_three(1)(2)(3)
    ```

-   Infix tick marks:

    ```Haskell
    3 `add` 4
    ```

    Can be thought of as:

    ```Haskell
    ((add 3) 4)
    ```

    So can be used on any function w/ 2 or more args: `a -> a -> a`

## Questions

-   [ ] How do you divide `Int` by `Int`?
