You have an ordinal categorical feature (e.g., high, medium, low) and you want to transform them into
numerical values.Use pandas DataFrame’s replace method to transform string labels to numerical equivalents Often we have a feature with classes that have some kind of natural ordering. A famous example is the
Likert scale Likert scale:
Strongly Agree
Agree
Neutral
Disagree
Strongly Disagreeو When encoding the feature for use in machine learning, we need to transform the ordinal classes into
numerical values that maintain the notion of ordering. The most common approach is to create a
dictionary that maps the string label of the class to a number and then apply that map to the feature.
It is important that our choice of numeric values is based on our prior information on the ordinal classes.
In our solution, high is literally three times larger than low. This is fine in many instances, but can
break down if the assumed intervals between the classes are not equal  the distance between Low and Medium is the same as the distance between Medium and
Barely More Than Medium, which is almost certainly not accurate. The best approach is to be
conscious about the numerical values mapped to classes
