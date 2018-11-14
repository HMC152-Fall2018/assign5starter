# CS 152
# Assignment 6
# November 14, 2018
##  Due Tuesday, November 4, 2018, 11 PM


 
The goal in this assignment is to create a replacement for [nn.GRU](https://pytorch.org/docs/0.3.1/nn.html?highlight=gru#torch.nn.GRU). The parameters for the GRU constructor are:

* ```input_size``` – The number of expected features in the input x
* ```hidden_size``` – The number of features in the hidden state h
* ```num_layers``` – Number of recurrent layers.
* ```bias``` – If False, then the layer does not use bias weights b_ih and b_hh. Default: True
* ```batch_first``` – If True, then the input and output tensors are provided as (batch, seq, feature)
* ```dropout``` – If non-zero, introduces a dropout layer on the outputs of each RNN layer except the last layer
* ```bidirectional``` – If True, becomes a bidirectional RNN. Default: False

You only need to implement ```input_size``` and ```hidden_size``` (other parameters should be accepted, but may be silently ignored).  For extra credit, implement ```num_layers```, ```dropout```, and/or ```bidirectional```.

FYI, my implementation was about 50 lines of code.


As a testbed, use the [dickens.ipynb notebook](https://github.com/nrhodes/cs152/blob/master/notebooks/dickens.ipynb) from the cs152 repository, replacing ```nn.GRU``` with your ```MyGRU```.

### Groups
You may work by yourself or in groups of 2. All work in a group should be done with the group members physically working together.

Outside resources: You may use any pytorch and fastai documentation and general web resources on using the two libraries. You should not look at the source code of PyTorch's GRU. 

### What to turn in
A notebook named Assignment5.ipynb which is a copy of dickens.ipynb modified to use your new MyGRU class. Please make sure your notebook includes the output of the training loop so I can see the losses.  You can adjust the 2nd parameter of learn.fit from 7 to 5 to reduce the number of epochs that are trained.  You may need to adjust the batch size if you run 

### Suggestions

* The documentation for nn.GRU is extremely helpful. Pay careful attention to shapes of incoming and outgoing values.

* The debugger is your friend.  To use it, import:

```from IPython.core.debugger import set_trace```

And then call ```set_trace()``` wherever you’d like a breakpoint.

* Be extremely clear about the shapes of everything.


* Useful PyTorch calls:
    * ```nn.init.normal```
    * ```nn.init.constant```
    * ```torch.mm```
    * ```torch.sigmoid```
    * ```torch.tanh```
    * ```torch.stack```
    * ```torch.unsqueeze```

* You may find it useful to install PyTorch and a CPU-version of PyTorch on your local machine.
[Here](https://forums.fast.ai/t/fastai-v0-7-install-issues-thread/24652) is a thread on installation.
To summarize



