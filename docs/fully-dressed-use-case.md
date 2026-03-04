# Kaleab Dessalegne Use Cases

- UC-01 Create and Manage User Profile
- UC-02 Manage Kitchen Equipment
- UC-03 Apply Personalized Recipe Filters
- UC-04 Configure Cooking Budget Constraints

-----------------------------------------------------------------------------

## UC-01 Create and Manage User Profile (kaleab)

**Primary Actor:**  
User (Student / Beginner Cook)

**Stakeholders and Interests:**  
- User: wants recipes tailored to dietary needs, allergies, and budget constraints  
- System: must store and apply preferences consistently when recommending recipes

**Preconditions:**  
- User has access to the application  
- The system is running and able to store user profile data

**Main Success Scenario:**
1. User opens the profile setup page.
2. System prompts user to enter dietary preferences, allergies, and budget constraints.
3. User inputs their preferences and confirms submission.
4. System validates the input data.
5. System stores the user profile information.
6. System confirms that the profile has been successfully saved.

**Extensions:**
- 4a. User enters invalid or incomplete information.  
  - System prompts user to correct the input before saving.

**Special Requirements:**  
- Profile data must be securely stored and retrievable during recipe filtering.

## UC-02 Manage Kitchen Equipment (kaleab)

**Primary Actor:**  
User (Student / Beginner Cook)

**Stakeholders and Interests:**  
- User: wants recipes that match the tools they actually have available  
- System: must accurately track available kitchen equipment to filter recipes

**Preconditions:**  
- User has an existing profile  
- User is logged into the system

**Main Success Scenario:**
1. User opens the kitchen equipment management section.
2. System displays a list of common kitchen tools.
3. User selects the tools they have available (e.g., stove, oven, pan, blender).
4. User saves the equipment list.
5. System stores the selected equipment in the user profile.
6. System uses the stored equipment to filter compatible recipes.

**Extensions:**
- 3a. User adds a custom tool not listed.  
  - System allows manual entry of additional equipment.

**Special Requirements:**  
- Equipment data should be stored and used during recipe recommendation and filtering.