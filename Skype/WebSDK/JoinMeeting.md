
# Join an existing meeting

 **Last modified:** February 02, 2016

 _**Applies to:** Skype for Business 2015_

A user can join an existing meeting with that meeting's URI.


### Joining an existing meeting


1. Get an instance of the [Conversation](https://msdn.microsoft.com/en-us/library/office/dn962132(v=office.16).aspx). At this point the user still has not joined the conversation.


  ```js
  var conversation = client.conversationsManager.getConversationByUri(uri);
  ```

2. Start the desired modality for this conversation. At this point the user will have joined the conversation.
    
    The user can join the conversation when the app starts the desired service:
    


  ```js
  // join chat
conversation.chatService.start().then(function() {
…
});
  ```




  ```js
  // join audio
conversation.audioService.start().then(function() {
…
});
  ```




  ```js
  // join video
conversation.videoService.start().then(function() {
…
});
  ```


## Additional resources

- [Join a meeting anonymously](AnonymousMeetingJoin.md)
