# unreal._Logger

```python
class unreal.Logger(encoding, log_func, flush_func)
```


**Bases:** ``BufferedIOBase``


close()

Flush and close the IO object.

This method has no effect if the file is already closed.

detach()

Disconnect this buffer from its underlying raw stream and return it.

After the raw stream has been detached, the buffer is in an unusable
state.

flush()

Flush write buffers, if applicable.

This is not implemented for read-only and non-blocking streams.

writable()

Return whether object was opened for writing.

If False, write() will raise OSError.

write( _b_)

Write the given buffer to the IO stream.

Returns the number of bytes written, which is always the length of b
in bytes.

Raises BlockingIOError if the buffer is full and the
underlying raw stream cannot accept more data at the moment.

### Table of Contents

- `unreal._Logger`
  - `_Logger`
    - `_Logger.close()`
    - `_Logger.detach()`
    - `_Logger.flush()`
    - `_Logger.writable()`
    - `_Logger.write()`