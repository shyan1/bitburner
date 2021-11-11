<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [bitburner](./bitburner.md) &gt; [NS](./bitburner.ns.md) &gt; [fileExists](./bitburner.ns.fileexists.md)

## NS.fileExists() method

Check if a file exists.

<b>Signature:</b>

```typescript
fileExists(filename: string, host?: string): boolean;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  filename | string | Filename of file to check. |
|  host | string | Host of target server. This is optional. If it is not specified then the function will use the current server as the target server. |

<b>Returns:</b>

boolean

True if specified file exists, and false otherwise.

## Remarks

RAM cost: 0.1 GB

Returns a boolean indicating whether the specified file exists on the target server. The filename for scripts is case-sensitive, but for other types of files it is not. For example, fileExists(“brutessh.exe”) will work fine, even though the actual program is named 'BruteSSH.exe'.

If the hostname/ip argument is omitted, then the function will search through the current server (the server running the script that calls this function) for the file.

## Example 1


```ts
//The function call will return true if the script named foo.script exists on the foodnstuff server, and false otherwise.
fileExists("foo.script", "foodnstuff");
```

## Example 2


```ts
//The function call will return true if the current server contains the FTPCrack.exe program, and false otherwise.
fileExists("ftpcrack.exe");
```
