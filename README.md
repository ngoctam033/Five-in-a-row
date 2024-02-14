# Five-in-a-row
Đây là một dự án đơn giản về trò chơi cờ Caro được xây dựng bằng Python sử dụng thư viện tkinter để tạo giao diện đồ họa. Dưới đây là một số thông tin và hướng dẫn để hiểu và chạy dự án này:

### Cài Đặt và Chạy Dự Án:
1. Đảm bảo bạn đã cài đặt Python trên máy tính của mình. Nếu chưa, bạn có thể tải Python từ [python.org](https://www.python.org/) và cài đặt theo hướng dẫn.
2. Sao chép toàn bộ mã từ file này và lưu vào một tập tin Python mới (vd: `caro_game.py`).
3. Mở Command Prompt hoặc Terminal và điều hướng đến thư mục chứa tập tin Python vừa tạo.
4. Chạy lệnh sau để khởi động trò chơi:

    ```
    python caro_game.py
    ```

### Hướng Dẫn Sử Dụng:
- Khi chạy chương trình, một cửa sổ mới sẽ xuất hiện hiển thị bàn cờ Caro.
- Bạn có thể nhấp chuột vào bất kỳ ô nào trên bàn cờ để đánh cờ.
- Cờ của bạn sẽ được đánh bằng ký hiệu "O", trong khi cờ của máy sẽ được đánh bằng ký hiệu "X".
- Trò chơi sẽ kết thúc khi có người chiến thắng hoặc bàn cờ đã được đánh hết. Kết quả sẽ được hiển thị trên cửa sổ.

### Cấu Trúc Dự Án:
- Mã nguồn này được chia thành một số phương thức và lớp để quản lý bàn cờ, hiển thị đồ họa và logic của trò chơi.
- Sử dụng thư viện `tkinter` để tạo giao diện người dùng và vẽ bàn cờ.
- Có một lớp `ChessboardApp` để quản lý toàn bộ trò chơi và các phương thức để xử lý sự kiện nhấp chuột và logic trò chơi.
- Điểm mạnh và yếu của mỗi nước đi được tính bằng thuật toán đánh giá điểm.
### Đoạn code này sử dụng một số thuật toán và kỹ thuật sau:

Thuật toán Minimax:

Thuật toán Minimax được sử dụng trong hàm best_move để đánh giá và chọn ra nước đi tốt nhất cho máy tính.
Thuật toán này đánh giá tất cả các nước đi có thể từ trạng thái hiện tại của bàn cờ và chọn ra nước đi tối ưu nhất dựa trên điểm số ước tính của trạng thái tương lai.

Alpha-Beta Pruning:

Mặc dù không được triển khai trực tiếp trong code, tuy nhiên, cách triển khai thuật toán Minimax trong best_move có thể được cải thiện bằng cách áp dụng Alpha-Beta Pruning để cắt bỏ các nhánh không cần thiết, từ đó cải thiện hiệu suất của thuật toán.

Heuristic Evaluation:

Hàm stupid_score được sử dụng để đánh giá tính hợp lý của mỗi nước đi từ góc độ của máy tính.
Thuật toán này đánh giá các nước đi bằng cách tính điểm dựa trên lợi thế của mỗi nước đi cho máy tính. Điểm số này được tính toán dựa trên số lượng quân cờ của máy tính và người chơi, cũng như các điểm số có thể dẫn đến chiến thắng trong tương lai.
Tìm kiếm trạng thái chiến thắng:

Hàm winning_situation được sử dụng để xác định các trạng thái có thể dẫn đến chiến thắng trong tương lai.
Thuật toán này đánh giá các trạng thái trên bàn cờ và xác định xem máy tính có thể chiến thắng trong tương lai dựa trên việc có được một dãy quân cờ liên tiếp nào đó.
Kiểm tra thắng/thua/hòa:

Hàm is_win được sử dụng để kiểm tra xem trò chơi đã kết thúc chưa và nếu đã kết thúc thì xác định kết quả (người chơi thắng, máy tính thắng hoặc hòa).
Thuật toán này kiểm tra trạng thái hiện tại của bàn cờ và xác định kết quả dựa trên việc có một người chơi hoặc máy tính chiến thắng hoặc bàn cờ đã đầy.

### Điều Chỉnh:
- Bạn có thể tinh chỉnh kích thước của bàn cờ bằng cách thay đổi giá trị của biến `ROWS_COLS` và `PIXEL` trong phương thức `__init__` của lớp `ChessboardApp`.
- Nếu bạn muốn cải thiện thuật toán AI hoặc thêm tính năng mới, bạn có thể chỉnh sửa các phương thức liên quan đến logic của trò chơi.

Đây là một dự án đơn giản để tìm hiểu về Python, giao diện người dùng và các thuật toán trò chơi. Chúc bạn có thời gian vui vẻ với trò chơi!
