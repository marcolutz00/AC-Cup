# AC-Cup

Road to 1.0
Submission Deadline: Monday, January 29, 8 am

Alle notwendigen Bibliotheken sind in der requirements.txt Datei enthalten. -> `pip install -r requirements.txt`

Plan:
1. Datenbereinigung: 
    - ⬜️ Daten auslesen
    - ⬜️ Daten in einheitliches Format bringen
    - ⬜️ Daten bereinigen, Null-Werte beseitigen, andere Datentypen, etc.
    - ⬜️ Daten joinen und in einer Tabelle darstellen

2. Datenanalyse:
    - ⬜️ Daten visualisieren
    - ⬜️ Daten analysieren
    - ⬜️ Modelle erstellen und trainieren
    - ⬜️ Modelle testen und vergleichen
    - ⬜️ Modelle optimieren


Allgemein:
- recipes.csv: ontains 75,604 recipes generated by the LLM and suggested to the users. The recipes can be uniquely identified by the entry in the column RecipId. Note we consider a meal vegan if it does not contain any animal products and vegetarian if it
does not have any meat or fish.

- reviews.csv: includes the results of a short survey displayed to the users after suggesting new recipes. They could evaluate the difficulty of the recipe in a range from 1 (easy) to 5 (very difficult) and whether they like the recipe. The file contains 140,195 reviews.

- diet.csv: contains 271,907 entries about customers dietary preferences

- requests.csv: includes the users’ search filter to find new recipes. This table depicts the newly developed interface mentioned before. In the future, it should serve as the input to the recipe LLM. Overall, you obtained 140,195 requests.


Aufgabe:
Use these data sets to develop a model that can predict the outcome of the column Like, which
indicates whether a customer likes a recipe (your model predicts Like=1) or dislikes it (your model predicts
Like=0).
For reviews with a TestSetId and for which you are not given the Like (the “private test set”), you must make
predictions that will form your submission. See the “submission_template.csv” for details about the required
format. Your project will be evaluated and graded based on these predictions.

Zu predicten:
For reviews with a TestSetId and for which you are not given the Like (the “private test set”), you must make
predictions that will form your submission. See the “submission_template.csv” for details about the required
format. Your project will be evaluated and graded based on these predictions.



Aktuelle Modelle Marco - Best Scores:
- Linear Regression (19.01.2024) - WLS (Weighted Least Squares):
True Positives:  956
True Negatives:  5121
False Positives:  2977
False Negatives:  252
BAC:  0.7118845467526116

- Logistic Regression (19.01.2024)
True Positives:  758
True Negatives:  6076
False Positives:  2022
False Negatives:  450
BAC:  0.6888960809553173

