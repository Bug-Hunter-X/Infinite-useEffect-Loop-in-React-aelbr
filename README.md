# Infinite useEffect Loop in React

This repository demonstrates a common React bug: an infinite loop caused by a missing dependency array in the `useEffect` hook.

The `bug.js` file contains the buggy code.  The `useEffect` hook logs the current count to the console after every render, creating an infinite loop because it doesn't specify any dependencies. This results in a continuously updating count and excessive console logging.

The `bugSolution.js` file provides the corrected code. The `useEffect` hook now includes the `count` variable in its dependency array, ensuring it only runs when the `count` changes.