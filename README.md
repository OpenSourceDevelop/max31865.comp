# max31865.comp

## A MAX31865 Module for LinuxCNC

This module provides an interface for the MAX31865 RTD-to-Digital Converter within a LinuxCNC environment. It enables accurate temperature readings using RTD sensors such as PT100 and PT1000. The implementation handles SPI communication, temperature conversion, and fault detection.

---

### Features
- **SPI Initialization**: Configures the SPI protocol for the MAX31865 (8-bit transfers, SPI mode 0).
- **Resistance-to-Temperature Conversion**: Implements the Callendar-Van Dusen equation for precise temperature calculations based on RTD characteristics.
- **Fault Detection**: Detects errors (e.g., open wire) and sets a fault bit for easy monitoring.
- **Flexible Configuration**: Adjustable parameters for reference resistance, nominal RTD resistance, and wire configuration (2-wire, 3-wire, or 4-wire).

---

### Installation
To compile and install the component:
```bash
halcompile --install max31865.comp
