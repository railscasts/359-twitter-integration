# RailsCasts Episode #359: Twitter Integration

http://railscasts.com/episodes/359-twitter-integration

Requires Ruby 1.9.2 or higher.


### Commands used in this episode

```
rails g model testimony tweet_id screen_name content:text
rake db:migrate
rails g migration add_oauth_to_users oauth_token oauth_secret
rake db:migrate
```

### Commands used in rails console

```ruby
Twitter.favorites("railscasts", count: 1)
t = _.first
t.text
t.id
t.created_at
t.user.name
t.user.screen_name
t.user.profile_image_url
Testimony.pull_tweets
Twitter.favorites(count: 1)
Twitter.rate_limit_status
Twitter.update("This week's topic will be on Twitter integration. You will see me send this tweet during the episode!")
u = User.first
u.twitter.current_user.screen_name
```
