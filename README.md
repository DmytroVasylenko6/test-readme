# CLI Personal Assistant

## Description
A CLI organizer that can help store contacts' phone numbers and birthday dates.

## Get Started

Run `pip install py_brigade_personal_assistant` to install the package and then `get-started` to get started.<br><br>

**The list of available commands is as follows:**

- `hi` or `hello` or `greeting` - to say hi to your favorite PA!
- `contacts` - to enter the address book interface;
- `notes` - to enter the notes interface;
- `close` or `exit` - to exit the personal assistant;


### Contacts Interface
| Command                         |    Options                                | Description                                                           |
| ---                             |  ---                                      | ---                                                                   |
| 🗂️ __Contact__                                                                                                                                      |
| `add`                           |   name, phone                             | to add a contact and its phone number;                                |
| `find`                          |   text                                    | to search a contact from your list by name, phone, email, or address; |
| `delete / remove`               |   name                                    | to delete the contact;                                                |
| `num-contacts`                  |   text                                    | to show the number of contacts;                                       |
| `all`                           |   -                                       | to list all the contacts and their phone numbers;                     |
| `help`                          |   -                                       | to show the list of available commands for the address book;          |
| `back / return / -`             |   -                                       | to exit the address book;                                             |
| 🗂️ __Phone__                                                                                                                   |
| `show-phone`                    |   name                                    | to list all the phone numbers associated with the contact;            |
| `change-phone`                  |   name, old name, new phone               | to change the phone number;                                           |
| `delete-phone / remove-phone`   |   name, phone                             | to change the phone number;                                           |


### Birthday
- `add-birthday + name + DD.MM.YYYY` - to add birthday;
- `show-birthday + name` - to show birthday associate with the contact;
- `birthdays (+ n)?` - to show a list of contacts with birthdays for the next n days, if specified;

### Email
- `add-email + name + email` - to add email;
- `show-email + name` - to show email associate with the contact;
- `change-email + name + old email + new email` - to change the email;
- `delete-email + name` - to remove the email;

### Address
- `add-address + name + address` - to add address;
- `show-address + name` - to show address associate with the contact;
- `change-address + name + new address` - to change the address;
- `delete-address name` - to remove the address;

## Notes Interface

- `add` + `additional inputs` - to create a note;
- `search / seek / find / filter / grep` + `additional name=<text> / tag=<text> / text=<text>` - to show one note;
- `edit / upd / update / change / ch` + `additional inputs` - to change one note;
- `remove / delete / del / rm` + `additional inputs` - to remove one note by ordinal number;
- `find` + `additional name=<text> / tag=<text> / text=<text>` - to show all notes that contain the keyword;
- `show / all / list / ls` - to list all notes with a ordinal number and note text;
- `help` - to show the list of available commands for notes;
- `back / return / -` - to exit notes;

<!-- ## Optional

- `add-tag note number tag name` - to add a tag to a note;
- `find-tag tag name` - to show all notes that contain the specified tag;
- `sort-tag` - to sort notes by tag;-->


## Additional Notes

1. Currently, it is not possible to add a contact with a name only. Both `name` and a `phone number` must be provided;
2. Calling the command again with the same name will add another phone number to the same contact;
3. `name` - a string with a minimum of 1 character and a maximum of 30 characters;
4. `phone number` - only numbers, 10 characters;
5. `birthday` - the format is DD.MM.YYYY;
6. `email` - a string, the format is example@example.com;
7. `address` - a string that may contain spaces, commas, periods, etc.; the address contains from 10 to 100 characters;
8. `text` - a string that can contain spaces, commas, periods, etc.; during note creation, it is assigned a ordinal number for management;
9. The PA saves the progress upon exiting; this does not apply to the cases when it is forcefully shut down (e.g. keyboard interrupt);
10. The PA supports machine-learning enabled intent recognition for all the intents except for:

- show-phone
- num-contacts
- add-address
- change-address
- show-address
- delete-address
+ these commands must be entered the way they are written above.