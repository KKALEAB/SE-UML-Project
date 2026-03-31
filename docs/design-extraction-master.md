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
- kitchenEquipment
- Review
- CookingSession
- GroceryList (Possibly shared)

---

## Add Methods Only If Supported by Use Cases

---

# Member Sections

---

## Kaleab

### Candidate Classes
- user (shared)
- userprofile (shared)
- Recipe (shared)
- KitchenEquipment
- BudgetConstraint
- recipeFilter (shared class)

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
- dietarypreferences
- allergies
- availableEquipment
- budgetLimit

#### Recipe
- recipeID
- title

### Notes
- user profile includes user's dietary preference, budget, and allergies
- kitchenEquipment is connected to UserProfile
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
- user
- userprofile
- recipe
- Ingredient
- kitchenEquipment

### Concepts That May Merge Later
- BudgetConstraint → UserProfile
- RecipeFilter → UserProfile
- GroceryList → shoppinglist
- CookingSession → CookingHistory
- Review may stay separate but must connect to user and recipe