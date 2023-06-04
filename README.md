# JS_Task_9
# JavaScript Login Form Validation

This JavaScript code provides a simple login form validation for validating user input in a login form. It checks whether the username and password fields are empty and displays error messages if necessary.

## Usage

1. Include the JavaScript code in your HTML file:

   ```html
   <form id="loginForm">
     <div>
       <label for="username">Username:</label>
       <input type="text" id="username" name="username">
       <span id="usernameError" class="error"></span>
     </div>
     <div>
       <label for="password">Password:</label>
       <input type="password" id="password" name="password">
       <span id="passwordError" class="error"></span>
     </div>
     <button type="submit">Login</button>
   </form>

   <script src="login-form-validation.js"></script>
   ```

2. Add CSS styles to display error messages:

   ```css
   .error {
     color: red;
     display: none;
   }
   ```

3. Include the JavaScript code for form validation:

   ```javascript
   const loginForm = document.getElementById('loginForm');
   const usernameInput = document.getElementById('username');
   const passwordInput = document.getElementById('password');
   const usernameError = document.getElementById('usernameError');
   const passwordError = document.getElementById('passwordError');

   loginForm.addEventListener('submit', function (event) {
     event.preventDefault(); // Prevent form submission

     // Clear previous error messages
     usernameError.style.display = 'none';
     passwordError.style.display = 'none';

     // Fetch input values
     const username = usernameInput.value.trim();
     const password = passwordInput.value.trim();

     // Perform validation
     if (username === '') {
       usernameError.textContent = 'Username is required';
       usernameError.style.display = 'block';
       return;
     }

     if (password === '') {
       passwordError.textContent = 'Password is required';
       passwordError.style.display = 'block';
       return;
     }

     // Validation successful, proceed with login process
     // Add your login logic here
   });
   ```

4. Customize the error messages, validation logic, and login process to match your requirements.

## Example

HTML:

```html
<form id="loginForm">
  <div>
    <label for="username">Username:</label>
    <input type="text" id="username" name="username">
    <span id="usernameError" class="error"></span>
  </div>
  <div>
    <label for="password">Password:</label>
    <input type="password" id="password" name="password">
    <span id="passwordError" class="error"></span>
  </div>
  <button type="submit">Login</button>
</form>

<script src="login-form-validation.js"></script>
```

CSS:

```css
.error {
  color: red;
  display: none;
}
```

JavaScript (login-form-validation.js):

```javascript
const loginForm = document.getElementById('loginForm');
const usernameInput = document.getElementById('username');
const passwordInput = document.getElementById('password');
const usernameError = document.getElementById('usernameError');
const passwordError = document.getElementById('passwordError');

loginForm.addEventListener('submit', function (event) {
  event.preventDefault(); // Prevent form submission

  // Clear previous error messages
  usernameError.style.display = 'none';
  passwordError.style.display = 'none';

  // Fetch input values
  const username = usernameInput.value.trim();
  const password = passwordInput.value.trim();

  // Perform validation
  if (username === '') {
   

 usernameError.textContent = 'Username is required';
    usernameError.style.display = 'block';
    return;
  }

  if (password === '') {
    passwordError.textContent = 'Password is required';
    passwordError.style.display = 'block';
    return;
  }

  // Validation successful, proceed with login process
  // Add your login logic here
});
```

In this example, the login form has two input fields, one for the username and one for the password. The JavaScript code listens for the form's submit event and performs the following validation:

1. It prevents the default form submission using `event.preventDefault()`.

2. It clears any previous error messages by hiding them.

3. It retrieves the values of the username and password inputs, trimming any leading or trailing whitespace.

4. It checks if the username is empty. If so, it displays an error message and stops further validation.

5. It checks if the password is empty. If so, it displays an error message and stops further validation.

6. If the validation passes, you can add your login logic or further processing inside the validation successful block.

Customize the error messages, styling, and login process according to your requirements.
