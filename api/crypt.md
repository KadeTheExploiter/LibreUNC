# Crypt

The **crypt** library provides methods for the encryption and decryption of string data.

Behavior and examples documented on this page are based on Script-Ware.

---

## crypt.base64encode

```lua
function crypt.base64encode(data: string): string
```

Encodes a string of bytes into Base64.

### Parameters

 * `data` - The data to encode.

### Aliases

 * `crypt.base64.encode`
 * `crypt.base64_encode`
 * `base64.encode`
 * `base64_encode`

### Example

```lua
local base64 = crypt.base64encode("Hello, World!")
local raw = crypt.base64decode(base64)

print(base64) --> SGVsbG8sIFdvcmxkIQ==
print(raw) --> Hello, World!
```

---

## crypt.base64decode

```lua
function crypt.base64decode(data: string): string
```

Decodes a Base64 string to a string of bytes.

### Parameters

 * `data` - The data to decode.

### Aliases

 * `crypt.base64.decode`
 * `crypt.base64_decode`
 * `base64.decode`
 * `base64_decode`

### Example

```lua
local base64 = crypt.base64encode("Hello, World!")
local raw = crypt.base64decode(base64)

print(base64) --> SGVsbG8sIFdvcmxkIQ==
print(raw) --> Hello, World!
```
