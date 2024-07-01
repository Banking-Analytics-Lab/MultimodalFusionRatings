### ***GROUP 1- Simple Concatenation***
 
In this group, each numerical dataset separately passed through a network.  We then concatenated their penultimate layers, and the simple intermediate level of fusion was used.
Following are the architectures of each base model:

 - CNN based Model: [View architecture](11.pdf)
 - LSTM based Model: [View architecture](12.pdf)
 - GRU based Model: [View architecture](13.pdf)
 - BERT based Model: [View architecture](14.pdf)

   
### ***GROUP 2- Simple Concatenation-Attention***
 
In this group, an initial phase involved training four distinct numeric channels individually, while the text channel underwent training via another Network. After completion of training, the penultimate layer of the numeric modalities was concatenated. In the final step, fusion was executed between the text layer and the concatenated layer employing the cross-attention technique. Therefore, this architecture utilizes a simple Concatenation-Attention fusion approach.


 - CNN based Model: [View architecture](21.pdf)
 - LSTM based Model: [View architecture](22.pdf)
 - GRU based Model: [View architecture](23.pdf)
 - BERT based Model: [View architecture](24.pdf)

### ***GROUP 3- Hybrid Concatenation***
 
In this group, this architecture employed a hybrid fusion approach. In this manner, all numerical datasets underwent early fusion, functioning as inputs for a Network. Conversely, text data underwent training via another Network. Subsequently, intermediate fusion was executed, and the penultimate layers of distinct modalities were merged through concatenation of their corresponding output layers.


 - CNN based Model: [View architecture](31.pdf)
 - LSTM based Model: [View architecture](32.pdf)
 - GRU based Model: [View architecture](33.pdf)
 - BERT based Model: [View architecture](34.pdf)

### ***GROUP 4- Hybrid Concatenation-Attention***
 
In this group, a hybrid architecture has been implemented. An initial fusion of all numerical datasets was conducted (signal fusion), resulting in the concatenation of the numerical channel for the training of a Network. Meanwhile, the text channel was directed to the other Network, and the output layers were combined utilizing cross-attention fusion.



 - CNN based Model: [View architecture](41.pdf)
 - LSTM based Model: [View architecture](42.pdf)
 - GRU based Model: [View architecture](43.pdf)
 - BERT based Model: [View architecture](44.pdf)
