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
- User: wants recipes tailored to dietary needs, allergies, and budget constraints.  
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



# Jenny Ibrahim Use Cases

- UC-05 create, edit, and organize recipes with Metadata
- UC-06 view recipe with steps, timers, nutritional info, and media
- UC-07 share recipes via generated links
- UC-08 convert units and standardize measurements across recipes

----------------------------------------------------------------------------------------

## UC-05 create, edit, and organize recipes with Metadata

**Primary actor:**
User (student/beginner cook)

**Stakeholders and interests:**
- User: wants to create and organize personal recipes with relevant metadata such as ingredients, equipment, and tags for easy retrieval.
- System: must store structured recipe data consistently and make it
  accessible for filtering and recommendations.

**Preconditions:**
- User has an existing profile and is logged into the system.
- The system is running and able to store recipe data.

**Main success scenarios:**
1. User opens the recipe creation page
2. System presents a structured form for entering recipe details
3. User enters the recipe name, ingredients, required equipment, and relevant tags
4. User submits the recipe
5. System validates the input for completeness and structure
6. System saves the recipe and associates it with the users profile
7. System confirms the recipe has been created

**Extension:**
5a. User submits incomplete or improperly formatted recipe data.
  - system highlights missing fields and prompts the user to correct them
3a. User wants to edit an existing recipe
  - system retrieves the stored recipe and allows the user to modify any field, then re-validates and saves the updated version.

**Special Requirements:**
Recipe metadata (ingredients, equipment, tags) must be stored in a structured format to support consistent filtering and search.

----------------------------------------------------------------------------------------

## UC-06 view recipe with steps, timers, nutritional info, and media

**Primary actor:**
User (student/beginner cook)

**Stakeholders and interests:**
- User: wants a clear, guided view of a recipe including step-by-step instructions, timers, nutritional information, and any associated media
- System: must present recipe content in a unified, readable, and interactive format

**Preconditions:**
- The recipe exists in the system
- User has access to the recipe viewing page
  
**Main success scenarios:**
1. User selects a recipe to view
2. System retrieves and displays the full recipe in a unified viewing module.
3. System presents step-by-step cooking instructions in sequential order.
4. System displays associated timers for relevant steps.
5. System shows nutritional information for the recipe.
6. System displays any associated media (e.g., photos or instructional images).

**Extension:**
4a. User activates a timer for a specific step.
  - System starts a countdown and notifies the user when the time has elapsed.
5a. Nutritional information is unavailable for the recipe.
  - System indicates that nutritional data is not available for that recipe.

**Special Requirements:**
The viewing module must present all recipe components (steps, timers, nutrition, media) in a consistent and organized layout.

----------------------------------------------------------------------------------------
## UC-07 share recipes via generated links

**Primary actor:**
User (student/beginner cook)

**Stakeholders and interests:**
- User: wants to share a recipe with others outside the application using a simple shareable link.
- System: must generate a stable, accessible link that allows external users to view the recipe without requiring an account.

**Preconditions:**
- The recipe exists in the system and belongs to the user's profile.
- User is logged into the system.

**Main success scenarios:**
1. User opens a recipe they own.
2. User selects the share option.
3. System generates a unique shareable link for the recipe.
4. System displays the link to the user for copying and external distribution.
5. User copies and shares the link externally.
6. External recipient opens the link and views the recipe in a read-only format.

**Extension:**
3a. The system fails to generate a link.
  - System notifies the user and prompts them to try again.
6a. The recipe has been deleted or made private after the link was generated.
  - System informs the external recipient that the recipe is no longer available.

**Special Requirements:**
Generated links must remain valid and point to consistent recipe data as long as the recipe exists in the system.

----------------------------------------------------------------------------------------
## UC-08 convert units and standardize measurements across recipes

**Primary actor:**
User (student/beginner cook)

**Stakeholders and interests:**
- User: wants ingredient measurements presented in a familiar or preferred unit system without manual conversion.
- System: must apply accurate unit conversions consistently across all recipe content.

**Preconditions:**
- The recipe contains ingredient measurements.
- The system has a unit conversion reference available.

**Main success scenarios:**
1. User opens a recipe containing ingredient measurements.
2. System detects the units used in the recipe.
3. User selects a preferred unit system (e.g., metric or imperial).
4. System converts all measurements in the recipe to the selected unit system.
5. System displays the updated measurements consistently throughout the recipe.

**Extension:**
4a. A measurement cannot be accurately converted (e.g., ambiguous unit).
   - System flags the measurement and displays the original value with a note.

3a. User does not select a unit preference.
  - System defaults to the unit system stored in the user's profile, or displays the recipe's original units if no preference is set.
  - 
**Special Requirements:**
Unit conversions must be accurate and applied uniformly across all ingredients and steps within a recipe, consistent with the non-functional requirement for data consistency and structured organization.

----------------------------------------------------------------------------------------



# Cooper Brown Use Cases

- UC-09 Authenticate User Account
- UC-10 Share Completed Meal Photos
- UC-11 Rate and Comment on Recipes
- UC-12 View Personalized Dashboard

----------------------------------------------------------------------------------------

## UC-9 Authenticate User Account (Cooper)

**Primary actor:**
User (student/beginner cook)

**Stakeholders and interests:**
- User: Sign into account more securely or verify they are who they say before doing something significant with the account (e.g deleting account)
- System: Checks that the user is who they say they are

**Preconditions:**
- The account being signed into exists

**Main success scenarios:**
1. User submits their information correctly
2. System generates 4 digit code
3. System sends the 4 digit code to a predetermined secure channel
4. System prompts the User to input a 4 digit code
5. User inputs code
6. System checks code against generated code and verifies before proceeding

**Extension:**
3a. Authentication channels
  - Can be predetermined to be a phone number or email address owned by the account owner
6a. Incorrect codes reject the action being taken

**Special Requirements:**
- N/A

----------------------------------------------------------------------------------------

## UC-10 Share Completed Meal Photos (Cooper)

**Primary actor:**
User (student/beginner cook)

**Stakeholders and interests:**
- User: Share pictures of their meal after it is cooked
- System: Have space to post completed meal pictures

**Preconditions:**
- There is a recipe to commit on

**Main success scenarios:**
1. Users clicks the share photo option under a recipe
2. The system prompts the user to take a picture to submit
3. The system uploads the picture into the gallery for the recipe
4. System updates gallery to show the new image at the front of the viewable section

**Extension:**
2a. Pictures
  - Can be done within app by accessing camera or gallery
3a. Show username on picture
  - Adds watermark with username of person posting the image on bottom
**Special Requirements:**
- Identify who posted the images and be able to see what the results look like for others

----------------------------------------------------------------------------------------

## UC-11 Rating and commenting system on recipes (Cooper)

**Primary actor:**
User (student/beginner cook)

**Stakeholders and interests:**
- User: ability to rate recipes and leave comments alongside the rating
- System: compile the ratings and displays the ratings

**Preconditions:**
- The User is signed in
- The recipe exists

**Main success scenarios:**
1. User clicks the "rate" button on the recipe
2. User is prompted to give a 1-5 star rating to the recipe and type a comment
3. system adds the star rating too the recipe's list of star ratings
4. the system adds the comment with a display of the star rating too the comments section

**Extension:**
3a. No preexisting ratings 
  - If no star rating list exists, one for the recipe is created

**Special Requirements:**
- display total rating for the recipe based on these ratings

----------------------------------------------------------------------------------------

## UC-12 View personalized dashboard (Cooper)

**Primary actor:**
User (student/beginner cook)

**Stakeholders and interests:**
User: Have an interactable space to navigate in
System: Present an interactable space for the User to navigate within

**Preconditions:**
- User has filled in the account information
- Other functions exist properly

**Main success scenarios:**
1. User logs into their account
2. Buttons and UI corresponding too other elements are generated and formatted
3. User selects option
4. System routes too the applicable use case for that option
**Extension:**
2a. Specifications
  - The specifications of such depend on the other use cases
  - Options include but are not limited too Recipe search, profile management, and recipe creation
**Special Requirements:**

----------------------------------------------------------------------------------------

## UC-13 Estimate Recipe Cost (Vanshika)

**Primary actor:**
User (student/beginner cook)

**Stakeholders and interests:**
User: wants step-by-step cooking instructions adjusted to their skill level.
System: must adapt instruction complexity dynamically.

**Preconditions:**
- User is logged in.
- User skill level is stored in the profile.
- The recipe exists.

**Main success scenarios:**
1. User opens a recipe.
2. User selects “Start Guided Cooking.”
3. System retrieves the user’s stored skill level.
4. System adjusts instruction detail accordingly:
  Beginner: includes detailed explanations and tips.
  Intermediate: includes moderate explanation.
  Advanced: concise instructions.
5. System displays the first step.
6. User confirms completion of each step.
7. System advances sequentially until recipe completion.
8. System marks recipe as completed in cooking history.

**Extension:**
3a. No skill level stored.
    - System defaults to beginner mode.
resumption
6a. User pauses the session.
    - System saves progress for later .

**Special Requirements:**
Instruction adjustments must occur instantly without noticeable delay.

----------------------------------------------------------------------------------------

## UC-14 Scale Recipe Serving Size (Vanshika)

**Primary actor:**
User (student/beginner cook)

**Stakeholders and interests:**
User: wants ingredient quantities recalculated automatically.
System: must ensure accurate proportional scaling.

**Preconditions:**
- Recipe includes ingredient quantities.
- Recipe includes default serving size.

**Main success scenarios:**
1. User opens a recipe.
2. System displays the default serving size.
3. User enters a new desired serving size.
4. System calculates scaling factor.
5. System recalculates ingredient quantities proportionally.
6. System updates displayed ingredient list.

**Extension:**
3a. User enters invalid input (zero, negative, non-numeric).
    - System prompts user to enter a valid number.

**Special Requirements:**
Scaling calculations must maintain mathematical accuracy and consistent formatting.

----------------------------------------------------------------------------------------
## UC-15 Customize Recipe Ingredients Within Cooking Flow (Vanshika)

**Primary actor:**
User (student/beginner cook)

**Stakeholders and interests:**
User: wants flexibility to modify ingredients during cooking.
System: must update recipe data dynamically.

**Preconditions:**
- Recipe exists.
- User is viewing the recipe (guided or standard view).

**Main success scenarios:**
1. User opens a recipe.
2. User selects an ingredient to modify.
3. User edits quantity, removes ingredient, or adds a new ingredient.
4. System validates the modification.
5. System updates ingredient list.
6. System updates related measurements or calculations if necessary.
7. User continues cooking with updated version.

**Extension:**
4a. Modification conflicts with dietary restrictions.
    - System warns the user but allows override.

3a. User cancels modification.
    - System retains original recipe data.

**Special Requirements:**
Modifications must not permanently alter the original stored recipe unless explicitly saved.

----------------------------------------------------------------------------------------

## UC-16 Track User Cooking History (Vanshika)

**Primary actor:**
User (student/beginner cook)

**Stakeholders and interests:**
User: wants to track completed recipes and modifications.
System: must store historical cooking activity.

**Preconditions:**
- User is logged in. 
- User has completed at least one recipe.

**Main success scenarios:**
1. User completes a recipe.
2. System records the completion event.
3. System stores associated data (date, modifications, ratings if provided).
4. User navigates to the “Cooking History” section.
5. System retrieves completed recipes.
6. System displays them in chronological order.
7. User selects a past recipe to review details.

**Extension:**
2a. User exits before marking completion.
    - System prompts user to confirm completion.
5a. No history exists.
    - System displays a message indicating no completed recipes.

**Special Requirements:**
Cooking history data must be associated only with the authenticated user account.

----------------------------------------------------------------------------------------
----------------------------------------------------------------------------------------
## UC-17 Search Recipes by Keywords (Ishita)


**Primary actor:**
User (student/beginner cook)


**Stakeholders and interests:**
-User: wants to quickly find recipes by typing words like an ingredient, dish name, or cuisine.
-System: must return accurate and relevant recipe results based on what the user typed.


**Preconditions:**
-The user has access to the application.
-The recipe database has recipes stored in it.


**Main success scenarios:**
1. User opens the recipe search page.
2. User types one or more keywords into the search bar (e.g., "pasta", "chicken soup").
3. System searches the recipe database for matches based on the keywords.
4. System displays a list of matching recipes to the user.
5. User selects a recipe from the results to view it.
**Extension:**
No recipes match the keywords.
      - System shows a message saying no results were found and  suggests trying different keywords.
2a. User submits an empty search.
     - System prompts the user to enter at least one keyword before searching.


**Special Requirements:**
Search results should appear quickly, within 200ms of the user submitting the query.


----------------------------------------------------------------------------------------
## UC-18 Apply Unified Recipe Filters (Ishita)


**Primary actor:**
User (student/beginner cook)


**Stakeholders and interests:**
- User: wants to narrow down recipe results using filters like available equipment, budget, dietary restrictions, and allergens.
- System: must apply all selected filters together and return only recipes that match every condition.


**Preconditions:**
- The user has access to the recipe search page.
- The recipe database is available.


**Main success scenarios:**
1. User opens the recipe search or filter page.
2. User selects one or more filters (e.g., no oven, budget under $10, gluten free, no nuts).
3. System applies all selected filters to the recipe database.
4. System displays only the recipes that pass all the chosen filters.
5. User browses the filtered results.


**Extension:**
4a. No recipes match all the selected filters.
System notifies the user and suggests removing one or more filters to see more results.


2a. User does not select any filters.
System displays all available recipes without filtering.
**Special Requirements:**
Filtered results should load within 200ms. All filters must work together at the same time, not one at a time.
----------------------------------------------------------------------------------------
## UC-19 Save and Manage Favorite Recipes (Ishita)


**Primary actor:**
User (student/beginner cook)


**Stakeholders and interests:**
User: wants to save recipes they like so they can find them again easily later.
System: must store the user's saved recipes and link them to their account.


**Preconditions:**
The user is logged into their account.
The recipe the user wants to save exists in the system.


**Main success scenarios:**
1. User opens a recipe they want to save.
2. User clicks the bookmark or favorite button on the recipe.
3. System saves the recipe to the user's favorites list.
4. System confirms the recipe has been saved (e.g., the bookmark icon changes).
5. User can go to their favorites section to view all saved recipes.
6. User can remove a recipe from their favorites by clicking the bookmark button again.


**Extension:**
3a. The recipe is already in the user's favorites.
System removes it from favorites (acts as a toggle).


5a. The user has no saved favorites yet.
System shows a message saying the favorites list is empty and suggests browsing recipes.


**Special Requirements:** Saved recipes must stay linked to the user's account and be accessible after logging out and back in.


----------------------------------------------------------------------------------------
## UC-20 View Ranked Search Results (Ishita)


**Primary actor:**
User (student/beginner cook)


**Stakeholders and interests:**
User: wants the most relevant and useful recipes to appear at the top of search results.
System: must rank recipes based on how well they match the user's search and profile.


**Preconditions:**
- The user has performed a recipe search.
- There are matching results available to display.


**Main success scenarios:**
1. User submits a recipe search (with or without filters).
2. System retrieves all matching recipes from the database.
3. System ranks the results based on factors like keyword match, user preferences, and ratings.
4. System displays the ranked list with the most relevant recipes at the top.
5. User scrolls through the results and selects a recipe.


**Extension:**
3a. All results have the same relevance score.
System falls back to sorting by recipe rating or most recently added.


2a. No results are found.
System displays a message and suggests adjusting the search or filters.


**Special Requirements:**
The ranking logic should factor in the user's stored preferences and dietary profile when available.


----------------------------------------------------------------------------------------
## UC-21 Generate Dynamic Shopping List(Isaac)

**Primary actor:**
User (student/beginner cook)

**Stakeholders and interests:**
User: wants an organized list of ingredients to buy based on selected recipes.
System: must accurately aggregate and calculate total ingredient quantities.

**Preconditions:**
User has selected recipes for upcoming meals.
Recipes contain structured ingredient data.

**Main success scenarios:**
User selects recipes for meals.
User triggers shopping list generation.
System aggregates all required ingredients.
System consolidates duplicate ingredients.
System displays the dynamic shopping list.

**Extension:**
3a. Recipe has missing ingredient quantity data. 
- System lists ingredient separately for manual verification.

**Special Requirements:**
Shopping list must update dynamically in real-time when recipes are added or removed.

----------------------------------------------------------------------------------------
## UC-22 Substitute Ingredients in Recipe (Isaac)

**Primary actor:**
User (student/beginner cook)

**Stakeholders and interests:**
User: wants to replace an ingredient. 
System: must calculate the correct quantity for the substitute.

**Preconditions:**
User is viewing a recipe.
Substitution logic data exists in the database.

**Main success scenarios:**
User selects an ingredient to substitute.
System displays a list of valid substitutions.
User selects a substitute.
System applies logic to calculate the correct quantity.
System updates the recipe with the new ingredient and quantity.

**Extension:**
2a. No valid substitutions exist. 
- System informs user that no verified substitutions are available.

**Special Requirements:**
Accuracy must ensure substitution logic and quantity adjustments work chemically and culinarily.

----------------------------------------------------------------------------------------
## UC-23 Estimate Recipe Cost(Isaac)

**Primary actor:**
User (student/beginner cook)

**Stakeholders and interests:**
User: wants to know the approximate cost of a recipe. 
System: must calculate pricing using predefined store data.

**Preconditions:**
Predefined store pricing data for ingredients is available.

**Main success scenarios:**
User opens a recipe.
System retrieves predefined store pricing data for ingredients.
System calculates total estimated cost.
System displays the estimated total cost.

**Extension:**
2a. Pricing data is missing for an ingredient. 
- System calculates partial cost and flags unpriced items.

**Special Requirements:**
Accuracy must rely on accurately verified pricing data for reliable cost estimates.

----------------------------------------------------------------------------------------
## UC-24 Suggest Ingredient and Equipment Alternatives (Isaac)

**Primary actor:**
User (student/beginner cook)

**Stakeholders and interests:**
User: needs workarounds for missing tools or ingredients. 
System: must provide viable alternatives using constraint optimization.

**Preconditions:**
User is viewing a recipe.
Equipment and alternative mapping constraints exist in the database.

**Main success scenarios:**
User indicates a missing piece of equipment or ingredient.
System runs constraint optimization against recipe requirements.
System identifies a feasible alternative technique or item.
System displays the alternative suggestions.

**Extension:**
3a. No feasible alternatives can be found. 
- System advises that the item is strictly required.

**Special Requirements:**
Accuracy must ensure constraint optimization logic does not result in failed recipes.


