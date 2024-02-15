Session Authentication
This project contains tasks for learning to authenticate a user through session authentication.

Tasks To Complete
 0. Et moi et moi et moi!

Copy all your work of the 0x06. Basic authentication project in this new folder.

1. Empty session

Create a class SessionAuth in api/v1/auth/session_auth.py that inherits from Auth. For the moment this class will be empty.

 2. Create a session

Update SessionAuth class:
Create a class attribute user_id_by_session_id initialized by an empty dictionary.

 3. User ID for Session ID

Update SessionAuth class:
Create an instance method def user_id_for_session_id(self, session_id: str = None) -> str: that returns a User ID based on a Session ID:
Return None if session_id is None.

 4. Session cookie

Update api/v1/auth/auth.py by adding the method def session_cookie(self, request=None): that returns a cookie value from a request:
Return None if request is None.

 5. Before request

Update the @app.before_request method in api/v1/app.py:
Add the URL path /api/v1/auth_session/login/ in the list of excluded paths of the method require_auth - this route doesn't exist yet but it should be accessible outside authentication.

 6. Use Session ID for identifying a User

Update SessionAuth class:

Create an instance method def current_user(self, request=None): (overload) that returns a User instance based on a cookie value:

You must use self.session_cookie(...) and self.user_id_for_session_id(...) to return the User ID based on the cookie _my_session_id.

 7. New view for Session Authentication

Create a new Flask view that handles all routes for the Session authentication.
In the file api/v1/views/session_auth.py, create a route POST /auth_session/login (= POST /api/v1/auth_session/login):
Slash tolerant (/auth_session/login == /auth_session/login/).

 8. Logout

Update the class SessionAuth by adding a new method def destroy_session(self, request=None): that deletes the user session / logout:
If the request is equal to None, return False.

 9. Expiration?

Actually you have 2 authentication systems:
Basic authentication.
Session authentication.

 10. Sessions in database

Since the beginning, all Session IDs are stored in memory. It means, if your application stops, all Session IDs are lost.
