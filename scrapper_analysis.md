
# Tổng Quan

Dự án nhằm triển khai một Scrapper để thu thập dữ liệu các bài viết (giới hạn phân tích bao gồm 300 bài viết) từ trang web [viettel.idc.com.vn](https://viettel.idc.com.vn). Sau đó, thông qua chỉ số Gunning Fox Index, dự án thực hiện phân tích độ đọc hiểu của các bài viết.

# Mục Đích

Dự án này hướng đến việc phân tích độ đọc hiểu của các bài viết. Từ đó, dự án có thể đề xuất những cải tiến để nâng cao thứ hạng bài viết cho Viettel.

# Hướng Dẫn Cài Đặt

1. Tạo môi trường ảo và cài đặt các thư viện cần thiết:

```bash
python3 -m venv scrapper_env
source scrapper_env/bin/activate
pip3 install -r requirements.txt
```

2. Khởi chạy chương trình:

```bash
python3 main.py --target prod --thread False
```

3. Cấu hình thông tin Scrapper bằng file YAML.

# Quy Trình Hoạt Động

1. **Cấu hình Scrapper**:
   - Các thông tin Scrapper được khai báo trong file YAML.

2. **Trích Xuất Đường Link Bài Viết**:
   - Thu thập danh sách link bài viết, kết quả trả về là một danh sách.

3. **Xử Lý Trang Bài Viết**:
   - Module `page_parse` sẽ xử lý trích xuất nội dung dựa theo link bài viết.

4. **Lưu Trữ Dữ Liệu**:
   - Các bài viết được lưu trữ dưới dạng file JSON.

5. **Phân Tích**:
   - Tiến hành phân tích tại folder `notebooks` để đưa ra các kết luận.

# Tác Giả

- Phần tích và phát triển: [Tên bạn].