# Technical assessment

This small set of exercises is intended to test some basic habilities as a software developer.

## Exercise 1
 
Clone this repository in your development machine. You should answer the questions below directly in this text file and commit the answers to your local copy of the repository.

## Exercise 2

Given the following piece of code, written in Javascript:
```
async function routine(value) {
  const items = await dataService.fetchAllItems();
  const filtered = items.filter(i => i.value === value);
  return filtered;
}
```

Answer the following questions:
1. What is this routine returning?

This function returns an array whose elements are equal and of the same type (===) as the "value" attribute.

2. What type of return value can be expected (string, number, array, object)? 

An array.

3. What happens if the method *dataService.fetchAllItems()* returns null?

The function throws the “Uncaught TypeError: Cannot read property 'filter' of null”.

4. Why do we use the keyword "await" at the first line of the code?

The await expression pauses the execution of the async function and waits for result of the dataService.fetchAllItems().

## Exercise 3

Change the method of Exercise 2 to return an empty array if the method *dataService.fetchAllItems()* returns null.

```
async function routine(value) {
  const items = await dataService.fetchAllItems();
  if (items != null) {
  	const filtered = items.filter(i => i.value === value);
  	return filtered;
  } else {
	return [];
  }
}
```

## Exercise 4

Create a single HTML file, including the necessary CSS inside the <style> tags, representing the following webpage:
![Webpage](https://raw.githubusercontent.com/algebrik/web-basic-assessment/master/html-mockup.png)

## Exercise 5

Create a private repository and push this exercise to it. Tip: add a new remote repository to your local git copy. Keep the repository private and grant access only to codehashi@codehashi.com. 
