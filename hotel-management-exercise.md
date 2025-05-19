# Hotel Room Management System: Understanding Free Space Lists

This exercise demonstrates how free space lists provide an efficient way to manage resources like hotel rooms, allowing quick allocation, deallocation, and tracking of available space without requiring expensive operations.

## Introduction

Free space lists are data structures used in memory management to track available resources. Unlike traditional arrays, they efficiently handle dynamic allocation and deallocation of resources without requiring expensive shifts or copies, making them ideal for systems that frequently acquire and release resources.

## Task: Build a Hotel Room Management System

Create a hotel room management system using free space lists in Python. This practical implementation will help you understand how free space lists work and why they're useful for resource management.

## Requirements

### Core Structures

1. Create a `Room` class that represents a memory block with:
   - Room number
   - Size (single, double, suite)
   - Status (available/occupied)
   - Reference to the next available room

2. Create a `Hotel` class that manages rooms with:
   - Head reference to the first available room
   - Total rooms in the hotel
   - Name of the hotel

### Required Operations

Implement the following methods in your `Hotel` class:

1. `initialize_rooms(num_singles, num_doubles, num_suites)` - Set up the initial free space list of all rooms
2. `book_room(size)` - Allocate a room of specified size from the free list
3. `checkout(room_number)` - Return a room to the free list
4. `display_available_rooms()` - Show all available rooms in the free list
5. `display_occupied_rooms()` - Show all occupied rooms
6. `get_availability()` - Return counts of available rooms by type
7. `is_full()` - Check if the hotel has no available rooms

### Advanced Operations (Bonus)

8. `defragment()` - Reorganize the free list to combine adjacent free rooms (simulating memory compaction)
9. `find_best_fit(size)` - Implement a best-fit allocation strategy instead of first-fit
10. `simulate_busy_day(bookings, checkouts)` - Simulate a day of random bookings and checkouts

## Example Usage

```python
grand_hotel = Hotel("Grand Budapest", 20)
grand_hotel.initialize_rooms(10, 8, 2)  # 10 singles, 8 doubles, 2 suites

# Book some rooms
room1 = grand_hotel.book_room("single")
room2 = grand_hotel.book_room("double")
room3 = grand_hotel.book_room("suite")

grand_hotel.display_available_rooms()
# Should display remaining available rooms

grand_hotel.checkout(room1)
# Should return room1 to the free list

grand_hotel.display_available_rooms()
# Should show updated available rooms including room1
```

## Reflection Questions

After completing the implementation, answer these questions:
1. How does the free space list implementation help in efficient room allocation and deallocation?
2. What advantages does this system have over a simple array-based room tracking system?
3. How would you handle fragmentation in this system? What real-world hotel situations might cause fragmentation?
4. How is this similar to memory management in operating systems?