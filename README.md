# Relational-model-Checkpoint
Hotel (
    ID_H PRIMARY KEY,
    Name,
    Category,
    Address,
    ID_L FOREIGN KEY REFERENCES Location(ID_L)
)

Location (
    ID_L PRIMARY KEY,
    Name
)

Room (
    Num_R PRIMARY KEY,
    Floor,
    Type,
    Price,
    ID_H FOREIGN KEY REFERENCES Hotel(ID_H)
)

Client (
    ID_C PRIMARY KEY,
    Name,
    Firstname,
    Address
)

Reservation (
    ID_C FOREIGN KEY REFERENCES Client(ID_C),
    Num_R FOREIGN KEY REFERENCES Room(Num_R),
    Date_Reservation PRIMARY KEY,
    Date_Arrival,
    Date_Departure
)
