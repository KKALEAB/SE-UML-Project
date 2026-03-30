# FirstPan Design Model Extraction
Source artifacts:
- Fully Dressed Use Cases
- Supplementary Specifications
- Conceptual Diagram

## Team Extraction Rules
- If a concept may overlap with another teammate’s concept, mark it as (shared class)

## Shared Candidate Classes & possibly shared Classes
- User
- UserProfile
- Recipe
- Ingredient
- kitchenEquipment
- Review
- CookingSession
- GroceryList (Possibly shared)
## Add methods only if supported by use cases


Member Sections
-------------------------------------------------------------------------

### Kaleab
# canidate Classes
* user (shared)
* userprofile (shared)
* Recipe (shared)
* KitchenEquipment
* BudgetConstraint
* recipeFilter (shared class)

## notes
* user profile includes user's dietary preference, budget, and allergies.
* kitchenEquipment is connected to UserProfile.
* RecipeFilter uses UserProfile data to filter recipes.
* BudgetConstraint alters filtering and grocery list generation.
* RecipeFilter may overlap with the search filter/system handled by      other team members.


-------------------------------------------------------------------------

### Jenny
_To be filled_

## notes

-------------------------------------------------------------------------
### Cooper
_To be filled_

## notes

-------------------------------------------------------------------------

### Vanshika
_To be filled_

## notes

-------------------------------------------------------------------------

### Ishita
_To be filled_

## notes

-------------------------------------------------------------------------

### Isaac
_To be filled_

## notes

-------------------------------------------------------------------------

#### Merge Review Notes
- Make sure not to create a new class if a shared class already covers the same meaning

### shared classes that shoud stay stingle
- user
- userprofile
- recipe
- Ingredient
- kitchenEquipment

### Concept that may merge later
- BudgetConstraint ->> UserProfile
- RecipeFilter ->> UserProfile
- GroceryList ->> shoppinglist
- CookingSession ->> CookingHistory
- Review may stay separate but must connect to user and recipe


-------------------------------------------------------------------------
