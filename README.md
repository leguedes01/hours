# hours

import tkinter as tk
import time

def atualizar_relogio():
    hora_atual = time.strftime('%H:%M:%S')
    relogio.config(text=hora_atual)
    janela.after(1000, atualizar_relogio)

janela = tk.Tk()
janela.title('Relógio Digital')
relogio = tk.Label(janela, font=('Arial', 48))
relogio.pack()

atualizar_relogio()
janela.mainloop()
