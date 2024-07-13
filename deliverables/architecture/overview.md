```
静的アーキテクチャ概要

[ユーザー]　⇒　[CloudFront]　⇒　[S3 (静的コンテンツ)]   
                    ↓   
                [API Gateway]   
                    ↓
                [Lambda関数]
               /     |     \
              v      v      v
        [SageMaker] [RDS] [S3 (データ)]
```