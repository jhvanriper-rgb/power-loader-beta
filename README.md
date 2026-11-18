# Power Loader for SAP® software: free public beta

Load Excel data into SAP GUI transactions. Work through a transaction once, fill in an Excel workbook, rehearse, and load the rows into SAP one record at a time.

> This repository holds only the downloads of the free public beta. The program window still carries its working title, **Transaction Loader**.

## Download

**[Get the newest beta](https://github.com/jhvanriper-rgb/power-loader-beta/releases/latest)**, unzip it anywhere and run `TxLoader.exe`. There is nothing to install. The SHA-256 of every zip is in the notes of its release.

| | |
| --- | --- |
| Price | Free to try |
| Limits | A load runs at most 500 records, and the beta stops working on March 1, 2027. |
| Needs | Windows 10 or 11, SAP GUI for Windows with scripting switched on, Excel or any program that opens .xlsx files |
| Questions and problems | beta@getpowerloader.com (no promise of support, see the terms) |

Start on a development or test system. You use the beta at your own risk: the author accepts no responsibility for data errors. The program asks you to accept the [terms of use](TERMS.md) the first time it starts.

## How it works

1. **Connect.** The program finds your open SAP session. SAP asks you to allow the script, and you click OK in SAP.
2. **Capture.** You work through a transaction once, in a second SAP window, and the program records what you did.
3. **Map and generate.** You review the pages and fields. The program writes an Excel template with one tab for each page, and a loader script.
4. **Fill in the workbook.** One row for each record.
5. **Rehearse, then load.** A rehearsal does every step above the one you choose and sends nothing after it. A load runs the records one at a time, and the results show SAP's own message for each one.

The program uses the SAP GUI Scripting interface and the authorizations of the user who is logged in to SAP. It does not get around any SAP check. A load presses the buttons and keys that you recorded, so it cannot tell which of them change data, and it cannot undo a load.

## The first start

Windows may warn that it protected your PC, because the beta is not signed yet. Choose **More info**, then **Run anyway**. A company PC may block the file: ask your IT team. Compare the zip with the SHA-256 value in the release notes (`Get-FileHash <file> -Algorithm SHA256` in PowerShell).

## Privacy

The program makes no network connections and sends nothing anywhere. It writes only the files that you ask for, a small settings file, a log in your user profile (program messages and transaction codes, no business data) and a note that you accepted the terms.

## Not affiliated

This is an independent product. SAP SE and its affiliates do not make, sponsor or endorse it. SAP and other SAP products and services mentioned herein, as well as their respective logos, are trademarks or registered trademarks of SAP SE (or an SAP affiliate company) in Germany and other countries. All other product and service names are the trademarks of their respective owners.
