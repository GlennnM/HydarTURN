### HydarTURN
HydarTURN is a lightweight and embeddable Java implementation of the STUN/TURN protocol.<br>
It runs a single instance bound to a single IP(for now).<br>
Features:
- STUN: binding requests/responses
- TURN: Allocations
- Message integrity and fingerprinting
- Authentication(authenticator can only be provided programatically for now)
- Permissions and nonces(associated with an allocation)
- Relaying(DATA/SEND)
- Channel binding and channel relaying(CHANNELBIND)
- Support for both UDP & TCP instances

These features are sufficient to route WebRTC voice and video calls from most browsers. To ensure TURN is being used when testing, set ice transport type as 'relay'.<br>
Unimplemented features:
- Port reservations and dont-fragment requests are ignored, and the new STUN features added in RFC 8489(sha256 message integrity) are not supported.
- Only one authentication realm, "hydar", is ever supported.
- The third protocol allowed for TURN relaying, TURN-over-TLS, is not supported. Note that this doesn't mean calls are insecure, since WebRTC encrypts its own messages regardless of the transport.

### Implementation

The implementation consists of a single source file, xyz.hydar.turn.HydarTURN.

HydarTURN was designed for embedding in <a href=https://hydar.xyz>hydar.xyz</a>, another open source project.<br>

