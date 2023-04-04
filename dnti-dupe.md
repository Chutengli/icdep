# Anti-Duplication (anti-dupe.md): How can we ensure that each card is received once and only once?

Each card can be wrapped with a header, and the header can include the following information to make sure that the each card is received once and only once

- Sequence Number: The receiver can cache the sequence number of the card it has received. If the sequence number appeared again, the receiver can refuse to accept this card
- Hash of the card: The receiver can cache the hash of the card it has received. If hash appeared again, the receiver can refuse to accept this.

Also, once the card is received, the receiver could send back an acknowledgement back to the sender so that the sender won't send out the card again
