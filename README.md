# real_robot_lab

## Get Ready

You need to install `Isaac Lab`.

## Installation

Using a python interpreter that has Isaac Lab installed, install the library

```bash
python -m pip install -e ./exts/real_robot_lab
```

## Try unitree-a1 example

```bash
# To train
python scripts/rsl_rl/train.py --task RealRobot-Isaac-Velocity-Rough-Unitree-A1-v0 --headless
# To play
python scripts/rsl_rl/play.py --task RealRobot-Isaac-Velocity-Rough-Unitree-A1-Play-v0
```

## Add your own robot

To convert urdf, you need to run `convert_urdf.py` of dir `IsaacLab`

For example, to generate A1 usd file:

```bash
./isaaclab.sh -p source/standalone/tools/convert_urdf.py <YOUR_ROBOT>.urdf source/extensions/omni.isaac.lab_assets/data/Robots/<YOUR_ROBOT>/<YOUR_ROBOT>.usd --merge-join
```

Check [import_new_asset](https://docs.robotsfan.com/isaaclab/source/how-to/import_new_asset.html) for detail
