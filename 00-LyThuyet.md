# Lý thuyết - Toán rời rạc

## Các nguyên lý đếm cơ bản

### Nguyên lý cộng

- Áp dụng khi các phần từ của các tập hợp không giao nhau (không có phần tử chung).

- Nếu tập hợp \(S\) được chia thành \(n\) tập con \(S_1, S_2, \ldots, S_n\) sao cho \(S_i \cap S_j = \emptyset\) với \(i \neq j\), thì số phần tử của \(S\) là tổng số phần tử của các tập con:
  \[
  |S| = |S_1| + |S_2| + \ldots + |S_n|
  \]

### Nguyên lý nhân

- Áp dụng khi một nhiêm vụ có nhiều lựa chọn liên tiếp nhau. Các lựa chọn phải độc lập với nhau.

- Định lý 1: Nếu tập \(S\) gồm \(m\) tập hợp con và mỗi tập hợp con đều có \(n\) phần từ thì số phần tử của \(S\) là:
  \[
  |S| = m \times n
  \]

- Định lý 2: Nếu một nhiệm vụ có \(k\) bước và mỗi bước có \(n_i\) lựa chọn thì số cách thực hiện nhiệm vụ là:
  \[
  |S| = n_1 \times n_2 \times \ldots \times n_k
  \]

### Nguyên lý đếm lặp

- Sử dụng khi các phương pháp đếm tự nhiên dẫn đến việc mỗi phần tử bị đếm lặp lại một số lần nhất định.

- Nếu mỗi phần tử của tập \(S\) bị đếm lặp lại \(r\) lần trong quá trình đếm, thì số phần tử thực sự của \(S\) là:
  \[
  |S| = \frac{\text{Tổng số lần đếm}}{r}
  \]

## Hàm

- Một hàm số \(f\) từ tập \(A\) đến tập \(B\) là một quy tắc gán cho mỗi phần tử \(a\) trong tập \(A\) một phần tử duy nhất \(b\) trong tập \(B\).

- Ký hiệu: \(f: A \to B\).

- Tập hợp tất cả các hàm số từ \(A\) đến \(B\) được ký hiệu là \(B^A\).

- Đêm số lượng hàm số: 

    - Giả sử tập \(A\) có \(k\) phần tử và tập \(B\) có \(n\) phần tử, thì số lượng hàm số từ \(A\) đến \(B\) là:
      \[
      |B^A| = n^k
      \]

- Đơn ánh: 
## Hoán vị và Giai thừa

### Hoán vị
- Một hoán vị hữu hạn của tập hợp \(S\) là một cách sắp xếp lại các phần tử của \(S\) theo một thứ tự cụ thể.

- Số hoán vị của \(n\) phần tử là \(n!\) (giai thừa của \(n\)), được tính bằng công thức:
  \[
  n! = n \times (n-1) \times (n-2) \times \ldots \times 1
  \]
  với \(0! = 1\).

Ví dụ: Số hoán vị của 3 phần tử \(A, B, C\) là \(3! = 3.2.1 = 6\), bao gồm các hoán vị: \(ABC, ACB, BAC, BCA, CAB, CBA\).

### Hoán vị của tập hợp con

- Khi chúng ta không sắp xếp toàn bộ tập hợp mà chỉ chọn sắp xếp một nhóm gồm \(k\) phần tử từ một tập hợp \(n\) phần tử, số hoán vị của nhóm này được tính bằng công thức:
  \[
  P(n, k) = \frac{n!}{(n-k)!}
  \]
  trong đó \(P(n, k)\) là số hoán vị của \(k\) phần tử được chọn từ \(n\) phần tử.

- Ví dụ: Nếu có 10 người, muốn chọn ra một ban điều hành gồm Chủ tịch, Phó chủ tịch và Thư ký, thì số cách chọn là:
  \[
  P(10, 3) = \frac{10!}{(10-3)!} = \frac{10!}{7!} = 10 \times 9 \times 8 = 720
  \]

### Tổ hợp

- Khác với hoán vị, tổ hợp là cách chọn ra một nhóm phần tử mà không quan tâm đến thứ tự. Số tổ hợp của \(k\) phần tử được chọn từ \(n\) phần tử được tính bằng công thức:

\[
C(n, k) = \frac{n!}{k!(n-k)!}
\]
- Ví dụ: Nếu có 10 người, muốn chọn ra một nhóm 3 người để tham gia một cuộc thi, thì số cách chọn là:
\[
C(10, 3) = \frac{10!}{3!(10-3)!} = \frac{10!}{3!7!} = \frac{10 \times 9 \times 8}{3 \times 2 \times 1} = 120
\]

- Tính chất đối xứng: \(C(n, k) = C(n, n-k)\), nghĩa là số cách chọn \(k\) phần tử từ \(n\) phần tử bằng số cách chọn \(n-k\) phần tử từ \(n\) phần tử.

### Nguyên lý bù trừ

- Đôi khi việc đếm trực tiếp số phần tử của một tập hợp có thể khó khăn, nhưng việc đếm phần tử của tập hợp bù trừ (tập hợp các phần tử không thuộc tập cần đếm) lại dễ dàng hơn. Trong trường hợp này, ta có thể sử dụng nguyên lý bù trừ để tính số phần tử của tập cần đếm bằng cách lấy tổng số phần tử của tập lớn trừ đi số phần tử của tập bù trừ.

## Bài toán chia kẹo

- Để chia \(k\) viên kẹo giống nhau cho \(n\) đứa trẻ khác nhau, ta biểu diễn \(k\) viên kẹo bằng các dấu (*) và sử dụng \(n-1\) dấu phân cách (|) để chia các viên kẹo thành \(n\) phần. Số cách chia này được tính bằng công thức:
  \[
  C(k+n-1, n-1) = \frac{(k+n-1)!}{k!(n-1)!}
  \]

hoặc có thể viết lại là:
  \[
  C(k+n-1, k) = \frac{(k+n-1)!}{k!(n-1)!}
  \]

## Hệ số nhị thức và Tam giác Pascal

- Hệ số nhị thức \(C(n, k)\) xuất hiện trong khai triển nhị thức \((x + y)^n\) theo công thức:
  \[
  (x + y)^n = \sum_{k=0}^{n} C(n, k) x^{n-k} y^k
  \]