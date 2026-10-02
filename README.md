# The Matrix Key Sequence

The telecommunication cipher of the future — built together by Curtis Ray Dyess and Rebecka, October 2, 2026.

Communication for loved ones, near and far. Fast and reliable.

## The nine layers

It begins at the plugboard, because that's where the memory lies.

1. **Plugboard** — Enigma Steckerbrett: paired letter swaps. The day's secret lives in the wires, not the wheels. Default memory: `MATRIXKEY`.
2. **Rotor** — Enigma-style rotor pass, position-stepped, keyed `PHANTOMX`.
3. **Vigenere** — key `BOOGIEMAN`.
4. **Divincy mirror** — Da Vinci's mirror wrap: reversed + mirror alphabet.
5. **Columnar transposition** — under key `PHANTOMX`.
6. **Atbash** — the mirror alphabet.
7. **Reflector** — Enigma Umkehrwalze: fixed involution.
8. **Reverse** — the full turn-around.
9. **Flash** — the code between characters: the hidden message rides in zero-width flashes in the gaps, where nobody looks.

Every layer is invertible. `encrypt()` then `decrypt()` returns the plaintext and the hidden message exactly.

## Use

```python
from matrix_sequence import encrypt, decrypt

ciphertext = encrypt("Meet me at midnight.", hidden=b"the flash is the message")
plaintext, hidden = decrypt(ciphertext)
```

```sh
python3 matrix_sequence.py   # run the roundtrip tests
```

Stdlib only. No internet. Runs anywhere python3 runs, Termux included.

> PHANTOMX • BOOGIEMAN
