project deepspeech project deepspeech is an open source speech to text engine using a model trained by machine learning techniques based on baidus deep speech research paper project deepspeech uses googles tensorflow project to make the implementation easier pre built binaries that can be used for performing inference with a trained model can be installed with pip3 proper setup using virtual environment is recommended and you can find that documented below a pre trained english model is available for use and can be downloaded using the instructions below once everything is installed you can then use the deepspeech binary to do speech to text on short approximately 5 second audio files currently only wave files with 16 bit 16 khz mono are supported in the python client bash pip3 install deepspeech deepspeech model models output graph pbmm alphabet models alphabet txt lm models lm binary trie models trie audio my audio file wav alternatively quicker inference the realtime factor on a geforce gtx 1070 is about 0 44 can be performed using a supported nvidia gpu on linux see the release notes to find which gpus are supported this is done by instead installing the gpu specific package bash pip3 install deepspeech gpu deepspeech model models output graph pbmm alphabet models alphabet txt lm models lm binary trie models trie audio my audio file wav see the output of deepspeech h for more information on the use of deepspeech if you experience problems running deepspeech please check required runtime dependencies table of contents prerequisites getting the code getting the pre trained model using the model using the python package using the command line client using the node js package installing bindings from source third party bindings training installing prerequisites for training recommendations common voice training data training a model checkpointing exporting a model for inference distributed computing across more than one machine continuing training from a frozen graph code documentation contact getting help prerequisites python 3 6 git large file storage getting the code install git large file storage either manually or through a package like git lfs if available on your system then clone the deepspeech repository normally bash git clone https github com mozilla deepspeech getting the pre trained model if you want to use the pre trained english model for performing speech to text you can download it along with other important inference material from the deepspeech releases page alternatively you can run the following command to download and unzip the files in your current directory bash wget o https github com mozilla deepspeech releases download v0 1 1 deepspeech 0 1 1 models tar gz tar xvfz using the model there are three ways to use deepspeech inference the python package the command line client the node js package using the python package pre built binaries that can be used for performing inference with a trained model can be installed with pip3 you can then use the deepspeech binary to do speech to text on an audio file for the python bindings it is highly recommended that you perform the installation within a python 3 5 or later virtual environment you can find more information about those in this documentation we will continue under the assumption that you already have your system properly setup to create new virtual environments create a deepspeech virtual environment in creating a virtual environment you will create a directory containing a python3 binary and everything needed to run deepspeech you can use whatever directory you want for the purpose of the documentation we will rely on home tmp deepspeech venv you can create it using this command virtualenv p python3 home tmp deepspeech venv once this command completes successfully the environment will be ready to be activated activating the environment each time you need to work with deepspeech you have to activate load this virtual environment this is done with this simple command source home tmp deepspeech venv bin activate installing deepspeech python bindings once your environment has been setup and loaded you can use pip3 to manage packages locally on a fresh setup of the virtualenv you will have to install the deepspeech wheel you can check if it is already installed by taking a look at the output of pip3 list to perform the installation just issue pip3 install deepspeech if it is already installed you can also update it pip3 install upgrade deepspeech alternatively if you have a supported nvidia gpu on linux see the release notes to find which gpus are supported you can install the gpu specific package as follows pip3 install deepspeech gpu or update it as follows pip3 install upgrade deepspeech gpu in both cases it should take care of installing all the required dependencies once it is done you should be able to call the sample binary using deepspeech on your command line note the following command assumes you downloaded the pre trained model bash deepspeech model models output graph pbmm alphabet models alphabet txt lm models lm binary trie models trie audio my audio file wav the last two arguments are optional and represent a language model see client py for an example of how to use the package programatically using the command line client to download the pre built binaries use util taskcluster py bash python3 util taskcluster py target or if youre on macos bash python3 util taskcluster py arch osx target also if you need some binaries different than current master like v0 2 0 alpha 6 you can use branch bash python3 util taskcluster py branch v0 2 0 alpha 6 target this will download native client tar xz which includes the deepspeech binary and associated libraries and extract it into the current folder taskcluster py will download binaries for linux x86 64 by default but you can override that behavior with the arch parameter see the help info with python util taskcluster py h for more details proper deepspeech or tensorflows branch can be specified as well note the following command assumes you downloaded the pre trained model bash deepspeech model models output graph pbmm alphabet models alphabet txt lm models lm binary trie models trie audio audio input wav see the help output with deepspeech h and the native client readme for more details using the node js package you can download the node js bindings using npm bash npm install deepspeech alternatively if youre using linux and have a supported nvidia gpu see the release notes to find which gpus are supported you can install the gpu specific package as follows bash npm install deepspeech gpu see client js for an example of how to use the bindings installing bindings from source if pre built binaries arent available for your system youll need to install them from scratch follow these instructions third party bindings in addition to the bindings above third party developers have started to provide bindings to other languages asticode provides golang bindings in its go astideepspeech repo rustaudio provide a rust binding the installation and use of which is described in their deepspeech rs repo stes provides preliminary pkgbuilds to install the client and python bindings on arch linux in the arch deepspeech repo gst deepspeech provides a gstreamer plugin which can be used from any language with gstreamer bindings training installing prerequisites for training install the required dependencies using pip bash cd deepspeech pip3 install r requirements txt youll also need to download native client tar xz or build the native client files yourself to get the custom tensorflow op needed for decoding the outputs of the neural network you can use util taskcluster py to download the files for your architecture bash python3 util taskcluster py target this will download the native client files for the x86 64 architecture without cuda support and extract them into the current folder if you prefer building the binaries from source see the native client readme file we also have binaries with cuda enabled arch gpu and for arm7 arch arm recommendations if you have a capable nvidia at least 8gb of vram gpu it is highly recommended to install tensorflow with gpu support training will likely be significantly quicker than using the cpu to enable gpu support you can do bash pip3 uninstall tensorflow pip3 install tensorflow gpu 1 6 0 common voice training data the common voice corpus consists of voice samples that were donated through common voice we provide an importer that automates the whole process of downloading and preparing the corpus you just specify a target directory where all common voice contents should go if you already downloaded the common voice corpus archive from here you can simply run the import script on the directory where the corpus is located the importer will then skip downloading it and immediately proceed to unpackaging and importing to start the import process you can call bash bin import cv py path to target directory please be aware that this requires at least 70gb of free disk space and quite some time to conclude as this process creates a huge number of small files using an ssd drive is highly recommended if the import script gets interrupted it will try to continue from where it stopped the next time you run it unfortunately there are some cases where it will need to start over once the import is done the directory will contain a bunch of csv files the following files are official user validated sets for training validating and testing cv valid train csv cv valid dev csv cv valid test csv the following files are the non validated unofficial sets for training validating and testing cv other train csv cv other dev csv cv other test csv cv invalid csv contains all samples that users flagged as invalid a sub directory called cv corpus version contains the mp3 and wav files that were extracted from an archive named cv corpus version tar gz all entries in the csv files refer to their samples by absolute paths so moving this sub directory would require another import or tweaking the csv files accordingly to use common voice data during training validation and testing you pass comma separated combinations of their filenames into train files dev files test files parameters of deepspeech py if for example common voice was imported into data cv deepspeech py could be called like this bash deepspeech py train files data cv cv valid train csv dev files data cv cv valid dev csv test files data cv cv valid test csv if you are brave enough you can also include the other dataset which contains not yet validated content and thus can be broken from time to time bash deepspeech py train files data cv cv valid train csv data cv cv other train csv dev files data cv cv valid dev csv test files data cv cv valid test csv training a model the central python script is deepspeech py in the projects root directory for its list of command line options you can call bash deepspeech py help to get the output of this in a slightly better formatted way you can also look up the option definitions top of deepspeech py for executing pre configured training scenarios there is a collection of convenience scripts in the bin folder most of them are named after the corpora they are configured for keep in mind that the other speech corpora are very large on the order of tens of gigabytes and some arent free downloading and preprocessing them can take a very long time and training on them without a fast gpu gtx 10 series recommended takes even longer if you experience gpu oom errors while training try reducing the batch size with the train batch size dev batch size and test batch size parameters as a simple first example you can open a terminal change to the directory of the deepspeech checkout and run bash bin run ldc93s1 sh this script will train on a small sample dataset called ldc93s1 which can be overfitted on a gpu in a few minutes for demonstration purposes from here you can alter any variables with regards to what dataset is used how many training iterations are run and the default values of the network parameters feel also free to pass additional or overriding deepspeech py parameters to these scripts then just run the script to train the modified network each dataset has a corresponding importer script in bin that can be used to download if its freely available and preprocess the dataset see bin import librivox py for an example of how to import and preprocess a large dataset for training with deep speech if youve run the old importers in util importers they could have removed source files that are needed for the new importers to run in that case simply remove the extracted folders and let the importer extract and process the dataset from scratch and things should work checkpointing during training of a model so called checkpoints will get stored on disk this takes place at a configurable time interval the purpose of checkpoints is to allow interruption also in the case of some unexpected failure and later continuation of training without losing hours of training time resuming from checkpoints happens automatically by just re starting training with the same checkpoint dir of the former run be aware however that checkpoints are only valid for the same model geometry they had been generated from in other words if there are error messages of certain tensors having incompatible dimensions this is most likely due to an incompatible model change one usual way out would be to wipe all checkpoint files in the checkpoint directory or changing it before starting the training exporting a model for inference if the export dir parameter is provided a model will have been exported to this directory during training refer to the corresponding readme md for information on building and running a client that can use the exported model making a mmap able model for inference the output graph pb model file generated in the above step will be loaded in memory to be dealt with when running inference this will result in extra loading time and memory consumption one way to avoid this is to directly read data from the disk tensorflow has tooling to achieve this it requires building the target tensorflow contrib util convert graphdef memmapped format binaries are produced by our taskcluster for some systems including linux amd64 and macos amd64 use util taskcluster py tool to download specifying tensorflow as a source producing a mmap able model is as simple as convert graphdef memmapped format in graph output graph pb out graph output graph pbmm upon sucessfull run it should report about conversion of a non zero number of nodes if it reports converting 0 nodes something is wrong make sure your model is a frozen one and that you have not applied any incompatible changes this includes quantize weights distributed training across more than one machine deepspeech has built in support for distributed tensorflow to get an idea on how this works you can use the script bin run cluster sh for running a cluster with workers just on the local machine bash bin run cluster sh help usage run cluster sh help script script p w g help print this help message script run the provided script instead of deepspeech py p number of local parameter servers w number of local workers g number of local gpus per worker remaining parameters will be forwarded to deepspeech py or a provided script example usage the following example will create a local deepspeech py cluster with 1 parameter server and 2 workers with 1 gpu each run cluster sh 1 2 1 epoch 10 be aware that for the help example to be able to run you need at least two cuda capable gpus 2 workers times 1 gpu the script utilizes environment variable cuda visible devices for deepspeech py to see only the provided number of gpus per worker the script is meant to be a template for your own distributed computing instrumentation just modify the startup code for the different servers workers and parameter servers accordingly you could use ssh or something similar for running them on your remote hosts continuing training from a frozen graph if youd like to use one of the pre trained models released by mozilla to bootstrap your training process transfer learning fine tuning you can do so by using the initialize from frozen model flag in deepspeech py for best results make sure youre passing an empty checkpoint dir when resuming from a frozen model for example if you want to fine tune the entire graph using your own data in my train csv my dev csv and my test csv for three epochs you can something like the following tuning the hyperparameters as needed bash mkdir fine tuning checkpoints python3 deepspeech py n hidden 2048 initialize from frozen model path to model output graph pb checkpoint dir fine tuning checkpoints epoch 3 train files my train csv dev files my dev csv test files my dev csv learning rate 0 0001 note the released models were trained with n hidden 2048 so you need to use that same value when initializing from the release models code documentation documentation incomplete for the code can be found here http deepspeech readthedocs io en latest contact getting help there are several ways to contact us or to get help faq we have a list of common questions and their answers in our faq when just getting started its best to first check the faq to see if your question is addressed discourse forums if your question is not addressed in the faq the discourse forums is the next place to look they contain conversations on general topics using deep speech and deep speech development irc if your question is not addressed by either the faq or discourse forums you can contact us on the machinelearning channel on mozilla irc people there can try to answer help issues finally if all else fails you can open an issue in our repo