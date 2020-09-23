<div align="center">

## a very small picture viewer in one minute\.


</div>

### Description

Your own homemade picture viewer in ONE minute, supports at least jpg, gif, bmp, pcx & many others
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Happy Coder](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/happy-coder.md)
**Level**          |Unknown
**User Rating**    |2.7 (19 globes from 7 users)
**Compatibility**  |VB 4\.0 \(16\-bit\), VB 4\.0 \(32\-bit\), VB 5\.0, VB 6\.0
**Category**       |[Complete Applications](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/complete-applications__1-27.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/happy-coder-a-very-small-picture-viewer-in-one-minute__1-2487/archive/master.zip)





### Source Code

```
'add following code to your form
VERSION 4.00
Begin VB.Form Form1
 Caption  = "Very simple picture viewer"
 ClientHeight = 9450
 ClientLeft = 1140
 ClientTop = 1515
 ClientWidth = 11460
 Height  = 9855
 Left  = 1080
 LinkTopic = "Form1"
 ScaleHeight = 9450
 ScaleWidth = 11460
 Top  = 1170
 Width  = 11580
 Begin VB.PictureBox Picture1
 AutoSize = -1 'True
 Height  = 9135
 Left  = 1680
 ScaleHeight = 9075
 ScaleWidth = 9675
 TabIndex = 3
 Top  = 120
 Width  = 9735
 End
 Begin VB.FileListBox File1
 Height  = 6300
 Left  = 0
 TabIndex = 2
 Top  = 3000
 Width  = 1575
 End
 Begin VB.DirListBox Dir1
 Height  = 2505
 Left  = 0
 TabIndex = 1
 Top  = 480
 Width  = 1575
 End
 Begin VB.DriveListBox Drive1
 Height  = 315
 Left  = 0
 TabIndex = 0
 Top  = 120
 Width  = 1575
 End
End
Attribute VB_Name = "Form1"
Attribute VB_Creatable = False
Attribute VB_Exposed = False
Private Sub Dir1_Change()
File1.Path = Dir1.Path
End Sub
Private Sub Drive1_Change()
Dir1.Path = Drive1.Drive
End Sub
Private Sub File1_Click()
On Error Resume Next ' if not supported picture format, don't show it
Picture1.Picture = LoadPicture(Dir1.Path + "\" + File1.filename)
End Sub
```

