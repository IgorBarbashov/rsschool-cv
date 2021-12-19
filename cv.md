# Junior Frontend Developer

## Igor Barbashov
Nizhny Novgorod  
40 years old

## Contact Info
**Phone**: +7 (905) 667-00-89  
**E-mail**: [bis200705@gmail.com](mailto:bis200705@gmail.com)  
**Skype**: [bis200705](skype:bis200705)  
**FB**: [https://www.facebook.com/Barbashov.Igor](https://www.facebook.com/Barbashov.Igor)  
**Telegram**: [https://t.me/igor_barbashov](https://t.me/igor_barbashov)  
**VK**: [https://vk.com/igor_barbashov](https://vk.com/igor_barbashov)  

## Summary
My **learning goal** in RS-school - get strong knowledge in frontend development, create several project and expand my employment opportunities  And my **long-term professional goal** - to become a senior Frontend developer.

I am very close to the position of the RS-school that education can be high quality, accessible and free for all. And I would like to take part in the development of this community. So, **one of my goals** is to **become a mentor** of the next stages on these courses.

About my character I can say that I am a person who is completely immersed into the current work. Beside the work I spend all free time to learning computer science and upgrade my frontend-developer skills. I’m a pragmatic, usually easy get a new knowledge (especially in computer science). If I don’t understand something, I work hard and do everything to do my job completely. I have analytic skills and it easy to me to systematize information.

## Skills
* HTML
* CSS
* JavaScript ES6
* React
* Redux
* MobX + MST
* TypeScript
* Git
* Eslint
* Webpack
* Docker (by simple docker-files)
* Bash
* Java

## Code examples
I can't give links to my job projects because they are staying on the private cooperative gitlab repositories.
But I can give link to me study application - the [game '4-in-line'](https://fourlines-68ec8.firebaseapp.com/game) with elements of AI (when computeris able to playing instead one ot two players).

All codes samples are posted in my [GitHub repositories](https://github.com/IgorBarbashov?tab=repositories).

Below is part of the code one of the training projects
```javascript
import React, { Component, PureComponent } from 'react';
import ReactDOM from 'react-dom';
import {
  observable,
  computed,
  extendObservable,
  configure,
  action,
  decorate,
  runInAction,
} from 'mobx';
import { observer } from 'mobx-react';

configure({ enforceActions: 'observed' });

type UserInterface = {
  login: { username: string };
} | null;

class Store {
  public user: UserInterface = null;

  public getUser(): void {
    fetch('https://randomuser.me/api/')
      .then(res => res.json())
      .then(json => {
        if (json.results) {
          const [newUser] = json.results;
          runInAction(() => {
            this.user = newUser;
          });
        }
      })
      .catch(error => {});
  }
}

decorate(Store, {
  user: observable,
  getUser: action.bound,
});

const appStore = new Store();

@observer
class App extends PureComponent<{ store: Store }, {}> {
  public render(): JSX.Element {
    const { store } = this.props;

    return (
      <div>
        <div>{`User: ${store.user ? store.user.login.username : ''}`}</div>
        <button onClick={store.getUser} type="button">
          New user
        </button>
      </div>
    );
  }
}

ReactDOM.render(<App store={appStore} />, document.getElementById('root'));
```

## Experience
My developer experience - 10 month. I was zero knowledge when I came to frontend developers courses, which was organized by one of Nizhny Novgorod IT-company. Before the courses end, I was invited to a job as junior frontend developer.

After 3-month adapting period I was assigned to a team that works on the real commercial project. I've upgraded my level by one grade on last assessment. And now I am the assistant of our tech lead on courses with which I self began.

## Education
* Nizhny Novgorod Polytechnical University, speciality “Computers, systems and networks”
* [htmlacadeny](https://htmlacademy.ru/profile/id979665/achievements)
* [hexlet](https://ru.hexlet.io/u/isbnn)
* [codecademy](https://www.codecademy.com/profiles/IgorBarbashov)
* [codewars](https://www.codewars.com/users/IgorBarbashov/stats)
* freecodecamp
* javarush

## English
Last june I finished courses by programm “Cambridge English Empower B1 - Pre-Intermediate” in the Nizhny Novgorod Linguistic University.

Now I’m learning on the programm which prepare students for pass Cambridge Preliminary English Test.

My best practice in English - is three-weeks traveling in the USA and communication with native English speakers.