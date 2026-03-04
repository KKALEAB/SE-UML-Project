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


## UC-03 Apply Personalized Recipe Filters (kaleab)

**Primary Actor:**  
User (Student / Beginner Cook)

**Stakeholders and Interests:**  
- User: wants recipes that match their dietary preferences, allergies, available equipment, and budget.
- System: must filter recipes accurately using the user’s stored profile information.

**Preconditions:**  
- User has an existing profile with preferences and equipment stored.
- The recipe database is available.

**Main Success Scenario:**
1. User opens the recipe search page.
2. System retrieves the user's stored preferences (dietary restrictions, allergens, equipment, and budget).
3. User initiates a recipe search.
4. System filters recipes based on the user’s stored profile constraints.
5. System displays the filtered recipe results to the user.

**Extensions:**
- 2a. User has no preferences stored.  
  - System displays recipes without applying filters.
- 4a. No recipes match the filters.  
  - System informs the user and suggests relaxing some constraints.

**Special Requirements:**  
- Filtering results should be fast and responsive (consistent with performance requirements).

## UC-04 Configure Cooking Budget Constraints(kaleab)

**Primary Actor:**  
User (Student / Beginner Cook)

**Stakeholders and Interests:**  
- User: wants recipes that stay within a specified ingredient budget.
- System: must apply the user’s budget constraints when filtering and recommending recipes.

**Preconditions:**  
- User has an existing profile.
- Recipe ingredient price estimates are available in the system.

**Main Success Scenario:**
1. User opens the budget settings section in their profile.
2. System prompts the user to enter a preferred ingredient budget limit.
3. User enters the desired budget amount.
4. System validates the input.
5. System saves the budget constraint to the user profile.
6. System applies the budget constraint when filtering recipes.

**Extensions:**
- 4a. User enters an invalid or negative budget value.  
  - System prompts the user to correct the input before saving.

**Special Requirements:**  
- Budget constraints should be applied automatically when generating recipe recommendations and grocery lists.