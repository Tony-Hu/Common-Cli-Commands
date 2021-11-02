# ELK

## 1 Create template
```
PUT _index_template/discord_bot_template
{
    "index_patterns": [
        "discord-bot-logs-*"
    ],
    "template": {
        "settings": {
            "number_of_shards": 1
        },
        "mappings": {
            "properties": {
                "message": {
                    "dynamic": true,
                    "properties": {
                        "d": {
                            "type": "object"
                        }
                    }
                }
            }
        }
    }
}
```

See https://www.elastic.co/guide/en/elasticsearch/reference/current/index-templates.html for details.
