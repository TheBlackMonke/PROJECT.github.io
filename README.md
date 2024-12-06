#include <stdio.h>
#include <stdlib.h>
#include <string.h>

// Function declarations
void displayCategories();
void displayKnotsInCategory(int category);
void displayKnotDetails(int category, int knot);
void displayKnotProcess(int category, int knot);
void displayFinalDesign();

int main() {
    int categoryChoice, knotChoice, detailChoice, processChoice, designChoice;

    printf("Welcome to Knot Explorer!\n");
    printf("Let's explore different types of knots.\n\n");

    // Step 1: Choose a category
    displayCategories();
    printf("Enter the number corresponding to your choice of knot category: ");
    scanf("%d", &categoryChoice);

    if (categoryChoice < 1 || categoryChoice > 7) {
        printf("Invalid category. Exiting program.\n");
        return 0;
    }

    // Step 2: Display knots in the chosen category
    displayKnotsInCategory(categoryChoice);
    printf("Enter the number corresponding to your choice of knot: ");
    scanf("%d", &knotChoice);

    // Step 3: Provide details based on user choice
    printf("\nWould you like to know the description and application of the knot?\n");
    printf("1. Yes\n2. No\n");
    printf("Enter your choice: ");
    scanf("%d", &detailChoice);

    if (detailChoice == 1) {
        displayKnotDetails(categoryChoice, knotChoice);
    }

    printf("\nWould you like to know the process of making the knot?\n");
    printf("1. Yes\n2. No\n");
    printf("Enter your choice: ");
    scanf("%d", &processChoice);

    if (processChoice == 1) {
        displayKnotProcess(categoryChoice, knotChoice);
    }

    printf("\nWould you like to see the final design of the knot?\n");
    printf("1. Yes\n2. No\n");
    printf("Enter your choice: ");
    scanf("%d", &designChoice);

    if (designChoice == 1) {
        displayFinalDesign(); // Placeholder for design display
    }

    printf("\nThank you for exploring knots with us!\n");
    return 0;
}

void displayCategories() {
    printf("Knot Categories:\n");
    printf("1. Basic Knots\n");
    printf("2. Climbing Knots\n");
    printf("3. Sailing Knots\n");
    printf("4. Decorative Knots\n");
    printf("5. Fishing Knots\n");
    printf("6. Utility Knots\n");
    printf("7. Specialized Knots\n");
}

void displayKnotsInCategory(int category) {
    printf("\nKnots in the chosen category:\n");
    switch (category) {
        case 1:
            printf("1. Square Knot (Reef Knot)\n2. Bowline Knot\n3. Sheet Bend Knot\n4. Clove Hitch Knot\n");
            break;
        case 2:
            printf("1. Figure Eight Knot\n2. Alpine Butterfly Knot\n3. Prusik Knot\n4. Water Knot\n");
            break;
        case 3:
            printf("1. Rolling Hitch Knot\n2. Clove Hitch Knot\n3. Reef Knot\n4. Bowline Knot\n");
            break;
        case 4:
            printf("1. Monkey's Fist Knot\n2. Turk's Head Knot\n3. Matthew Walker Knot\n4. Carrick Bend Knot\n");
            break;
        case 5:
            printf("1. Blood Knot\n2. Fisherman's Knot\n3. Improved Clinch Knot\n4. Barrel Knot\n");
            break;
        case 6:
            printf("1. Trucker's Hitch Knot\n2. Taut-Line Hitch Knot\n3. Round Turn and Two Half Hitches\n4. Timber Hitch Knot\n");
            break;
        case 7:
            printf("1. Eldridge Knot\n2. Gordian Knot\n3. Klemheist Knot\n4. Bends\n");
            break;
        default:
            printf("Invalid category.\n");
    }
}

void displayKnotDetails(int category, int knot) {
    printf("\nDetails of the selected knot:\n");
    if (category == 1 && knot == 1) {
        printf("Name: Square Knot (Reef Knot)\n");
        printf("Description: A simple binding knot used to secure two ends of rope together.\n");
        printf("Application: Commonly used in first aid to tie bandages and in packaging to secure items.\n");
        printf("Crossing Number: 4\nBridge Number: 2\nUnknotting Number: 2\n");
    } else if (category == 1 && knot == 2) {
        printf("Name: Bowline Knot\n");
        printf("Description: Creates a fixed loop at the end of a rope.\n");
        printf("Application: Used in rescue operations and sailing to secure loops that won't slip.\n");
        printf("Crossing Number: 5\nBridge Number: 2\nUnknotting Number: 2\n");
    } else {
        printf("Details for this knot are not yet implemented.\n");
    }
}

void displayKnotProcess(int category, int knot) {
    printf("\nProcess of making the selected knot:\n");
    if (category == 1 && knot == 1) {
        printf("1. Take two ends of the rope, one in each hand.\n");
        printf("2. Cross the right end over the left and tuck it under.\n");
        printf("3. Pull tight.\n");
        printf("4. Take the left end over the right and tuck it under.\n");
        printf("5. Pull tight again to secure.\n");
    } else if (category == 1 && knot == 2) {
        printf("1. Create a small loop in the rope (the rabbit hole).\n");
        printf("2. Pass the working end (rabbit) through the loop from underneath.\n");
        printf("3. Wrap it around the standing part (the tree).\n");
        printf("4. Bring it back down through the loop.\n");
        printf("5. Pull tight to secure.\n");
    } else {
        printf("Process for this knot is not yet implemented.\n");
    }
}

void displayFinalDesign() {
    printf("\nFinal design display is a placeholder.\n");
    printf("Integration with a graphical system or ASCII art is required for this feature.\n");
}
