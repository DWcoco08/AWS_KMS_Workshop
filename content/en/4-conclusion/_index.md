---
title: "Summary and Cleanup"
weight: 40
chapter: true
pre: "<b>4. </b>"
translationKey: "conclusion"
---

## Knowledge Summary

Through this lab, you have learned how to:

- Create and use KMS keys to encrypt data in S3
- Integrate CloudTrail to monitor activities
- Manage keys to maintain long-term security

KMS helps protect sensitive data, and combined with S3/CloudTrail creates a comprehensive security system. Remember to check costs (KMS charges per usage request) and clean up resources after the lab.

## Reference Documentation

- [AWS KMS Official Documentation](https://docs.aws.amazon.com/kms/latest/developer-guide/overview.html)
- [CloudTrail Guide](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-user-guide.html)
- [S3 Encryption Tutorial](https://docs.aws.amazon.com/AmazonS3/latest/userguide/UsingKMSEncryption.html)
- [AWS Skill Builder](https://skillbuilder.aws/) - For additional hands-on labs
- [AWS Documentation](https://docs.aws.amazon.com/) - Complete AWS service documentation

## Feedback

If you have feedback about the workshop:

- Create an issue on the GitHub repository
- Contribute improvements via pull requests
- Share experiences with the community

## Wrap Up

Done. First AWS KMS workshop completed.

Honestly, I didn't really get what encryption and key management were about at first. Thought it was just about encrypting files. But after going through this, it's way more complex - creating keys, setting permissions, key rotation, even auditing who uses your keys and when.

What I learned:
- Encryption isn't as hard as I thought, AWS handles the hard parts
- KMS and S3 work pretty smoothly together, just check a few boxes and your data is encrypted
- CloudTrail is pretty cool, you can see who's doing what with your keys
- Regular key rotation actually matters, can't just set and forget everything

Still fuzzy on some stuff, especially the policy and IAM parts. But that's fine, it'll click eventually. At least now I know how to protect data in the cloud, not leaving everything exposed like before.

---

Thanks if you made it this far too. Good luck with your next labs!