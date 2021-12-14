<a href="https://beyonk.com">
    <br />
    <br />
    <img src="https://user-images.githubusercontent.com/218949/144224348-1b3a20d5-d68e-4a7a-b6ac-6946f19f4a86.png" width="198" />
    <br />
    <br />
</a>

## Svelte Facebook Customer Chat

[![js-standard-style](https://img.shields.io/badge/code%20style-standard-brightgreen.svg)](http://standardjs.com) [![CircleCI](https://circleci.com/gh/beyonk-adventures/svelte-facebook-customer-chat.svg?style=shield)](https://circleci.com/gh/beyonk-adventures/svelte-facebook-customer-chat)


Pure vanilla JS Facebook Customer Chat integration

![facebook customer chat](https://scontent-lhr3-1.xx.fbcdn.net/v/t39.2365-6/26906829_1994780764110817_8797989954643820544_n.png?_nc_cat=102&_nc_ht=scontent-lhr3-1.xx&oh=752e7a70e0d37e1a93e70e7067af4fb7&oe=5CC65975 "Facebook Customer Chat")

## Install

```bash
$ npm install --save-dev @beyonk/svelte-facebook-customer-chat
```

## Usage (With Svelte)

```html
<CustomerChat ref:fb page_id="163258547622199" theme_color="#05a092"  />

<script>
  import CustomerChat from '@beyonk/svelte-facebook-customer-chat'

	export default {
		components: {
			CustomerChat
		}
	}
</script>
```

The attributes you pass to the CustomerChat component are [as per facebook documentation](https://developers.facebook.com/docs/messenger-platform/discovery/customer-chat-plugin/).

You definitely need to pass the attribute `page_id`.

## Usage (Vanilla JS)

```html
<div id="my-chat"></div>

<script>
  import CustomerChat from '@beyonk/svelte-facebook-customer-chat'

	const chat = new CustomerChat({
		target: document.querySelector('#my-chat'),
		data: {
			page_id: '1234567890',
			theme_color: '#ff0000'
		}
	})
</script>
```

## Other (non facebook attributes)

There are a number of configuration attributes you can pass, but all are optional.

List of possible options in the module:

| Option            | Default  | Required | Description                                                                                         |
|-------------------|----------|----------|-----------------------------------------------------------------------------------------------------|
| locale            | en_GB    | false    | Facebook chat locale                                                                                |
| version           | v2.12    | false    | Facebook Customer Chat SDK version                                                                  |
| autoLogAppEvents  | true     | false    | as Facebook. Automatically log app events                                                           |
| lib               | true     | false    | Unique id to determine if component is loaded. You probably don't need to change this.              |

## License

[MIT License](./LICENSE)
