# IS403_O21_13

# GVHD: PGS.TS Nguyễn Đình Thuân
# Trợ giảng: Nguyễn Minh Nhựt

## Danh sách thành viên nhóm 13: 
|  MSSV  |          Họ Tên           |          GMail         |          Model         |
|:------:|:------------------------:|:----------------------:|:----------------------:|
|21520086|Huỳnh Lê Phong            |21520086@gm.uit.edu.vn  |        ARIMA, VAR      |
|21521556|Nguyễn Quốc Trạng         |21521556@gm.uit.edu.vn  |   RNN, RANDOM FOREST   |
|21522812|Nguyễn Triệu Vy           |21522812@gm.uit.edu.vn  | LINEAR REGRESSION, TiDE|
|20521541|Vũ Thị Phương Linh        |20521541@gm.uit.edu.vn  |         GRU, MLP       |
|21522218|Đỗ Đình Đăng Khoa         |21522218@gm.uit.edu.vn  |     LSTM, AUTOFORMER   |

## Tổng quan dự án
Báo cáo này nghiên cứu về chất lượng không khí tại ba thành phố lớn ở Việt Nam: Hà Nội, Hạ Long và Việt Trì. Mục tiêu là sử dụng các kỹ thuật phân tích chuỗi thời gian tiên tiến để dự báo và hiểu chỉ số PM2.5, góp phần vào việc giải quyết vấn đề ô nhiễm không khí và thúc đẩy môi trường đô thị bền vững.

### Phương pháp
Nhóm đã áp dụng một loạt các thuật toán từ truyền thống đến tiên tiến, bao gồm Hồi quy tuyến tính, mô hình ARIMA, mạng nơ-ron hồi quy (RNN), đơn vị hồi quy cổng (GRU), bộ nhớ ngắn hạn - dài hạn (LSTM), hồi quy vector (VAR), rừng ngẫu nhiên (Random Forest), mô hình mã hóa dày chuỗi thời gian (TiDE), Autoformer, và mạng nơ-ron đa tầng (MLP).

### Bộ dữ liệu
Báo cáo sử dụng 3 bộ dữ liệu lấy từ dữ liệu chất lượng không khí trên trang web aqicn.org từ 01/03/2019 - 01/06/2024 ở 3 thành phố Hà Nội, Hạ Long và Việt Trì. Sử dụng chỉ số pm2.5 để dự đoán.

### Kết quả
Hiệu suất của các mô hình được so sánh dựa trên ba chỉ số: MAPE, RMSE, và MAE. Hai mô hình có hiệu suất tốt nhất là GRU và MLP, được sử dụng để dự báo chất lượng không khí trong 90 ngày tiếp theo từ ngày 2/6/2024.


## Số liệu hiệu suất trên bộ dữ liệu pm2.5 ở Hạ Long

| **Model**           | **Ratio** | **RMSE** | **MAE** | **MAPE (%)** |
|---------------------|-----------|----------|---------|--------------|
|                     | 7-3       | 12.48    | 9.62    | 26.55        |
| LINEAR REGRESSION   | 8-2       | 13.17    | 10.12   | 30.13        |
|                     | 9-1       | 15.28    | 11.29   | 21.79        |
|                     | 7-3       | 14.27    | 11.53   | 38.34        |
| ARIMA               | 8-2       | 14.49    | 11.77   | 39.81        |
|                     | 9-1       | 18.50    | 16.46   | 42.62        |
|                     | 7-3       | 12.06    | 9.36    | 28.23        |
| VAR                 | 8-2       | 13.10    | 10.17   | 31.21        |
|                     | 9-1       | 12.44    | 9.14    | 18.77        |
|                     | 7-3       | 5.29     | 4.20    | 11.60        |
| Random Forest       | 8-2       | 4.67     | 3.70    | 10.88        |
|                     | 9-1       | 4.71     | 3.74    | 8.61         |
|                     | 7-3       | 8.76     | 6.94    | 19.54        |
| RNN                 | 8-2       | 9.21     | 7.38    | 20.93        |
|                     | 9-1       | 13.58    | 12.08   | 28.23        |
|                     | 7-3       | 7.04     | 5.80    | 14.10        |
| MLP                 | 8-2       | 3.98     | 3.18    | 9.11         |
|                     | 9-1       | 4.00     | 3.17    | 7.52         |
|                     | 7-3       | 7.09     | 5.97    | 13.57        |
| GRU                 | 8-2       | 6.84     | 13.35   | 5.85         |
|                     | 9-1       | 5.20     | 4.38    | 8.66         |
|                     | 7-3       | 26.35    | 24.60   | 58.96        |
| LSTM                | 8-2       | 22.14    | 20.02   | 47.18        |
|                     | 9-1       | 27.13    | 25.87   | 55.53        |
|                     | 7-3       | 12.67    | 9.67    | 26.33        |
| TiDE                | 8-2       | 18.53    | 16.29   | 53.34        |
|                     | 9-1       | 13.14    | 10.23   | 22.95        |
|                     | 7-3       | 12.14    | 9.36    | 27.45        |
| Autoformer          | 8-2       | 13.14    | 10.26   | 32.43        |
|                     | 9-1       | 15.67    | 11.66   | 22.43        |


## Số liệu hiệu suất trên bộ dữ liệu pm2.5 ở Hà Nội

| **Model**           | **Ratio** | **RMSE** | **MAE** | **MAPE (%)** |
|---------------------|-----------|----------|---------|--------------|
|                     | 7-3       | 51.26    | 42.36   | 46.14        |
| LINEAR REGRESSION   | 8-2       | 30.01    | 21.71   | 23.65        |
|                     | 9-1       | 34.86    | 25.56   | 23.76        |
|                     | 7-3       | 41.83    | 32.03   | 34.23        |
| ARIMA               | 8-2       | 36.78    | 28.35   | 30.36        |
|                     | 9-1       | 44.69    | 40.51   | 52.87        |
|                     | 7-3       | 43.02    | 33.01   | 34.66        |
| VAR                 | 8-2       | 33.68    | 25.09   | 26.72        |
|                     | 9-1       | 28.47    | 20.81   | 19.86        |
|                     | 7-3       | 8.52     | 6.57    | 8.25         |
| Random Forest       | 8-2       | 8.23     | 6.39    | 7.91         |
|                     | 9-1       | 9.35     | 7.51    | 8.61         |
|                     | 7-3       | 49.36    | 44.18   | 55.23        |
| RNN                 | 8-2       | 52.56    | 48.51   | 62.20        |
|                     | 9-1       | 42.88    | 39.47   | 45.89        |
|                     | 7-3       | 7.06     | 5.34    | 6.63         |
| MLP                 | 8-2       | 7.63     | 5.75    | 7.11         |
|                     | 9-1       | 8.43     | 6.50    | 7.29         |
|                     | 7-3       | 7.05     | 6.40    | 7.35         |
| GRU                 | 8-2       | 9.43     | 8.76    | 7.89         |
|                     | 9-1       | 3.25     | 2.45    | 2.43         |
|                     | 7-3       | 50.99    | 46.98   | 55.33        |
| LSTM                | 8-2       | 42.06    | 38.77   | 46.54        |
|                     | 9-1       | 56.05    | 52.83   | 56.89        |
|                     | 7-3       | 72.62    | 60.77   | 83.88        |
| TiDE                | 8-2       | 49.92    | 40.00   | 54.50        |
|                     | 9-1       | 28.40    | 21.45   | 21.76        |
|                     | 7-3       | 50.08    | 41.07   | 44.73        |
| Autoformer          | 8-2       | 25.18    | 18.85   | 23.51        |
|                     | 9-1       | 26.91    | 20.11   | 20.61        |

## Số liệu hiệu suất trên bộ dữ liệu pm2.5 ở Việt Trì

| **Model**         | **Ratio** | **RMSE** | **MAE**  | **MAPE (%)** |
|-------------------|-----------|----------|----------|--------------|
|                   | 7-3       | 28.91    | 21.07    | 39.62        |
| LINEAR REGRESSION | 8-2       | 19.52    | 15.96    | 45.73        |
|                   | 9-1       | 25.77    | 21.05    | 36.69        |
|                   | 7-3       | 22.51    | 17.96    | 53.78        |
| ARIMA             | 8-2       | 23.04    | 17.26    | 37.96        |
|                   | 9-1       | 20.45    | 16.52    | 44.11        |
|                   | 7-3       | 22.72    | 17.04    | 42.66        |
| VAR               | 8-2       | 18.76    | 15.42    | 45.87        |
|                   | 9-1       | 17.35    | 14.54    | 30.51        |
|                   | 7-3       | 6.31     | 4.58     | 10.88        |
| Random Forest     | 8-2       | 5.06     | 3.80     | 9.66         |
|                   | 9-1       | 5.90     | 4.64     | 8.39         |
|                   | 7-3       | 19.97    | 16.70    | 41.66        |
| RNN               | 8-2       | 15.93    | 12.87    | 34.26        |
|                   | 9-1       | 14.03    | 11.57    | 25.25        |
|                   | 7-3       | 5.31     | 4.00     | 9.77         |
| MLP               | 8-2       | 5.16     | 11.67    | 4.07         |
|                   | 9-1       | 5.87     | 4.52     | 9.69         |
|                   | 7-3       | 4.32     | 12.92    | 3.80         |
| GRU               | 8-2       | 4.25     | 4.00     | 14.00        |
|                   | 9-1       | 5.29     | 5.24     | 12.22        |
|                   | 7-3       | 28.89    | 24.95    | 52.06        |
| LSTM              | 8-2       | 26.87    | 23.65    | 54.81        |
|                   | 9-1       | 34.99    | 32.43    | 60.89        |
|                   | 7-3       | 30.28    | 22.28    | 41.96        |
| TiDE              | 8-2       | 30.24    | 24.66    | 60.67        |
|                   | 9-1       | 28.36    | 24.03    | 42.76        |
|                   | 7-3       | 22.47    | 16.91    | 43.82        |
| Autoformer        | 8-2       | 22.52    | 18.93    | 69.40        |
|                   | 9-1       | 19.12    | 15.51    | 32.48        |

## Kết luận
Qua việc áp dụng các mô hình dự báo chất lượng không khí, nhóm đã tìm ra mô hình phù hợp nhất cho từng thành phố. Các mô hình GRU và MLP đã cho kết quả tốt nhất, giúp cung cấp dự báo chính xác về chỉ số PM2.5. Kết quả dự báo này có thể được sử dụng để hỗ trợ chính sách và biện pháp giảm thiểu ô nhiễm không khí.

## Tài liệu tham khảo
1. E. Marinov, D. Petrova-Antonova, and S. Malinov, “Time Series Forecasting of Air Quality: A Case Study of Sofia City,” Atmosphere, vol. 13, p. 788, 2022. [Online]. Available: [https://www.mdpi.com/2073-4433/13/5/788](https://www.mdpi.com/2073-4433/13/5/788)
2. K. N. Sh, I. Irfani, and U. Mukhaiyar, “Predicting Air Pollution Levels in Jakarta Using Vector Autoregressive Analysis,” Proceedings of the 5th International Conference on Statistics, Mathematics, Teaching, and Research 2023 (ICSMTR 2023), pp. 14-22, Atlantis Press, 2023. [Online]. Available: [https://doi.org/10.2991/978-94-6463-332-0_3](https://doi.org/10.2991/978-94-6463-332-0_3)
3. K. H. Waseem, H. Mushtaq, F. Abid, A. M. Abu-Mahfouz, A. Shaikh, M. Turan, and J. Rasheed, “Forecasting of Air Quality Using an Optimized Recurrent Neural Network,” Processes, vol. 10, no. 10, p. 2117, 2022. [Online]. Available: [https://doi.org/10.3390/pr1010211](https://doi.org/10.3390/pr1010211)
4. Esager, M.W.M.; Ünlü, K.D. “Forecasting Air Quality in Tripoli: An Evaluation of Deep Learning Models for Hourly PM2.5 Surface Mass Concentrations.” Atmosphere 2023, 14, 478. [Online]. Available: [https://doi.org/10.3390/atmos14030478](https://doi.org/10.3390/atmos14030478)
5. A. Das, W. Kong, A. Leach, S. Mathur, R. Sen, and R. Yu, “Long-term Forecasting with TiDE: Time-series Dense Encoder,” arXiv:2304.08424 [stat.ML], April 2023. [Online]. Available: [https://doi.org/10.48550/arXiv.2304.08424](https://doi.org/10.48550/arXiv.2304.08424)
6. B. T. Ong, K. Sugiura, and K. Zettsu, “Dynamically pre-trained deep recurrent neural networks using environmental monitoring data for predicting PM2.5,” Neural Comput Appl, vol. 27, no. 6, pp. 1553–1566, 2016. [Online]. Available: [https://doi.org/10.1007/s00521-015-1955-3](https://doi.org/10.1007/s00521-015-1955-3)
7. Y. B. Lim, I. Aliyu, and C. G. Lim, “Air pollution matter prediction using recurrent neural networks with sequential data,” In: Proceedings of the 2019 3rd International Conference on Intelligent Systems, Metaheuristics & Swarm Intelligence. ISMSI 2019, pp. 40–44, Association for Computing Machinery, New York, NY, USA, 2019. [Online]. Available: [https://doi.org/10.1145/3325773.3325788](https://doi.org/10.1145/3325773.3325788)
8. H. Wu, J. Xu, J. Wang, & M. Long, “Autoformer: Decomposition Transformers with Auto-Correlation for Long-Term Series Forecasting,” 2021.
