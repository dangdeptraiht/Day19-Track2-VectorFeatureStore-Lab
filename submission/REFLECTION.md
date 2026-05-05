# Reflection — Lab 19

**Tên:** _<Họ Tên>_
**Cohort:** _<A20-K1 / A20-K2 / ...>_
**Path đã chạy:** _<lite | docker | both>_

---

## Câu hỏi (≤ 200 chữ)

> Trên golden set 50 queries, mode nào thắng ở loại query nào (`exact` /
> `paraphrase` / `mixed`), và tại sao? Khi nào bạn **không** dùng hybrid
> (i.e. khi nào pure BM25 hoặc pure vector là lựa chọn đúng)?

- **Exact queries**: Keyword (BM25) mode thắng hoặc ngang bằng, vì nó bắt chính xác các từ khóa kỹ thuật/verbatim.
- **Paraphrase queries**: Semantic (Vector) mode mạnh hơn do khả năng hiểu ngữ nghĩa đồng nghĩa, vượt qua rào cản khác biệt từ vựng.
- **Mixed queries**: Hybrid mode thắng áp đảo nhờ kết hợp được cả tín hiệu từ khóa và ngữ nghĩa bằng RRF.

**Khi không dùng hybrid**:
- Dùng pure BM25 khi cần tra cứu chính xác mã ID, log error, tên riêng (cần exact match, tiết kiệm compute).
- Dùng pure Vector khi tìm kiếm cross-lingual (ngôn ngữ chéo) hoặc thuần tuý semantic similarity nơi keyword overlap bằng 0.

---

## Điều ngạc nhiên nhất khi làm lab này

_(Optional, 1–2 câu)_

---

## Bonus challenge

- [ ] Đã làm bonus (xem `bonus/`)
- [ ] Pair work với: _<tên đồng đội nếu có>_
