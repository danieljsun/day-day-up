# Gotcha
* Handling pagination within one lambda invocation is not scalalbe.
* It may fail because of time out with large data set.
* Solution- `Choice` state
  * Condition on the pagination hint (e.g. `nextToken`)
  * If present, repeat
