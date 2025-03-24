# System API Documentation

## Summary

This API documentation provides details about the message structure, status codes, and message types used in the system. It includes tables for:

- Message ID
- Status
- Message Types
- Distance Sensor (Message Type 1)
- Motor Control (Message Type 2)

---

## Message ID

The Message ID table defines the unique identifiers for system members and their associated addresses. Each member is assigned a specific ID and address for communication within the system.

| Member        | System         | ID  | Address |
|---------------|----------------|-----|---------|
| Divine    | Wifi           | 1   | 0x01    |
| Jake        | Human Interface| 2   | 0x02    |
| Jacob         | Accuator    | 3   | 0x03    |
| Andrey           | Sensor    | 4   | 0x04    |
| Broadcast     | All            | 88  | 0x58    |

---

## Status

The Status table defines the status codes used in the system to indicate the state of a message or operation.

| Status | Code |
|--------|------|
| Normal | 0x00 |
| Error  | 0x01 |

---

## Message Types

The Message Types table categorizes the types of messages and their associated status or code ranges.

| Category          | Status/Code                        | Address |
|-------------------|------------------------------------|---------|
| Accuator Data         | -40 to 155                         | 0x10    |
| Motor  Control       | 0-125                              | 0x20    |
| System Status     | Normal (0x00), Error (0x01)        | 0x30    |
| System Initialize | Pending (0x00), Complete (0x01)    | 0x40    |
| Error             | Error Code                         | 0x99    |
