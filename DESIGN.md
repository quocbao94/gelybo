# Gelybo — Thiết kế đã chốt

Đây là nguồn sự thật của dự án. Mọi AI (Claude, GPT, Gemini) và mọi lần sửa phải bám theo file này. Thay đổi thiết kế thì sửa file này trước.

## 1. Tổng quan

- Thể loại: nuôi thú cozy, khám phá nhẹ nhàng. Web trước, mobile sau.
- Lộ trình: game nuôi Gelybo trên Moonbell Observatory, sau đó mở rộng sang **Gelybo English Run** (game chạy học tiếng Anh, Gelybo lăn qua cổng đáp án).
- Mục đích: học tập, phi thương mại.

## 2. Nhân vật Gelybo

### Hình dáng (lấy đường kính thân D làm chuẩn)

| Phần | Thông số |
|---|---|
| Thân | Quả cầu gel trong suốt, đường kính **D** |
| Lõi | Đường kính **0,40D**, tâm thấp hơn tâm quả cầu **0,08D**, luôn đứng thẳng, không lăn theo thân |
| Đầu | Viên sỏi dẹt, rộng **0,78D**, cao **0,34D**, sâu **0,46D**, hai đầu bo tròn, mặt trên và dưới hơi phẳng |
| Khe hở | **0,14D** giữa đỉnh thân và đáy đầu |
| Liên kết từ tính | **Một vòng elip mảnh** nằm ngang và **hai chấm sáng** (một trên, một dưới, bập bềnh nhẹ). Không có cổ vật lý, không thêm vòng |
| Miệng, má hồng | Không có |

Trong code hiện tại: `BR = 0.68` (bán kính thân), `GAP = 0.19`, `HH = 0.23` (nửa bề cao đầu).

### Mắt

Vệt sáng nằm ngay dưới bề mặt đầu: lõi trắng, viền ánh theo màu lõi, quầng tối rất mờ ban ngày để dễ đọc. Ảnh gốc là hai vệt cong mảnh, nằm cao, gần mặt trước của đầu.

| Trạng thái | Hình mắt |
|---|---|
| Bình thường | Hai hạt bầu dục dọc, chớp bằng cách tắt dịu |
| Vui | Vòng cung ^ ^ |
| Buồn ngủ | Vòng cung ‿ ‿, sáng mờ theo nhịp thở |
| Mơ màng | Vệt ngang nửa mở |
| Nháy mắt | Một bầu dục, một ^ |
| Bị chọc | > < |
| Phấn khích | Ngôi sao (lõi Sao) hoặc trái tim (lõi Tim) |

### Chất liệu

Gel pha lê trong suốt có khúc xạ thật, ánh cầu vồng nhẹ, viền sáng ở mép. Lõi hắt màu vào thân, bloom toả quầng.

### Chuyển động

- **Lăn** để di chuyển, có vật lý: trôi theo dốc, đung đưa trong hố lõm, va chạm với vật thể.
- **Đầu bám thân bằng lò xo**: luôn đứng thẳng khi thân lăn, trễ nhịp khi tăng giảm tốc, nhún xuống khi thân nảy.
- Đầu hướng mặt theo chiều lăn; đứng yên một lúc thì quay về phía người chơi.
- Chạm đầu: đầu bật lên, mắt đổi sang biểu cảm bị chọc. Chạm thân: thân rung như thạch.
- Rảnh thì tự lăn đi thăm các khu trên đảo.

### Đã thử và loại bỏ (đừng lặp lại)

- Thân hạt đậu có tay chân: nhìn giống slime.
- Nhân vật đầu nấm có tay chân, dựng bằng Blender và gắn khung xương: khó làm, thiếu hồn.
- Lõi dựng bằng đốm sáng kiểu khắc laser: rối mắt.
- Chòm sao bên trong bụng: không ổn.
- Mắt chấm đen: không hợp chất gel.

## 3. Lõi ngũ hành (14 lõi)

Lõi nằm trong bụng, đổi màu ánh sáng của thân và tính cách của Gelybo. Chỉ để trang trí và sưu tầm, không tăng chỉ số.

| Hệ | Lõi | Tính cách |
|---|---|---|
| Kim (trắng bạc, sáng dịu hơn các hệ khác) | Sao, Đồng xu lỗ vuông, Chuông | Hớn hở nhảy; ngửa đầu tự tin; đầu đung đưa |
| Mộc (xanh lá) | Lá, Nấm | Ngó nghiêng; lắc lư |
| Thủy (xanh dương) | Trăng, Mây, Giọt nước | Buồn ngủ; lơ lửng; nhún tung tăng |
| Hỏa (đỏ cam) | Lửa, Tim, Lồng đèn Trung thu | Hăng hái; e thẹn; thỉnh thoảng xoay đầu một vòng |
| Thổ (vàng đất) | Hổ phách, Hũ gốm, Núi | Điềm tĩnh; lắc lư; vững chãi |

## 4. Phụ kiện hoàng đạo (12)

Chất liệu **gel ngân hà**: trong suốt, viền sáng, tinh vân trôi và sao lấp lánh bên trong, tự phát sáng. Gắn trên đầu, độc lập với hệ ngũ hành.

Bạch Dương: sừng cừu xoăn · Kim Ngưu: sừng bò cài hoa · Song Tử: ăng-ten sao đôi · Cự Giải: càng cua · Sư Tử: bờm · Xử Nữ: vòng hoa · Thiên Bình: cân vàng mini · Bọ Cạp: đuôi cong · Nhân Mã: bờm ngựa · Ma Kết: sừng dê và râu · Bảo Bình: bình nước rót · Song Ngư: hai chú cá bơi quanh

Lưu ý: phụ kiện đang được thu nhỏ theo đầu viên sỏi, một số món cần chỉnh lại vị trí.

## 5. Thế giới: Moonbell Observatory

Đảo mặt trăng lơ lửng giữa trời sao và cực quang. Đá trăng tím nhạt nhiều hố, đường lát kem viền vàng gắn sao phát sáng, điểm nhấn vàng ấm. Môi trường không được lấn át Gelybo.

### Đảo trung tâm (đã dựng thô)

| Khu | Vị trí | Vai trò |
|---|---|---|
| Quả cầu thiên văn | Giữa | Biểu tượng của đảo, sau này dùng chọn và mở khoá các cung |
| Đường vòng | Quanh trung tâm | Trục di chuyển chính, năm nhánh toả ra |
| Nhà mái vòm | Tây bắc | Nhà của Gelybo, mái đục sao phát sáng |
| Vườn chuông | Tây nam | Hai vòm, sáu chuông reo khi đầu Gelybo lăn qua |
| Hố lăn | Đông bắc | Ba hố lõm có trọng lực, lăn đung đưa |
| Hang sao | Đông nam | Hang tối, pha lê sáng lên theo lõi khi Gelybo lại gần |
| Bục phía bắc | Bắc | Cổng sang 12 mặt trăng hoàng đạo (chưa làm) |

### 12 mặt trăng hoàng đạo (chưa làm)

Mỗi cung một mặt trăng nhỏ xếp vòng quanh đảo trung tâm, nối bằng ray vàng, có biểu tượng riêng. Hoàn thành một mặt trăng thì nhận phụ kiện của cung đó.

Hướng đề xuất để tránh đơn điệu: chia 12 cung theo 4 nguyên tố hoàng đạo (Lửa, Đất, Khí, Nước), mỗi nhóm một bảng màu và chất liệu riêng; tượng biểu tượng đơn giản hoá thành hình khối.

Câu hỏi còn mở: lõi ngũ hành xuất hiện thế nào trong thế giới này (ví dụ nhặt rải rác trên các mặt trăng).

## 6. Kỹ thuật

- Một file `index.html`, three.js **r147** (bản cuối còn nạp kiểu script UMD), không cần build.
- Thân và đầu gel: `MeshPhysicalMaterial` có transmission. Phụ kiện gel ngân hà và vũng sáng dưới chân: shader GLSL tự viết.
- Bloom: `EffectComposer` + `UnrealBloomPass`, có nút HD/Nhẹ cho máy yếu.
- Nhân vật dựng hoàn toàn bằng code (quả cầu + viên sỏi), không dùng file mô hình, không cần khung xương.
- Chạy được trên điện thoại (cảm ứng, safe area) và máy tính (chuột, khay tự xuống dòng).

## 7. Quy ước làm việc

- Sửa thiết kế: cập nhật DESIGN.md trước, rồi mới sửa code.
- Mỗi lần sửa một commit, mô tả rõ đã đổi gì.
- Ảnh concept mới bỏ vào `concepts/`, đặt tên có số thứ tự và nội dung, ví dụ `05-moonbell-hub-map.png`.
