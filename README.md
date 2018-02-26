# async-patterns

# Async Await Promise All Array Destructuring
```javascript
const getBook = async bookName => {
  const book = await fetchBook(bookName);

  const [author, rating] = await Promise.all([
    fetchAuthor(book.authorId),
    fetchRating(book.id)
  ]);

  return {
    ...book,
    author,
    rating
  };
};
```
Reference: https://www.dalejefferson.com/blog/async-await-promise-all-array-destructuring/
