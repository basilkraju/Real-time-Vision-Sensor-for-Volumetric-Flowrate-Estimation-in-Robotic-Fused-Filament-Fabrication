# Real-time-Vision-Sensor-for-Volumetric-Flowrate-Estimation-in-Robotic-Fused-Filament-Fabrication.

Fused Filament Fabrication(FFF) process is an additive manufacturing method where we build a product by
depositing material layer by layer through a moving, heated
printer extruder head. The real time sensing and control of
different process parameters in the FFF process is important in
deciding the quality in terms of different properties of the finished
product. One of the important process parameters in FFF is the
output polymer flow rate. We can compute the output polymer
flow rate in the FFF process if we know the extrusion width
of the polymer flow. Extrusion width is the width of polymer
extruded through the nozzle. In this project, we have calculated
the extrusion width of the polymer flow in FFF with different
approaches based on computer vision. We used the videos of
the polymer flow taken at different deposition speeds to extract
the extrusion width. We tried different methods to improve the
latency in processing all the frames from each of the videos and
measuring the corresponding extrusion width from each of the
frames to achieve real time sensing of extrusion width.

![FFF Vision Canny Edge Detection.ipynb](https://github.com/basilkraju/Real-time-Vision-Sensor-for-Volumetric-Flowrate-Estimation-in-Robotic-Fused-Filament-Fabrication/blob/main/FFF%20Vision%20Canny%20Edge%20Detection.ipynb)  is the code in which different image processing steps and canny edge detection are used for finding the extrusion width.

## Image Processing Steps
Different image processing steps are used.

![Steps](https://user-images.githubusercontent.com/45179359/226188899-28303406-0d0d-4d2e-827d-05971e284898.jpg)

Mainly only two methods are used to reduce the computation time.
1. Image Processing followed by Canny Edge Detection.
2. Image Processing followed by Hough Transform.

In both cases the image processing steps are the same.The difference between them is
that one is used for edge detection (Canny) and the other is used for line detection
(Hough Transform).
Among the above canny perform well, so then we tried changing the programming
concept like vectorization and recursion.Recursion is a common mathematical and
programming concept which helps to loop through the data without using many for loops.
As like the recursion , vectorization is also used to speed up the python code without
using loops.
Since the Canny edge detection performed well, it is implemented in both above
programming concepts.Among that, recursive method shows less computational time
than vectorization.But since the recursive method usually allows only 1000 recursive calls, it cannot be used in production enviornment.


# Results

A summary plot showing comparison of the road width measurements resulting from the revised methods vs original method. x-axis is frame count, y-axis is measured road width. 5 such plots for each of the five deposition speeds (vR=10, 20, 30, 40, 50).
# vR = 10
![vR = 10](https://user-images.githubusercontent.com/45179359/226188247-d25f2cbe-6224-4735-bc10-253e571b51ce.png)
# vR = 20
![pasted image 0 (3)](https://user-images.githubusercontent.com/45179359/226188219-e87308cd-b790-4e1c-813f-cb72aab7bd32.png)
# vR = 30
![pasted image 0 (2)](https://user-images.githubusercontent.com/45179359/226188343-6dba2cc1-c813-455d-bc63-9f7fe9851e89.png)
# vR = 40
![pasted image 0 (1)](https://user-images.githubusercontent.com/45179359/226188322-c07a92ad-4f7f-4c1e-8ebe-0109bed72944.png)
# vR = 50
![pasted image 0](https://user-images.githubusercontent.com/45179359/226188316-9e4a2f32-1026-42be-a784-bf8c795cd39e.png)

The time taken for processing each frame and each video are calculated and attached to
the result sheet of each video and the final summary result sheet.
time.perf_counter() method is used to measure the time.
![image](https://user-images.githubusercontent.com/45179359/226279514-bad19f6e-846c-4ca2-9eba-8b737462ae2b.png)


## References
<a id ="1">[1]</a>
Rakshith. Badarinath; Basil K Raju; Mohammed Anshad Vittaldas Prabhu; Sinnu Susan Thomas,
“Real-time Vision Sensor for Volumetric Flowrate Estimation in Robotic Fused Filament Fabrication,” in IFAC World Congress, Yokohawa, Japan, Jul 9-14, 2023.
