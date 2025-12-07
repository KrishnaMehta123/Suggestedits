---
title: Using Liquid Tags
excerpt: >-
  This section refers to the syntax requirements and types of liquid tags in
  Clevertap.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Liquid Syntax Requirements

To ensure Liquid Tags work correctly within your campaigns, follow these syntax rules:

### Use Correct Delimiters

- **Output Tags**: Wrap variables in double curly braces  
  Example:  
  ```liquid
  {{ Profile.name }}
  ```
- **Logic/Control Tags**: Wrap logic in `{% %}`  
  Example:  
  ```liquid
  {% if Profile.city == "Mumbai" %}
    Hello Mumbaikar!
  {% endif %}
  ```

### Close the Tags

- Every `{% if %}`, `{% for %}`, `{% case %}`, and so on, must be closed with `{% endif %}`, `{% endfor %}`, `{% endcase %}` respectively.
- Incorrect:  
  ```liquid
  {% if Profile.name == "John" %}
    Hi John!
  ```
  Correct:  
  ```liquid
  {% if Profile.name == "John" %}
    Hi John!
  {% endif %}
  ```

### Use Default Filters for Missing Values

Always provide fallback values to avoid blanks in messages:

```liquid
{{ Profile.name | default: "there" }}
```

### Data Type

- Strings must be enclosed in quotes:  
  ```liquid
  {% if Profile.city == "Delhi" %}
  ```
- Numbers must not be enclosed in quotes:  
  ```liquid
  {% if Profile.age > 25 %}
  ```

# Types of Liquid Tags

You can start creating your message by declaring tags in the campaign editor. You can declare the tags in the following ways:

<!DOCTYPE html>

<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

```
/* This hides the right-hand TOC */
.content-toc.grid-25 {
  display: none !important;
}

.grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(300px, 1fr));
  gap: 1rem;
  max-width: 1200px;
  margin: 2rem auto;
  padding: 1rem;
}

.integration-card {
  display: flex;
  align-items: center;
  padding: 1.5rem;
  background: white;
  border-radius: 12px;
  min-width: 200px;
  border: 1px solid rgba(0, 0, 0, 0.1);
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
  transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
  text-decoration: none;
}

.integration-card:hover {
  box-shadow: 0px 7px 10px rgba(0, 0, 0, 0.1);
}

.logo-container {
  display: flex;
  align-items: center;
  padding-right: 1rem;
  border-right: 1px solid rgba(0, 0, 0, 0.1);
  margin-right: 1rem;
}

.logo {
  width: 50px;
  height: 50px;
  object-fit: contain;
  border-radius: 5px;
}

.content {
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.name {
  font-size: 1rem;
  font-weight: 600;
  color: #000;
  margin-bottom: 0.3rem;
}

.category {
  font-size: 0.8rem;
  color: #666;
}

@media (max-width: 768px) {
  .grid {
    grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
  }
}

@media (max-width: 480px) {
  .grid {
    grid-template-columns: 1fr;
  }
}
```

  </style>
</head>
<body>

<div class="grid">

  <!-- Conditional Tags -->

  <a href="https://staging.docs.user.clevertap.net/docs/liquid-tags-use-cases#conditional-tags" class="integration-card">
    <div class="logo-container">
      <img src="https://img.icons8.com/fluency/48/conditional.png" alt="Conditional Tags" class="logo">
    </div>
    <div class="content">
      <div class="name">Conditional Tags</div>
      <div class="category">if, else, switch, loops</div>
    </div>
  </a>

  <!-- Variable Tags -->

  <a href="https://staging.docs.user.clevertap.net/docs/liquid-tags-use-cases#variable-tags" class="integration-card">
    <div class="logo-container">
      <img src="https://img.icons8.com/color/48/code.png" alt="Variable Tags" class="logo">
    </div>
    <div class="content">
      <div class="name">Variable Tags</div>
      <div class="category">assign, reuse, fallback</div>
    </div>
  </a>

  <!-- Theme Tags -->

  <a href="https://staging.docs.user.clevertap.net/docs/liquid-tags-use-cases#theme-tags" class="integration-card">
    <div class="logo-container">
      <img src="https://img.icons8.com/fluency/48/layout.png" alt="Theme Tags" class="logo">
    </div>
    <div class="content">
      <div class="name">Theme Tags</div>
      <div class="category">styling & structure</div>
    </div>
  </a>

  <!-- Operators -->

  <a href="https://staging.docs.user.clevertap.net/docs/liquid-tags-use-cases#operators" class="integration-card">
    <div class="logo-container">
      <img src="https://img.icons8.com/external-flat-icons-inmotus-design/48/external-logic-coding-flat-icons-inmotus-design.png" alt="Operators" class="logo">
    </div>
    <div class="content">
      <div class="name">Operators</div>
      <div class="category">==, !=, or, and, >, <</div>
    </div>
  </a>

  <!-- Output Tags -->

  <a href="https://staging.docs.user.clevertap.net/docs/liquid-tags-use-cases#output-tags" class="integration-card">
    <div class="logo-container">
      <img src="https://img.icons8.com/fluency/48/console.png" alt="Output Tags" class="logo">
    </div>
    <div class="content">
      <div class="name">Output Tags</div>
      <div class="category">{{ show value }}</div>
    </div>
  </a>

</div>

</body>
</html>

## Conditional Tags

Conditional tags allow you to vary message content based on specific conditions. For example, if a user makes a purchase, you can send them a coupon for their next order. These tags use `{% if %} ... {% endif %}` syntax and can dynamically handle simple or complex conditional statements to personalize messages.

Following are the conditional tags:

- if
- else
- else-if
- unless
- switch case
- for
- break
- continue
- abort
- limit
- offset
- tablerow
- now

### If

```text If Tag
{% if Profile.PREFERED_LANGUAGE  == "French"%} 

Bon Jour !

{% endif %}
```

### Else/Elseif

You can send messages conditionally to each recipient. 

```liquid Else/Elseif Tag
{% if Profile.PREFERED_LANGUAGE  == "French"%} 

Bon Jour !

{% elsif  Profile.PREFERED_LANGUAGE  == "Spanish"%} 

Hola!

{% else %}

Hello!

{% endif %}
```

If the user's preferred language is French, the greeting will appear in French.  If the user's preferred language is Spanish, the greeting will appear in Spanish. However, if the preferred language is anything other than French and Spanish, then the greeting will appear in English. 

```text Output - Else/Elseif
Hello!
```

You can display different messages based on the value of an Event Property (for example, Requested Product). Here is an example demonstrating the syntax for using Event Properties in Liquid Tags:

```liquid Else/Elseif Tag
{% if Event["Requested Product"] == "Personal Loan" %}
You selected **Personal Loan**. Here's what you need to know about it.
  
{% elsif Event["Requested Product"] == "Car Title Loan" %}
You selected **Car Title Loan**. Let's get started with your application.
  
{% else %}
It seems like we couldn't determine your requested product. Please try again.
{% endif %}
```

### Unless

You can use this tag if a condition is not true. For example, if a user's language is "not" French, then greet with "Hello" in English. 

```liquid Unless Tag
{% unless Profile.PREFERED_LANGUAGE  == "French"%} 

Hello!

{% endunless %}
```

The message display will be as follows:

```text Output - Unless
Hello!
```

### Switch case

You can switch a statement when a variable changes in value.  The `when` statements define the various conditions. For example, you have three types of customers, namely "Gold", "Silver" and "Others". They are represented by the profile property "customer_type".  You can change the displayed message based on the type of customers. 

```liquid Switch case Tag
{% case Profile.customer_type %}
  {% when "Gold" %}
     You are eligible for free lounge access!
  {% when "Silver" %}
     You are eligible for lounge access at only 50% of the cost!
  {% else %}
     Upgrade your membership now for free lounge access!
{% endcase %}
```

```text Output - Switch case
Upgrade your membership now for free lounge access!
```

### for

You can repeat execution in liquid script with the for loop.

```liquid for Tag
{% for item in hiking.items %}
  {{ item.names | default: "NA"}}
{% endfor %}
```

```text Output - For Tag
flashlight  backpack boots
```

### break

You can stop execution in the liquid script by adding a break in a loop.

```liquid Break - Tag
{% for i in (1..10) %}
  {% if i == 7 %}
    {% break %}
  {% else %}
    {{ i | default: "NA" }}
  {% endif %}
{% endfor %}
```

```text Output - Break
1 2 3 4 5 6
```

### continue

You can skip the current iteration in a loop with the continue tag.

```liquid continue - Tag
{% for i in (1..10) %}
  {% if i == 7 %}
    {% continue %}
  {% else %}
    {{ i | default: "NA"}}
  {% endif %}
{% endfor %}
```

```text output - continue
1 2 3 4 5 6   8 9 10
```

### abort

This is a CleverTap Tag within Liquid. You can abort sending a message with the abort tag. If a condition is not fulfilled for a user, it is displayed in the campaign reports as `LiquidLogicAborted`.

```liquid abort - Tag
{% if Event.price > 100%}
Thank you for your purchase. Here is a coupon code for you. 
COUPON
{% else %}
{% abort %}
{% endif %}
```

```text output - abort
Thank you for your purchase. Here is a coupon code for you. 
COUPON
```

### limit

You can specify the limit of the for loop with this tag. 

```liquid limit - Tag
<!-- if array = [1,2,3,4,5,6] -->
{% for item in array limit:2 %}
  {{ item | default: "NA" }}
{% endfor %}
```

```text output - limit
1 2
```

### offset

You can begin the loop at a specified index.

```liquid offset - Tag
<!-- if array = [1,2,3,4,5,6] -->
{% for item in array offset:2 %}
  {{ item | default: "NA" }}
{% endfor %}
```

```text output - offset
3 4 5 6
```

### tablerow

You can generate an HTML table with this tag. It must be wrapped in opening `<table>` and closing `</table>` HTML tags. 

```liquid tablerow - Tag
<table>
{% tablerow product in Profile.multi %}
{{ product | default: "def" }}
{% endtablerow %}
</table>
```

```text output - Tag
<table>
  <tr class="row1">
    <td class="col1">
      Cool Shirt
    </td>
    <td class="col2">
      Alien Poster
    </td>
    <td class="col3">
      Batman Poster
    </td>
    <td class="col4">
      Bullseye Shirt
    </td>
    <td class="col5">
      Another Classic Vinyl
    </td>
    <td class="col6">
      Awesome Jeans
    </td>
  </tr>
</table>
```

### now

Using this tag, you can insert the current date and time in the specified format.

```Text now - tag
{{ "now" | date: "%Y-%m-%d %H:%M" }}

```

## Variable Tags

You can use Variable tags to store dynamic data within messages. They allow you to assign values or modify content using Liquid variables. 

### Assign

You can use the `assign` tag to assign value to a variable. The value of this variable can change based on the defined condition or a range. You can then reuse this variable across your message. 

For example, you want to greet a user in French. You create a variable called `LANG`. Now, you can use this variable for all available languages. If the value of the `LANG` variable is French, the greeting is "Bonjour!". The greeting is "Hello!" for all other languages. 

```liquid Assign Variable Tag
{% assign LANG = PROFILE.PREFERED_LANGUAGE %}
{% if LANG == "FRENCH" %}
Bonjour!
{% else %}
Hello!
{% endif %}
```

## Theme Tags

Theme tags define styling, layout, and reusable templates within messages. They are used to apply consistent branding and design elements across multiple communications. Example: `{% include 'header' %}` inserts a predefined header template into the message.

### Raw

You can use the raw tag to display characters used by the tag syntax. 

```liquid Raw Tag
{% raw %}{{ 5 | plus: 6 }}{% endraw %} equals 11.
```

```text Output - raw
{{ 5 | plus: 6 }} equals 11.
```

### Comment

You can comment on your code with this tag. It can be notes or descriptions that you want to add to make your code more understandable. 

```liquid Comment Tag
{% if Profile.PREFERED_LANGUAGE  == "French"%} 

{% comment %} This condition is only fulfilled if the value is 
French {% endcomment %}

Bonjour!

{% endif %}
```

```text Output - Comment
Bonjour!
```

## Output tags

You can use Output tags to display the output of a variable. They are enclosed in double curly braces `{{ ... }}` and can be combined with filters to modify output. For example, `{{ user.name | default: 'there' }}` dynamically personalizes the message by greeting the user by name or defaulting to "there" if the name is unavailable.

## Operators

Operators in Liquid Tags perform comparisons and logical evaluations within conditions. You can use the following operators to evaluate conditions in your tags.

| Operator     | Description                                                |
| :----------- | :--------------------------------------------------------- |
| **==**       | equals                                                     |
| **!=**       | does not equal                                             |
| **>**        | greater than                                               |
| **\<**       | less than                                                  |
| **>=**       | greater than or equal to                                   |
| **\<=**      | less than or equal to                                      |
| **or**       | logical or. Choose between condition one or condition two. |
| **and**      | logical and. Choose conditions one and two.                |
| **contains** | check for a string within a string                         |