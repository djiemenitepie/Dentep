
#include <stdio.h>

int main() {
  int num_students, present = 0, absent = 0;
  char name[20];

  printf("Enter the number of students: "); // Asks the user for the number of students
  scanf("%d", &num_students);

  for (int i = 0; i < num_students; i++) { // Loop through each student
    printf("Enter the name of student %d: ", i+1); // Asks the user for the name of the student
    scanf("%s", name);

    printf("Is %s present? (y/n): ", name); // Asks the user if the student is present
    char attendance;
    scanf(" %c", &attendance);

    if (attendance == 'y' || attendance == 'Y') { // If the student is present, increment the present variable
      present++;
    } else { // If the student is absent, increment the absent variable
      absent++;
    }
  }

  printf("Number of students present: %d\n", present); // Prints out the number of students present
  printf("Number of students absent: %d\n", absent); // Prints out the number of students absent

  return 0;
}
