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
- install intl package for localization and date formate where here we target date format `flutter pub add intl`

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
- expand widget solve problem of overlapping and fits the elements widgets inside
- we can use `showmodalbotomsheet` and other show methods from flutter to show modal and calender and so on from autocomplete we can checkn these show function
- context is widget of meta data informatiuon passed through the widgets and overdf all UI 
- for builder function it expoects to return widget
- `EditTextController widget` is used to save input or titles field so for many fields we need many controllers and we have to dispose or terminate the value of this controllers when close the `overlay modal`
- check the code
```sh
Navigator.pop(context);
```
- used to exist the overlay widget
- check the code
```sh
DropdownButton(
                value: _selectedCategory,
                items: Category.values
                    .map(
                      (category) => DropdownMenuItem(
                        value: category,
                        child: Text(
                          category.name.toUpperCase(),
                        ),
                      ),
                    )
                    .toList(),
                onChanged: (value) {
                  if (value == null) {
                    return;
                  }
                  setState(() {
                    _selectedCategory = value;
                  });
                },
              ),
```
- Category.values returns all enum words and then tolist convert to array so map can work
- compiningh condition with and or
- validating user input and showing an error dialog
- saving new expenses
- creating full screen modal
- using the dismissable widget for dismissing list items
- showing and managing snackbar
- 