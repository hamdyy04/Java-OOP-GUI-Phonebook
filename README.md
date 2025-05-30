# Java-OOP-GUI-Phonebook
This Java application demonstrates object-oriented programming (OOP) principles by encapsulating contact management functionality within a class. Users can add, edit, delete, and clear contacts in a table.

![cMtxo5ysNc](https://github.com/user-attachments/assets/514b9e48-cd23-4597-852e-c55826860091)

# Class Definition
```java
public class jframe1 extends javax.swing.JFrame {
```
The `jframe1` class extends `javax.swing.JFrame`, making it a Swing frame (window) that can contain other Swing components.

# Instance Variables
```java
private DefaultTableModel tableModel;
```
`tableModel` is an instance of `DefaultTableModel`, which is used to manage the data displayed in the `JTable`.

# Constructor
```java
public jframe1() {
    initComponents();
    tableModel = new DefaultTableModel(new Object[][] {}, new String[]{"Name", "Email", "Phone"});
    jTable1.setModel(tableModel);
}
```
The constructor initializes the components of the frame and sets up the table model with columns "Name", "Email", and "Phone".

# initComponents Method
```java
private void initComponents() {
    // Component initialization code
}
```
This method is auto-generated by the NetBeans IDE and contains the code to initialize and layout the GUI components. It includes labels, text fields, buttons, and a table.

# Action Listeners
The code defines several action listeners for the buttons:

# Add Button
```java
private void AddActionPerformed(java.awt.event.ActionEvent evt) {
    String name = jTextField1.getText();
    String email = jTextField2.getText();
    String phone = jTextField3.getText();
    // Validation and adding a row to the table
}
```
This method retrieves the text from the input fields, validates it, and adds a new row to the table if the input is valid.

# Edit Button
```java
private void EditActionPerformed(java.awt.event.ActionEvent evt) {
    int selectedRow = jTable1.getSelectedRow();
    // Load selected row data into input fields
}
```
This method loads the data from the selected row in the table into the input fields for editing.

# Clear All Button
```java
private void ClearAllActionPerformed(java.awt.event.ActionEvent evt) {
    tableModel.setRowCount(0);
    clearFormFields();
}
```
This method clears all rows from the table and resets the input fields.

# Delete Button
```java
private void DeleteActionPerformed(java.awt.event.ActionEvent evt) {
    int selectedRow = jTable1.getSelectedRow();
    // Remove selected row from table
}
```
This method deletes the selected row from the table.

# Confirm Edit Button
```java
private void ConfirmEditActionPerformed(java.awt.event.ActionEvent evt) {
    int selectedRow = jTable1.getSelectedRow();
    // Update selected row with new data from input fields
}
```
After validation, this method updates the selected row in the table with the data from the input fields.

# Validation Methods
The code includes methods to validate the input fields:

# Email Validation
```java
private boolean isValidEmail(String email) {
    String emailRegex = "^[a-zA-Z0-9_+&*-]+(?:\\.[a-zA-Z0-9_+&*-]+)*@(?:[a-zA-Z0-9-]+\\.)+[a-zA-Z]{2,7}$";
    return email.matches(emailRegex);
}
```
This method checks if the email matches a regular expression pattern.

# Phone Validation
```java
private boolean isValidPhone(String phone) {
    String phoneRegex = "^(010|011|012|015)[0-9]{8}$";
    return phone.matches(phoneRegex);
}
```
This method checks if the phone number matches a specific pattern for Egyptian mobile numbers (010,011,012,015).

# Name Validation
```java
private boolean isValidName(String name) {
    String nameRegex = "^[a-zA-Z\\s]+$";
    return name.matches(nameRegex);
}
```
This method checks if the name contains only letters and spaces

# Utility Method
```java
private void clearFormFields() {
    jTextField1.setText("");
    jTextField2.setText("");
    jTextField3.setText("");
}
```
This method clears the text fields.

# Main Method
This code provides a basic contact management application with a GUI, allowing users to perform CRUD (Create, Read, Update, Delete) operations on a contacts list
```java
contacts.private boolean isValidName(String name) {
    String nameRegex = "^[a-zA-Z\\s]+$";
    return name.matches(nameRegex);
}
```
This method checks if the name contains only letters and spaces.

This code provides a basic contact management application with a GUI, allowing users to Create, Read, Update, Delete operations on a list of contacts.
