# Sequential Learning for Dance generation

Generating dance using deep learning techniques.

### Use of GPU
If you use GPU in your experiment, set `--gpu` option in `run.sh` appropriately, e.g., 
```sh
$ ./run.sh --gpu 0
```
Default setup uses GPU 0 (`--gpu 0`). For CPU execution set gpu to -1

## Execution
The main routine is executed by:
```sh
$ ./run.sh --net $net --exp $exp --sequence $sequence --epoch $epochs --stage $stage
```
Being possible to train different type of datasets (`$exp`)

To run into a docker container use the file (`run_in_docker.sh`) instead of (`run.sh`)

## Unreal Engine 4 Visualization

For demostration from evaluation files or for testing training files use (`local/ue4_send_osc.py`).
For realtime emulation execute (`run_realtime.sh`). 


## Requirements

For training and evaluating the following libraries are required:
- [chainer=>3.1.0](https://github.com/chainer/chainer)
- [cupy=>2.1.0](https://github.com/cupy/cupy)
- [madmom](https://github.com/CPJKU/madmom/)
- [Beat Tracking Evaluation toolbox](https://github.com/adamstark/Beat-Tracking-Evaluation-Toolbox) or [updated](https://github.com/Fhrozen/Beat-Tracking-Evaluation-Toolbox)
- [mir_eval](https://github.com/craffel/mir_eval)
- [transforms3d](https://github.com/matthew-brett/transforms3d)
- h5py, numpy, soundfile, scipy, scikit-learn, pandas, colorama

For real-time emulation:
- pyOSC (for python v2)
- python-osc (for python v3)
- vlc (optional)

## ToDo:
- New Dataset
- Detailed Audio information

## References

[1]Nelson Yalta, Kazuhiro Nakadai, Tetsuya Ogata, "Sequential Deep Learning for Dancing Motion Generation", SIG-Challenge 2016
