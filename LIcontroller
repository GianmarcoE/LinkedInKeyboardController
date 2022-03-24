from pynput.keyboard import Listener, Key
import pyautogui
import time
import sys
import os
import tkinter as tk
from tkinter import filedialog
from tkinter.messagebox import showinfo
from tkinter import *
from tkinter.ttk import *

try:
    from ctypes import windll
    windll.shcore.SetProcessDpiAwareness(1)
except:
    pass

root= tk.Tk()

root.title('LinkedIn Controller')

root.geometry('450x220')
root.minsize(450, 220)
root.configure(background='#fff')

def on_press(key):

    try:

        if key == Key.up:  
            pyautogui.scroll(55)
        elif key == Key.down:  
            pyautogui.scroll(-50)
        elif key == Key.right:  
            pyautogui.click(1798, 202)
            time.sleep(1)
            pyautogui.click(1259, 857)
        elif key == Key.left:  
            pyautogui.click(1566, 202)
            time.sleep(1)
            pyautogui.click(1259, 857)
        elif key == Key.enter:          #save profile to project/archive
            pyautogui.scroll(6000)
            time.sleep(0.2)
            pyautogui.click(802, 621) #702 x to save
            #pyautogui.click(802, 651)
            pyautogui.click(802, 591)
        elif key == Key.page_up:           #click mouse
            pyautogui.click()
        elif key == Key.page_down:          #save to another project
            pyautogui.scroll(6000)
            pyautogui.click(1087, 621)
            time.sleep(0.5)
            pyautogui.click(973, 825)
            time.sleep(1)
            pyautogui.click(1581, 470)
        elif key.char == "'":          #close and refresh
            pyautogui.click(1884, 202)
            time.sleep(1.5)
            pyautogui.click(126, 77)
            time.sleep(10)
            pyautogui.click(690, 623)
            pyautogui.moveTo(1259, 857)
        elif key.char == ";":           #rejects with message from other app
            os.chdir("C:\\Users\\ercolani\\OneDrive - TomTom\\Desktop")
            os.system("rejector.pyw")
        elif key.char == ".":           #rejects with message from other app
            os.chdir("C:\\Users\\ercolani\\OneDrive - TomTom\\Desktop")
            os.system("scheduler.pyw")
            
##            pyautogui.moveTo(1123, 601)
##            pyautogui.click()
##            pyautogui.scroll(6000)
##            time.sleep(0.2)
##            pyautogui.doubleClick(653, 518)
##            pyautogui.hotkey('ctrl', 'c')
##            pyautogui.click(863, 871)
##            pyautogui.write("Hi ")
##            pyautogui.hotkey('ctrl', 'v')
##            pyautogui.write(",\n\nI understand, thank you for letting me know anyway.\n\nKind Regards,\n\nGianmarco")
        else:
            pass

    except:
            
        window = tk.Toplevel()
        window.configure(background='#fff')

        label = Label(window, text="The controller is paused.\nDo you want to resume?", font=('helvetica 12'), foreground='#333', background="#fff")
        label.grid(row=0, padx=50, pady=50, columnspan=2)

        var = tk.IntVar()
        
        button = tk.Button(window, text="Yes", command=lambda: var.set(1), bg='#fff')
        button.grid(row=1, column=0, sticky='EW')
        
        button = tk.Button(window, text="No", command=lambda: var.set(2), bg='#fff')
        button.grid(row=1, column=1, sticky='EW')

        button.wait_variable(var)

        if var.get() == 1:
            window.destroy()
            return
        elif var.get() == 2:
            root.destroy()

        window.columnconfigure(0, weight=1)
        window.columnconfigure(1, weight=1)

def descript ():
        window = tk.Toplevel()
        window.title('Guide')
        window.configure(background='#fff')
        window.geometry('300x430')

        arrowup = Label(window, text="\u2191", font=('helvetica 10'), foreground='#555', background='#fff')
        arrowup.grid(row=0, column=0, pady=(10, 0))
        arrowupdesc = Label(window, text="Scroll up", font=('helvetica 10'), foreground='#555', background='#fff')
        arrowupdesc.grid(row=0, column=1, pady=(15, 0))

        arrowdown = Label(window, text="\u2193", font=('helvetica 10'), foreground='#555', background='#fff')
        arrowdown.grid(row=1, column=0, pady=(10, 0))
        arrowdowndesc = Label(window, text="Scroll down", font=('helvetica 10'), foreground='#555', background='#fff')
        arrowdowndesc.grid(row=1, column=1, pady=(15, 0))

        arrowdx = Label(window, text="\u2192", font=('helvetica 10'), foreground='#555', background='#fff')
        arrowdx.grid(row=2, column=0, pady=(10, 0))
        arrowdxdesc = Label(window, text="Next profile", font=('helvetica 10'), foreground='#555', background='#fff')
        arrowdxdesc.grid(row=2, column=1, pady=(15, 0))

        arrowsx = Label(window, text="\u2190", font=('helvetica 10'), foreground='#555', background='#fff')
        arrowsx.grid(row=3, column=0, pady=(10, 0))
        arrowsxdesc = Label(window, text="Prev profile", font=('helvetica 10'), foreground='#555', background='#fff')
        arrowsxdesc.grid(row=3, column=1, pady=(15, 0))

        entercom = Label(window, text="\u23ce", font=('helvetica 10'), foreground='#555', background='#fff')
        entercom.grid(row=4, column=0, pady=(10, 0))
        entercom = Label(window, text="Save profile", font=('helvetica 10'), foreground='#555', background='#fff')
        entercom.grid(row=4, column=1, pady=(15, 0))

        clickcom = Label(window, text="Pg Up", font=('helvetica 10'), foreground='#555', background='#fff')
        clickcom.grid(row=5, column=0, pady=(10, 0))
        clickcom = Label(window, text="Left click", font=('helvetica 10'), foreground='#555', background='#fff')
        clickcom.grid(row=5, column=1, pady=(15, 0))

        dotcom = Label(window, text="Pg Down", font=('helvetica 10'), foreground='#555', background='#fff')
        dotcom.grid(row=6, column=0, pady=(10, 0))
        dotcom = Label(window, text="Save to another project", font=('helvetica 10'), foreground='#555', background='#fff')
        dotcom.grid(row=6, column=1, pady=(15, 0))

        refreshcom = Label(window, text="'", font=('helvetica 13'), foreground='#555', background='#fff')
        refreshcom.grid(row=7, column=0, pady=(10, 0))
        refreshcom = Label(window, text="Refresh list", font=('helvetica 10'), foreground='#555', background='#fff')
        refreshcom.grid(row=7, column=1, pady=(15, 0))

        shiftcom = Label(window, text="Shift", font=('helvetica 10'), foreground='#555', background='#fff')
        shiftcom.grid(row=8, column=0, pady=(10, 0))
        shiftcom = Label(window, text="Pause", font=('helvetica 10'), foreground='#555', background='#fff')
        shiftcom.grid(row=8, column=1, pady=(15, 0))

        semicocom = Label(window, text=";", font=('helvetica 13'), foreground='#555', background='#fff')
        semicocom.grid(row=9, column=0, pady=(10, 0))
        semicocom = Label(window, text="Thank candidate", font=('helvetica 10'), foreground='#555', background='#fff')
        semicocom.grid(row=9, column=1, pady=(15, 0))

        window.columnconfigure(0, weight=1)
        window.columnconfigure(1, weight=1)

infolbl = Label(root, text="TomTom", font=('helvetica 8 bold'), foreground='#555', background='#fff')
infolbl.grid(row=0, sticky='W', padx=(10, 0))
Separator(root, orient="horizontal")
Separator().grid(row=0, column= 0, pady= (20, 0), sticky=EW, columnspan=2)

message = Label(root, text = "The app is up and running \u263a", font=('helvetica 12'), foreground='#333', background='#fff')
message.grid(row=1, column=0, padx= 15, pady=(50, 0))
message2 = Label(root, text = "Control LinkedIn with your keyboard!", font=('helvetica 12'), foreground='#333', background='#fff')
message2.grid(row=2, column=0, padx= 15, pady=(10, 0))

instructions = tk.Button(root, text="Instructions", font=('helvetica 8'), command=descript, foreground='#555', background='#fff', highlightthickness = 0, bd = 0)
instructions.grid(row=3, sticky='W', padx=(10, 0), pady=(50, 10))

signature = Label(root, text="By Gianmarco Ercolani", font=('helvetica 7 bold'), foreground='#555', background='#fff')
signature.grid(row=3, sticky='E', padx=(0, 10), pady=(50, 10))

root.columnconfigure(0, weight=1)

with Listener(on_press=on_press) as listener:  # Setup the listener
    root.mainloop()
    listener.join()  # Join the thread to the main thread
