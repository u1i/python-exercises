# Music Playlist Exercise: Understanding Linked Lists

This exercise demonstrates how linked lists provide a natural representation for sequential data like playlists, allowing efficient additions, removals, and traversals.

## Introduction

Linked lists are fundamental data structures where elements (nodes) are stored non-contiguously in memory. Each node contains data and a reference to the next node. Unlike arrays, linked lists allow efficient insertions and deletions without requiring resizing or shifting elements.

## Task: Build a Music Playlist Manager

Create a music playlist system using linked lists in Python. This practical implementation will help you understand how linked lists work and why they're useful for sequential data.

## Requirements

### Core Structures

1. Create a `Song` class that represents a node with:
   - Title
   - Artist
   - Duration (in seconds)
   - Reference to the next song

2. Create a `Playlist` class that manages songs with:
   - Head reference to the first song
   - Name of the playlist

### Required Operations

Implement the following methods in your `Playlist` class:

1. `add_song(title, artist, duration)` - Add a new song to the end of the playlist
2. `remove_song(title)` - Remove a song with the given title
3. `display_playlist()` - Display all songs in the playlist
4. `play()` - Simulate playing the playlist from beginning to end
5. `skip()` - Skip to the next song
6. `get_playlist_length()` - Return the number of songs in the playlist
7. `is_empty()` - Check if the playlist is empty

### Advanced Operations (Bonus)

8. `shuffle()` - Randomly reorder the songs in the playlist
9. `insert_after(target_title, new_title, new_artist, new_duration)` - Insert a new song after a specific song
10. `reverse()` - Reverse the order of songs in the playlist

## Example Usage

```python
my_playlist = Playlist("Road Trip Mix")
my_playlist.add_song("Bohemian Rhapsody", "Queen", 354)
my_playlist.add_song("Hotel California", "Eagles", 390)
my_playlist.add_song("Sweet Child O' Mine", "Guns N' Roses", 356)

my_playlist.display_playlist()
# Should display all three songs with their details

my_playlist.skip()  # Should move to the second song
my_playlist.remove_song("Hotel California")
my_playlist.shuffle()  # Should randomize the order

my_playlist.display_playlist()
# Should show the updated playlist
```

## Reflection Questions

After completing the implementation, answer these questions:
1. How does a linked list implementation of a playlist differ from an array implementation?
2. What operations are more efficient with linked lists, and which ones are less efficient?
3. How would you implement a doubly-linked list to allow moving backward in the playlist?