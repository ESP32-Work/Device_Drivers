# LED Toggling Project

This project demonstrates how to toggle an LED using FreeRTOS on an ESP32 microcontroller. The LED is toggled on and off at regular intervals using GPIO registers.

## File Structure

- `led-toggleing.c`: Contains the main code for initializing and toggling the LED.

## Dependencies

- FreeRTOS: The project uses FreeRTOS for task management.
- ESP32 SDK: The project is designed to run on an ESP32 microcontroller.

## Code Overview

### Macros

- `LED_GPIO`: Defines the GPIO pin number for the inbuilt LED.
- `GPIO_OUT_W1TS_REG`: GPIO register address for setting the output high.
- `GPIO_OUT_W1TC_REG`: GPIO register address for setting the output low.
- `GPIO_ENABLE_W1TS_REG`: GPIO register address for enabling the output.

### Global Variables

- `gpio_enable_reg`: Pointer to the GPIO enable register.
- `gpio_out_w1ts_reg`: Pointer to the GPIO output set register.
- `gpio_out_w1tc_reg`: Pointer to the GPIO output clear register.

### Functions

#### `void intialize_led(void)`

Initializes the LED by enabling the GPIO pin for output.

#### `void toggle_led(void)`

Toggles the LED by setting the GPIO pin low and then high with a delay in between.

#### `void led_task(void *pvParameter)`

FreeRTOS task that continuously toggles the LED.

#### `void app_main(void)`

Main function that initializes the LED and creates the FreeRTOS task for toggling the LED.

## How to Build and Run

1. Set up the ESP32 development environment.
2. Clone the repository to your local machine.
3. Navigate to the project directory.
4. Build the project using the ESP32 build tools.
5. Flash the firmware to the ESP32 board.
6. Monitor the serial output to see the LED toggling.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request with your changes.

## Contact

For any questions or issues, please open an issue on the GitHub repository.