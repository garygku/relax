# Relax Results

In order to find whether there is any relation between the variables provided and whether or not a user a user is ‘adopted’ according to the definition given, the following steps were taken:

1. The user and user engagement tables were both imported into the workspace.
2. A binary ‘adopted’ column was added to the user engagement table describing  whether the user had at least one 7-day period where they logged in 3+ times or not.
3. The user engagement table was grouped by the user id column then outer joined with the user table to form a comprehensive data frame.
4. The invited by column was transformed into a binary column describing whether or not the user was invited by another user.
5. The creation source column was transformed into a series of binary dummy variables.
6. The creation time and user id columns were dropped as well as any rows with missing data.
7. SMOTE was used to balance the data frame.
8. A  logistic regression model was run yielding an accuracy of .536.
9. A  KNN model was run yielding an accuracy of .510.
10. A  random forest model was run yielding an accuracy of .541.

Overall no significant results were found suggesting that there is little to no relation between the given variables and whether or not a user a user is ‘adopted’.
