# Example Form

## General Information
### Facility name

| type          | name   | text                 | relevance | constraint | required | repeated |
|---------------|--------|-----------------------|-----------|----------|-----------|---------|
| text          | name  | What is the name of the facility? | | yes | no |

Other relevant information.

Options: (if required).


# Details

This form is originally written in markdown, see example.md for a template. The form uses the heading hierarchy to separate out forms (heading 1), groups (heading 2), and questions (heading 3).  

type: A question type using the types listed at [xlsform](https://xlsform.org/en/#question-types)

name: The variable name to appear in the database

text: The text as it appears on the form

relevance: If this question is condition on the response(s) to another question then these conditions should be provided here. Refer to the conditional questions by their name. For example, age >= 5, services == "other".

constraint: If there are restrictions on the value that can be input, add them here. For example, if the variable is age we might add <=100.

required: If "yes" then this question cannot be skipped. Otherwise it may be skipped without a response.

repeated: If multiple entries are required or not, for example if listing multiple family members, then this question can be repeated.

options: If the question has a range of possible responses, like select_one or select_multiple, then list the responses here. 

There are lots of other constraints, information, or conditioning that can be applied to a form. Please describe these within the relevant questions or groups.




