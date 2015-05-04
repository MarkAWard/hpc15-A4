# hpc15-A4

I used the below image to time the performance of the convolution algorithm on different platforms.
![](/bike.jpg?raw=True "Original bike")

The final blurred version of the image looked like this:
![](/bike-blur.jpg?raw=True "Blurred bike")

Here are the times and performance measures for different devices and cofigurations:

| Platform/Device | local work group size | MPixels/s | GBit/s | GFlop/s |
|:---------------:|:---------------------:|:---------:|:------:|:-------:|
| MacBook Pro Iris | 20x20 | 202.01 | 1.62 | 9.78 |
|  | 16x16| 247.88 | 1.98 | 11.99 |
|  | 8x8 | 233.54 | 1.87 | 11.30 |
|  | 4x4 | 77.58 | 0.62 | 3.76 |
| cuda3 Tesla T10 | 20x20 | 289.57 | 2.32 | 14.02 |
|  | 16x16| 320.99 | 2.57 | 15.54 |
|  | 8x8 | 281.64 | 2.25 | 13.63 |
|  | 4x4 | 152.37 | 1.22 | 7.38 |
| opencl1 Cypress | 16x16| 282.38 | 2.27 | 13.71 |
|  | 8x8 | 208.96 | 1.67 | 10.11 |
|  | 4x4 | 48.39| 0.39 | 2.34 |

We can see that I did not get better performance using a different local work group size instead of the default 16x16.


