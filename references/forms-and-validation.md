# Forms and Validation

## Before building
Identify required fields, optional fields, dependencies between fields, server rules, submission effects, and what must be preserved on failure.

## Field design
- Use explicit labels and concise helper text.
- Group fields in the order users need to answer them.
- Choose input types and autocomplete hints that match the data.
- Explain constraints before users encounter errors.
- Use conditional fields only when they reduce complexity; preserve values when hiding a field if the product's rules permit it.

## Validation
- Validate locally for speed and on the server for authority.
- Make errors specific, actionable, and adjacent to the relevant field.
- Move focus appropriately for submission errors without causing confusing jumps.
- Avoid showing every error before the user has had a reasonable chance to enter data.
- Do not silently discard user input after server errors.

## Submission lifecycle
Model idle, submitting, success, failure, and retry. Prevent duplicate submissions where necessary. Tell users what was saved and what remains unsaved. Do not display success until the operation has actually succeeded.

## Verification cases
Test valid data, missing required fields, invalid formats, server rejection, network failure, repeat submission, keyboard navigation, and mobile viewport behavior.
