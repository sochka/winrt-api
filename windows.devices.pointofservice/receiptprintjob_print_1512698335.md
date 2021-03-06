---
-api-id: M:Windows.Devices.PointOfService.ReceiptPrintJob.Print(System.String)
-api-type: winrt method
---

<!-- Method syntax
public void Print(System.String data)
-->

# Windows.Devices.PointOfService.ReceiptPrintJob.Print

## -description
Adds an instruction to the print job to print the specified text on the receipt printer station.

## -parameters
### -param data
The text to print on the receipt printer station.

## -remarks
If [ClaimedPosPrinter.IsCharacterSetMappingEnabled](claimedposprinter_ischaractersetmappingenabled.md) is true, the text is mapped to the font on the printer that [ClaimedPosPrinter.CharacterSet](claimedposprinter_characterset.md) specifies. If [ClaimedPosPrinter.IsCharacterSetMappingEnabled](claimedposprinter_ischaractersetmappingenabled.md) is false, the driver or provider sends the low byte of each Unicode character to the printer verbatim.

## -examples

## -see-also
[IPosPrinterJob.Print](iposprinterjob_print.md)