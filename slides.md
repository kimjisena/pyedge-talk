---
theme: apple-basic
layout: intro-image
image: '/pyedge-intro.jpg'
title: pyedge
transition: fade-out
---

<div class="absolute top-10 ml-4">
  <h1>pyedge</h1>
  <p>python bindings for low-level languages</p>
</div>

<div class="absolute bottom-10 ml-4">
  <img src="/kimjisena.jpg" alt="Kim Jisena" class="h-20 mb-4 rounded-full shadow" />
  <a href="https://x.com/kimjisena" target="_blank">
    <span class="font-700">
      @kimjisena
    </span>
  </a>
</div>
<!--
- introduce yourself
- introduce the subject
- lighten the mood
- get comfortable
-->

---

<div class="absolute top-30 right-40 ml-4 w-50 h-50">
  <iframe src="https://giphy.com/embed/0Vv0Ne2CnOClIExIuL" width="100%" height="100%" style="position:absolute" frameBorder="0" class="giphy-embed" allowFullScreen></iframe>
</div>


# why combine python and c?

<v-clicks>

- performance optimization

- versatility

- ecosystem integration

</v-clicks>

<!-- visible after 3 clicks -->
<v-clicks at="3">

  <div class="mt-10">

  **notable projects**

  numpy, pandas, scikit-learn, pytorch and tensorflow

  </div>
</v-clicks>

<!--
- **performance optimization:**
  - python excels in high-level tasks, but for performance-critical components, the speed of C can significantly enhance overall application performance

- **versatility:**
  - python's versatility makes it an excellent choice for a wide range of tasks, while c can handle computationally intensive operations efficiently

- **ecosystem integration:**
  - leveraging c allows seamless integration with existing c libraries and ecosystems, expanding the capabilities of Python applications
-->

---

# overview of python `ctypes` module

- `ctypes` is a foreign function interface (ffi) module in python, allowing the calling of functions from dynamic link libraries/shared libraries

- **use cases**
  - interfacing with libraries written in low-level languages like c or c++
  - accessing shared libraries for system-level interactions

```python {1,2|4,5|7,8|all}
# 1.  import the module
import ctypes

# 2. load the shared library
lib = ctypes.CDLL('./lib.so')

# 3. call function from the library
lib.fast_func()
```
<!-- 
demonstrate the use of the `ctypes` module 

- switch to branch `step-0-hello-world`
- write c code
- write python code
- compile c code
- run program
-->

---

# understanding sobel edge detection
<v-clicks>

- sobel edge detection is a technique used to highlight edges in an image
- it employs the sobel operator, a convolution-based method, to emphasize changes in intensity between pixels

- **edge detection**
  - edges represent significant transitions in image intensity and often correspond to object boundaries
  - sobel helps identify these transitions, making it valuable for various computer vision and image processing tasks

- **application**
  - used in computer vision, image analysis, and feature extraction
  - enables the detection of key features in images, forming the basis for various image processing applications

</v-clicks>

<!--

- explain sobel edge detection
- use `excalidraw.io` for illustrations

**conceptual illustration**
  - imagine viewing an image as a landscape of intensity
  - sobel acts like a filter, emphasizing areas where the intensity changes abruptly, revealing the contours of objects
  
-->

---

# python: a powerful high-level language

- **handling user input**
  - utilizing the `argparse` module for robust and user-friendly command-line argument parsing

  ```python
  def parse_arguments():
    # ...
  ```
- **file operations**
  - leveraging the `PIL` (pillow) library for opening and manipulating images
  ```python
  def load_image(file_path):
    # ...

  def save_image(file_path, result_image):
    # ...
  ```
<!--

explain the high level functionalities that python will handle

- `parse_arguments()`
- `load_image()`
- `save_image()`
-->

---

# seamless integration with c

- **python interfacing with low-level languages**
  - pyedge integrates Python with C to harness performance benefits
  - utilizes the `ctypes` module to facilitate communication between python and c components

  ```python
  # creating ctypes pointers
  input_ptr = (ctypes.c_ubyte * len(input_array)).from_buffer(input_array)
  ```

- **using pointers for data exchange**
  - python's `ctypes` enables the creation of pointers for efficient data exchange between python and c
  - pointers facilitate the passing of data structures, enhancing the performance of critical operations

---

# performance-critical implementation in c

- **showcasing c code for sobel edge detection**
  - the `sobel.h` header file defines the c function responsible for sobel edge detection
  - the `sobel_edge_detection_c` function takes input, processes it, and produces the result

  ```c
  // sobel.h
  void sobel_edge_detection_c(unsigned char* input, unsigned char* result, int width, int height);
  ```

- **performance benefits**
  - c provides lower-level control and direct access to hardware, optimizing computation-heavy tasks
  - the performance benefits of the c implementation enhance the speed and efficiency of the sobel edge detection algorithm

<!--

as you are nearing the end of this slide, ask the audience to share pictures for 
edge detection

-->

---

# sobel edge detection in action

<div style="width:100%;height:0;padding-bottom:49%;position:relative;"><iframe src="https://giphy.com/embed/ZkuzNEs9e1ZIHWhBBs" width="100%" height="100%" style="position:absolute" frameBorder="0" class="giphy-embed" allowFullScreen></iframe></div>

<!--
show the code, switching from one branch to another
-->

---

# the power of collaboration

<v-clicks depth="2">

- **advantages of combining python and c**
  - **performance optimization**
    - python's high-level expressiveness combined with c's low-level efficiency
    - performance-critical components benefit from c's speed, win win

  - **versatility in ecosystems**
    - python's extensive ecosystem is enriched by seamlessly integrating with c libraries
    - access to low-level languages extends Python's capabilities

- **python's versatility in working with c**
  - **`ctypes` module**
    - a seamless way to interface with c code
    - simplifies communication, enabling python to harness the performance advantages of c

</v-clicks>

---

# questions
<div style="width:100%;height:0;padding-bottom:50%;position:relative;"><iframe src="https://giphy.com/embed/xT5LMB2WiOdjpB7K4o" width="100%" height="100%" style="position:absolute" frameBorder="0" class="giphy-embed" allowFullScreen></iframe></div>