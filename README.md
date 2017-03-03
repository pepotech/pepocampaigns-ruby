PepoCampaigns Ruby client
========================

Ruby client for PepoCampaigns REST API. For details about the API, documentation and examples please visit: [https://know.pepocampaigns.com/categories/api/](https://know.pepocampaigns.com/categories/api/)

## Requirements

* Ruby 2.1+ (Tested with rails 5.0)
* openssl 1.0.1
* TLS 1.2 protocol is recommended

## Usage

### Initiation 
	
```ruby
require "pepo_campaigns"

# api_key and api_secret to be passed while initiation
pepo_campaigns = PepoCampaigns.new('3gd68b470d1205bd57fd4dbfa1208ab1', 'e74c748409db3fae8add716fbeb315a2')
```    

### Example API Calls

[Creating a new list](https://know.pepocampaigns.com/articles/managing-lists-api/#creating-a-new-list)

```ruby
pepo_campaigns.create_list('test list2', 'My Pepo Campaigns Test List2', 'double')
```

[Adding a contact to a List](https://know.pepocampaigns.com/articles/managing-lists-api/#adding-a-contact-to-a-list)

```ruby
pepo_campaigns.add_contact(419,'vpuui.skbbx21@gmail.com', {'First Name' => 'Vpuui', 'Last Name' => 'Skbbx'})
```

[Removing a contact from a list](https://know.pepocampaigns.com/articles/managing-lists-api/#removing-a-contact-from-a-list)

```ruby
pepo_campaigns.remove_contact(419,'vpuui.skbbx21@gmail.com')
```

[Changing User Status](https://know.pepocampaigns.com/articles/managing-contacts-api/#changing-user-status)

```ruby
pepo_campaigns.change_user_status('vpuui.skbbx21@gmail.com', 'unsubscribe')
```

[Send Transactional Email](https://know.pepocampaigns.com/articles/managing-transactional/#send-transactional-email)

```ruby
pepo_campaigns.send_transactional_email("vpuui.skbbx21@gmail.com", "welcome", {'a' => 1, 'b' => 2, 'c' => {'d' => 3, 'e' => 4}})
```

## License

[MIT License](LICENSE)
