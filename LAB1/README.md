# Thuật toán Tìm kiếm Đồ thị (Graph Search Algorithms)

### Giới thiệu

Thuật toán tìm kiếm đồ thị là những phương pháp quan trọng trong khoa học máy tính và toán học rời rạc, được sử dụng để khám phá các nút và cạnh của một đồ thị. Chúng có ứng dụng rộng rãi trong nhiều lĩnh vực như tìm đường đi ngắn nhất, phân tích mạng, trí tuệ nhân tạo, và tối ưu hóa.

### Nội dung

Kho lưu trữ này bao gồm các chủ đề chính sau:

#### Khái niệm cơ bản

* **Đồ thị (Graph)**: Tập hợp các đỉnh (nodes/vertices) và các cạnh (edges) nối các đỉnh.
* **Đỉnh (Vertex/Node)**: Một thực thể trong đồ thị.
* **Cạnh (Edge)**: Một kết nối giữa hai đỉnh.
* **Đồ thị có trọng số (Weighted Graph)**: Các cạnh có gán một giá trị (trọng số).
* **Đồ thị không trọng số (Unweighted Graph)**: Các cạnh không có trọng số.
* **Đường đi (Path)**: Một chuỗi các đỉnh được nối bởi các cạnh.

#### Thuật toán Breadth-First Search (BFS)

* **Nguyên lý hoạt động**: Duyệt đồ thị theo từng lớp (level by level), bắt đầu từ nút gốc và khám phá tất cả các nút kề trước khi chuyển sang các nút ở lớp tiếp theo.
* **Cấu trúc dữ liệu chính**: Hàng đợi (Queue).
* **Ứng dụng**:
    * Tìm đường đi ngắn nhất trong đồ thị không trọng số.
    * Tìm kiếm tất cả các nút trong cùng một "lớp" (khoảng cách) từ nút gốc.
    * Kiểm tra tính liên thông của đồ thị.
    * Tô màu đồ thị hai phía (bipartite graph).
* **Ví dụ**:
    * Đồ thị mẫu 1 (không trọng số) và đường đi BFS từ S đến G.
    * Đồ thị mẫu 5 (có trọng số) và đường đi BFS có trọng số từ S đến G.

#### Thuật toán Depth-First Search (DFS)

* **Nguyên lý hoạt động**: Duyệt đồ thị theo chiều sâu, khám phá càng xa càng tốt dọc theo mỗi nhánh trước khi quay lui (backtrack).
* **Cấu trúc dữ liệu chính**: Ngăn xếp (Stack) hoặc đệ quy.
* **Ứng dụng**:
    * Tìm kiếm tất cả các đường đi giữa hai nút.
    * Tìm kiếm chu trình trong đồ thị.
    * Kiểm tra tính liên thông mạnh (strongly connected components).
    * Sắp xếp tô-pô (topological sorting).
* **Ví dụ**:
    * Đồ thị mẫu 1 (không trọng số) và đường đi DFS từ S đến G.
    * Đồ thị mẫu 5 (có trọng số) và đường đi DFS có trọng số từ S đến G.

#### So sánh hiệu suất (trên các đồ thị lớn)

* **BFS**: Thường nhanh hơn và hiệu quả hơn để tìm đường đi ngắn nhất trong đồ thị không trọng số hoặc khi cần khám phá theo từng lớp. Độ phức tạp thời gian thường là $O(V + E)$ (V: số đỉnh, E: số cạnh). Khi được mở rộng để xử lý đồ thị có trọng số (ví dụ: như thuật toán Dijkstra), nó vẫn là một trong những lựa chọn tốt nhất để tìm đường đi ngắn nhất.
* **DFS**: Thường được sử dụng khi cần duyệt toàn bộ nhánh hoặc tìm kiếm theo chiều sâu. Độ phức tạp thời gian cũng là $O(V + E)$. Khi dùng để tìm đường đi ngắn nhất trong đồ thị có trọng số, DFS cần duyệt nhiều đường đi hơn và có thể chậm hơn nhiều so với BFS (hoặc Dijkstra), đặc biệt nếu nó phải tìm tất cả các đường đi để xác định đường ngắn nhất.

#### Các ví dụ minh họa

* Đồ thị mẫu 1 (không trọng số) và đường đi BFS/DFS từ S đến G.
* Đồ thị mẫu 5 (có trọng số) và đường đi BFS/DFS có trọng số từ S đến G.
* Đồ thị mẫu 6 (có trọng số) và đường đi BFS/DFS từ S đến H.
* Đồ thị mẫu 7 (không trọng số) và đường đi BFS/DFS từ S đến H.