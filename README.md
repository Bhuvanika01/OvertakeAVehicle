# CARLA OVERTAKING SYSTEM

This Python script allows you to replay recorded simulation sessions in [CARLA Simulator](https://carla.org/) using the built-in replay feature. It connects to a running CARLA server and replays a specified `.log` recording file.

## Requirements

* **CARLA version:** `0.9.11`
* **Python version:** Compatible with Python 3.6–3.8 (tested with CARLA 0.9.11)
* CARLA Python API installed or accessible from the `../carla/dist/` path

## Installation

Clone or download this repository and ensure CARLA is installed and running.

## Usage

```bash
python start_replayinggg.py --recorder_filename "C:\Users\Sarath\Downloads\CARLA_0.9.11\WindowsNoEditor\PythonAPI\examples\test1.log"
```

### Optional Arguments

| Argument              | Description                                  | Default                   |
| --------------------- | -------------------------------------------- | ------------------------- |
| `--host`              | IP of the CARLA server                       | `127.0.0.1`               |
| `--port`              | TCP port to connect to CARLA                 | `2000`                    |
| `--start`             | Start time of replay (in seconds)            | `0.0`                     |
| `--duration`          | Duration of replay (in seconds)              | `0.0` (plays entire file) |
| `--recorder_filename` | Path to the `.log` recording file            | `"test1.log"`             |
| `--camera`            | Follows the actor with this ID during replay | `0`                       |

> 💡 The `camera` argument allows you to attach the camera to a specific actor ID during the replay. Use `0` to disable.

## About `test1.log`

The `test1.log` file is a simulation recording created using CARLA's built-in recording functionality. It stores all simulation events, vehicle movements, and environment changes during the recorded session. This file must be accessible by the script when replaying.

## Output

The visual output of the replay is recorded and saved as a video file named **`over_taking.mp4`** in the current directory.

## Notes

* Make sure the CARLA simulator is running **before** executing this script.
* Adjust the path to `carla-*.egg` in the script if needed, especially if your CARLA installation is in a different location.

