# 🛒 Redux Shopping App

This project is a **React + Redux Toolkit Shopping Cart App** built for understanding key Redux concepts including:

- Redux & React-Redux Basics
- Advanced Redux Toolkit
- Async Redux (Side Effects, Thunks)
- Backend communication using Firebase
- Error handling and notifications

---

## 📦 Features Implemented

### 1. Shopping Page App Using Reducers

📌 **Tasks Completed:**
- Used `react-redux` and `@reduxjs/toolkit`
- Created cart UI that toggles visibility on clicking `My Cart` button (via `cartReducer`)
- Implemented a UI toggle slice to manage cart display state

🟢 **Commit ID:** `first-task-commit-id`

69eb34d

### 2. Add to Cart Fixes

🛠️ **Tasks Implemented:**
- Items with quantity `0` are automatically removed from cart
- Cart icon updates with total item count on addition/removal
- When an item is added again, quantity increases instead of duplicating
- User can increase or decrease quantity within cart
- All cart items are dynamically displayed in the cart view

🟢 **Commit ID:** `second-task-commit-id`

c982b72

### 3. Network Calls and Handling Responses

🧠 **Learnings:**
- Async code should be handled in:
  - Component’s `useEffect`
  - Redux thunk/action creators
- Avoid direct mutation like `cart.totalQuantity += 1` in reducers
- PUT is used instead of POST to **replace** entire cart data

📌 **Tasks Completed:**
- Displayed notifications during:
  - Sending (`status: pending`)
  - Success (`status: success`)
  - Error (`status: error`)
- Used existing `Notification` component from `UI/`
- Managed `notification` state inside `uiSlice`
- Prevented sending request on first render (using `useRef` and `useEffect`)
- Applied best practices in data handling

🟢 **Commit ID:** `third-task-commit-id`

fe4b7e0

### 4. Fixing the Cart Problems (Data Persistence on Reload)

🧠 **Learnings:**
- Thunk action creator allows us to perform async logic (like fetching/saving data) inside Redux
- Makes the Redux store cleaner and more reusable

📌 **Tasks Completed:**
- On page load, fetched previously saved cart data via `GET` request to Firebase
- Managed loading, success, and error states using Redux and showed them via `Notification` component
- Used `thunk` middleware for both `sendCartData` and `fetchCartData` logic

🟢 **Commit ID:** `fourth-task-commit-id

d28a3a4

## 💡 Technologies Used

- **React**
- **Redux Toolkit**
- **React Redux**
- **Thunk Middleware**
- **Firebase Realtime Database** for backend
- **CSS Modules** for styling

---

## 🧠 Learning Outcomes

- Complete understanding of state management using Redux Toolkit
- Writing clean reducers and actions with `createSlice`
- Managing UI state like notifications elegantly
- Avoiding side-effects inside components using thunk-based async logic
- Best practices in structuring a Redux-powered app
