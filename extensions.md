# Extensions

[Paul Irish's gist on how to view source of chrome extension](https://gist.github.com/paulirish/78d6c1406c901be02c2d)

.crx file would not open as zip file on Windows -- think it's because `unzip`
in Linux ignores extra bytes at the beginning of zip file, but Windows does
not. The extra bytes is the package header:

https://developer.chrome.com/extensions/crx

Remove the package header bytes, and we have the zip file.
