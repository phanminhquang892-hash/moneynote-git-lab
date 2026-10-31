# Trả lời bài tập Git

## Câu 1

Main ban đầu có 15 commit. Bốn nhánh còn lại là `feature/giao-dien-moi`, `feature/tieu-de`, `feature/xuat-csv` và `hotfix/sua-loi-cong`.

## Câu 2

Lan có 7 commit trong repo ban đầu. Dùng `git log --all --author="Lan" --oneline` để xem cả những commit trên nhánh khác.

## Câu 3

Dòng `reduce` do Lê Hùng sửa ở commit `df17ab7` – Thêm bộ lọc thu/chi. Kết quả xem bằng `git blame js/tinh-toan.js` trước khi sửa bài.

## Câu 4

`git diff` xem phần sửa chưa add, còn `git diff --staged` xem phần đã add so với commit hiện tại. Không đưa `.env` lên Git vì file này có thể chứa mật khẩu hoặc khóa API.

## Câu 5

Bước 3.1 là fast-forward vì main chưa có commit mới sau khi tạo nhánh giới thiệu. Bước 3.2 thì main và nhánh giao diện đều có commit riêng nên Git tạo merge commit để gộp hai bên.

## Câu 6

Nhánh giao diện không sửa trùng vùng với thay đổi trên main nên không xung đột. Sau khi gộp giao diện, nhánh tiêu đề cũng sửa dòng h1 thành nội dung khác nên Git không tự chọn được.

## Câu 7

Revert tạo commit mới đảo thay đổi và giữ lịch sử cũ. Reset lùi nhánh về commit trước, dễ làm lịch sử khác với máy của những bạn đã pull về nên không phù hợp để gỡ commit trên nhánh chung.

## Câu 8

- Soft: giữ nguyên thay đổi trong vùng chờ và các file.
- Mixed: bỏ phần đã stage nhưng vẫn giữ nội dung sửa trong file.
- Hard: đặt lại cả vùng chờ và các file được Git theo dõi về commit đã chọn, có thể mất phần chưa commit.

## Câu 9

Commit gây lỗi là `df17ab7` – Thêm bộ lọc thu/chi, tác giả Lê Hùng.

Trong commit đó, reduce khởi tạo bằng chuỗi rỗng `''` nên dấu cộng nối chuỗi tiền. Hai khoản 100000 và 50000 thành `"10000050000"`. Dùng số `0` làm giá trị ban đầu thì cộng đúng.

## Câu 10

Merge cả nhánh hotfix sẽ lấy luôn phần thử font Comic Sans chưa được duyệt. Cherry-pick chỉ lấy commit sửa lỗi được chọn.

## Câu 11

Commit Thêm hàm xuất CSV đổi từ `6650471` sang `8656665` sau rebase. Do commit có cha mới nên mã cũng thay đổi. Không nên rebase nhánh mà bạn khác đã kéo về vì họ vẫn giữ lịch sử cũ và sẽ khó đồng bộ.

## Câu 12

Fetch tải thay đổi từ GitHub về nhưng chưa gộp vào nhánh đang làm. Pull tải về rồi gộp bằng merge hoặc rebase tùy cấu hình, nên có thể gặp xung đột.
