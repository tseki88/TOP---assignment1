The Odin Project - Assignment 1

*has been modified for DOM project.

TO DO
1. Make buttons for player input - DONE
2. Display Output to HTML window instead of console log / add a play count - DONE
3. Fix best of 5 function and disable playerInput buttons until reset - DONE
    - make a counter when above 5 to disable
    - reset button to clear counter, therefore able to replay again.


Learnings Notes

Issue #1:

Was stuck on why this function wasn't working.
On click, was under the assumption that I can get a function to run, with a nested function but giving it a value which it would return.
Instead, changed it to an arrow function to make the even assign the value of button.id to a variable playerInput (declared earlier).

Function I had issues with:

 playerInput(x){
     return x
 }

 const buttons = document.querySelectorAll("button");

 buttons.forEach((button) => {
     button.addEventListener("click", function(e){
         playerInput(button.id);
     });
     button.addEventListener("click", function(){
         runGame();
     });
 });


Issue #2:

Creating a function where the results which went to console.log in prior excercise, to instead output to a 'p' box in the body.
Redeclare creating the <p> for the info inside it's own shell otherwise would append both text to same line.
code was getting cluttered, therefore declared a logOutput function where the output can be declared within the parenthesis of the function.