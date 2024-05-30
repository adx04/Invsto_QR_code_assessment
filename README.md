**INVSTO ASSIGNMENT**


# Frontend Mentor - QR code component solution

This is a solution to the [QR code component challenge on Frontend Mentor given by Invsto](https://www.frontendmentor.io/challenges/qr-code-component-iux_sIO_H). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

### Table of contents

- [Overview](#overview)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

### Overview

### Screenshot

![@Screenshot](./screenshot.jpg)

### Links

- Solution URL: [@here](https://github.com/adx04/Invsto_QR_code_assessment)
- Live Site URL: [@here](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow
- [@React](https://reactjs.org/) - JS library
- [@Styled Components](https://styled-components.com/) - For styles
- [@Redux](https://redux.js.org/) - For state management

Certainly! Here's the updated content with specific learnings from the project:

### What I learned

This project reinforced my understanding of creating responsive designs and integrating state management with Redux. I learned how to use styled-components to create dynamic styles and how to implement a dark mode toggle using Redux for state management. Additionally, I explored advanced CSS animations, such as the cyberlight hover effect, to enhance user interactions.

Here are some of the key code snippets that illustrate what I learned:

1. **Styled-components for Dynamic Styles**:
   - Using styled-components to apply conditional styling based on theme state.
   
   ```jsx
   const CardContainer = styled.div`
     background-color: ${({ theme }) => theme.colors.white};
     transition: background-color 0.3s ease;
     &:hover {
       transform: scale(1.05);
       box-shadow: 0 20px 30px rgba(0, 0, 0, 0.2);
     }
   `;
   ```

2. **Redux for State Management**:
   - Implementing a dark mode toggle button with Redux to manage the application’s theme state.
   
   ```jsx
   // Action
   export const toggleDarkMode = () => ({
     type: 'TOGGLE_DARK_MODE',
   });

   // Reducer
   const themeReducer = (state = initialState, action) => {
     switch (action.type) {
       case 'TOGGLE_DARK_MODE':
         return {
           ...state,
           darkMode: !state.darkMode,
         };
       default:
         return state;
     }
   };

   // Toggle Button Component
   const ThemeToggle = () => {
     const dispatch = useDispatch();
     const darkMode = useSelector((state) => state.theme.darkMode);

     return (
       <button onClick={() => dispatch(toggleDarkMode())}>
         {darkMode ? 'Switch to Light Mode' : 'Switch to Dark Mode'}
       </button>
     );
   };
   ```

3. **CSS Animations and Hover Effects**:
   - Creating a cyberlight hover effect using CSS animations to enhance the visual appeal of the card component.
   
   ```css
   @keyframes cyberlight {
     0% {
       top: -50%;
       left: -50%;
       opacity: 1;
     }
     100% {
       top: 150%;
       left: 150%;
       opacity: 0;
     }
   }

   const CardContainer = styled.div`
     position: relative;
     overflow: hidden;

     &:hover::before {
       content: '';
       position: absolute;
       top: -50%;
       left: -50%;
       width: 200%;
       height: 200%;
       background: radial-gradient(circle at center, rgba(0, 255, 255, 0.5) 0%, rgba(0, 255, 255, 0) 60%);
       animation: cyberlight 1s ease-out;
     }
   `;
   ```

These learnings have improved my ability to create dynamic, responsive, and visually appealing web applications using React, Redux, and styled-components.


### Continued development

I plan to focus on several key areas to enhance my skills:

1. **Advanced CSS Techniques**:
    - **CSS Grid and Flexbox**: Mastering these tools for creating complex, responsive layouts.
    - **CSS Variables**: Using custom properties for consistent theming and easier maintenance.
    - **Responsive Design**: Ensuring designs look great on all devices using modern techniques like media queries and responsive units.

2. **State Management with Redux**:
    - **Redux Fundamentals**: Deepening my understanding of actions, reducers, and the store.
    - **Redux Middleware**: Learning to handle asynchronous operations with tools like Redux Thunk and Redux Saga.
    - **Redux Toolkit**: Exploring Redux Toolkit to simplify setup and reduce boilerplate.
    - **Dark Mode Toggle**: Implementing theme toggling functionality using Redux to manage the application's state, allowing users to switch between light and dark modes seamlessly.

3. **Interactive Components Using React**:
    - **Hooks and Context API**: Using Hooks for state management and Context API for global state without additional libraries.
    - **Component Libraries**: Experimenting with libraries like Material-UI to speed up development.
    - **Performance Optimization**: Implementing techniques like memoization, code splitting, and lazy loading.

4. **CSS Animations**:
    - **Keyframe Animations**: Creating sophisticated animations to enhance user experience.
    - **Hover Effects**: Implementing engaging hover effects like the cyberlight effect to make the interface more interactive.
    - **User Experience Enhancements**: Using animations to provide visual feedback and improve interactivity.

By focusing on these areas, I aim to build more dynamic, responsive, and high-performing applications that offer an excellent user experience.

### Useful resources

- [Styled Components Documentation](https://styled-components.com/docs) - This helped me understand how to create dynamic styles in React.
- [Redux Documentation](https://redux.js.org/introduction/getting-started) - Its actually an amazing resource to learn about state management in React applications.
- [The Markdown Guide](https://www.markdownguide.org/) - This helped me with writing better markdown for my README file, furthermore though a good README guide was already provided in the project materials initially.

## Author
- Ayush Dey
- Website - [@Invsto_Assignment]
- Linkedin - [@Ayush Dey](https://www.linkedin.com/in/ayush-dey-36919825a/)
- Hackerrank - [@adx04](https://www.hackerrank.com/profile/adx04))

## Acknowledgments

Certainly! Here's the improved acknowledgment section:

## Acknowledgments

I'd like to thank the Frontend Mentor community and the Stack Overflow community for their support and feedback throughout this project. Their insights were invaluable in helping me improve my code and design skills. Specifically, the Frontend Mentor community provided detailed critiques that guided me in refining the responsiveness and aesthetics of my project. The Stack Overflow community offered solutions and advice on implementing advanced CSS techniques, Redux for state management, and creating interactive React components. Their collective expertise greatly contributed to my learning and the overall success of this project.
```
