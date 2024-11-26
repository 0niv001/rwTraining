Connection orientated protocol - Guarantees that data sent is received

Creates a connection through the use of handshakes that create channels between senders. 

End to End principle,

Two of the main issues are: corruption and congestion. TCP addresses both.

### Transport service primitives

- Primitives:
    - Listen: Block until process tries to connect
    - Connect: sends connection request,-
    - Send: sends data packet
    - Receive: Blocks until a data packet arrives
    - Disconnect: sends a disconnection request

TDPU - Transport Protocol Data Unit, sends messages from transport entity to transport entity in packets.

### Go back N

Allows transmission of multiple packets without waiting for ack, but has a limit of N that can be sent before an acknowledged packet needs to be received again.

The limit is imposed because of flow control.

Sliding window protocol- Receiver that only accepts segments that arrive in sequence and discards out of sequence segments.

Returns ACK containing sequence number of last segment received.