# Incorrect `node-fetch` import in Next.js `getServerSideProps`

This repository demonstrates a common error when using `node-fetch` within a Next.js `getServerSideProps` function.  The problem arises from attempting to import `node-fetch` directly, which is unnecessary.  Next.js provides built-in `fetch` functionality, eliminating the need for an external library.

## Bug

The original code incorrectly imports `node-fetch`. This causes an error during runtime, as `node-fetch` is not automatically available in the Next.js environment for `getServerSideProps`.

## Solution

The solution removes the `node-fetch` import and utilizes the native `fetch` API provided by Next.js. This ensures the code runs correctly and avoids runtime errors.