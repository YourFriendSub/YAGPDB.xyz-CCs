What is it?
  - It counts Positive & Negative reactions of the forum post.
  - Then Subtracts the negatives from positive reactions.
  - Based on the remaining reaction counts, it updates the tag of post.

  - Best for forum channels used for Art Sharing, Code Sharing etc.
    - I use for Art channel.

Configuration Help:
  ————————————————————
  - FORUM_CHANNEL_ID: Forum ChannelID, In which channel you want to turn it ON.
  - EmojiP: Like or Upvote emoji. P=Positive. If custom emoji: `"EMOJI_NAME:EMOJI_ID"` else `"❤️"`.
  - EmojiN: Dislike or Downvote emoji. N=Negative. If custom emoji: `"EMOJI_NAME:EMOJI_ID"` else `"💔"`.
  - SelfRate: If `true`, OP's reaction will be also counted. Else, removed.
  - Rating: Read Below.
    - C: On how many reactions (Output) the tag should be changed. N will be removed from P. If N=2, P=5 then Output=3.
    - T: Name of tag to add when reaching the desired Reaction (Output).
  ————————————————————

By Author:
  - I'M NOT REMOVING MY SET VALUES JUST FOR UNDERSTANDINGS.
