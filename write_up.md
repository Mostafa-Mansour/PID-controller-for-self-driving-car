# Reflections
---

* Proportional, differential and integral coefficients are tuned manually by try and error.

* Using Proportional term only will make the car vibrating around the lane center and them lead to car spinning and the control over it will be lost. In this [video](https://youtu.be/-ySUJFw2RGY) I show how using a proportional factor only will lead to car vibrating around lane center and then car spinning.

* Using proportional and differential terms will give good results but we should take care from the values of the differential factor. The bigger the value of the differential factor. From the one side, the faster the car turning to a lane center and this can make passengers bad due to sharp turns. From the other side, the smaller the value of the differential factor, the slower the car turns to lane center and this may lead to losing a control over a car and the car may drift away from the road. This [video](https://youtu.be/8aRP0rRFIUo) shows the effect of differential factor on car performance.

*So, we need to tune the values of P and D factors. I start with random small number and make the D factor a little bit bigger than P factor. Then I start to change P slightly to get the best performance for a given D, then change D to get a higher performance for PID controller.

*Using P and D factors only can be good in ideal cases where there is no biases in car wheels which is not the case. So, I add an international factor, a small factor, to compensate biasing errors.

* PID works well in the simulation.

* The values can be tuned using twiddle technique.




