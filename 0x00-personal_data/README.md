Personal Data
This project contains tasks for learning to protect a user's personal data.

Tasks To Complete
 0. Regex-ing
filtered_logger.py contains a function called filter_datum that returns the log message obfuscated with the following requirements:

  1. Log formatter
filtered_logger.py contains the following updates:

 2. Create logger
filtered_logger.py contains

Use user_data.csv for this task.

 3. Connect to secure database
filtered_logger.py contains the following updates:

INFO:Database credentials should NEVER be stored in code or checked into version control. One secure option is to store them as environment variable on the application server.

 4. Read and filter data
filtered_logger.py contains a main function that takes no arguments and returns nothing with the following requirements:

The function will obtain a database connection using get_db and retrieve all rows in the users table and display each row under a filtered format

 5. Encrypting passwords
encrypt_password.py contains a script that meets the following requirements:

INFO: User passwords should NEVER be stored in plain text in a database.

 6. Check valid password
app.py contains an is_valid function that expects 2 arguments and returns a boolean:
