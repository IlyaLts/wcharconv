wcharconv
======
Functions for converting between single-byte character string (char) and 2 byte wide character string (wchar_t).

### Usage
```
#include <locale.h>
#include "wcharconv.h"

int main()
{
    char buf[64];
    wchar_t wbuf[64];

    wchar_to_char(L"Привет, мир! Begrüßung!", buf, sizeof(wbuf));
    char_to_wchar(buf, wbuf, sizeof(buf));

    setlocale(LC_ALL, ".UTF8");
    printf("%s\n", buf);
    wprintf(L"%s\n", wbuf);

    return 0;
}
```

## Documentation

| Functions | Descriptions |
| --- | --- |
| char_to_wchar(const char *from, wchar_t *to, size_t to_size) | Converts a single-byte character string to a 2 byte wide character string. |
| wchar_to_char(const wchar_t *from, char *to, size_t to_size) | Converts a 2 byte wide character string to a single-byte character string. |


## License

wcharconv is licensed under the MIT License, see LICENSE.txt for more information.