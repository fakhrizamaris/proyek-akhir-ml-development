The data is originally came from pjredddie:

wget http://pjreddie.com/media/files/cifar.tgz    

The downloaded dataset files are reorganized to match the expected directory structure to be easily feed to fastai library, so that there is a dedicated folder for each class under 'test' and 'train', e.g.:

* test/airplane/airplane-1001.png
* test/bird/bird-1043.png

* train/bird/bird-10018.png
* train/automobile/automobile-10000.png

The filename of the image doesn't have to include its class.
