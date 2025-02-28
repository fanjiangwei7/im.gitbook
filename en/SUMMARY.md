# Table of contents

* [Instant Messaging Development Guide (IM)](README.md)
* [Quick Start](quick-start/README.md)
  * [IOS SDK Quick Start](quick-start/floo-ios-quick-start.md)
  * [Android SDK Quick Start](quick-start/floo-android-quick-start.md)
  * [C++ SDK Quick Start](quick-start/floo-quick-start.md)
  * [Web SDK Quick Start](quick-start/floo-web-quick-start.md)
  * [Server API Development Guide](quick-start/server-api-quick-start.md)
  * [Push Development Guide](quick-start/push-dev-guide.md)
  * [Private Cloud Deployment](quick-start/how-to-deploy-private-cloud.md)
* [API Reference](reference/README.md)
  * [IOS SDK API (floo-ios)](reference/floo-ios.md)
    * [Classes](reference/floo-ios/classes.md)
      * [BMXChatService](reference/floo-ios/Classes/BMXChatService.md)
      * [BMXClient](reference/floo-ios/Classes/BMXClient.md)
      * [BMXConversation](reference/floo-ios/Classes/BMXConversation.md)
      * [BMXDevice](reference/floo-ios/Classes/BMXDevice.md)
      * [BMXFileAttachment](reference/floo-ios/Classes/BMXFileAttachment.md)
      * [BMXGroup](reference/floo-ios/Classes/BMXGroup.md)
      * [BMXGroupAnnouncement](reference/floo-ios/Classes/BMXGroupAnnouncement.md)
      * [BMXGroupApplication](reference/floo-ios/Classes/BMXGroupApplication.md)
      * [BMXGroupBannedMember](reference/floo-ios/Classes/BMXGroupBannedMember.md)
      * [BMXGroupInvitation](reference/floo-ios/Classes/BMXGroupInvitation.md)
      * [BMXGroupMember](reference/floo-ios/Classes/BMXGroupMember.md)
      * [BMXGroupService](reference/floo-ios/Classes/BMXGroupService.md)
      * [BMXGroupServiceCreateGroupOptions](reference/floo-ios/Classes/BMXGroupServiceCreateGroupOptions.md)
      * [BMXGroupSharedFile](reference/floo-ios/Classes/BMXGroupSharedFile.md)
      * [BMXImageAttachment](reference/floo-ios/Classes/BMXImageAttachment.md)
      * [BMXLocationAttachment](reference/floo-ios/Classes/BMXLocationAttachment.md)
      * [BMXMessage](reference/floo-ios/Classes/BMXMessage.md)
      * [BMXMessageAttachment](reference/floo-ios/Classes/BMXMessageAttachment.md)
      * [BMXMessageAttachmentSize](reference/floo-ios/Classes/BMXMessageAttachmentSize.md)
      * [BMXMessageConfig](reference/floo-ios/Classes/BMXMessageConfig.md)
      * [BMXPushService](reference/floo-ios/Classes/BMXPushService.md)
      * [BMXPushUserProfile](reference/floo-ios/Classes/BMXPushUserProfile.md)
      * [BMXPushUserProfileMessagePushSetting](reference/floo-ios/Classes/BMXPushUserProfileMessagePushSetting.md)
      * [BMXRTCEngine](reference/floo-ios/Classes/BMXRTCEngine.md)
      * [BMXRTCService](reference/floo-ios/Classes/BMXRTCService.md)
      * [BMXRoomAuth](reference/floo-ios/Classes/BMXRoomAuth.md)
      * [BMXRosterItem](reference/floo-ios/Classes/BMXRosterItem.md)
      * [BMXRosterService](reference/floo-ios/Classes/BMXRosterService.md)
      * [BMXRosterServiceApplication](reference/floo-ios/Classes/BMXRosterServiceApplication.md)
      * [BMXSDKConfig](reference/floo-ios/Classes/BMXSDKConfig.md)
      * [BMXSDKConfigHostConfig](reference/floo-ios/Classes/BMXSDKConfigHostConfig.md)
      * [BMXStream](reference/floo-ios/Classes/BMXStream.md)
      * [BMXUserProfile](reference/floo-ios/Classes/BMXUserProfile.md)
      * [BMXUserProfileAuthQuestion](reference/floo-ios/Classes/BMXUserProfileAuthQuestion.md)
      * [BMXUserProfileMessageSetting](reference/floo-ios/Classes/BMXUserProfileMessageSetting.md)
      * [BMXUserService](reference/floo-ios/Classes/BMXUserService.md)
      * [BMXVideoAttachment](reference/floo-ios/Classes/BMXVideoAttachment.md)
      * [BMXVideoCanvas](reference/floo-ios/Classes/BMXVideoCanvas.md)
      * [BMXVideoConfig](reference/floo-ios/Classes/BMXVideoConfig.md)
      * [BMXVoiceAttachment](reference/floo-ios/Classes/BMXVoiceAttachment.md)
    * [Protocols](reference/floo-ios/protocols.md)
      * [BMXChatServiceProtocol](reference/floo-ios/Protocols/BMXChatServiceProtocol.md)
      * [BMXGroupServiceProtocol](reference/floo-ios/Protocols/BMXGroupServiceProtocol.md)
      * [BMXPushServiceProtocol](reference/floo-ios/Protocols/BMXPushServiceProtocol.md)
      * [BMXRTCEngineProtocol](reference/floo-ios/Protocols/BMXRTCEngineProtocol.md)
      * [BMXRTCServiceProtocol](reference/floo-ios/Protocols/BMXRTCServiceProtocol.md)
      * [BMXRosterServiceProtocol](reference/floo-ios/Protocols/BMXRosterServiceProtocol.md)
      * [BMXUserServiceProtocol](reference/floo-ios/Protocols/BMXUserServiceProtocol.md)
    * [Constants](reference/floo-ios/constants.md)
      * [BMXChatService_ThumbnailStrategy](reference/floo-ios/Constants/BMXChatService_ThumbnailStrategy.md)
      * [BMXClientType](reference/floo-ios/Constants/BMXClientType.md)
      * [BMXConnectStatus](reference/floo-ios/Constants/BMXConnectStatus.md)
      * [BMXConversation_Direction](reference/floo-ios/Constants/BMXConversation_Direction.md)
      * [BMXConversation_Type](reference/floo-ios/Constants/BMXConversation_Type.md)
      * [BMXErrorCode](reference/floo-ios/Constants/BMXErrorCode.md)
      * [BMXGroup_ApplicationStatus](reference/floo-ios/Constants/BMXGroup_ApplicationStatus.md)
      * [BMXGroup_GroupStatus](reference/floo-ios/Constants/BMXGroup_GroupStatus.md)
      * [BMXGroup_GroupType](reference/floo-ios/Constants/BMXGroup_GroupType.md)
      * [BMXGroup_InvitationStatus](reference/floo-ios/Constants/BMXGroup_InvitationStatus.md)
      * [BMXGroup_InviteMode](reference/floo-ios/Constants/BMXGroup_InviteMode.md)
      * [BMXGroup_JoinAuthMode](reference/floo-ios/Constants/BMXGroup_JoinAuthMode.md)
      * [BMXGroup_MemberRoleType](reference/floo-ios/Constants/BMXGroup_MemberRoleType.md)
      * [BMXGroup_ModifyMode](reference/floo-ios/Constants/BMXGroup_ModifyMode.md)
      * [BMXGroup_MsgMuteMode](reference/floo-ios/Constants/BMXGroup_MsgMuteMode.md)
      * [BMXGroup_MsgPushMode](reference/floo-ios/Constants/BMXGroup_MsgPushMode.md)
      * [BMXGroup_UpdateInfoType](reference/floo-ios/Constants/BMXGroup_UpdateInfoType.md)
      * [BMXLogLevel](reference/floo-ios/Constants/BMXLogLevel.md)
      * [BMXMessageAttachment_DownloadStatus](reference/floo-ios/Constants/BMXMessageAttachment_DownloadStatus.md)
      * [BMXMessageAttachment_Type](reference/floo-ios/Constants/BMXMessageAttachment_Type.md)
      * [BMXMessageConfig_BadgeCountType](reference/floo-ios/Constants/BMXMessageConfig_BadgeCountType.md)
      * [BMXMessageConfig_RTCCallType](reference/floo-ios/Constants/BMXMessageConfig_RTCCallType.md)
      * [BMXMessageConfig_RTCRoomType](reference/floo-ios/Constants/BMXMessageConfig_RTCRoomType.md)
      * [BMXMessage_ContentType](reference/floo-ios/Constants/BMXMessage_ContentType.md)
      * [BMXMessage_DeliveryQos](reference/floo-ios/Constants/BMXMessage_DeliveryQos.md)
      * [BMXMessage_DeliveryStatus](reference/floo-ios/Constants/BMXMessage_DeliveryStatus.md)
      * [BMXMessage_MessageType](reference/floo-ios/Constants/BMXMessage_MessageType.md)
      * [BMXNetworkType](reference/floo-ios/Constants/BMXNetworkType.md)
      * [BMXPushEnvironmentType](reference/floo-ios/Constants/BMXPushEnvironmentType.md)
      * [BMXPushProviderType](reference/floo-ios/Constants/BMXPushProviderType.md)
      * [BMXPushService_PushDirection](reference/floo-ios/Constants/BMXPushService_PushDirection.md)
      * [BMXPushService_PushSdkStatus](reference/floo-ios/Constants/BMXPushService_PushSdkStatus.md)
      * [BMXRenderMode](reference/floo-ios/Constants/BMXRenderMode.md)
      * [BMXRoomType](reference/floo-ios/Constants/BMXRoomType.md)
      * [BMXRosterItem_AddFriendAuthMode](reference/floo-ios/Constants/BMXRosterItem_AddFriendAuthMode.md)
      * [BMXRosterItem_RosterRelation](reference/floo-ios/Constants/BMXRosterItem_RosterRelation.md)
      * [BMXRosterService_ApplicationStatus](reference/floo-ios/Constants/BMXRosterService_ApplicationStatus.md)
      * [BMXSignInStatus](reference/floo-ios/Constants/BMXSignInStatus.md)
      * [BMXUserProfile_AddFriendAuthMode](reference/floo-ios/Constants/BMXUserProfile_AddFriendAuthMode.md)
      * [BMXUserProfile_UserCategory](reference/floo-ios/Constants/BMXUserProfile_UserCategory.md)
      * [BMXVideoMediaType](reference/floo-ios/Constants/BMXVideoMediaType.md)
      * [BMXVideoProfile](reference/floo-ios/Constants/BMXVideoProfile.md)
  * [IOS SDK API (floo-rtc-ios)](reference/floo-rtc-ios.md)
    * [Classes](reference/floo-rtc-ios/classes.md)
      * [RTCEngineManager](reference/floo-rtc-ios/Classes/RTCEngineManager.md)
  * [Android SDK API (floo-android)](reference/floo-android.md)
    * [im::floo::floolib::BMXChatManager](reference/floo-android/classim_1_1floo_1_1floolib_1_1_b_m_x_chat_manager.md)
    * [im::floo::floolib::BMXChatService](reference/floo-android/classim_1_1floo_1_1floolib_1_1_b_m_x_chat_service.md)
    * [im::floo::floolib::BMXChatServiceListener](reference/floo-android/classim_1_1floo_1_1floolib_1_1_b_m_x_chat_service_listener.md)
    * [im::floo::floolib::BMXClient](reference/floo-android/classim_1_1floo_1_1floolib_1_1_b_m_x_client.md)
    * [im::floo::floolib::BMXConversation](reference/floo-android/classim_1_1floo_1_1floolib_1_1_b_m_x_conversation.md)
    * [im::floo::floolib::BMXDevice](reference/floo-android/classim_1_1floo_1_1floolib_1_1_b_m_x_device.md)
    * [im::floo::floolib::BMXFileAttachment](reference/floo-android/classim_1_1floo_1_1floolib_1_1_b_m_x_file_attachment.md)
    * [im::floo::floolib::BMXGroup](reference/floo-android/classim_1_1floo_1_1floolib_1_1_b_m_x_group.md)
      * [Announcement](reference/floo-android/classim_1_1floo_1_1floolib_1_1_b_m_x_group_1_1_announcement.md)
      * [Application](reference/floo-android/classim_1_1floo_1_1floolib_1_1_b_m_x_group_1_1_application.md)
    * [im::floo::floolib::BMXGroup::BannedMember](reference/floo-android/classim_1_1floo_1_1floolib_1_1_b_m_x_group_1_1_banned_member.md)
    * [im::floo::floolib::BMXGroup::Invitation](reference/floo-android/classim_1_1floo_1_1floolib_1_1_b_m_x_group_1_1_invitation.md)
    * [im::floo::floolib::BMXGroup::Member](reference/floo-android/classim_1_1floo_1_1floolib_1_1_b_m_x_group_1_1_member.md)
    * [im::floo::floolib::BMXGroup::SharedFile](reference/floo-android/classim_1_1floo_1_1floolib_1_1_b_m_x_group_1_1_shared_file.md)
    * [im::floo::floolib::BMXGroupManager](reference/floo-android/classim_1_1floo_1_1floolib_1_1_b_m_x_group_manager.md)
    * [im::floo::floolib::BMXGroupService](reference/floo-android/classim_1_1floo_1_1floolib_1_1_b_m_x_group_service.md)
      * [CreateGroupOptions](reference/floo-android/classim_1_1floo_1_1floolib_1_1_b_m_x_group_service_1_1_create_group_options.md)
    * [im::floo::floolib::BMXGroupServiceListener](reference/floo-android/classim_1_1floo_1_1floolib_1_1_b_m_x_group_service_listener.md)
    * [im::floo::floolib::BMXImageAttachment](reference/floo-android/classim_1_1floo_1_1floolib_1_1_b_m_x_image_attachment.md)
    * [im::floo::floolib::BMXLocationAttachment](reference/floo-android/classim_1_1floo_1_1floolib_1_1_b_m_x_location_attachment.md)
    * [im::floo::floolib::BMXMessage](reference/floo-android/classim_1_1floo_1_1floolib_1_1_b_m_x_message.md)
    * [im::floo::floolib::BMXMessageAttachment](reference/floo-android/classim_1_1floo_1_1floolib_1_1_b_m_x_message_attachment.md)
    * [im::floo::floolib::BMXMessageAttachment::Size](reference/floo-android/classim_1_1floo_1_1floolib_1_1_b_m_x_message_attachment_1_1_size.md)
    * [im::floo::floolib::BMXMessageConfig](reference/floo-android/classim_1_1floo_1_1floolib_1_1_b_m_x_message_config.md)
    * [im::floo::floolib::BMXNetworkListener](reference/floo-android/classim_1_1floo_1_1floolib_1_1_b_m_x_network_listener.md)
    * [im::floo::floolib::BMXPushManager](reference/floo-android/classim_1_1floo_1_1floolib_1_1_b_m_x_push_manager.md)
    * [im::floo::floolib::BMXPushService](reference/floo-android/classim_1_1floo_1_1floolib_1_1_b_m_x_push_service.md)
    * [im::floo::floolib::BMXPushServiceListener](reference/floo-android/classim_1_1floo_1_1floolib_1_1_b_m_x_push_service_listener.md)
    * [im::floo::floolib::BMXPushUserProfile](reference/floo-android/classim_1_1floo_1_1floolib_1_1_b_m_x_push_user_profile.md)
      * [MessagePushSetting](reference/floo-android/classim_1_1floo_1_1floolib_1_1_b_m_x_push_user_profile_1_1_message_push_setting.md)
    * [im::floo::floolib::BMXRosterItem](reference/floo-android/classim_1_1floo_1_1floolib_1_1_b_m_x_roster_item.md)
    * [im::floo::floolib::BMXRosterManager](reference/floo-android/classim_1_1floo_1_1floolib_1_1_b_m_x_roster_manager.md)
    * [im::floo::floolib::BMXRosterService](reference/floo-android/classim_1_1floo_1_1floolib_1_1_b_m_x_roster_service.md)
      * [Application](reference/floo-android/classim_1_1floo_1_1floolib_1_1_b_m_x_roster_service_1_1_application.md)
    * [im::floo::floolib::BMXRosterServiceListener](reference/floo-android/classim_1_1floo_1_1floolib_1_1_b_m_x_roster_service_listener.md)
    * [im::floo::floolib::BMXSDKConfig](reference/floo-android/classim_1_1floo_1_1floolib_1_1_b_m_x_s_d_k_config.md)
      * [HostConfig](reference/floo-android/classim_1_1floo_1_1floolib_1_1_b_m_x_s_d_k_config_1_1_host_config.md)
    * [im::floo::floolib::BMXUserManager](reference/floo-android/classim_1_1floo_1_1floolib_1_1_b_m_x_user_manager.md)
    * [im::floo::floolib::BMXUserProfile](reference/floo-android/classim_1_1floo_1_1floolib_1_1_b_m_x_user_profile.md)
    * [im::floo::floolib::BMXUserProfile::AuthQuestion](reference/floo-android/classim_1_1floo_1_1floolib_1_1_b_m_x_user_profile_1_1_auth_question.md)
    * [im::floo::floolib::BMXUserProfile::MessageSetting](reference/floo-android/classim_1_1floo_1_1floolib_1_1_b_m_x_user_profile_1_1_message_setting.md)
    * [im::floo::floolib::BMXUserService](reference/floo-android/classim_1_1floo_1_1floolib_1_1_b_m_x_user_service.md)
    * [im::floo::floolib::BMXUserServiceListener](reference/floo-android/classim_1_1floo_1_1floolib_1_1_b_m_x_user_service_listener.md)
    * [im::floo::floolib::BMXVideoAttachment](reference/floo-android/classim_1_1floo_1_1floolib_1_1_b_m_x_video_attachment.md)
    * [im::floo::floolib::BMXVoiceAttachment](reference/floo-android/classim_1_1floo_1_1floolib_1_1_b_m_x_voice_attachment.md)
  * [C++ SDK API (floo)](reference/floo.md)
    * [floo::BMXChatService](reference/floo/classfloo_1_1_b_m_x_chat_service.md)
    * [floo::BMXChatServiceListener](reference/floo/classfloo_1_1_b_m_x_chat_service_listener.md)
    * [floo::BMXClient](reference/floo/classfloo_1_1_b_m_x_client.md)
    * [floo::BMXConversation](reference/floo/classfloo_1_1_b_m_x_conversation.md)
    * [floo::BMXDevice](reference/floo/classfloo_1_1_b_m_x_device.md)
    * [floo::BMXError](reference/floo/classfloo_1_1_b_m_x_error.md)
    * [floo::BMXFileAttachment](reference/floo/classfloo_1_1_b_m_x_file_attachment.md)
    * [floo::BMXForwardAttachment](reference/floo/classfloo_1_1_b_m_x_forward_attachment.md)
      * [Message](reference/floo/classfloo_1_1_b_m_x_forward_attachment_1_1_message.md)
    * [floo::BMXGroup](reference/floo/classfloo_1_1_b_m_x_group.md)
    * [floo::BMXGroupService](reference/floo/classfloo_1_1_b_m_x_group_service.md)
    * [floo::BMXGroupServiceListener](reference/floo/classfloo_1_1_b_m_x_group_service_listener.md)
    * [floo::BMXImageAttachment](reference/floo/classfloo_1_1_b_m_x_image_attachment.md)
    * [floo::BMXLocationAttachment](reference/floo/classfloo_1_1_b_m_x_location_attachment.md)
    * [floo::BMXMessage](reference/floo/classfloo_1_1_b_m_x_message.md)
    * [floo::BMXMessageAttachment](reference/floo/classfloo_1_1_b_m_x_message_attachment.md)
    * [floo::BMXMessageConfig](reference/floo/classfloo_1_1_b_m_x_message_config.md)
    * [floo::BMXNetworkListener](reference/floo/classfloo_1_1_b_m_x_network_listener.md)
    * [floo::BMXPushService](reference/floo/classfloo_1_1_b_m_x_push_service.md)
    * [floo::BMXPushServiceListener](reference/floo/classfloo_1_1_b_m_x_push_service_listener.md)
    * [floo::BMXPushUserProfile](reference/floo/classfloo_1_1_b_m_x_push_user_profile.md)
    * [floo::BMXResultPage](reference/floo/classfloo_1_1_b_m_x_result_page.md)
    * [floo::BMXRosterItem](reference/floo/classfloo_1_1_b_m_x_roster_item.md)
    * [floo::BMXRosterService](reference/floo/classfloo_1_1_b_m_x_roster_service.md)
    * [floo::BMXRosterServiceListener](reference/floo/classfloo_1_1_b_m_x_roster_service_listener.md)
    * [floo::BMXSDKConfig](reference/floo/classfloo_1_1_b_m_x_s_d_k_config.md)
    * [floo::BMXUserProfile](reference/floo/classfloo_1_1_b_m_x_user_profile.md)
    * [floo::BMXUserService](reference/floo/classfloo_1_1_b_m_x_user_service.md)
    * [floo::BMXUserServiceListener](reference/floo/classfloo_1_1_b_m_x_user_service_listener.md)
    * [floo::BMXVideoAttachment](reference/floo/classfloo_1_1_b_m_x_video_attachment.md)
    * [floo::BMXVoiceAttachment](reference/floo/classfloo_1_1_b_m_x_voice_attachment.md)
  * [Web SDK API (floo-web)](reference/floo-web.md)
    * [flooim](reference/floo-web/flooim.md)
    * [userManage](reference/floo-web/userManage.md)
    * [rosterManage](reference/floo-web/rosterManage.md)
    * [groupManage](reference/floo-web/groupManage.md)
    * [sysManage](reference/floo-web/sysManage.md)
    * [types](reference/floo-web/types.md)
  * [Server API](reference/server-api/README.md)
    * [User Operation](reference/server-api/user.md)
    * [Token Interface](reference/server-api/token.md)
    * [Roster Operation](reference/server-api/roster.md)
    * [Group Operation](reference/server-api/group.md)
    * [Message Manipulation](reference/server-api/message.md)
    * [File Manipulation](reference/server-api/file.md)
    * [Push Interface](reference/server-api/push.md)
