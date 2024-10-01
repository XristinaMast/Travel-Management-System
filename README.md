# Travel-Management-System


This is a simple **C-based travel management system** that allows users to register, login, and track their trips to different destinations. The program manages user data including personal information, trip counts to various destinations, and generates usernames and passwords. It also supports functionalities like modifying user details, searching, sorting, and viewing all users' data.

## Features

- **User Registration**: Allows up to 100 users to register with personal information and the number of trips to different destinations.
- **Login**: Users can log in using a username and password generated during registration.
- **Modify User Data**: Users can update personal information like name, age, and trip counts.
- **Password Change**: Users with more than 20 trips can modify their passwords.
- **View User Data**: Displays all registered users and their data in tabular form.
- **Search by Trip Count**: Search for users by the total number of trips.
- **Sort Users**: Sorts and displays users based on the total number of trips in descending order.

## How It Works

### Main Functions

1. **Register**: Collects user details such as name, surname, age, and the number of trips to three destinations: Lamia, Patra, and Volos. After registration, a username and password are generated for the user.

2. **Login**: Prompts the user to enter their username and password to log in. It checks the credentials from previously registered users.

3. **Screen_traveller**: After logging in, users can:
   - Modify personal data.
   - Change their password.
   - View their or others' information.
   - Search for users by trip count.
   - Sort the list of users by the total number of trips.

4. **Modify**: Allows users to update their personal information like surname, name, age, and trip counts to Lamia, Patra, and Volos.

5. **Pass**: Enables users to change their password if they have more than 20 total trips. It subtracts 5 random trips before allowing the password change.

6. **View**: Displays all registered users and their details such as name, surname, age, and trip counts.

7. **Search**: Searches for users with a specific number of total trips.

8. **Sort**: Sorts and displays users based on the total number of trips in descending order.

### Data Structure

- The system uses two 2D arrays `a[100][7][100]` and `lg[100][2][50]`.
  - `a[][][]` stores user information including personal details and trip counts.
  - `lg[][]` stores usernames and passwords for login purposes.
  
- Additionally, `su[]` keeps track of the total number of trips for each user.

### Running the Program

To run the program:
1. Compile the C file:
   ```bash
   gcc travel_management.c -o travel_management
   ```
2. Execute the program:
   ```bash
   ./travel_management
   ```

The program will prompt whether you want to register or login. After login, you can modify data, change the password, view, search, or sort user information.

### Example Interaction

1. **Register a New User:**
   - Input personal data such as surname, name, age, and trips to different destinations.
   - Get a generated username and password.

2. **Login**:
   - Use the username and password from registration to log in.

3. **Choose Options**:
   - Modify personal data.
   - View or sort other users.
   - Change password if eligible (more than 20 trips).
