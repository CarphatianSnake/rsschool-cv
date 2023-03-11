# Markuntovych Dmytro
##### Front-End Developer

![My Photo](https://user-images.githubusercontent.com/17194679/224482756-07a4ba13-9b5b-4a6b-aa59-a236f610e1a4.jpg)

## Contacts
 - Email: dmytro.markuntovych@gmail.com
 - Phone: +380502754918
 - Location: Ukraine, Vinnitsa

## About me
Being challenged is what motivates me!

I'm Web Developer specializing in front end development. Experienced with all stages online store content development. I'm proficient in HTML5, CSS3, JavaScript, TypeScript, React.js and really motivated to develop high quality web projects and applications. Open to learning new technologies and I want to grow and develop as a web developer. I also have a team management and teamwork experience.

In my free time, I like to ride a bike. I am fond of extreme types of mountain biking, such as enduro and downhill. I love nature, especially mountains. I like to travel and listen to music.

## Tech Skills
 - React.js
 - Redux Toolkit
 - JavaScript
 - TypeScript
 - HTML5
 - CSS3
 - SCSS
 - Node.js
 - GIT
 - Webpack
 - Gulp
 - VSCode
 - Figma
 - Adobe Photoshop

## Soft Skills
 - Quick Learning
 - Communicable
 - Teamwork
 - Team management

## Code Example
 ```javascript
 function undoRedo(object) {
 
  let undoArr = [];
  let redoArr = [];
  
  const setLastAction = (arr, key) => {
  
    const obj = { key, value: object[key] };
    obj.action = !object[key] ? 'del' : 'set';
    arr.push(obj);
    
  };
  
  const setActionData = (key) => {
  
    redoArr = [];
    setLastAction(undoArr, key);
    
  };
  
  const restoreLastAction = (unReAction, restoreActionArr, setActionArr) => {
  
    if (restoreActionArr.length > 0) {
      const lastAction = restoreActionArr.pop();
      const { action, key, value } = lastAction;
      setLastAction(setActionArr, key);
      action === 'set' ? object[key] = value :  delete object[key];
    } else {
      console.error(`There is nothing to ${unReAction}!`);
    }
    
  };
  
  return {
  
    set(key, value) {
      setActionData(key);
      object[key] = value;
    },
    
    get(key) {
      return object[key];
    },
    
    del(key) {
      setActionData(key);
      delete object[key];
    },
    
    undo() {
      restoreLastAction('undo', undoArr, redoArr);
    },
    
    redo() {
      restoreLastAction('redo', redoArr, undoArr);
    }
    
  };
  
}
 ```
