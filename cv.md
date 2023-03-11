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

## Experience
  I have no commercial experience as Front-End developer, but I have some study projects:
  1. Songbird
    - This is single page application that fully generates by JavaScript
    - Repo: https://github.com/CarphatianSnake/songbird
    - Deploy: https://carphatiansnake.github.io/songbird/
  2. Simple calculator of providers prices
    - Repo: https://github.com/CarphatianSnake/bytecloudtest
    - Deploy: https://serene-pavlova-247a26.netlify.app/
  3. Petspaw application
    - Not finished. And I decided to remake it using TypeScript and RTK Query. Work only for desktop version. And some functionality like search and filters don't work.
    - Repo: https://github.com/CarphatianSnake/petspaw
    - Deploy: https://imaginative-cascaron-943041.netlify.app/
    - And, it's sad, but some requests began not working :(
    - Second vesion (with TypeScript and RTK Query), that I making deployed here: https://petspaw-692a7b.netlify.app/
    - Now it only has responsive layout, theme switching and you can vote for photos, thats all for this moment.
  4. Eldrich Horror
    - It was a task to make and algorithm for stack mixing.
    - Repo: https://github.com/CarphatianSnake/eldritch
    - Deploy: https://carpathiansnake-eldrich.netlify.app/
  5. CRUD practice aplication
    - Repo: https://carpathiansnake-eldrich.netlify.app/
    - No deploy.
  6. HTML builder
    - Node.js basics practice task.
    - Repo: https://github.com/CarphatianSnake/HTML-builder
