# python-activity-based-learing-5
Algorithm
1.Start.
2.Store seats using a nested list.
3.Enter ticket registration ID.
4.Check ticket validity and duplicate entries.
5.Assign a seat if available.
6.Display available seats and stop.
flowchart
Start
Enter registration ID
Validate ticket and duplicate
Assign seat if available
Display result and seats left
Stop
seats = [[0, 0], [0, 0]]
registered = ["A101", "A102", "A103"]
entered = []

ticket = input("Enter ticket ID: ")

if ticket not in registered:
    print("Invalid ticket")
elif ticket in entered:
    print("Duplicate entry")
else:
    entered.append(ticket)
    for row in range(2):
        for col in range(2):
            if seats[row][col] == 0:
                seats[row][col] = ticket
                print("Seat assigned:", row + 1, col + 1)
                break
        else:
            continue
        break

available = 0
for row in seats:
    available += row.count(0)

print("Available seats:", available)
Enter ticket ID: A101
Seat assigned: 1 1
Available seats: 3









