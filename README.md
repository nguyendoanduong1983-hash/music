# Thư viện nhạc và truyện ma D-Bot

Thư viện MP3 cá nhân cho firmware D-Bot. Danh mục được đọc từ `index.json`; bài hát nằm trong `songs/`, còn truyện ma nằm trong `truyện ma/`. Các mục truyện ma vẫn dùng `category: "song"` để tương thích với bộ phát MP3 hiện tại và có thẻ `truyện ma` để robot tìm, đọc tên khi được hỏi.

## Thêm bài hát

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

## Thêm truyện ma

1. Chép tệp MP3 vào `truyện ma/`.
2. Thêm mục trong `index.json` với `category: "song"`, đường dẫn tương đối tới tệp và thẻ `truyện ma`.

Thiết bị đọc thư viện từ URL raw của repo. Chỉ dùng MP3; WAV chưa được thêm vì firmware hiện giải mã luồng MP3.
