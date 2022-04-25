# Looping constructs comparison chart

|                      | `async/await` support | skips non-numeric props | immutable index |
|----------------------|-----------------------|-------------------------|-----------------|
| Simple `for(;;)` loop| Yes                   | Yes                     | No              |
| `Array.forEach()`    | No                    | Yes                     | Yes             |
| `for/in`             | Yes                   | No                      | Yes             |
| `for/of`             | Yes                   | Yes                     | Yes             |

**You should prefer to use for/of unless you have a good reason not to**. You
may want to use `forEach()` for some neat syntactic sugar with `filter()` and
`map()`, or you may actually want to loop through non-numeric properties on an
array and use `for/in`. But `for/of` is the most robust approach and works well
for almost all cases.


