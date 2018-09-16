# ANA215 App

## Description
The purpose of this app is to provide a range of your exam mark prediction based on your semester results.
ANA215 - Inrtoduction to Paleoanthropology - is the subject on which this app is based, the model used to predict the exam mark, is a Gradient Boosting Model.

## Input
Input required for the app includes the following:
- "Are you repeating this subject?", an indicator of Y/N for whether or not you are repeating this subject
- "Did you miss any of the practicals?", an indicator of Y/N for whether you have missed any of the practical sessions
- "How many lectures did you miss?", a numerical input on the number of lectures you missed
- "Click-up Test 1 (/20)", a numerical input of your mark out of 20 in Click-up test 1
- "Click-up Test 2 (/20)", a numerical input of your mark out of 20 in Click-up test 2
- "Click-up Test 3 (/20)", a numerical input of your mark out of 20 in Click-up test 3
- "Click-up Test 4 (/20)", a numerical input of your mark out of 20 in Click-up test 4
- "Click-up Test 5 (/20)", a numerical input of your mark out of 20 in Click-up test 5
- "Hardy Weinberg (/49)", a numerical input of your mark out of 49 for the Hardy Weinberg assignment
- "Hominin Watch (/100)", a numerical input of your mark out of 100 for the Hominin Watch assignment
- "Lonely Fossils Abstract (/10)", a numerical input of your mark out of 10 for the Lonely Fossils abstract
- "Lonely Fossils Presentation (/30)", a numerical input of your mark out of 30 for the Lonely Fossils presentation
- "Human Variation (/100)", a numerical input of your mark out of 100 for the Human Variation assignment
- "Semester Test 1 (/40)", a numerical input of your mark out of 40 for Semester test 1
- "Semester Test 2 (/70)", a numerical input of your mark out of 70 for semester test 2

## Output
The output of the app includes 3 components.

### Subjects Marks
A table that includes a summary of your semester marks.
It includes the following breakdown of your semester marks:
- "Click-up Mark", the total mark for all the Click-up tests
- "Assignments", the total mark for all the assignments
- "Semester Test 1", the mark for Semester Test 1
- "Semester Test 2", the mark for Semester Test 2
- "Module Mark", the total mark for the semester that includes Click-up Mark, Assignments, Semester Test 1 and Semester Test 2

The table includes the following columns:
- "Part", to indicate which part of the semester marks
- "Weight", the weight the part contributes to the Module Mark
- "Mark", the mark for the particular part
 
### Exam Prediction (Text)
The exam prediction text displays the exam status and a range of the precition for the exam mark.
The exam status can either be one of the following:
- "Your exam mark would likely be in the range of", this incidates that you have qualified for exam entry and are required to attend the exam
- "Promoted, you do not need to write exam, but if you did your exam mark would be in the range of", this incidates that the module mark was above 65% and that no praticals were missed. Which means that exam attendance is not required
- "Module mark is too low for exam admission, but if you did your exam mark would be in the range of", this incidates that the module mark was below 40%, which means that exam attendance is not permitted

### Exam Prediction (Graph)
The graph displays the exam prediction range compared to a normal distribution fit of exam marks previously achieved by learners.
The first black line displays the lower limit of the range and the second black line displays the median of the range and the third black line displays the upper limit of the range.

Do note the following:
- The exam mark prediction is out of 100
- The range is based on the prediciton and the absolute average error of the predictions against the actuals from the input data that was used to fit the model
- Continued from the previous point, this means that the range does not include the only possibilities based on the input variables
- Due to year on year changes to the module, the model might not be callibrated towards these changes

