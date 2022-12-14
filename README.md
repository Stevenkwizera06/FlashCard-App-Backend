# Flashcards-app-backend


# Flashcard Backend
This project uses: 
- graphql
- apollo
- typescript generated by nexus
- prism ORM
- postgreSQL as database

## Environment Variables
In your `.env `  include your postgress **DATABASE_URL**

`DATABASE_URL="postgres://<user>:<password>@localhost:5432/database_name>"
`
## Testing your GraphQL api

1. Clone this repo to your PC
2. Run the development server with 
```bash
npm run dev
```
## Test data

To use these data open [http://localhost:5000](http://localhost:5000) with your browser to test your graphql server using **studio apollographql**.

**create a card**
```
mutation {
  createCard(question: "what is the capital city of Rwanda?", description: "Capital city", answer: "Kigali") {
    id
  }
}
```

**To view all cards**
```
query AllCards {
  allCards {
    id
    question
    description
    answer
  }
}


```
**To view one card**
```
query oneCard {
 oneCard (id:1) {
    id
    question
    description
    answer
  }
}
```

**To delete one card**
```
mutation {
  deleteCard(id:1) {
    id
  }
}
```

**To update one card**
```
mutation {
  updateCard(id:2, question: "What", description: "Be brief", answer: "A library") {
    id
  }
}
```

**To view one card**
```
query oneCard {
 oneCard (id:1) {
    id
    question
    description
    answer
  }
}
```

# FlashCard-App-Backend
