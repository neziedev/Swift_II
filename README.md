# Central Park Zoo Animal Exhibitions

Welcome to the Central Park Zoo! Help us design a new system using Swift for managing our animal exhibitions. We need to keep track of each animal's species, exhibit, and status, and be able to alert visitors about any changes in their display.

## Objectives

- Gain experience in using optional binding to safely unwrap values and display appropriate placeholders
- Master the creation of custom types including `enum`, `struct`, and `class`
- Understand the concept of a free-standing function and how to create one
- Add methods to a `class` or `struct` type
- Control the flow of the program through the utilization of `switch` statements
- Practice writing calculations using `Int` and `Double` types

## Instructions

1. Fork and clone this repository
2. Or Download as a zip and unzip
3. Complete all of the tasks outlined in the `Exhibition.playground` file

## Required

- Define an `enum` type for `AnimalStatus`
- Define a `struct` to represent a `Zoo`
- Define a `struct` to represent an `Animal`
- Define a `class` to represent a `ZooExhibit`
- Use the `Array.append()` method to add `Animals` to the exhibit
- Set the status of one animal to `.offExhibit` with a nil exhibit field
- Give one animal a unique exhibit to differentiate it from others
- Create a function to print the exhibit information using a `for-in` loop
- Make the `AnimalStatus` enum conform to `String` so you can print its raw value
- Call the function to print the current `ZooExhibit`
- Add an instance method to the `ZooExhibit` class that sends an alert message to visitors about the status of an animal
- Use a `switch` statement to send the appropriate message based on the animal's status
- Call the `alertVisitors()` method to send the alert messages

## Steps:

### before starting:

- Look at data from <a target="_blank" href="https://www.centralparkzoo.com/exhibits">Animal Exhibitions at the Central Park Zoo</a> for reference.

# Central Park Zoo Data Quick Reference

Location: New York City, NY

## Exhibits:

| Exhibit              | Location                    | Number of Animals | On Display | Behind the Scenes | Off-Exhibit |
| -------------------- | --------------------------- | ----------------- | ---------- | ----------------- | ----------- |
| Tisch Children's Zoo | Eastern side of the zoo     | 20                | 20         | 0                 | 0           |
| African Plains       | Western side of the zoo     | 20                | 20         | 0                 | 0           |
| Arctic Tundra        | Northern section of the zoo | 20                | 20         | 0                 | 0           |
| Rainforest           | Southern section of the zoo | 20                | 20         | 0                 | 0           |
| Discovery Center     | Center of the zoo           | 0                 | 0          | 0                 | 0           |

## I. Data Structures

- AnimalStatus Enum

  - Define an `enum` type for `AnimalStatus` (On Display, Behind the Scenes, Off-Exhibit, etc.)

- Zoo Struct

  - Define a `struct` to represent a Zoo (Name, Location, Number of Animals, etc.)

- Animal Struct

  - Define a `struct` to represent an Animal with a species, exhibit and status field.
  - Use a `String` for the exhibit name as it may not change.
  - Use a `String` for the species name as it is a required field.

- ZooExhibit Class
  - Define a `class` to represent a `ZooExhibit` with a list of animal exhibitions and the current zoo information.

## II. Adding Animals to the Zoo Exhibit

- Array `append()` Method

  - Use the Array `append()` method to add Animals to the exhibit.

- Setting Animal Status

  - Set the status of one animal to `.offExhibit` with a `nil` exhibit field.

- Unique Exhibit

  - Give one animal a unique exhibit to differentiate it from the others.

- Species Mapping with a Dictionary
  - Challenge: Use a dictionary to `map` species names to a specific exhibit.

## III. Printing Animal Information

- `printZooExhibit` Function

  - Create a free-standing function to `print` the exhibit information: `printZooExhibit(zooExhibit:)`

- For in Loop

  - Use a `for-in` loop to iterate over each animal in the exhibit.

- Conforming to String

  - Make the `AnimalStatus` `enum` conform to `String` so you can print the `rawValue` `String` values from the `enum`.

- Printing the `ZooExhibit`
  - Call the function to print the current `ZooExhibit`.

## IV. Printing On Display Exhibits

- `printOnDisplayExhibit` Function

  - Create a new function `printOnDisplayExhibit(zooExhibit:)` or modify the previous function.

- Optional Binding

  - Use optional binding to unwrap any optional values.

- Printing Only On Display Exhibits

  - Call the new or updated function to only `print` the exhibit name for animals that are on display.

- Sorting by Species
  - Challenge: Sort the animals in the exhibit by species before printing.

## V. Sending Alert Messages

- `alertVisitors` Method

  - Add an instance method to your `ZooExhibit` class that can send an alert message to visitors about the status of an animal.

- Switch Statement

  - Use a `switch` statement on the animal status variable to send the appropriate message:

    - If the animal is off-exhibit, `print "Sorry, the (species) is not on display at the moment. Please check back later."`
    - If the animal is on display, `print "Come visit the (species) in the (exhibit) exhibit!"`
    - If the animal is behind the scenes, `print "The (species) is currently behind the scenes. Thank you for your understanding."`

- Calling the Method
  - Call the `alertVisitors()` method to send the alert messages.
