  ### Hallo, my name is Ana and I am criating projects to train the Python linguage 😊 </br>
<span style="font-family:Verdana"> <b>Calculator in Python </b></span> </br>
<br> ⚠️⚠️ <b>Attention, in developement </b>⚠️⚠️ <br/>
<span style="font-family:Verdana"> <b> How this app is possible to do the main mathematical operations </b></span> </br>

<span style="font-family:Verdana"> <b> In this project you will find layout managers.
EX: grid, it adds through row and column positions, like a table or grid. 
And also the place it adds widgets in specific positions, with specific sizes.  </b></span> </br>

<span style="font-family:Verdana"> <b> And to start creating calculator I imported the tkinter library.📚  </b></span> </br>

<span style="font-family:Verdana"> <b> I hope you like the project and leave your opinion.There's always somenthing to improve 📖 </b></span> </br>


 <span style="font-family:Verdana"> <b>FOLLOW THE PROJECT CODE BELOW </b></span> </br>
 

![Gato Programador](https://media.giphy.com/media/VbnUQpnihPSIgIXuZv/giphy-downsized.gif)


 <span style="font-family:Verdana"> <b>from tkinter import * </br>
from tkinter import ttk </br>
#cores  </br>
cor1 = "#3b3b3b" </br>  #preta #variavel  
cor2 = "#feffff"  </br>
cor3 = "#38576b"  </br>
cor4 = "#ECEFF1"  </br>
cor5 = "#FFAB40"  </br>

janela = Tk()  </br>
janela.title("Calculadora")  </br>
janela.geometry("235x310")   </br>
janela.config(bg=cor1)  </br>


#criando frames </br>

frame_tela = Frame(janela, width=235, height=50,bg= cor3) </br>
frame_tela.grid(row=0, column =0) </br>

frame_corpo = Frame(janela, width=235, height=268) </br>
frame_corpo.grid(row=1, column =0) </br>

#variavel todos os valores </br>
todos_valores ='' </br>


#criando função </br>
def entrada_valores(event): </br>

  global todos_valores </br>

  todos_valores = todos_valores + str(event) </br>


#passando valor para a tela </br>

  valor_texto.set(todos_valores) </br>

#função para calcular </br>
def calcular(): </br>
    global todos_valores  </br>
    resultado = eval(todos_valores)  </br>
    valor_texto.set(str(resultado))  </br>

#funçãolimpar tela  </br>

def limpar_tela():  </br>
    global todos_valores  </br>
    todos_valores = ""  </br>
    valor_texto.set("")  </br>


#criando label  </br>
valor_texto = StringVar()  </br>
app_label = Label(frame_tela,textvariable= valor_texto,width=16,height=2, padx=7,relief=FLAT,anchor="e",justify=RIGHT,font=('Ivy 18'),bg=cor3,fg=cor2) </br>
app_label.place(x=0,y=0)  </br>



#criando botões  </br>
b_1 = Button(frame_corpo,command=limpar_tela,text="C",width=11,height=2, bg=cor4,font=('Ivy 13 bold'), relief=RAISED, overrelief=RIDGE) </br>
b_1.place(x=0,y=0)  </br>

b_2 = Button(frame_corpo,command= lambda: entrada_valores('%'),text="%",width=5,height=2, bg=cor4,font=('Ivy 13 bold'), relief=RAISED, overrelief=RIDGE)</br>
b_2.place(x=118,y=0) </br>

b_3 = Button(frame_corpo,command= lambda: entrada_valores('/'),text="/",width=5,height=2, bg=cor5,fg=cor2,font=('Ivy 13 bold'), relief=RAISED, overrelief=RIDGE) </br>
b_3.place(x=177,y=0) </br>


b_4 = Button(frame_corpo,command= lambda: entrada_valores('7'),text="7",width=5,height=2, bg=cor4,font=('Ivy 13 bold'), relief=RAISED, overrelief=RIDGE)</br>
b_4.place(x=0,y=52) </br>

b_5 = Button(frame_corpo,command= lambda: entrada_valores('8'),text="8",width=5,height=2, bg=cor4,font=('Ivy 13 bold'), relief=RAISED, overrelief=RIDGE)</br>
b_5.place(x=59,y=52)</br>

b_6 = Button(frame_corpo,command= lambda: entrada_valores('9'),text="9",width=5,height=2, bg=cor4,font=('Ivy 13 bold'), relief=RAISED, overrelief=RIDGE)</br>
b_6.place(x=118,y=52)  </br> #X=HORIZONTALY=VERTICAL

b_7 = Button(frame_corpo,command= lambda: entrada_valores('*'),text="*",width=5,height=2, bg=cor5,fg=cor2,font=('Ivy 13 bold'), relief=RAISED, overrelief=RIDGE)</br>
b_7.place(x=177,y=52)</br>

b_8 = Button(frame_corpo,command= lambda: entrada_valores('4'),text="4",width=5,height=2, bg=cor4,font=('Ivy 13 bold'), relief=RAISED, overrelief=RIDGE)</br>
b_8.place(x=0,y=104)</br>

b_9 = Button(frame_corpo,command= lambda: entrada_valores('5'),text="5",width=5,height=2, bg=cor4,font=('Ivy 13 bold'), relief=RAISED, overrelief=RIDGE)</br>
b_9.place(x=59,y=104)</br>

b_10 = Button(frame_corpo,command= lambda: entrada_valores('6'),text="6",width=5,height=2, bg=cor4,font=('Ivy 13 bold'), relief=RAISED, overrelief=RIDGE)</br>
b_10.place(x=118,y=104)</br>

b_11 = Button(frame_corpo,command= lambda: entrada_valores('-'),text="-",width=5,height=2, bg=cor5,fg=cor2,font=('Ivy 13 bold'), relief=RAISED, overrelief=RIDGE)</br>
b_11.place(x=177,y=104)</br>

b_12 = Button(frame_corpo,command= lambda: entrada_valores('1'),text="1",width=5,height=2, bg=cor4,font=('Ivy 13 bold'), relief=RAISED, overrelief=RIDGE)</br>
b_12.place(x=0,y=156)</br>

b_13 = Button(frame_corpo,command= lambda: entrada_valores('2'),text="2",width=5,height=2, bg=cor4,font=('Ivy 13 bold'), relief=RAISED, overrelief=RIDGE)</br>
b_13.place(x=59,y=156)</br>

b_14 = Button(frame_corpo,command= lambda: entrada_valores('3'),text="3",width=5,height=2, bg=cor4,font=('Ivy 13 bold'), relief=RAISED, overrelief=RIDGE)</br>
b_14.place(x=118,y=156)</br>

b_15 = Button(frame_corpo,command= lambda: entrada_valores('+'),text="+",width=5,height=2, bg=cor5,fg=cor2,font=('Ivy 13 bold'), relief=RAISED, overrelief=RIDGE)</br>
b_15.place(x=177,y=156)</br>

b_16 = Button(frame_corpo,command= lambda: entrada_valores('0'),text="0",width=11,height=2, bg=cor4,font=('Ivy 13 bold'), relief=RAISED, overrelief=RIDGE)</br>
b_16.place(x=0,y=208)</br>

b_17 = Button(frame_corpo,command= lambda: entrada_valores('.'),text=".",width=5,height=2, bg=cor4,font=('Ivy 13 bold'), relief=RAISED, overrelief=RIDGE)</br>
b_17.place(x=118,y=208)</br>

b_18 = Button(frame_corpo,command= calcular,text="=",width=5,height=2, bg=cor5,fg=cor2,font=('Ivy 13 bold'), relief=RAISED, overrelief=RIDGE)</br>  
b_18.place(x=177,y=208)</br>


janela.mainloop()  </b></span> </br>



