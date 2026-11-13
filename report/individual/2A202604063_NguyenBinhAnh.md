# Báo cáo cá nhân — NguyenBinhAnh-2A202604063

Đoạn video: MOT17-09, 150 frame (frame 1–150), nguồn MOTChallenge, giấy phép CC BY-NC-SA 3.0.

## 0. Thông tin học viên

- Họ tên: Nguyễn Bình Anh
- MSSV: 2A202604063
- Mã đề (A/B/C): B
- Email: binhybc0@gmail.com
- Link repository: https://github.com/binhybc0/K5-L2B-DAY05-Nguyen-Binh-Anh-2A202604063-MOTTracking
- Giờ bắt đầu: 19:00
- Giờ kết thúc: 23:35

## 1. Xem trước đoạn video (CP0)

Ghi **trước khi vẽ**, mỗi người một dòng.

| Mã | Frame xuất hiện | Frame cuối thấy được | Rẽ / dừng / đổi tốc độ ở frame | Bị che ở frame | Ghi chú |
|---|---|---|---|---|---|
| P1 | 0 | 149 | 65, 95, 115 | Không bị che | Phụ nữ mặc áo khoác xanh đậm, đi thẳng về phía camera |
| P2 | 0 | 139 | 35, 88, 125 | 107–123 | Phụ nữ áo xám đi cùng bé gái, bị P1 và P4 che khuất hoàn toàn ở đoạn giữa |
| P3 | 0 | 147 | 40, 105, 135 | 112–134 | Bé gái mặc váy hoa nắm tay P2, bị P1 và P4 đi ngang qua che khuất |
| P4 | 0 | 149 | 50, 82, 110 | 60–125 (che 1 phần) | Nam mặc áo polo xanh dương đi phía sau P1, đổi hướng nhẹ ở cuối đoạn |
| P5 | 0 | 136 | 25, 60, 105 | 120–127 | Nam mặc áo tối màu di chuyển sát mép trái, bị khuất tạm thời trước khi xuất hiện lại |

## 2. Keyframe và thời gian (CP1, CP4)

Số keyframe lấy từ kết quả `src/check_submission.py`.

| Mã | Số keyframe | Keyframe ở frame | Số frame có mặt | Keyframe / 100 frame | Thời gian (phút) | Chỗ khó |
|---|---|---|---|---|---|---|
| P1 | 63 | [0, 5, 8, 10, 20, 30, 40, 49, 59, 65, 66, 67, 68, 69, 72, 74, 75, 76, 77, 78, 79, 80, 81, 82, 83, 84, 85, 86, 87, 89, 90, 92, 93, 94, 95, 97, 98, 99, 100, 101, 102, 103, 108, 109, 110, 111, 112, 115, 116, 117, 118, 119, 121, 122, 124, 125, 126, 127, 133, 136, 139, 143, 149] | 150 | 42.0 | 35 | Tiến gần camera nên kích thước hộp thay đổi nhanh |
| P2 | 20 | [0, 10, 20, 30, 32, 35, 36, 41, 42, 88, 124, 125, 126, 128, 131, 132, 133, 137, 138, 139] | 123 | 16.3 | 20 | Bị che khuất hoàn toàn ở đoạn 107–123 và lộ lại ở frame 124 |
| P3 | 9 | [0, 10, 20, 30, 40, 105, 135, 141, 142] | 125 | 7.2 | 15 | Kích thước nhỏ, đi sát cạnh P2 và bị che khuất đoạn 112–134 |
| P4 | 38 | [0, 3, 5, 10, 20, 30, 40, 50, 60, 63, 64, 66, 71, 73, 76, 77, 78, 79, 82, 84, 86, 87, 91, 92, 94, 95, 96, 98, 99, 107, 109, 110, 111, 112, 117, 129, 139, 149] | 150 | 25.3 | 30 | Đi sau lưng P1 nên phải ước lượng khung hình qua đoạn bị che 1 phần |
| P5 | 97 | [0, 10, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 32, 33, 34, 35, 36, 37, 38, 39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 50, 51, 52, 54, 55, 56, 57, 58, 59, 60, 61, 62, 63, 64, 65, 66, 67, 68, 69, 70, 71, 72, 74, 75, 76, 77, 78, 82, 83, 84, 85, 86, 87, 88, 89, 90, 92, 93, 94, 95, 96, 97, 98, 101, 102, 103, 104, 105, 109, 111, 112, 113, 114, 115, 116, 117, 118, 119, 128, 129, 130, 131, 132, 135, 136] | 129 | 75.2 | 40 | Di chuyển sát mép ảnh, đổi góc nhìn và bị che khuất liên tục |
| **Tổng** | **227** | — | **677** | **33.5** | **140** | — |

Keyframe / 100 frame của cả bài = tổng keyframe ÷ tổng số frame có mặt × 100 = $227 \div 677 \times 100 = 33.5$.

Bạn đặt keyframe nhiều nhất ở người nào? Vì sao (người đó rẽ, dừng, lại gần camera hay bị che)?

Đặt keyframe nhiều nhất ở **P5 (Track 4)** với 97 keyframe (và P1 với 63 keyframe). Nguyên nhân là P5 di chuyển sát mép khung hình, liên tục thay đổi góc nghiêng cơ thể và bị che khuất phức tạp nên cần đặt keyframe dày hơn để giữ hộp bám sát, không bị trôi lệch khỏi đối tượng.

## 3. Đoạn bị che (CP2)

Người bị che: `P2`

| Mốc | Frame |
|---|---:|
| Bắt đầu bị che một phần (bật `occluded`) | 102 |
| Mất hẳn (bật `outside`) | 107 |
| Hiện lại (tắt `outside`) | 124 |
| Thấy rõ trở lại (tắt `occluded`) | 128 |

- Thời gian khuất hẳn: `17` frame (từ frame 107 đến 123) = `0.57` giây (với tốc độ 30 fps).
- Quyết định: **giữ cùng ID** (`PERSON 2`).
- Lý do (trả lời 3 câu: khuất bao lâu so với 60 frame, ngoại hình có khớp, chỗ hiện lại có đúng hướng và tốc độ):

Thời gian bị che khuất hoàn toàn chỉ kéo dài 17 frame (ngắn hơn rất nhiều so với ngưỡng 60 frame). Khi đối tượng xuất hiện trở lại tại frame 124, trang phục (áo khoác xám, quần tối màu) và vóc dáng khớp hoàn toàn với người trước khi bị che, đồng thời vị trí lộ diện nằm đúng trên quỹ đạo di chuyển và tốc độ bước đi ban đầu.

Ảnh chụp màn hình:

![Trước khi che](images/che_1_truoc.png)
![Giữa đoạn che, thấy cờ trên panel object](images/che_2_giua.png)
![Sau khi hiện lại, cùng ID](images/che_3_sau.png)

## 4. Tự review ID (CP3)

Lượt 1 theo người (đi ngược từ frame 149 về 0 trên CVAT), lượt 2 theo cảnh (nhảy 10 frame). Ít nhất 3 dòng; không có lỗi thì ghi một dòng "đã kiểm hai lượt, không lỗi".

Loại lỗi dùng đúng một trong 7 mã: `id_switch`, `fragmentation`, `lost`, `merge`, `false_track`, `drift`, `flag`.

| Frame | Mã người | Loại lỗi | Mô tả một câu | Phát hiện ở lượt | Đã sửa? |
|---:|---|---|---|---|---|
| 115 | P1 | `drift` | Cạnh dưới của hộp trôi lên cao làm cắt lẹm mất phần giày khi P1 tiến gần camera. | Lượt 1 | Đã sửa |
| 125 | P2, P3 | `false_track` | Đối tượng đã khuất hẳn sau lưng người khác nhưng quên bật `outside` khiến hộp đứng im đè lên người khác. | Lượt 2 | Đã sửa |
| 141 | P4 | `flag` | Đối tượng đã bước ra lộ rõ toàn thân nhưng vẫn bật cờ `occluded` (viền nét đứt) và cạnh trên hộp hở đầu. | Lượt 2 | Đã sửa |

Tổng hợp số lỗi theo loại:

| `id_switch` | `fragmentation` | `lost` | `merge` | `false_track` | `drift` | `flag` |
|---:|---:|---:|---:|---:|---:|---:|
| 0 | 0 | 0 | 0 | 1 | 1 | 1 |

Lỗi nào chỉ lượt 2 (theo cảnh) mới thấy, lượt 1 (theo người) không thấy? Vì sao?

Lỗi `false_track` (quên bật `outside` khiến hộp cũ đè lên người khác) và lỗi `flag` (quên tắt `occluded` khi hai người đã tách nhau ra) dễ phát hiện nhất ở **lượt 2 (theo cảnh)**. Vì khi nhìn toàn cảnh tất cả các hộp cùng lúc, ta dễ dàng đối chiếu tương quan vị trí giữa người che và người bị che để nhận ra hộp thừa hoặc sai trạng thái viền.

## 5. File xuất và kết quả tự kiểm (CP4)

| Kiểm tra | Kết quả |
|---|---|
| Tên file MOT 1.1 | `src/exports/NguyenBinhAnh_mot.zip` |
| Tên file CVAT for video 1.1 | `src/exports/NguyenBinhAnh_cvat_video.zip` |
| Số track ID khác nhau trong `gt/gt.txt` (phải là 5) | `5` |
| Frame `outside` không có dòng trong `gt.txt` (đúng / sai) | `đúng` |
| Job đã completed trên CVAT máy cá nhân | `đã completed` |

Dán phần tóm tắt in ra từ `src/check_submission.py`:

```text
Số frame in theo CVAT (bắt đầu từ 0). Trong gt.txt, frame_id = frame CVAT + 1.

=== File MOT 1.1: NguyenBinhAnh_mot.zip ===
  Số track ID: 5   |   Tổng số box: 677
  [OK]        Đúng 5 track ID.

  Track | Frame có mặt | Số frame | Đoạn vắng (outside)
      1 |   0–149      |      150 | -
      2 |   0–139      |      123 | 107–123
      3 |   0–147      |      125 | 112–134
      4 |   0–149      |      150 | -
      5 |   0–136      |      129 | 120–127


=== File CVAT for video 1.1: NguyenBinhAnh_cvat_video.zip ===

  Track | Nhãn   | Frame thấy | Keyframe | KF/100 frame | Frame occluded | Lần bật outside
      0 | person |        150 |       63 |         42.0 |              0 |               0
      1 | person |        123 |       20 |         16.3 |             35 |               2
      2 | person |        125 |        9 |          7.2 |             19 |               2
      3 | person |        150 |       38 |         25.3 |             66 |               0
      4 | person |        129 |       97 |         75.2 |             57 |               2
  [CẢNH BÁO]  Track 4: 75 keyframe / 100 frame > 50. Quá dày, dồn keyframe vào chỗ rẽ / dừng / bị che.

  Tổng: 227 keyframe / 677 frame có mặt = 33.5 keyframe / 100 frame
  [OK]        Đọc được 5 track từ annotations.xml.

=== Tóm tắt ===
  Lỗi: 0   |   Cảnh báo: 1
  Không có lỗi định dạng. Mở CVAT xem lại từng [CẢNH BÁO]; cảnh báo đúng ý bạn thì ghi lý do vào báo cáo.
```

> **Giải thích cảnh báo Track 4:** Đối tượng P5 (Track 4) di chuyển sát mép khung hình, liên tục thay đổi góc nhìn và bị che khuất phức tạp nên đã chủ động đặt mật độ keyframe dày hơn ở đoạn chuyển động khó để đảm bảo hộp bám sát toàn thân, tránh trôi lệch.

## 6. Ba câu kết

1. Nếu được gán lại, bạn sẽ đặt keyframe khác ở đâu? Vì sao?

   Ở Track 4 (P5), tôi sẽ giảm bớt số lượng keyframe đặt liên tiếp từng frame ở đoạn từ frame 20 đến 78, chỉ giữ lại các mốc cách nhau 10 frame và các điểm đổi hướng chính. Điều này giúp tận dụng tốt tính năng nội suy tuyến tính của CVAT, làm hộp di chuyển mượt mà hơn và tránh hiện tượng rung giật nhẹ.

2. Có chỗ nào bạn không chắc "cùng ID hay ID mới"? Bạn đã quyết định và ghi chú thế nào?

   Tại đoạn P2 và P3 bị P1 và P4 đi ngang qua che khuất hoàn toàn (khoảng frame 107–134), ban đầu dễ phân vân liệu có nên tạo ID mới khi lộ ra hay không. Tuy nhiên do thời gian khuất ngắn (dưới 30 frame), trang phục và hướng bước đi hoàn toàn khớp với quỹ đạo cũ nên tôi quyết định giữ nguyên ID cũ, sử dụng cờ `outside` trong lúc khuất hẳn và ghi chú rõ vào Mục 3.

3. Một lỗi ID trong job của bạn (nếu không còn sót, chọn lỗi đã sửa) có thể làm xe tự lái dự đoán sai chuyển động của người đó như thế nào? Lỗi đó ảnh hưởng MOTA hay IDF1 nhiều hơn?

   Nếu xảy ra lỗi nhảy ID (`id_switch`) hoặc để sót hộp đứng yên (`false_track`) lúc hai người cắt ngang nhau, hệ thống dự đoán quỹ đạo của xe tự lái sẽ tính sai vận tốc và hướng di chuyển của người đi bộ (tưởng người đó dừng đột ngột hoặc đổi hướng lao ra đường), dẫn đến phanh gấp nhầm hoặc đánh lái nguy hiểm. Lỗi `id_switch` làm giảm mạnh chỉ số **IDF1** hơn vì chỉ số này đo lường trực tiếp khả năng duy trì nhất quán danh tính của đối tượng xuyên suốt chuỗi thời gian.

## 7. Tài liệu tham khảo và công cụ AI đã dùng

- Tài liệu hướng dẫn thực hành Lab MOT Tracking (K5-L2-DAY05) và bộ dữ liệu chuẩn MOTChallenge (MOT17-09).
- Công cụ CVAT (Computer Vision Annotation Tool) và script kiểm tra `src/check_submission.py`.
- Công cụ AI (Gemini) hỗ trợ giải đáp quy tắc gán nhãn (`occluded`, `outside`), rà soát lỗi bounding box trên video và tổng hợp định dạng báo cáo.