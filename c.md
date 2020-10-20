# C

## Dealing with structured data

```C
#include <stdio.h>
#include <string.h>

struct Books {
   char  title[50];
   char  author[50];
   int   book_id;
};

int main() {
   struct Books Book1;        /* Declare Book1 of type Book */
   struct Books Book2;        /* Declare Book2 of type Book */

   /* book 1 specification */
   strcpy(Book1.title, "The C Programming Language");
   strcpy(Book1.author, "Brian W. Kernighan & Dennis M. Ritchie");
   Book1.book_id = 6495407;

   /* book 2 specification */
   strcpy(Book2.title, "Code: The Hidden Language of Computer Hardware and Software");
   strcpy(Book2.author, "Charles Petzold");
   Book2.book_id = 6495700;

   /* print Book1 info */
   printf("Book 1 title : %s\n", Book1.title);
   printf("Book 1 author : %s\n", Book1.author);
   printf("Book 1 book_id : %d\n", Book1.book_id);

   /* print Book2 info */
   printf("Book 2 title : %s\n", Book2.title);
   printf("Book 2 author : %s\n", Book2.author);
   printf("Book 2 book_id : %d\n", Book2.book_id);

   return 0;
}
```

## Passing struct as parameters

Structs can be passed as parameters just like any other basic data type.

```C
struct Books
{
  char title[50];
  char author[50];
  char subject[100];
  int book_id;
};

void print_book(struct Books book)
{
  printf("Book title : %s\n", book.title);
  printf("Book author : %s\n", book.author);
  printf("Book subject : %s\n", book.subject);
  printf("Book book_id : %d\n", book.book_id);
}
```
