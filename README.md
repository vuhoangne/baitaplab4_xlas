# Bài tập Lab 4 - Xử lý ảnh số

## Mô tả
Bài tập thực hành xử lý ảnh với OpenCV và Python, bao gồm các kỹ thuật biến đổi hình học và phân đoạn ảnh.

## Cấu trúc dự án
```
XLA_lab4/
├── README.md
├── baitaplab4.ipynb    # Notebook chính với 4 bài tập
├── exercise/                 # Thư mục chứa ảnh đầu vào
│   └── dalat.jpg
└── output/                   # Ảnh kết quả
    ├── lang_biang.jpg
    ├── ho_xuan_huong.jpg
    └── quan_truong_lam_vien.jpg
```

## Bài tập

### Bài 1: Vùng ảnh LangBiang
- Chọn vùng LangBiang từ ảnh Đà Lạt
- Tịnh tiến sang phải 100px
- Áp dụng Otsu thresholding với ngưỡng 0.3
- **Output**: `lang_biang.jpg`

### Bài 2: Vùng ảnh Hồ Xuân Hương
- Chọn vùng Hồ Xuân Hương
- Xoay 45 độ
- Áp dụng Adaptive Thresholding (C=60)
- **Output**: `ho_xuan_huong.jpg`

### Bài 3: Vùng ảnh Quảng Trường Lâm Viên
- Chọn vùng Quảng Trường Lâm Viên
- Coordinate Mapping (biến đổi affine)
- Binary Closing (morphological operation)
- **Output**: `quan_truong_lam_vien.jpg`

### Bài 4: Menu xử lý ảnh tương tác
Menu với 2 nhóm chức năng:

**Geometric Transformation:**
1. Coordinate Mapping
2. Rotate (45°)
3. Scale (1.2x)
4. Shift (50,30)

**Segmentation:**
5. Adaptive Thresholding
6. Binary Dilation
7. Binary Erosion
8. Otsu

**Tính năng đặc biệt:**
- Chọn 1 chức năng đơn lẻ
- Kết hợp 2 chức năng (geometric + segmentation)

## Cài đặt

### Yêu cầu
```bash
pip install opencv-python numpy matplotlib
```

### Chạy chương trình
1. Mở Jupyter Notebook:
```bash
jupyter notebook baitaplab4.ipynb
```

2. Chạy từng cell theo thứ tự

3. Với bài 4, chạy cell cuối để khởi động menu tương tác

## Sử dụng Menu (Bài 4)
1. Nhập số 1-8 để chọn chức năng đơn lẻ
2. Nhập số 9 để kết hợp 2 chức năng:
   - Chọn geometric transformation (1-4)
   - Chọn segmentation (5-8)
3. Nhập 0 để thoát

## Kỹ thuật sử dụng
- **OpenCV**: Xử lý ảnh cơ bản
- **Geometric Transformation**: Affine, rotation, scaling, translation
- **Thresholding**: Otsu, Adaptive
- **Morphological Operations**: Dilation, Erosion, Closing
- **Matplotlib**: Hiển thị kết quả

## Tác giả
Lê Nguyễn Vũ Hoàng - 2174802010606
