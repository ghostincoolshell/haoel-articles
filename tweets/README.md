- `haoel.csv`: [@haoel](https://twitter.com/haoel) 发表的所有 tweets.

  Copied from https://github.com/yihong0618/twint . Thanks [@yihong0618](https://github.com/yihong0618).

- `haoel.db`: 已格式化并转换为 SQLite 数据库的同一份数据

  Schema:

  ```sqlite
  CREATE TABLE "tweets" (
  	"id"	INTEGER NOT NULL UNIQUE,  -- Snowflake ID
  	"timestamp"	INTEGER NOT NULL,     -- Unix timestamp
  	"likes_count"	INTEGER NOT NULL,
  	"retweet_count"	INTEGER NOT NULL,
  	"reply_count"	INTEGER NOT NULL,
  	"content"	TEXT NOT NULL         -- 已解析 HTML entities 和 t.co 短链
  );
  ```

  Note: 可使用 <https://github.com/wangfenjin/simple> 进行全文索引。
