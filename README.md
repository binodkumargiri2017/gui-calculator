# gui-calculator



from tkinter import *
window =Tk()
window.title("calculator")
window.geometry("400x500")

def button_press(num):
    global equation_text

    equation_text=equation_text+str(num)
    equation_label.set(equation_text)

def equal():
    global equation_text
    try:

       total = str(eval(equation_text))
       equation_label.set(total)
       equation_text=total
    except SyntaxError:
        equation_label.set("syntax error")

    except ZeroDivisionError:
        equation_label.set("INFINITE")


def clear():
    global equation_text
    equation_label.set("")
    equation_text=""



equation_text=""

equation_label=StringVar()

label=Label(window,textvariable=equation_label,font=("Arial",20,"bold"),bg="#BDC4D1",width=20)
label.pack()

frame=Frame(window)
frame.pack()
button1=Button(frame,text="1",command=lambda:button_press(1),height=2,width=10,bg="#F59AF9",
               font=("Arial",10,"bold"))
button1.grid(row=0,column=0)

button2=Button(frame,text="2",command=lambda:button_press(2),height=2,width=10,
               bg="#F59AF9",
               font=("Arial", 10, "bold")
               )
button2.grid(row=0,column=1)

button3=Button(frame,text="3",command=lambda:button_press(3),height=2,width=10
               ,bg="#F59AF9",
               font=("Arial",10,"bold"))
button3.grid(row=0,column=2)

button4=Button(frame,text="4",command=lambda:button_press(4),height=2,width=10,
               bg="#F59AF9",
               font=("Arial", 10, "bold")
               )
button4.grid(row=1,column=0)

button5=Button(frame,text="5",command=lambda:button_press(5),height=2,width=10,
               bg="#F59AF9",
               font=("Arial", 10, "bold")
               )
button5.grid(row=1,column=1)

button6=Button(frame,text="6",command=lambda:button_press(6),height=2,width=10,
               bg="#F59AF9",
               font=("Arial", 10, "bold")
               )
button6.grid(row=1,column=2)

button7=Button(frame,text="7",command=lambda:button_press(7),height=2,width=10,
               bg="#F59AF9",
               font=("Arial", 10, "bold")
               )
button7.grid(row=2,column=0)

button8=Button(frame,text="8",command=lambda:button_press(8),height=2,width=10
               ,bg="#F59AF9",
               font=("Arial",10,"bold"))
button8.grid(row=2,column=1)

button9=Button(frame,text="9",command=lambda:button_press(9),height=2,width=10,
               bg="#F59AF9",
               font=("Arial", 10, "bold")
               )
button9.grid(row=2,column=2)

button10=Button(frame,text="0",command=lambda:button_press(0),height=2,width=10,
                bg="#F59AF9",
                font=("Arial", 10, "bold")
                )
button10.grid(row=3,column=0)

plus=Button(frame,text="+",command=lambda:button_press("+"),height=2,width=10
            ,bg="#F59AF9",
               font=("Arial",10,"bold"))
plus.grid(row=0,column=4)

minus=Button(frame,text="-",command=lambda:button_press("-"),height=2,width=10
             ,bg="#F59AF9",
               font=("Arial",10,"bold"))
minus.grid(row=1,column=4)

divide=Button(frame,text="/",command=lambda:button_press("/"),height=2,width=10
              ,bg="#F59AF9",
               font=("Arial",10,"bold"))
divide.grid(row=2,column=4)

multiply=Button(frame,text="*",command=lambda:button_press("*"),height=2,width=10
                ,bg="#F59AF9",
               font=("Arial",10,"bold"))
multiply.grid(row=3,column=4)

equal=Button(frame,text="=",command=equal,height=2,width=10
             ,bg="#F59AF9",
               font=("Arial",10,"bold"))
equal.grid(row=4,column=4)

clear=Button(frame,text="clear",command=clear,height=2,width=10
             ,bg="#F59AF9",
               font=("Arial",10,"bold"))
clear.grid(row=3,column=1)

dot=Button(frame,text=".",command=lambda:button_press("."),height=2,width=10,
           bg="#F59AF9",
           font=("Arial", 10, "bold")
           )
dot.grid(row=3,column=2)

bracket1=Button(frame,text="(",command=lambda:button_press("("),height=2,width=10
                ,bg="#F59AF9",
               font=("Arial",10,"bold"))
bracket1.grid(row=4,column=0)
bracket2=Button(frame,text="[",command=lambda:button_press("),"),height=2,width=10,
bg = "#F59AF9",
font = ("Arial", 10, "bold")
)
bracket2.grid(row=4,column=1)
hmm=Button(frame,text="hmmm",command=lambda:button_press(""),height=2,width=10
           ,bg = "#F59AF9",
font = ("Arial", 10, "bold"))
hmm.grid(row=4,column=2)







window.mainloop()
