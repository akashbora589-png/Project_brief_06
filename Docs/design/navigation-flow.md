# Event Management System – Navigation Flow

## Main Navigation Flow

```mermaid
flowchart TD

    A[Login] --> B{Select User Role}

    B -->|Administrator| C[Admin Dashboard]
    B -->|Organizer| D[Organizer Dashboard]
    B -->|Participant| E[Participant Dashboard]

    %% Administrator
    C --> C1[User Management]
    C --> C2[Event Management]
    C --> C3[Registration Management]
    C --> C4[Schedule Management]
    C --> C5[Reports]
    C --> C6[Profile]

    C1 --> C1A[View Users]
    C1 --> C1B[Add / Edit User]
    C1 --> C1C[Delete User]

    C2 --> C2A[View Events]
    C2 --> C2B[Create Event]
    C2 --> C2C[Edit Event]
    C2 --> C2D[Delete Event]

    C3 --> C3A[View Registrations]
    C3 --> C3B[Manage Participants]

    C4 --> C4A[View Schedule]
    C4 --> C4B[Add / Edit Schedule]

    C5 --> C5A[View Reports]

    %% Organizer
    D --> D1[My Events]
    D --> D2[Registrations]
    D --> D3[Schedule]
    D --> D4[Profile]

    D1 --> D1A[View Events]
    D1 --> D1B[Create Event]
    D1 --> D1C[Edit Event]
    D1 --> D1D[Delete Event]

    D2 --> D2A[View Participants]

    D3 --> D3A[View Schedule]
    D3 --> D3B[Manage Schedule]

    %% Participant
    E --> E1[Browse Events]
    E --> E2[My Registrations]
    E --> E3[Event Schedule]
    E --> E4[Profile]

    E1 --> E1A[View Event Details]
    E1A --> E1B[Register for Event]

    %% Logout
    C6 --> F[Logout]
    D4 --> F
    E4 --> F