
#### 1. Install Vox Modal globally:


```sh
$ npm install --global vox-modal
```

#### 2. Install Vox Modal in your project devDependencies:

```sh
$ npm install --save-dev vox-modal
```

#### 3. Setup Module

Import VoxModalModule into your app.module.

```ts
import { VoxModalModule } from 'vox-modal';

@NgModule({
  ...
  imports: [
    VoxModalModule
  ],
})
```


#### 4 . Basic Usage
Import AlertService into your app.component

```ts
import { Component } from '@angular/core';

import { AlertService } from './alert/alert-service';
@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
})
export class AppComponent {
    title = 'app';
    constructor(
      private alertService: AlertService
    ) {

    }

    open() {
      this.alertService.openModal('AlertServiceService', 'Modal title', 'success');
    }
}

```

#### 5. Setup View
Place the app-alert selector at the bottom of your app.component.html
```html

<button type="button" class="btn btn-info" (click)="open()">Create template modal</button>

<app-alert></app-alert>

```

### Alert Types
The following message types are avialable. The typess below represent the Bootstrap [alert](https://v4-alpha.getbootstrap.com/components/alerts/) classes.
* success
* info
* warning
* danger
