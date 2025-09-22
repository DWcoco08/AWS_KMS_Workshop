# AWS KMS Workshop 🔐

[![Hugo](https://img.shields.io/badge/Hugo-0.150.0-blue.svg)](https://gohugo.io/)
[![AWS](https://img.shields.io/badge/AWS-KMS-orange.svg)](https://aws.amazon.com/kms/)

A comprehensive bilingual workshop (English/Vietnamese) for learning AWS Key Management Service (KMS) implementation and best practices.

## 📚 Workshop Overview

This workshop provides hands-on experience with AWS KMS, covering:

- Creating and managing KMS keys
- Encrypting data in Amazon S3
- Monitoring key usage with CloudTrail
- Managing access permissions through IAM

## ✨ Features

- **Bilingual Support**: Full content in English and Vietnamese
- **Interactive Labs**: Step-by-step practical exercises
- **Real-world Scenarios**: Industry-relevant use cases
- **Visual Learning**: Screenshots and diagrams for each step

## 🗂 Workshop Structure

### English Version (`/en/`)

1. **Introduction to AWS KMS** - Core concepts and benefits
2. **Lab Overview** - Workshop objectives and requirements
3. **Lab Walkthrough** - Hands-on implementation
   - 3.1 Create KMS Master Key
   - 3.2 Configure CloudTrail
   - 3.3 Upload and Encrypt in S3
   - 3.4 Access Encrypted Data
   - 3.5 Manage Permissions
4. **Summary and Cleanup** - Key takeaways and resource cleanup

### Vietnamese Version (`/vi/`)

Parallel content structure in Vietnamese for local learners.

## 🔧 Prerequisites

- AWS Account with appropriate permissions
- Basic understanding of cloud computing
- Familiarity with AWS Console

## 🚀 Local Development

### Requirements

- [Hugo Extended](https://gohugo.io/installation/) v0.150.0+
- Git

### Setup

```bash
# Clone the repository
git clone https://github.com/DWcoco08/AWS_KMS_Workshop.git
cd AWS_KMS_Workshop

# Install theme submodule
git submodule update --init --recursive

# Run local development server
hugo serve
```

Access the workshop at `http://localhost:1313/`

## 🏗️ Build

```bash
# Build static site
hugo

# Build with drafts
hugo -D
```

## 📁 Project Structure

```
AWS_KMS_Workshop/
├── content/
│   ├── en/          # English content
│   └── vi/          # Vietnamese content
├── layouts/         # Custom templates
├── static/          # Images and assets
├── themes/          # Hugo Learn theme
└── config.toml      # Site configuration
```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 👤 Author

**Đặng Nguyễn Đức Huy**

- LinkedIn: [Đặng Nguyễn Đức Huy](https://www.linkedin.com/in/dwuy-wiii-b72596370/)
- Email: dnduchuy08@gmail.com

## 🙏 Acknowledgments

- AWS Study Group community
- Hugo Learn theme contributors
- All workshop participants and contributors

---

🚀 Happy Learning!
