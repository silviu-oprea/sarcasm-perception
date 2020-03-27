sarcasm-annotations.jsonl contains a list of tweet IDs together with sarcasm labels for the corresponding tweet. There are 4 such labels for each tweet, one provided by its author, and three more provided by third-party annotators of varying sociocultural backgrounds.

Each line in the file contains a json document with the following fields:

- tweet_id: ID of the tweet, which can be used to retrieve the corresponding tweet using the Twitter API;
- speaker_background: speaker (i.e. author of the tweet) sociocultural background. It is specified as <gender>_<age>_<country>, where gender ∈ {M, F}, age ∈ {25-34, >45}, country ∈ {UK, US};
- listeners_background: sociocultural background that the three annotators who labelled the current tweet for sarcasm share. It is specified as <gender>_<age>_<country>(_<nativeness)?, where <nativeness> can be "!native", indicating that the listener is not a native speaker of English, or can be not specified, indicating that the listener is a native speaker;
- with_context: whether the annotators were given the link to the tweet (with_context=YES), or just the text of the tweet (with_context=NO);
- speaker_label: 0 or 1, indicating the sarcastic nature of the current tweet, as specified by the speaker (i.e. the author of the tweet);
- listener_labels: list of three digits, each being either 0 or 1, each specifying the sarcastic nature of the current tweet according to one of the three annotators.
