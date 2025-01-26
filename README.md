# Test Task: x.com API Integration 

## Objective
create a function "getAuthenticatedClient" which accepts auth_token cookie value as an argument
and returns authenticated axios client for making requests to x.com api
---

## Requirements

1. **API Integration**
    - Use the https://github.com/the-convocation/twitter-scraper repository as a reference,
    this repo contains working flow for authentication using USERNAME + PASSWORD + EMAIL,
   the goal is to achieve Authenticated requests just using auth_token cookie value , omitting default login flow.
    - for testing purpose u can use your own twitter account (or create new one)

2. **expected working code**
```javascript
(async function run() {

    const client = await getAuthenticatedClient('PLS_DO_NOT_COMMIT_YOUR_AUTH_TOKEN')


    try {
        const response = await client.get('https://twitter.com/i/api/1.1/dm/inbox_initial_state.json?nsfw_filtering_enabled=false&include_profile_interstitial_type=1&include_blocking=1&include_blocked_by=1&include_followed_by=1&include_want_retweets=1&include_mute_edge=1&include_can_dm=1&include_can_media_tag=1&include_ext_is_blue_verified=1&include_ext_verified_type=1&include_ext_profile_image_shape=1&skip_status=1&dm_secret_conversations_enabled=false&krs_registration_enabled=true&cards_platform=Web-12&include_cards=1&include_ext_alt_text=true&include_ext_limited_action_results=true&include_quote_count=true&include_reply_count=1&tweet_mode=extended&include_ext_views=true&dm_users=true&include_groups=true&include_inbox_timelines=true&include_ext_media_color=true&supports_reactions=true&supports_edit=true&include_ext_edit_control=true&include_ext_business_affiliations_label=true&include_ext_parody_commentary_fan_label=true&ext=mediaColor%2CaltText%2CmediaStats%2ChighlightedLabel%2CparodyCommentaryFanLabel%2CvoiceInfo%2CbirdwatchPivot%2CsuperFollowMetadata%2CunmentionInfo%2CeditControl%2Carticle')

        console.log('response',JSON.stringify(response.data))
    }
    catch (e) {
        console.log(e)
    }


})()

async function getAuthenticatedClient(auth_token) {
    
    //here goes your implementation
}

```
    
---

## Deliverables
- A GitHub repository containing your code. 

---

## Bonus Points 
- Use TypeScript for stricter typing. 

---

## Deadline
You have **24 hours** to complete the task. Please submit the GitHub repository link before the deadline.
