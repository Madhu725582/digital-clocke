import tkinter as tk
from time import strftime
root = tk.Tk()
root.title("Digital Clock")
label = tk.Label(root, font=('calibri', 50, 'bold'), background='yellow', foreground='black')
label.pack(anchor='center')
def timeI():
    string = strftime('%H:%M:%S %p %d/%m/%Y') 
    label.config(text=string)
    label.after(1000, timeI)  
timeI()
root.mainloop()
