# Python Style Guide [HDK]

1. don't close a connection either of file or db use `with` to use as context manager
    ```python
    with open("harsh.txt","r") as f:
        d = f.readlines()
    ```
2. don't use `time.time` use `time.perf_counter`

    ```python
    import time
    start = time.perf_counter()
    a = 3 + 6
    d = a * 5
    end = time.perf_counter()
    elapsed_time = end - start
    ```
