```
#NoEnv
#Persistent
#SingleInstance, force
SetMouseDelay, 10
SendMode, event

#IfWinActive Path of Exile

f12:: ;<- use the f12 key to start/stop the clicking routine

clicktoggle := !clicktoggle

if (!clicktoggle)
{ SetTimer, startclick, off
  tooltip
  return
}

; drops through into the click timer

startclick:
Random R, 27193, 271317
a := round(R / 1000, 2)
tooltip, auto-clicking is on %a%s
click
SetTimer, startclick, %R%
return

; Esc:: Exitapp ; use the esc key to end the script
```

![image](https://user-images.githubusercontent.com/899183/232332550-27395d2d-470a-4e24-85cf-5761e4c59a01.png)

press F12 to toggle on/off the script. it'll click once where the mouse was left off.
