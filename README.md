# Voting Rest API.

Similar to StackOverflow, the service allows the user to vote answers up or down depending on how they view the answer

Tech used: Node, Express and MongoDB.


## API Reference

#### Get all questions

```http
  GET /questions
```
Returns all questions in store.

#### Adds new questions

```http
  POST /questions
```

Will add new questions to current store. 

#### Returns a specific question 

```http
  GET /questions/${qID}
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `qID`      | `string` | **Required**. question Id |

Returns specific question.


#### Updates question with answer

```http
  POST /questions/${qID}/answers
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `qID`      | `string` | **Required**. question Id |

Adds a new answer to a question.

#### Edit a specific answer

```http
  PUT /questions/${qID}/answers/aID
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `qID`      | `string` | **Required**. question id |
| `aID`      | `string` | **Required**. answer id |

Edits a answer to a question.

```http
  DELETE /${qID}/answers/aID
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `qID`      | `string` | **Required**. question id |
| `aID`      | `string` | **Required**. answer id |

Deletes a answer to a question.

```http
  POST questions/${qID}/answers/aID/vote-up
  POST questions/${qID}/answers/aID/vote-down
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `qID`      | `string` | **Required**. question id |
| `aID`      | `string` | **Required**. answer id |
| `vote-up`      | `string` | **Required**. votes answer up |
| `vote-down`      | `string` | **Required**. votes answer down |

Votes answer up/down. 
