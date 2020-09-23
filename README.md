<div align="center">

## Image Flipping


</div>

### Description

Explains on How to Flip Images to 270 Degrees
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[manikantan](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/manikantan.md)
**Level**          |Advanced
**User Rating**    |5.0 (15 globes from 3 users)
**Compatibility**  |VB 5\.0
**Category**       |[Graphics](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/graphics__1-46.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/manikantan-image-flipping__1-12294/archive/master.zip)





### Source Code

```
Article Written by
Manikantan
3rd Agenda,
Web Development,
India.
Website:www.3rdagenda.com
Email:manikantan@3rdagenda.com
Image Flipping
Another use of Visual Basic is the Flipping Images using the Paintpicture.Used to Flip the images around the Center either for 90 180 270 degrees.Can be useful in DTP works.
PaintPicture is the most useful method of the pciturebox control which takes 10 Arguments to give various Effects to still images the Arguments are
1) Source Picture
2) Dest X
3) Dest Y
4) Dest Width
5) Dest Height
6) Source X
7) Source Y
8) Source Width
9) Source Height
10)Operation code.
Private Sub Cmd_hflip_Click()
        picture_dest.PaintPicture picture_src.Picture, 0, 0, picture_src.ScaleWidth, picture_src.ScaleHeight, picture_src.ScaleWidth, 0, -picture_src.ScaleWidth, picture_src.ScaleHeight, &HCC0020
End Sub
Private Sub Cmd_vflip_Click()
        picture_dest.PaintPicture picture_src.Picture, 0, 0, picture_src.ScaleWidth, picture_src.ScaleHeight, 0, picture_src.ScaleHeight, picture_src.ScaleWidth, -picture_src.ScaleHeight, &HCC0020
End Sub
Private Sub Cmd_load_Click()
    On Error Resume Next
    CommonDialog.ShowOpen
    picture_src.Picture = LoadPicture(CommonDialog1.filename)
    If Err.Number = 481 Then MsgBox ("The File Mentioned By You Is not A image file")
End Sub
Private Sub Cmd_save_Click()
	CommonDialog1.ShowSave
	SavePicture picture_dest.Image, CommonDialog1.filename
End Sub
Private Sub Cmd_exit_Click()
	Unload Me
End Sub
Private Sub Rotate_Click()
      picture_dest.PaintPicture picture_src.Picture, 0, 0, picture_src.ScaleWidth, picture_src.ScaleHeight, picture_src.ScaleWidth, picture_src.ScaleHeight, -picture_src.ScaleWidth, -picture_src.ScaleHeight, &HCC0020
End Sub
Articel by
Manikantan
Email:manikantan@3rdagenda.com
```

