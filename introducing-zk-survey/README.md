---
description: Zk Surv
---

# Introducing ZK Survey

{% hint style="warning" %}
The smart contracts nor the circuits are audited. Is not production ready.
{% endhint %}



ZK Survey is a survey tool akin to Google Forms or Typeform, but with the ability to conduct surveys that respondents can **answer anonymously** while **proving their answers' trustworthiness without revealing their identity**. It is also **highly composable**; both surveys and answers reside on Arweave, and the reputation verification is concluded in a smart contract on Ethereum.



but with three unique features Composabiligy, end-to-end anonymity, with a trustless reputation&#x20;

### Composability





### End-to-end anonymity





### Trustless survey data credibility







\












## Install the libray

The best way to interact with our API is to use one of our official libraries:

{% tabs %}
{% tab title="Node" %}
```
# Install via NPM
npm install --save my-api
```
{% endtab %}

{% tab title="Python" %}
```
# Install via pip
pip install --upgrade myapi
```
{% endtab %}
{% endtabs %}

{% hint style="info" %}
**Good to know:** Using tabs to separate out different languages is a great way to present technical examples or code documentation without cramming your docs with extra sections or pages per language.
{% endhint %}

## Make your first request

To make your first request, send an authenticated request to the pets endpoint. This will create a `pet`, which is nice.

{% swagger baseUrl="https://api.myapi.com/v1" method="post" path="/pet" summary="Create pet." %}
{% swagger-description %}
Creates a new pet.
{% endswagger-description %}

{% swagger-parameter in="body" name="name" required="true" type="string" %}
The name of the pet
{% endswagger-parameter %}

{% swagger-parameter in="body" name="owner_id" required="false" type="string" %}
The 

`id`

 of the user who owns the pet
{% endswagger-parameter %}

{% swagger-parameter in="body" name="species" required="false" type="string" %}
The species of the pet
{% endswagger-parameter %}

{% swagger-parameter in="body" name="breed" required="false" type="string" %}
The breed of the pet
{% endswagger-parameter %}

{% swagger-response status="200" description="Pet successfully created" %}
```javascript
{
    "name"="Wilson",
    "owner": {
        "id": "sha7891bikojbkreuy",
        "name": "Samuel Passet",
    "species": "Dog",}
    "breed": "Golden Retriever",
}
```
{% endswagger-response %}

{% swagger-response status="401" description="Permission denied" %}

{% endswagger-response %}
{% endswagger %}

{% hint style="info" %}
**Good to know:** You can use the API Method block to fully document an API method. You can also sync your API blocks with an OpenAPI file or URL to auto-populate them.
{% endhint %}

Take a look at how you might call this method using our official libraries, or via `curl`:

{% tabs %}
{% tab title="curl" %}
```
curl https://api.myapi.com/v1/pet  
    -u YOUR_API_KEY:  
    -d name='Wilson'  
    -d species='dog'  
    -d owner_id='sha7891bikojbkreuy'  
```
{% endtab %}

{% tab title="Node" %}
```javascript
// require the myapi module and set it up with your API key
const myapi = require('myapi')(YOUR_API_KEY);

const newPet = away myapi.pet.create({
    name: 'Wilson',
    owner_id: 'sha7891bikojbkreuy',
    species: 'Dog',
    breed: 'Golden Retriever',
})
```
{% endtab %}

{% tab title="Python" %}
```python
// Set your API key before making the request
myapi.api_key = YOUR_API_KEY

myapi.Pet.create(
    name='Wilson',
    owner_id='sha7891bikojbkreuy',
    species='Dog',
    breed='Golden Retriever',
)
```
{% endtab %}
{% endtabs %}