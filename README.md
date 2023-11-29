
# Quiz App ReadMe

## Introduction
This ReadMe documents the key functionalities and code structure of the Quiz App developed by Team5. The app offers an interactive platform for users to engage in quiz activities with features like topic selection, question-answering, flashcard usage, and user authentication.

### Version
- App Version: Final
- Last Updated: November 2023

## Key Features
- **User Authentication:** SignIn, SignUp, and SignOut functionalities created with firebaseAuth.
- **Topic Management:** Add, edit, and delete quiz topics.
- **Question Management:** Add, edit, and delete questions related to topics.
- **Flashcard Management:** Add, edit, and delete flashcards for study aids.
- **User Experience Enhancements:** Swipe-to-edit feature, improved animations, and bug fixes.

## Components
1. **LogViewController:** Handles user login and navigation to topic selection.
2. **RegisterViewController:** Manages user registration.
3. **UserService:** Core service layer for handling user data and Firestore interactions.
4. **AuthView:** Manages the authentication state and data model interactions.
5. **FirebaseFile:** Sets up Firebase services and authentication.

## Recent Updates
- Replaced traditional screens for adding topics, questions, and flashcards with more intuitive overlays.
- Implemented a swipe-left feature in table views for easier editing of topics and questions.
- Added a register button for new users.
- General bug fixes, including resolving issues with deleting flashcards and initial game bugs.
- Enhanced flashcard animations for a more dynamic user experience.

## Code Snippets
### LogViewController.swift
- Handles user login, navigation, and error alert presentations.

### RegisterViewController.swift
- Manages new user registrations and navigations post-registration.

### UserService.swift
- Facilitates interactions with Firestore for CRUD operations on topics, questions, and flashcards.

### AuthView.swift
- Manages user session and performs authentication-related operations.

## Usage Instructions
1. **Authentication:** Use `LogViewController` for login and `RegisterViewController` for new user registration.
2. **Adding Content:** Use overlays to add new topics, questions, and flashcards.
3. **Editing Content:** Swipe left on items in the table view to edit topics and questions.
4. **Deleting Content:** Utilize UserService functions to remove topics, questions, and flashcards.

## Dependencies
- UIKit
- FirebaseAuth
- FirebaseFirestore

## Setup
1. Clone the repository.
2. Install required dependencies via CocoaPods or manually.
3. Open the project in Xcode.
4. Run the app in a simulator or real device.

## Contribution
- For contributions, please create a branch and submit a pull request for review.

## License
- This project is licensed under [appropriate license].

---

*Note: This ReadMe is structured to provide a comprehensive overview of the Quiz App's functionalities, code structure, and usage instructions. It's recommended to update this document as the app evolves.*

