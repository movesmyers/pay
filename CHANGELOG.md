### 2.0.3

* [FIX] Stripe subscription cancel shouldn't change status
* [FIX] Stripe test payment methods should now work (ie. `pm_card_visa`)

### 2.0.2

* [FIX] Styling tweaks for payment intent page

### 2.0.1

* [FIX] Stripe Refund and Charge references weren't matching the right
  class

### 2.0.0

* [NEW] Stripe SCA support
* [BREAKING] Requires using PaymentMethods instead of Source and Tokens
* [BREAKING] Drops Ruby 2.4 support
* [BREAKING] `automount_webhook_routes` config option has been renamed to `automount_routes`
* [BREAKING]`webhooks_path` config option has been renamed to `routes_path`
* Added `status` column to payments to keep in sync with Stripe. We're
  also adding statuses to Braintree subscriptions to keep them in sync as best we can.
* Added `payments#show` route to handle SCA payments that require action
* Added webhook handler for payments that require action
* Added `trial_period_days` when creating a subscription that works the
  same on Stripe and Braintree

### 1.0.3

* Set default from email to `Pay.support_email`

### 1.0.2

* Add `on_trial_or_subscribed?` convenience method

### 1.0.1

* Removed Rails HTML Sanitizer dependency since it wasn't being used

### 1.0.0

* Add `stripe?`, `braintree?`, and `paypal?` to Pay::Charge
* Add webhook mounting and path options

### 1.0.0.beta4 - 2019-03-26

* Makes `stripe?`, `braintree?`, and `paypal?` helper methods always
  available on Billable.

### 1.0.0.beta3 - 2019-03-12

* Update migration to reference Billable instead of Users

### 1.0.0.beta2 - 2019-03-11

* Check ENV first when looking up keys to allow for overrides

