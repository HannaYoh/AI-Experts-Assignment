1. What was the bug?
2. Why did it happen?
3. Why does your fix solve it?
4. One realistic case / edge case your tests still don’t cover

The bug was seen in a test case that failed to refresh token when handling dictionary token. The program did not request a new token. This is beacause dictionary checks were ignored only none and expired where handled. To solve the issue I added a type check for dictionary. UNexpected errors such as missing values for the tokens is not handled in the tests.
