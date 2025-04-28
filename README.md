
# 📰 Fake News Detection Project

## Mô tả
Dự án này nhằm **phát hiện tin giả** (Fake News) bằng cách sử dụng **Machine Learning**.  
Dữ liệu đầu vào là nội dung các bài báo và hệ thống sẽ phân loại bài viết thành:
- **Fake News** (Tin giả)
- **Not a Fake News** (Tin thật)

## Các bước thực hiện

1. **Đọc dữ liệu**
   - File dữ liệu: `Fake.csv`, `True.csv`
2. **Tiền xử lý**
   - Làm sạch văn bản (xoá dấu câu, link, ký tự HTML, số,...).
   - Gán nhãn `0` cho tin giả và `1` cho tin thật.
3. **Xử lý dữ liệu**
   - Xáo trộn dữ liệu.
   - Chia tập huấn luyện và tập kiểm tra (train/test split).
4. **Vector hóa**
   - Sử dụng **TF-IDF Vectorizer** để biến văn bản thành các vector số.
5. **Huấn luyện mô hình**
   - Logistic Regression
   - Decision Tree
   - Gradient Boosting
   - Random Forest
6. **Đánh giá mô hình**
   - In ra **classification report** cho từng mô hình.
7. **Kiểm tra thủ công**
   - Người dùng nhập nội dung tin tức để kiểm tra.

## Yêu cầu hệ thống

- Python >= 3.7
- Các thư viện:
  ```bash
  pip install pandas numpy seaborn matplotlib scikit-learn
  ```

## Cách chạy chương trình

```bash
python fake_news.py
```

## Chức năng chính

- Tự động hóa pipeline từ tiền xử lý tới huấn luyện mô hình.
- So sánh kết quả nhiều thuật toán ML khác nhau.
- Cho phép nhập tin bất kỳ để dự đoán.

## File cấu trúc

```
fake_news.py        # File code chính
Fake.csv            # Dữ liệu tin giả
True.csv            # Dữ liệu tin thật
manual_testing.csv  # File kiểm tra bằng tay
README.md           # (Bạn đang đọc)
```

## Ghi chú

- Hiện tại trong file code bị **nhầm** khi đọc file: cả `df_fake` và `df_true` đều đọc từ `Fake.csv`.
  > Cần sửa lại `df_true = pd.read_csv("/content/True.csv")` để đúng dữ liệu.
