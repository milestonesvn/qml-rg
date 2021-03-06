Quantum Machine Learning Reading Group @ ICFO
=============================================

The reading group serves a dual purpose.
On one hand, we would like to develop an understanding of statistical learning theory and how quantum resources can make a difference.
On the other hand, we would like to develop skills that are marketable outside academia.
To achieve this dual purpose, we structure the meetings along three topics:

1. A recent, but already important paper on classical machine learning.

2. A quantum machine learning paper.

3. Coding exercises that implement a learning algorithm or a simulation of a quantum protocol.

Papers will be announced a week in advance.
Each week there will be a person responsible for a paper, but everybody is expected to read the two papers in advance and prepare with questions.
Coding will be done collaboratively through this repository.
The reading group requires commitment: apart from the 1.5-2 contact hours a week, at least another 2-3 hours must be dedicated to reading and coding.
You are not expected to know machine learning or programming before joining the group, but you are expected to commit the time necessary to catch up and develop the relevant skills.

The language of choice is Python 3.
MATLAB users will be shot on sight.
Julia is an upcoming language in which the bleeding-edge of machine learning and quantum simulation are easier to implement, and therefore it is an accepted alternative.

Resources
---------
The broader QML community is still taking shape.
We are attempting to organize it through the website [quantummachinelearning.org](http://quantummachinelearning.org/). You can also sign up for the mailing list there.
Please also consider contributing to the recently rewritten [Wikipedia article on QML](https://en.wikipedia.org/wiki/Quantum_machine_learning).
Apart from new content, stylistic and grammatical edits, figures, and translations are all welcome.

The best way to learn machine learning is by doing it.
The book [Python Machine Learning](https://www.packtpub.com/big-data-and-business-intelligence/python-machine-learning) is a good starter, along with its [GitHub repository](https://github.com/rasbt/python-machine-learning-book).
[Kaggle](http://kaggle.com/) is a welcoming community of data scientists.
It is not only about competitions: several hundred datasets are hosted on Kaggle, along with notebooks and scripts (collectively known as kernels) that do interesting stuff with the data.
These provide perfect stepping stones for beginners.
Find a dataset that is close to your personal interests and dive in.
For a sufficiently engaging theoretical introduction to machine learning, the book [The Elements of Statistical Learning: Data Mining, Inference, and Prediction](https://statweb.stanford.edu/~tibs/ElemStatLearn/) is highly recommended.

[Anaconda](https://www.continuum.io/downloads) is the recommended Python distribution if you are new to the language.
It ships with most of the scientific and machine learning ecosystem around Python.
It includes [Scikit-learn](http://scikit-learn.org/), which is excellent for prototyping machine learning models.
For scalable deep learning, [Keras](https://keras.io/) is recommended: it can transparently change between TensorFlow and Theano as back-ends.
[QuTiP](http://qutip.org/) is an excellent quantum simulation library, and with the latest version (4.0.2), it is [reasonably straightforward](http://qutip.org/docs/4.0.2/installation.html#platform-independent-installation) to install it in Anaconda with [conda-forge](https://conda-forge.github.io/).
QuTiP is somewhat limited in scalability, so perhaps it is worth checking out other simulators, such as [ProjectQ](http://projectq.ch/).

As for [Julia](http://julialang.org/), the [JuliaML](https://github.com/JuliaML) project collects most of the machine learning efforts.
It includes cool stuff like [Transformations](https://github.com/JuliaML/Transformations.jl), which allows you to define arbitrary computational graphs, not just the run-of-the-mill static ones implemented in TensorFlow and Theano.
[Quantum simulators](https://juliaquantum.github.io/) lag behind a bit, but there are interesting initiatives for doing [tensor network calculations](https://github.com/Jutho/TensorOperations.jl).

We will follow the good practices of [software carpentry](http://software-carpentry.org/), that is, elementary IT skills that every scientist should have.
In particular, we use [git](https://rogerdudler.github.io/git-guide/) as a version control system and host the repository right here on GitHub.
When editing text or [Markdown](https://guides.github.com/features/mastering-markdown/) documents like this one, please write every sentence in a new line to ensure that conflicts are efficiently resolved when several people edit the same file.

Meeting 1
---------
10.00-11.30, 16 February 2017, Seminar Room (201).

Papers:

- Kingma, D. & Ba, J. [Adam: A Method for Stochastic Optimization](https://arxiv.org/abs/1412.6980). *Proceedings of ICLR-15, 3rd International Conference for Learning Representations*, 2014.
This paper introduces a derivative of stochastic gradient descent that is now widely used in training deep learning networks.
For instance, it is one of the [available optimizers](https://keras.io/optimizers/) in Keras.

- Wan, K. H.; Dahlsten, O.; Kristjánsson, H.; Gardner, R. & Kim, M. S. [Quantum generalisation of feedforward neural networks](https://arxiv.org/abs/1612.01045). *arXiv:1612.01045*, 2016.
Papers on quantum neural networks are typically written by crackpots, and this work is one of the refreshing exceptions.
It gives a twist on gradient descent to train neural networks of the quantum generalization of classical tasks. One of the examples is an autoencoder: a [related and equally interesting paper](https://arxiv.org/abs/1612.02806) came out a few days later, which is also worth reading.
This latter paper explicitly mentions that all simulations were implemented in Python with QuTiP.

Coding exercise:

- The first week does not have a coding exercise.
Instead, please ensure that your computational environment is up and running.
Python with the recommended libraries should be there, along with an editor.
Either use your favourite text editor, or opt for Spyder, which is also bundled in Anaconda.
Ensure that you can open and run Jupyter notebooks.
Go through a git tutorial, like the one linked under Resources, fork this repository, clone it, and add the upstream repo to follow.
If you need help, we will be around in 372 from 5pm on Wednesday, 15 Feb.

Tutorial 1
----------
16.00-17.30, 21 February 2017, Yellow Lecture Room (247).

This tutorial is about the importance of using a version control system. The focus is on git, starting with using it locally, for collaborating on LaTeX documents on Overleaf, and finishing with some examples using GitHub. The [notes](Tutorials/Git.md) are in the Tutorials folder.


Meeting 2
---------
10.00-11.30, 23 February 2017, Seminar Room (201).

Papers:

- Abadi, M.; Barham, P.; Chen, J.; Chen, Z.; Davis, A.; Dean, J.; Devin, M.; Ghemawat, S.; Irving, G.; Isard, M.; Kudlur, M.; Levenberg, J.; Monga, R.; Moore, S.; Murray, D. G.; Steiner, B.; Tucker, P.; Vasudevan, V.; Warden, P.; Wicke, M.; Yu, Y. & Zheng, X.
[TensorFlow: A System for Large-scale Machine Learning](https://arxiv.org/abs/1603.04467).
*Proceedings of the 12th USENIX Conference on Operating Systems Design and Implementation*, 2016, 265-283.
This is the only systems paper we will discuss.
Given the hype around it, its actual importance, and its relevance for getting a job in real life, it is worth looking at it.
An earlier open source effort, [Theano](http://deeplearning.net/software/theano/) implements the same idea of using a data flow graph as a computational abstraction; see the [matching paper](https://arxiv.org/abs/1605.02688).

- Lau, H.-K.; Pooser, R.; Siopsis, G. & Weedbrook, C.
[Quantum machine learning over infinite dimensions](https://arxiv.org/abs/1603.06222). *arXiv:1603.06222*, 2016.
This paper is the only proposal so far for using continuous variable systems for doing machine learning.
These systems are attractive for both their theoretical and experimental properties, and the paper also allows us to talk about building blocks of machine learning algorithms.

Coding exercises:

- Implement an autoenconder in TensorFlow, say, random ten dimensional vectors encoded on a six dimensional hidden layer.
Use Adam as the optimization routine.
Keras is a recommended abstraction layer around TensorFlow.

- Simulate a swap test.
The [circuit](https://en.wikipedia.org/wiki/Quantum_digital_signature#Public_Key_should_be_the_same_for_every_recipient_.28Swap_Test.29) is nothing but a Fredkin gate and a Hadamard gate, followed by a local measurement on the ancilla.
This task is trivial to do in QuTiP, but you can also try your hands on ProjectQ, or the [IBM Quantum Experience](https://www.research.ibm.com/quantum/).

Tutorial 2
----------
16.00-17.30, 07 March 2017, Yellow Lecture Room (247).

This is a Python introduction without talking about introductory stuff on Python. The goal was to give a general idea of what goes into designing a programming language and what kind of trade-offs have to be made, followed by some idiomatic expressions in Python and some caveats. The [corresponding notebook](Tutorials/Python_Introduction.ipynb) is in the Tutorials folder.

Meeting 3
---------
10.00-11.30, 09 March 2017, Seminar Room (201).

Papers:

- Silver, D.; Huang, A.; Maddison, C. J.; Guez, A.; Sifre, L.; van den Driessche, G.; Schrittwieser, J.; Antonoglou, I.; Panneershelvam, V.; Lanctot, M.; Dieleman, S.; Grewe, D.; Nham, J.; Kalchbrenner, N.; Sutskever, I.; Lillicrap, T.; Leach, M.; Kavukcuoglu, K.; Graepel, T. & Hassabis, D. [Mastering the game of *Go* with deep neural networks and tree search](http://doi.org/10.1038/nature16961). *Nature*, 2016, 529, 484-489. It is the state-of-the-art in reinforcement learning. The scheme combines deep learning with a heuristic search, which is a pattern that is seen over and over again since this paper came out. The simpler, but equally glamorous task of playing Atari games was published by the same group; [that paper](https://arxiv.org/abs/1312.5602) is also worth a look.

- Dunjko, V.; Taylor, J. M. & Briegel, H. J. [Quantum-Enhanced Machine Learning](https://arxiv.org/abs/1610.08251). *Physical Review Letters*, 2016, 117, 130501. This paper takes a comprehensive look at what quantum agents can learn in a reinforcement learning scenario. It is worth looking at an [earlier and much longer version](https://arXiv.org/abs/1507.08482) of this paper.

Coding exercises:

- Teach an agent to learn a reinforcement learning task. [OpenAI Gym](http://gym.openai.com) is a collection of environments in which you can benchmark reinforcement learning algorithms. It was officially announced at NIPS in December 2016. [This](https://github.com/claymcleod/dqn) works fine with Pacman, it uses Keras and Theano for implementing the agent, and it is barely a hundred lines of code.

- Optional: The classical first-person shooter Doom is [one of the possible environments](https://gym.openai.com/envs#doom). Installing the Doom environment is fairly intricate as it is not included by default. Follow [these](https://github.com/peterwittek/qml-rg/issues/8#issuecomment-282140692) instructions to get it right.

Meeting 4
---------
10.00-11.30, 16 March 2017, Seminar Room (201).

Papers:

- LeCun, Y.; Bengio, Y. & Hinton, G. [Deep learning](http://doi.org/10.1038/nature14539). *Nature*, 2015, 521, 436-444. This is a review paper by the three greatest giants in deep learning. The paper gives you an idea of the most important neural network architectures that we use today. The current flood of deep learning was unleashed on us by [this paper on convolutional neural networks](http://papers.nips.cc/paper/4824-imagenet-classification-with-deep-convolutional-neural-networks) by Geoff Hinton. It is also well worth reading: you seldom come across a paper that accumulated over 10,000 citations in five years. [This blog post](http://www.asimovinstitute.org/neural-network-zoo/) gives an entertaining overview of neural network architectures.

- Wiebe, N.; Kapoor, A. & Svore, K. M. [Quantum Deep Learning](http://arxiv.org/abs/1412.3489). *arXiv:1412.3489*, 2014. This is an insightful paper on stacked Boltzmann machines that highlights many possibilities and limitations of using quantum protocols for learning. It was also one of the first papers to consider Boltzmann machines for quantum-enhanced learning -- since then, this line of research took off and now there are N+1 papers on it.

Coding exercises:

- Implement Q-learning from scratch for a [simple toy example](Meeting 4/rl_toy_example.py). The state space is trivial and the agent has full access to it, there is no adversary and the distribution does not change depending on the actions of the agent. After the classical agent, try it with simulated quantum agents. See, for instance, [this paper](https://arxiv.org/abs/1401.4997) or [this one](https://arxiv.org/abs/1601.07358) for clues. The trivial solution is to replace the search by Grover's.

- Optional: Do the same thing with tic-tac-toe against a perfect AI (i.e., you cannot win). See the instructions in the [corresponding file](Meeting 4/tictactoe.py). Here the state and the action space might prove too large for a classical simulation of a quantum agent, so you might want to introduce heuristics to reduce it.

Tutorial 3
----------
16.00-17.30, 21 March 2017, Yellow Lecture Room (247).

The tutorial will be on Python and the scientific ecosystem: using Python for science and machine learning, plotting and visualization, how to write beautiful scientific code, and the best practices of providing a computational appendix to your papers.
