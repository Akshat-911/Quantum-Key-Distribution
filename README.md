# Quantum-Key-Distribution
The BB84 protocol is one of the most famous Quantum Key Distribution algorithm developed by  Charles Bennett and Gilles Brassard in 1984(hence the name BB84) and is used to securely share a private key from one party to another using the principles of Quantum mechanics like superposition, teleportation, the no cloning theorem etc.

HERE IS A SMALL OVERVIEW OF THE BB84 PROTOCOL

BB84 relies on the principles of quantum mechanics, particularly quantum superposition and measurement disturbance, to ensure secure communication. The protocol consists of the following steps:

Step 1: Alice Generates Random Bits and Bases

Alice creates a random sequence of bits (0s and 1s).

She also selects random bases for encoding: Rectilinear (|0> and |1>) or Diagonal (|+> and |->).

Step 2: Alice Encodes Qubits

If using the rectilinear basis:

0 is encoded as |0>

1 is encoded as |1>

If using the diagonal basis:

0 is encoded as |+> (|0> + |1>) / sqrt(2)

1 is encoded as |-> (|0> - |1>) / sqrt(2)

Step 3: Alice Sends the Qubits to Bob

Alice transmits the quantum states to Bob over a quantum channel.

Step 4: Bob Chooses Random Bases and Measures the Qubits

Bob selects random bases (rectilinear or diagonal) for measurement.

If Bob's basis matches Alice's encoding basis, he obtains the correct bit. Otherwise, the measurement collapses randomly to 0 or 1.

Step 5: Basis Reconciliation

Alice and Bob publicly share which bases they used but not the actual bit values.

They discard bits where their bases didn't match, keeping only the correctly measured bits.

Step 6: Key Sifting and Error Detection

Alice and Bob compare a subset of their key bits to check for discrepancies.

If errors exceed a certain threshold, they suspect an eavesdropper (Eve) and abort the communication.

