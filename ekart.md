# E-Kart — Product Brief

**Portfolio:** [Home](index.html) · [Promo](ekart-promo.html) · [Case Study](ekart-case-study.html) · [Mockups](ekart-mockups.html) · [System Design](ekart-system-design.html) · [App Flow](ekart-app-flow.html)

---

App Title: E-Kart
App Description: E-Kart is a ios/android app for filipino grocery, creating checklist and capturing the items in the cart. a dedicated catalog to check the price of a desired items in all available grocery stores.

Screens:

- On-boarding Screen (3 slides)
- Login Screen
- Home Screen
  - Show the analytics of the user's shopping behavior and a dedicated footer for displaying promos across the groceries.
- Checklist
  - Create a master checklist, tapping on it will open a screen where user can add items to the checklist.
  - Each Item has a camera on right side, tapping on it will open a camera screen where user can capture the item.
  - The camera will extract the item price and user can input the quantity then user can tap the save.
  - After tapping on the save, the image will be added on the item on the checklist and have a price tag on the right side.
  - User can swipe left to display edit and delete button.
  - User can input the estimated budget for the checklist.
  - User can see the actual cost of the checklist.
  - User can share the checklist to other users.
- Catalog
  - A dedicated catalog to check the price of a desired items in all available grocery stores.
  - The list view will display the grocery store and the equivalent item on the user search.
- Forum
  - A forum similar to reddit, user can post a topic and other users can comment on it.
  - User can upvote or downvote the post.
  - User can join a subforum to discuss a specific topic.
  - User can create a subforum to discuss a specific topic.
  - User can join a subforum to discuss a specific topic.
- Profile
  - User can view their profile and their activity.
  - User can view their forum posts and comments.
  - User can edit a generated alias name.
  - Alias name is shown on the forum posts and comments.
  - User can change password, email, and phone number.
  - User can delete their account.
- Settings
  - User can change the language of the app.
  - User can change the theme of the app (light and dark mode).

Features:

- Camera OCR to extract the item price.
- Camera to capture the item.
- Forum post and comment.
- Subforum post and comment.
- Profile and activity.
- Alias name.
- Password, email, and phone number.
- Delete account.
- Language and theme.

Tech Stack: - Frontend: - React Native - GlueStack - Zustand - TypeScript - Backend: - NestJS - Authentication - Checklist Creation - Forum Post and Comment - Subforum Post and Comment - Profile and Activity - Alias Name - Password, Email, and Phone Number - Delete Account - Language and Theme - FastApi - Catalog Search - Database - MongoDB

Architecture:

- MVVM
- Clean Architecture
- No over-engineering, keep it simple and clean.

Note:
Create the specs files in format ex. 01-project-setup, first phase of development should focus on the frontend. backend is the second phase.
