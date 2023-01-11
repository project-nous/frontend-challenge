# Nous frontend coding challenge

Hey 👋, congratulations on getting to coding challenge stage. 

This task resembles what we do here at Nous so it should give you a good idea of problems we are dealing with and how we work. 

In this task you will be given access to an API and a Figma file. Your task is to implement some of the design system components in the Figma file and to use them to display the data from the API.

You are free to solve this in any programming language and make use of any frameworks you wish.

For transparency, at Nous we use [Typescript](https://www.typescriptlang.org/), [React](https://reactjs.org/), and [TailwindCSS](https://tailwindcss.com/) - but please don't feel like you have to use them, we'd prefer you to smash this challenge in whatever you feel comfortable coding in.

## Background

One way Nous gathers data about a household is via users connecting their bank accounts through Open Banking. Nous can use data on the transactions in a user's bank account to build up a picture of their household's spending habits, which is presented in an easy-to-understand way.

## Exercise

### Task 1

You will find a Figma file [here](https://www.figma.com/file/z4u4boBGc4tZ5KMIgw01vZ/Nous-frontend-challenge?node-id=0%3A1&t=18kwC6fFt8pQTYQ0-0).

Your first task is to implement the design system components.

#### What we're looking for
- Implementing designs reliably
- Simplicity and reusability
- Thoughtful accessibility

### Task 2

#### Background

We have a REST API hosted on [frontend-challenge.nous.co/api/rest](https://frontend-challenge.nous.co/api/rest) and a GraphQL API hosted on [frontend-challenge.nous.co/api/graphql](https://frontend-challenge.nous.co/api/graphql)

Both APIs are able to return:
- A list of banks
- Details about a specifc bank
- A list of bank accounts
- Details about a specific bank account

The REST endpoints you will be interested in are
- [/bank](https://frontend-challenge.nous.co/api/rest/bank)
- [/bank/{id}](https://frontend-challenge.nous.co/api/rest/bank/1)
- [/account](https://frontend-challenge.nous.co/api/rest/account)
- [/account/{id}](https://frontend-challenge.nous.co/api/rest/account/1)

The respective GraphQL queries you will be interested in are:
- `banks`
- `bank`
- `accounts`
- `account`

In both cases, the schema of a **bank** is:
```
id: number
name: string
logo: string
```
and the schema of an **account** is
```
id: number
sortCode: string
accountNumber: string
bankId: number
```

In the case of the GraphQL API you are able to query `bank` through the `account` schema.

#### Task

Your task is to implement the page found [here](https://www.figma.com/file/z4u4boBGc4tZ5KMIgw01vZ/Nous-frontend-challenge?node-id=6%3A2&t=18kwC6fFt8pQTYQ0-0) using the components you created in [Task 1](#task-1)

You may choose either the REST API or the GraphQL API, whatever you feel more comfortable with. For transparency, at Nous we use GraphQL.

Both APIs intentionally add a random time to the latency of every request of between 0 and 2000 milliseconds. Make sure your solution handles this gracefully by including your own design thinking; for example, loading states.

#### What we're looking for
- Your ability to interpret designs with limited information
- Use of the design system from previous task
- A responsive design
- State feedback to the user
- Your ability to connect frontend with API
