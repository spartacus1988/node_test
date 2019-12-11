# node_test

Используя библиотеки type-graphql и typeorm (может быть что-то еще?):

1) Создать мутацию на создание книги и автора в базе

2) Реализовать запрос на получение списка книг с автором из базы

3) Тест

 

Типы graphql схемы:

 

type Book {

  bookId: number;

  name: string;

  pageCount: number;

  authorId: number;

  author: Author;

}

 

type Author {

  authorId: number;

  name: string;

}

 

Пример запроса к graphql:

 

query {

  books() {

    name

    author {

      name

    }

  }

}
