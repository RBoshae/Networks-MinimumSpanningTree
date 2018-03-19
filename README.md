# Spanning Tree Protocol

In this project I implement the spanning tree protocol using Python. The Spanning	Tree protocol is used	to build loop	free networks	while	still	allowing backup links	for
fault	 tolerance. The	STP	 algorithm creates a spanning tree within a set of connected bridges/switches by disabling links that are not part of the spanning tree.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

To run this code you need mininet installed on your machine.

### Installing

For instructions on how to install mininet please refer to this [link](http://mininet.org/download/)

## Running the tests

Once mininet has been installed on your machine you are ready to run the program.

Start by opening mininet with the following code:

```
sudo mn --custom projecttopo.py --topo projecttopo
```

Next, open four nodes using xterm.

```
xterm b1 b2 b3 b4
```

For each opened node run the code by typing the following.

```
python bridge.py
```

Each node will begin the Spanning Tree algorithm until a root is established. Once a root is established, the root will send BPDU's every 5 seconds. Each Node will forward the BPDU to their Designated ports.

### Done Testing, Time For Cleanup

To quit the algorithm press ctrl-c

```
ctrl-c
```

Exit mininet by typing:
```
exit
```

Once you are back on your normal terminal cleanup mininet by typing:
```
mn -c

```

You are done. Thank you for testing.

## Author

* **Rick Boshae** - [Personal Website](rboshae.github.io)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Dr. Mart Molle
* Elizabeth Liri
