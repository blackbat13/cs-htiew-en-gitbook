# Rail-fence cipher

## Problem description

{% content-ref url="../../../../algorithms/cryptography/rail-fence.md" %}
[rail-fence.md](../../../../algorithms/cryptography/rail-fence.md)
{% endcontent-ref %}

## Encoding

### Implementation

{% code overflow="wrap" lineNumbers="true" %}
```python
def encode(message: str, key: int) -> str:
    """
        Encodes message using Rail Fence Cipher with given key
        :param message: message to encode
        :param key: key
        :return: message encode using Rail Fence with given key
        """
    encoded = ""

    for k in range(key):
        if k == key - 1:
            jump = (key - 1) * 2
        else:
            jump = (key - (k + 1)) * 2
            
        i = k
        
        while i < len(message):
            encoded += message[i]
            i += jump

    return encoded


message = "computer science"

encoded = encode(message, 3)

print(f"Encoded: {encoded}")
```
{% endcode %}

## Decoding

### Implementation

{% code overflow="wrap" lineNumbers="true" %}
```python
def decode(message: str, key: int) -> str:
    """
        Decodes message using Rail Fence Cipher with given key
        :param message: message to encode
        :param key: key
        :return: message decoded using Rail Fence Cipher with given key
    """
    decoded = list(message)
    j = 0

    for k in range(key):
        if k == key - 1:
            jump = (key - 1) * 2
        else:
            jump = (key - (k + 1)) * 2
            
        i = k
        
        while i < len(message):
            decoded[i] = message[j]
            j += 1
            i += jump

    return "".join(decoded)


message = "cu eoptrsinemecc"

decoded = decode(message, 3)

print(f"Decoded: {decoded}")
```
{% endcode %}
