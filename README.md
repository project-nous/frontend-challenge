# Nous frontend challenge

Hey 👋, congratulations on getting to code challenge stage. 

This task resembles what we do here at Nous so it should give you a good idea of problems we are dealing with here and how we work. 

In this task you will be given access to an API and a Figma file; your task is to implement some of the design system components in the Figma file and to use them to display the data from the API.

You are free to solve this in any programming language and make use of any frameworks you wish.

For transparency, here at Nous we use [Typescript](https://www.typescriptlang.org/), [React](https://reactjs.org/), and [TailwindCSS](https://tailwindcss.com/) - but don't feel you have to use them, we'd prefer you to smash this task in whatever you feel comfortable coding in.

## Background

One way Nous gathers data about a household is via users connecting their bank accounts through open banking. Nous then uses the transactional data to build a modal of the household's spending habits and presents it in an easy to understand way.

## Exercise

### 1

You will find a Figma file [here]().

Your first task is to implement the design system components found [here]()

### 2

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

Your task is to implement the page found [here]() using the components you created in **task 1**

You maybe choose either the REST API or the GraphQL API, whatever you feel more comfortable with. 

For transparency, here at Nous we use GraphQL.

Note, both APIs introduce an intential random latency between 0 and 2000 milliseconds for every request - make sure your solution handles this gracefully but including your own design thinking of loading states, etc. 