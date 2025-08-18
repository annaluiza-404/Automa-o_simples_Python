# Automatizar_simples_Python
Projeto simples de automação em Python que entra no Chrome, digita o link do YouTube, entra nele, digita o nome de algum canal e vídeo para depois clicar no vídeo e assistir. Como ilustração, o vídeo escolhido foi do canal Curso em Vídeo no curso de Python.


import pyautogui     #importação da biblioteca 'pyautogui' com todos os comandos
import time          #importação da biblioteca 'time' para utilizar 'sleep'; esperar próximos comandos para que todos possam ser executados no tempo de espera e execução correto

pyautogui.PAUSE=0.5       #pausa que pode ser usada em algum momento

pyautogui.press('win')          #comando 'press' para pressionar a tecla 'windows'
time.sleep(1)                   #espera o próximo comando em 1 segundo
pyautogui.write('chrome')       #comando 'write' para escrever algo ('chrome')
pyautogui.press('enter')        #comando 'press' para pressionar a tecla 'enter'
pyautogui.click(x=1366, y=1050)    #comando que ao posicionar o mouse em algum lugar da tela, ele pegará as coordenadas x e y do lugar para saber a posição

time.sleep(2)                                     #espera o próximo comando em 1 segundo
pyautogui.click(x=265, y=75)                      #coordenadas no local da tela para clicar
pyautogui.write('https://www.youtube.com/')       #comando 'write' para escrever algo - link que entra no YouTube
pyautogui.press('enter')                          #comando 'enter' para efetivamente entrar no site

time.sleep(2)                                     #espera de 2 segundos - para os comandos não se atropelarem
pyautogui.click(x=623, y=147)                     #coordenadas no local da tela para clicar
pyautogui.write('Curso em video python')          #escreve na barra de pesquisa do YouTube o que quer procurar
pyautogui.press('enter')                          #entra na pesquisa

time.sleep(2)                                     #espera carregar tudo
pyautogui.click(x=631, y=767)                     #clica e abre no vídeo do canal
