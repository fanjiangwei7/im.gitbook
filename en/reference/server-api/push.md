# 7 Push interface{#push}

## 7.1 Get push certificate{#get__push_certificate}

> GET /push/certificate

#### Request Header
|  Parameter name |  Data Type | Required |  Description |
|  ------ |  ------ |  ------ |  ------ |
| access-token | string | false | Token |
| app_id | string | true | App ID |
| group_id | int64 | false | This field can be set only if access-token is an Admin token, means call this interface as an Admin for this group ID |
| user_id | int64 | false | This field can be set only if access-token is a user token, means call this interface as a group member for this user ID |

#### Query Param
|  Parameter name |  Data Type | Required |  Description |
|  ------ |  ------ |  ------ |  ------ |
| environment | int32 | false | Run environment, 0 - development environment, 1 - production environment, default: 1 |
| provider | int32 | true | Certificate provider, 1-APNS,2-Huawei,3-Xiaomi,4-Meizu,5-VIVO, 6-OPPO, 7-FCM |

#### Response Body
● 200 Response data format:JSON

|  Parameter name |  Type |  Description |
|  ------ |  ------ |  ------ |
| code | int32 | Return code, 200 is success |
| data | object | Result data |
|⇥ app_id | string | APP ID |
|⇥ app_key | string | APP KEY |
|⇥ app_secret | string | APP SECRET |
|⇥ certificate | string | Certificate |
|⇥ name | string | Certificate name |
| message | string | Error information, null means success |
#### Interface Description
> 

## 7.2 Send push notification{#post__push_notify}

> POST /push/notify

#### Request Header
|  Parameter name |  Data Type | Required |  Description |
|  ------ |  ------ |  ------ |  ------ |
| access-token | string | false | Token |
| app_id | string | true | App ID |
| group_id | int64 | false | This field can be set only if access-token is an Admin token, means call this interface as an Admin for this group ID |
| user_id | int64 | false | This field can be set only if access-token is a user token, means call this interface as a group member for this user ID |

#### Request Body
|  Parameter name |  Data Type | Required  |  Default |  Description |
|  ------ |  ------ |  ------ |  ------ |  ------ |
| audience | object | false |  | Target of push, cannot be blank. Type is string or JSONObject:<br>"all", means push to all devices<br>{"tag":["tag1","tag2"]} means push to devices labeled tag1 or tag2<br>{"alias":["alias1","alias2"]} means push to devices with alias1 or alias2<br>{"user_id":[111,222]} means push to devices with user ID 111 or 222<br>{"push_token":["push_token1","push_token2"]} means push to devices with PushToken push_token1 or push_token2<br>List length cannot exceed 500 when pushed with tag/alias/user ID/pushToken |
| setting | object | false |  | Push settings, can be blank |
|⇥ request_id | string | false |  | Request ID for request deduplication, not pushed if request ID has been present before. Can be blank, which means no deduplication. |
|⇥ distribution_strategy | string | false |  | Notification distribution strategy: combined- means to use Lanying channel to distribute first, and if Lanying is not online, use vendor channel to distribute; Mxpush_only- indicates that only the Lanying channel is used for distribution; Ospush_only- indicates that only the vendor channel is used for distribution. Can be empty, which defaults to combined |
|⇥ ospush_sequence | array[string] | false |  | Vendor push priority: ups - domestic vendors (Xiaomi/Huawei/Meizu/oppo/vivo); fcm - FCM push; Huawei - Huawei push; Xiaomi - Xiaomi push; Oppo - OPPO push; Vivo - Vivo push, Meizu - Meizu push. Can be empty, which defaults to [ups, fcm] |
| message | object | false |  | Message body pushed, cannot be blank |
|⇥ type | string | false |  | Message type:text - text,image - image, cmd - pass-through message. Can be blank, which means text by default |
|⇥ title | string | false |  | Tittle, can be blank |
|⇥ body | string | false |  | Content, can be blank |
|⇥ attachment_url | string | false |  | Attachment address: URL address of image/audio/video, can be blank. If it is an image address, it needs to end with .jpg/jpeg/png, and the picture size should be less than 1M. 876*324 px is recommended |
|⇥ big_text | string | false |  | Large text: If this field is set and the vendor supports pushing large text, use this field to push large text; Otherwise, use the body field to push ordinary text |
|⇥ badge | string | false |  | Badge: If it is a number, modify the badge to this number; If starts with +, means adding this number to badge, ex. “+1” means adding 1 to badge; If blank, default “+1" |
|⇥ ext | object | false |  | Extension field: Can be blank, JSONObject type, ex. {"key1":123, "key2":"value2"} |
|⇥ show_begin_time | int64 | false |  | Start timestamp of timed presentation (seconds), blank for immediate presentation |
|⇥ show_end_time | int64 | false |  | End timestamp of timed presentation (seconds), can be blank |
|⇥ ios | object | false |  | Android extra parameter, can be blank |
|⇥⇥ sound | string | false |  | Notification alert sound, can be blank |
|⇥⇥ content_available | boolean | false |  | Corresponding to content-available in APNs, can be blank |
|⇥⇥ mutable_content | boolean | false |  | Corresponding to mutable-content in APNs, can be blank |
|⇥⇥ category | string | false |  | Corresponding to category in APNs Payload, can be blank |
|⇥⇥ thread_id | string | false |  | Corresponding to thread-id in APNs, can be blank; which is used for grouping notifications by thread-id |
|⇥⇥ subtitle | string | false |  | Subtitle corresponding to APNs, can be empty |
|⇥⇥ apns_collapse_id | string | false |  | apns-collapse-id corresponding to APNs, can be empty. The notifications with apns-collapse-id parameter will override other notifications with the same apns-collapse-id in the Notification Center. |
|⇥ android | object | false |  | ios extra parameter, can be blank |
|⇥⇥ sound | string | false |  | Message alert sound, can be blank |
|⇥⇥ channel_id | string | false |  | Notification bar channel, can be blank |
|⇥⇥ click_action | string | false |  | What to do after notification clicked: intent to open a specific page; open_app to open App homepage. Can be blank. |
|⇥⇥ intent | string | false |  | Click notification to open a specific page: can be blank, unless click_action is intent. Ex. intent:#Intent;component= package name/activity full path; S.parm1=value1;S.parm2=value2;end |
|⇥ huawei | object | false |  | huawei vendor extra parameter |
|⇥⇥ sound | string | false |  | Message alert sound, can be blank |
|⇥⇥ channel_id | string | false |  | Notification bar channel, can be blank |
|⇥⇥ click_action | string | false |  | What to do after notification clicked: intent to open a specific page; open_app to open App homepage. Can be blank. |
|⇥⇥ intent | string | false |  | Click notification to open a specific page: can be blank, unless click_action is intent. Ex. intent:#Intent;component= package name/activity full path; S.parm1=value1;S.parm2=value2;end |
|⇥⇥ badge_class | string | false |  | The application entry Activity class corresponding to the desktop icon, such as com.test.badge.MainActivity, which can be blank |
|⇥ xiaomi | object | false |  | xiaomi vendor extra parameter |
|⇥⇥ sound | string | false |  | Message alert sound, can be blank |
|⇥⇥ channel_id | string | false |  | Notification bar channel, can be blank |
|⇥⇥ click_action | string | false |  | What to do after notification clicked: intent to open a specific page; open_app to open App homepage. Can be blank. |
|⇥⇥ intent | string | false |  | Click notification to open a specific page: can be blank, unless click_action is intent. Ex. intent:#Intent;component= package name/activity full path; S.parm1=value1;S.parm2=value2;end |
|⇥ oppo | object | false |  | oppo vendor extra parameter |
|⇥⇥ sound | string | false |  | Message alert sound, can be blank |
|⇥⇥ channel_id | string | false |  | Notification bar channel, can be blank |
|⇥⇥ click_action | string | false |  | What to do after notification clicked: intent to open a specific page; open_app to open App homepage. Can be blank. |
|⇥⇥ intent | string | false |  | Click notification to open a specific page: can be blank, unless click_action is intent. Ex. intent:#Intent;component= package name/activity full path; S.parm1=value1;S.parm2=value2;end |
|⇥ vivo | object | false |  | vivo vendor extra parameter |
|⇥⇥ sound | string | false |  | Message alert sound, can be blank |
|⇥⇥ channel_id | string | false |  | Notification bar channel, can be blank |
|⇥⇥ click_action | string | false |  | What to do after notification clicked: intent to open a specific page; open_app to open App homepage. Can be blank. |
|⇥⇥ intent | string | false |  | Click notification to open a specific page: can be blank, unless click_action is intent. Ex. intent:#Intent;component= package name/activity full path; S.parm1=value1;S.parm2=value2;end |
|⇥⇥ push_mode | int32 | false |  | Push mode: 0 - production push; 1 - testing push. Default 0 |
|⇥⇥ classification | int32 | false |  | Message type: 0 - operational message; 1 - system message. Default 0 |
|⇥ flyme | object | false |  | meizu vendor extra parameter |
|⇥⇥ sound | string | false |  | Message alert sound, can be blank |
|⇥⇥ channel_id | string | false |  | Notification bar channel, can be blank |
|⇥⇥ click_action | string | false |  | What to do after notification clicked: intent to open a specific page; open_app to open App homepage. Can be blank. |
|⇥⇥ intent | string | false |  | Click notification to open a specific page: can be blank, unless click_action is intent. Ex. intent:#Intent;component= package name/activity full path; S.parm1=value1;S.parm2=value2;end |
|⇥ fcm | object | false |  | fcm vendor extra parameter |
|⇥⇥ sound | string | false |  | Message alert sound, can be blank |
|⇥⇥ channel_id | string | false |  | Notification bar channel, can be blank |
|⇥⇥ click_action | string | false |  | What to do after notification clicked: intent to open a specific page; open_app to open App homepage. Can be blank. |
|⇥⇥ intent | string | false |  | Click notification to open a specific page: can be blank, unless click_action is intent. Ex. intent:#Intent;component= package name/activity full path; S.parm1=value1;S.parm2=value2;end |

#### Response Body
● 200 Response data format:JSON

|  Parameter name |  Type |  Description |
|  ------ |  ------ |  ------ |
| code | int32 | Return code, 200 is success |
| data | object | Result data |
|⇥ task_id | int64 | Task ID |
| message | string | Error information, null means success |
#### Interface Description
> 

## 7.3 Query push stats{#post__push_task_detail}

> POST /push/task/detail

#### Request Header
|  Parameter name |  Data Type | Required |  Description |
|  ------ |  ------ |  ------ |  ------ |
| access-token | string | false | Token |
| app_id | string | true | App ID |
| group_id | int64 | false | This field can be set only if access-token is an Admin token, means call this interface as an Admin for this group ID |
| user_id | int64 | false | This field can be set only if access-token is a user token, means call this interface as a group member for this user ID |

#### Request Body
|  Parameter name |  Data Type | Required  |  Default |  Description |
|  ------ |  ------ |  ------ |  ------ |  ------ |
| list | array[int64] | true |  | List of task IDs |

#### Response Body
● 200 Response data format:JSON

|  Parameter name |  Type |  Description |
|  ------ |  ------ |  ------ |
| code | int32 | Return code, 200 is success |
| data | array[object] | Result data |
|⇥ apns_received | int64 | Delivery number on APNs channel |
|⇥ apns_sent | int64 | Sent number on APNs channel |
|⇥ apns_target | int64 | Valid target number on APNs channel |
|⇥ fcm_received | int64 | Delivery number on FCM channel |
|⇥ fcm_sent | int64 | Sent number on FCM channel |
|⇥ fcm_target | int64 | Valid target number on FCM channel |
|⇥ flyme_received | int64 | Delivery number on Meizu channel |
|⇥ flyme_sent | int64 | Sent number on Meizu channel |
|⇥ flyme_target | int64 | Valid target number on Meizu channel |
|⇥ huawei_received | int64 | Delivery number on Huawei channel |
|⇥ huawei_sent | int64 | Sent number on Huawei channel |
|⇥ huawei_target | int64 | Valid target number on Huawei channel |
|⇥ mxpush_received | int64 | Delivery number on Lanying channel |
|⇥ mxpush_sent | int64 | Sent number on Lanying channel |
|⇥ mxpush_target | int64 | Valid target number on Lanying channel |
|⇥ oppo_received | int64 | Delivery number on oppo channel |
|⇥ oppo_sent | int64 | Sent number on oppo channel |
|⇥ oppo_target | int64 | Valid target number on oppo channel |
|⇥ vivo_received | int64 | Delivery number on vivo channel |
|⇥ vivo_sent | int64 | Sent number on vivo channel |
|⇥ vivo_target | int64 | Valid target number on vivo channel |
|⇥ xiaomi_received | int64 | Delivery number on Xiaomi channel |
|⇥ xiaomi_sent | int64 | Sent number on Xiaomi channel |
|⇥ xiaomi_target | int64 | Valid target number on Xiaomi channel |
|⇥ task_id | int64 | Push task ID |
| message | string | Error information, null means success |
#### Interface Description
> 

