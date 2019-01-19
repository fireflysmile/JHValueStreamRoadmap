# JHValueStreamRoadmap

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 7.2.1.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).


##use modal
*.html
use div with class .modal-header to wrap header
example:
<button (click)="openModal('custom-modal-1')">Open Modal 1</button>
<div class="modal-header">this is head</div>
<app-modal id="custom-modal-1">
  <h1>A Custom Modal!</h1>
  <p>Home page text:</p>
  <button (click)="closeModal('custom-modal-1');">Close</button>
</app-modal>

*.ts
import { ModalService } from './components/modal/modal.service';

constructor(private modalService: ModalService) {
}
//to show Modal
openModal(id: string) {
    this.modalService.open(id);
}

//to hide Modal
closeModal(id: string) {
    this.modalService.close(id);
}

//to remove Modal
removeModal(id: string) {
    this.modalService.remove(id);
}
----