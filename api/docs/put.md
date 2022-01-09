# OxyCloud API

## Upload a document

Generate a presigned form to be used to upload the file directly on the returned s3 bucket

**URL**: `/docs`

**Method**: `PUT`

**Auth required**: YES

### Request

#### Params

|name   |description|type   |source   |default |required|
|-------|-----------|-------|---------|--------|--------|

### Response

#### Scheme

*success:*

```json
{
  "url": string,
  "fields": Map<string,string>
}
```

*error:*

```json
{
    "message": string,
}
```

#### Example

```json
{
  "url": "https://[BUCKET_NAME].s3.amazonaws.com/",
  "fields": {
    "x-amz-meta-displayname": "[base64(filename)]",
    "x-amz-meta-folder": "[FOLDER_ID]",
    "x-amz-meta-user": "[USER_ID]",
    "key": "[FILE_ID]",
    "x-amz-algorithm": "XXX",
    "x-amz-credential": "XXX",
    "x-amz-date": "XXXX",
    "x-amz-security-token": "XXX",
    "policy": "XXX",
    "x-amz-signature": "XXX"
  }
}
```

## Flow

![flow](https://www.plantuml.com/plantuml/png/VL5DQniz4BxhLqnoYL-mBN8rBoLk325GIC2O7aefiwlPNRLQIPL6thY7_lPAkvicXBXxM6cavsEUqKra39nw8ouKDTeIR3_l7tCD7REF6oa33kjMSvUg52dKpZ9PNjUkbpX4WrKiwqhdYxXgN5XvWxO8okFrzVfQAXrPN6XRcwGe1VEiB_Dww_hUsRKlzk8A3ZQhzbaTk2Ded35kqBO5KzfY1tKWP8AeUszqeqd1KTDmJdp_5pORl8Ux8qi1ZJpaQ2FiVJMVbMfaxUozPMh3k9NRn_ixP1hmT9wwfpe5pQTxHPRpcYDdBRGroLlNMitkFBTW4vFyX7sby1yUx0As9CV4D5Tx2aTTqtdM3XahZ2Ht9ukzstsSe8OQBiCEkkqOb0vKbx2YJ6YHycy9syIT2_eNAPWEVlydNcQnoDibF3oTRerB2afL0CykYqORYjzKjOJBkLLuRkLocO7lfLZ4gNp5gLBzWtXaY6b0YvRimHk7wX43zd49q-ioWGyKTMj9WSTGRZ9h9hcPS_0g8tUbhGSBFl53zJr7XpIUWwekHvQuof-uobP2bF3m_shreOJSGA2VIMSZu8ucdpB7DAe3GibTnZGntlIwWIy-kAVJrsomhJcXcOclJEOPRC1JQ5oHdxK7pTre-f8nIueP3uNxDkNcLK8wacNn5Z7IvhVAy25e9kY9CL-Zk26hKc_-0000)