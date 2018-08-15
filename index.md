## Adam Don - projects, bits and pieces

A collection of projects I wanted to document to help keep track of what I've been working on.
 - [GitHub](https://github.com/adamdon)
 - [LinkedIn](https://www.linkedin.com/in/adam-don/)

### CaledonianOpticians - Customer Management Database
![Screenshot of UI](/img/CaledonianOpticians_screenshot01.png)

Developed by myself as part of a larger 1st year project to create an appointments management tool that could make, update, search and store bookings.

The UI was make using a JavaFX gridpane, the logic was implemented in the Controller class (using the Model–view–controller design) and the database utilised ObjectOutputStream with FileOutputStream to write the full array of objects to disk for persistence.


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

 - [View Source (github)](https://github.com/adamdon)
 - [Download .jar (unzip)](https://www.linkedin.com/in/adam-don/)
