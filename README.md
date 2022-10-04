## Self Driving Cars

<img src = https://www.rd.com/wp-content/uploads/2022/08/self-driving-cars-GettyImages-1292394282-JVedit.jpg width=500>

An autonomous car is a vehicle capable of sensing its environment and operating without human involvement. A human passenger is not required to take control of the vehicle at any time, nor is a human passenger required to be present in the vehicle at all. An autonomous car can go anywhere a traditional car goes and do everything that an experienced human driver does.

## How do they work?

Autonomous cars rely on sensors, actuators, complex algorithms, machine learning systems, and powerful processors to execute software.

Autonomous cars create and maintain a map of their surroundings based on a variety of sensors situated in different parts of the vehicle. Radar sensors monitor the position of nearby vehicles. Video cameras detect traffic lights, read road signs, track other vehicles, and look for pedestrians. Lidar (light detection and ranging) sensors bounce pulses of light off the car’s surroundings to measure distances, detect road edges, and identify lane markings. Ultrasonic sensors in the wheels detect curbs and other vehicles when parking.

Sophisticated software then processes all this sensory input, plots a path, and sends instructions to the car’s actuators, which control acceleration, braking, and steering. Hard-coded rules, obstacle avoidance algorithms, predictive modeling, and object recognition help the software follow traffic rules and navigate obstacles.

## Self Driving Cars promises

The scenarios for convenience and quality-of-life improvements are limitless. The elderly and the physically disabled would have independence. If your kids were at summer camp and forgot their bathing suits and toothbrushes, the car could bring them the missing items. You could even send your dog to a veterinary appointment.

But the real promise of autonomous cars is the potential for dramatically lowering CO2 emissions. In a recent study, experts identified three trends that, if adopted concurrently, would unleash the full potential of autonomous cars: vehicle automation, vehicle electrification, and ridesharing. By 2050, these “three revolutions in urban transportation” could:

* Reduce traffic congestion (30% fewer vehicles on the road)
* Cut transportation costs by 40% (in terms of vehicles, fuel, and infrastructure)
* Improve walkability and livability
* Free up parking lots for other uses (schools, parks, community centers)
* Reduce urban CO2 emissions by 80% worldwide 


## Vision Transformers(ViT)

The concept of Vision Transformer (ViT) is an extension of the original concept of Transformer. It is only the application of Transformer in the image domain with slight modification in the implementation in order to handle the different data modality. More specifically, a ViT uses different methods for tokenization and embedding. However, the generic architecture remains the same. An input image is split into a set of image patches, called visual tokens. The visual tokens are embedded into a set of encoded vectors of fixed dimension. The position of a patch in the image is embedded along with the encoded vector and fed into the transformer encoder network which is essentially the same as the one responsible for processing the text input. 

<img src=https://miro.medium.com/max/1400/1*l37va2Mu8Snx6LLb13430A.png width=700/>

There are multiple blocks in the ViT encoder and each block consists of three major processing elements: Layer Norm, Multi-head Attention Network (MSP) and Multi-Layer Perceptrons (MLP). Layer Norm keeps the training process on track and let model adapt to the variations among the training images. MSP is a network responsible for generation of attention maps from the given embedded visual tokens. These attention maps help network focus on most important regions in the image such as object(s). 

## General CNN vs. ViT talk

The differences between CNNs and Vision Transformers are many and lie mainly in their architectural differences.
In fact, CNNs achieve excellent results even with training based on data volumes that are not as large as those required by Vision Transformers.
This different behaviour seems to derive from the presence in the CNNs of some inductive biases that can be somehow exploited by these networks to grasp more quickly the particularities of the analysed images even if, on the other hand, they end up limiting them making it more complex to grasp global relations.

On the other hand, the Vision Transformers are free from these biases which leads them to be able to capture also global and wider range relations but at the cost of a more onerous training in terms of data.
Vision Transformers also proved to be much more robust to input image distortions such as adversarial patches or permutations.
However, choosing one architecture over another is not always the wisest choice, and excellent results have been obtained in several Computer Vision tasks through hybrid architectures combining convolutional layers with Vision Transformers.

## Word about NVIDIA paper

<img src=https://cdn1.dotesports.com/wp-content/uploads/2020/10/02082149/nvidia-768x432.jpg width=500>

In 2016 nvidia introduced <b>End-to-End Deep Learning for Self-Driving Cars</b> paper which used 3 camera provided images as input and the steering value as output and used CNN based model in order to take the decision. 

<img src=https://developer.nvidia.com/blog/parallelforall/wp-content/uploads/2016/08/data-collection-system-624x411.png width=500>

In our own implementation we will be developing a ViT instead of the CNN used in the paper. In general self driving car technologies have advanced in the last years exponentially and most of the solutions now are based on reinforcement learning but in this implementaion we will be formulating the problem in a supervised manner with the hardware scheme presented in the paper mentioned before.

The data collection process in the original data was based on real scinareos of driving on a wide variety of roads and in a diverse set of lighting and weather conditions. We gathered surface street data in central New Jersey and highway data from Illinois, Michigan, Pennsylvania, and New York. Other road types include two-lane roads (with and without lane markings), residential roads with parked cars, tunnels, and unpaved roads. In our implementation here we will be using Udacity simulator provided specially for this purpose. 

<img src=https://techcrunch.com/wp-content/uploads/2017/02/sim_image.png width= 500/>

## Used ViT Architecture

<img src = https://github.com/EssamMohamedAbo-ElMkarem/Self-Driving-Car-using-ViT/blob/main/model.png/>

## Training vs. Validation Loss

<img src=https://github.com/EssamMohamedAbo-ElMkarem/Self-Driving-Car-using-ViT/blob/main/loss.png/>
