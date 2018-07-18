# Quiz API

This is a simple quiz API for use in assignments and technical interviews.

You can try it out yourself [here][deploy]!

## API

The package exposes a REST API with two separate endpoints:

- `/questsions` - returns a list of questions on the format:

    ```json
    [
      {
        "id": 2,
        "question": "Which actor played Richard III in the 1995 British film drama of the same title?",
        "choices": ["Ian McKellen", "Partrick Stewart", "Elijah Wood"]
      }
    ]
    ```

    Some questions come with optional choices and some don't.

- `/answer/:id` - returns the answer to a given question

  ```json
  {
    "id": 2,
    "answer": "Ian McKellen"
  }
  ```

> The API is CORS enabled so you can make requests from other origins.

## Deployment

The package is easy to deploy using `now`. Just run:

```bash
now
```

[deploy]: https://futu-quiz-api.now.sh/
