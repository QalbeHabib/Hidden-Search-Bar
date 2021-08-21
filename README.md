toggle() Method


toggle() is an interesting method. It removes the class if it already exists, otherwise, it adds it to the collection.



Without this method, you have to manually check if the class exists using contain() before toggling it on or off:




// manual toggle
if (pizza.classList.contains('olive')) {
    pizza.classList.remove('olive');
} else {
    pizza.classList.add('olive');
}




With the toggle() method, you simply pass the name of the class which you want to toggle:




pizza.classList.toggle('olive');
The toggle() method returns true if the class was added, and false if it was removed:

const status = pizza.classList.toggle('olive');

console.log(status); // true --> class was added


You can also pass a second boolean parameter to the toggle() method to indicate whether to add the class or remove it. This will turn toggle() into one way-only operation. If the second argument evaluates to false, then the class will only be removed, but not added. If it evaluates to true, then the class will only be added, but not removed.

Here is an example:

const status = pizza.classList.toggle('hot', false);

console.log(status); // false --> class was removed

[Edit on StackBlitz ⚡️](https://stackblitz.com/edit/web-platform-b7yc97)
