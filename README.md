Technical Specifications

                        Microcontrollers: PIC18F series (utilizing internal/external CAN controllers).
                        Communication Protocol: CAN 2.0B (ISO 11898).
                        Transceivers: MCP2551 or equivalent.
                        Peripherals: 16x2 LCD Display, Tactile Switches (Mode, CF, Up, Down, ACK), EEPROM for persistent storage.
                        Software Stack: C Programming (Embedded C), MPLAB X IDE, XC8 Compiler.

Core Implementation

                        DetailsMessage Filtering & Masking: Implemented local hardware filtering to ensure each node only processes relevant Data Frames, reducing CPU overhead.
                        Multi-Mode User Interface: Developed a state-machine-based UI to toggle between Operation Mode (real-time monitoring) and Config Mode (system calibration).
                        Persistent Storage: Integrated EEPROM routines to save Node IDs and sensor thresholds, ensuring data retention across power cycles.
                        Event-Driven Alerts: Configured the system to automatically transmit emergency messages to the "server" node when sensor values exceed user-defined thresholds.
  
  
Key Features Explained

      Bus Arbitration:      Leveraged CAN's non-destructive bitwise arbitration to ensure high-priority messages (like Over-temperature) gain bus access first.
      Node Identity  :      Dynamic Node ID configuration via the LCD menu, allowing for modularity in a multi-node network.
      Reliability:     Utilized CAN’s built-in Error Frames and CRC checks to ensure data integrity in a simulated "noisy" automotive environment.
