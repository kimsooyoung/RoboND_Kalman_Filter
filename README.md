# RoboND_Kalman_Filter

Kalman Filter를 구현하는 C++ 예제들입니다.

다음과 같은 예제들이 포함되어 있습니다. 

* Lesson2_1D_Gaussian
* Lesson2_StatePrediction
* Lesson2_MeasurementUpdate
* Lesson2_1DKalmanFilter
* Lesson2_MultidimensionalKF


## Usage

```bash
# clone repo
git clone https://github.com/kimsooyoung/RoboND_Kalman_Filter.git

# build
cd RoboND_Kalman_Filter/<example-name>
cd build && rm -rf *
cmake .. && make

# run executable project
./<project-name>
```

## Projects

### Lesson2_1D_Gaussian

* 다음과 같은 정규분포의 수식을 C++ 코드로 표현해봅니다.

![](Images/Untitled%205.png)

## StatePrediction &  MeasurementUpdate

* 칼만 필터를 이루는 주요한 두 부분을 구현해봅니다.

![](Images/Untitled%208.png)
![](Images/Untitled%2016.png)

### Lesson2_StatePrediction

* 로봇의 motion은 다음과 같이 두 정규분포의 합으로 생각할 수 있습니다. 이를 수식으로 표현하면 다음과 같으며 코드로 구현해봅니다.

![](Images/Untitled%2015.png)

* 로봇이 움직임에 따라, 그 위치를 점차 불확실해지며, 그림으로 표현하면 다음과 같습니다.

![](Images/Untitled%2014.png)
![](Images/Untitled%204.png)

### Lesson2_MeasurementUpdate

* 로봇에 달려있는 센서를 통해 로봇의 위치를 알 수 있습니다!

![](Images/Untitled%2013.png)

* 이를 수학적으로 표현해보면 다음과 같고, 마찬가지로 코드로 구현해 봅니다.

![](Images/Untitled%2010.png)
![](Images/Untitled%2011.png)

### Lesson2_1DKalmanFilter

* 앞서 살펴본 Prediction / Measurement를 반복하는 1차원 Kalman Filter를 구현해봅니다.

![](Images/Untitled%2017.png)

### Lesson2_MultidimensionalKF

* Kalman Filter는 measurement 할 수 없는 정보도 유추할 수 있는 장점이 있습니다. 이 예제에서는 위치 정보를 통해 속도까지 예측하는 구현을 해봅니다.

![](Images/Untitled%2017.png)


* Kalman Filter의 전 과정 수식을 다음과 같습니다. 여기서는 C++의 Eigen을 사용하여 행렬 연산을 하게 됩니다.

![](Images/Untitled%2046.png)

## Reference

* Udacity - Robotics Software Engineer Nanodegree