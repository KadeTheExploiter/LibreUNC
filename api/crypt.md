# Encoding

The **Encoding** library provides methods for the modification of string data.

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

---

## lz4compress

```lua
function lz4compress(data: string): string
```

Compresses `data` using LZ4 compression.

### Parameters

 * `data` - The uncompressed data.

### Example

```lua
local text = "Hello, world! Hello, world! Goodbye, world!"
print(#text) --> 43
print(#lz4compress(text)) --> 34
```

---

## lz4decompress

```lua
function lz4decompress(data: string, size: number): string
```

Decompresses `data` using LZ4 compression, with the decompressed size specified by `size`.

### Parameters

 * `data` - The compressed data.
 * `size` - The size of the decompressed data.

### Example

```lua
local text = "Hello, world! Hello, world!"
local compressed = lz4compress(text)
print(lz4decompress(compressed, #text)) --> "Hello, world! Hello, world!"
```
