User Authentication Service
This project contains tasks for learning to create a user authentication service.

Requirements
SQLAlchemy 1.3.x
pycodestyle 2.5
bcrypt
python3 3.7
Tasks To Complete
 0. User model
user.py contains a SQLAlchemy model named User for a database table named users (by using the mapping declaration of SQLAlchemy) and meets the following requirements:

 1. create user
db.py contains a completion of the DB class provided below to implement the add_user method according to the given requirements:

 2. Find user
db.py contains the following updates:

Implement the DB.find_user_by method. This method takes in arbitrary keyword arguments and returns the first row found in the users table as filtered by the method’s input arguments. 

 3. update user
db.py contains the following updates:

Implement the DB.update_user method that takes as arguments a required user_id integer, an arbitrary keyword arguments, and returns None.

  4. Hash password
auth.py contains a _hash_password method that takes in a password string arguments and returns bytes, which is a salted hash of the input password, hashed with bcrypt.hashpw.

 5. Register user
auth.py contains the following updates:

Implement the Auth.register_user in the Auth class provided.

 6. Basic Flask app
app.py contains a basic Flask app with the following requirements:

Create a Flask app that has a single GET route ("/") and use flask.jsonify to return a JSON payload.

 7. Register user
app.py contains the following updates:

Implement the end-point to register a user. Define a users function that implements the POST /users route.

 8. Credentials validation
auth.py contains the following updates:

Implement the Auth.valid_login method. It should expect email and password required arguments and return a boolean.

 9. Generate UUIDs
auth.py contains the following updates:

Implement a _generate_uuid function in the auth module. The function should return a string representation of a new UUID. Use the uuid module.

 10. Get session ID
auth.py contains the following updates:

Implement the Auth.create_session method. It takes an email string argument and returns the session ID as a string.

  11. Log in
app.py contains the following updates:

Implement a login function to respond to the POST /sessions route.

 12. Find user by session ID
auth.py contains the following updates:

Implement the Auth.get_user_from_session_id method. It takes a single session_id string argument and returns the corresponding User or None.

 13. Destroy session
auth.py contains the following updates:

Implement Auth.destroy_session. The method takes a single user_id integer argument and returns None.

 14. Log out
app.py contains the following updates:

Implement a logout function to respond to the DELETE /sessions route.

 15. User profile
app.py contains the following updates:

Implement a profile function to respond to the GET /profile route.

 16. Generate reset password token
auth.py contains the following updates:

Implement the Auth.get_reset_password_token method. It takes an email string argument and returns a string.

 17. Get reset password token
app.py contains the following updates:

Implement a get_reset_password_token function to respond to the POST /reset_password route.

 18. Update password
auth.py contains the following updates:

Implement the Auth.update_password method. It takes reset_token string argument and a password string argument and returns None.

 19. Update password end-point
app.py contains the following updates:

Implement the update_password function in the app module to respond to the PUT /reset_password route.

 20. End-to-end integration test

Start the Flask app you created in the previous tasks. Open a new terminal window.
