# Typescript Labs

## Lab 3: Optional Properties

file: `/src/03-optional-properties.problem.ts`

Consider this getName function:

```ts
export const getName = (params: { first: string; last: string }) => {
  if (params.last) {
    return `${params.first} ${params.last}`;
  }
  return params.first;
};
```
Reading the code, we can see that we don't need to pass in a last name in order for the function to work.

However, TypeScript doesn't know that yet.

We have an error with our "Should work with just the first name" test:

```sh
Argument of type '{ first: string; }' is not assignable to parameter of type '{ first: string; last: string; }'.
Property 'last' is missing in type '{ first: string; }' but required in type '{ first: string; last: string; }'.
```

Your challenge is to figure out how to type the object so that `last` is optional.