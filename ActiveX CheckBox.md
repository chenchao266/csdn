x64目录下的oleview.exe 打开C:\Windows\System32\FM20.DLL
[The Complete Guide to Excel VBA ActiveX Checkboxes](https://wellsr.com/vba/2015/excel/complete-guide-to-excel-vba-ActiveX-checkboxes/)

// typelib filename: **FM20.DLL**

[
  uuid(0D452EE1-E08F-101A-852E-02608C4D0BB4),
  version(2.0),
  helpstring("Microsoft Forms 2.0 Object Library"),
  helpfile("fm20.hlp"),
  helpcontext(00000000),
  custom(0F21F359-AB84-41E8-9A78-36D110E6D2F9, "Microsoft.Vbe.Interop.Forms.dll")

]
library MSForms
......

[
  uuid(8BD21D40-EC42-11CE-9E0D-00AA006002F3),
  helpcontext(0x001e8656),
  noncreatable,
  control
]
coclass **CheckBox** {

```c
[default] interface IMdcCheckBox;
[default, source] dispinterface MdcCheckBoxEvents;
```

};

[
  uuid(E9729012-8271-4E1F-BC56-CF85F914915A),
  helpcontext(0x001e8656),
  noncreatable,
  hidden,
  control
]
coclass **CheckBox2** {

```c
[default] interface IMdcCheckBox;
[default, source] dispinterface MdcCheckBoxEvents;
```

};



[
  odl,
  uuid(8BD21D43-EC42-11CE-9E0D-00AA006002F3),
  hidden,
  dual,
  oleautomation
]
interface **IMdcCheckBox** : IDispatch {

```c
[id(0xfffffde1), propput, bindable, helpcontext(0x001e8732)]
HRESULT Accelerator([in] BSTR Accelerator);
[id(0xfffffde1), propget, bindable, helpcontext(0x001e8732)]
HRESULT Accelerator([out, retval] BSTR* Accelerator);
[id(0x000002c6), propput, bindable, helpcontext(0x001e8746)]
HRESULT Alignment([in] fmAlignment Alignment);
[id(0x000002c6), propget, bindable, helpcontext(0x001e8746)]
HRESULT Alignment([out, retval] fmAlignment* Alignment);
[id(0xfffffe0c), propput, bindable, helpcontext(0x001e8764)]
HRESULT AutoSize([in] VARIANT_BOOL AutoSize);
[id(0xfffffe0c), propget, bindable, helpcontext(0x001e8764)]
HRESULT AutoSize([out, retval] VARIANT_BOOL* AutoSize);
[id(0xfffffe0b), propput, bindable, helpcontext(0x001e8782)]
HRESULT BackColor([in] OLE_COLOR BackColor);
[id(0xfffffe0b), propget, bindable, helpcontext(0x001e8782)]
HRESULT BackColor([out, retval] OLE_COLOR* BackColor);
[id(0xfffffe0a), propput, bindable, helpcontext(0x001e878c)]
HRESULT BackStyle([in] fmBackStyle BackStyle);
[id(0xfffffe0a), propget, bindable, helpcontext(0x001e878c)]
HRESULT BackStyle([out, retval] fmBackStyle* BackStyle);
[id(0x00000014), propput, bindable, hidden]
HRESULT BordersSuppress([in] VARIANT_BOOL BordersSuppress);
[id(0x00000014), propget, bindable, hidden]
HRESULT BordersSuppress([out, retval] VARIANT_BOOL* BordersSuppress);
[id(0xfffffdfa), propput, bindable, helpcontext(0x001e87f0)]
HRESULT Caption([in] BSTR Caption);
[id(0xfffffdfa), propget, bindable, helpcontext(0x001e87f0)]
HRESULT Caption([out, retval] BSTR* Caption);
[id(0xfffffdfe), propput, bindable, helpcontext(0x001e88e0)]
HRESULT Enabled([in] VARIANT_BOOL Enabled);
[id(0xfffffdfe), propget, bindable, helpcontext(0x001e88e0)]
HRESULT Enabled([out, retval] VARIANT_BOOL* Enabled);
[id(0x7ffffdff), propput, bindable, hidden, helpcontext(0x001e8688)]
HRESULT _Font_Reserved([in] Font* rhs);
[id(0xfffffe00), propputref, bindable, helpcontext(0x001e8688)]
HRESULT Font([in] Font* Font);
[id(0xfffffe00), propget, bindable, helpcontext(0x001e8688)]
HRESULT Font([out, retval] Font** Font);
[id(0x00000003), propput, bindable, hidden, helpcontext(0x001e88fe)]
HRESULT FontBold([in] VARIANT_BOOL FontBold);
[id(0x00000003), propget, bindable, hidden, helpcontext(0x001e88fe)]
HRESULT FontBold([out, retval] VARIANT_BOOL* FontBold);
[id(0x00000004), propput, bindable, hidden, helpcontext(0x001e8908)]
HRESULT FontItalic([in] VARIANT_BOOL FontItalic);
[id(0x00000004), propget, bindable, hidden, helpcontext(0x001e8908)]
HRESULT FontItalic([out, retval] VARIANT_BOOL* FontItalic);
[id(0x00000001), propput, bindable, hidden, helpcontext(0x001e8912)]
HRESULT FontName([in] BSTR FontName);
[id(0x00000001), propget, bindable, hidden, helpcontext(0x001e8912)]
HRESULT FontName([out, retval] BSTR* FontName);
[id(0x00000002), propput, bindable, hidden, helpcontext(0x001e891c)]
HRESULT FontSize([in] CURRENCY FontSize);
[id(0x00000002), propget, bindable, hidden, helpcontext(0x001e891c)]
HRESULT FontSize([out, retval] CURRENCY* FontSize);
[id(0x00000006), propput, bindable, hidden, helpcontext(0x001e8926)]
HRESULT FontStrikethru([in] VARIANT_BOOL FontStrikethru);
[id(0x00000006), propget, bindable, hidden, helpcontext(0x001e8926)]
HRESULT FontStrikethru([out, retval] VARIANT_BOOL* FontStrikethru);
[id(0x00000005), propput, bindable, hidden, helpcontext(0x001e8930)]
HRESULT FontUnderline([in] VARIANT_BOOL FontUnderline);
[id(0x00000005), propget, bindable, hidden, helpcontext(0x001e8930)]
HRESULT FontUnderline([out, retval] VARIANT_BOOL* FontUnderline);
[id(0x00000007), propput, bindable, hidden, helpcontext(0x001e893a)]
HRESULT FontWeight([in] short FontWeight);
[id(0x00000007), propget, bindable, hidden, helpcontext(0x001e893a)]
HRESULT FontWeight([out, retval] short* FontWeight);
[id(0xfffffdff), propput, bindable, helpcontext(0x001e8944)]
HRESULT ForeColor([in] OLE_COLOR ForeColor);
[id(0xfffffdff), propget, bindable, helpcontext(0x001e8944)]
HRESULT ForeColor([out, retval] OLE_COLOR* ForeColor);
[id(0x0000000a), propput, bindable, helpcontext(0x001e8a3e)]
HRESULT Locked([in] VARIANT_BOOL Locked);
[id(0x0000000a), propget, bindable, helpcontext(0x001e8a3e)]
HRESULT Locked([out, retval] VARIANT_BOOL* Locked);
[id(0xfffffdf6), propput, bindable, helpcontext(0x001e8a84)]
HRESULT MouseIcon([in] Picture* MouseIcon);
[id(0xfffffdf6), propputref, bindable, helpcontext(0x001e8a84)]
HRESULT MouseIcon([in] Picture* MouseIcon);
[id(0xfffffdf6), propget, bindable, helpcontext(0x001e8a84)]
HRESULT MouseIcon([out, retval] Picture** MouseIcon);
[id(0xfffffdf7), propput, bindable, helpcontext(0x001e8a8e)]
HRESULT MousePointer([in] fmMousePointer MousePointer);
[id(0xfffffdf7), propget, bindable, helpcontext(0x001e8a8e)]
HRESULT MousePointer([out, retval] fmMousePointer* MousePointer);
[id(0xfffffdec), propput, bindable, hidden]
HRESULT MultiSelect([in] fmMultiSelect MultiSelect);
[id(0xfffffdec), propget, bindable, hidden]
HRESULT MultiSelect([out, retval] fmMultiSelect* MultiSelect);
[id(0xfffffdf5), propput, bindable, helpcontext(0x001e8b2e)]
HRESULT Picture([in] Picture* Picture);
[id(0xfffffdf5), propputref, bindable, helpcontext(0x001e8b2e)]
HRESULT Picture([in] Picture* Picture);
[id(0xfffffdf5), propget, bindable, helpcontext(0x001e8b2e)]
HRESULT Picture([out, retval] Picture** Picture);
[id(0x0000000b), propput, bindable, helpcontext(0x001e8b38)]
HRESULT PicturePosition([in] fmPicturePosition PicPos);
[id(0x0000000b), propget, bindable, helpcontext(0x001e8b38)]
HRESULT PicturePosition([out, retval] fmPicturePosition* PicPos);
[id(0x0000000c), propput, bindable, helpcontext(0x001e8c28)]
HRESULT SpecialEffect([in] fmButtonEffect SpecialEffect);
[id(0x0000000c), propget, bindable, helpcontext(0x001e8c28)]
HRESULT SpecialEffect([out, retval] fmButtonEffect* SpecialEffect);
[id(0x000002bc), propput, helpcontext(0x001e8ce6)]
HRESULT TripleState([in] VARIANT_BOOL TripleState);
[id(0x000002bc), propget, helpcontext(0x001e8ce6)]
HRESULT TripleState([out, retval] VARIANT_BOOL* TripleState);
[id(0xfffffdf4), propget, hidden]
HRESULT Valid([out, retval] VARIANT_BOOL* Valid);
[id(00000000), propput, bindable, displaybind, defaultbind, helpcontext(0x001e8d04)]
HRESULT Value([in] VARIANT* Value);
[id(00000000), propget, bindable, displaybind, defaultbind, helpcontext(0x001e8d04)]
HRESULT Value([out, retval] VARIANT* Value);
[id(0xfffffde8), propput, bindable, helpcontext(0x001e8d36)]
HRESULT WordWrap([in] VARIANT_BOOL WordWrap);
[id(0xfffffde8), propget, bindable, helpcontext(0x001e8d36)]
HRESULT WordWrap([out, retval] VARIANT_BOOL* WordWrap);
[id(0xfffffde4), propget, bindable, hidden]
HRESULT DisplayStyle([out, retval] fmDisplayStyle* DisplayStyle);
[id(0xfffffde3), propput, bindable, helpcontext(0x001e895d)]
HRESULT GroupName([in] BSTR GroupName);
[id(0xfffffde3), propget, bindable, helpcontext(0x001e895d)]
HRESULT GroupName([out, retval] BSTR* GroupName);
[id(0x00002714), propput, bindable, helpcontext(0x001e8ca0)]
HRESULT TextAlign([in] fmTextAlign TextAlign);
[id(0x00002714), propget, bindable, helpcontext(0x001e8ca0)]
HRESULT TextAlign([out, retval] fmTextAlign* TextAlign);
```

};


[
  uuid(8BD21D42-EC42-11CE-9E0D-00AA006002F3),
  hidden
]
dispinterface **MdcCheckBoxEvents** {

```c
properties:
methods:
    [id(0x00000003), helpcontext(0x001e849e)]
    void BeforeDragOver(
                    [in] ReturnBoolean* Cancel, 
                    [in] DataObject* Data, 
                    [in] single X, 
                    [in] single Y, 
                    [in] fmDragState DragState, 
                    [in] ReturnEffect* Effect, 
                    [in] short Shift);
    [id(0x00000004), helpcontext(0x001e84a8)]
    void BeforeDropOrPaste(
                    [in] ReturnBoolean* Cancel, 
                    [in] fmAction Action, 
                    [in] DataObject* Data, 
                    [in] single X, 
                    [in] single Y, 
                    [in] ReturnEffect* Effect, 
                    [in] short Shift);
    [id(0x00000002), helpcontext(0x001e84bc)]
    void Change();
    [id(0xfffffd9e), helpcontext(0x001e84c6)]
    void Click();
    [id(0xfffffda7), helpcontext(0x001e84d0)]
    void DblClick([in] ReturnBoolean* Cancel);
    [id(0xfffffda0), helpcontext(0x001e84e4)]
    void Error(
                    [in] short Number, 
                    [in] ReturnString* Description, 
                    [in] long SCode, 
                    [in] BSTR Source, 
                    [in] BSTR HelpFile, 
                    [in] long HelpContext, 
                    [in] ReturnBoolean* CancelDisplay);
    [id(0xfffffda6), helpcontext(0x001e84f8)]
    void KeyDown(
                    [in] ReturnInteger* KeyCode, 
                    [in] short Shift);
    [id(0xfffffda5), helpcontext(0x001e8502)]
    void KeyPress([in] ReturnInteger* KeyAscii);
    [id(0xfffffda4), helpcontext(0x001e850c)]
    void KeyUp(
                    [in] ReturnInteger* KeyCode, 
                    [in] short Shift);
    [id(0xfffffda3), helpcontext(0x001e852a)]
    void MouseDown(
                    [in] short Button, 
                    [in] short Shift, 
                    [in] single X, 
                    [in] single Y);
    [id(0xfffffda2), helpcontext(0x001e8534)]
    void MouseMove(
                    [in] short Button, 
                    [in] short Shift, 
                    [in] single X, 
                    [in] single Y);
    [id(0xfffffda1), helpcontext(0x001e853e)]
    void MouseUp(
                    [in] short Button, 
                    [in] short Shift, 
                    [in] single X, 
                    [in] single Y);
```

};

---------------
打开Office安装目录\Microsoft Office\Office16\EXCEL.EXE
[The Complete Guide to Excel VBA Form Control Checkboxes](https://wellsr.com/vba/2015/excel/complete-guide-to-excel-vba-form-control-checkboxes/)
// typelib filename: **EXCEL.EXE**

[
  uuid(00020813-0000-0000-C000-000000000046),
  version(1.9),
  helpstring("Microsoft Excel 16.0 Object Library"),
  helpfile("VBAXL10.CHM"),
  helpcontext(0x0000ffff),
  custom(0F21F359-AB84-41E8-9A78-36D110E6D2F9, "Microsoft.Office.Interop.Excel.dll")

]
library Excel
......


[
  odl,
  uuid(0002087F-0001-0000-C000-000000000046),
  helpcontext(0x00041728),
  hidden
]
interface **ICheckBox** : IDispatch {
```c
    [propget, helpcontext(0x00041729)]
    HRESULT _stdcall Application([out, retval] Application** RHS);
    [propget, helpcontext(0x0004172a)]
    HRESULT _stdcall Creator([out, retval] XlCreator* RHS);
    [propget, helpcontext(0x00041b11)]
    HRESULT _stdcall Parent([out, retval] IDispatch** RHS);
    [propget, helpcontext(0x00041b12)]
    HRESULT _stdcall BottomRightCell([out, retval] Range** RHS);
    [helpcontext(0x00041b13)]
    HRESULT _stdcall BringToFront([out, retval] VARIANT* RHS);
    [helpcontext(0x00041b14)]
    HRESULT _stdcall Copy([out, retval] VARIANT* RHS);
    [helpcontext(0x00041b15)]
    HRESULT _stdcall CopyPicture(
                    [in, optional, defaultvalue(2)] XlPictureAppearance Appearance, 
                    [in, optional, defaultvalue(-4147)] XlCopyPictureFormat Format, 
                    [out, retval] VARIANT* RHS);
    [helpcontext(0x00041b16)]
    HRESULT _stdcall Cut([out, retval] VARIANT* RHS);
    [helpcontext(0x00041b17)]
    HRESULT _stdcall Delete([out, retval] VARIANT* RHS);
    [helpcontext(0x00041b18)]
    HRESULT _stdcall Duplicate([out, retval] IDispatch** RHS);
    [propget, helpcontext(0x00041b19)]
    HRESULT _stdcall Enabled([out, retval] VARIANT_BOOL* RHS);
    [propput, helpcontext(0x00041b19)]
    HRESULT _stdcall Enabled([in] VARIANT_BOOL RHS);
    [propget, helpcontext(0x00041b1a)]
    HRESULT _stdcall Height([out, retval] double* RHS);
    [propput, helpcontext(0x00041b1a)]
    HRESULT _stdcall Height([in] double RHS);
    [propget, helpcontext(0x00041b1b)]
    HRESULT _stdcall Index([out, retval] long* RHS);
    [propget, helpcontext(0x00041b1c)]
    HRESULT _stdcall Left([out, retval] double* RHS);
    [propput, helpcontext(0x00041b1c)]
    HRESULT _stdcall Left([in] double RHS);
    [propget, helpcontext(0x00041b1d)]
    HRESULT _stdcall Locked([out, retval] VARIANT_BOOL* RHS);
    [propput, helpcontext(0x00041b1d)]
    HRESULT _stdcall Locked([in] VARIANT_BOOL RHS);
    [propget, helpcontext(0x00041b1e)]
    HRESULT _stdcall Name([out, retval] BSTR* RHS);
    [propput, helpcontext(0x00041b1e)]
    HRESULT _stdcall Name([in] BSTR RHS);
    [propget, hidden, helpcontext(0x00041b1f)]
    HRESULT _stdcall OnAction([out, retval] BSTR* RHS);
    [propput, hidden, helpcontext(0x00041b1f)]
    HRESULT _stdcall OnAction([in] BSTR RHS);
    [propget, helpcontext(0x00041b20)]
    HRESULT _stdcall Placement([out, retval] VARIANT* RHS);
    [propput, helpcontext(0x00041b20)]
    HRESULT _stdcall Placement([in] VARIANT RHS);
    [propget, helpcontext(0x00041b21)]
    HRESULT _stdcall PrintObject([out, retval] VARIANT_BOOL* RHS);
    [propput, helpcontext(0x00041b21)]
    HRESULT _stdcall PrintObject([in] VARIANT_BOOL RHS);
    [helpcontext(0x00041b22)]
    HRESULT _stdcall Select(
                    [in, optional] VARIANT Replace, 
                    [out, retval] VARIANT* RHS);
    [helpcontext(0x00041b23)]
    HRESULT _stdcall SendToBack([out, retval] VARIANT* RHS);
    [propget, helpcontext(0x00041b24)]
    HRESULT _stdcall Top([out, retval] double* RHS);
    [propput, helpcontext(0x00041b24)]
    HRESULT _stdcall Top([in] double RHS);
    [propget, helpcontext(0x00041b25)]
    HRESULT _stdcall TopLeftCell([out, retval] Range** RHS);
    [propget, helpcontext(0x00041b26)]
    HRESULT _stdcall Visible([out, retval] VARIANT_BOOL* RHS);
    [propput, helpcontext(0x00041b26)]
    HRESULT _stdcall Visible([in] VARIANT_BOOL RHS);
    [propget, helpcontext(0x00041b27)]
    HRESULT _stdcall Width([out, retval] double* RHS);
    [propput, helpcontext(0x00041b27)]
    HRESULT _stdcall Width([in] double RHS);
    [propget, helpcontext(0x00041b28)]
    HRESULT _stdcall ZOrder([out, retval] long* RHS);
    [propget, helpcontext(0x00041b29)]
    HRESULT _stdcall ShapeRange([out, retval] ShapeRange** RHS);
    [propget, helpcontext(0x00041ef9)]
    HRESULT _stdcall Caption([out, retval] BSTR* RHS);
    [propput, helpcontext(0x00041ef9)]
    HRESULT _stdcall Caption([in] BSTR RHS);
    [propget, helpcontext(0x00041efa)]
    HRESULT _stdcall Characters(
                    [in, optional] VARIANT Start, 
                    [in, optional] VARIANT Length, 
                    [out, retval] Characters** RHS);
    [helpcontext(0x00041efb)]
    HRESULT _stdcall CheckSpelling(
                    [in, optional] VARIANT CustomDictionary, 
                    [in, optional] VARIANT IgnoreUppercase, 
                    [in, optional] VARIANT AlwaysSuggest, 
                    [in, optional] VARIANT SpellLang, 
                    [out, retval] VARIANT* RHS);
    [propget, helpcontext(0x00041efc)]
    HRESULT _stdcall LockedText([out, retval] VARIANT_BOOL* RHS);
    [propput, helpcontext(0x00041efc)]
    HRESULT _stdcall LockedText([in] VARIANT_BOOL RHS);
    [propget, helpcontext(0x00041efd)]
    HRESULT _stdcall Text([out, retval] BSTR* RHS);
    [propput, helpcontext(0x00041efd)]
    HRESULT _stdcall Text([in] BSTR RHS);
    [propget, helpcontext(0x000422e1)]
    HRESULT _stdcall Accelerator([out, retval] VARIANT* RHS);
    [propput, helpcontext(0x000422e1)]
    HRESULT _stdcall Accelerator([in] VARIANT RHS);
    [propget, helpcontext(0x000422e2)]
    HRESULT _stdcall Border([out, retval] Border** RHS);
    [propget, helpcontext(0x000422e3)]
    HRESULT _stdcall _Default([out, retval] long* RHS);
    [propput, helpcontext(0x000422e3)]
    HRESULT _stdcall _Default([in] long RHS);
    [propget, helpcontext(0x000422e4)]
    HRESULT _stdcall Display3DShading([out, retval] VARIANT_BOOL* RHS);
    [propput, helpcontext(0x000422e4)]
    HRESULT _stdcall Display3DShading([in] VARIANT_BOOL RHS);
    [propget, helpcontext(0x000422e5)]
    HRESULT _stdcall Interior([out, retval] Interior** RHS);
    [propget, helpcontext(0x000422e6)]
    HRESULT _stdcall LinkedCell([out, retval] BSTR* RHS);
    [propput, helpcontext(0x000422e6)]
    HRESULT _stdcall LinkedCell([in] BSTR RHS);
    [propget, helpcontext(0x000422e7)]
    HRESULT _stdcall PhoneticAccelerator([out, retval] VARIANT* RHS);
    [propput, helpcontext(0x000422e7)]
    HRESULT _stdcall PhoneticAccelerator([in] VARIANT RHS);
    [propget, helpcontext(0x000422e8)]
    HRESULT _stdcall Value([out, retval] VARIANT* RHS);
    [propput, helpcontext(0x000422e8)]
    HRESULT _stdcall Value([in] VARIANT RHS);
```
};

[
  odl,
  uuid(00020880-0001-0000-C000-000000000046),
  helpcontext(0x000426c8),
  hidden
]
interface **ICheckBoxes** : IDispatch {
```c
    [propget, helpcontext(0x000426c9)]
    HRESULT _stdcall Application([out, retval] Application** RHS);
    [propget, helpcontext(0x000426ca)]
    HRESULT _stdcall Creator([out, retval] XlCreator* RHS);
    [propget, helpcontext(0x00042ab1)]
    HRESULT _stdcall Parent([out, retval] IDispatch** RHS);
    [restricted, hidden]
    void _stdcall _Dummy3();
    [helpcontext(0x00042ab2)]
    HRESULT _stdcall BringToFront([out, retval] VARIANT* RHS);
    [helpcontext(0x00042ab3)]
    HRESULT _stdcall Copy([out, retval] VARIANT* RHS);
    [helpcontext(0x00042ab4)]
    HRESULT _stdcall CopyPicture(
                    [in, optional, defaultvalue(2)] XlPictureAppearance Appearance, 
                    [in, optional, defaultvalue(-4147)] XlCopyPictureFormat Format, 
                    [out, retval] VARIANT* RHS);
    [helpcontext(0x00042ab5)]
    HRESULT _stdcall Cut([out, retval] VARIANT* RHS);
    [helpcontext(0x00042ab6)]
    HRESULT _stdcall Delete([out, retval] VARIANT* RHS);
    [helpcontext(0x00042ab7)]
    HRESULT _stdcall Duplicate([out, retval] IDispatch** RHS);
    [propget, helpcontext(0x00042ab8)]
    HRESULT _stdcall Enabled([out, retval] VARIANT_BOOL* RHS);
    [propput, helpcontext(0x00042ab8)]
    HRESULT _stdcall Enabled([in] VARIANT_BOOL RHS);
    [propget, helpcontext(0x00042ab9)]
    HRESULT _stdcall Height([out, retval] double* RHS);
    [propput, helpcontext(0x00042ab9)]
    HRESULT _stdcall Height([in] double RHS);
    [restricted, hidden]
    void _stdcall _Dummy12();
    [propget, helpcontext(0x00042aba)]
    HRESULT _stdcall Left([out, retval] double* RHS);
    [propput, helpcontext(0x00042aba)]
    HRESULT _stdcall Left([in] double RHS);
    [propget, helpcontext(0x00042abb)]
    HRESULT _stdcall Locked([out, retval] VARIANT_BOOL* RHS);
    [propput, helpcontext(0x00042abb)]
    HRESULT _stdcall Locked([in] VARIANT_BOOL RHS);
    [restricted, hidden]
    void _stdcall _Dummy15();
    [propget, hidden, helpcontext(0x00042abc)]
    HRESULT _stdcall OnAction([out, retval] BSTR* RHS);
    [propput, hidden, helpcontext(0x00042abc)]
    HRESULT _stdcall OnAction([in] BSTR RHS);
    [propget, helpcontext(0x00042abd)]
    HRESULT _stdcall Placement([out, retval] VARIANT* RHS);
    [propput, helpcontext(0x00042abd)]
    HRESULT _stdcall Placement([in] VARIANT RHS);
    [propget, helpcontext(0x00042abe)]
    HRESULT _stdcall PrintObject([out, retval] VARIANT_BOOL* RHS);
    [propput, helpcontext(0x00042abe)]
    HRESULT _stdcall PrintObject([in] VARIANT_BOOL RHS);
    [helpcontext(0x00042abf)]
    HRESULT _stdcall Select(
                    [in, optional] VARIANT Replace, 
                    [out, retval] VARIANT* RHS);
    [helpcontext(0x00042ac0)]
    HRESULT _stdcall SendToBack([out, retval] VARIANT* RHS);
    [propget, helpcontext(0x00042ac1)]
    HRESULT _stdcall Top([out, retval] double* RHS);
    [propput, helpcontext(0x00042ac1)]
    HRESULT _stdcall Top([in] double RHS);
    [restricted, hidden]
    void _stdcall _Dummy22();
    [propget, helpcontext(0x00042ac2)]
    HRESULT _stdcall Visible([out, retval] VARIANT_BOOL* RHS);
    [propput, helpcontext(0x00042ac2)]
    HRESULT _stdcall Visible([in] VARIANT_BOOL RHS);
    [propget, helpcontext(0x00042ac3)]
    HRESULT _stdcall Width([out, retval] double* RHS);
    [propput, helpcontext(0x00042ac3)]
    HRESULT _stdcall Width([in] double RHS);
    [propget, helpcontext(0x00042ac4)]
    HRESULT _stdcall ZOrder([out, retval] long* RHS);
    [propget, helpcontext(0x00042ac5)]
    HRESULT _stdcall ShapeRange([out, retval] ShapeRange** RHS);
    [propget, helpcontext(0x00042e99)]
    HRESULT _stdcall Caption([out, retval] BSTR* RHS);
    [propput, helpcontext(0x00042e99)]
    HRESULT _stdcall Caption([in] BSTR RHS);
    [propget, helpcontext(0x00042e9a)]
    HRESULT _stdcall Characters(
                    [in, optional] VARIANT Start, 
                    [in, optional] VARIANT Length, 
                    [out, retval] Characters** RHS);
    [helpcontext(0x00042e9b)]
    HRESULT _stdcall CheckSpelling(
                    [in, optional] VARIANT CustomDictionary, 
                    [in, optional] VARIANT IgnoreUppercase, 
                    [in, optional] VARIANT AlwaysSuggest, 
                    [in, optional] VARIANT SpellLang, 
                    [out, retval] VARIANT* RHS);
    [propget, helpcontext(0x00042e9c)]
    HRESULT _stdcall LockedText([out, retval] VARIANT_BOOL* RHS);
    [propput, helpcontext(0x00042e9c)]
    HRESULT _stdcall LockedText([in] VARIANT_BOOL RHS);
    [propget, helpcontext(0x00042e9d)]
    HRESULT _stdcall Text([out, retval] BSTR* RHS);
    [propput, helpcontext(0x00042e9d)]
    HRESULT _stdcall Text([in] BSTR RHS);
    [propget, helpcontext(0x00043281)]
    HRESULT _stdcall Accelerator([out, retval] VARIANT* RHS);
    [propput, helpcontext(0x00043281)]
    HRESULT _stdcall Accelerator([in] VARIANT RHS);
    [propget, helpcontext(0x00043282)]
    HRESULT _stdcall Border([out, retval] Border** RHS);
    [propget, helpcontext(0x00043283)]
    HRESULT _stdcall _Default([out, retval] long* RHS);
    [propput, helpcontext(0x00043283)]
    HRESULT _stdcall _Default([in] long RHS);
    [propget, helpcontext(0x00043284)]
    HRESULT _stdcall Display3DShading([out, retval] VARIANT_BOOL* RHS);
    [propput, helpcontext(0x00043284)]
    HRESULT _stdcall Display3DShading([in] VARIANT_BOOL RHS);
    [propget, helpcontext(0x00043285)]
    HRESULT _stdcall Interior([out, retval] Interior** RHS);
    [propget, helpcontext(0x00043286)]
    HRESULT _stdcall LinkedCell([out, retval] BSTR* RHS);
    [propput, helpcontext(0x00043286)]
    HRESULT _stdcall LinkedCell([in] BSTR RHS);
    [propget, helpcontext(0x00043287)]
    HRESULT _stdcall PhoneticAccelerator([out, retval] VARIANT* RHS);
    [propput, helpcontext(0x00043287)]
    HRESULT _stdcall PhoneticAccelerator([in] VARIANT RHS);
    [propget, helpcontext(0x00043288)]
    HRESULT _stdcall Value([out, retval] VARIANT* RHS);
    [propput, helpcontext(0x00043288)]
    HRESULT _stdcall Value([in] VARIANT RHS);
    [helpcontext(0x0004366d)]
    HRESULT _stdcall Add(
                    [in] double Left, 
                    [in] double Top, 
                    [in] double Width, 
                    [in] double Height, 
                    [out, retval] CheckBox** RHS);
    [propget, helpcontext(0x0004366e)]
    HRESULT _stdcall Count([out, retval] long* RHS);
    [helpcontext(0x0004366f)]
    HRESULT _stdcall Group([out, retval] GroupObject** RHS);
    [helpcontext(0x00043670)]
    HRESULT _stdcall Item(
                    [in] VARIANT Index, 
                    [out, retval] IDispatch** RHS);
    [helpcontext(0x00043671)]
    HRESULT _stdcall _NewEnum([out, retval] IUnknown** RHS);
```
};



[
  uuid(0002087F-0000-0000-C000-000000000046),
  helpcontext(0x00041728),
  hidden
]
dispinterface **CheckBox** {
```c
    properties:
    methods:
        [id(0x60000000), restricted]
        void QueryInterface(
                        [in] GUID* riid, 
                        [out] void** ppvObj);
        [id(0x60000001), restricted]
        unsigned long AddRef();
        [id(0x60000002), restricted]
        unsigned long Release();
        [id(0x60010000), restricted]
        void GetTypeInfoCount([out] unsigned int* pctinfo);
        [id(0x60010001), restricted]
        void GetTypeInfo(
                        [in] unsigned int itinfo, 
                        [in] unsigned long lcid, 
                        [out] void** pptinfo);
        [id(0x60010002), restricted]
        void GetIDsOfNames(
                        [in] GUID* riid, 
                        [in] char** rgszNames, 
                        [in] unsigned int cNames, 
                        [in] unsigned long lcid, 
                        [out] long* rgdispid);
        [id(0x60010003), restricted]
        void Invoke(
                        [in] long dispidMember, 
                        [in] GUID* riid, 
                        [in] unsigned long lcid, 
                        [in] unsigned short wFlags, 
                        [in] DISPPARAMS* pdispparams, 
                        [out] VARIANT* pvarResult, 
                        [out] EXCEPINFO* pexcepinfo, 
                        [out] unsigned int* puArgErr);
        [id(0x00000094), propget, helpcontext(0x00041729)]
        Application* Application();
        [id(0x00000095), propget, helpcontext(0x0004172a)]
        XlCreator Creator();
        [id(0x00000096), propget, helpcontext(0x00041b11)]
        IDispatch* Parent();
        [id(0x00000267), propget, helpcontext(0x00041b12)]
        Range* BottomRightCell();
        [id(0x0000025a), helpcontext(0x00041b13)]
        VARIANT BringToFront();
        [id(0x00000227), helpcontext(0x00041b14)]
        VARIANT Copy();
        [id(0x000000d5), helpcontext(0x00041b15)]
        VARIANT CopyPicture(
                        [in, optional, defaultvalue(2)] XlPictureAppearance Appearance, 
                        [in, optional, defaultvalue(-4147)] XlCopyPictureFormat Format);
        [id(0x00000235), helpcontext(0x00041b16)]
        VARIANT Cut();
        [id(0x00000075), helpcontext(0x00041b17)]
        VARIANT Delete();
        [id(0x0000040f), helpcontext(0x00041b18)]
        IDispatch* Duplicate();
        [id(0x00000258), propget, helpcontext(0x00041b19)]
        VARIANT_BOOL Enabled();
        [id(0x00000258), propput, helpcontext(0x00041b19)]
        void Enabled([in] VARIANT_BOOL rhs);
        [id(0x0000007b), propget, helpcontext(0x00041b1a)]
        double Height();
        [id(0x0000007b), propput, helpcontext(0x00041b1a)]
        void Height([in] double rhs);
        [id(0x000001e6), propget, helpcontext(0x00041b1b)]
        long Index();
        [id(0x0000007f), propget, helpcontext(0x00041b1c)]
        double Left();
        [id(0x0000007f), propput, helpcontext(0x00041b1c)]
        void Left([in] double rhs);
        [id(0x0000010d), propget, helpcontext(0x00041b1d)]
        VARIANT_BOOL Locked();
        [id(0x0000010d), propput, helpcontext(0x00041b1d)]
        void Locked([in] VARIANT_BOOL rhs);
        [id(0x0000006e), propget, helpcontext(0x00041b1e)]
        BSTR Name();
        [id(0x0000006e), propput, helpcontext(0x00041b1e)]
        void Name([in] BSTR rhs);
        [id(0x00000254), propget, hidden, helpcontext(0x00041b1f)]
        BSTR OnAction();
        [id(0x00000254), propput, hidden, helpcontext(0x00041b1f)]
        void OnAction([in] BSTR rhs);
        [id(0x00000269), propget, helpcontext(0x00041b20)]
        VARIANT Placement();
        [id(0x00000269), propput, helpcontext(0x00041b20)]
        void Placement([in] VARIANT rhs);
        [id(0x0000026a), propget, helpcontext(0x00041b21)]
        VARIANT_BOOL PrintObject();
        [id(0x0000026a), propput, helpcontext(0x00041b21)]
        void PrintObject([in] VARIANT_BOOL rhs);
        [id(0x000000eb), helpcontext(0x00041b22)]
        VARIANT Select([in, optional] VARIANT Replace);
        [id(0x0000025d), helpcontext(0x00041b23)]
        VARIANT SendToBack();
        [id(0x0000007e), propget, helpcontext(0x00041b24)]
        double Top();
        [id(0x0000007e), propput, helpcontext(0x00041b24)]
        void Top([in] double rhs);
        [id(0x0000026c), propget, helpcontext(0x00041b25)]
        Range* TopLeftCell();
        [id(0x0000022e), propget, helpcontext(0x00041b26)]
        VARIANT_BOOL Visible();
        [id(0x0000022e), propput, helpcontext(0x00041b26)]
        void Visible([in] VARIANT_BOOL rhs);
        [id(0x0000007a), propget, helpcontext(0x00041b27)]
        double Width();
        [id(0x0000007a), propput, helpcontext(0x00041b27)]
        void Width([in] double rhs);
        [id(0x0000026e), propget, helpcontext(0x00041b28)]
        long ZOrder();
        [id(0x000005f8), propget, helpcontext(0x00041b29)]
        ShapeRange* ShapeRange();
        [id(0x0000008b), propget, helpcontext(0x00041ef9)]
        BSTR Caption();
        [id(0x0000008b), propput, helpcontext(0x00041ef9)]
        void Caption([in] BSTR rhs);
        [id(0x0000025b), propget, helpcontext(0x00041efa)]
        Characters* Characters(
                        [in, optional] VARIANT Start, 
                        [in, optional] VARIANT Length);
        [id(0x000001f9), helpcontext(0x00041efb)]
        VARIANT CheckSpelling(
                        [in, optional] VARIANT CustomDictionary, 
                        [in, optional] VARIANT IgnoreUppercase, 
                        [in, optional] VARIANT AlwaysSuggest, 
                        [in, optional] VARIANT SpellLang);
        [id(0x00000268), propget, helpcontext(0x00041efc)]
        VARIANT_BOOL LockedText();
        [id(0x00000268), propput, helpcontext(0x00041efc)]
        void LockedText([in] VARIANT_BOOL rhs);
        [id(0x0000008a), propget, helpcontext(0x00041efd)]
        BSTR Text();
        [id(0x0000008a), propput, helpcontext(0x00041efd)]
        void Text([in] BSTR rhs);
        [id(0x0000034e), propget, helpcontext(0x000422e1)]
        VARIANT Accelerator();
        [id(0x0000034e), propput, helpcontext(0x000422e1)]
        void Accelerator([in] VARIANT rhs);
        [id(0x00000080), propget, helpcontext(0x000422e2)]
        Border* Border();
        [id(00000000), propget, helpcontext(0x000422e3)]
        long _Default();
        [id(00000000), propput, helpcontext(0x000422e3)]
        void _Default([in] long rhs);
        [id(0x00000462), propget, helpcontext(0x000422e4)]
        VARIANT_BOOL Display3DShading();
        [id(0x00000462), propput, helpcontext(0x000422e4)]
        void Display3DShading([in] VARIANT_BOOL rhs);
        [id(0x00000081), propget, helpcontext(0x000422e5)]
        Interior* Interior();
        [id(0x00000422), propget, helpcontext(0x000422e6)]
        BSTR LinkedCell();
        [id(0x00000422), propput, helpcontext(0x000422e6)]
        void LinkedCell([in] BSTR rhs);
        [id(0x00000461), propget, helpcontext(0x000422e7)]
        VARIANT PhoneticAccelerator();
        [id(0x00000461), propput, helpcontext(0x000422e7)]
        void PhoneticAccelerator([in] VARIANT rhs);
        [id(0x00000006), propget, helpcontext(0x000422e8)]
        VARIANT Value();
        [id(0x00000006), propput, helpcontext(0x000422e8)]
        void Value([in] VARIANT rhs);
 ```
};

[
  uuid(00020880-0000-0000-C000-000000000046),
  helpcontext(0x000426c8),
  hidden
]
dispinterface **CheckBoxes** {
```c
    properties:
    methods:
        [id(0x60000000), restricted]
        void QueryInterface(
                        [in] GUID* riid, 
                        [out] void** ppvObj);
        [id(0x60000001), restricted]
        unsigned long AddRef();
        [id(0x60000002), restricted]
        unsigned long Release();
        [id(0x60010000), restricted]
        void GetTypeInfoCount([out] unsigned int* pctinfo);
        [id(0x60010001), restricted]
        void GetTypeInfo(
                        [in] unsigned int itinfo, 
                        [in] unsigned long lcid, 
                        [out] void** pptinfo);
        [id(0x60010002), restricted]
        void GetIDsOfNames(
                        [in] GUID* riid, 
                        [in] char** rgszNames, 
                        [in] unsigned int cNames, 
                        [in] unsigned long lcid, 
                        [out] long* rgdispid);
        [id(0x60010003), restricted]
        void Invoke(
                        [in] long dispidMember, 
                        [in] GUID* riid, 
                        [in] unsigned long lcid, 
                        [in] unsigned short wFlags, 
                        [in] DISPPARAMS* pdispparams, 
                        [out] VARIANT* pvarResult, 
                        [out] EXCEPINFO* pexcepinfo, 
                        [out] unsigned int* puArgErr);
        [id(0x00000094), propget, helpcontext(0x000426c9)]
        Application* Application();
        [id(0x00000095), propget, helpcontext(0x000426ca)]
        XlCreator Creator();
        [id(0x00000096), propget, helpcontext(0x00042ab1)]
        IDispatch* Parent();
        [id(0x00010003), restricted, hidden]
        void _Dummy3();
        [id(0x0000025a), helpcontext(0x00042ab2)]
        VARIANT BringToFront();
        [id(0x00000227), helpcontext(0x00042ab3)]
        VARIANT Copy();
        [id(0x000000d5), helpcontext(0x00042ab4)]
        VARIANT CopyPicture(
                        [in, optional, defaultvalue(2)] XlPictureAppearance Appearance, 
                        [in, optional, defaultvalue(-4147)] XlCopyPictureFormat Format);
        [id(0x00000235), helpcontext(0x00042ab5)]
        VARIANT Cut();
        [id(0x00000075), helpcontext(0x00042ab6)]
        VARIANT Delete();
        [id(0x0000040f), helpcontext(0x00042ab7)]
        IDispatch* Duplicate();
        [id(0x00000258), propget, helpcontext(0x00042ab8)]
        VARIANT_BOOL Enabled();
        [id(0x00000258), propput, helpcontext(0x00042ab8)]
        void Enabled([in] VARIANT_BOOL rhs);
        [id(0x0000007b), propget, helpcontext(0x00042ab9)]
        double Height();
        [id(0x0000007b), propput, helpcontext(0x00042ab9)]
        void Height([in] double rhs);
        [id(0x0001000c), restricted, hidden]
        void _Dummy12();
        [id(0x0000007f), propget, helpcontext(0x00042aba)]
        double Left();
        [id(0x0000007f), propput, helpcontext(0x00042aba)]
        void Left([in] double rhs);
        [id(0x0000010d), propget, helpcontext(0x00042abb)]
        VARIANT_BOOL Locked();
        [id(0x0000010d), propput, helpcontext(0x00042abb)]
        void Locked([in] VARIANT_BOOL rhs);
        [id(0x0001000f), restricted, hidden]
        void _Dummy15();
        [id(0x00000254), propget, hidden, helpcontext(0x00042abc)]
        BSTR OnAction();
        [id(0x00000254), propput, hidden, helpcontext(0x00042abc)]
        void OnAction([in] BSTR rhs);
        [id(0x00000269), propget, helpcontext(0x00042abd)]
        VARIANT Placement();
        [id(0x00000269), propput, helpcontext(0x00042abd)]
        void Placement([in] VARIANT rhs);
        [id(0x0000026a), propget, helpcontext(0x00042abe)]
        VARIANT_BOOL PrintObject();
        [id(0x0000026a), propput, helpcontext(0x00042abe)]
        void PrintObject([in] VARIANT_BOOL rhs);
        [id(0x000000eb), helpcontext(0x00042abf)]
        VARIANT Select([in, optional] VARIANT Replace);
        [id(0x0000025d), helpcontext(0x00042ac0)]
        VARIANT SendToBack();
        [id(0x0000007e), propget, helpcontext(0x00042ac1)]
        double Top();
        [id(0x0000007e), propput, helpcontext(0x00042ac1)]
        void Top([in] double rhs);
        [id(0x00010016), restricted, hidden]
        void _Dummy22();
        [id(0x0000022e), propget, helpcontext(0x00042ac2)]
        VARIANT_BOOL Visible();
        [id(0x0000022e), propput, helpcontext(0x00042ac2)]
        void Visible([in] VARIANT_BOOL rhs);
        [id(0x0000007a), propget, helpcontext(0x00042ac3)]
        double Width();
        [id(0x0000007a), propput, helpcontext(0x00042ac3)]
        void Width([in] double rhs);
        [id(0x0000026e), propget, helpcontext(0x00042ac4)]
        long ZOrder();
        [id(0x000005f8), propget, helpcontext(0x00042ac5)]
        ShapeRange* ShapeRange();
        [id(0x0000008b), propget, helpcontext(0x00042e99)]
        BSTR Caption();
        [id(0x0000008b), propput, helpcontext(0x00042e99)]
        void Caption([in] BSTR rhs);
        [id(0x0000025b), propget, helpcontext(0x00042e9a)]
        Characters* Characters(
                        [in, optional] VARIANT Start, 
                        [in, optional] VARIANT Length);
        [id(0x000001f9), helpcontext(0x00042e9b)]
        VARIANT CheckSpelling(
                        [in, optional] VARIANT CustomDictionary, 
                        [in, optional] VARIANT IgnoreUppercase, 
                        [in, optional] VARIANT AlwaysSuggest, 
                        [in, optional] VARIANT SpellLang);
        [id(0x00000268), propget, helpcontext(0x00042e9c)]
        VARIANT_BOOL LockedText();
        [id(0x00000268), propput, helpcontext(0x00042e9c)]
        void LockedText([in] VARIANT_BOOL rhs);
        [id(0x0000008a), propget, helpcontext(0x00042e9d)]
        BSTR Text();
        [id(0x0000008a), propput, helpcontext(0x00042e9d)]
        void Text([in] BSTR rhs);
        [id(0x0000034e), propget, helpcontext(0x00043281)]
        VARIANT Accelerator();
        [id(0x0000034e), propput, helpcontext(0x00043281)]
        void Accelerator([in] VARIANT rhs);
        [id(0x00000080), propget, helpcontext(0x00043282)]
        Border* Border();
        [id(00000000), propget, helpcontext(0x00043283)]
        long _Default();
        [id(00000000), propput, helpcontext(0x00043283)]
        void _Default([in] long rhs);
        [id(0x00000462), propget, helpcontext(0x00043284)]
        VARIANT_BOOL Display3DShading();
        [id(0x00000462), propput, helpcontext(0x00043284)]
        void Display3DShading([in] VARIANT_BOOL rhs);
        [id(0x00000081), propget, helpcontext(0x00043285)]
        Interior* Interior();
        [id(0x00000422), propget, helpcontext(0x00043286)]
        BSTR LinkedCell();
        [id(0x00000422), propput, helpcontext(0x00043286)]
        void LinkedCell([in] BSTR rhs);
        [id(0x00000461), propget, helpcontext(0x00043287)]
        VARIANT PhoneticAccelerator();
        [id(0x00000461), propput, helpcontext(0x00043287)]
        void PhoneticAccelerator([in] VARIANT rhs);
        [id(0x00000006), propget, helpcontext(0x00043288)]
        VARIANT Value();
        [id(0x00000006), propput, helpcontext(0x00043288)]
        void Value([in] VARIANT rhs);
        [id(0x000000b5), helpcontext(0x0004366d)]
        CheckBox* Add(
                        [in] double Left, 
                        [in] double Top, 
                        [in] double Width, 
                        [in] double Height);
        [id(0x00000076), propget, helpcontext(0x0004366e)]
        long Count();
        [id(0x0000002e), helpcontext(0x0004366f)]
        GroupObject* Group();
        [id(0x000000aa), helpcontext(0x00043670)]
        IDispatch* Item([in] VARIANT Index);
        [id(0xfffffffc), helpcontext(0x00043671)]
        IUnknown* _NewEnum();
 ```
};


------------------------------
QAxObject 设置 CheckBox
7-Zip可以打开xlsx文件，查看sheet1.xml
 
```cpp
   QAxObject *workSheet = workBook->querySubObject("WorkSheets(int)", 1);
   QAxObject *checkbox1 = workSheet->querySubObject("CheckBox1");//MSForms
   if (checkbox1)
   { 
       QAxBase::PropertyBag pbag = checkbox1->propertyBag();
       for (auto mit = pbag.begin(); mit != pbag.end(); ++mit)
       {
           qDebug() << mit.key() << mit.value();
           //"Caption" QVariant(QString, "xxx")
           //"Value" QVariant(QString, "0")
       }
       QVariant ret = checkbox1->dynamicCall("Value", QVariant("1"));
       //qDebug() << ret;
   }
   //------
   QAxObject *checkbox3 = workSheet->querySubObject("CheckBoxes(\"Check Box 3\")");//Excel
   if (checkbox3)
   {
       QAxBase::PropertyBag pbag = checkbox3->propertyBag();
       for (auto mit = pbag.begin(); mit != pbag.end(); ++mit)
       {
           qDebug() << mit.key() << mit.value();
           //"Caption" QVariant(QString, "yyy")
           //"Value" QVariant(int, -4146)       
       }
       QVariant ret = checkbox3->dynamicCall("Value", QVariant( 1 ));
      //qDebug() << ret;
   }
```
