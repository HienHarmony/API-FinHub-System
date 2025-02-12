# Real-time Financial Market Data Pipeline and Kafka

Dự án này nhằm mục đích xây dựng một đường ống dữ liệu phát trực tuyến bằng cách sử dụng thư viện yfinance dữ liệu thị trường tài chính Việt Nam . Kiến trúc của nó chủ yếu bao gồm năm lớp:  Data Ingestion, Message broker, Stream processing, Serving database, and Visualization. 

Quy trình bao gồm một số thành phần, bao gồm một producer tìm nạp dữ liệu từ yfinancer và gửi nó đến một Topics Kafka, một Cluster Kafka để lưu trữ và xử lý dữ liệu. Để xử lý luồng, Apache Spark sẽ được sử dụng. Tiếp theo, Cassandra được sử dụng để lưu trữ dữ liệu thị trường tài chính của pipeline streamming. Grafana được sử dụng để tạo bảng điều khiển cuối cùng hiển thị các biểu đồ và đồ thị theo thời gian thực dựa trên dữ liệu trong cơ sở dữ liệu, cho phép người dùng theo dõi dữ liệu thị trường trong thời gian thực và xác định xu hướng và mô hình.
