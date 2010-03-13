django-creditcard-fields provides custom form fields for collecting and
validating credit card information.

Example usage:

from django import forms
from fields import CreditCardField, ExpiryDateField

class PaymentForm(forms.Form):

    name_on_card = forms.CharField(max_length=50, required=True)
    card_number = CreditCardField(required=True)
    expiry_date = ExpiryDateField(required=True)

