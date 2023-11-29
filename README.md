# Quiz App ReadMe

## Introduction
This ReadMe documents the functionalities and code structure of the Quiz App developed by Team5. This interactive platform enables users to participate in quiz activities, featuring topic selection, question-answering, and flashcard usage, coupled with robust user authentication.

### Version
- App Version: Final
- Last Updated: November 2023

## Key Features
- **User Authentication:** SignIn, SignUp, and SignOut using FirebaseAuth.
- **Topic Management:** Add, edit, and delete quiz topics.
- **Question Management:** Add, edit, and delete questions related to topics.
- **Flashcard Management:** Add, edit, and delete flashcards for study aids.
- **User Experience Enhancements:** Swipe-to-edit feature, improved animations, and bug fixes.

## Components
1. **LogViewController:** Manages user login and navigation to topic selection.
2. **RegisterViewController:** Handles user registration.
3. **UserService:** Provides core services for user data and Firestore interactions.
4. **AuthView:** Manages authentication state and data model interactions.
5. **FirebaseFile:** Configures Firebase services, including CRUD operations.

## Recent Updates
- Replaced screens for adding topics, questions, and flashcards with intuitive overlays.
- Added swipe-left feature in table views for editing topics and questions.
- Introduced a register button for new users.
- Addressed bugs in flashcard deletion and initial game experience.
- Enhanced flashcard animations for dynamic interaction.

## Code Snippets
### LogViewController.swift
- Manages user login, navigation, and error alert presentations.

### RegisterViewController.swift
- Handles new user registrations and post-registration navigation.

### UserService.swift
- Interacts with Firestore for CRUD operations on topics, questions, and flashcards.

### AuthView.swift
- Manages user session and authentication-related operations.

## TableFlashController and Overlay Views
### Overview
`TableFlashController` is integral to the app, managing the display and interaction with quiz topics. It incorporates `AddViewController` and `EditViewController` for adding and editing topics.

### TableFlashController
- **Functionality:** Displays and manages quiz topics in a table view.
- **User Interaction:** Implements sign-out, addition of new topics through an overlay, and swipe actions for editing and deleting topics.
- **Data Handling:** Dynamically fetches and updates data for synchronization with the backend.
- **Navigation:** Facilitates user movement to different app segments.

#### Key Methods
- `addTopic`: Initiates an overlay for adding new topics.
- `tableView`: Configures the table view's appearance and functionality.
- `handleTap`: Manages tap gestures for overlay dismissal.
- `didDismissOverlay`: Refreshes data post-overlay interaction.

### AddViewController
- **Purpose:** Overlay for adding new topics.
- **Design:** User-friendly interface with a topic input field and 'Done' button.
- **Interaction:** Captures and submits new topics to the backend.

### EditViewController
- **Purpose:** Overlay for editing topics.
- **Functionality:** Allows editing of topic names with backend update.
- **User Interface:** Includes a label, editing field, and 'Done' button.

### Usage
- **Adding Topics:** Presents `AddViewController` on tapping the add button.
- **Editing Topics:** Launches `EditViewController` via swipe actions.

## AddTopicViewController
### Overview
`addTopicViewController` facilitates adding new topics. It features a simple interface for users to submit new quiz topics.

### Functionality
- **User Interface:** Includes a field for topic title input.
- **Adding Topics:** Integrates with the backend for topic addition.
- **Navigation:** Redirects to `TableFlashController` post-topic addition.

#### Key Components
- `topicTitle`: Text field for topic name input.
- `addTopic`: Action to capture and submit the new topic.

### Usage
- **Primary Use:** Enables users to input and add new topics.
- **User Journey:** Navigates from `TableFlashController` to `addTopicViewController` for adding topics and then returns to update the topic list.

### Implementation
- **Segue Management:** Handles navigation and data refresh in `TableFlashController`.
- **Error Handling:** Provides feedback for issues during topic addition.

## Usage Instructions
1. **Authentication:** Use `LogViewController` for login and `RegisterViewController` for registration.
2. **Adding Content:** Employ overlays for new topics, questions, and flashcards.
3. **Editing Content:** Swipe left in the table view to edit topics and questions.
4. **Deleting Content:** Use `UserService` functions for content removal.

## Dependencies
- UIKit
- FirebaseAuth
- FirebaseFirestore

## Setup
1. Clone the repository.
2. Install dependencies via CocoaPods or manually.
3. Open the project in Xcode.
4. Run the app in a simulator or on a real device.

## Contribution
- For contributions, create a branch and submit a pull request for review.


## License
- This project is licensed under [appropriate license].

---

*This ReadMe is structured to provide a comprehensive overview of the Quiz App's features, structure, and instructions. Update this document as the app evolves.*
