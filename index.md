## Adam Don - projects, bits and pieces

A collection of projects I wanted to document to help keep track of what I've been working on.
 - [GitHub](https://github.com/adamdon)
 - [LinkedIn](https://www.linkedin.com/in/adam-don/)

### CaledonianOpticians - Customer Management Database
![Screenshot of UI](/img/CaledonianOpticians_screenshot01.png)

Developed by myself as part of a larger 1st year project to create an appointments management tool that could make, update, search and store bookings.

The UI was make using a JavaFX gridpane, the logic was implemented in the Controller class (using the Model–view–controller design) and the database utilised ObjectOutputStream with FileOutputStream to write the full array of objects to disk for persistence.


```markdown
code snippet:

    public void handleBtnAppointmentRegister()
    {
        isAppointmentModifyModeActive = false;
        clearAppointmentDetails();
        view.txtAppointmentRef.setText(Integer.toString(allAppointments.get(allAppointments.size() - 1).getIntAppointmentRef() + 1));
        appointmentDetailsMakeEditable();
        updateStatusBar("Type all Appointment details then Save");
    }
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/adamdon/adamdon.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
