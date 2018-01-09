# Async/Await

map内でのasync/awaitの使い方

https://stackoverflow.com/questions/40140149/use-async-await-with-array-map

引用
```
var arr = [1, 2, 3, 4, 5];

var results: number[] = await Promise.all(arr.map(async (item): Promise<number> => {
    await callAsynchronousOperation(item);
    return item + 1;
}));
```