# FirstPan Design Model Extraction


## Source Artifacts

- Fully Dressed Use Cases

- Supplementary Specifications

- Conceptual Diagram


---


## Team Extraction Rules

- If a concept may overlap with another teammate’s concept, mark it as (shared class)


---


## Shared Candidate Classes & Possibly Shared Classes

- User

- UserProfile

- Recipe

- Ingredient

- KitchenEquipment

- Review

- CookingSession

- GroceryList (Possibly shared)


---


## Method Constraint

- Add methods only if supported by use cases


---


# Member Sections


---


## Kaleab


### Candidate Classes

- User (shared)

- UserProfile (shared)

- Recipe (shared)

- KitchenEquipment

- BudgetConstraint

- RecipeFilter (shared class)


---


### Candidate Attributes


#### User

- userID

- name

- email


#### UserProfile

- profileID

- dietaryPreferences

- allergies


#### KitchenEquipment

- equipmentID

- equipmentName

- equipmentType

- isCustom


#### BudgetConstraint

- budgetID

- maxBudget


#### RecipeFilter

- filterID

- dietaryPreferences

- allergies

- availableEquipment

- budgetLimit


#### Recipe

- recipeID

- title


---


### Candidate Relationships

- User ->> UserProfile (1..1)

- UserProfile ->> KitchenEquipment (1..*)

- UserProfile ->> BudgetConstraint (1..1)

- UserProfile ->> RecipeFilter (1..1)

- RecipeFilter ->> Recipe (*..*)

- Recipe ->> KitchenEquipment (*..*)

#### Class Diagram Ready Mapping

- User
- UserProfile
- KitchenEquipment
- BudgetConstraint
- RecipeFilter
- Recipe

---


### Notes

- UserProfile includes user's dietary preference, budget, and allergies

- KitchenEquipment is connected to UserProfile

- RecipeFilter uses UserProfile data to filter recipes

- BudgetConstraint alters filtering and grocery list generation

- RecipeFilter may overlap with the search filter/system handled by other team members


---


## Jenny


### Candidate Classes

_To be filled_


### Candidate Attributes

_To be filled_


### Notes


---


## Cooper


### Candidate Classes

_To be filled_


### Candidate Attributes

_To be filled_


### Notes


---


## Vanshika


### Candidate Classes

_To be filled_


### Candidate Attributes

_To be filled_


### Notes


---


## Ishita


### Candidate Classes

_To be filled_


### Candidate Attributes

_To be filled_


### Notes


---


## Isaac


### Candidate Classes

_To be filled_


### Candidate Attributes

_To be filled_


### Notes


---


## Merge Review Notes


### Shared Classes That Should Stay Single

- User

- UserProfile

- Recipe

- Ingredient

- KitchenEquipment


### Concepts That May Merge Later

- BudgetConstraint → UserProfile

- RecipeFilter → UserProfile

- GroceryList → shoppinglist

- CookingSession → CookingHistory

- Review may stay separate but must connect to User and Recipe