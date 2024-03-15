# ARIMA实现对车辆SOH的预测
***本项目较为简单，使用ARIMA实现对车辆SOH的预测，建议使用jupyter实现***

## 数据集介绍
  **该部分数据集是某车辆行驶的里程、时间和soh的记录，数据质量较高，可以不用差分处理，代码虽给出了差分但没有实际应用，字段意义如下：**  
  **vin：**
  车辆唯一识别码。  
  **start_time/end_time：**
  车辆数据采集开始时间，SOH是基于车辆充电计算的，所以存在时间段。  
  **org_soh：**
  车辆未经平滑处理的SOH。  
  **smooth_soh：**
  车辆平滑处理后的SOH。  
  **summileage：**
  车辆行驶里程。

 **arima_soh.ipynb:**
 使用原始的数据，利用arima模型进行预测。

 **interpolated_mean.ipynb：**
 取原始数据中的年月日日期，以周分组求取平均，再对数据插值处理，使用arima对处理后的数据进行预测。

