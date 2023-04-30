###HydarTURN
HydarTURN is a Java implementation of the STUN/TURN protocol. It runs a single instance bound to a single IP(for now). Features:
-STUN: binding requests/responses
-TURN: Allocations
-Message integrity and fingerprinting
-Authentication(authenticator can only be provided programatically for now)
-Permissions and nonces(associated with an allocation)
-Relaying(DATA/SEND)
-Channel binding and channel relaying(CHANNELBIND)
These features are sufficient to route WebRTC voice and video calls from most browsers. To ensure TURN is being used when testing, set ice transport type as 'relay'.
Port reservations and dont-fragment requests are ignored, and the new STUN features added in RFC 8489(sha256 message integrity) are not supported.
Only one authentication realm, "hydar", is ever supported.
The implementation consists of a single source file, xyz.hydar.turn.HydarTURN.