import java.util.Scanner;
public class hotelbooking {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int floors = 4;
        int roomsPerFloor = 5;

        String[][] roomStatus = new String[floors][roomsPerFloor];

        for (int i = 0; i < floors; i++) {
            for (int j = 0; j < roomsPerFloor; j++) {
                roomStatus[i][j] = "A";
            }
        }
        int choice;
        do {
            System.out.println("\nWelcome to hotel booking system!");
            System.out.println("1. View rooms");
            System.out.println("2. Book a room");
            System.out.println("3. Exit");
            System.out.print("Enter your choice: ");
            choice = sc.nextInt();

            switch (choice) {
                case 1:
                    System.out.println("\nRoom Availability (A = Available, B = Booked):");
                    System.out.print("       ");
                    for (int j = 0; j < roomsPerFloor; j++) {
                        System.out.print("Room " + (j + 1) + "  ");
                    }
                    System.out.println();

                    for (int i = 0; i < floors; i++) {
                        System.out.print("Floor " + (i + 1) + ": ");
                        for (int j = 0; j < roomsPerFloor; j++) {
                            System.out.print("   " + roomStatus[i][j] + "    ");
                        }
                        System.out.println();
                    }
                    break;
                case 2:
                    System.out.print("Enter the floor number to book a room on (1-" + floors + "): ");
                    int floor = sc.nextInt();
                    while (floor < 1 || floor > floors) {
                        System.out.print("Invalid floor. Please enter a number between 1 and " + floors + ": ");
                        floor = sc.nextInt();
                    }
                    System.out.print("Enter the room number to book (1-" + roomsPerFloor + "): ");
                    int room = sc.nextInt();
                    while (room < 1 || room > roomsPerFloor) {
                        System.out.print("Invalid room. Please enter a number between 1 and " + roomsPerFloor + ": ");
                        room = sc.nextInt();
                    }
                    if (roomStatus[floor - 1][room - 1].equalsIgnoreCase("B")) {
                        System.out.println("Sorry, that room is already booked.");
                    } else {
                        roomStatus[floor - 1][room - 1] = "B";
                        System.out.println("Room " + room + " on Floor " + floor + " has been successfully booked!");
                    }
                    break;
                case 3:
                    System.out.println("Thank you for using the hotel booking system. Goodbye!");
                    break;
                default:
                    System.out.println("Invalid choice. Please try again.");
            }
        } while (choice != 3);
        sc.close();
    }
} 
   

