# 2024 AP Computer Science Principles Free-Response Questions: Set 1

## AP® Computer Science Principles Written Response Prompts

### Instructions:

- **Time:** 1 hour
- **Questions:** 2
- Read each question carefully and completely.
- Write your response in the space provided for each question in the Written Response booklet.
- You may plan your answers in this orange booklet, but no credit will be given for anything written in this booklet. You will only earn credit for what you write in the separate Written Response booklet.

---

### Pre-FRQ Practice

## Identify the Algorithm present in the JavaScript Files.

```JavaScript
///Evan
  function removeToDo() {
    const specificCard = this.parentElement; //Sequencing by defining variables
    const specificCardText =
      specificCard.querySelector(".to-do-card").textContent;

    for (let i = 0; i < ToDoItems.length; i++) { /// Iteration
      if (ToDoItems[i] === specificCardText) { /// Selection
        ToDoItems.splice(i, 1);
        break;
      }
    }
    specificCard.remove();
  }
///Gabe
     function final(array){
        let a = 0  ///Sequencing
        let b = 0
        for (let i = 0; i < array.length; i++){  ///Iteration
         if (array[i].includes("Correct")) {a++}  ///Selection
         if (array[i].includes("Incorrect")) {b++}}
         clear()
         const correct = a * 100/DOMSelectors.input.value
         const incorrect = b * 100/DOMSelectors.input.value
         DOMSelectors.question.insertAdjacentHTML("beforeend", `<h1>You got ${correct}% of them right and ${incorrect}% of them wrong!</h1>`)
        }
```

### Aspects of Algorithm

Sequencing
Selection
Iteration

### Question 1

Programs accept input to achieve their intended functionality. **Describe at least one valid input to your program and what your program does with that input.**

```JavaScript
//Evan
  const removeButton = document.querySelectorAll(".remove-button");
  removeButton.forEach((button) => {
    button.addEventListener("click", removeToDo);
  });

  function removeToDo() {
    const specificCard = this.parentElement;
    const specificCardText =
      specificCard.querySelector(".to-do-card").textContent;

    for (let i = 0; i < ToDoItems.length; i++) {
      if (ToDoItems[i] === specificCardText) {
        ToDoItems.splice(i, 1);
        break;
      }
    }
    specificCard.remove();
  }
```

This function awaits for users to interact by clicking the remove button, which will then run the function removeToDo, which will identify a certain card that the user is trying to remove and will then remove it.

```JavaScript
//Gabe
     DOMSelectors.form.addEventListener('submit', function(event) {
         event.preventDefault()
         const input = DOMSelectors.input.value;
         displayQuestion(input)
     });
```

This function awaits for users to interact by submitting the form, which it will then display questions using the input of the users from the form.

- Writs function awaite your responses to this question only on the designated pages in the separate Written Response booklet.
- If there are multiple parts to this question, write the part letter with your response.

---

### Question 2

Refer to your Personalized Project Reference when answering this question.

#### Part (a):

Consider the first iteration statement included in the Procedure section of your Personalized Project Reference. **Describe what is being accomplished by the code in the body of the iteration statement.**

```Javascript
//Evan
 for (let i = 0; i < ToDoItems.length; i++) {
     if (ToDoItems[i] === specificCardText) {
       ToDoItems.splice(i, 1);
       break;
     }
   }
```

This iteration statement continues to repeat the code using a for loop by looking at all of the items in the to do list, breaking off the specific part that the user wants to remove by not having it be defined as i, and then breaking it off as a seperate variable from the rest of the program so that the remove function is able to successfully remove it.

```Javascript
//Gabe
   function final(array){
        let a = 0
        let b = 0
        for (let i = 0; i < array.length; i++){
         if (array[i].includes("Correct")) {a++}
         if (array[i].includes("Incorrect")) {b++}}
         clear()
         const correct = a * 100/DOMSelectors.input.value
         const incorrect = b * 100/DOMSelectors.input.value
         DOMSelectors.question.insertAdjacentHTML("beforeend", `<h1>You got ${correct}% of them right and ${incorrect}% of them wrong!</h1>`)
        }
```

This iteration statement uses a for loop in order to repeat the code which is able to calculate the score of the user after completing the test. The for loop repeats so that the entirety of the array is run.

#### Part (b):

Consider the procedure identified in part (i) of the Procedure section of your Personalized Project Reference.

- Write two calls to your procedure that each cause a different code segment in the procedure to execute.
- Describe the expected behavior of each call. If it is not possible for two calls to your procedure to cause different code segments to execute, explain why this is the case for your procedure.

//Evan
The addToDo(); function runs when the user submits the form, which then adds another to do to the array
THe removeToDo(); function runs when the user clicks the remove button. This function identifies the specific to-do item to remove from both the ToDoItems array and the DOM. It removes the item from the array using splice() and deletes the corresponding DOM element.

//Gabe
The main function runs at the beginning of the code which fetches the questions from the api.
the game(qa) function runs which begins the main part of the program after the questions are put from the api into the qa.

#### Part (c):

Suppose another programmer provides you with a procedure called `checkValidity(value)` that:

- Returns `true` if a value passed as an argument is considered valid by the other programmer.
- Returns `false` otherwise.

Using the list identified in the List section of your Personalized Project Reference, **explain in detailed steps an algorithm that uses `checkValidity` to check whether all elements in your list are considered valid by the other programmer.** Your explanation must be detailed enough for someone else to write the program code for the algorithm that uses `checkValidity`.

- Write your responses to this question only on the designated pages in the separate Written Response booklet.
- If there are multiple parts to this question, write the part letter with your response.

  //Evan

```Javascript
function checkValidity(ToDoItems) {
    let result = true;
    for (let i=0; i< ToDoItems.length(); i++) {
        if(checkValidity(ToDoItems(i)) === false) {
            result = false;
            return false;
        }
    }
    return result;
}
```

//Gabe

```Javascript
function checkValidity(array) {
    let result = true;
    for (let i=0; i< array.length(); i++) {
        if(checkValidity(array(i)) === false) {
            result = false;
            return false;
        }
    }
    return result;
}
```

---

### End of Exam

```

```

```

```

```

```
