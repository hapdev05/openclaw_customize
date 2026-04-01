---
name: image-reader
description: >
  Đọc và phân tích hình ảnh do người dùng gửi. Sử dụng khi người dùng gửi ảnh kèm câu hỏi,
  yêu cầu mô tả ảnh, đọc text trong ảnh (OCR), phân tích screenshot, nhận diện lỗi từ ảnh,
  hoặc bất kỳ tác vụ nào liên quan đến hình ảnh. Hỗ trợ: ảnh chụp màn hình, ảnh lỗi app,
  ảnh giao dịch, ảnh QR code, ảnh chứa text, và ảnh thông thường.
---

# Image Reader Skill

Skill này cho phép bot đọc, phân tích và mô tả hình ảnh mà người dùng gửi qua chat.

## Khi nào sử dụng

- Người dùng gửi ảnh kèm câu hỏi (ví dụ: "ảnh này là lỗi gì?")
- Yêu cầu đọc text/chữ trong ảnh (OCR)
- Yêu cầu mô tả nội dung ảnh
- Gửi screenshot lỗi app để hỏi cách xử lý
- Gửi ảnh giao dịch, ví, QR code
- Bất kỳ tin nhắn nào có đính kèm hình ảnh

## Cách xử lý

### 1. Nhận diện hình ảnh
Khi nhận được tin nhắn có kèm hình ảnh:
- Phân tích nội dung hình ảnh bằng vision capability của model
- Nếu ảnh chứa text → đọc và trích xuất text (OCR)
- Nếu ảnh là screenshot lỗi → nhận diện lỗi và đề xuất giải pháp
- Nếu ảnh là giao dịch/ví → đọc thông tin liên quan

### 2. Mô tả và phân tích
- Mô tả ngắn gọn nội dung ảnh
- Trả lời câu hỏi của user dựa trên nội dung ảnh
- Nếu ảnh liên quan đến Interlink → kết hợp với skill `interlink-support` để trả lời

### 3. Kết hợp với các skill khác
- Nếu ảnh là screenshot lỗi Interlink app → dùng `interlink-support` skill để tra mã lỗi và hướng dẫn
- Nếu ảnh chứa thông tin token/ví → kết hợp với `whitepaper-data` nếu cần

## Quy tắc trả lời

1. **Mô tả chính xác**: Chỉ mô tả những gì nhìn thấy trong ảnh, không bịa thêm
2. **Ngôn ngữ**: Trả lời theo ngôn ngữ người dùng đang dùng
3. **Ngắn gọn**: Trả lời đúng trọng tâm, không lan man
4. **Bảo mật**: KHÔNG đọc to/lặp lại thông tin nhạy cảm (mật khẩu, private key, seed phrase) nếu thấy trong ảnh. Cảnh báo user che thông tin nhạy cảm
5. **Hỏi thêm nếu cần**: Nếu ảnh không rõ hoặc cần thêm context → hỏi user
6. **Không hỗ trợ**: Nội dung bạo lực, NSFW, hoặc vi phạm pháp luật → từ chối lịch sự

## Mẫu trả lời

### Khi user gửi ảnh lỗi app:
> Mình thấy trong ảnh bạn đang gặp lỗi [mô tả lỗi]. Đây là lỗi [mã lỗi nếu có].
> Cách xử lý: [hướng dẫn từ interlink-support skill nếu liên quan]

### Khi user gửi ảnh và hỏi "đây là gì?":
> Trong ảnh là [mô tả nội dung]. [Thông tin thêm nếu liên quan đến Interlink]

### Khi user gửi ảnh chứa text:
> Mình đọc được nội dung trong ảnh:
> "[nội dung text]"
> [Trả lời câu hỏi liên quan nếu có]

### Khi ảnh không rõ:
> Ảnh hơi mờ/không rõ. Bạn có thể gửi lại ảnh rõ hơn được không?
