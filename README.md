# Thư viện nhạc D-Bot

Thư viện MP3 cá nhân cho firmware D-Bot Music. Danh mục được đọc từ `index.json`; các tệp âm thanh nằm trong `songs/`.

## Thêm bài mới

1. Chép tệp MP3 vào `songs/` với tên ngắn, chỉ dùng chữ Latin, số và dấu gạch ngang.
2. Thêm một mục vào mảng trong `index.json`:

```json
{
  "category": "song",
  "id": "ma-bai-hat",
  "name": "Tên bài hát - Nghệ sĩ",
  "path": "songs/ma-bai-hat.mp3",
  "tags": ["nghệ sĩ", "thể loại"]
}
```

3. Lưu thay đổi lên nhánh `main`. Thiết bị đọc thư viện từ URL raw của repo.

Chỉ dùng MP3 trong thư viện hiện tại. WAV trong thư mục nguồn chưa được thêm vì firmware này đang giải mã luồng MP3.
