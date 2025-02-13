# Beacon: A Naturalistic Driving Dataset During Blackouts for Benchmarking Traffic Reconstruction and Control

This repository contains files and scripts for the **Beacon Dataset**, a naturalistic driving dataset collected during blackout conditions at two unsignalized intersections in Memphis, TN. The dataset supports research in **traffic reconstruction, unsignalized intersection control, and mixed traffic management** involving robot vehicles (RVs) and human-driven vehicles (HVs).

## Dataset Description

### Intersections

![satellite_view](https://github.com/user-attachments/assets/5ac3c5a7-58bf-4adf-a412-9f03f7d1872e)

- **[Walnut Grove-Goodlett](https://maps.app.goo.gl/Evvxe3cxLwy3p9fd6)**
  - Noon (12:00 PM - 1:00 PM)
  - Afternoon (5:00 PM - 6:00 PM)
- **[Walnut Grove-Mendenhall](https://maps.app.goo.gl/WJp31i2NYdrc1WCT8)**
  - Noon (12:00 PM - 1:00 PM)
  - Afternoon (5:00 PM - 6:00 PM)


## Configuration Files

These are **SUMO configuration files** used to simulate traffic flow at the respective intersections.

- `GWG_AN.sumocfg`: Walnut Grove-Goodlett Afternoon
- `GWG_N.sumocfg`: Walnut Grove-Goodlett Noon
- `WGM_AN.sumocfg`: Walnut Grove-Mendenhall Afternoon
- `WGM_N.sumocfg`: Walnut Grove-Mendenhall Noon

## Requirements

- SUMO (Simulation of Urban MObility)
- Python 3.x
- Required Python packages:
  ```
  pandas
  numpy
  traci
  ```

## Scripts

### traci_script.py
Main script for running traffic simulations using SUMO's TraCI interface. Handles:
- Vehicle addition and routing
- Simulation step management
- Output generation

### data_process.py
Processes raw data files:
- Data cleaning and formatting
- Vehicle ID generation
- Route creation

### parse_output.py
Parses simulation outputs:
- XML parsing
- Metrics calculation
- Results formatting

## Usage

1. Install dependencies:
   ```bash
   pip install pandas numpy
   ```

2. Set up [SUMO](https://sumo.dlr.de/docs/Installing/index.html) environment

3. Run simulation:
   ```bash
   python traci_script.py
   ```
   - Modify `base_path` and `dataset_name` inside the script to point to your desired dataset.

### Mixed Traffic Simulation
For mixed traffic simulation, detailed instructions can be found at: [Fluidic-City-Lab/MixedTrafficControl](https://github.com/Fluidic-City-Lab/MixedTrafficControl)


## Citation

```bibtex
@article{sarker2024beacon,
  title={Beacon: A Naturalistic Driving Dataset During Blackouts for Benchmarking Traffic Reconstruction and Control},
  author={Sarker, Supriya and Islam, Iftekharul and Poudel, Bibek and Li, Weizi},
  journal={arXiv preprint arXiv:2412.14208},
  year={2024}
}
```
