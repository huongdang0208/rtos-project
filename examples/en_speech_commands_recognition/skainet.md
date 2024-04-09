# Một vài hàm trong skainet
## esp_srmodel_filter function
    hàm sử dụng để lọc và chọn model nhận dạng giọng nói Tiếng Anh, thực chất đây là một tập hợp dữ liệu và thuật toán AI được training để nhận biết và xử lí các command
    Kết quả trả về là một con trỏ đến tên của mô hình nhận dạng voice được chọn sau đó nó được dùng để tạo và quản lí model trong quá trình nhận dạng

# Struct
## esp_mn_iface_t
    dạng dữ liệu này chứa các hàm con trỏ, mỗi hàm thực hiện một chức năng cụ thể liên quan đến mô hình nhận dạng giọng nói
    đây là một đại diện cho mô hình Multinet, giao diện này cung cấp các hàm để tạo, nhận dạng và quản lí mô hình nhận dạng giọng nói
    nó cung cấp một số hàm như sau
    - `create`: tạo dữ liệu mô hình mới từ tên mô hình và tần số lấy mẫu
    - `get_samp_chunksize`: lấy kích thước khối mẫu âm thanh dùng cho nhận dạng
    - `detect`: nhận dạng dữ liệu giọng nói
    - `get_results`: nhận kết quả nhận dạng giọng nói sau khhi lấy thành công
    - `print_active_speech_commands`: in ra các lệnh giọng nói đang hoạt động
    -  `commands_update_from_sdkconfig`: cập nhật lệnh giọng nói từ cấu hình SDK ( Software Development Kit)