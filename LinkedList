import java.util.Scanner;

class LinkedList {

    Node head;

    LinkedList() {
        this.head = null;
    }

    static class Node {
        int data;
        Node next;

        Node() {
            this.data = 0;
            this.next = null;
        }
        Node(int data){
            this.data = data;
            this.next = null;
        }
        Node(int data, Node next) {
            this.data = data;
            this.next = next;
        }
    }

    void insertNode(int data) {
        Node node = new Node(data);
        if(this.head == null) {
            this.head = node;
        } else {
            Node track = this.head;
            while(track.next != null) {
                track = track.next;
            }
            track.next = node;
        }
        System.out.println("Node inserted: " + data);
    }

    void insertAtBegin(int data) {
        Node node = new Node(data);
        if(this.head == null) {
            this.head = node;
        } else {
            node.next = this.head;
            this.head = node;
        }
        System.out.println("Node inserted: " + data);
    }

    void removeNode(int data) {
        Node track = this.head;
        Node prev = null;
        boolean nodeFound = false;
        if(track != null) {
            while(track != null) {
                if(track.data == data) {
                    prev.next = track.next;
                    nodeFound = true;
                    break;
                }
                prev = track;
                track = track.next;
            }
        } else {
            System.out.println("The linked list is empty!");
        }
        if(!nodeFound) {
            System.out.println("Node not found with data: " + data);
        } else {
            System.out.println("Node removed: " + data);
        }
    }

    void removeNode() {
        Node track = this.head;
        track = this.head;
        Node prev = null;
        if(track != null) {
            while(track.next != null) {
                prev = track;
                track = track.next;
            }
            System.out.println("Node removed: " + track.data);
            if(prev != null) {
                prev.next = null;
            } else {
                this.head = null;
            }
            
        } else {
            System.out.println("The linked list is empty!");
        }
    }

    void sizeOfList() {
        Node track = this.head;
        int size = 0;
        if(track != null) {
            while(track != null) {
                size++;
                track = track.next;
            }
        }
        System.out.println("Number of Nodes: " + size);
    }

    void printList() {
        if(this.head == null) {
            System.out.println("The linked List is empty!");
        } else {
            System.out.print("Linked List: ");
            Node track = this.head;
            while(track != null)
            {
                System.out.print(track.data + " -> ");
                track = track.next;
            }
            System.out.print("\n");
        }
    }

    public static void main(String[] args) throws Exception {

        System.out.println("-- LinkedList Operations Menu --");
        System.out.println("Press 1 to Print");
        System.out.println("Press 2 to Insert Empty Node (Data=0)");
        System.out.println("Press 3 to Insert Data Node at the End");
        System.out.println("Press 4 to Insert Data Node at the Beginning");
        System.out.println("Press 5 to Delete Last Node");
        System.out.println("Press 6 to Delete Data Node");
        System.out.println("Press 7 to Get Size");
        System.out.println("Press 0 to Exit");
        
        LinkedList linkedList = new LinkedList();
        Scanner scan = new Scanner(System.in);
        int choice = -1;
        do {
            choice = scan.nextInt();
            switch (choice) {
                case 1:
                    linkedList.printList();
                    break;
                case 2:
                    linkedList.insertNode(0);
                    break;
                case 3:
                    System.out.print("Enter new node data: ");
                    linkedList.insertNode(scan.nextInt());
                    break;
                case 4:
                    System.out.print("Enter new node data: ");
                    linkedList.insertAtBegin(scan.nextInt());
                    break;
                case 5:
                    linkedList.removeNode();
                    break;
                case 6:
                    System.out.print("Enter node to be removed having data: ");
                    linkedList.removeNode(scan.nextInt());
                    break;
                case 7:
                    linkedList.sizeOfList();
                    break;
                case 0:
                    System.out.println("GoodBye! See you later, Alligator.");
                    break;
                default:
                    System.out.println("Please enter a valid choice!");
                    break;
            }
        } while (choice != 0);
    }

}
