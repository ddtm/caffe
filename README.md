# Gradient Reversal Branch

This is an extension to Caffe which allows one to reproduce some of the results presented in the paper [Unsupervised Domain Adaptation by Backpropagation](http://jmlr.org/proceedings/papers/v37/ganin15.pdf) (accepted to ICML 2015).

## How to use

Download and unpack the [Office dataset](http://www.cs.uml.edu/~saenko/data/domain_adaptation_images.tar.gz). Let `<office_dir>` be the path where you uncompressed the files. 

Change the current directory to the root folder of the Caffe repository. Use the following command to fetch additional files, prepare lmdb datasets for Caffe and setup directories for the experiments:
```
./examples/adaptation/scripts/prepare_experiments.sh <office_dir>
```

Now everything is ready for reproducing the results. For example, to train an adapted model for the **Amazon to Webcam** setting invoke:
```
./examples/adaptation/experiments/amazon_to_webcam/scripts/train.sh
```
Change `amazon_to_webcam` either to `dslr_to_webcam` or to `webcam_to_dslr` in order to obtain models for other settings.

## Citation

Please cite the following technical report if you are using this extension in your research:

    @inproceedings{ganin2015unsupervised,
        author    = {Yaroslav Ganin and Victor S. Lempitsky},
        title     = {Unsupervised Domain Adaptation by Backpropagation},
        booktitle = {ICML},
        year      = {2015}
    }
