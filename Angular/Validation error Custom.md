
<mat-form-field class="w-full">

          <mat-label>Email</mat-label>

          <input matInput formControlName="email">

          <mat-error *ngIf="control_is_invalid_email('email')">

            {{ validation_msgemail('email', 'Email') }}

          </mat-error>

        </mat-form-field>
        
        
    
```validation_msgemail(controlName: string, fieldName: string): string {

    const controlErrors = this.form.get(controlName)?.errors;

    if (controlErrors?.['required']) {

      return `${fieldName} is required.`;

    }

    if (controlErrors?.['email']) {

      return `Please enter valid email address.`;

    }

    return '';

  }

  

  control_is_invalid_email(controlName: string): boolean {

    const control = this.form.get(controlName);

    return !!control && control.invalid && (control.dirty || control.touched);

  }
        