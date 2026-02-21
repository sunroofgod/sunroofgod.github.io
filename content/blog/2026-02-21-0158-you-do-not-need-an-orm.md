+++
title = 'You Do Not Need an Orm'
date = 2026-02-21T01:58:40+08:00
tags = [
    "database",
    "sql",
]
+++

Was watching this [video](https://www.youtube.com/watch?v=8vrEtKc-TBU) and it got me thinking about 
why was the ORM architecture created in the first place?

I'd previously assumed ORMs allowed develops to more easily do queries from DB effectively, similar
to that of the `ActiveRecordModel` in Ruby on Rails. Thinking deeper, it seems like ORMs are just
what developers like - further abstraction (from the hell that is fine-tuning SQL queries).

> There is also the added tediousness/technical friction of having to maintain SQL queries.

The talk goes into one alternative solution to ORMs that resolves the issues mentioned above - one that
keeps the same levels of abstraction as ORMs. By providing a wrapper of some kind, you store and optimise
SQL queries elsewhere, and only directly interact with DB through function calls.

```python {linenos=inline}
def get_book_covers_and_name_by_genre(db: sql.db.connection, query: str):
    books: list = db.query(str)
    for book in books:
        book_instance = BookLibrary.get(book.id)
        # do book stuff
```

Advantages of something like this would be that you're free to manipulate the implementation of the
table objects without altering the database. Something like this wouldn't be affected by migrations
and is also free to be easily extended, along with better documentation capabilities.