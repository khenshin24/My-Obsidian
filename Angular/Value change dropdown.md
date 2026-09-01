
```import { CommonModule, NgFor, NgIf } from '@angular/common';

import { Component } from '@angular/core';

import { RouterOutlet } from '@angular/router';

@Component({

  selector: 'app-root',

  standalone: true,

  imports: [RouterOutlet,NgFor,NgIf],

  templateUrl: './app.component.html',

  styleUrl: './app.component.css',

})

export class AppComponent {

  title = 'example';
  

  data = [

    {label : 'Option 1',value : 'option1'},

    {label : 'Option 2',value : 'option2'},

    {label : 'Option 3',value : 'option3'},

    {label : 'Option 4',value : 'option4'},

    {label : 'Option 5',value : 'option5'},

  ]

  
  selectedValue : string = this.data[0].value;// setting the default value is the Option 1 in UI

  onSelectChange(event : any){

    this.selectedValue = event.target.value;

  }

}