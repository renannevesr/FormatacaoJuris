from selenium import webdriver
from webdriver_manager.chrome import *
import time
from tkinter import *


def pesquisar():
    texto = f'''
    
    URL: {url}
    
    '''
    print(texto)
    browser = webdriver.Chrome(ChromeDriverManager().install())
    browser.get(url)
    time.sleep(2)
    Acessar = browser.find_element_by_xpath(
        '//*[@id="app-root"]/div/div[1]/div/div/div[1]/div[1]/div/div[3]/div/div/div/div[1]/button')
    time.sleep(2)
    Acessar.click()
    time.sleep(2)
    Juris = browser.find_element_by_xpath(
        '//*[@id="app-root"]/div/div[2]/div/span/div/div[2]/div/div[1]/div/div/div/div/p[1]')
    txtJuris = Juris.text
    txt_Tk_Juris["text"] = txtJuris

    Ref = browser.find_element_by_xpath(
        '//*[@id="app-root"]/div/div[2]/div/span/div/div[2]/div/div[1]/div/div/div/div/p[3]')
    txtRef = Ref.text
    txt_Tk_Ref["text"] = txtRef
    time.sleep(2)


janela = Tk()
janela.title("Formatador de Jurisprudencia")

texto_orientacao = Label(janela, text="Insira o link da jurisprudencia")
texto_orientacao.grid(column=0, row=0)
url = Entry(janela)
url.grid(column=0, row=1)
url.place()


botao = Button(janela, text="pesquisar", command=pesquisar)
botao.grid(column=0, row=2)
txt_Tk_Juris = Label(janela, text="")
txt_Tk_Juris.grid(column=0, row=3)

txt_Tk_Ref = Label(janela, text="")
txt_Tk_Ref.grid(column=0, row=4)


janela.mainloop()
