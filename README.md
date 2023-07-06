# expense_tracker

A new Flutter project.

## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://docs.flutter.dev/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://docs.flutter.dev/cookbook)

For help getting started with Flutter development, view the
[online documentation](https://docs.flutter.dev/), which offers tutorials,
samples, guidance on mobile development, and a full API reference.

# Objectives
- Making Apps more interactive and easier
- Using Modals Dialogs and more
- Basic User input handling
- Configuring and using Apps

# Install
- 'flutter pub add name ofpackage' here we need to add uuid so `flutter pub add uuid` if `google_fonts` just replace it with uuid 
- uuid package generates ids

# Note 
- check next code 
```sh
class Expense {
  Expense({
    required this.title,
    required this.amount,
    required this.date,
    required this.category,
  }) : id = uuid.v4();
```
- where ` : id = uuid.v4();` is called initailizer which is dart feature in class when add after constructor it initilize the code required
- ListView can replace the map where it allows item builder that can loop over list by its index 