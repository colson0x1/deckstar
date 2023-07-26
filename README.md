# Deckstar - A Simple Card Deck Manipulation Program in Go

Deckstar is a simple card deck manipulation program written in Go. It provides functionalities to create a new deck of cards, shuffle the deck, print the deck, and deal cards for games or other purposes. This program serves as a basic demonstration of how to work with slices and file I/O in Go.

## Usage

To use Deckstar, you must have Go installed on your system. If you haven't installed Go, you can find instructions [here](https://golang.org/doc/install).

1. Clone the Deckstar repository:
   ```
   git clone https://github.com/colson0x1/deckstar.git
   ```

2. Navigate to the Deckstar directory:
   ```
   cd deckstar
   ```

3. Run the main program to see the shuffled deck of cards:
   ```
   go run main.go
   ```

4. Run the unit tests to ensure everything is functioning correctly:
   ```
   go test
   ```

## Features

Deckstar provides the following features:

- Creating a new deck of cards with a standard set of values and suits.
- Printing the deck to the console to view the cards.
- Shuffling the deck randomly to change the card order.
- Dealing cards from the deck, returning two separate decks (hands).
- Saving the deck to a file for later use.
- Loading a deck from a saved file.

## Example

```go
package main

import (
	"fmt"
)

func main() {
	// Create a new deck
	cards := newDeck()

	// Shuffle the deck
	cards.shuffle()

	// Print the deck
	cards.print()

	// Deal two hands from the deck
	hand1, remainingDeck := deal(cards, 5)
	fmt.Println("Hand 1:")
	hand1.print()

	fmt.Println("Remaining Deck:")
	remainingDeck.print()
}
```