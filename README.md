# **RISC-V Assembly Math Operations for Machine Learning Classification**

### **Overview**
This project was inspired by my passion for low-level programming and machine learning, developed during my experience in UC Berkeley’s CS61C course. The goal of this project is to implement key mathematical operations in RISC-V assembly, which are later used in a simple machine learning classification task. The journey involves working with integer arrays, matrix operations, and neural network-like classification, all within the realm of assembly language.

Though this project may seem technical, my aim was to bridge the gap between hardware and machine learning by understanding how fundamental operations are performed at the processor level.

---

### **Problem Statement**
At its core, this project implements fundamental math operations that are crucial for machine learning. The objective is to build RISC-V assembly functions for tasks such as:
- Absolute Value Calculation
- Rectified Linear Unit (ReLU)
- Argmax
- Dot Product
- Matrix Multiplication

These functions work together to classify input matrices, similar to a neural network’s process. In essence, I constructed the building blocks of a simple neural network in RISC-V assembly.

---

### **Methods**
The project starts by constructing individual mathematical operations in assembly language and testing them via a custom Python-based unit testing framework. The code is then optimized for both functionality and performance. 

1. **Task 1: Absolute Value Function**
   - Implemented a basic absolute value function for integer arrays, a building block for ReLU activation in neural networks.
   - Debugging and testing done using Venus (RISC-V simulator) and Python tests.
   
2. **Task 2: ReLU Function**
   - Developed the ReLU function to zero out negative integers in an array.
   - This function modifies the input array in place, emulating the behavior of ReLU in machine learning models.
   
3. **Task 3: Argmax Function**
   - Identified the index of the largest element in an integer array.
   - This is useful for classification tasks in neural networks, where the output class is the index of the largest value in the output array.
   
4. **Task 4: Dot Product Function**
   - Implemented dot product functionality between two integer arrays, with customizable strides. This is the foundation for matrix multiplication.
   
5. **Task 6: Matrix Multiplication**
   - Performed matrix multiplication using the dot product of row and column vectors.
   - This is a critical function in machine learning for transforming data between layers of a neural network.
   
6. **Task 9: Neural Network-like Classification**
   - Integrated all the math functions (dot product, ReLU, argmax) to classify input data by reading and processing matrix files.
   - The final step involved computing matrix products and applying the argmax function to determine the predicted class.

---

### **Workflow**
- **Assembly Language**: All functions were written in RISC-V assembly to demonstrate how low-level operations can perform high-level machine learning tasks.
- **Debugging**: Leveraged Venus's built-in debugger (**VDB**) to identify bugs and ensure correct memory handling.
- **Venus RISC-V Simulator**: A web-based simulator for running and debugging RISC-V assembly code.
- **Testing Framework**: Python-based unit tests were compiled into RISC-V assembly and tested using Venus. Memcheck was utilized to catch memory access errors.



---

### **Findings**
The process of building these fundamental functions in assembly revealed key insights:
- **Optimization at the Hardware Level**: Writing these operations in assembly provided a deeper understanding of how hardware-level operations affect the speed and efficiency of machine learning algorithms.
- **Memory Management**: Assembly requires precise control over memory, forcing me to be deliberate about memory allocation and access, an essential skill in systems programming.
- **Bridging Machine Learning and Low-Level Programming**: This project served as a bridge between two of my interests—machine learning and low-level programming—allowing me to explore the relationship between high-level algorithms and their hardware implementations.

---

### **Code Details**

Below is an overview of how the implemented functions interact in a neural network-like process:


1. **Input Matrix**: The input is a matrix of integers, representing features.
2. **Matrix Multiplication**: The input is transformed by multiplying it with weight matrices (mimicking layers of a neural network).
3. **ReLU Activation**: The ReLU function sets negative values to 0, introducing non-linearity.
4. **Argmax**: The largest value in the final matrix determines the predicted class.

---

### **Tools Used**
- **RISC-V Assembly**: Core language for all function implementations.
- **Venus Simulator**: A web-based RISC-V simulator for running, testing, and debugging assembly code.
- **Python**: Used for unit testing and converting test cases into RISC-V assembly.
- **Memcheck**: A tool for catching memory-related bugs, such as invalid memory access.
- **VDB (Venus Debugger)**: Essential for step-by-step debugging of assembly instructions.

---

### **Conclusion**
This project not only deepened my understanding of assembly language and low-level computation but also expanded my perspective on how machine learning algorithms function at the hardware level. By blending concepts from machine learning and systems programming, this project showcases my ability to tackle problems that span multiple layers of the computing stack—from hardware to algorithms.

Though the code cannot be published due to course regulations, this project represents a significant step forward in my journey toward bridging machine learning with systems programming.

---

### **Future Work**
I plan to continue refining my understanding of systems programming, possibly applying similar low-level optimization techniques to more advanced machine learning models or parallel computing projects.

