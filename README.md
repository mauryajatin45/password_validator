# Password Strength Checker - React App

This project is a simple React-based password strength checker. It evaluates a password input based on several conditions such as length, the presence of uppercase and lowercase letters, and the inclusion of special symbols. The user is provided with real-time feedback about their password strength.

## Features

- **Password validation** based on:
  - Minimum length of 12 characters
  - At least one uppercase letter
  - At least one lowercase letter
  - At least one special character (e.g., `!@#$%^&*()`)
  
- **Real-time feedback** indicating whether the entered password is "Strong" or "Weak" based on the above conditions.
- **Visual feedback** for each validation condition with checkmarks and crosses to indicate whether each criterion is met.

## Technologies Used

- **React** - A JavaScript library for building user interfaces.
- **CSS** - For styling the components and making the UI responsive.
- **State Management** - React's `useState` hook to manage state for the password conditions.

## Installation

To run this project locally, follow these steps:

1. **Clone the repository**:

   ```bash
   git clone https://github.com/your-username/password-strength-checker.git
   ```

2. **Navigate into the project directory**:

   ```bash
   cd password-strength-checker
   ```

3. **Install dependencies**:

   If you don't have `npm` installed, first install [Node.js](https://nodejs.org/). Then, run:

   ```bash
   npm install
   ```

4. **Start the development server**:

   ```bash
   npm start
   ```

5. Open your browser and navigate to `http://localhost:3000`.

## Usage

1. **Enter a password** in the input field.
2. As you type, the app will automatically evaluate the password based on the following conditions:
   - Whether it contains at least one **lowercase** letter
   - Whether it contains at least one **uppercase** letter
   - Whether it includes a **special character** (e.g., `!@#$%^&*`)
   - Whether it is at least **12 characters long**
3. The password strength will be displayed as either "Strong" or "Weak" based on whether all conditions are met.
4. Each condition is displayed with either a **checkmark (✅)** or a **cross (❌)** to visually indicate whether it is satisfied.

## Component Breakdown

### `Content.js`

This is the core component where the password validation logic takes place.

- **State**:
  - `identifier`: A boolean that tracks whether the password is strong or weak.
  - `conditions`: An object holding the conditions for the password strength.

- **Functions**:
  - `check()`: This function is called whenever the user types in the password input. It checks whether the password meets the required conditions and updates the state accordingly.

- **Conditional Feedback**: The `ConditionFeedback` component displays feedback on each individual validation condition (e.g., if the password contains a special character).

### `App.js`

The root component of the app. It imports `Content` and `Header`, and wraps them in the main container. It sets up the overall structure and layout.

### `styles.css`

The CSS file is used to style the components and make the app visually appealing. It includes:
- A dark background for the page.
- Centering of content using Flexbox.
- Styling for input fields, labels, and condition feedback messages.

### `ConditionFeedback.js`

A helper component that displays whether a specific validation condition is met. It receives a `condition` (boolean) and `text` (string) as props and shows either a green checkmark for valid conditions or a red cross for invalid ones.

## Example

When you type a password, such as `Passw0rd@1234`, the app will evaluate it based on the conditions and provide feedback like:

- ✅ 12 characters
- ✅ UpperCase
- ✅ LowerCase
- ✅ Special Symbol

If the password meets all conditions, it will be marked as "Strong"; otherwise, it will be marked as "Weak".

## Contributing

If you would like to contribute to this project, feel free to fork the repository, make changes, and submit a pull request.

### Bugs or Issues?

If you encounter any bugs or issues, please feel free to open an issue in the GitHub repository.

## License

This project is open source and available under the [MIT License](LICENSE).

---

Enjoy testing and improving password strength!
