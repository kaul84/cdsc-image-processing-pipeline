# Overview #

The [Center for Domain Specific Computing](http://www.cdsc.ucla.edu) is developing a methodology and hardware platform with the goal of looking beyond parallelization and focusing on domain-specific customization to bring orders-of-magnitude power-performance efficiency improvement to important application domains. This effort involves both software and hardware innovations that include the development of:
  * A wide range of customizable computing elements, from heterogeneous fixed cores to coarse-grain customizable cores and fine-grain field-programmable circuit fabrics
  * High-performance RF-interconnects
  * Highly automated compilation tools and runtime management systems

As an application area for these developments, the Center is analyzing the domain of medical image processing, which has a high computing demand. Medical imaging is now a routine and integral clinical tool in the diagnosis and treatment of many conditions, but many advances in this field have been constrained to the research environment due to a lack of computational power. Several medical image processing algorithms are infeasible for real-time clinical use. Power and cost-efficient high-performance computing can have a significant impact on healthcare in terms of preventive medicine (e.g., virtual colonoscopy), diagnostic procedures (e.g., automated tumor volume quantification), and therapeutic procedures (e.g., pre-surgery decision making).

## About this Project ##

A medical imaging pipeline typically consists of the following steps:
  * Image reconstruction
  * Image restoration
  * Registration
  * Segmentation
  * Analysis

Algorithms vary from one step to another, requiring different architecture support for the best efficiency. As part of the CDSC's efforts to disseminate knowledge, the Applications Thrust is releasing a set of medical image processing algorithms and supporting libraries that are being used as the driving applications for work within the Center. The purpose of this release is to provide the entire research community with access to these algorithms for comparison or incorporation into other projects. The algorithms and code, unless otherwise stated, are being released under the Lesser GNU Public License.

## What is Available ##

The initial release consists of three components:
  * **imageViewer:** A Java-based medical image viewer that supports basic manipulations, custom layouts, and annotations. Supports DICOM, Analyze 7.5, and RAW formats.
  * **Image processing pipeline plug-in:** A plug-in for the above imageViewer that ties together several image processing algorithms (denoising, registration, segmentation) with a front-end graphical user interface.
  * **Individual algorithms:** Each algorithm is being released individually along with each variant created (e.g., CUDA, HDL, etc). The goal is to provide interested parties with nontrivial demonstration of how original algorithms implemented in C/MATLAB are optimized and rewritten in Habanero C.

## What is Coming ##

In December, 2011, the CDSC is planning on releasing a Benchmark Server. The CDSC Benchmark Server aims to provide the public with a means for testing their image processing algorithms on the customizable heterogeneous platform being developed as part of the CDSC. The server is open to any researcher who wishes to share their algorithm with the team for the purposes of evaluation. The CDSC team will provide a set of application programming interfaces that the algorithm developer may use when interacting with the server. The algorithm must have a standardized method for inputting and obtaining images. The server will also provide means for accessing specific resources such as OpenMP and CUDA instructions. Once an algorithm developer is ready to submit his/her algorithm, the code is uploaded to the server. The algorithm developer may select to run one of several test collections (brain/chest) for the task of segmenting tumors. Seed points will be given for every image. The result of the execution will be runtime information (the time from start to finish), power consumption (an estimation of the number of Joules required to perform a task), and segmentation accuracy (deviation of segmentation from an averaged gold standard).

## Funding ##

This research is supported by the Center for Domain-Specific Computing (CDSC) funded by the NSF Expedition in Computing Award CCF-0926127.