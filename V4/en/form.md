# Fill-in forms

Use fill-in forms to collect data during your presentation. Answers are stored on the computer. 

## Interactions in the Compositeur Digital

On fill-in forms, you can:
- Key in text in dedicated fields using a physical or virtual keyboard
- Toggle checkboxes to answer multiple-choice questions or select a value from a range of options
- Press the `Save` button on the bottom right to save the data on the computer and reset the form

![Aperçu du formulaire](img/form_preview.jpg)

## Content management

- Folder extension : `form`
- optional '_background' image file for customizing the form 
- form specification file in the folder: `_questions.csv`

The form specification file is a CSV file (*comma-separated values* with `;` as delimiter): it is editable with any spreadsheet application such as Microsoft Excel.
This file will describe the list of questions that will appear in the form. One line describes one question at a time

Here is a example of file for the form displayed above:

![Aperçu du fichier _questions.csv](img/form_csv.jpg)

### Line formatting:

- 1st cell: question type
- 2nd cell: question 
- following cells: possible answers for multiple-choice questions

### Answer types

- `text`: for questions requiring text entries using the physical or virtual keyboard
- `single`: for questions allowing one answer at a time   
- `multiple`: for questions allowing multiple answers 

### Results

Results are saved on disk in the `Documents \ Compositeur Digital Form` folder.	
In this file a line with all answers is added each time the `Save` button in pressed in the form.

[Back to supported types](content_types.md)
