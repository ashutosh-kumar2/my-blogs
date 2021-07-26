## Creating my first app using NodeJS

Hi folks,

A few days back I started working on my first CLI (Command Line Interface) App. This app was a simple quiz on some facts about myself, which I could share with my friends to see how well they knew me. I created this app with beginner-level NodeJS concepts and hosted it on [repl.it](https://replit.com/@kashslash7/How-Well-Do-You-Know-Ashutosh?embed=1&output=1). 



![Screenshot 2021-07-26 at 14-29-30 How-Well-Do-You-Know-Ashutosh.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1627290013874/djNFiWHUg.png)

## Getting Started
While creating this quiz, I came across some interesting concepts in NodeJS, along with a few useful libraries/packages. These were the ones I used in the app:


- The very first package I used is called [readline-sync](https://www.npmjs.com/package/readline-sync). Using this package in your app allows you to have an interactive conversation with the user via a console. A simple example of this is: 


![Screenshot 2021-07-26 at 14-37-07 readline-sync.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1627290501090/Dz_N-nqS2.png)

Here, we pass the properties of the library [readline-sync](https://www.npmjs.com/package/readline-sync) to a variable ```readlineSync```. After this, we use the  ['question'](https://www.npmjs.com/package/readline-sync#question)  method with the variable to display a query to the user, and store his response in the variable ```userName```. Thereafter, we can simply use [console.log](https://developer.mozilla.org/en-US/docs/Web/API/console/log)  to print the user's response to the query, along with some other text as required.


- The second interesting library I used in the app was [chalk](https://www.npmjs.com/package/chalk). This library is used to style our strings in the terminal, which is a very useful feature while designing CLI apps. Using this library was a lovely experience in itself, because it transformed a bland-looking app into a stylized and colorful one. A simple example of this is:

![Screenshot 2021-07-26 at 15-00-08 chalk.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1627291838294/r9J4taW_m.png)

This will simply print **Hello world!** in the terminal, and also impart a blue color to it. This library can be used to style in terms of color, background, font etc. The best part about using chalk is that we can style the same string in many different ways according to our liking, and doing so is simple! Chalk comes with an easy to use **composable API** where **we just chain and nest the styles we want**. For example:


![Screenshot 2021-07-26 at 15-06-17 chalk.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1627292212684/X5bTZoICr.png)

## How the quiz works

Firstly, I created an **array of objects**, through which we can iterate when the quiz is started. Each object has a question and its relevant answer inside it. It looks like this:


![quesAndAns.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1627293795687/26LtRNzPG.png)

When the quiz starts, we iterate through this array of objects, firstly storing the current object in a variable ```currentQuestion``` , then accessing the ```question``` and ```answer``` property of the object by using ```currentQuestion.question``` and ```currentQuestion.answer```. This section of code helped me to understand how to implement arrays, objects and also learn how to access the properties of an object.


![Screenshot 2021-07-26 at 15-35-38 How-Well-Do-You-Know-Ashutosh.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1627293998714/fHwItYD5W.png)

As you can see in the above image, for each object we go through a function ```play()```. This function is at the heart of the working of this quiz, and looks like this:


![Screenshot 2021-07-26 at 15-47-39 How-Well-Do-You-Know-Ashutosh.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1627294736781/iSZp9bvIS.png)

This function takes the ```question``` and ```answer``` properties of the object ```currentQuestion``` as its input parameters, and asks the user for the response to a question, storing it in a variable ```userAnswer```. If ```currentQuestion.answer``` matches with ```userAnswer```, we congratulate the user and increment his/her score, else we move to the next question. Also note that I use ```.toLowerCase``` option while comparing the answers, so that entering the answer becomes case-insensitive, and my friends do not miss out on marks! 

At the end, we display user's score to him/her. Also, we compare user's score to the existing high scores stored in the code, so if the user gets a high score, he/she can send me a screenshot to update the code.


![Screenshot 2021-07-26 at 15-59-50 How-Well-Do-You-Know-Ashutosh.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1627295527370/2mHgr4A78.png)


The final output to the user looks like this:

![Screenshot 2021-07-26 at 16-03-33 How-Well-Do-You-Know-Ashutosh.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1627295696076/QgvjmYK6K.png)

## Conclusion

Creating an app from scratch, however simple it may be, is always a major confidence boost, and also an indicator that I can apply what I learnt. Please check out the [app](https://replit.com/@kashslash7/How-Well-Do-You-Know-Ashutosh?embed=1&output=1) I made, and also the [source code](https://github.com/ashutosh-kumar2/HowWellDoYouKnowAshutosh-fun-quiz-using-CLI) behind it. Also, feel free to suggest any changes/improvements you feel I could do to make it better.

## Resources

If you want to learn more about the packages/methods I used in this app, please read the documentation for them:

- [readline-sync](https://www.npmjs.com/package/readline-sync)
- [chalk](https://www.npmjs.com/package/chalk)
- [console.log](https://developer.mozilla.org/en-US/docs/Web/API/console/log)


 
