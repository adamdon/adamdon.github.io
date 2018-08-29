# Adam Don - projects, bits and pieces

A collection of projects I wanted to document to help keep track of what I've been working on.
 - [GitHub](https://github.com/adamdon)
 - [LinkedIn](https://www.linkedin.com/in/adam-don/)
 

## CaledonianOpticians
#### Customer Management Database

 - [Download .jar (unzip)](https://github.com/adamdon/CaledonianOpticians/releases/download/1.0/CaledonianOpticians1.0.zip)
 
![Screenshot of UI](/img/CaledonianOpticians_screenshot01.png)

Developed by myself as part of a larger 1st year project to create an appointments management tool that could make, update, search and store bookings. I was given a lot of freedom in what language and tools to be used, so I decided lean JavaFX using onlne resources and omit the use of any scene builders as coding the GUI would give better contol. 

The UI was coded with JavaFX nested gridpanes, the logic was implemented in the Controller class (using the Model–view–controller design) and the database utilised ObjectOutputStream with FileOutputStream to write the full array of objects to disk for persistence.

```markdown
public void handleBtnAppointmentRegister()
{
    isAppointmentModifyModeActive = false;
    clearAppointmentDetails();
    view.txtAppointmentRef.setText(Integer.toString(allAppointments.get(allAppointments.size() - 1).getIntAppointmentRef() + 1));
    appointmentDetailsMakeEditable();
    updateStatusBar("Type all Appointment details then Save");
}
```
 - [View Full Source (github)](https://github.com/adamdon/CaledonianOpticians/tree/1.0/src/caledonianopticians)




## TouristReviewsGlasgow
#### Android App with MySql login

 - [Download .apk](https://github.com/adamdon/TouristReviewsGlasgow/releases/download/1.0.0/app-debug.apk)
 
![Screenshot of UI](https://adamdon.github.io/img/TouristReviewsGlasgow_screenshot01.png)

I developed this project prior to university to implement a Database within an Android app. The UI was kept at a prototype stage using XML to position the layout, the DBHandler Class was used for CRUD functions and a database was created with SQLite.

```markdown
public void onCreate(SQLiteDatabase db)
{
    String CREATE_LOGIN_TABLE = "CREATE TABLE Login (Username TEXT PRIMARY KEY, PinNumber TEXT)";
    db.execSQL(CREATE_LOGIN_TABLE);

    String CREATE_PERSON_TABLE = "CREATE TABLE Person (Username TEXT PRIMARY KEY, Email TEXT)";
    db.execSQL(CREATE_PERSON_TABLE);
}

public void addLogin(Login login, SQLiteDatabase db)
{
    ContentValues values = new ContentValues();
    values.put("Username", login.getUsername());
    values.put("PinNumber", login.getPinNumber());
    db.insert("Login", null, values);
}
```
 - [View Full Source (github)](https://github.com/adamdon/TouristReviewsGlasgow/tree/master/app/src/main/java/uk/ac/cityofglasgowcollege/gccadamdon)
 
 
 
