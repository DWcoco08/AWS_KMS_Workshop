---
title: "Tổng kết và dọn dẹp"
weight: 40
chapter: true
pre: "<b>4. </b>"
translationKey: "conclusion"
---

## Tổng kết kiến thức

Qua bài lab, bạn đã học cách:

- Tạo và sử dụng khóa KMS để mã hóa dữ liệu trong S3
- Tích hợp CloudTrail để giám sát hoạt động
- Quản lý khóa để duy trì bảo mật lâu dài

KMS giúp bảo vệ dữ liệu nhạy cảm, và kết hợp với S3/CloudTrail tạo nên một hệ thống bảo mật toàn diện. Nhớ kiểm tra chi phí (KMS tính phí theo yêu cầu sử dụng) và dọn dẹp tài nguyên sau lab.

## Tài liệu tham khảo

- [Tài liệu chính thức AWS KMS](https://docs.aws.amazon.com/kms/latest/developer-guide/overview.html)
- [Hướng dẫn CloudTrail](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-user-guide.html)
- [Tutorial S3 Encryption](https://docs.aws.amazon.com/AmazonS3/latest/userguide/UsingKMSEncryption.html)
- [AWS Skill Builder](https://skillbuilder.aws/) - Cho các bài lab thực hành thêm
- [AWS Documentation](https://docs.aws.amazon.com/) - Tài liệu đầy đủ các dịch vụ AWS

## Feedback

Nếu bạn có feedback về workshop:

- Tạo issue trên GitHub repository
- Đóng góp improvements via pull requests
- Chia sẻ kinh nghiệm với community

## Kết

Xong rồi. Workshop đầu tiên về AWS KMS.

Nói thật là ban đầu mình cũng không hiểu encryption với key management này nó làm gì. Cứ nghĩ đơn giản là mã hóa file thôi. Nhưng làm xong mới thấy nó phức tạp hơn nhiều - từ việc tạo key, phân quyền, rotate key, đến cả việc audit xem ai dùng key lúc nào.

Mấy cái học được:
- Encryption thực ra không khó như mình tưởng, AWS đã lo hết phần khó rồi
- KMS với S3 kết hợp khá mượt, chỉ cần tick vài cái là data được mã hóa
- CloudTrail này hay phết, biết được ai làm gì với key của mình
- Rotate key định kỳ quan trọng thật, chứ không phải cái gì cũng set rồi quên được

Còn nhiều thứ chưa rõ lắm, nhất là phần policy với IAM. Nhưng thôi, từ từ rồi sẽ quen. Ít nhất giờ biết cách bảo vệ data trên cloud rồi, không còn để trần như trước nữa.

---

Cảm ơn nếu bạn cũng theo dõi đến đây. Chúc may mắn với các lab tiếp theo!
