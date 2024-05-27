# JMeter-Test
# Kiểm tra hiệu năng trang web

## Mục tiêu:

- Sử dụng jMeter để tạo một kịch bản kiểm tra mô phỏng người dùng truy cập 2 trang web https://www.instagram.com/ và https://www.facebook.com/
- Chạy kịch bản kiểm tra và ghi lại kết quả.
- Phân tích kết quả kiểm tra, bao gồm thời gian phản hồi, số lượng yêu cầu thành công, số lượng yêu cầu thất bại, v.v.
- Dựa trên kết quả phân tích, đưa ra kết luận về hiệu năng của trang web.

## Kịch bản:

- Thread Group
  - Number of Threads (users): 100
  - Ramp-Up Period (in seconds): 10
  - Loop Count: 5
- HTTP Request:
  - URL: https://www.instagram.com/
  - Method: GET
  - Content encoding: UTF-8
- Listeners:
  - View Results Tree
  - Aggregate Report

![image](https://github.com/tr4duc/JMeter-Test/assets/96672630/255b0a03-61f9-428d-8ce1-29f89e185a37)

## Phân tích kết quả kiểm tra:
- Số lượng yêu cầu thành công: 998/1000 = 99,8%
- Số lượng yêu cầu thất bại: 2/1000 = 0,2%
- Thời gian phản hồi trung bình: 40 ms
- Thời gian phản hồi trung vị: 38 ms
- Thời gian phản hồi percentil 90: 70 ms
- Chuyển tải: 16 yêu cầu/giây

![image](https://github.com/tr4duc/JMeter-Test/assets/96672630/1e9dd1f0-f1ab-4f60-b6b0-b3b901f21c60)

## Phân tích kết quả kiểm tra:
- Số lượng yêu cầu thành công: 995/1000 = 99,5%
- Số lượng yêu cầu thất bại: 5/1000 = 0,5%
- Thời gian phản hồi trung bình: 50 ms
- Thời gian phản hồi trung vị: 48 ms
- Thời gian phản hồi percentil 90: 80 ms
- Chuyển tải: 14 yêu cầu/giây

## Kết luận Tổng thể
Từ các số liệu phân tích trên, chúng ta có thể đưa ra các kết luận sau:

- Instagram vượt trội hơn về mặt hiệu năng so với Facebook khi xét về thời gian phản hồi trung bình, trung vị, và thời gian phản hồi ở bách phân vị thứ 90.
- Instagram cũng cho thấy độ tin cậy cao hơn với tỷ lệ yêu cầu thành công cao hơn và thông lượng tốt hơn.
- Facebook mặc dù có hiệu năng không kém quá xa so với Instagram nhưng vẫn cần cải thiện để đạt được mức hiệu năng tương đương, đặc biệt trong các trường hợp tải cao.

Như vậy, dựa trên kết quả kiểm thử hiệu năng, Instagram có thể được xem là có hiệu năng tốt hơn so với Facebook trong các điều kiện kiểm thử đã thực hiện.
