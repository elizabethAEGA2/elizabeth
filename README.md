## SENSORES  KY-038 Small Sound Y KY-034 7 COLOR FLASH
Se combinaron dos sensores para que cuando el sensor small sound detectara sonido el sensor color flash prendiera en todos sus colores 
este es el codigo que se utilizo para esta practica.
## CODIGO

```python
import machine
import utim

# Configurar los pines
sound_pin = machine.Pin(26, machine.Pin.IN)
led_pin = machine.Pin(1, machine.Pin.OUT)

# Bucle principal
while True:
    # Leer el valor del sensor de sonido
    sound_value = sound_pin.value()

    # Encender el LED si se detecta un sonido
    if sound_value == 1:
        led_pin.on()
    else:
        led_pin.off()

    # Retardo para evitar lecturas rápidas y estables
    utime.sleep(0.1)
   ```
## PUEBRA
![images](https://github.com/elizabethAEGA2/elizabeth/blob/main/GITHUB/Captura%20de%20pantalla%202023-05-15%20181105.png)
