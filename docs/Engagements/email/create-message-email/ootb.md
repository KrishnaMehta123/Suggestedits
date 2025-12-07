---
title: Email Templates
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Overview

Here’s an improved and more engaging overview for your **CleverTap HTML Email Templates – Template Overview** section:

(@Krishna - provide a common intro here for OOTB templates.)

# HTML Templates

This section provides a comprehensive overview of all HTML email templates available in CleverTap. Each template is designed for a specific use case—from onboarding and re-engagement to promotions and transactional updates—helping marketing and design teams quickly identify the best fit for their campaign goals.

Alongside each use case, you’ll find a breakdown of customizable components like logos, banners, CTAs, product grids, and theme colors. This ensures easy editing and brand consistency across campaigns. Whether you're launching a birthday offer, confirming an order, or showcasing a flash sale, this guide gives you the structure and flexibility to build beautiful, conversion-ready emails in minutes.

## Birthday Template

<br />

| Template Name     | Description                                                                                     | Use case                                                                                        | Components                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| :---------------- | :---------------------------------------------------------------------------------------------- | :---------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Birthday Template | A celebratory template designed to acknowledge a customer’s birthday and make them feel valued. | A celebratory template designed to acknowledge a customer’s birthday and make them feel valued. | <li> [Replace the Logo](doc:ootb#1-replace-the-logo) </li><li>[Update Banner/Product Images](doc:ootb#2-update-bannerproduct-images)</li> <li> [Update Call-To-Actions (CTAs)](https://staging.docs.user.clevertap.net/docs/ootb#3-call-to-actions-ctas) </li> <li>[Update Links in the Header/Footer](doc:ootb#4-update-links-in-the-headerfooter) </li> <li>[Change the Theme or Background Color](doc:ootb#5-change-the-theme-or-background-color)</li>  <li>[Update Social Media Links and Download Links](doc:ootb#update-social-media-links-and-download-links)</li> |

<br />

<details>

<summary><b>Birthday Template Sample HTML</b></summary>

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Birthday</title>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <style>
      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Light.ttf') format('woff');
        font-style: normal;
        font-weight: 300;
      }
      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Regular.ttf') format('woff');
        font-style: normal;
        font-weight: 400;
      }
      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Medium.ttf') format('woff');
        font-style: normal;
        font-weight: 500;
      }
      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-SemiBold.ttf') format('woff');
        font-style: normal;
        font-weight: 600;
      }
      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Bold.ttf') format('woff');
        font-style: normal;
        font-weight: 700;
      }

      @media screen and (max-width: 480px) {
        .container {
          max-width: 95% !important;
        }
        .logo {
          width: 150px !important;
          height: 60px !important;
        }
        .offer-wrap {
          padding: 40px 15px !important;
        }
        .offer-title {
          font-size: 35px !important;
          line-height: 45px !important;
        }
        .cta {
          padding: 10px 25px !important;
        }
      }
    </style>
  </head>
  <body style="font-family: 'Jost', Arial, sans-serif; font-weight: 400; margin: 0; padding: 0; background: aliceblue;">
    <table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%" style="max-width: 600px; margin: 0 auto; background-color: #FFFFFF;">
      <!-- header start -->
      <tr>
        <td align="center" style="display: block; padding: 24px 0; max-width: 90%; margin: 0 auto;" class="container">
          <div class="logo-wrap">
            <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Birthday/logo.png" alt="Logo" class="logo" style="width: 159px; height: 73px; object-fit: cover;" />
          </div>
        </td>
      </tr>
      <!-- Banner -->
      <tr>
        <td style="text-align: center;">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Birthday/banner.png" alt="Banner" style="width: 100%; height: auto;" />
        </td>
      </tr>

      <!-- Offer Section -->
      <tr>
        <td style="padding: 50px 30px;" class="offer-wrap">
          <h1 class="offer-title" style="font-size: 45px; font-weight: 600; text-align: center; color: #252525; margin: 0;">
            Happy Birthday!
          </h1>
          <p style="text-align: center; font-size: 18px; font-weight: 400; line-height: 30px; margin-top: 15px; color: #252525;">
            We’ve got something special for you. Here’s a little birthday treat from us to make your day even more delightful!
          </p>
        </td>
      </tr>

      <!-- Discount Code -->
      <tr>
        <td align="center" style="padding: 0 30px;">
          <table style="width: 100%; text-align: center;">
            <tr>
              <td style="background: #f3f3f3; padding: 20px 0; border: 2px dashed #ac8763;">
                <p style="margin: 0; font-size: 18px; font-weight: 500; letter-spacing: 2px; color: #000;">BDAY20</p>
              </td>
            </tr>
          </table>
        </td>
      </tr>

      <!-- CTA -->
      <tr>
        <td style="text-align: center; padding: 30px;">
          <a href="#" class="cta" style="text-decoration: none; background: #ac8763; padding: 12px 50px; color: #fff; font-size: 14px; text-transform: uppercase; display: inline-block;">Claim Now</a>
        </td>
      </tr>
      <!-- Validity Note -->
      <tr>
        <td align="center" style="padding: 0 30px;">
          <p style="font-size: 28px; font-weight: 600; color: #252525; margin: 0;">
            Valid till: 30th April 2025
          </p>
          <p style="font-size: 12px; font-weight: 400; color: #7a7a7a; line-height: 22px; margin-top: 5px;">
            Offer valid on selected items only. T&C apply.
          </p>
        </td>
      </tr>

      <!-- Divider -->
      <tr>
        <td style="padding: 40px 0;">
          <hr style="border: none; border-top: 1px solid #d8d8d8; width: 80%; margin: 0 auto;" />
        </td>
      </tr>

      <!-- Footer -->
      <tr>
        <td style="background-color: #1e1e1e; text-align: center; padding: 30px 0;">
          <!-- Social Icons -->
          <a href="#" style="margin: 0 10px;">
            <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Birthday/logo-insta.png" width="20" alt="Instagram" />
          </a>
          <a href="#" style="margin: 0 10px;">
            <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Birthday/logo-facebook.png" width="20" alt="Facebook" />
          </a>
          <a href="#" style="margin: 0 10px;">
            <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Birthday/logo-x.png" width="20" alt="Twitter" />
          </a>
          <!-- Footer Text -->
          <p style="color: #ffffff; font-size: 14px; line-height: 24px; margin-top: 20px; font-weight: 400;">
            is simply dummy text of the printing and typesetting industry.
          </p>

          <p style="color: #ffffff; font-size: 14px; font-weight: 400; margin-top: 5px;">
            To stop receiving these emails,
            <a href="#" style="color: #ffffff; font-weight: bold; text-decoration: underline;">unsubscribe here</a>
          </p>
        </td>
      </tr>

      <!-- Fallback for Button -->
      <tr>
        <td style="padding: 20px; text-align: center;">
          <p style="font-size: 12px; color: #7a7a7a;">
            If you're having trouble clicking the "Claim Now" button, copy and paste this URL into your browser:
            <br />
            <a href="#" style="color: #ac8763;">https://yourbrand.com/birthday</a>
          </p>
        </td>
      </tr>
    </table>
  </body>
</html>

```

</details>

***

## Feedback Template

A post-interaction follow-up template used to collect user opinions and improve service quality.

**Use Case:** Collects customer feedback after interaction or purchase to improve product or service offerings.

**Components:**

- [Replace the Logo](doc:ootb#1-replace-the-logo)
- [Update Banner/Product Images](doc:ootb#2-update-bannerproduct-images)
- [Update Call-To-Actions (CTAs)](https://staging.docs.user.clevertap.net/docs/ootb#3-call-to-actions-ctas)
- [Update Links in the Header/Footer](doc:ootb#4-update-links-in-the-headerfooter)
- [Change the Theme or Background Color](doc:ootb#5-change-the-theme-or-background-color)
- [Update the Privacy Policy](doc:ootb#update-the-privacy-policy)

### Template Code

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Feedback</title>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <style>
      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Regular.ttf') format('woff');
        font-style: normal;
        font-weight: 400;
      }

      @media screen and (max-width: 480px) {
        .container {
          max-width: 90% !important;
        }
        .logo {
          width: 150px !important;
          height: 60px !important;
        }
        .cta {
          padding: 10px 25px !important;
        }
      }
    </style>
  </head>
  <body style="font-family: 'Jost', Arial, sans-serif; font-weight: 400; margin: 0; padding: 0;">
    <!-- Change Theme -->
    <table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%"
      style="max-width: 600px; margin: 0 auto; background-color: #FFFFFF; border-spacing: 0 !important;">
      <!-- Header -->
      <tr>
        <td align="center" style="display: block; padding: 20px 0; max-width: 90%; margin: 0 auto;" class="container">
          <div class="logo-wrap">
            <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/feedback-html/logo.png"
              alt="Logo" class="logo" style="width: 159px; height: 73px; object-fit: cover;" />
          </div>
        </td>
      </tr>
      <!-- Banner -->
      <tr>
        <td style="text-align: center;">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/feedback-html/banner.png"
            alt="Feedback Banner" style="width: 100%; height: auto;" />
        </td>
      </tr>

      <!-- Message -->
      <tr>
        <td style="padding: 40px 30px; text-align: center;">
          <h1 style="font-size: 28px; font-weight: 600; color: #252525; margin: 0;">We Value Your Feedback!</h1>
          <p style="font-size: 16px; color: #4f4f4f; line-height: 26px; margin-top: 15px;">
            Let us know how we’re doing and help us improve. Your opinion matters!
          </p>
        </td>
      </tr>

      <!-- CTA -->
      <tr>
        <td style="text-align: center; padding: 20px;">
          <a href="#" class="cta"
            style="text-decoration: none; background: #ac8763; padding: 12px 40px; color: #fff; font-size: 14px; text-transform: uppercase; display: inline-block;">
            Share Feedback
          </a>
        </td>
      </tr>
      <!-- Optional Note -->
      <tr>
        <td style="padding: 0 30px; text-align: center;">
          <p style="font-size: 12px; font-weight: 400; color: #7a7a7a; line-height: 22px;">
            It only takes a minute and helps us serve you better.
          </p>
        </td>
      </tr>

      <!-- Divider -->
      <tr>
        <td style="padding: 40px 0;">
          <hr style="border: none; border-top: 1px solid #d8d8d8; width: 80%; margin: 0 auto;" />
        </td>
      </tr>

      <!-- Footer -->
      <tr>
        <td style="background-color: #1e1e1e; text-align: center; padding: 30px 0;">
          <!-- Social Icons -->
          <a href="#" style="margin: 0 10px;">
            <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/feedback-html/logo-insta.png" width="20" alt="Instagram" />
          </a>
          <a href="#" style="margin: 0 10px;">
            <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/feedback-html/logo-facebook.png" width="20" alt="Facebook" />
          </a>
          <a href="#" style="margin: 0 10px;">
            <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/feedback-html/logo-x.png" width="20" alt="Twitter/X" />
          </a>
          <!-- Footer Text -->
          <p style="color: #ffffff; font-size: 14px; line-height: 24px; margin-top: 20px; font-weight: 400;">
            is simply dummy text of the printing and typesetting industry.
          </p>

          <p style="color: #ffffff; font-size: 14px; font-weight: 400; margin-top: 5px;">
            To stop receiving these emails,
            <a href="#" style="color: #ffffff; font-weight: bold; text-decoration: underline;">unsubscribe here</a>
          </p>
        </td>
      </tr>

      <!-- Fallback CTA Note -->
      <tr>
        <td style="padding: 20px; text-align: center;">
          <p style="font-size: 12px; color: #7a7a7a;">
            If you're having trouble clicking the "Share Feedback" button, copy and paste this URL into your browser:
            <br />
            <a href="#" style="color: #ac8763;">https://yourdomain.com/feedback</a>
          </p>
        </td>
      </tr>
    </table>
  </body>
</html>
```

## First Purchase Incentive Template

A promotional email that incentivizes users to make their first purchase using a discount or limited-time offer.

**Use Case:** Encourages new users to make their first purchase by offering a limited-time coupon or discount.

**Components:**

- [Replace the Logo](doc:ootb#1-replace-the-logo)
- [Update Banner/Product Images](doc:ootb#2-update-bannerproduct-images)
- [Update Call-To-Actions (CTAs)](https://staging.docs.user.clevertap.net/docs/ootb#3-call-to-actions-ctas)
- [Update Links in the Header/Footer](doc:ootb#4-update-links-in-the-headerfooter)
- [Change the Theme or Background Color](doc:ootb#5-change-the-theme-or-background-color)
- [Update the Privacy Policy](doc:ootb#update-the-privacy-policy)
- [Update Social Media Links and Download Links](doc:ootb#update-social-media-links-and-download-links)

### Template Code

```html
<!doctype html>
<html lang="en">
  <head>
    <title>First Purchase Incentive</title>
    <style type="text/css">
      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Light.ttf') format('woff');
        font-style: normal;
        font-weight: 300;
      }

      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Regular.ttf') format('woff');
        font-style: normal;
        font-weight: 400;
      }

      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Medium.ttf') format('woff');
        font-style: normal;
        font-weight: 500;
      }

      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-SemiBold.ttf') format('woff');
        font-style: normal;
        font-weight: 600;
      }

      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Bold.ttf') format('woff');
        font-style: normal;
        font-weight: 700;
      }

      @media screen and (max-width: 480px) {
        .container { max-width: 100% !important; }
        .content { max-width: 90% !important; }
        .cta { padding: 5px !important; font-size: 10px !important; }
        .logo { width: 110px !important; height: 50px !important; }
      }
    </style>
  </head>
  <body>
    <!-- Change Theme -->
    <table border="0" cellpadding="0" cellspacing="0" role="presentation" width="100%" style="max-width: 600px; margin: 0 auto; background-color: #ffffff; font-family: Jost, Arial, sans-serif; font-weight: 400;">
      <tbody>
        <tr>
          <td align="center" style="padding: 15px 0;">
            <img alt="Logo" class="logo" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/first_purchase_incentive/logo.png" style="width: 145px; height: 60px; object-fit: cover;" />
          </td>
        </tr>
        <tr>
          <td>
            <img alt="Banner" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/first_purchase_incentive/banner.png" style="width: 100%; height: auto;" />
          </td>
        </tr>

        <tr>
          <td class="content" style="text-align: center; padding: 40px 30px;">
            <h1 style="font-size: 35px; font-weight: 600; color: #252525; margin: 0 0 20px;">Here’s 10% off your first order!</h1>
            <p style="font-size: 16px; color: #4f4f4f; line-height: 26px; margin: 0;">
              Thanks for signing up! Use this special welcome discount to shop your favorites.
            </p>
          </td>
        </tr>

        <tr>
          <td align="center" style="padding: 20px 30px;">
            <table border="0" cellpadding="0" cellspacing="0" style="background: #f3f3f3; border: 2px dashed #ac8763; padding: 15px 30px;">
              <tr>
                <td style="font-size: 18px; font-weight: 600; letter-spacing: 2px; color: #252525; text-align: center;">
                  WELCOME10
                </td>
              </tr>
            </table>
          </td>
        </tr>

        <tr>
          <td align="center" style="padding-top: 30px;">
            <a href="#" class="cta" style="background: #ac8763; padding: 12px 40px; color: #fff; font-size: 14px; text-transform: uppercase; text-decoration: none; display: inline-block;">Shop Now</a>
          </td>
        </tr>
        <tr>
          <td align="center" style="padding: 30px 30px 0;">
            <p style="font-size: 12px; font-weight: 400; color: #7a7a7a; line-height: 22px;">
              Valid on your first purchase only. Cannot be combined with other offers. T&C apply.
            </p>
          </td>
        </tr>

        <tr>
          <td style="padding: 40px 0;">
            <hr style="border: none; border-top: 1px solid #d8d8d8; width: 80%; margin: 0 auto;" />
          </td>
        </tr>

        <tr>
          <td style="background-color: #1e1e1e; text-align: center; padding: 30px 0;">
            <!-- Social Icons -->
            <a href="#" style="margin: 0 10px;">
              <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/first_purchase_incentive/logo-insta.png" width="20" alt="Instagram" />
            </a>
            <a href="#" style="margin: 0 10px;">
              <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/first_purchase_incentive/logo-facebook.png" width="20" alt="Facebook" />
            </a>
            <a href="#" style="margin: 0 10px;">
              <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/first_purchase_incentive/logo-x.png" width="20" alt="Twitter/X" />
            </a>
            <!-- Footer Text -->
            <p style="color: #ffffff; font-size: 14px; line-height: 24px; margin-top: 20px; font-weight: 400;">
              is simply dummy text of the printing and typesetting industry.
            </p>

            <p style="color: #ffffff; font-size: 14px; font-weight: 400; margin-top: 5px;">
              To stop receiving these emails,
              <a href="#" style="color: #ffffff; font-weight: bold; text-decoration: underline;">unsubscribe here</a>
            </p>
          </td>
        </tr>

        <!-- Fallback for CTA -->
        <tr>
          <td style="padding: 20px; text-align: center;">
            <p style="font-size: 12px; color: #7a7a7a;">
              If you're having trouble clicking the "Shop Now" button, copy and paste this URL into your browser:
              <br />
              <a href="#" style="color: #ac8763;">https://yourbrand.com/first-purchase</a>
            </p>
          </td>
        </tr>
      </tbody>
    </table>
  </body>
</html>
```

## Flash Sale Template

A high-conversion template designed to build urgency around a limited-time offer or flash sale.

**Use Case:** Promotes limited-time sales with urgency-driven elements like countdown timers to drive quick conversions.

**Components:**

- [Replace the Logo](doc:ootb#1-replace-the-logo)
- [Update Banner/Product Images](doc:ootb#2-update-bannerproduct-images)
- [Update Call-To-Actions (CTAs)](https://staging.docs.user.clevertap.net/docs/ootb#3-call-to-actions-ctas)
- [Update Links in the Header/Footer](doc:ootb#4-update-links-in-the-headerfooter)
- [Change the Theme or Background Color](doc:ootb#5-change-the-theme-or-background-color)
- [Update the Privacy Policy](doc:ootb#update-the-privacy-policy)
- [Update Social Media Links and Download Links](doc:ootb#update-social-media-links-and-download-links)
- [Configure the Countdown Timer](doc:ootb#countdown-timer-flash-sale-only)

```html HTML
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Flash Sale</title>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <style>
      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Light.ttf') format('woff');
        font-style: normal;
        font-weight: 300;
      }

      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Regular.ttf') format('woff');
        font-style: normal;
        font-weight: 400;
      }

      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Medium.ttf') format('woff');
        font-style: normal;
        font-weight: 500;
      }

      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-SemiBold.ttf') format('woff');
        font-style: normal;
        font-weight: 600;
      }

      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Bold.ttf') format('woff');
        font-style: normal;
        font-weight: 700;
      }

      @media only screen and (max-width: 480px) {
        .container { max-width: 100% !important; }
        .product-container, .footer-wrap, .content { max-width: 95% !important; }
        .content-wrap { width: 60% !important; }
        .btn-wrap { width: 40% !important; }
        .flash-detail-wrap { height: 140px !important; padding: 0px 20px !important; }
        .img-wrap { height: 95px !important; width: 100% !important; }
        .logo { max-width: 130px !important; }
        .cta { padding: 5px 15px !important; }
        .media-item { padding: 0 20px !important; }
      }

      @media only screen and (max-width: 360px) {
        .img-wrap {
          height: 80px !important;
          width: 100% !important;
        }
      }
    </style>
  </head>
  <body style="font-family: 'Jost', Arial, sans-serif; font-weight: 400; margin: 0; padding: 0;">
    <table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%" style="max-width: 600px; margin: 0 auto; background-color: #FFFFFF;">
      <!-- Header Logo -->
      <tr>
        <td align="center" style="padding: 24px 0;" class="container">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/FlashSale/logo.png"
               alt="Logo" class="logo" style="width: 159px; height: 73px; object-fit: cover;" />
        </td>
      </tr>

      <!-- Hero Banner -->
      <tr>
        <td style="text-align: center;">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/FlashSale/banner.png"
               alt="Flash Sale Banner" style="width: 100%; height: auto;" />
        </td>
      </tr>

      <!-- Countdown Timer -->
      <tr>
        <td align="center" style="padding: 24px 0;">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/FlashSale/timer.gif"
               alt="Countdown Timer" style="width: 85%; height: auto;" />
        </td>
      </tr>

      <!-- Flash Sale Message -->
      <tr>
        <td style="padding: 0 30px;">
          <h1 style="font-size: 36px; font-weight: 600; color: #252525; margin: 0 0 15px; text-align: center;">
            Flash Sale is Live Now!
          </h1>
          <p style="font-size: 16px; color: #4f4f4f; text-align: center; line-height: 26px; margin: 0;">
            Enjoy exclusive discounts for the next few hours only. Shop your favorites before time runs out!
          </p>
        </td>
      </tr>
      <!-- CTA Button -->
      <tr>
        <td style="text-align: center; padding: 30px 0;">
          <a href="#" class="cta"
             style="text-decoration: none; background: #ac8763; padding: 12px 50px; color: #fff; font-size: 14px; text-transform: uppercase; display: inline-block;">
            Shop Now
          </a>
        </td>
      </tr>

      <!-- Divider -->
      <tr>
        <td style="padding: 40px 0;">
          <hr style="border: none; border-top: 1px solid #d8d8d8; width: 80%; margin: 0 auto;" />
        </td>
      </tr>

      <!-- Footer -->
      <tr>
        <td style="background-color: #1e1e1e; text-align: center; padding: 30px 0;">
          <!-- Social Icons -->
          <a href="#" style="margin: 0 10px;">
            <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/FlashSale/logo-insta.png" width="20" alt="Instagram" />
          </a>
          <a href="#" style="margin: 0 10px;">
            <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/FlashSale/logo-facebook.png" width="20" alt="Facebook" />
          </a>
          <a href="#" style="margin: 0 10px;">
            <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/FlashSale/logo-x.png" width="20" alt="Twitter/X" />
          </a>
          <!-- Footer Text -->
          <p style="color: #ffffff; font-size: 14px; line-height: 24px; margin-top: 20px; font-weight: 400;">
            is simply dummy text of the printing and typesetting industry.
          </p>

          <p style="color: #ffffff; font-size: 14px; font-weight: 400; margin-top: 5px;">
            To stop receiving these emails,
            <a href="#" style="color: #ffffff; font-weight: bold; text-decoration: underline;">unsubscribe here</a>
          </p>
        </td>
      </tr>

      <!-- Fallback for CTA -->
      <tr>
        <td style="padding: 20px; text-align: center;">
          <p style="font-size: 12px; color: #7a7a7a;">
            If you're having trouble clicking the "Shop Now" button, copy and paste this URL into your browser:
            <br />
            <a href="#" style="color: #ac8763;">https://yourbrand.com/flash-sale</a>
          </p>
        </td>
      </tr>
    </table>

    <!-- Background Wrapper End -->
  </body>
</html>
```

## Cart Abandonment Template

A re-engagement email aimed at reminding users of unpurchased items left in their cart.

### Use Case Examples

Re-engages users who have added items to their cart but did not complete the purchase. Encourages conversion with reminders and product imagery.

### Template Customization Options

- [Replace the Logo](doc:ootb#1-replace-the-logo)
- [Update Banner/Product Images](doc:ootb#2-update-bannerproduct-images)
- [Update Call-To-Actions (CTAs)](https://staging.docs.user.clevertap.net/docs/ootb#3-call-to-actions-ctas)
- [Update Links in the Header/Footer](doc:ootb#4-update-links-in-the-headerfooter)
- [Change the Theme or Background Color](doc:ootb#5-change-the-theme-or-background-color)
- [Update the Privacy Policy](doc:ootb#update-the-privacy-policy)
- [Update Social Media Links and Download Links](doc:ootb#update-social-media-links-and-download-links)

### Template Code

```html HTML
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Cart Abandonment</title>
    <style type="text/css">
      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Light.ttf') format('woff');
        font-weight: 300;
      }

      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Regular.ttf') format('woff');
        font-weight: 400;
      }

      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Medium.ttf') format('woff');
        font-weight: 500;
      }

      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-SemiBold.ttf') format('woff');
        font-weight: 600;
      }

      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Bold.ttf') format('woff');
        font-weight: 700;
      }

      @media screen and (max-width: 480px) {
        .container {
          max-width: 100% !important;
        }

        .main {
          max-width: 90% !important;
        }

        .look-sec {
          padding-top: 30px !important;
        }

        .sec-head {
          max-width: 65% !important;
        }

        .cta {
          font-size: 10px !important;
          padding: 5px !important;
        }
      }
    </style>
  </head>
  <body style="font-family: Jost, Arial, sans-serif; font-weight: 400; margin: 0px; padding: 0px;">
    <!-- Change Theme -->
    <table
      border="0"
      cellpadding="0"
      cellspacing="0"
      class="container"
      role="presentation"
      style="max-width: 600px; margin: 0 auto; background-color: #ffffff;"
      width="100%"
    >
      <!-- header start-->
      <tbody>
        <tr>
          <td style="text-align: left; vertical-align: middle; padding: 20px">
            <!-- Change Logo Image src as per your requirements -->
            <img
              alt="Logo"
              class="logo"
              src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/logo.png"
              style="display: inline-block; width: 127px; height: 58px; object-fit: cover;"
            />
          </td>
          <td style="text-align: right; vertical-align: middle; padding: 20px">
            <div class="head-nav">
              <img
                alt="call icon"
                src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/call-icon.png"
                style="width: 20px; height: 20px; display: inline-block; vertical-align: middle;"
              />
              <span
                style="
                  font-family: 'Jost', Arial, sans-serif;
                  font-size: 14px;
                  font-weight: 400;
                  line-height: 24px;
                  text-align: center;
                  color: #464646;
                  display: inline-block;
                  vertical-align: middle;
                "
                >9878725637</span
              >
            </div>
          </td>
        </tr>
        <!-- header end-->
        <!-- Banner -->
        <tr>
          <td colspan="2">
            <img
              src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/banner.png"
              alt="Banner"
              style="width: 100%; max-height: 361px;"
            />
          </td>
        </tr>

        <!-- Products Section -->
        <tr>
          <td colspan="2">
            <div class="look-sec" style="padding-top: 50px;">
              <h2
                class="sec-head"
                style="
                  border-bottom: 1px solid #000;
                  max-width: 120px;
                  margin: 0 auto;
                  font-size: 20px;
                  font-weight: 400;
                  text-align: center;
                "
              >
                Products
              </h2>

              <!-- Product Card 1 -->
              <div class="look-card" style="padding: 50px 0px 0px; width: 100%; max-width: 300px; margin: 0 auto;">
                <div style="background: #f1f1f1; padding: 20px; text-align: center;">
                  <img
                    src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/look-1.png"
                    style="width: 100%;"
                  />
                  <h2
                    style="font-size: 20px; color: #252525; font-weight: 600; margin: 12px 0px 8px 0px;"
                  >
                    Product Name
                  </h2>
                  <p style="font-style: italic; font-size: 22px;">₹1500</p>
                  <p
                    style="font-size: 10px; color: #545454; font-weight: 400; line-height: 16px;"
                  >
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod.
                  </p>
                  <a
                    href="#"
                    class="cta"
                    style="
                      display: inline-block;
                      padding: 8px 34px;
                      background: #000;
                      color: #fff;
                      text-transform: uppercase;
                      font-size: 14px;
                      text-decoration: none;
                      margin-top: 10px;
                    "
                    >Add to Cart</a
                  >
                </div>
              </div>

              <!-- Add more product cards below as needed -->
            </div>
          </td>
        </tr>

        <!-- Product Suggestions Section -->
        <tr>
          <td colspan="2">
            <div style="background: #f1f1f1; padding: 30px 0px;">
              <h2
                style="
                  font-size: 20px;
                  font-weight: 400;
                  text-align: center;
                  padding-bottom: 20px;
                "
              >
                Product Suggestions
              </h2>

              <table role="presentation" width="100%" cellpadding="0" cellspacing="0">
                <tr>
                  <!-- Product Suggestion 1 -->
                  <td style="text-align: center;" width="33%">
                    <img
                      src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/product-1.png"
                      style="width: 100%; max-width: 140px;"
                    />
                    <h4 style="margin: 5px 0;">Product name</h4>
                    <p style="font-size: 10px;">₹1500</p>
                  </td>

                  <!-- Product Suggestion 2 -->
                  <td style="text-align: center;" width="33%">
                    <img
                      src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/product-2.png"
                      style="width: 100%; max-width: 140px;"
                    />
                    <h4 style="margin: 5px 0;">Product name</h4>
                    <p style="font-size: 10px;">₹1500</p>
                  </td>

                  <!-- Product Suggestion 3 -->
                  <td style="text-align: center;" width="33%">
                    <img
                      src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/product-3.png"
                      style="width: 100%; max-width: 140px;"
                    />
                    <h4 style="margin: 5px 0;">Product name</h4>
                    <p style="font-size: 10px;">₹1500</p>
                  </td>
                </tr>
              </table>

              <div style="text-align: right; padding-top: 10px; padding-right: 15px;">
                <a
                  href="#"
                  style="text-decoration: none; color: #000; font-size: 12px;"
                  >Shop More →</a
                >
              </div>
            </div>
          </td>
        </tr>
        <!-- Footer Section -->
        <tr>
          <td colspan="2">
            <div
              style="
                padding: 32px 0px;
                background: #1e1e1e;
                text-align: center;
              "
            >
              <!-- Social Media Icons -->
              <a href="#" style="margin: 0 10px;">
                <img
                  src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/logo-insta.png"
                  width="20"
                  alt="Instagram"
                />
              </a>
              <a href="#" style="margin: 0 10px;">
                <img
                  src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/logo-facebook.png"
                  width="20"
                  alt="Facebook"
                />
              </a>
              <a href="#" style="margin: 0 10px;">
                <img
                  src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/logo-x.png"
                  width="20"
                  alt="Twitter"
                />
              </a>

              <!-- Footer Text -->
              <p
                style="
                  color: #ffffff;
                  font-size: 14px;
                  margin-top: 20px;
                  font-weight: 400;
                "
              >
                is simply dummy text of the printing and typesetting industry.
              </p>

              <p
                style="
                  color: #ffffff;
                  font-size: 14px;
                  font-weight: 400;
                  margin-top: 5px;
                "
              >
                To stop receiving these emails,
                <a
                  href="#"
                  style="color: #ffffff; font-weight: bold; text-decoration: underline;"
                  >unsubscribe here</a
                >
              </p>
            </div>
          </td>
        </tr>
      </tbody>
    </table>
  </body>
</html>

```

## Access to Early Sales Template

An exclusive offer template that gives early access to select customers before the sale opens publicly.

**Use Case:** Offers select users early access to sales or exclusive product launches to create a feeling of privilege and drive early conversions.

**Components:**

- [Replace the Logo](doc:ootb#1-replace-the-logo)
- [Update Banner/Product Images](doc:ootb#2-update-bannerproduct-images)
- [Update Call-To-Actions (CTAs)](https://staging.docs.user.clevertap.net/docs/ootb#3-call-to-actions-ctas)
- [Update Links in the Header/Footer](doc:ootb#4-update-links-in-the-headerfooter)
- [Change the Theme or Background Color](doc:ootb#5-change-the-theme-or-background-color)
- [Update the Privacy Policy](doc:ootb#update-the-privacy-policy)
- [Update Social Media Links and Download Links](doc:ootb#update-social-media-links-and-download-links)

```html HTML
<!DOCTYPE html>
<html lang="en">
<head>
  <title>Access to early sale</title>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta http-equiv="X-UA-Compatible" content="IE=edge" />
  <style>
    @font-face {
      font-family: 'Jost';
      src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Light.ttf') format('woff');
      font-weight: 300;
    }
    @font-face {
      font-family: 'Jost';
      src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Regular.ttf') format('woff');
      font-weight: 400;
    }
    @font-face {
      font-family: 'Jost';
      src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Medium.ttf') format('woff');
      font-weight: 500;
    }
    @font-face {
      font-family: 'Jost';
      src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-SemiBold.ttf') format('woff');
      font-weight: 600;
    }
    @font-face {
      font-family: 'Jost';
      src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Bold.ttf') format('woff');
      font-weight: 700;
    }
    @font-face {
      font-family: 'Poppins';
      src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Fonts/Poppins-Regular.woff') format('woff');
      font-weight: 400;
    }
    @media screen and (max-width: 480px) {
      .container { max-width: 100% !important; }
      .main { max-width: 90% !important; }
      .img-wrap { max-width: 50px !important; max-height: 50px !important; }
      .logo { width: 130px !important; height: 52px !important; padding: 15px 0 !important; }
      .main-title { font-size: 30px !important; line-height: 40px !important; }
      .main-desc { font-size: 12px !important; line-height: 18px !important; max-width: 70% !important; }
    }
  </style>
</head>
<body style="font-family: 'Jost', Arial, sans-serif; font-weight: 400; margin: 0; padding: 0;">
<!-- Theme -->
<table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%" style="max-width: 600px; margin: 0 auto; background-color: #FFFFFF;" class="container">
  <!-- Header -->
  <tr>
    <td style="text-align: center; position: relative;">
      <table width="100%" cellpadding="0" cellspacing="0" border="0" class="main" style="max-width: 90%; margin: 0 auto; border: 1px solid #AC8763; border-top: 0;">
        <tr>
          <td>
            <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/access-to-early-sales/logo.png" class="logo" alt="Logo" style="display: inline-block; width: 146px; height: 57px; object-fit: cover; padding: 30px 0;" />
          </td>
        </tr>
      </table>
    </td>
  </tr>
  <!-- Banner -->
  <tr>
    <td style="text-align: center;">
      <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/access-to-early-sales/banner.png" style="width: 100%;" alt="Banner" />
    </td>
  </tr>

  <!-- Content -->
  <tr>
    <td>
      <table width="100%" cellpadding="0" cellspacing="0" border="0" class="main" style="max-width: 90%; margin: 0 auto;">
        <tr>
          <td style="padding: 30px 0; text-align: center;">
            <h1 class="main-title" style="font-size: 40px; line-height: 50px; font-weight: 700; color: #000000; margin: 0;">You've Got Early Access!</h1>
          </td>
        </tr>
        <tr>
          <td style="text-align: center;">
            <p class="main-desc" style="font-size: 14px; font-weight: 400; color: #4F4F4F; line-height: 22px; margin: 0 auto; max-width: 66%;">
              Get a head start on shopping our exclusive sale before anyone else. Don't miss out on the best deals!
            </p>
          </td>
        </tr>
        <tr>
          <td style="text-align: center; padding-top: 30px;">
            <a href="#" style="text-decoration: none; background: #AC8763; padding: 12px
  <!-- Product Grid Section -->
  <tr>
    <td style="padding: 50px 0 30px 0;">
      <table width="100%" cellpadding="0" cellspacing="0" border="0" class="main" style="max-width: 90%; margin: 0 auto;">
        <tr>
          <td colspan="3" style="text-align: center; padding-bottom: 30px;">
            <h2 style="font-size: 20px; font-weight: 600; margin: 0;">Handpicked Just for You</h2>
          </td>
        </tr>
        <tr>
          <!-- Product 1 -->
          <td style="text-align: center;" width="33%">
            <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/access-to-early-sales/product-1.png" style="width: 100%; max-width: 160px;" alt="Product 1" />
            <h4 style="margin: 10px 0 5px 0; font-size: 16px; font-weight: 600;">Product Name</h4>
            <p style="margin: 0; font-size: 14px; color: #4F4F4F;">₹1500</p>
          </td>

          <!-- Product 2 -->
          <td style="text-align: center;" width="33%">
            <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/access-to-early-sales/product-2.png" style="width: 100%; max-width: 160px;" alt="Product 2" />
            <h4 style="margin: 10px 0 5px 0; font-size: 16px; font-weight: 600;">Product Name</h4>
            <p style="margin: 0; font-size: 14px; color: #4F4F4F;">₹1500</p>
          </td>

          <!-- Product 3 -->
          <td style="text-align: center;" width="33%">
            <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/access-to-early-sales/product-3.png" style="width: 100%; max-width: 160px;" alt="Product 3" />
            <h4 style="margin: 10px 0 5px 0; font-size: 16px; font-weight: 600;">Product Name</h4>
            <p style="margin: 0; font-size: 14px; color: #4F4F4F;">₹1500</p>
          </td>
        </tr>
      </table>
    </td>
  </tr>
  <!-- CTA Section -->
  <tr>
    <td style="text-align: center; padding: 30px 0;">
      <a href="#" style="text-decoration: none; background: #AC8763; padding: 12px 40px; color: #fff; font-size: 14px; text-transform: uppercase; display: inline-block;">Explore More</a>
    </td>
  </tr>

  <!-- Footer -->
  <tr>
    <td style="background: #1E1E1E; padding: 30px 0;">
      <table width="100%" cellpadding="0" cellspacing="0" border="0" class="main" style="max-width: 90%; margin: 0 auto; text-align: center;">
        <tr>
          <td>
            <a href="#" style="margin: 0 10px;">
              <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/access-to-early-sales/logo-insta.png" alt="Instagram" width="20" />
            </a>
            <a href="#" style="margin: 0 10px;">
              <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/access-to-early-sales/logo-facebook.png" alt="Facebook" width="20" />
            </a>
            <a href="#" style="margin: 0 10px;">
              <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/access-to-early-sales/logo-x.png" alt="Twitter" width="20" />
            </a>
          </td>
        </tr>
        <tr>
          <td style="padding-top: 20px;">
            <p style="color: #ffffff; font-size: 14px; margin: 0;">
              is simply dummy text of the printing and typesetting industry.
            </p>
          </td>
        </tr>
        <tr>
          <td style="padding-top: 5px;">
            <p style="color: #ffffff; font-size: 14px; margin: 0;">
              To stop receiving these emails,
              <a href="#" style="color: #ffffff; font-weight: bold; text-decoration: underline;">unsubscribe here</a>
            </p>
          </td>
        </tr>
      </table>
    </td>
  </tr>
</table>
</body>
</html>

```

## Account Verification Template

A transactional template used to confirm new user sign-ups or secure account activity with verification steps.

**Use Case:** Sends a verification link or code to validate new user signups and confirm account security.

**Components:**

- [Replace the Logo](doc:ootb#1-replace-the-logo)
- [Update Banner/Product Images](doc:ootb#2-update-bannerproduct-images)
- [Update Call-To-Actions (CTAs)](https://staging.docs.user.clevertap.net/docs/ootb#3-call-to-actions-ctas)
- [Update Links in the Header/Footer](doc:ootb#4-update-links-in-the-headerfooter)
- [Change the Theme or Background Color](doc:ootb#5-change-the-theme-or-background-color)
- [Update the Privacy Policy](doc:ootb#update-the-privacy-policy)
- [Update Social Media Links and Download Links](doc:ootb#update-social-media-links-and-download-links)

```html HTML
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Account Verification</title>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <style>
      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Light.ttf') format('woff');
        font-style: normal;
        font-weight: 300;
      }
      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Regular.ttf') format('woff');
        font-style: normal;
        font-weight: 400;
      }
      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Medium.ttf') format('woff');
        font-style: normal;
        font-weight: 500;
      }
      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-SemiBold.ttf') format('woff');
        font-style: normal;
        font-weight: 600;
      }
      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Bold.ttf') format('woff');
        font-style: normal;
        font-weight: 700;
      }
      @media screen and (max-width: 480px) {
        .container {
          max-width: 100% !important;
        }
        .box-table {
          margin: 15px 15px 0px !important;
          padding: 20px 0px !important;
        }
        .imgConfirmation {
          width: 50% !important;
        }
        .content-sec {
          padding: 10px !important;
          margin-top: 0px !important;
        }
        .footer-content {
          padding: 0px 10px !important;
        }
        .expiry-para {
          padding: 0px 0px !important;
        }
        .main-heading {
          font-size: 24px !important;
          line-height: 30px !important;
        }
      }
    </style>
  </head>
  <body style="font-family: 'Jost', Arial, sans-serif; font-weight: 400; margin: 0; padding: 0;">
    <!-- Change Theme -->
    <table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%" style="max-width: 600px; margin: 0 auto; background-color: #F0EEF6; padding: 30px 0px 0px;" class="container">
      <!-- header start-->
      <tr>
        <td style="text-align: center; vertical-align: middle; padding: 20px; margin: 0px 30px; display: block;">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/logo.png" class="logo" alt="Logo" style="display: inline-block; width: 127px; height: 58px; object-fit: cover;" />
        </td>
      </tr>
      <!-- Box Start -->
      <tr>
        <td style="padding: 0px 30px;">
          <table width="100%" cellpadding="0" cellspacing="0" border="0" class="box-table" style="border-radius: 20px; background: #ffffff; border: 1px solid #ac8763; padding: 30px 0px;">
            <!-- Icon Image -->
            <tr>
              <td style="text-align: center;">
                <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/account-verification/email.png" class="imgConfirmation" alt="email icon" style="width: 90px;" />
              </td>
            </tr>
            <!-- Headline -->
            <tr>
              <td style="text-align: center; padding-top: 20px;">
                <h2 class="main-heading" style="font-size: 30px; font-weight: 700; margin: 0; color: #000000;">Verify Your Email Address</h2>
              </td>
            </tr>
            <!-- Body Text -->
            <tr>
              <td style="padding: 10px 30px;">
                <p class="content-sec" style="margin: 20px auto 0; font-size: 14px; font-weight: 400; color: #4f4f4f; line-height: 24px;">
                  To continue setting up your account, please verify that this is your email address.
                </p>
              </td>
            </tr>
            <!-- CTA -->
            <tr>
              <td style="text-align: center; padding-top: 30px;">
                <a href="#" style="text-decoration: none; background: #ac8763; padding: 12px 50px; color: #fff; font-size: 14px; text-transform: uppercase; display: inline-block;">Verify Now</a>
              </td>
            </tr>
            <!-- Expiry Note -->
            <tr>
              <td style="padding: 30px 30px 0;">
                <p class="expiry-para" style="font-size: 12px; line-height: 22px; text-align: center; color: #7a7a7a;">
                  This link will expire in 24 hours for your security.
                </p>
              </td>
            </tr>
          </table>
        </td>
      </tr>
      <!-- Footer Section -->
      <tr>
        <td style="padding: 32px 0px; background: #1e1e1e; text-align: center;">
          <!-- Social Icons -->
          <a href="#" style="margin: 0 10px;">
            <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/account-verification/logo-insta.png" alt="Instagram" width="20" />
          </a>
          <a href="#" style="margin: 0 10px;">
            <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/account-verification/logo-facebook.png" alt="Facebook" width="20" />
          </a>
          <a href="#" style="margin: 0 10px;">
            <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/account-verification/logo-x.png" alt="Twitter/X" width="20" />
          </a>

          <!-- Footer Text -->
          <p style="color: #ffffff; font-size: 14px; margin-top: 20px;">
            is simply dummy text of the printing and typesetting industry.
          </p>
          <p style="color: #ffffff; font-size: 14px;">
            To stop receiving these emails,
            <a href="#" style="color: #ffffff; font-weight: bold; text-decoration: underline;">unsubscribe here</a>
          </p>
        </td>
      </tr>
      <!-- Footer Section -->
      <tr>
        <td style="padding: 32px 0px; background: #1e1e1e; text-align: center;">
          <!-- Social Icons -->
          <a href="#" style="margin: 0 10px;">
            <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/account-verification/logo-insta.png" alt="Instagram" width="20" />
          </a>
          <a href="#" style="margin: 0 10px;">
            <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/account-verification/logo-facebook.png" alt="Facebook" width="20" />
          </a>
          <a href="#" style="margin: 0 10px;">
            <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/account-verification/logo-x.png" alt="Twitter/X" width="20" />
          </a>

          <!-- Footer Text -->
          <p style="color: #ffffff; font-size: 14px; margin-top: 20px;">
            is simply dummy text of the printing and typesetting industry.
          </p>
          <p style="color: #ffffff; font-size: 14px;">
            To stop receiving these emails,
            <a href="#" style="color: #ffffff; font-weight: bold; text-decoration: underline;">unsubscribe here</a>
          </p>
        </td>
      </tr>
    </table>
    <!-- Closing main wrapper -->

    <!-- Optional fallback text -->
    <table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%" style="max-width: 600px; margin: 0 auto;" class="container">
      <tr>
        <td style="text-align: center; padding: 20px;">
          <p style="font-size: 12px; color: #7a7a7a;">
            If you're having trouble clicking the "Verify Now" button, copy and paste the URL below into your web browser:
            <br />
            <a href="#" style="color: #ac8763;">https://yourdomain.com/verify</a>
          </p>
        </td>
      </tr>
    </table>
  </body>
</html>
```

## Anniversary Template

A relationship-nurturing template that celebrates a customer's anniversary with the brand, often offering a special incentive.

**Use Case:** Celebrates the anniversary of a customer’s signup or purchase. Reinforces brand loyalty with personalized offers.

**Components:**

- [Replace the Logo](doc:ootb#1-replace-the-logo)
- [Update Banner/Product Images](doc:ootb#2-update-bannerproduct-images)
- [Update Call-To-Actions (CTAs)](https://staging.docs.user.clevertap.net/docs/ootb#3-call-to-actions-ctas)
- [Update Links in the Header/Footer](doc:ootb#4-update-links-in-the-headerfooter)
- [Change the Theme or Background Color](doc:ootb#5-change-the-theme-or-background-color)
- [Update Social Media Links and Download Links](doc:ootb#update-social-media-links-and-download-links)

```html HTML
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Anniversary</title>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <style>
      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Light.ttf') format('woff');
        font-style: normal;
        font-weight: 300;
      }
      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Regular.ttf') format('woff');
        font-style: normal;
        font-weight: 400;
      }
      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Medium.ttf') format('woff');
        font-style: normal;
        font-weight: 500;
      }
      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-SemiBold.ttf') format('woff');
        font-style: normal;
        font-weight: 600;
      }
      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Bold.ttf') format('woff');
        font-style: normal;
        font-weight: 700;
      }
      @media screen and (max-width: 478px) {
        .container {
          max-width: 90% !important;
        }
        .logo {
          width: 150px !important;
          height: 60px !important;
        }
        .cta {
          padding: 10px 25px !important;
        }
        .offer-wrap {
          padding: 40px 15px !important;
        }
        .offer-title {
          font-size: 35px !important;
          line-height: 45px !important;
        }
        .title {
          font-size: 35px !important;
          line-height: 45px !important;
        }
        .code {
          line-height: 20px !important;
          margin-bottom: 20px !important;
        }
        .date {
          font-size: 26px !important;
          line-height: 30px !important;
        }
        .wishes-txt {
          font-size: 16px !important;
          line-height: 24px !important;
        }
        .footer-desc {
          line-height: 28px !important;
        }
      }
    </style>
  </head>
  <body style="font-family: 'Jost', Arial, sans-serif; font-weight: 400; margin: 0; padding: 0; background: aliceblue;">
    <table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%" style="max-width: 600px; margin: 0 auto; background-color: #FFFFFF;">
      <!-- header start-->
      <tr>
        <td align="center" style="display: block; padding: 24px 0; max-width: 90%; margin: 0 auto;" class="container">
          <div class="logo-wrap">
            <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Anniversary/logo.png" alt="Logo" class="logo" style="width: 159px; height: 73px; object-fit: cover;" />
          </div>
        </td>
      </tr>
      <!-- Banner -->
      <tr>
        <td style="text-align: center;">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Anniversary/banner.png" alt="Banner" style="width: 100%; height: auto;" />
        </td>
      </tr>

      <!-- Offer Section -->
      <tr>
        <td style="padding: 50px 30px;" class="offer-wrap">
          <h1 class="offer-title" style="font-size: 45px; font-weight: 600; text-align: center; color: #252525; margin: 0;">
            Happy Anniversary!
          </h1>
          <p class="wishes-txt" style="text-align: center; font-size: 18px; font-weight: 400; line-height: 30px; margin-top: 15px; color: #252525;">
            We're thrilled to celebrate your journey with us. Here's a little something to say thank you!
          </p>
        </td>
      </tr>

      <!-- Discount Code -->
      <tr>
        <td align="center" style="padding: 0 30px;">
          <table style="width: 100%; text-align: center;">
            <tr>
              <td style="background: #f3f3f3; padding: 20px 0; border: 2px dashed #ac8763;">
                <p class="code" style="margin: 0; font-size: 18px; font-weight: 500; letter-spacing: 2px; color: #000;">ANNI10</p>
              </td>
            </tr>
          </table>
        </td>
      </tr>

      <!-- CTA -->
      <tr>
        <td style="text-align: center; padding: 30px;">
          <a href="#" class="cta" style="text-decoration: none; background: #ac8763; padding: 12px 50px; color: #fff; font-size: 14px; text-transform: uppercase; display: inline-block;">Shop Now</a>
        </td>
      </tr>
      <!-- Date and Disclaimer -->
      <tr>
        <td align="center" style="padding: 0 30px;">
          <p class="date" style="font-size: 28px; font-weight: 600; color: #252525; margin: 0;">
            Valid till: 30th April 2025
          </p>
          <p style="font-size: 12px; font-weight: 400; color: #7a7a7a; line-height: 22px; margin-top: 5px;">
            Offer valid on selected items only. T&C apply.
          </p>
        </td>
      </tr>

      <!-- Divider -->
      <tr>
        <td style="padding: 40px 0;">
          <hr style="border: none; border-top: 1px solid #d8d8d8; width: 80%; margin: 0 auto;" />
        </td>
      </tr>

      <!-- Footer -->
      <tr>
        <td style="background-color: #1e1e1e; text-align: center; padding: 30px 0;">
          <!-- Social Icons -->
          <a href="#" style="margin: 0 10px;">
            <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Anniversary/logo-insta.png" width="20" alt="Instagram" />
          </a>
          <a href="#" style="margin: 0 10px;">
            <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Anniversary/logo-facebook.png" width="20" alt="Facebook" />
          </a>
          <a href="#" style="margin: 0 10px;">
            <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Anniversary/logo-x.png" width="20" alt="Twitter" />
          </a>
          <!-- Footer Text -->
          <p class="footer-desc" style="color: #ffffff; font-size: 14px; line-height: 24px; margin-top: 20px; font-weight: 400;">
            is simply dummy text of the printing and typesetting industry.
          </p>

          <p style="color: #ffffff; font-size: 14px; font-weight: 400; margin-top: 5px;">
            To stop receiving these emails,
            <a href="#" style="color: #ffffff; font-weight: bold; text-decoration: underline;">unsubscribe here</a>
          </p>
        </td>
      </tr>

      <!-- Optional fallback URL -->
      <tr>
        <td style="padding: 20px; text-align: center;">
          <p style="font-size: 12px; color: #7a7a7a;">
            If you're having trouble clicking the "Shop Now" button, copy and paste this URL into your browser:
            <br />
            <a href="#" style="color: #ac8763;">https://yourbrand.com/anniversary</a>
          </p>
        </td>
      </tr>
    </table>
  </body>
</html>

```

## Informative Mailer Template

A neutral template for communicating non-promotional updates such as policy changes, feature introductions, or general announcements.

### Use Case Templates

Shares important business updates, new features, or informational content that doesn’t focus on sales.

**Components:**

- [Replace the Logo](doc:ootb#1-replace-the-logo)
- [Update Banner/Product Images](doc:ootb#2-update-bannerproduct-images)
- [Update Call-To-Actions (CTAs)](https://staging.docs.user.clevertap.net/docs/ootb#3-call-to-actions-ctas)
- [Update Links in the Header/Footer](doc:ootb#4-update-links-in-the-headerfooter)
- [Change the Theme or Background Color](doc:ootb#5-change-the-theme-or-background-color)
- [Update Social Media Links and Download Links](doc:ootb#update-social-media-links-and-download-links)

```html HTML
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Informative</title>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">

    <style>
      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Light.ttf') format('woff');
        font-style: normal;
        font-weight: 300;
      }

      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Regular.ttf') format('woff');
        font-style: normal;
        font-weight: 400;
      }

      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Medium.ttf') format('woff');
        font-style: normal;
        font-weight: 500;
      }

      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-SemiBold.ttf') format('woff');
        font-style: normal;
        font-weight: 600;
      }

      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Bold.ttf') format('woff');
        font-style: normal;
        font-weight: 700;
      }

      @media screen and (max-width: 480px) {
        .container { max-width: 100% !important; }
        .main { max-width: 90% !important; }
        .faq-sec { padding: 10px !important; }
      }
    </style>
  </head>
  <body style="background: #dddddd; font-family: 'Jost', Arial, sans-serif; font-weight: 400; margin: 0; padding: 0;">
    <!-- Change Theme -->
    <table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%" class="container" style="max-width: 600px; margin: 0 auto; background-color: #FFFFFF;">
      <!-- Header -->
      <tr>
        <td align="center" style="padding: 24px 0;">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Informative/logo.png"
               alt="Logo" class="logo" style="width: 159px; height: 73px; object-fit: cover;" />
        </td>
      </tr>

      <!-- Banner -->
      <tr>
        <td style="text-align: center;">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Informative/banner.png"
               alt="Banner" style="width: 100%; height: auto;" />
        </td>
      </tr>

      <!-- Heading & Paragraph -->
      <tr>
        <td class="main" style="padding: 40px 30px;">
          <h1 style="font-size: 30px; font-weight: 600; color: #252525; margin: 0;">We’ve made some changes</h1>
          <p style="font-size: 16px; color: #4f4f4f; line-height: 26px; margin: 15px 0 0;">
            Our terms of service and privacy policy have been updated to improve your experience.
          </p>
        </td>
      </tr>
      <!-- CTA Button -->
      <tr>
        <td style="text-align: center; padding: 30px;">
          <a href="#" class="cta"
             style="text-decoration: none; background: #ac8763; padding: 12px 40px; color: #fff; font-size: 14px; text-transform: uppercase; display: inline-block;">
            Read More
          </a>
        </td>
      </tr>

      <!-- Divider -->
      <tr>
        <td style="padding: 40px 0;">
          <hr style="border: none; border-top: 1px solid #d8d8d8; width: 80%; margin: 0 auto;" />
        </td>
      </tr>

      <!-- Footer -->
      <tr>
        <td style="background-color: #1e1e1e; text-align: center; padding: 30px 0;">
          <!-- Social Icons -->
          <a href="#" style="margin: 0 10px;">
            <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Informative/logo-insta.png" width="20" alt="Instagram" />
          </a>
          <a href="#" style="margin: 0 10px;">
            <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Informative/logo-facebook.png" width="20" alt="Facebook" />
          </a>
          <a href="#" style="margin: 0 10px;">
            <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Informative/logo-x.png" width="20" alt="Twitter/X" />
          </a>
          <!-- Footer Text -->
          <p style="color: #ffffff; font-size: 14px; line-height: 24px; margin-top: 20px; font-weight: 400;">
            is simply dummy text of the printing and typesetting industry.
          </p>

          <p style="color: #ffffff; font-size: 14px; font-weight: 400; margin-top: 5px;">
            To stop receiving these emails,
            <a href="#" style="color: #ffffff; font-weight: bold; text-decoration: underline;">unsubscribe here</a>
          </p>
        </td>
      </tr>

      <!-- Fallback Link -->
      <tr>
        <td style="padding: 20px; text-align: center;">
          <p style="font-size: 12px; color: #7a7a7a;">
            If you're having trouble clicking the "Read More" button, copy and paste this URL into your browser:
            <br />
            <a href="#" style="color: #ac8763;">https://yourbrand.com/policy-update</a>
          </p>
        </td>
      </tr>
    </table>

    <!-- End Main Container -->
  </body>
</html>
```

## Loyalty Expiry Template

A template that alerts users about expiring loyalty points and urges them to use them before they expire.

**Use Case:** Drives redemption activity by informing users that their loyalty points are about to expire.

**Components:**

- [Replace the Logo](doc:ootb#1-replace-the-logo)
- [Update Banner/Product Images](doc:ootb#2-update-bannerproduct-images)
- [Update Call-To-Actions (CTAs)](https://staging.docs.user.clevertap.net/docs/ootb#3-call-to-actions-ctas)
- [Update Links in the Header/Footer](doc:ootb#4-update-links-in-the-headerfooter)
- [Change the Theme or Background Color](doc:ootb#5-change-the-theme-or-background-color) 
- [Update Social Media Links and Download Links](doc:ootb#update-social-media-links-and-download-links)

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Loyalty Point Expiry</title>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <style>
      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Light.ttf') format('woff');
        font-style: normal;
        font-weight: 300;
      }
      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Regular.ttf') format('woff');
        font-style: normal;
        font-weight: 400;
      }
      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Medium.ttf') format('woff');
        font-style: normal;
        font-weight: 500;
      }
      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-SemiBold.ttf') format('woff');
        font-style: normal;
        font-weight: 600;
      }
      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Bold.ttf') format('woff');
        font-style: normal;
        font-weight: 700;
      }
      @media screen and (max-width: 480px) {
        .container { max-width: 100% !important; }
        .loyalty-sec { padding: 30px !important; }
        .footer-content { padding: 0px 30px !important; }
        .expiry-para { padding: 10px 20px !important; }
        .main-heading { font-size: 30px !important; line-height: 40px !important; }
      }
    </style>
  </head>
  <body style="font-family: 'Jost', Arial, sans-serif; font-weight: 400; margin: 0; padding: 0;">
    <!-- Change Image -->
    <table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%"
           style="max-width: 600px; margin: 0 auto; background-color: #F0EEF6; padding: 30px 0px 0px;"
           class="container">
      <!-- Logo -->
      <tr>
        <td align="center" style="padding: 24px 0;">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/loyalty-expiry/logo.png"
               alt="Logo" class="logo" style="width: 159px; height: 73px; object-fit: cover;" />
        </td>
      </tr>

      <!-- Banner -->
      <tr>
        <td style="text-align: center;">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/loyalty-expiry/banner.png"
               alt="Banner" style="width: 100%; height: auto;" />
        </td>
      </tr>

      <!-- Message Block -->
      <tr>
        <td class="loyalty-sec" style="padding: 50px 40px;">
          <h1 class="main-heading" style="font-size: 36px; font-weight: 600; color: #252525; margin: 0 0 15px; text-align: center;">
            Your Points Are Expiring Soon!
          </h1>
          <p style="text-align: center; font-size: 16px; color: #4f4f4f; line-height: 26px; margin: 0;">
            Don’t miss out on using your loyalty points before they expire. Redeem them now and enjoy exclusive rewards.
          </p>
        </td>
      </tr>
      <!-- CTA -->
      <tr>
        <td style="text-align: center; padding: 0 40px 40px;">
          <a href="#" class="cta"
             style="text-decoration: none; background: #ac8763; padding: 12px 50px; color: #fff; font-size: 14px; text-transform: uppercase; display: inline-block;">
            Redeem Now
          </a>
        </td>
      </tr>

      <!-- Divider -->
      <tr>
        <td style="padding: 0 0 40px;">
          <hr style="border: none; border-top: 1px solid #d8d8d8; width: 80%; margin: 0 auto;" />
        </td>
      </tr>

      <!-- Footer Section -->
      <tr>
        <td style="background-color: #1e1e1e; text-align: center; padding: 30px 0;">
          <!-- Social Icons -->
          <a href="#" style="margin: 0 10px;">
            <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/loyalty-expiry/logo-insta.png" width="20" alt="Instagram" />
          </a>
          <a href="#" style="margin: 0 10px;">
            <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/loyalty-expiry/logo-facebook.png" width="20" alt="Facebook" />
          </a>
          <a href="#" style="margin: 0 10px;">
            <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/loyalty-expiry/logo-x.png" width="20" alt="Twitter/X" />
          </a>
          <!-- Footer Text -->
          <p style="color: #ffffff; font-size: 14px; line-height: 24px; margin-top: 20px; font-weight: 400;">
            is simply dummy text of the printing and typesetting industry.
          </p>

          <p style="color: #ffffff; font-size: 14px; font-weight: 400; margin-top: 5px;">
            To stop receiving these emails,
            <a href="#" style="color: #ffffff; font-weight: bold; text-decoration: underline;">unsubscribe here</a>
          </p>
        </td>
      </tr>

      <!-- Fallback for CTA -->
      <tr>
        <td style="padding: 20px; text-align: center;">
          <p style="font-size: 12px; color: #7a7a7a;">
            If you're having trouble clicking the "Redeem Now" button, copy and paste this URL into your browser:
            <br />
            <a href="#" style="color: #ac8763;">https://yourbrand.com/redeem</a>
          </p>
        </td>
      </tr>
    </table>
  </body>
</html>
```

## Loyalty Points Template

A retention-focused template that updates users about their earned loyalty points and encourages usage.

**Use Case:** Motivates users to engage more with the brand by highlighting earned loyalty points and available rewards.

**Components:**

- [Replace the Logo](doc:ootb#1-replace-the-logo)
- [Update Call-To-Actions (CTAs)](https://staging.docs.user.clevertap.net/docs/ootb#3-call-to-actions-ctas)
- [Change the Theme or Background Color](doc:ootb#5-change-the-theme-or-background-color)
- [Update Social Media Links and Download Links](doc:ootb#update-social-media-links-and-download-links)

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Loyalty Point</title>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <style>
      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Light.ttf') format('woff');
        font-style: normal;
        font-weight: 300;
      }
      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Regular.ttf') format('woff');
        font-style: normal;
        font-weight: 400;
      }
      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Medium.ttf') format('woff');
        font-style: normal;
        font-weight: 500;
      }
      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-SemiBold.ttf') format('woff');
        font-style: normal;
        font-weight: 600;
      }
      @font-face {
        font-family: 'Jost';
        src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Bold.ttf') format('woff');
        font-style: normal;
        font-weight: 700;
      }
      @media screen and (max-width: 480px) {
        .container { max-width: 100% !important; }
        .loyalty-sec { padding: 30px !important; }
        .footer-content { padding: 0px 30px !important; }
        .main-heading { font-size: 30px !important; line-height: 40px !important; }
      }
    </style>
  </head>
  <body style="font-family: 'Jost', Arial, sans-serif; font-weight: 400; margin: 0; padding: 0;">
    <!-- Change Theme -->
    <table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%" style="max-width: 600px; margin: 0 auto; background-color: #F0EEF6; padding: 30px;" class="container">
      <!-- Header -->
      <tr>
        <td align="center" style="padding: 24px 0;">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/loyalty-points/logo.png"
               alt="Logo" class="logo" style="width: 159px; height: 73px; object-fit: cover;" />
        </td>
      </tr>

      <!-- Banner -->
      <tr>
        <td style="text-align: center;">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/loyalty-points/banner.png"
               alt="Banner" style="width: 100%; height: auto;" />
        </td>
      </tr>

      <!-- Main Message -->
      <tr>
        <td class="loyalty-sec" style="padding: 50px 40px;">
          <h1 class="main-heading" style="font-size: 36px; font-weight: 600; color: #252525; margin: 0 0 15px; text-align: center;">
            You’ve earned loyalty points!
          </h1>
          <p style="text-align: center; font-size: 16px; color: #4f4f4f; line-height: 26px; margin: 0;">
            Great news! You’ve accumulated points through your recent activity. Redeem them for exciting rewards and perks.
          </p>
        </td>
      </tr>
      <!-- CTA Button -->
      <tr>
        <td style="text-align: center; padding: 0 40px 40px;">
          <a href="#" class="cta"
             style="text-decoration: none; background: #ac8763; padding: 12px 50px; color: #fff; font-size: 14px; text-transform: uppercase; display: inline-block;">
            View My Points
          </a>
        </td>
      </tr>

      <!-- Divider -->
      <tr>
        <td style="padding: 0 0 40px;">
          <hr style="border: none; border-top: 1px solid #d8d8d8; width: 80%; margin: 0 auto;" />
        </td>
      </tr>

      <!-- Footer Section -->
      <tr>
        <td style="background-color: #1e1e1e; text-align: center; padding: 30px 0;">
          <!-- Social Icons -->
          <a href="#" style="margin: 0 10px;">
            <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/loyalty-points/logo-insta.png" width="20" alt="Instagram" />
          </a>
          <a href="#" style="margin: 0 10px;">
            <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/loyalty-points/logo-facebook.png" width="20" alt="Facebook" />
          </a>
          <a href="#" style="margin: 0 10px;">
            <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/loyalty-points/logo-x.png" width="20" alt="Twitter/X" />
          </a>
          <!-- Footer Text -->
          <p style="color: #ffffff; font-size: 14px; line-height: 24px; margin-top: 20px; font-weight: 400;">
            is simply dummy text of the printing and typesetting industry.
          </p>

          <p style="color: #ffffff; font-size: 14px; font-weight: 400; margin-top: 5px;">
            To stop receiving these emails,
            <a href="#" style="color: #ffffff; font-weight: bold; text-decoration: underline;">unsubscribe here</a>
          </p>
        </td>
      </tr>

      <!-- Fallback CTA -->
      <tr>
        <td style="padding: 20px; text-align: center;">
          <p style="font-size: 12px; color: #7a7a7a;">
            If you're having trouble clicking the "View My Points" button, copy and paste this URL into your browser:
            <br />
            <a href="#" style="color: #ac8763;">https://yourbrand.com/loyalty-points</a>
          </p>
        </td>
      </tr>
    </table>
  </body>
</html>
```

## Newsletter Template

A recurring email layout used to share curated content like blogs, product updates, or brand stories.

**Use Case:** Keeps users informed and engaged by providing valuable content in a consistent format.

**Components:**

- [Replace the Logo](doc:ootb#1-replace-the-logo)
- [Update Banner/Product Images](doc:ootb#2-update-bannerproduct-images)
- [Update Call-To-Actions (CTAs)](https://staging.docs.user.clevertap.net/docs/ootb#3-call-to-actions-ctas)
- [Update Links in the Header/Footer](doc:ootb#4-update-links-in-the-headerfooter)
- [Change the Theme or Background Color](doc:ootb#5-change-the-theme-or-background-color)
- [Update the Privacy Policy](doc:ootb#update-the-privacy-policy)
- [Update Social Media Links and Download Links](doc:ootb#update-social-media-links-and-download-links)

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <title>Newsletter</title>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <style>
    @font-face {
      font-family: 'Jost';
      src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Light.ttf') format('woff');
      font-style: normal;
      font-weight: 300;
    }
    @font-face {
      font-family: 'Jost';
      src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Regular.ttf') format('woff');
      font-style: normal;
      font-weight: 400;
    }
    @font-face {
      font-family: 'Jost';
      src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Medium.ttf') format('woff');
      font-style: normal;
      font-weight: 500;
    }
    @font-face {
      font-family: 'Jost';
      src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-SemiBold.ttf') format('woff');
      font-style: normal;
      font-weight: 600;
    }
    @font-face {
      font-family: 'Jost';
      src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Bold.ttf') format('woff');
      font-style: normal;
      font-weight: 700;
    }
    @media screen and (max-width: 480px) {
      .main { max-width: 100% !important; }
      .container { max-width: 90% !important; }
    }
  </style>
</head>
<body style="font-family: 'Jost', Arial, sans-serif; font-weight: 400; margin: 0;">
  <!-- Change Theme -->
  <table align="center" cellpadding="0" cellspacing="0" width="100%" style="max-width: 600px; margin: 0 auto; background-color: #F5F5F5;">
    <!-- Logo -->
    <tr>
      <td align="center" style="padding: 24px 0;">
        <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/newsletter/logo.png"
             alt="Logo" class="logo" style="width: 159px; height: 73px; object-fit: cover;" />
      </td>
    </tr>

    <!-- Banner -->
    <tr>
      <td style="text-align: center;">
        <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/newsletter/banner.png"
             alt="Banner" style="width: 100%; height: auto;" />
      </td>
    </tr>

    <!-- Newsletter Heading -->
    <tr>
      <td class="container" style="padding: 40px 30px;">
        <h1 style="font-size: 30px; font-weight: 600; color: #252525; margin: 0 0 20px;">
          What’s New This Month?
        </h1>
        <p style="font-size: 16px; color: #4f4f4f; line-height: 26px; margin: 0;">
          Stay updated with the latest product features, community stories, and expert tips.
        </p>
      </td>
    </tr>
    <!-- Featured Section -->
    <tr>
      <td style="padding: 0 30px;">
        <h2 style="font-size: 20px; font-weight: 600; color: #252525; margin-bottom: 10px;">Feature Spotlight</h2>
        <p style="font-size: 16px; color: #4f4f4f; line-height: 26px; margin-top: 0;">
          Discover how to personalize your customer journeys with our new automation tools.
        </p>
      </td>
    </tr>

    <!-- CTA Button -->
    <tr>
      <td style="text-align: center; padding: 30px;">
        <a href="#" class="cta"
           style="text-decoration: none; background: #ac8763; padding: 12px 40px; color: #fff; font-size: 14px; text-transform: uppercase; display: inline-block;">
          Learn More
        </a>
      </td>
    </tr>

    <!-- Divider -->
    <tr>
      <td style="padding: 40px 0;">
        <hr style="border: none; border-top: 1px solid #d8d8d8; width: 80%; margin: 0 auto;" />
      </td>
    </tr>
    <!-- Footer -->
    <tr>
      <td style="background-color: #1e1e1e; text-align: center; padding: 30px 0;">
        <!-- Social Icons -->
        <a href="#" style="margin: 0 10px;">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/newsletter/logo-insta.png" width="20" alt="Instagram" />
        </a>
        <a href="#" style="margin: 0 10px;">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/newsletter/logo-facebook.png" width="20" alt="Facebook" />
        </a>
        <a href="#" style="margin: 0 10px;">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/newsletter/logo-x.png" width="20" alt="Twitter/X" />
        </a>

        <!-- Footer Text -->
        <p style="color: #ffffff; font-size: 14px; line-height: 24px; margin-top: 20px; font-weight: 400;">
          is simply dummy text of the printing and typesetting industry.
        </p>
        <p style="color: #ffffff; font-size: 14px; font-weight: 400; margin-top: 5px;">
          To stop receiving these emails,
          <a href="#" style="color: #ffffff; font-weight: bold; text-decoration: underline;">unsubscribe here</a>
        </p>
      </td>
    </tr>
    <!-- Fallback CTA Link -->
    <tr>
      <td style="padding: 20px; text-align: center;">
        <p style="font-size: 12px; color: #7a7a7a;">
          If you're having trouble clicking the "Learn More" button, copy and paste this URL into your browser:
          <br />
          <a href="#" style="color: #ac8763;">https://yourbrand.com/newsletter</a>
        </p>
      </td>
    </tr>
  </table>
</body>
</html>
```

## Order Delivered Template

A transactional template confirming successful delivery of an order.

**Use Case:** Notifies customers that their order has been delivered, closing the purchase loop and reinforcing reliability.

**Components:**

- [Replace the Logo](doc:ootb#1-replace-the-logo)
- [Update Banner/Product Images](doc:ootb#2-update-bannerproduct-images)
- [Update Call-To-Actions (CTAs)](https://staging.docs.user.clevertap.net/docs/ootb#3-call-to-actions-ctas)
- [Update Links in the Header/Footer](doc:ootb#4-update-links-in-the-headerfooter)
- [Change the Theme or Background Color](doc:ootb#5-change-the-theme-or-background-color)
- [Update the Privacy Policy](doc:ootb#update-the-privacy-policy)
- [Update Social Media Links and Download Links](doc:ootb#update-social-media-links-and-download-links)

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <title>Order Delivered</title>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <style>
    @font-face {
      font-family: 'Jost';
      src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Regular.ttf') format('woff');
      font-style: normal;
      font-weight: 400;
    }
    @font-face {
      font-family: 'Jost';
      src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-SemiBold.ttf') format('woff');
      font-style: normal;
      font-weight: 600;
    }
    @font-face {
      font-family: 'Jost';
      src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Bold.ttf') format('woff');
      font-style: normal;
      font-weight: 700;
    }
    @font-face {
      font-family: 'Poppins';
      src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Fonts/Poppins-Regular.woff') format('woff');
      font-style: normal;
      font-weight: 400;
    }
    @media screen and (max-width: 480px) {
      .container { max-width: 100% !important; margin-bottom: 20px !important; }
      .logo { width: 145px !important; height: 55px !important; }
      .cta { padding: 10px 25px !important; margin: 30px 0 !important; font-size: 16px !important; line-height: 20px !important; }
      .content-wrap { max-width: 90% !important; }
      .title { font-size: 22px !important; line-height: 28px !important; }
      .border-line { width: 40% !important; }
      .desc { font-size: 12px !important; line-height: 18px !important; margin: 0 0 30px !important; }
    }
  </style>
</head>
<body style="font-family: 'Jost', Arial, sans-serif; font-weight: 400; margin: 0; padding: 0;">
  <!-- Change Theme -->
  <table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%" style="max-width: 600px; margin: 0 auto; background-color: #F5F5F5;">
    <!-- Logo -->
    <tr>
      <td align="center" style="padding: 24px 0;">
        <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/order-delivered/logo.png"
             alt="Logo" class="logo" style="width: 159px; height: 73px; object-fit: cover;" />
      </td>
    </tr>

    <!-- Banner -->
    <tr>
      <td style="text-align: center;">
        <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/order-delivered/banner.png"
             alt="Banner" style="width: 100%; height: auto;" />
      </td>
    </tr>

    <!-- Delivery Message -->
    <tr>
      <td align="center" style="padding: 50px 40px;">
        <h1 class="title" style="font-size: 32px; font-weight: 600; color: #252525; margin-bottom: 20px;">
          Your Order Has Been Delivered!
        </h1>
        <p class="desc" style="font-size: 16px; color: #4f4f4f; line-height: 26px; margin: 0;">
          We hope you enjoy your purchase. Thank you for shopping with us!
        </p>
      </td>
    </tr>
    <!-- CTA Button -->
    <tr>
      <td style="text-align: center; padding-bottom: 40px;">
        <a href="#" class="cta"
           style="text-decoration: none; background: #ac8763; padding: 12px 50px; color: #fff; font-size: 14px; text-transform: uppercase; display: inline-block;">
          View Order
        </a>
      </td>
    </tr>

    <!-- Divider -->
    <tr>
      <td style="padding: 0 0 40px;">
        <hr style="border: none; border-top: 1px solid #d8d8d8; width: 80%; margin: 0 auto;" />
      </td>
    </tr>

    <!-- Footer Section Start -->
    <tr>
      <td style="background-color: #1e1e1e; text-align: center; padding: 30px 0;">
        <!-- Social Icons -->
        <a href="#" style="margin: 0 10px;">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/order-delivered/logo-insta.png" width="20" alt="Instagram" />
        </a>
        <a href="#" style="margin: 0 10px;">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/order-delivered/logo-facebook.png" width="20" alt="Facebook" />
        </a>
        <a href="#" style="margin: 0 10px;">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/order-delivered/logo-x.png" width="20" alt="Twitter/X" />
        </a>
        <!-- Footer Text -->
        <p style="color: #ffffff; font-size: 14px; line-height: 24px; margin-top: 20px; font-weight: 400;">
          is simply dummy text of the printing and typesetting industry.
        </p>

        <p style="color: #ffffff; font-size: 14px; font-weight: 400; margin-top: 5px;">
          To stop receiving these emails,
          <a href="#" style="color: #ffffff; font-weight: bold; text-decoration: underline;">unsubscribe here</a>
        </p>
      </td>
    </tr>

    <!-- Fallback Link -->
    <tr>
      <td style="padding: 20px; text-align: center;">
        <p style="font-size: 12px; color: #7a7a7a;">
          If you're having trouble clicking the "View Order" button, copy and paste this URL into your browser:
          <br />
          <a href="#" style="color: #ac8763;">https://yourbrand.com/order-details</a>
        </p>
      </td>
    </tr>
  </table>
</body>
</html>
```

## Order Placed Template

A confirmation email sent after a customer places an order.

**Use Case:** Provides immediate confirmation of a completed purchase along with key order details.

**Components:**

- [Replace the Logo](doc:ootb#1-replace-the-logo)
- [Update Banner/Product Images](doc:ootb#2-update-bannerproduct-images)
- [Update Call-To-Actions (CTAs)](https://staging.docs.user.clevertap.net/docs/ootb#3-call-to-actions-ctas)
- [Update Links in the Header/Footer](doc:ootb#4-update-links-in-the-headerfooter)
- [Change the Theme or Background Color](doc:ootb#5-change-the-theme-or-background-color)
- [Update the Privacy Policy](doc:ootb#update-the-privacy-policy)
- [Update Social Media Links and Download Links](doc:ootb#update-social-media-links-and-download-links)

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <title>Order Placed</title>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta http-equiv="X-UA-Compatible" content="IE=edge" />
  <style>
    @font-face {
      font-family: 'Jost';
      src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Light.ttf') format('woff');
      font-style: normal;
      font-weight: 300;
    }
    @font-face {
      font-family: 'Jost';
      src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Regular.ttf') format('woff');
      font-style: normal;
      font-weight: 400;
    }
    @font-face {
      font-family: 'Jost';
      src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Medium.ttf') format('woff');
      font-style: normal;
      font-weight: 500;
    }
    @font-face {
      font-family: 'Jost';
      src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-SemiBold.ttf') format('woff');
      font-style: normal;
      font-weight: 600;
    }
    @font-face {
      font-family: 'Jost';
      src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Bold.ttf') format('woff');
      font-style: normal;
      font-weight: 700;
    }
    @media screen and (max-width: 480px) {
      .container { max-width: 100% !important; margin-bottom: 20px !important; }
      .logo { width: 145px !important; height: 55px !important; }
      .cta { padding: 10px 25px !important; margin: 30px 0 !important; font-size: 16px !important; line-height: 20px !important; }
      .content-wrap { max-width: 90% !important; }
      .title { font-size: 22px !important; line-height: 28px !important; }
      .border-line { width: 40% !important; }
      .desc { font-size: 12px !important; line-height: 18px !important; margin: 0 0 30px !important; }
    }
  </style>
</head>
<body style="font-family: 'Jost', Arial, sans-serif; font-weight: 400; margin: 0; padding: 0;">
  <!-- Change Theme -->
  <table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%"
         style="max-width: 600px; margin: 0 auto; background-color: #F5F5F5;">
    <!-- Logo -->
    <tr>
      <td align="center" style="padding: 24px 0;">
        <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/order-placed/logo.png"
             alt="Logo" class="logo" style="width: 159px; height: 73px; object-fit: cover;" />
      </td>
    </tr>

    <!-- Banner -->
    <tr>
      <td style="text-align: center;">
        <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/order-placed/banner.png"
             alt="Banner" style="width: 100%; height: auto;" />
      </td>
    </tr>

    <!-- Confirmation Text -->
    <tr>
      <td align="center" style="padding: 50px 40px;">
        <h1 class="title" style="font-size: 32px; font-weight: 600; color: #252525; margin-bottom: 20px;">
          Your Order Is Confirmed!
        </h1>
        <p class="desc" style="font-size: 16px; color: #4f4f4f; line-height: 26px; margin: 0;">
          We’re getting your order ready to be shipped. We will notify you once it’s on the way.
        </p>
      </td>
    </tr>
    <!-- CTA Button -->
    <tr>
      <td style="text-align: center; padding-bottom: 40px;">
        <a href="#" class="cta"
           style="text-decoration: none; background: #ac8763; padding: 12px 50px; color: #fff; font-size: 14px; text-transform: uppercase; display: inline-block;">
          View Order
        </a>
      </td>
    </tr>

    <!-- Divider -->
    <tr>
      <td style="padding: 0 0 40px;">
        <hr style="border: none; border-top: 1px solid #d8d8d8; width: 80%; margin: 0 auto;" />
      </td>
    </tr>

    <!-- Footer Section -->
    <tr>
      <td style="background-color: #1e1e1e; text-align: center; padding: 30px 0;">
        <!-- Social Icons -->
        <a href="#" style="margin: 0 10px;">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/order-placed/logo-insta.png" width="20" alt="Instagram" />
        </a>
        <a href="#" style="margin: 0 10px;">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/order-placed/logo-facebook.png" width="20" alt="Facebook" />
        </a>
        <a href="#" style="margin: 0 10px;">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/order-placed/logo-x.png" width="20" alt="Twitter/X" />
        </a>
        <!-- Footer Text -->
        <p style="color: #ffffff; font-size: 14px; line-height: 24px; margin-top: 20px; font-weight: 400;">
          is simply dummy text of the printing and typesetting industry.
        </p>

        <p style="color: #ffffff; font-size: 14px; font-weight: 400; margin-top: 5px;">
          To stop receiving these emails,
          <a href="#" style="color: #ffffff; font-weight: bold; text-decoration: underline;">unsubscribe here</a>
        </p>
      </td>
    </tr>

    <!-- Fallback Link -->
    <tr>
      <td style="padding: 20px; text-align: center;">
        <p style="font-size: 12px; color: #7a7a7a;">
          If you're having trouble clicking the "View Order" button, copy and paste this URL into your browser:
          <br />
          <a href="#" style="color: #ac8763;">https://yourbrand.com/view-order</a>
        </p>
      </td>
    </tr>
  </table>
</body>
</html>
```

## Order Shipped Template

An update email informing customers that their order has been dispatched.

**Use Case:** Notifies customers that their product is on its way and includes tracking details to reduce post-purchase anxiety.

**Components:**

- [Replace the Logo](doc:ootb#1-replace-the-logo)
- [Update Banner/Product Images](doc:ootb#2-update-bannerproduct-images)
- [Update Call-To-Actions (CTAs)](https://staging.docs.user.clevertap.net/docs/ootb#3-call-to-actions-ctas)
- [Update Links in the Header/Footer](doc:ootb#4-update-links-in-the-headerfooter)
- [Change the Theme or Background Color](doc:ootb#5-change-the-theme-or-background-color)
- [Update the Privacy Policy](doc:ootb#update-the-privacy-policy)

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <title>Order Shipped</title>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta http-equiv="X-UA-Compatible" content="IE=edge" />
  <style>
    @font-face {
      font-family: 'Jost';
      src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Regular.ttf') format('woff');
      font-style: normal;
      font-weight: 400;
    }
    @font-face {
      font-family: 'Jost';
      src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Medium.ttf') format('woff');
      font-style: normal;
      font-weight: 500;
    }
    @font-face {
      font-family: 'Jost';
      src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-SemiBold.ttf') format('woff');
      font-style: normal;
      font-weight: 600;
    }
    @font-face {
      font-family: 'Jost';
      src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Bold.ttf') format('woff');
      font-style: normal;
      font-weight: 700;
    }
    @font-face {
      font-family: 'Poppins';
      src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Fonts/Poppins-Regular.woff') format('woff');
      font-style: normal;
      font-weight: 400;
    }
    @media screen and (max-width: 480px) {
      .container { margin-bottom: 20px !important; }
      .logo { width: 145px !important; height: 55px !important; }
      .cta { padding: 10px 25px !important; margin: 30px 0 !important; font-size: 16px !important; line-height: 20px !important; }
      .content-wrap { max-width: 90% !important; }
      .title { font-size: 22px !important; line-height: 28px !important; }
      .border-line { width: 40% !important; }
      .desc { font-size: 12px !important; line-height: 18px !important; margin: 0 0 30px !important; }
    }
  </style>
</head>
<body style="font-family: 'Jost', Arial, sans-serif; font-weight: 400; margin: 0; padding: 0;">
  <table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%" style="max-width: 600px; margin: 0 auto; background-color: #F5F5F5;">
        <!-- Logo -->
    <tr>
      <td align="center" style="padding: 24px 0;">
        <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/order-shipped/logo.png"
             alt="Logo" class="logo" style="width: 159px; height: 73px; object-fit: cover;" />
      </td>
    </tr>

    <!-- Banner -->
    <tr>
      <td style="text-align: center;">
        <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/order-shipped/banner.png"
             alt="Banner" style="width: 100%; height: auto;" />
      </td>
    </tr>

    <!-- Main Message -->
    <tr>
      <td align="center" style="padding: 50px 40px;">
        <h1 class="title" style="font-size: 32px; font-weight: 600; color: #252525; margin-bottom: 20px;">
          Your Order Is On Its Way!
        </h1>
        <p class="desc" style="font-size: 16px; color: #4f4f4f; line-height: 26px; margin: 0;">
          Good news! Your order has been shipped and is on the way to your doorstep.
        </p>
      </td>
    </tr>
    <!-- CTA Button -->
    <tr>
      <td style="text-align: center; padding-bottom: 40px;">
        <a href="#" class="cta"
           style="text-decoration: none; background: #ac8763; padding: 12px 50px; color: #fff; font-size: 14px; text-transform: uppercase; display: inline-block;">
          Track Order
        </a>
      </td>
    </tr>

    <!-- Divider -->
    <tr>
      <td style="padding: 0 0 40px;">
        <hr style="border: none; border-top: 1px solid #d8d8d8; width: 80%; margin: 0 auto;" />
      </td>
    </tr>

    <!-- Footer Section Start -->
    <tr>
      <td style="background-color: #1e1e1e; text-align: center; padding: 30px 0;">
        <!-- Social Icons -->
        <a href="#" style="margin: 0 10px;">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/order-shipped/logo-insta.png" width="20" alt="Instagram" />
        </a>
        <a href="#" style="margin: 0 10px;">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/order-shipped/logo-facebook.png" width="20" alt="Facebook" />
        </a>
        <a href="#" style="margin: 0 10px;">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/order-shipped/logo-x.png" width="20" alt="Twitter/X" />
        </a>
        <!-- Footer Text -->
        <p style="color: #ffffff; font-size: 14px; line-height: 24px; margin-top: 20px; font-weight: 400;">
          is simply dummy text of the printing and typesetting industry.
        </p>

        <p style="color: #ffffff; font-size: 14px; font-weight: 400; margin-top: 5px;">
          To stop receiving these emails,
          <a href="#" style="color: #ffffff; font-weight: bold; text-decoration: underline;">unsubscribe here</a>
        </p>
      </td>
    </tr>

    <!-- Fallback Link -->
    <tr>
      <td style="padding: 20px; text-align: center;">
        <p style="font-size: 12px; color: #7a7a7a;">
          If you're having trouble clicking the "Track Order" button, copy and paste this URL into your browser:
          <br />
          <a href="#" style="color: #ac8763;">https://yourbrand.com/track-order</a>
        </p>
      </td>
    </tr>
  </table>
</body>
</html>
```

## Password Reset Template

A security-focused transactional email that helps users reset their passwords securely and quickly.

### Use Case Examples

Sends a reset password link to users who have forgotten or initiated a reset request, ensuring account access is restored with minimal friction.

### Template Customization Options

- [Replace the Logo](doc:ootb#1-replace-the-logo)
- [Update Banner/Product Images](doc:ootb#2-update-bannerproduct-images)
- [Update Call-To-Actions (CTAs)](https://staging.docs.user.clevertap.net/docs/ootb#3-call-to-actions-ctas)
- [Update Links in the Header/Footer](doc:ootb#4-update-links-in-the-headerfooter)
- [Change the Theme or Background Color](doc:ootb#5-change-the-theme-or-background-color)
- [Update the Privacy Policy](doc:ootb#update-the-privacy-policy)
- [Update Social Media Links and Download Links](doc:ootb#update-social-media-links-and-download-links)

### Template Code

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <title>Password Reset</title>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta http-equiv="X-UA-Compatible" content="IE=edge" />
  <style>
    @media screen and (max-width: 480px) {
      .header { padding: 10px 0 !important; }
      .main-container { padding: 0 10px !important; }
      .footer-container { width: 95% !important; padding: 0 10px !important; }
    }
  </style>
</head>
<body style="margin: 0; padding: 0; font-family: 'Jost', Arial, sans-serif; background-color: #ffff;">
  <!-- Change Theme -->
  <table style="font-family: 'Jost', Arial, sans-serif; max-width: 600px; width: 100%; margin: 0 auto; background: #f5f5f5;">
    <!-- Logo -->
    <tr>
      <td align="center" class="header" style="padding: 24px 0;">
        <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/password-reset/logo.png"
             alt="Logo" class="logo" style="width: 159px; height: 73px; object-fit: cover;" />
      </td>
    </tr>

    <!-- Banner -->
    <tr>
      <td align="center">
        <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/password-reset/banner.png"
             alt="Banner" style="width: 100%; height: auto;" />
      </td>
    </tr>

    <!-- Title -->
    <tr>
      <td align="center" class="main-container" style="padding: 50px 40px;">
        <h1 style="font-size: 32px; font-weight: 600; color: #252525; margin-bottom: 20px;">
          Forgot your password?
        </h1>
        <p style="font-size: 16px; color: #4f4f4f; line-height: 26px; margin: 0;">
          Don't worry, resetting your password is easy. Just click the button below to get started.
        </p>
      </td>
    </tr>
    <!-- CTA Button -->
    <tr>
      <td align="center" style="padding-bottom: 40px;">
        <a href="#" style="text-decoration: none; background: #ac8763; padding: 12px 50px; color: #fff; font-size: 14px;
           text-transform: uppercase; display: inline-block;">
          Reset Password
        </a>
      </td>
    </tr>

    <!-- Divider -->
    <tr>
      <td style="padding: 0 0 40px;">
        <hr style="border: none; border-top: 1px solid #d8d8d8; width: 80%; margin: 0 auto;" />
      </td>
    </tr>

    <!-- Footer Start -->
    <tr>
      <td style="background-color: #1e1e1e; text-align: center; padding: 30px 0;">
        <!-- Social Icons -->
        <a href="#" style="margin: 0 10px;">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/password-reset/logo-insta.png"
               width="20" alt="Instagram" />
        </a>
        <a href="#" style="margin: 0 10px;">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/password-reset/logo-facebook.png"
               width="20" alt="Facebook" />
        </a>
        <a href="#" style="margin: 0 10px;">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/password-reset/logo-x.png"
               width="20" alt="Twitter/X" />
        </a>
        <!-- Footer Text -->
        <p style="color: #ffffff; font-size: 14px; line-height: 24px; margin-top: 20px; font-weight: 400;">
          is simply dummy text of the printing and typesetting industry.
        </p>

        <p style="color: #ffffff; font-size: 14px; font-weight: 400; margin-top: 5px;">
          To stop receiving these emails,
          <a href="#" style="color: #ffffff; font-weight: bold; text-decoration: underline;">unsubscribe here</a>
        </p>
      </td>
    </tr>

    <!-- Fallback Link -->
    <tr>
      <td style="padding: 20px; text-align: center;">
        <p style="font-size: 12px; color: #7a7a7a;">
          If you're having trouble clicking the "Reset Password" button, copy and paste this URL into your browser:
          <br />
          <a href="#" style="color: #ac8763;">https://yourbrand.com/reset-password</a>
        </p>
      </td>
    </tr>
  </table>
</body>
</html>
```

## Promotional Template

A high-impact marketing email used to announce ongoing deals, highlight product collections, or showcase limited-time offers.

### Use Case Examples

- Announce a limited-time festive discount.
- Promote newly launched products or collections.
- Re-engage users with a category-specific deal.

### Template Customization Options

- [Replace the Logo](doc:ootb#1-replace-the-logo)
- [Update Banner/Product Images](doc:ootb#2-update-bannerproduct-images)
- [Update Call-To-Actions (CTAs)](https://staging.docs.user.clevertap.net/docs/ootb#3-call-to-actions-ctas)
- [Update Links in the Header/Footer](doc:ootb#4-update-links-in-the-headerfooter)
- [Change the Theme or Background Color](doc:ootb#5-change-the-theme-or-background-color)
- [Update the Privacy Policy](doc:ootb#update-the-privacy-policy)
- [Update Social Media Links and Download Links](doc:ootb#update-social-media-links-and-download-links)

### Template Code

```html
<!DOCTYPE html>
<html lang="en" xmlns="http://www.w3.org/1999/xhtml">

<head>
    <meta charset="utf-8">
    <title></title>
    <meta name="description" content="">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <style type="text/css">
        * {
            box-sizing: border-box;
        }

        body {
            margin: 0;
            padding: 0;
            font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif;
            background-color: #f4f4f4;
        }

        table {
            border-spacing: 0;
        }

        td {
            padding: 0;
        }

        img {
            border: 0;
        }

        .wrapper {
            width: 100%;
            table-layout: fixed;
            background-color: #f4f4f4;
            padding-bottom: 40px;
        }

        .main {
            background-color: #ffffff;
            margin: 0 auto;
            width: 100%;
            max-width: 600px;
            border-spacing: 0;
            color: #4a4a4a;
        }
    </style>
</head>

<body>
    <center class="wrapper">
        <table class="main" width="100%">
            <!-- Logo -->
            <tr>
                <td style="padding: 20px 0; text-align: center;">
                    <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/logo.png" alt="Brand Logo"
                         width="150" style="height: auto; display: block; margin: 0 auto;" />
                </td>
            </tr>

            <!-- Hero Image -->
            <tr>
                <td>
                    <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/hero-banner.jpg" alt="Promo Banner"
                         width="100%" style="width: 100%; height: auto; display: block;" />
                </td>
            </tr>

            <!-- Headline Text -->
            <tr>
                <td style="padding: 30px 20px 10px; text-align: center;">
                    <h1 style="font-size: 24px; color: #252525; margin: 0;">Unmissable Offers Just For You!</h1>
                </td>
            </tr>

            <!-- Subheading Text -->
            <tr>
                <td style="padding: 0 20px 20px; text-align: center;">
                    <p style="font-size: 16px; color: #4f4f4f; margin: 0;">
                        Shop the latest collections at exciting discounts. Limited time only!
                    </p>
                </td>
            </tr>
            <!-- CTA Button -->
            <tr>
                <td style="padding: 20px 0 40px; text-align: center;">
                    <a href="https://yourdomain.com/shop-now"
                       style="background-color: #ac8763; color: #ffffff; text-decoration: none;
                       padding: 12px 30px; font-size: 14px; font-weight: bold; border-radius: 4px;
                       display: inline-block;">
                        Shop Now
                    </a>
                </td>
            </tr>

            <!-- Product Grid -->
            <tr>
                <td style="padding: 0 20px;">
                    <table width="100%" cellpadding="0" cellspacing="0">
                        <tr>
                            <td width="50%" style="padding: 10px;">
                                <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/product1.jpg" alt="Product 1"
                                     width="100%" style="border-radius: 8px; display: block;" />
                                <p style="font-size: 14px; text-align: center; margin: 8px 0 0;">Product One</p>
                            </td>
                            <td width="50%" style="padding: 10px;">
                                <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/product2.jpg" alt="Product 2"
                                     width="100%" style="border-radius: 8px; display: block;" />
                                <p style="font-size: 14px; text-align: center; margin: 8px 0 0;">Product Two</p>
                            </td>
                        </tr>
                    </table>
                </td>
            </tr>
            <!-- Footer Divider -->
            <tr>
                <td style="padding: 40px 0 20px;">
                    <hr style="border: none; border-top: 1px solid #ddd; width: 80%; margin: 0 auto;" />
                </td>
            </tr>

            <!-- Footer Social Links -->
            <tr>
                <td style="text-align: center; padding: 10px 0;">
                    <a href="#"><img src="https://d1qzvqecfo5h8o.cloudfront.net/images/logo-facebook.png" width="24" alt="Facebook" style="margin: 0 8px;" /></a>
                    <a href="#"><img src="https://d1qzvqecfo5h8o.cloudfront.net/images/logo-insta.png" width="24" alt="Instagram" style="margin: 0 8px;" /></a>
                    <a href="#"><img src="https://d1qzvqecfo5h8o.cloudfront.net/images/logo-x.png" width="24" alt="Twitter" style="margin: 0 8px;" /></a>
                </td>
            </tr>

            <!-- Footer Text -->
            <tr>
                <td style="text-align: center; font-size: 12px; color: #999999; padding: 0 20px 20px;">
                    <p style="margin: 0;">This is a promotional email from [Your Brand].</p>
                    <p style="margin: 0;">If you no longer wish to receive these emails,
                        <a href="#" style="color: #ac8763; text-decoration: underline;">unsubscribe here</a>.
                    </p>
                </td>
            </tr>
        </table>
    </center>
</body>
</html>
```

## Referral Template

This growth marketing template is crafted to boost customer acquisition through referral programs.

### Use Case Examples

 Sends referral emails encouraging users to invite friends by offering incentives to referrers and referees.

### Template Customization Options

- [Replace the Logo](doc:ootb#1-replace-the-logo)
- [Update Banner/Product Images](doc:ootb#2-update-bannerproduct-images) 
- [Update Call-To-Actions (CTAs)](https://staging.docs.user.clevertap.net/docs/ootb#3-call-to-actions-ctas)
- [Update Links in the Header/Footer](doc:ootb#4-update-links-in-the-headerfooter)
- [Change the Theme or Background Color](doc:ootb#5-change-the-theme-or-background-color)
- [Update the Privacy Policy](doc:ootb#update-the-privacy-policy) 

### Template Code

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <title>Referral</title>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta http-equiv="X-UA-Compatible" content="IE=edge" />
  <style>
    @font-face {
      font-family: 'Jost';
      src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Regular.ttf') format('woff');
      font-style: normal;
      font-weight: 400;
    }
    @font-face {
      font-family: 'Jost';
      src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Medium.ttf') format('woff');
      font-style: normal;
      font-weight: 500;
    }
    @font-face {
      font-family: 'Poppins';
      src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Fonts/Poppins-Regular.woff') format('woff');
      font-style: normal;
      font-weight: 400;
    }
    @media screen and (max-width: 480px) {
      .container { max-width: 95% !important; margin-bottom: 20px !important; padding: 20px 10px !important; }
      .logo { width: 145px !important; height: 55px !important; }
      .cta { padding: 10px 25px !important; }
      .sec-title { margin-bottom: 15px !important; font-size: 20px !important; }
      .b-desc { max-width: 100% !important; }
      .icon { width: 50px !important; height: 50px !important; }
      .content-wrap { margin-left: 10px !important; }
    }
  </style>
</head>
<body style="margin: 0; padding: 0; font-family: 'Jost', Arial, sans-serif; background-color: #F5F5F5;">
  <table cellspacing="0" cellpadding="0" border="0" width="100%"
         style="max-width: 600px; margin: 0 auto; background-color: #F5F5F5;">
    
    <!-- Logo -->
    <tr>
      <td align="center" style="padding: 24px 0;">
        <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/referral/logo.png"
             alt="Logo" class="logo" style="width: 159px; height: 73px; object-fit: cover;" />
      </td>
    </tr>

    <!-- Banner -->
    <tr>
      <td align="center">
        <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/referral/banner.png"
             alt="Referral Banner" style="width: 100%; height: auto;" />
      </td>
    </tr>

    <!-- Title Section -->
    <tr>
      <td align="center" style="padding: 50px 40px;">
        <h1 class="sec-title" style="font-size: 32px; font-weight: 600; color: #252525; margin-bottom: 20px;">
          Refer & Earn
        </h1>
        <p style="font-size: 16px; color: #4f4f4f; line-height: 26px; margin: 0;">
          Invite your friends and earn exciting rewards when they join and make their first purchase!
        </p>
      </td>
    </tr>
    <!-- CTA Button -->
    <tr>
      <td align="center" style="padding-bottom: 40px;">
        <a href="#" class="cta"
           style="text-decoration: none; background: #ac8763; padding: 12px 50px; color: #fff;
           font-size: 14px; text-transform: uppercase; display: inline-block;">
          Refer Now
        </a>
      </td>
    </tr>

    <!-- Divider -->
    <tr>
      <td style="padding: 0 0 40px;">
        <hr style="border: none; border-top: 1px solid #d8d8d8; width: 80%; margin: 0 auto;" />
      </td>
    </tr>

    <!-- Footer Start -->
    <tr>
      <td style="background-color: #1e1e1e; text-align: center; padding: 30px 0;">
        <!-- Social Icons -->
        <a href="#" style="margin: 0 10px;">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/referral/logo-insta.png" width="20" alt="Instagram" />
        </a>
        <a href="#" style="margin: 0 10px;">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/referral/logo-facebook.png" width="20" alt="Facebook" />
        </a>
        <a href="#" style="margin: 0 10px;">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/referral/logo-x.png" width="20" alt="Twitter/X" />
        </a>
        <!-- Footer Text -->
        <p style="color: #ffffff; font-size: 14px; line-height: 24px; margin-top: 20px; font-weight: 400;">
          is simply dummy text of the printing and typesetting industry.
        </p>

        <p style="color: #ffffff; font-size: 14px; font-weight: 400; margin-top: 5px;">
          To stop receiving these emails,
          <a href="#" style="color: #ffffff; font-weight: bold; text-decoration: underline;">unsubscribe here</a>
        </p>
      </td>
    </tr>

    <!-- Fallback Link -->
    <tr>
      <td style="padding: 20px; text-align: center;">
        <p style="font-size: 12px; color: #7a7a7a;">
          If you're having trouble clicking the "Refer Now" button, copy and paste this URL into your browser:
          <br />
          <a href="#" style="color: #ac8763;">https://yourbrand.com/refer</a>
        </p>
      </td>
    </tr>
  </table>
</body>
</html>
```

## Show Recommendations Template

This personalized content email template is designed to showcase relevant video and music or suggest content based on user engagement and interests. It is available in both dark and light modes for aesthetic preference.

### Use Case Examples

- Suggest items based on browsing, cart, or purchase history 
- Recommend articles, videos, or learning modules based on prior engagement or interests.
- Promote complementary or premium products to increase average order value 
- Engage users post-transaction with related product or content recommendations.
- Bring users back by showcasing trending or personalized items based on past behavior.
- Tailor deals or discounts based on recommended categories or affinity tags.
- Delivers curated video, show, or episode suggestions to users to enhance discovery, engagement, and viewership based on recent behavior.

### Template Customization Options

- [Replace the Logo](doc:ootb#1-replace-the-logo)
- [Update Banner/Product Images](doc:ootb#2-update-bannerproduct-images)
- [Update Call-To-Actions (CTAs)](https://staging.docs.user.clevertap.net/docs/ootb#3-call-to-actions-ctas)
- [Update Links in the Header/Footer](doc:ootb#4-update-links-in-the-headerfooter)
- [Change the Theme or Background Color](doc:ootb#5-change-the-theme-or-background-color)
- [Update the Privacy Policy](doc:ootb#update-the-privacy-policy)
- [Update Social Media Links and Download Links](doc:ootb#update-social-media-links-and-download-links)

### Template

```html Dark Mode
<!DOCTYPE html>
<html lang="en">
<head>
  <title>Show Recommendation</title>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta http-equiv="X-UA-Compatible" content="IE=edge" />
  <style>
    @font-face {
      font-family: 'Poppins';
      src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Fonts/Poppins-Light.woff') format('woff');
      font-style: normal;
      font-weight: 300;
    }
    @font-face {
      font-family: 'Poppins';
      src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Fonts/Poppins-Regular.woff') format('woff');
      font-style: normal;
      font-weight: 400;
    }
    @font-face {
      font-family: 'Poppins';
      src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Fonts/Poppins-Medium.woff') format('woff');
      font-style: normal;
      font-weight: 500;
    }
    @media screen and (max-width: 480px) {
      .container { max-width: 100% !important; }
      .heading h2 { font-size: 18px !important; line-height: 24px !important; }
      .borderSpan { width: 20% !important; }
    }
  </style>
</head>
<body style="margin: 0; padding: 0; background-color: #000;">
  <table width="100%" cellspacing="0" cellpadding="0" border="0" align="center"
         style="max-width: 600px; margin: 0 auto; background-color: #000; font-family: 'Poppins', sans-serif;">
    
    <!-- Logo -->
    <tr>
      <td align="center" style="padding: 24px 0;">
        <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-rec/logo.png"
             alt="Logo" style="width: 159px; height: 73px; object-fit: cover;" />
      </td>
    </tr>

    <!-- Heading -->
    <tr>
      <td align="center" style="padding: 20px;">
        <div class="heading" style="color: #ffffff;">
          <h2 style="margin: 0; font-size: 24px; line-height: 32px; font-weight: 500;">
            Recommended Just for You
          </h2>
        </div>
      </td>
    </tr>
    <!-- Product Grid -->
    <tr>
      <td align="center" style="padding: 20px;">
        <table cellspacing="0" cellpadding="0" border="0" width="100%" style="max-width: 520px;">
          <tr>
            <td align="center" style="padding: 10px;">
              <a href="#">
                <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-rec/product1.png"
                     alt="Show 1" style="width: 100%; height: auto;" />
              </a>
            </td>
            <td align="center" style="padding: 10px;">
              <a href="#">
                <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-rec/product2.png"
                     alt="Show 2" style="width: 100%; height: auto;" />
              </a>
            </td>
          </tr>
          <tr>
            <td align="center" style="padding: 10px;">
              <a href="#">
                <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-rec/product3.png"
                     alt="Show 3" style="width: 100%; height: auto;" />
              </a>
            </td>
            <td align="center" style="padding: 10px;">
              <a href="#">
                <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-rec/product4.png"
                     alt="Show 4" style="width: 100%; height: auto;" />
              </a>
            </td>
          </tr>
        </table>
      </td>
    </tr>
    <!-- Divider -->
    <tr>
      <td align="center" style="padding: 0 0 40px;">
        <hr style="border: none; border-top: 1px solid #444444; width: 80%; margin: 0 auto;" />
      </td>
    </tr>

    <!-- Footer -->
    <tr>
      <td style="background-color: #1e1e1e; text-align: center; padding: 30px 0;">
        <!-- Social Icons -->
        <a href="#" style="margin: 0 10px;">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-rec/logo-insta.png" width="20" alt="Instagram" />
        </a>
        <a href="#" style="margin: 0 10px;">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-rec/logo-facebook.png" width="20" alt="Facebook" />
        </a>
        <a href="#" style="margin: 0 10px;">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-rec/logo-x.png" width="20" alt="Twitter/X" />
        </a>
        <!-- Footer Text -->
        <p style="color: #ffffff; font-size: 14px; line-height: 24px; margin-top: 20px; font-weight: 400;">
          is simply dummy text of the printing and typesetting industry.
        </p>

        <p style="color: #ffffff; font-size: 14px; font-weight: 400; margin-top: 5px;">
          To stop receiving these emails,
          <a href="#" style="color: #ffffff; font-weight: bold; text-decoration: underline;">unsubscribe here</a>
        </p>
      </td>
    </tr>

    <!-- Fallback URL -->
    <tr>
      <td style="padding: 20px; text-align: center;">
        <p style="font-size: 12px; color: #7a7a7a;">
          If you're having trouble viewing the recommendations, copy and paste this URL into your browser:
          <br />
          <a href="#" style="color: #ac8763;">https://yourdomain.com/recommendations</a>
        </p>
      </td>
    </tr>
  </table>
</body>
</html>
```
```html Light Mode
<!DOCTYPE html>
<html lang="en">
<head>
  <title>Show Recommendation</title>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <style>
    @font-face {
      font-family: 'Poppins';
      src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Fonts/Poppins-Light.woff') format('woff');
      font-style: normal;
      font-weight: 300;
    }
    @font-face {
      font-family: 'Poppins';
      src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Fonts/Poppins-Regular.woff') format('woff');
      font-style: normal;
      font-weight: 400;
    }
    @font-face {
      font-family: 'Poppins';
      src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Fonts/Poppins-Medium.woff') format('woff');
      font-style: normal;
      font-weight: 500;
    }
    @media screen and (max-width: 480px) {
      .container { max-width: 100% !important; }
      .heading h2 { font-size: 18px !important; line-height: 24px !important; }
      .borderSpan { width: 20% !important; }
    }
  </style>
</head>
<body style="margin: 0; padding: 0; background-color: #ffffff;">
  <table width="100%" cellspacing="0" cellpadding="0" border="0" align="center"
         style="max-width: 600px; margin: 0 auto; background-color: #ffffff; font-family: 'Poppins', sans-serif;">

    <!-- Logo -->
    <tr>
      <td align="center" style="padding: 24px 0;">
        <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-rec-white/logo.png"
             alt="Logo" style="width: 159px; height: 73px; object-fit: cover;" />
      </td>
    </tr>

    <!-- Heading -->
    <tr>
      <td align="center" style="padding: 20px;">
        <div class="heading" style="color: #252525;">
          <h2 style="margin: 0; font-size: 24px; line-height: 32px; font-weight: 500;">
            Recommended Just for You
          </h2>
        </div>
      </td>
    </tr>
<body style="margin: 0; padding: 0; background-color: #ffffff;">
  <table width="100%" cellspacing="0" cellpadding="0" border="0" align="center"
         style="max-width: 600px; margin: 0 auto; background-color: #ffffff; font-family: 'Poppins', sans-serif;">

    <!-- Logo -->
    <tr>
      <td align="center" style="padding: 24px 0;">
        <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-rec-white/logo.png"
             alt="Logo" style="width: 159px; height: 73px; object-fit: cover;" />
      </td>
    </tr>

    <!-- Heading -->
    <tr>
      <td align="center" style="padding: 20px;">
        <div class="heading" style="color: #252525;">
          <h2 style="margin: 0; font-size: 24px; line-height: 32px; font-weight: 500;">
            Recommended Just for You
          </h2>
        </div>
      </td>
    </tr>
    <!-- Product Grid -->
    <tr>
      <td align="center" style="padding: 20px;">
        <table cellspacing="0" cellpadding="0" border="0" width="100%" style="max-width: 520px;">
          <tr>
            <td align="center" style="padding: 10px;">
              <a href="#">
                <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-rec-white/product1.png"
                     alt="Show 1" style="width: 100%; height: auto;" />
              </a>
            </td>
            <td align="center" style="padding: 10px;">
              <a href="#">
                <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-rec-white/product2.png"
                     alt="Show 2" style="width: 100%; height: auto;" />
              </a>
            </td>
          </tr>
          <tr>
            <td align="center" style="padding: 10px;">
              <a href="#">
                <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-rec-white/product3.png"
                     alt="Show 3" style="width: 100%; height: auto;" />
              </a>
            </td>
            <td align="center" style="padding: 10px;">
              <a href="#">
                <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-rec-white/product4.png"
                     alt="Show 4" style="width: 100%; height: auto;" />
              </a>
            </td>
          </tr>
        </table>
      </td>
    </tr>
    <!-- Divider -->
    <tr>
      <td align="center" style="padding: 0 0 40px;">
        <hr style="border: none; border-top: 1px solid #cccccc; width: 80%; margin: 0 auto;" />
      </td>
    </tr>

    <!-- Footer Section -->
    <tr>
      <td style="background-color: #f5f5f5; text-align: center; padding: 30px 0;">
        <!-- Social Media Icons -->
        <a href="#" style="margin: 0 10px;">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-rec-white/logo-insta.png" width="20" alt="Instagram" />
        </a>
        <a href="#" style="margin: 0 10px;">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-rec-white/logo-facebook.png" width="20" alt="Facebook" />
        </a>
        <a href="#" style="margin: 0 10px;">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-rec-white/logo-x.png" width="20" alt="Twitter/X" />
        </a>
        <!-- Footer Text -->
        <p style="color: #4f4f4f; font-size: 14px; line-height: 24px; margin-top: 20px; font-weight: 400;">
          is simply dummy text of the printing and typesetting industry.
        </p>

        <p style="color: #4f4f4f; font-size: 14px; font-weight: 400; margin-top: 5px;">
          To stop receiving these emails,
          <a href="#" style="color: #4f4f4f; font-weight: bold; text-decoration: underline;">unsubscribe here</a>
        </p>
      </td>
    </tr>

    <!-- Fallback Link -->
    <tr>
      <td style="padding: 20px; text-align: center;">
        <p style="font-size: 12px; color: #7a7a7a;">
          If you're having trouble viewing the recommendations, copy and paste this URL into your browser:
          <br />
          <a href="#" style="color: #ac8763;">https://yourdomain.com/recommendations</a>
        </p>
      </td>
    </tr>
  </table>
</body>
</html>
```

## What’s in Store Template

This product-focused promotional template showcases category-wise products, Men, Women, Kids, in a visual grid layout with distinct CTAs.

### Use Case Examples

- Promote seasonal or new arrivals across different product categories.
- Highlight interest-based collections (for example, Men, Women, Kids, Pets).
- Encourage exploration through curated visual sections such as Trending Now, Recommended for You, or Back in Stock.

### Template Customization Options

- [Replace the Logo](doc:ootb#1-replace-the-logo)
- [Update Banner/Product Images](doc:ootb#2-update-bannerproduct-images)
- [Update Call-To-Actions (CTAs)](https://staging.docs.user.clevertap.net/docs/ootb#3-call-to-actions-ctas)
- [Update Links in the Header/Footer](doc:ootb#4-update-links-in-the-headerfooter)
- [Change the Theme or Background Color](doc:ootb#5-change-the-theme-or-background-color)
- [Update the Privacy Policy](doc:ootb#update-the-privacy-policy)
- [Update Social Media Links and Download Links](doc:ootb#update-social-media-links-and-download-links)

### Template Code

```html HTML
!DOCTYPE html>
<html lang="en">

<head>
    <title>What's in the store</title>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <style>
        @font-face {
               font-family: 'Jost';
               src:
    url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Light.ttf')
    format('woff');
               font-style: normal;
               font-weight: 300;
           }
           @font-face {
               font-family: 'Jost';
               src:
    url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Regular.ttf')
    format('woff');
               font-style: normal;
               font-weight: 400;
           }
           @font-face {
               font-family: 'Jost';
              src:url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Medium.ttf')
    format('woff');
               font-style: normal;
               font-weight: 500;
           }
           @font-face {
               font-family: 'Jost';
               src:
    url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-SemiBold.ttf'
    ) format('woff');
               font-style: normal;
               font-weight: 600;
           }
           @font-face {
               font-family: 'Jost';
               src:
    url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Bold.ttf')
    format('woff');
               font-style: normal;
               font-weight: 700;
           }
           @media screen and (max-width: 480px) {
               .main {
                   max-width: 95% !important;
                   margin: 0 auto 20px !important;
               }
               .product-title {
                   margin: 0 10px 15px !important;
    }
               .shop-cta {
                   padding: 5px 10px !important;
    }
               .order-wrap {
                   padding: 15px 20px !important;
                 } }
    </style>
</head>

<body style="margin: 0; padding: 0; font-family:'Jost', Arial, sans-serif;
background-color: #774343;">
    <!-- Change Theme -->
    <table border="0" cellpadding="0" cellspacing="0" width="100%" style="font-family:'Jost', Arial, sans-serif; max-width: 600px; margin: 0 auto;
background: #FFFFFF;">
        <tr>
            <td align="center" style="padding: 17px 0;">
                <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/logo.png" alt="Logo" auto; " />
           </td>
</tr> <tr>
25px;">
                <td align="center" style="background-color: #d66437; padding: 38px 25px
    <h2
style=" display: block; max-width: 159px; width: 100%; height: style="margin: 0; font-size: 36px; font-weight: 400; line-height:
45px; color: #FFFFFF; text-transform: uppercase;">
                    What's in the store</h2>
                    <p style="margin: 10px 0 0; font-size: 14px; font-weight: 400;
line-height: 22px; color: #FFFFFF; text-transform: capitalize;">
                        Is simply dummy text of the fashion Industry</p>
                </td>
        </tr>
        <tr>
            <td align="center" style="background-color: #d66437;">
                <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/banner-imag
e.png" height: auto; " />
        alt="Banner " style="display: block; max-width: 600px; width: 100%; </td>
        </tr>
        <tr>
            <td align="center" style="background-color: #d66437; padding: 15px 35px;" class="order-wrap">
                <table border="0" cellpadding="0" cellspacing="0" width="100%">
                    <tr>
                        <td align="left" style="font-size: 14px; font-weight: 300;
line-height: 20px; color: #FFFFFF;">
                            all orders! Get <span style="font-weight: 500;">FREE Delivery</span> on
                        </td>
                        <td align="right">
                            <a href="#" class="shop-cta" style="max-width: 125px; display: inline-block;
padding: 8px 30px; font-size: 12px; font-weight: 400; line-height: 24px; color:
#000000; background-color: #FFFFFF; text-align: center; text-transform: uppercase;
text-decoration: none;">Shop
                               Now </a>
                        </td>
                    </tr>
                </table>
            </td>
        </tr>
        <!-- product section  -->
        <tr>
            <td align="center" style="padding: 40px 0 34px;">
                <h3 style="margin: 0; font-size: 32px; font-weight: 400; line-height:
42px; color: #0d0d0d; text-transform: uppercase;">
                   Products</h3>
                <p style="margin: 10px 0 0; font-size: 10px; font-weight: 400;
line-height: 20px; color: #909090; text-transform: capitalize;">
                    Is simply dummy text of the new age fashion industry.</p>
            </td>
        </tr>
        <!-- mens product -->
        <tr>
            <td align="center">
                <table border="0" cellpadding="0" cellspacing="0" width="100%" class="main">
                    style="width: 100%; max-width: 85%; margin: 0 auto 30px;"
                    <tr>
                        <td colspan="2">
                            <h2 class="product-title" style="margin: 0 10px 24px; font-family:'Jost', Arial,
sans-serif; font-size: 20px; font-weight: 400; line-height: 24px; color: #000000;
text-transform: uppercase;">
                               Men</h2>
                        </td>
                    </tr>
                    <tr>
                        <td align="right" width="50%" style="padding: 0 10px 29px;">
                            <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/men-product
-1.png" height: auto; " />
    alt="Product Image "
    style="display: block; max-width: 238px; width: 100%; <a href="#" style="font-size: 22px; font-weight: 300; line-height:
37px; color: #D66437; text-decoration: none; margin-top: 5px; display:
inline-block;">Shop now
                            <imgsrc="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/icon-arrow.
png" />
                            </a>
                            alt="arrow" style="max-width: 30px; height: 100%;"
                        </td>
                        <td align="right" width="50%" style="padding: 0 10px 29px;">
                            <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/men-product
-2.png" height: auto; " />
    alt="Product Image "
    style="display: block; max-width: 238px; width: 100%; <a href="#" style="font-size: 22px; font-weight: 300; line-height:
37px; color: #D66437; text-decoration: none; margin-top: 5px; display:
inline-block;">Shopnow <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/icon-arrow.
png" /></a>
                            alt="arrow" style="max-width: 30px; height: 100%;" -3.png" height: auto;" /> alt="Product Image" style="display: block; max-width: 238px; width: 100%;
                            <a href="#" style="font-size: 22px; font-weight: 300; line-height:
</td> </tr>
<tr>
    <td align=" right " width="50% " style="padding: 0 10px 29px; ">
                           <img
src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/men-product 37px; color: #D66437; text-decoration: none; margin-top: 5px; display: inline-block; ">Shop
                               now <img
src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/icon-arrow. png "
/></a>
            alt="arrow " style="max-width: 30px; height: 100%; "
</td>
<td align="right " width="50% " style="padding: 0 10px 29px; ">
                           <img
src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/men-product -4.png "
height: auto;" /> alt="Product Image" style="display: block; max-width: 238px; width: 100%;
                            <a href="#" style="font-size: 22px; font-weight: 300; line-height:
37px; color: #D66437; text-decoration: none; margin-top: 5px; display:
inline-block;">Shop
now <imgrc="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/icon-arrow.
png"
/></a> alt="arrow" style="max-width: 30px; height: 100%;" -3.png" height: auto;" /> alt="Product Image" style="display: block; max-width: 238px; width: 100%;
                            <a href="#" style="font-size: 22px; font-weight: 300; line-height:
</td> </tr>
<tr>
    <td align=" right " width="50% " style="padding: 0 10px 29px; ">
                           <img
src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/men-product 37px; color: #D66437; text-decoration: none; margin-top: 5px; display: inline-block; ">Shop
                               now <img
src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/icon-arrow. png "
/></a>
            alt="arrow " style="max-width: 30px; height: 100%; "
</td>
<td align="right " width="50% " style="padding: 0 10px 29px; ">
                           <img
src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/men-product-4.png "
height: auto;" /> alt="Product Image" style="display: block; max-width: 238px; width: 100%;
                            <a href="#" style="font-size: 22px; font-weight: 300; line-height:
37px; color: #D66437; text-decoration: none; margin-top: 5px; display:
inline-block;">Shop
now <imgsrc="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/icon-arrow.
png"
/></a> class="main"> style="width: 100%; max-width: 85%; margin: 0 auto 30px;"
                            <tr>
                                <td colspan="2">
                                    <h2 class="product-title" </td> </tr>
    </table>
</td>
</tr>
<!-- mens product -->
<!-- women product -->
<tr>
alt="arrow" style="max-width: 30px; height: 100%;"
<td align="center">
    <table border="0" cellpadding="0" cellspacing="0" width="100%"
                               style="margin: 0 10px 24px; font-family:'Jost', Arial,
sans-serif; font-size: 20px; font-weight: 400; line-height: 24px; color: #000000;
text-transform: uppercase;">
                               Women</h2>
                                </td>
                            </tr>
                            <tr>
                                <td align="right" width="50%" style="padding: 0 10px 29px;"><img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/women-produ
ct-1.png" height: auto; " />
    alt="Product Image "
    style="display: block; max-width: 238px; width: 100%; <a href="#" style="font-size: 22px; font-weight: 300; line-height:
37px; color: #D66437; text-decoration: none; margin-top: 5px; display:
inline-block;">Shop now
                                    <imgsrc="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/icon-arrow.
png" />
                                    </a>
                                    alt="arrow" style="max-width: 30px; height: 100%;"
                                </td>
                                <td align="right" width="50%" style="padding: 0 10px 29px;">
                                    <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/women-produ
ct-2.png" height: auto; " />
    alt="Product Image "
    style="display: block; max-width: 238px; width: 100%; <a href="#" style="font-size: 22px; font-weight: 300; line-height:
37px; color: #D66437; text-decoration: none; margin-top: 5px; display:
inline-block;">Shop now <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/icon-arrow.
png" /></a>
                                    alt="arrow" style="max-width: 30px; height: 100%;"
                                </td>
                            </tr>
                            <tr>
                                <td align="right" width="50%" style="padding: 0 10px 29px;">
                                    <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/women-produ
ct-3.png" height: auto; " />
    alt="Product Image "
    style="display: block; max-width: 238px; width: 100%; <a href="#" style="font-size: 22px; font-weight: 300; line-height:
37px; color: #D66437; text-decoration: none; margin-top: 5px; display:
inline-block;">Shop now <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/icon-arrow.
png" alt="arrow" style="max-width: 30px; height: 100%;" </td>
                                    <td align="right" width="50%" style="padding: 0 10px 29px;">
                                        <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/women-produ
ct-4.png" height: auto; " />
    alt="Product Image "
    style="display: block; max-width: 238px; width: 100%; <a href="#" style="font-size: 22px; font-weight: 300; line-height:
37px; color: #D66437; text-decoration: none; margin-top: 5px; display:
inline-block;">Shop now <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/icon-arrow.
png" /></a>
                                        alt="arrow" style="max-width: 30px; height: 100%;" class="main"> style="width: 100%; max-width: 85%; margin: 0 auto 30px;"
                                        <tr>
                                            <td colspan="2">
                                                <h2 class="product-title" </td> </tr>
    </table>
</td>
</tr>
<!-- women product -->
<!-- kids product -->
<tr>
<td align="center">
    <table border="0" cellpadding="0" cellspacing="0" width="100%"
                               style="margin: 0 10px 24px; font-family:'Jost', Arial,
sans-serif; font-size: 20px; font-weight: 400; line-height: 24px; color: #000000;
text-transform: uppercase;">
                               Kids</h2>
                                            </td>
                                        </tr>
                                        <tr>
                                            <td align="right" width="50%" style="padding: 0 10px 29px;">
                                                <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/kid-product
-1.png" height: auto; " />
    alt="Product Image "
    style="display: block; max-width: 238px; width: 100%; <a href="#" style="font-size: 22px; font-weight: 300; line-height:
37px; color: #D66437; text-decoration: none; margin-top: 5px; display:
inline-block;">Shop now <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/icon-arrow.
png" /></a>
                                                alt="arrow" style="max-width: 30px; height: 100%;"
                                            </td>
                                            <td align="right" width="50%" style="padding: 0 10px 29px;">
                                                <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/kid-product
-2.png" height: auto; " />
    alt="Product Image "
    style="display: block; max-width: 238px; width: 100%; <a href="#" style="font-size: 22px; font-weight: 300; line-height:
37px; color: #D66437; text-decoration: none; margin-top: 5px; display:
inline-block;">Shop now <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/icon-arrow.
png" /></a>
                                                alt="arrow" style="max-width: 30px; height: 100%;"
                                            </td>
                                        </tr>
                                        <tr>
                                            <td align="right" width="50%" style="padding: 0 10px 29px;">
                                                <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/kid-product
-3.png" height: auto; " />
    alt="Product Image "
    style="display: block; max-width: 238px; width: 100%; <a href="#" style="font-size: 22px; font-weight: 300; line-height:
37px; color: #D66437; text-decoration: none; margin-top: 5px; display:
inline-block;">Shop now <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/icon-arrow.
png" /></a>
                                                alt="arrow" style="max-width: 30px; height: 100%;"
                                            </td>
                                            <td align="right" width="50%" style="padding: 0 10px 29px;">
                                                <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/kid-product
-4.png" height: auto; " />
    alt="Product Image "
    style="display: block; max-width: 238px; width: 100%; <a href="#" style="font-size: 22px; font-weight: 300; line-height:
37px; color: #D66437; text-decoration: none; margin-top: 5px; display:
inline-block;">Shop now <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/icon-arrow.
png" /></a>
                                                alt="arrow" style="max-width: 30px; height: 100%;"
                                            </td>
                                        </tr>
                </table>
                </td>
                </tr>
                <!-- kids product -->
                <!-- product section  -->
                <!-- Footer Section  -->
                <tr>
                    <td align="center" style="border-top: 0.5px solid #D66437; padding: 39px 0;
text-align: center;">
                        <table border="0" cellpadding="0" cellspacing="0" align="center">
                            <!-- Add Links  -->
                            <!-- Download Android Section -->
                            <tr>
                                <td style="padding: 0 8px; display: inline-block;">
                                    <a href="#"><img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/logo-insta.
png" alt="Social Icon" style="display: block; width:
34px; height: 34px;" /></a>
                                </td>
                                <td style="padding: 0 8px; display: inline-block;">
                                    <a href="#"><img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/logo-facebo
ok.png" alt="Social Icon" style="display: block; width:
34px; height: 34px;" /></a>
                                </td>
                                <td style="padding: 0 8px; display: inline-block;">
                                    <a href="#"><img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/logo-x.png" alt="Social Icon" style="display: block; width:
34px; height: 34px;" /></a>
                                </td>
                            </tr>
                            <!-- Download Android Section -->
                            <!-- Add Links  -->
                            <tr>
                                <td colspan="3">
                                    <p style="font-family: 'Jost', Arial, sans-serif;
font-size: 14px; font-weight: 400; line-height: 24px; color: #939393; text-align:
center; max-width: 80%; margin: 34px auto 27px;">
                                        We're only getting started—rely on us to guide you every step of the way. Welcome to the [community/family/team]!
                                    </p>
                                </td>
                            </tr>
                            <!-- Privacy Policy  -->
                            <tr>
                                <td colspan="3" style="border-top: 0.5px solid #979797;
padding-top: 24px;padding-bottom:24px;">
                                    border="0" align="center">
                                    <table role="presentation" cellspacing="0" cellpadding="0" <tr>
                                        <td style="padding: 0 5px;"><a href="#" style="font-size: 14px; font-weight: 400;
line-height: 24px; text-align: center; color: #939393 !important; text-decoration:
none;">Privacy</a>
                                        </td>
                                        <td style="padding: 0 5px;"><a href="#" style="font-size: 14px; font-weight: 400;
line-height: 24px; text-align: center; color: #939393 !important; text-decoration:
none;">Account</a>
                                        </td>
                            </tr>
                            <!-- Privacy Policy  -->
                            <tr>
                                <td colspan="3" style="border-top: 0.5px solid #979797;
padding-top: 24px;">
                                    border="0" align="center">
                                    <table role="presentation" cellspacing="0" cellpadding="0" <tr>
                                        <td style="padding: 0 5px;">
                                            <p class="f-desc" </td>
                            </tr>
                            </table>
                            style="font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; color: #939393; max-width: 80%; margin: 0 auto;"> To stop receiving these emails, <a href="#" style="color:#939393;text-decoration:none;font-weight:bold">unsubscribe
                                               here</a></p>
                            </td>
                </tr>
                </table>
                </td>
                </tr>
                </table>
                </td>
        </tr>
        <!-- Footer Section  -->
    </table>
</body>

</html>
```

## Winback Template

This re-engagement email template is tailored to bring back inactive users who have not interacted recently with your brand or app.

### Use Case Examples

Encourages churned or inactive users to return by offering a compelling incentive such as a discount or limited-time offer, paired with personalized product recommendations.

### Template Customization Options

- [Replace the Logo](doc:ootb#1-replace-the-logo)
- [Update Banner/Product Images](doc:ootb#2-update-bannerproduct-images)
- [Update Call-To-Actions (CTAs)](https://staging.docs.user.clevertap.net/docs/ootb#3-call-to-actions-ctas)
- [Update Links in the Header/Footer](doc:ootb#4-update-links-in-the-headerfooter)
- [Change the Theme or Background Color](doc:ootb#5-change-the-theme-or-background-color)
- [Update the Privacy Policy](doc:ootb#update-the-privacy-policy)
- [Update Social Media Links and Download Links](doc:ootb#update-social-media-links-and-download-links)

### Template Code

```html HTML
<!DOCTYPE html>
<html lang="en">
<head>
   <title>WinBack</title>
   <meta charset="UTF-8">
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   <meta http-equiv="X-UA-Compatible" content="IE=edge">
   <style>
       @font-face {
           font-family: 'Jost';
           src:
url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Light.ttf')
format('woff');
           font-style: normal;
           font-weight: 300;
       }
       @font-face {
           font-family: 'Jost';
           src:
url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Regular.ttf')
format('woff');
           font-style: normal;
           font-weight: 400;
       }
       @font-face {
           font-family: 'Jost';
           src:
url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Medium.ttf')
format('woff');
           font-style: normal;
           font-weight: 500;
         }
       @font-face {
           font-family: 'Jost';
           src:
url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-SemiBold.ttf'
) format('woff');
           font-style: normal;
           font-weight: 600;
       }
       @font-face {
           font-family: 'Jost';
           src:
url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Bold.ttf')
format('woff');
           font-style: normal;
           font-weight: 700;
       }
       @media screen and (max-width: 480px) {
           .container {
               max-width: 100% !important;
           }
           .content {
               max-width: 90% !important;
} }
   </style>
</head>
<body style="font-family: 'Jost', Arial, sans-serif; font-weight: 400; margin: 0;
padding: 0; background: #ddd;">
   <!-- Change Theme -->
   <table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%"
       style="max-width: 600px; margin: 0 auto; background-color: #ffffff;">
       <!-- header start-->
       <tr>
           <td align="center"
style="display: block; padding: 26px 0; max-width: 78%; margin: 0
auto;border-bottom: 1px solid #DDB67C;">
               <div class="logo-wrap">
                   <!-- Change Logo Image src as per your requirements -->
                   <img
src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Winback/logo.png"
alt="Logo"
                       style="width: 159px; height: 73px; object-fit: cover;">
                   <!-- Change Logo Image src as per your requirements -->
</div> </td>
       </tr>
       <!-- header end-->
       <tr>
           <td style="text-align: center;">
               <h1 class="banner-title"
                   style="font-family: Jost; font-size: 50px; font-weight: 400;
line-height: 70px; color: #525C46; text-transform: uppercase; margin: 25px 0 28px;">
                   special offer </h1>
               <div class="banner-img">
                   <!-- Change image src as per your requirements -->
                   <img
src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Winback/product-banner.
png"
                       alt="banner" style="width: 100%; height: 100%; max-height:
663px; object-fit: cover;">
</div> </td>
</tr> <tr>
           <td align="center" style="display: block; padding: 30px 0 64px; max-width:
78%; margin: 0 auto;">
               <h3
                   style="color: #525C46; font-family: 'Jost', Arial, sans-serif;
font-size: 60px; font-weight: 400; line-height: 86px; text-transform: uppercase;
margin: 0 0 17px;">
                   <span style="font-weight: 300;">30% </span>Off everything</h3>
               <p
                   style="font-family: 'Jost', Arial, sans-serif; font-size: 14px;
font-weight: 400; line-height: 20px;color:#909090; text-align: center; margin: 0;
margin-bottom: 31px;">
Indulge in the ultimate skincare ritual, where every moment is a
chance to nurture your beauty. From
                   age-defying serums to revitalizing face masks, our range is
meticulously formulated to support every
                   skin type. </p>
               <a href="#"
                   style="background-color: #AC8763; font-family: 'Jost', Arial,
sans-serif; font-size: 16px; font-weight: 400;line-height: 20px;text-align: center;
color: #FFFFFF !important; text-transform: capitalize; border-radius: 20px;
text-decoration: none; max-width: 171px; padding: 10px 40px;">Redeem
                   now</a>
           </td>
</tr> <tr>
           <td>
               <div style="max-width: 90%; margin: 0 auto; width: 100%;">
                   <table role="presentation" cellspacing="0" cellpadding="0"
border="0" align="center">
                       <tr>
                           <td style="width: 33%; vertical-align: top;">
                               <!-- product card -->
                               <table role="presentation" cellspacing="0"
cellpadding="0" border="0" align="center"
requirements -->
style="margin-bottom: 15px; padding: 0 5px;">
<tr>
    <td colspan="2">
        <div class="img-wrap">
            <!-- Change image src as per your
                                               <img
src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Winback/product-1.png"
vertical-align: top;">
                alt="product" />
        </div>
</td> </tr>
<tr>
    <td style="width: 60%; margin-bottom: 2px;
<h4 style="font-family: 'Jost', Arial,
sans-serif; font-size: 14px; font-weight: 400; line-height: 24px; color: #252525;
margin: 0;padding-right: 5px;">
fashion industry.</p>
</td> </tr>
    </table>
</td>
        Product name</h4>
</td>
<td style="width: 20%; vertical-align: top;">
    <p
                                               style="margin:0; color: #252525;
font-family: 'Jost', Arial, sans-serif; font-size: 12px;font-weight: 300; line-height:
24px; text-align: right;"> class="rupee-sign">₹</span>1500</p>
</td> </tr>
                                   <tr>
                                       <td colspan="2">
                                           <p class="desc"
                                               style="font-family: 'Jost', Arial,
sans-serif;text-transform: capitalize; font-size: 8px; font-weight: 400; line-height:
13px; color: #909090; margin: 0; ">
cellpadding="0" border="0" align="center"
                                   style="margin-bottom: 15px; padding: 0 5px;">
requirements -->
<span
is simply dummy text of the new age
<td style="width: 33%; vertical-align: top;">
    <!-- product card -->
    <table role="presentation" cellspacing="0"
<tr>
    <td colspan="2">
        <div class="img-wrap">
            <!-- Change image src as per your
                                               <img
src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Winback/product-1.png"
                                                   alt="product" />
                                           </div>
</td>
</tr> <tr>
    <td style="width: 60%; margin-bottom: 2px;
        <h4
                                               style="font-family: 'Jost', Arial,
sans-serif; font-size: 14px; font-weight: 400; line-height: 24px; color: #252525;
margin: 0;padding-right: 5px;">
fashion industry.</p>
requirements --><img
src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Winback/product-1.png"
vertical-align: top;">
                alt="product" />
        </div>
</td> </tr>
<tr>
    <td style="width: 60%; margin-bottom: 2px;
        <h4
            style="font-family: 'Jost', Arial,
sans-serif; font-size: 14px; font-weight: 400; line-height: 24px; color: #252525;
margin: 0;padding-right: 5px;">
                                               Product name</h4>
                                       </td>
                                       <td style="width: 20%; vertical-align: top;">
                                           <p
                                               style="margin:0; color: #252525;
font-family: 'Jost', Arial, sans-serif; font-size: 12px;font-weight: 300; line-height:
24px; text-align: right;"> class="rupee-sign">₹</span>1500</p>
</td> </tr>
                                   <tr>
                                       <td colspan="2">
                                           <p class="desc"
                                               style="font-family: 'Jost', Arial,
sans-serif;text-transform: capitalize; font-size: 8px; font-weight: 400; line-height:
13px; color: #909090; margin: 0; ">
fashion industry.</p>
                </tr>
            </table>
</div> </td>
</tr>
<tr> <td>
right;">
<div style="max-width: 90%; margin: 0 auto; width: 100%; text-align:
    <a href="#" class="btn-link"
        style="font-family: 'Jost', Arial, sans-serif;
font-size: 12px; font-weight: 400; line-height: 15px;
text-transform: capitalize; color: #AC8763 !important; text-decoration: none; ">See
More
                       <img
src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Winback/arrow.png"
</a> </div>
</td> </tr>
align="center"
width="100%"
<table role="presentation" cellspacing="0" cellpadding="0" border="0"
    style=" max-width: 78%; margin: 0 auto;">
    <tr>
        <td style="border-top: 1px solid #DDB67C; padding: 19px 0;">
            <table align="center" cellpadding="0" cellspacing="0"
                style="text-align: center;">
                <!-- Download Android Section -->
                <tr>
                    <td style="padding: 0 8px; display: inline-block;">
                        <a href="#"
                            style="vertical-align: middle;display:
                            <!-- Change image src as per your
inline-block; width: 34px; height: 34px;">
requirements -->
alt="arrow" class="margin-left: 10px" />
<!-- Footer Section -->
<tr>
    <td align="center" style="padding: 30px 0;">
                                           <img
src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Winback/logo-insta.png"
height: 100%;">
</a>
 </td>
                                   <td style="padding: 0 8px; display: inline-block;">
                                       <a href="#"
                                           style="vertical-align: middle;display:
inline-block; width: 34px; height: 34px;">
                                           <img
src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Winback/logo-facebook.p
ng"
height: 100%;">
inline-block;"><a href="#"
</a> </td>
inline-block; width: 34px; height: 34px;"><img
src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Winback/logo-x.png"
                                               alt="x" style="width: 100%; height:
100%;"></a>
</td> </tr>
        </table>
    </td>
</tr> <tr>
    <td style="border-top: 1px solid #DDB67C;">
        <p
                               style="font-size: 14px; font-weight: 400; line-height:
24px; text-align: center; color: #909090; margin: 19px 0 21px;">
                               We're only getting started—rely on us to guide you
every step of the way. Welcome to the
                               [community/family/team]!
</p> </td>
</tr> <tr>
                       <td>
                           <table role="presentation" cellspacing="0" cellpadding="0"
border="0" align="center">
<!-- Privacy Policy --><tr>
                                   <td style="padding: 0 5px;"><a href="#"
                                           style="font-size: 14px; font-weight: 400;
line-height: 24px; text-align: center; color: #1E1E1E !important; text-decoration:
none;">Privacy</a>
                                   </td>
                                   <td style="padding: 0 5px;"><a href="#"
                                           style="font-size: 14px; font-weight: 400;
line-height: 24px; text-align: center; color: #1E1E1E !important; text-decoration:
none;">Account</a>
                                   </td>
                                   <td style="padding: 0 5px;"><a href="#"
                                           style="font-size: 14px; font-weight: 400;
line-height: 24px; text-align: center; color: #1E1E1E !important; text-decoration:
none;">Unsubscribe</a>
</tr> <tr>
</td> 
</tr>
    </table>
</td>
<!-- Privacy Policy -->
                       <td style="border-top: 1px solid #DDB67C;">
                           <p
                               style="font-size: 14px; font-weight: 400; line-height:
24px; text-align: center; color: #1E1E1E; padding-top:10px;">
                               To stop receiving these emails, <a href="#"
style="color:#1E1E1E;font-weight:bold;text-decoration:none;">unsubscribe here</a>
</p>
</td> </tr>
</table>
</td> </tr>
       <!-- footer end-->
   </table>
</body>
</html>
```

## Subscription Template

This confirmation or promotional email template is used to acknowledge new subscriptions or upsell subscription-based services.

### Use Case Examples

Confirms a successful subscription or entices users to upgrade by highlighting plan benefits and encouraging exploration of exclusive features.

### Template Customization Options

- [Replace the Logo](doc:ootb#1-replace-the-logo)
- [Update Banner/Product Images](doc:ootb#2-update-bannerproduct-images)
- [Update Call-To-Actions (CTAs)](https://staging.docs.user.clevertap.net/docs/ootb#3-call-to-actions-ctas)
- [Update Links in the Header/Footer](doc:ootb#4-update-links-in-the-headerfooter)
- [Change the Theme or Background Color](doc:ootb#5-change-the-theme-or-background-color)
- [Update the Privacy Policy](doc:ootb#update-the-privacy-policy)
- [Update Social Media Links and Download Links](doc:ootb#update-social-media-links-and-download-links)

### Template Code

```html
<!doctype html>
<html lang="en">
<head>
  <title>Subscription Renewal</title>
  <style type="text/css">
    @font-face {
      font-family: 'Jost';
      src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Light.ttf') format('woff');
      font-style: normal;
      font-weight: 300;
    }
    @font-face {
      font-family: 'Jost';
      src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Regular.ttf') format('woff');
      font-style: normal;
      font-weight: 400;
    }
    @font-face {
      font-family: 'Jost';
      src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Medium.ttf') format('woff');
      font-style: normal;
      font-weight: 500;
    }
    @font-face {
      font-family: 'Jost';
      src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-SemiBold.ttf') format('woff');
      font-style: normal;
      font-weight: 600;
    }
    @font-face {
      font-family: 'Jost';
      src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Bold.ttf') format('woff');
      font-style: normal;
      font-weight: 700;
    }
    @media screen and (max-width: 480px) {
      .container { max-width: 100% !important; }
      .logo { width: 145px !important; height: 55px !important; }
      .cta { padding: 10px 25px !important; }
      .title { font-size: 24px !important; line-height: 36px !important; }
    }
  </style>
</head>

<body style="margin: 0; padding: 0; background-color: #f5f5f5;">
  <table width="100%" cellspacing="0" cellpadding="0" border="0" align="center"
         style="max-width: 600px; margin: 0 auto; background-color: #ffffff; font-family: 'Jost', sans-serif;">
    
    <!-- Logo -->
    <tr>
      <td align="center" style="padding: 24px 0;">
        <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/subscription/logo.png"
             alt="Logo" class="logo" style="width: 159px; height: 73px; object-fit: cover;" />
      </td>
    </tr>

    <!-- Banner -->
    <tr>
      <td align="center">
        <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/subscription/banner.png"
             alt="Banner" style="width: 100%; height: auto;" />
      </td>
    </tr>
    <!-- Title & Description -->
    <tr>
      <td align="center" style="padding: 40px 30px 30px;">
        <h1 class="title" style="font-size: 32px; font-weight: 600; color: #252525; margin: 0 0 20px;">
          Your Subscription Just Got Better!
        </h1>
        <p style="font-size: 16px; color: #4f4f4f; line-height: 26px; margin: 0;">
          We’ve added exciting new features to your current plan. Tap below to explore what’s new and make the most of your membership.
        </p>
      </td>
    </tr>

    <!-- CTA Button -->
    <tr>
      <td align="center" style="padding: 30px 0 50px;">
        <a href="https://yourdomain.com/explore"
           style="text-decoration: none; background: #ac8763; padding: 12px 50px; color: #fff;
           font-size: 14px; text-transform: uppercase; display: inline-block;">
          Explore Now
        </a>
      </td>
    </tr>

    <!-- Divider -->
    <tr>
      <td style="padding: 0 0 40px;">
        <hr style="border: none; border-top: 1px solid #d8d8d8; width: 80%; margin: 0 auto;" />
      </td>
    </tr>
    <!-- Footer Section -->
    <tr>
      <td style="background-color: #1e1e1e; text-align: center; padding: 30px 0;">
        <!-- Social Icons -->
        <a href="#" style="margin: 0 10px;">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/subscription/logo-insta.png" width="20" alt="Instagram" />
        </a>
        <a href="#" style="margin: 0 10px;">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/subscription/logo-facebook.png" width="20" alt="Facebook" />
        </a>
        <a href="#" style="margin: 0 10px;">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/subscription/logo-x.png" width="20" alt="Twitter/X" />
        </a>

        <!-- Footer Text -->
        <p style="color: #ffffff; font-size: 14px; line-height: 24px; margin-top: 20px; font-weight: 400;">
          is simply dummy text of the printing and typesetting industry.
        </p>
        <p style="color: #ffffff; font-size: 14px; font-weight: 400; margin-top: 5px;">
          To stop receiving these emails,
          <a href="#" style="color: #ffffff; font-weight: bold; text-decoration: underline;">unsubscribe here</a>
        </p>
      </td>
    </tr>
    <!-- Fallback Link -->
    <tr>
      <td style="padding: 20px; text-align: center;">
        <p style="font-size: 12px; color: #7a7a7a;">
          If you're having trouble clicking the "Explore Now" button, copy and paste this URL into your browser:
          <br />
          <a href="https://yourdomain.com/explore" style="color: #ac8763;">https://yourdomain.com/explore</a>
        </p>
      </td>
    </tr>
  </table>
</body>
</html>
```

## Scratch Card Template

This is an interactive email template designed to gamify the user experience by letting them "scratch" to reveal a reward, such as a coupon, discount, or points.

### Use Case Examples

- Engage users during festive or seasonal campaigns with surprise offers.
- Reactivate dormant users by giving them a chance to win a reward.
- Reward loyal customers with a fun, interactive coupon reveal.
- Launch a limited-time “scratch-to-win” contest to drive urgency and clicks.

### Template Customization Options

- [Replace the Logo](doc:ootb#1-replace-the-logo)
- [Update Banner/Product Images](doc:ootb#2-update-bannerproduct-images)
- [Update Call-To-Actions (CTAs)](https://staging.docs.user.clevertap.net/docs/ootb#3-call-to-actions-ctas)
- [Update Links in the Header/Footer](doc:ootb#4-update-links-in-the-headerfooter)
- [Change the Theme or Background Color](doc:ootb#5-change-the-theme-or-background-color)
- [Update the Privacy Policy](doc:ootb#update-the-privacy-policy)
- [Update Social Media Links and Download Links](doc:ootb#update-social-media-links-and-download-links)

### Template Code

```html
<!doctype html>
<html lang="en">
<head>
  <title>Scratch Card</title>
  <style type="text/css">
    @font-face {
      font-family: 'Poppins';
      src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Fonts/Poppins-Light.woff') format('woff');
      font-style: normal;
      font-weight: 300;
    }
    @font-face {
      font-family: 'Poppins';
      src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Fonts/Poppins-Regular.woff') format('woff');
      font-style: normal;
      font-weight: 400;
    }
    @font-face {
      font-family: 'Poppins';
      src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Fonts/Poppins-Medium.woff') format('woff');
      font-style: normal;
      font-weight: 500;
    }
    @media screen and (max-width: 480px) {
      .container { max-width: 100% !important; }
      .heading { font-size: 38px !important; line-height: 60px !important; }
      .coupon { font-size: 24px !important; line-height: 60px !important; }
      .coupon-code { font-size: 32px !important; line-height: 46px !important; }
    }
  </style>
</head>
<body style="margin: 0; padding: 0; background-color: #f5f5f5;">
  <table width="100%" cellspacing="0" cellpadding="0" border="0" align="center" style="max-width: 600px; margin: 0 auto; background-color: #ffffff; font-family: 'Poppins', sans-serif;">
    
    <!-- Logo -->
    <tr>
      <td align="center" style="padding: 24px 0;">
        <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/scratch-card/logo.png"
             alt="Brand Logo" style="width: 159px; height: 73px; object-fit: cover;" />
      </td>
    </tr>

    <!-- Banner -->
    <tr>
      <td align="center">
        <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/scratch-card/banner.png"
             alt="Scratch Card Banner" style="width: 100%; height: auto;" />
      </td>
    </tr>

    <!-- Heading -->
    <tr>
      <td align="center" style="padding: 40px;">
        <h1 class="heading" style="font-size: 48px; color: #252525; margin: 0 0 20px;">
          It’s Time to Scratch & Win!
        </h1>
        <p style="font-size: 16px; color: #4f4f4f; line-height: 26px; margin: 0;">
          Reveal your surprise reward hidden inside the scratch card. Click below to try your luck!
        </p>
      </td>
    </tr>

    <!-- Scratch Card CTA Image -->
    <tr>
      <td align="center" style="padding-bottom: 40px;">
        <a href="https://yourdomain.com/scratch">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/scratch-card/scratch-btn.png"
               alt="Scratch Now" style="width: 220px; height: auto;" />
        </a>
      </td>
    </tr>

    <!-- Divider -->
    <tr>
      <td style="padding: 0 0 40px;">
        <hr style="border: none; border-top: 1px solid #d8d8d8; width: 80%; margin: 0 auto;" />
      </td>
    </tr>
    <!-- Footer Section -->
    <tr>
      <td style="background-color: #1e1e1e; text-align: center; padding: 30px 0;">
        <!-- Social Media Icons -->
        <a href="#" style="margin: 0 10px;">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/scratch-card/logo-insta.png" width="20" alt="Instagram" />
        </a>
        <a href="#" style="margin: 0 10px;">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/scratch-card/logo-facebook.png" width="20" alt="Facebook" />
        </a>
        <a href="#" style="margin: 0 10px;">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/scratch-card/logo-x.png" width="20" alt="Twitter/X" />
        </a>

        <!-- Footer Text -->
        <p style="color: #ffffff; font-size: 14px; line-height: 24px; margin-top: 20px; font-weight: 400;">
          is simply dummy text of the printing and typesetting industry.
        </p>
        <p style="color: #ffffff; font-size: 14px; font-weight: 400; margin-top: 5px;">
          To stop receiving these emails,
          <a href="#" style="color: #ffffff; font-weight: bold; text-decoration: underline;">unsubscribe here</a>
        </p>
      </td>
    </tr>
    <!-- Fallback Link -->
    <tr>
      <td style="padding: 20px; text-align: center;">
        <p style="font-size: 12px; color: #7a7a7a;">
          If you're having trouble clicking the "Scratch Now" button, copy and paste this URL into your browser:
          <br />
          <a href="https://yourdomain.com/scratch" style="color: #ac8763;">https://yourdomain.com/scratch</a>
        </p>
      </td>
    </tr>

  </table>
</body>
</html>
```

## Welcome Mailer Template

A warm onboarding email template used to greet new users, introduce your brand, and guide them towards their first action or purchase. These templates highlight core benefits and offer a smooth entry into your product or service experience.

### Use Case Examples

- Introduces new subscribers to the brand 
- Highlights key benefits of your product and encourages first engagement or purchases.
- ### Template Customization Options
- [Replace the Logo](doc:ootb#1-replace-the-logo)
- [Update Banner/Product Images](doc:ootb#2-update-bannerproduct-images)
- [Update Call-To-Actions (CTAs)](https://staging.docs.user.clevertap.net/docs/ootb#3-call-to-actions-ctas)
- [Update Links in the Header/Footer](doc:ootb#4-update-links-in-the-headerfooter)
- [Change the Theme or Background Color](doc:ootb#5-change-the-theme-or-background-color)
- [Update the Privacy Policy](doc:ootb#update-the-privacy-policy)
- [Update Social Media Links and Download Links](doc:ootb#update-social-media-links-and-download-links)

### Template Code

(@Shreejith: In the UX copy sheet, there are 2 welcome email templates - one with iunsubscribe button and the other without button. But, when I look at the code - both the templates have that option. Please confirm what should we do here??)

```html
<!doctype html>
<html lang="en">
<head>
  <title></title>
  <style type="text/css">
    @font-face {
      font-family: 'Poppins';
      src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Fonts/Poppins-Light.woff') format('woff');
      font-style: normal;
      font-weight: 300;
    }
    @font-face {
      font-family: 'Poppins';
      src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Fonts/Poppins-Regular.woff') format('woff');
      font-style: normal;
      font-weight: 400;
    }
    @font-face {
      font-family: 'Poppins';
      src: url('https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Fonts/Poppins-Medium.woff') format('woff');
      font-style: normal;
      font-weight: 500;
    }
    * {
      margin: 0;
      padding: 0;
    }
    @media screen and (max-width: 480px) {
      .container { max-width: 100% !important; }
      .hero-title { font-size: 28px !important; line-height: 38px !important; }
      .content-title { font-size: 22px !important; line-height: 30px !important; }
      .button { padding: 10px 25px !important; font-size: 14px !important; }
    }
  </style>
</head>

<body style="margin: 0; padding: 0; background-color: #f5f5f5;">
  <table width="100%" cellspacing="0" cellpadding="0" border="0" align="center"
         style="max-width: 600px; margin: 0 auto; background-color: #ffffff; font-family: 'Poppins', sans-serif;">

    <!-- Logo -->
    <tr>
      <td align="center" style="padding: 24px 0;">
        <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/welcome-1/logo.png"
             alt="Brand Logo" style="width: 159px; height: 73px; object-fit: cover;" />
      </td>
    </tr>

    <!-- Hero Banner -->
    <tr>
      <td align="center">
        <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/welcome-1/banner.png"
             alt="Welcome Banner" style="width: 100%; height: auto;" />
      </td>
    </tr>
    <!-- Welcome Message -->
    <tr>
      <td align="center" style="padding: 40px 30px 20px;">
        <h1 class="hero-title" style="font-size: 32px; font-weight: 600; color: #252525; margin-bottom: 20px;">
          Welcome Aboard!
        </h1>
        <p style="font-size: 16px; color: #4f4f4f; line-height: 26px; margin: 0;">
          We’re thrilled to have you with us. Get ready to explore a world of exclusive offers, fresh content, and more.
        </p>
      </td>
    </tr>

    <!-- CTA Button -->
    <tr>
      <td align="center" style="padding: 30px 0 50px;">
        <a href="https://yourdomain.com/start"
           style="text-decoration: none; background: #ac8763; padding: 12px 50px; color: #fff;
           font-size: 14px; text-transform: uppercase; display: inline-block;">
          Get Started
        </a>
      </td>
    </tr>

    <!-- Divider -->
    <tr>
      <td style="padding: 0 0 40px;">
        <hr style="border: none; border-top: 1px solid #d8d8d8; width: 80%; margin: 0 auto;" />
      </td>
    </tr>
    <!-- Footer Section -->
    <tr>
      <td style="background-color: #1e1e1e; text-align: center; padding: 30px 0;">
        <!-- Social Media Icons -->
        <a href="#" style="margin: 0 10px;">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/welcome-1/logo-insta.png" width="20" alt="Instagram" />
        </a>
        <a href="#" style="margin: 0 10px;">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/welcome-1/logo-facebook.png" width="20" alt="Facebook" />
        </a>
        <a href="#" style="margin: 0 10px;">
          <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/welcome-1/logo-x.png" width="20" alt="Twitter/X" />
        </a>

        <!-- Footer Text -->
        <p style="color: #ffffff; font-size: 14px; line-height: 24px; margin-top: 20px; font-weight: 400;">
          is simply dummy text of the printing and typesetting industry.
        </p>

        <p style="color: #ffffff; font-size: 14px; font-weight: 400; margin-top: 5px;">
          To stop receiving these emails,
          <a href="#" style="color: #ffffff; font-weight: bold; text-decoration: underline;">unsubscribe here</a>
        </p>
      </td>
    </tr>
    <!-- Fallback URL -->
    <tr>
      <td style="padding: 20px; text-align: center;">
        <p style="font-size: 12px; color: #7a7a7a;">
          If you're having trouble clicking the "Get Started" button, copy and paste this URL into your browser:
          <br />
          <a href="https://yourdomain.com/start" style="color: #ac8763;">https://yourdomain.com/start</a>
        </p>
      </td>
    </tr>
  </table>
</body>
</html>
```

~~~\`html Rounded Borders

~~~

# Template Customization Options

This guide outlines all reusable components found across CleverTap HTML email templates, along with customization steps and code snippets. Each section reflects actual structure and styling from templates.

## 1. Replace the Logo

### Purpose

To display your brand’s logo at the top of the email, ensuring immediate brand recognition and consistent visual identity.

### Option 1: Direct Code Editing

1. Locate the logo block in your HTML template. A common example looks like this:
   ```html
   <td style="text-align: left; vertical-align: middle; padding: 20px">
     <img 
       alt="Logo"
       class="logo"
       src="https://yourdomain.com/logo.png"
       style="display: inline-block; width: 127px; height: 58px; object-fit: cover;" />
   </td>
   ```

2. Replace the `src` value with the URL of your updated brand logo:
   ```html
   src="https://yourdomain.com/path-to-your-logo.png"
   ```

3. Optionally customize:
   - `alt`: Add accessible text such as `"Your Brand Logo"`
   - `width` and `height`: Adjust only if required (default is typically `127px × 58px`)

### Option 2: Using the CleverTap Visual Editor

1. Open the desired template in the CleverTap **Email Editor**.
2. Click on the existing logo image in the top section of the email.
3. In the toolbar, click **Replace Image** or the **image icon**.
4. Choose one of the following:
   - **Upload** a new image file (preferably PNG or SVG for sharpness), or  
   - Paste the hosted image link in the **Image URL** field.
5. Click **Add** or **Apply**.
6. Use the drag handles or the **Style** panel to adjust logo size and alignment as needed.
7. Click **Done**, and preview the email to ensure correct rendering.

### Template-Specific Exceptions

| Template Name                           | Exception Description                                                                                                   |
| --------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| **Show Recommendation (Black & White)** | The logo may be center-aligned within a full-width block and require horizontal centering styles (`text-align: center`) |
| **Flash Sale**                          | Logo may appear beside countdown or CTA in a split-column layout, potentially appearing smaller (around 100px width)    |
| **Winback**                             | The logo may be within a colored header block. Ensure proper contrast when updating logo                                |
| **Newsletter**                          | The logo may be stacked above headline text and additional top margin may be present                                    |
| **What's in the Store**                 | The logo size can vary and may be around **146px width**. Adjustments may be required for clarity in small areas.       |

> 📘 Note
> 
> For templates listed above, verify logo alignment, spacing, and sizing on both mobile and desktop previews after replacement.

## 2. Update Banner/Product Images

### Purpose

To visually highlight products, offers, or campaigns at the top of the email using a full-width banner image or a product tile grid, depending on the template layout.

### Option 1: Direct Code Editing

1. Locate the banner `<img>` tag in your HTML template. For example:
   ```html
   <tr>
     <td align="center">
       <img src="https://yourdomain.com/banner.jpg"
            alt="Promotional Banner"
            style="width: 100%; height: auto;" />
     </td>
   </tr>
   ```

2. Replace the `src` URL with the path to your new banner image.

3. Update the `alt` attribute to provide descriptive alternative text for accessibility and fallback scenarios.

4. Ensure the image meets the following specifications:
   - **Recommended size**: 600px (width) × 400px (height)
   - **Aspect ratio**: 3:2
   - **File formats**: `.jpg`, `.png`, `.gif`
   - **Maximum file size**: Under 1MB

### Option 2: Using the CleverTap Visual Editor

1. Open the template in the CleverTap **Email Editor**.
2. Click on the existing banner image.
3. In the toolbar, click **Replace Image** or the **image icon**.
4. Either:
   - **Upload** a new image (recommended size: 600×400px), or
   - Paste a hosted image link into the **Image URL** field.
5. Click **Add** or **Apply**.
6. Use the drag handles or the **Style** panel to adjust alignment and spacing.
7. Click **Done**, then preview the email across screen sizes to confirm correct rendering.

### Template-Specific Exceptions

Some templates use custom-sized banners or include grid layouts with smaller product tiles instead of a single large banner.

| Template Name                          | Banner Type              | Dimensions / Notes                                 |
| -------------------------------------- | ------------------------ | -------------------------------------------------- |
| **Cart Abandonment**                   | Standard Banner          | 600×400px banner and optional product grid         |
| **Newsletter**                         | Standard Banner          | 600×400px                                          |
| **Loyalty Expiry**                     | Standard Banner          | 600×400px                                          |
| **Order Placed / Shipped / Delivered** | Standard Banner          | 600×400px                                          |
| **Password Reset**                     | Standard Banner          | 600×400px                                          |
| **Access to Early Sales**              | Standard Banner + Grid   | 600×400px banner, plus product grid                |
| **Flash Sale**                         | Product Cards Grid       | Countdown and product cards (approx. 247×383px)    |
| **Show Recommendation (Black/White)**  | Grid Tiles               | 2–3 column layout, 180–250px width per tile        |
| **What’s in the Store**                | Hero Grid                | 3-column layout, 200–250px width per tile          |
| **Promotional**                        | Banner + Grid            | 600px banner, 2-column product grid (~270px width) |
| **Referral** (specific designs)        | Side-by-side Tiles       | Benefit tiles; sizes vary                          |
| **Winback**                            | Hero Grid                | 2–3 column layout with product images (~247×383px) |
| **Subscription**                       | Banner + Featured Blocks | 600×400px banner with optional tiles               |

For templates using grid-based layouts or product tiles, always match the original image dimensions and maintain consistent spacing to ensure the layout remains visually balanced and responsive.

## Update Call-To-Actions (CTAs)

### Purpose

To guide the user to take a specific action within the email, such as clicking a button to navigate to a web page, complete a purchase, or view more details.

### Option 1: Direct Code Editing

1. Locate the CTA section in your HTML template. A typical CTA looks like this:
   ```html
   <tr>
     <td style="text-align: center; padding: 20px;">
       <a href="https://your-link.com"
          style="background: #FF5733; padding: 10px 20px; color: #fff; text-decoration: none; font-size: 16px; border-radius: 5px;">
         Shop Now
       </a>
     </td>
   </tr>
   ```

2. Replace the `href` URL with the link where you want to direct the user:
   ```html
   href="https://yourdomain.com/your-action"
   ```

3. Optionally, modify the text of the CTA, such as changing "Shop Now" to "Get Started" or "Claim Your Offer."

4. Adjust the button's styling by modifying the CSS within the `<a>` tag (e.g., background color, padding, font size, etc.):
   ```html
   style="background: #FF5733; padding: 10px 20px; color: #fff; text-decoration: none; font-size: 16px; border-radius: 5px;"
   ```

### Option 2: Using the CleverTap Visual Editor

1. Open the template in the CleverTap **Email Editor**.
2. Click on the existing CTA button (or link).
3. In the toolbar, click **Edit** or the **link icon**.
4. Either:
   - **Update the link URL** to the desired destination, or
   - **Change the CTA text** to suit your new action.
5. Customize the styling, such as adjusting the button's size, padding, and color, using the editor's **Style** options.
6. Click **Done**, and preview the email to confirm that the CTA behaves as expected.

### Template-Specific Exceptions

| **Template Name**                       | **Exception Description**                                                                                                  |
| --------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| **Winback**                             | CTA buttons may be smaller and positioned within a split-column layout. Ensure sufficient padding for clickability.        |
| **Promotional**                         | Some CTAs might appear multiple times within the email. Keep consistency in text and color across all CTAs.                |
| **Flash Sale**                          | CTA is used in the countdown section, and might include urgency-driven language (e.g., "Hurry, limited time!").            |
| **Cart Abandonment**                    | CTA might include a special offer or discount code; ensure the link reflects the correct promotion.                        |
| **Referral Template**                   | Includes a "Refer Now" CTA, which might need special handling for personalized referral links.                             |
| **Show Recommendation (Black & White)** | CTA may be part of a multi-image grid or block with product tiles, requiring individual adjustments per image link.        |
| **What’s in the Store**                 | Multi-product grid layout with CTA links inside each product tile; ensure CTA links are correctly aligned within the grid. |

### Customizable Elements:

- **Text**: Modify the text within the anchor tag (e.g., "Discover More" → "Shop Now").
- **URL**: Update the `href` attribute with the desired link (e.g., `href="https://your-domain.com"`)
- **Styling**: Adjust the CSS properties to fit your design specifications (e.g., background color, padding, text size).

> 📘 Best Practices
> 
> Always make sure the CTAs are clear and actionable, and consider using verbs like "Buy," "Get Started," "Learn More," or "Shop Now."

## 4. Update Links in the Header/Footer

To update the links in the header or footer sections of the email, such as Privacy Policy, Terms of Service, or any social media or download links, to ensure they direct to the correct URLs.

### Option 1: Direct Code Editing

1. **Locate the Header/Footer Section**: Search for the relevant section in your HTML code. For example, a footer section might look like this:
   ```html
   <td class="footer" style="text-align: center; padding: 10px; font-size: 12px;">
     <a href="https://your-domain.com/privacy-policy" style="color: #939393; text-decoration: none;">Privacy Policy</a>
   </td>
   ```

2. **Update the Link**:
   - Replace the `href` URL with the new destination:
     ```html
     href="https://your-domain.com/new-link"
     ```

3. **Update the Text**: If required, update the link's visible text. For example:
   ```html
   <a href="https://your-domain.com/privacy-policy" style="color: #939393; text-decoration: none;">Terms & Conditions</a>
   ```

4. **Styling Adjustments**: You can adjust the text styles by modifying the `style` attribute (e.g., font color, size, etc.).

5. **Save and Preview**: After making changes, ensure to save the file and preview the email to confirm that the links are functional and styled properly.

### Option 2: Using the CleverTap Visual Editor

1. **Open the Template** in the CleverTap **Email Editor**.
2. **Click on the Header/Footer link** that needs to be updated (e.g., Privacy Policy).
3. In the toolbar, click **Edit Link** or the **link icon**.
4. **Update the Link URL** to the desired destination or modify the link text as necessary.
5. If available, **adjust the styling** for the link using the editor’s Style panel (e.g., font size, color).
6. **Click Apply** or **Done** to save your changes.
7. **Preview** the email to ensure that the link functions correctly and displays as expected.

### Template-Specific Exceptions

| **Template Name**               | **Exception Description**                                                                                                                                              |
| ------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Flash Sale**                  | Footer links might be placed in a **2-column layout**. Ensure responsiveness and proper alignment of links like "Shop Now" and "Terms".                                |
| **Promotional Template**        | May contain **multiple CTAs or links** in the footer. Ensure all links like "See More", "Shop Now", and "Terms" are updated correctly.                                 |
| **Referral Template**           | Includes **social media links** and **personalized referral program links** in the footer. Ensure referral URLs are dynamically generated per user.                    |
| **Winback**                     | Footer links may be aligned with a **call-to-action (CTA)** such as "Reclaim Your Rewards". Update links to match the promotional period.                              |
| **Newsletter**                  | May include an **Unsubscribe** link in the footer. Ensure it links to the correct unsubscribe page and complies with email regulations.                                |
| **What’s in the Store**         | A product grid footer may include **category-based links** (e.g., Men, Women, Kids). Verify the links for each category are correct.                                   |
| **Cart Abandonment**            | Footer may contain dynamic links like **"Apply Discount"** or **"Complete Purchase"**. Ensure the links reflect the current promotion or cart contents.                |
| **Show Recommendation (Black)** | Footer may contain **social media icons** or **show recommendation links**. Ensure the links lead to the correct landing page for content.                             |
| **Show Recommendation (White)** | Similar to the Black variant, footer links may contain **show or product recommendations**. Ensure the links point to accurate pages based on user preferences.        |
| **Subscription Template**       | Footer might contain links to **manage subscription preferences** or **subscription details**. Ensure links direct users to the appropriate management page.           |
| **Order Delivered**             | Footer may include **order-related links** such as "Track Your Order" or "Reorder". Ensure these links lead to valid tracking and reorder pages.                       |
| **Order Placed**                | Footer may contain links like **"View Order Details"** or **"Track Your Order"**. Ensure the links direct users to correct order confirmation or tracking pages.       |
| **Order Shipped**               | Footer may contain **order status links** such as "Track Package" or "Contact Support". Ensure these links are up-to-date with shipping information.                   |
| **Password Reset**              | The footer may contain a link to **"Help"** or **"Contact Support"**. Ensure these links point to valid support resources.                                             |
| **Scratch Card**                | The footer might contain a **"Claim Your Reward"** or similar CTA. Ensure the links reflect current offers and rewards.                                                |
| **First Purchase Incentive**    | Footer links might include **incentives or promo details** like "Apply Coupon" or "Shop Now". Verify that these links reflect any current first-purchase promotions.   |
| **Informative Mailer**          | Footer links could include **"Privacy Policy"**, **"Terms"**, or **"Contact Us"**. Make sure these links are correctly updated and reflect the latest legal documents. |
| **Loyalty Points Template**     | Footer links might refer to **loyalty rewards** such as "View Rewards" or "Redeem Points". Ensure the links reflect the correct loyalty program page.                  |

> 📘 Key Notes:
> 
> - **Unsubscribe Link**: For compliance with regulations such as GDPR and CAN-SPAM, all templates that include an **Unsubscribe** link in the footer must ensure it directs to the correct unsubscribe mechanism.
> - **Social Media Links**: Ensure all social media links, like those for Facebook, Instagram, etc., are up-to-date and lead to your current active profiles.
> - **Dynamic Links**: Some templates, like **Referral** or **Cart Abandonment**, require dynamic links that change based on user activity. Make sure these URLs are generated dynamically by your platform or manually updated.
> - **Call-to-Actions (CTAs)**: Some templates, especially those with **sales**, **product promotions**, or **loyalty rewards**, might have CTAs that need to be consistently checked and updated based on current offers or time-sensitive promotions.

## 5. Change the Theme or Background Color

To modify the background color or overall theme of the email to match your branding or campaign requirements. This ensures a consistent visual experience aligned with your marketing or seasonal themes.

### Option 1: Direct Code Editing

1. Locate the `<table>` tag defining the background color in your HTML code. A typical structure might look like this:
   ```html
   <table style="border-collapse: collapse; width: 100%; max-width: 600px; margin: 0 auto; background: #ffffff;" width="100%" cellspacing="0" cellpadding="0" border="0">
   ```

2. **Update the Background Color**:  
   Replace the existing `background` attribute value with your desired color. For example:
   ```html
   background: #f0f0f0;
   ```

3. **Save and Preview**: After making the changes, save the file and preview the email to ensure the new background color appears correctly across different devices.

### Option 2: Using the CleverTap Visual Editor

1. Open the template in the **CleverTap Email Editor**.
2. Click on the section (header, body, or footer) where you want to change the background color.
3. In the toolbar, select the **background color** option or open the **Style panel**.
4. Choose the new color from the color picker or input a **Hex code** (for example, `#f0f0f0` for light gray).
5. **Apply changes** and preview the email to ensure it looks as intended.

## Update the Privacy Policy

To ensure that the Privacy Policy link in the email template directs users to the most current and correct Privacy Policy page.

### Option 1: Direct Code Editing

1. **Locate the Privacy Policy Link**:  
   Search for the `<a>` tag associated with the Privacy Policy in the footer or header section of your template. A typical code structure might look like:
   ```html
   <a href="#" class="f-nav-link" style="font-family: 'Poppins', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 24px; color: #939393 !important; text-decoration: none;">Privacy Policy</a>
   ```

2. **Update the `href` URL**:  
   Replace the current `href="#"` with the correct URL for your Privacy Policy page. For example:
   ```html
   href="https://yourdomain.com/privacy-policy"
   ```

3. **Modify Text (Optional)**: You can optionally change the visible text of the link, such as replacing "Privacy Policy" with "Terms & Conditions" if required.

4. **Save and Preview**: After making the changes, save your template and preview it to ensure the Privacy Policy link is working correctly and properly displayed.

### Option 2: Using CleverTap Visual Editor

1. Open the Template in the **CleverTap Email Editor**.
2. Locate the Privacy Policy Link in the footer or header section of the email.
3. Click on the Link to open the link editing toolbar.
4. Edit the URL: Update the link URL to the correct Privacy Policy page URL.
5. **Modify the Link Text (Optional)**: Change the visible text if necessary (for example, from "Privacy Policy" to "Terms & Conditions").
6. Apply Changes: After editing the URL, click **Apply** or **Done** to save the changes.
7. Preview the Email: Preview the email to ensure the link works as intended and is visible across devices.

## Update Social Media Links and Download Links

To update and ensure that all social media and download links in your email template direct users to the correct platforms, apps, or resources.

### Option 1: Direct Code Editing

1. **Locate the Social Media and Download Sections**:  
   Search for sections in the HTML code related to social media platforms (such as Facebook, Twitter, Instagram, etc.) and download buttons (such as Android or Apple store download links). You may see something like:
   ```html
   <a href="https://your-facebook-link" target="_blank">
     <img src="https://path-to-facebook-icon.png" alt="Facebook" class="social-icon" />
   </a>
   ```

2. **Update the Links**:

   For social media platforms, replace the `href` with the correct URL. For example:

   ```html
   <a href="https://facebook.com/your-page" target="_blank">
     <img src="https://path-to-facebook-icon.png" alt="Facebook" class="social-icon" />
   </a>
   ```

   Similarly, for download links, locate the button or link related to the app download, like this:

   ```html
   <a href="#" class="btn-link" style="margin: 0 10px;">
     <img src="apple-btn.png" alt="Download on Apple" class="btn-img" style="background: #F7F7F7; position: relative; z-index: 1;">
   </a>
   ```

   Update the `href` attribute with the correct download link:

   ```html
   <a href="https://www.apple.com/app-store" class="btn-link" style="margin: 0 10px;">
     <img src="apple-btn.png" alt="Download on Apple" class="btn-img" style="background: #F7F7F7; position: relative; z-index: 1;">
   </a>
   ```

3. **Save and Preview**:  
   After updating the URLs for both social media and download links, save the file and preview the email to ensure all links work properly.

### Option 2: Using the CleverTap Visual Editor

1. Open the Template in the **CleverTap Email Editor**.
2. Locate the Social Media Links: Click on the social media icons (like Facebook, Twitter, Instagram, etc.) within the template.
3. Update the Link: In the toolbar, update the `href` attribute with the correct URL for the corresponding social media platform.
4. Locate the Download Links: For Android or iOS download buttons, click on the relevant download button.
5. Update the Download Link: In the toolbar, update the link for the download button, such as replacing `#` with the actual app store URL (e.g., Apple Store or Google Play Store).
6. Save and Preview: Save your changes and preview the email to ensure that the social media and download links are correctly updated.

## Countdown Timer (Flash Sale Only)

**Purpose:** Add urgency with a live or static countdown.

### Steps:

- Use a hosted GIF or PNG and replace image `src`.

```html
<img src="timer.gif" alt="Countdown Timer" style="width: 100%;" />
```

<br />

# AMP Templates

## What’s In Store

This AMP template is designed to promote a curated selection of new arrivals, trending products, or personalized recommendations — all within an interactive AMP-powered layout. With in-mail CTAs, users can explore your latest offerings directly from their inbox, creating a seamless browsing experience.

<details>

<summary>Expand to know more about the template.</summary>

### Use Case Examples

- Highlight newly launched or trending products from your catalog.
- Personalize the product showcase based on the user’s recent activity or preferences.
- Run weekly or monthly What’s New campaigns for returning users.
- Drive conversions by enabling users to click through to product pages without friction.

### Template Customization Options

- Replace the Logo
- Update Banner/Product Images
- Update Call-To-Actions (CTAs)
- Update Links in the Header/Footer
- Change the Theme or Background Color
- Update the Privacy Policy
- Update Social Media and Download Links

### Template Code

```html
<!doctype html>
<html ⚡4email>
<head>
    <meta charset="utf-8">
    <script async src="https://cdn.ampproject.org/v0.js"></script>
    <script async custom-element="amp-form" src="https://cdn.ampproject.org/v0/amp-form-0.1.js"></script>
    <script async custom-element="amp-bind" src="https://cdn.ampproject.org/v0/amp-bind-0.1.js"></script>
    <style amp4email-boilerplate>
        body {
            visibility: hidden
        }
    </style>
    <style amp-custom>
        * {
            margin: 0;
            padding: 0;
        }
        ul,
        li {
            list-style: none;
        }
        /* Change Theme */
        body {
            font-family: "Helvetica", arial, sans-serif;
            font-weight: 400;
            background-color: rgb(248, 250, 252);
        }
        /* Change Theme */
        img {
            width: 100%;
            height: 100%;
            object-fit: contain;
        }
        amp-img {
            position: relative;
        }
        .main {
            position: relative;
            width: 100%;
            max-width: 600px;
            overflow: hidden;
            margin: 0 auto;
            background: #FFFFFF;
        }
        .container {
            max-width: 85%;
            margin: 0 auto;
        }
        @media only screen and (max-width: 400px) {
            .container,
            .main {
                max-width: 95%;
            }
        }
        .cp-header {
            padding: 0 30px;
        }
        .cp-header.typ-shadow {
            box-shadow: 0px 4px 4px 0px #00000040;
        }
        .logo-wrap {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .logo-wrap .img-wrap {
            width: 127px;
            height: 58px;
            margin: 8.5px 0;
        }
        .nav-list {
            list-style: none;
            display: flex;
            align-items: center;
        }
        .nav-list .nav-item {
            padding: 25px 19px;
            border-left: 0.5px solid #919191;
            display: flex;
            align-items: center;
        }
        .nav-list .nav-item:last-child {
            padding-right: 0;
        }
        .cart-icon {
            border: 0;
            outline: 0;
            position: relative;
            background-color: transparent;
        }
        .cart-icon.active .dot {
            display: inline-block;
        }
        .dot {
            width: 6px;
            height: 6px;
            background: #FF533F;
            border-radius: 50%;
            display: none;
            position: absolute;
            top: 2px;
            right: 0px;
            z-index: 1;
        }
        .call-icon {
            width: 20px;
            height: 20px;
            margin-right: 5px;
        }
        .icon-text {
            font-size: 14px;
            font-weight: 400;
            line-height: 24px;
            text-align: center;
            color: #464646;
        }
        .cp-banner {
            width: 100%;
            max-height: 361px;
            margin-bottom: 22px;
        }
        .cp-footer {
            margin-top: 50px;
            background: #1E1E1E;
            padding: 32px 0 34px;
        }
        .media-logo-list {
            display: flex;
            justify-content: center;
            align-items: center;
            margin-bottom: 20px;
        }
        .media-logo-list .logo-item {
            padding: 6px 32px;
            border: 1px solid #FFFFFF;
        }
        .media-logo-list .logo-item .logo-link {
            display: inline-block;
        }
        .media-logo {
            width: 20px;
            height: 20px;
            display: inline-block;
        }
        .f-desc {
            font-size: 14px;
            font-weight: 400;
            line-height: 20px;
            text-align: center;
            color: #FFFFFF;
            margin: 0 auto;
            max-width: 84%;
            text-transform: capitalize;
        }
        .bs-sec {
            padding: 28px 0;
        }
        .bs-sec.typ-product {
            background: #F1F1F1;
        }
        .bs-sec .sec-title {
            padding: 0 26px 12px;
            text-transform: capitalize;
            font-size: 20px;
            font-weight: 400;
            line-height: 24px;
            text-align: center;
            position: relative;
            width: max-content;
            margin: 0 auto;
        }
        .bs-sec .sec-title.typ-2 {
            margin: 0;
            padding: 0 0 2px;
        }
        /* .bs-sec .sec-title.typ-2:after{
            display: none;
        } */
        .lyt-grid {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            gap: 15px;
            margin-top: 20px;
        }
        .lyt-grid .grid-item {
            width: 33%;
        }
        .product-card {
            padding: 5px;
            position: relative;
            background: #FFFFFF;
        }
        .product-card .img-wrap {
            max-height: 177px;
            max-width: 150px;
            margin: 0 auto;
            overflow: hidden;
        }
        .product-card .p-cart-icon {
            background: #FFFFFF;
            padding: 3px 5px;
            border: 0;
            outline: 0;
            position: absolute;
            top: 5px;
            right: 5px;
            cursor: pointer;
        }
        .product-card .p-wrap {
            display: flex;
            justify-content: space-between;
            align-items: baseline;
            margin: 5px 0;
        }
        .product-card .p-title {
            width: 60%;
            font-size: 14px;
            font-weight: 400;
            line-height: 18px;
            color: #252525;
            padding-right: 5px;
        }
        .product-card .p-amt {
            color: #252525;
            font-size: 12px;
            font-weight: 300;
            line-height: 15px;
            text-align: right;
            font-style: italic;
        }
        .product-card .rupee-sign {
            font-size: 10px;
        }
        .product-card .p-desc {
            text-transform: capitalize;
            font-size: 8px;
            font-weight: 400;
            line-height: 13px;
            color: #909090;
            overflow: hidden;
            text-overflow: ellipsis;
            -webkit-line-clamp: 2;
            display: -webkit-box;
            -webkit-box-orient: vertical;
        }
        .btn-wrap {
            text-align: right;
        }
        .shop-cta {
            font-size: 12px;
            font-weight: 400;
            text-transform: capitalize;
            line-height: 15px;
            color: #000000;
            text-decoration: none;
            display: inline-block;
            text-align: center;
            margin-top: 15px;
        }
        .catalog-card {
            margin-top: 30px;
        }
        .catalog-card .catalog-img {
            max-width: 506px;
            max-height: 316px;
            position: relative;
        }
        .catalog-card .offer-band {
            background: #1e1e1e;
            text-align: center;
            padding: 7px 20px;
            font-size: 12px;
            font-weight: 400;
            line-height: 13px;
            letter-spacing: 0.25em;
            position: absolute;
            top: 0;
            left: 0;
            z-index: 1;
            width: 92%;
            color: #fff;
        }
        .catalog-card .cart-wrap {
            position: absolute;
            bottom: 0;
            right: 0;
            padding: 8px 10px;
            background: #fff;
            z-index: 1;
        }
        .catalog-card .cart-wrap .count {
            position: absolute;
            top: 8px;
            right: 8px;
            width: 11px;
            height: 11px;
            background: #FF533F;
            border-radius: 50%;
            color: #FFFFFF;
            font-size: 7px;
            font-weight: 400;
            line-height: 11px;
            text-align: center;
            z-index: 1;
        }
        .catalog-card .catalog-body {
            background: #f1f1f1;
            padding: 12px 14px 10px;
        }
        .catalog-card .c-wrap {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
        }
        .catalog-card .c-title {
            margin-bottom: 5px;
            font-size: 20px;
            font-weight: 400;
            line-height: 24px;
            color: #252525;
            width: 50%;
        }
        .catalog-card .c-amt {
            font-size: 22px;
            font-style: italic;
            font-weight: 400;
            line-height: 15px;
            text-align: right;
        }
        .catalog-card .rupee-sign {
            font-size: 10px;
        }
        .catalog-card .c-desc {
            font-size: 10px;
            font-weight: 400;
            line-height: 13px;
            color: #545454;
            width: 40%;
            text-transform: capitalize;
        }
        .catalog-card .btn-wrap {
            width: 60%;
            display: flex;
            justify-content: flex-end;
        }
        .catalog-card .catalog-cta {
            font-size: 14px;
            font-weight: 400;
            text-transform: uppercase;
            line-height: 20px;
            color: #FFFFFF;
            text-decoration: none;
            background: #000000;
            padding: 4px 34px;
            display: inline-block;
            text-align: center;
            max-width: 167px;
            border: none;
            margin-left: 10px;
            cursor: pointer;
        }
        .product-count {
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 6px;
            background: #FFF;
            width: 60px;
        }
        .product-count .product-count-sign {
            background: transparent;
            border: 0;
            outline: none;
            cursor: pointer;
        }
        .product-count-value {
            font-size: 12px;
            font-weight: 400;
            line-height: 15px;
            text-align: center;
        }
        .input {
            border: 0.5px solid #000000;
            padding: 7px 10px;
            font-family: "Helvetica", arial, sans-serif;
            font-size: 16px;
            font-weight: 400;
            line-height: 24px;
            color: #000000;
            width: -webkit-fill-available;
        }
        .input::-webkit-input-placeholder,
        .input::-moz-placeholder,
        .input:-ms-input-placeholder,
        .input:-moz-placeholder {
            color: #919191;
        }
        @media only screen and (max-width: 480px) {
            .cp-header {
                max-width: 100%;
                padding: 0 10px;
            }
            .logo-wrap .img-wrap {
                width: 101px;
                height: 48px;
                margin: 5.5px 0;
            }
            .nav-list .nav-item {
                padding: 15px 10px;
            }
            .call-icon {
                width: 18px;
                height: 18px;
            }
            .icon-text {
                font-size: 12px;
                line-height: 20px;
            }
            .lyt-grid {
                gap: 5px;
            }
            .product-card .p-title {
                font-size: 12px;
                line-height: 16px;
            }
            .product-card .p-amt {
                font-size: 10px;
                line-height: 16px;
            }
            .bs-sec .sec-title {
                padding: 0 20px 12px;
                font-size: 18px;
                line-height: 20px;
            }
            .catalog-card .catalog-cta {
                font-size: 10px;
                line-height: 14px;
                padding: 5px;
            }
        }
        .form-list {
            margin-top: 20px;
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            gap: 10px;
        }
        .form-item {
            width: 49%;
            position: relative;
            padding-bottom: 20px;
        }
        .form-item.typ-full {
            width: 100%;
        }
        [visible-when-invalid]{
            display: block;
        }
        .error-msg{
            font-size: 10px;  
            display: none;   
            position: absolute;
            bottom: 0; left: 0;       
        }
        .error-msg.visible{
            display: block;   
        }
        .field-wrap {
            display: block;
            position: relative;
            padding-left: 25px;
            margin-bottom: 10px;
            cursor: pointer;
            -webkit-user-select: none;
            -moz-user-select: none;
            -ms-user-select: none;
            user-select: none;
            font-size: 16px;
            font-weight: 400;
            line-height: 24px;
        }
        .field-wrap input {
            position: absolute;
            opacity: 0;
            cursor: pointer;
        }
        .checkmark {
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
            left: 0;
            height: 17px;
            width: 17px;
            background-color: #0B0B0B;
            border-radius: 50%;
        }
        .field-wrap input:checked~.checkmark {
            background-color: #0B0B0B;
        }
        .checkmark:after {
            content: "";
            position: absolute;            
            display: block;
        }
        .field-wrap input:checked~.checkmark:after {
           display: none;
        }
        .field-wrap .checkmark:after {
            top: 2px;
            left: 2px;
            width: 13px;
            height: 13px;
            border-radius: 50%;
            background: #FFFFFF;
        }
        .mt-32 {
            margin-top: 32px;
        }
        .form-btn {
            font-size: 20px;
            font-weight: 400;
            line-height: 24px;
            text-align: center;
            width: 100%;
            background: #252525;
            border: 0;
            outline: none;
            color: #FFF;
            padding: 10px;
            cursor: pointer;
        }
        .tab-3 {
            position: relative;
        }
        .modal-overlay {
            width: 100%;
            height: 100%;
            background-color: #000000;
            padding: 100px 0;
        }
        .modal {
            width: 75%;
            margin: 40px auto;
            z-index: 12;
            background: #FFF;
            padding: 70px 30px;
            position: relative;
        }
        .close {
            width: 27px;
            height: 27px;
            display: inline-block;
            text-align: center;
            background: #000000;
            font-size: 13px;
            color: #FFFFFF;
            line-height: 27px;
            border-radius: 50%;
            position: absolute;
            top: 6px;
            right: 6px;
            cursor: pointer;
        }
        .m-title {
            font-size: 20px;
            font-weight: 400;
            line-height: 24px;
            text-align: center;
            margin-bottom: 20px;
            color: #000000;
            text-transform: uppercase;
        }
        .m-desc {
            font-size: 14px;
            font-weight: 400;
            line-height: 20px;
            text-align: center;
            color: #545454;
            text-transform: capitalize;
            max-width: 70%;
            margin: 0 auto;
        }
        .product-list {
            margin: 16px 0;
        }
        .product-list .product-item {
            display: flex;
            justify-content: space-between;
            padding: 16px 0;
            border-bottom: 1px solid #919191;
        }
        .product-list .product-item:last-child {
            border: 0;
            padding-bottom: 0;
        }
        .lhs {
            width: 80%;
        }
        .rhs {
            width: 20%;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            align-items: flex-end;
        }
        .product-item .p-name {
            font-size: 16px;
            font-weight: 400;
            line-height: 24px;
            color: #000000;
            margin-bottom: 6px;
        }
        .product-item .p-desc {
            font-size: 10px;
            font-weight: 400;
            line-height: 13px;
            color: #545454;
            margin-bottom: 6px;
        }
        .product-item .p-quality {
            font-size: 16px;
            font-weight: 400;
            line-height: 24px;
            color: #000000;
        }
        .product-item .delete-icon {
            background: transparent;
            outline: none;
            border: 0;
        }
        .product-item .p-amt {
            font-size: 22px;
            font-style: italic;
            font-weight: 300;
            line-height: 24px;
            color: #000000;
        }
        .product-item .p-total {
            font-size: 20px;
            font-weight: 400;
            line-height: 24px;
            color: #000000;
        }
        .typ-bottom-padding-zero {
            padding-bottom: 0;
        }
        .disabled {
            pointer-events: none;
            cursor: not-allowed;
            opacity: 0.7;
        }
        @media only screen and (max-width: 480px) {
            .catalog-card .offer-band {
                padding: 7px;
                font-size: 10px;
                line-height: 10px;
                width: 96%;
            }
            .catalog-card .c-title {
                font-size: 16px;
                line-height: 18px;
            }
            .catalog-card .c-amt {
                font-size: 18px;
                line-height: 20px;
            }
            .catalog-card .c-desc {
                margin-bottom: 7px;
            }
            .catalog-card .c-wrap {
                flex-wrap: wrap;
            }
            .catalog-card .btn-wrap,
            .catalog-card .c-desc {
                width: 100%;
            }
            .form-item {
                width: 100%;
            }
            .lhs,
            .rhs {
                width: 50%;
            }
            .product-item .p-total,
            .product-item .p-amt {
                font-size: 18px;
                line-height: 20px;
            }
        }
    </style>
</head>
<body>
    <div class="main">
        <div id="ProductCatalogform" on="tap:AMP.setState({productCatalog01: {fuuid: 01 }})" role="tab" tabindex="1"
            class="amp-html-block widget-container">
            <form class="form-container" method="post" id="productCatalog01Form" enctype="multipart/form-data"
                action-xhr="https://example.com" custom-validation-reporting="show-all-on-submit" on="submit:AMP.setState({
                    productCatalog01: {
                        currentStep: productCatalog01.currentStep == 2 : productCatalog01.currentStep + 1, 
                        submitting: true,
                        editAddress: false
                    }
                });
                submit-success:AMP.setState({
                    productCatalog01: {
                        submitting: false, 
                        paymentUrl: productCatalog01.paymentUrl || event.response.url
                    }
                });">
                <input hidden id="fuuid" name="fuuid" [value]="01" />
                <input hidden name="catalogType" value="STATIC" />
                <input hidden name="discountCouponCode" value="" />
                <amp-state id="productCatalog01">
                    <script type="application/json">
                        {
                            "first_name": "",
                            "last_name": "",
                            "address": "",
                            "landmark": "",
                            "city": "",
                            "country": "",
                            "pincode": "",
                            "phoneNumber": "",
                            "email": "",
                            "payment_mode": "",
                            "isFirstNameValid": false,
                            "isLastNameValid": false,
                            "isPhoneNumberValid": false,
                            "isEmailValid": false,
                            "isPincodeValid": false,
                            "isCityValid": false,
                            "editAddress": false,        
                            "paymentUrl": "",
                            "product1": {
                                "id": 1,
                                "qty": 0,
                                "title": "Mystic Elixir",
                                "price": 1500,
                                "selectedVariantId": 0,
                                "addedToCart": false,
                                "variantId": 101,
                                "variantTitle": "Default Title",
                                "comparePrice": "null",
                                "variants": {
                                    "101": {
                                        "id": 101,
                                        "price": 1500,
                                        "title": "Default Title",
                                        "comparePrice": "null"
                                    }
                                }
                            },
                            "product2": {
                                "id": 2,
                                "qty": 0,
                                "title": "Opulent Essence",
                                "price": 1500,
                                "selectedVariantId": 0,
                                "addedToCart": false,
                                "variantId": 102,
                                "variantTitle": "Default Title",
                                "comparePrice": "null",
                                "variants": {
                                    "102": {
                                        "id": 102,
                                        "price": 1500,
                                        "title": "Default Title",
                                        "comparePrice": "null"
                                    }
                                }
                            },
                            "product3": {
                                "id": 3,
                                "qty": 0,
                                "title": "Product Name 3",
                                "price": 1500,
                                "selectedVariantId": 0,
                                "addedToCart": false,
                                "variantId": 103,
                                "variantTitle": "Default Title",
                                "comparePrice": "null",
                                "variants": {
                                    "103": {
                                        "id": 103,
                                        "price": 1500,
                                        "title": "Default Title",
                                        "comparePrice": "null"
                                    }
                                }
                            },
                            "product4": {
                                "id": 4,
                                "qty": 0,
                                "title": "Product Name 4",
                                "price": 1500,
                                "selectedVariantId": 0,
                                "addedToCart": false,
                                "variantId": 104,
                                "variantTitle": "Default Title",
                                "comparePrice": "null",
                                "variants": {
                                    "104": {
                                        "id": 104,
                                        "price": 1500,
                                        "title": "Default Title",
                                        "comparePrice": "null"
                                    }
                                }
                            },
                            "product5": {
                                "id": 5,
                                "qty": 0,
                                "title": "Product Name 5",
                                "price": 1500,
                                "selectedVariantId": 0,
                                "addedToCart": false,
                                "variantId": 105,
                                "variantTitle": "Default Title",
                                "comparePrice": "null",
                                "variants": {
                                    "105": {
                                        "id": 105,
                                        "price": 1500,
                                        "title": "Default Title",
                                        "comparePrice": "null"
                                    }
                                }
                            },
                            "currentStep": 1
                        }
                    </script>
                </amp-state>
                <!-- <h1 [text]="productCatalog01.currentStep"></h1> -->
                <header class="cp-header typ-shadow" [hidden]="productCatalog01.currentStep == 3">
                    <div class="logo-wrap">
                        <div class="img-wrap">
                            <!-- Change Logo -->
                            <amp-img layout="responsive"
                                src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/logo.png"
                                alt="Logo" width="127" height="58" />
                            <!-- Change Logo -->
                        </div>
                        <ul class="nav-list">
                            <li class="nav-item">
                                <div class="cart-icon checkout-button"
                                    [class]="productCatalog01.currentStep == 2 ? 'cart-icon active' : 'cart-icon'"
                                    on="tap:AMP.setState({
                                        productCatalog01 : {
                                        currentStep:  2 ,
                                        editAddress: true,
                                        }
                                    })"
                                    >
                                    <amp-img layout="fixed"
                                        src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/icon-cart.png"
                                        alt="cart-icon" class="icon" width="22" height="22" />
                                    <span class="dot"></span>
                                </div>
                            </li>
                            <li class="nav-item">
                                <span class="icon-wrap">
                                    <amp-img class="call-icon" layout="responsive"
                                        src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/call-icon.png"
                                        alt="call icon" width="20" height="20" />
                                </span>
                                <p class="icon-text">9878725637</p>
                            </li>
                        </ul>
                    </div>
                </header>
                <div class="step1" [hidden]="productCatalog01.currentStep != 1">
                    <div class="bs-sec typ-look">
                        <div class="sec-head">
                            <h3 class="sec-title">PRODUCTS</h3>
                        </div>
                        <div class="sec-body">
                            <div class="container">
                                <div class="catalog-card">
                                    <div class="catalog-img">
                                        <h3 class="offer-band">Get 20% off for your first purchase.</h3>
                                        <!-- Change Product Image -->
                                        <amp-img
                                            src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/look-1.png"
                                            layout="responsive" alt="look" width="506" height="316" />
                                        <!-- Change Product Image -->
                                        <span class="cart-wrap">
                                            <span class="count" hidden [hidden]="productCatalog01.product1.qty <= 0"
                                                [text]="productCatalog01.product1.qty"></span>
                                            <amp-img layout="fixed"
                                                src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/icon-cart.png"
                                                alt="cart-icon" class="icon" width="27" height="27" />
                                        </span>
                                    </div>
                                    <div class="catalog-body">
                                        <div class="c-wrap">
                                            <h3 class="c-title">Mystic Elixir</h3>
                                            <p class="c-amt">
                                                <span class="rupee-sign">₹</span>
                                                <span class="amount"
                                                    [text]="(productCatalog01.product1.qty*productCatalog01.product1.price).toFixed(2)">1500.00</span>
                                            </p>
                                            <input hidden name='101'
                                                [value]="productCatalog01.product1.variantId == 101 ? productCatalog01.product1.qty:1" />
                                        </div>
                                        <div class="c-wrap">
                                            <p class="c-desc">is simply dummy text of the new age fashion industry.</p>
                                            <div class="btn-wrap">
                                                <div class="product-count">
                                                    <div class="product-count-sign" tabindex="1" role on="tap:AMP.setState({
                                                        productCatalog01 : {
                                                            product1: {
                                                                qty: productCatalog01.product1.qty > 0 ? productCatalog01.product1.qty - 1 : 0
                                                            }
                                                        }
                                                    })">
                                                        <amp-img layout="fixed"
                                                            src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/minsu-icon.png"
                                                            alt="minus-icon" class="icon" width="13" height="13" />
                                                    </div>
                                                    <div class="product-count-value"
                                                        [text]="productCatalog01.product1.qty">0</div>
                                                    <div class="product-count-sign" tabindex="1" on="tap:AMP.setState({
                                                            productCatalog01 :{
                                                                product1: {
                                                                    qty: productCatalog01.product1.qty < 5 ? productCatalog01.product1.qty + 1 : 5
                                                                }
                                                            }
                                                        })">
                                                        <amp-img layout="fixed"
                                                            src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/plus-icon.png"
                                                            alt="plus-icon" class="icon" width="13" height="13" />
                                                    </div>
                                                </div>
                                                <!-- Change CTA -->
                                                <button type="button" class="catalog-cta"
                                                    on="tap:AMP.setState({productCatalog01 :{product1: {addedToCart:true}}})">
                                                    ADD TO CART
                                                </button>
                                                          <!-- Change CTA -->
                                            </div>
                                        </div>
                                    </div>
                                </div>
                                <!-- Second product card -->
                                <div class="catalog-card">
                                    <div class="catalog-img">
                                        <h3 class="offer-band">Get 20% off for your first purchase.</h3>
                                        <amp-img
                                            src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/look-2.png"
                                            layout="responsive" alt="look" width="506" height="316" />
                                        <span class="cart-wrap">
                                            <span class="count" hidden [hidden]="productCatalog01.product2.qty <= 0"
                                                [text]="productCatalog01.product2.qty"></span>
                                            <amp-img layout="fixed"
                                                src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/icon-cart.png"
                                                alt="cart-icon" class="icon" width="27" height="27" />
                                        </span>
                                    </div>
                                    <div class="catalog-body">
                                        <div class="c-wrap">
                                            <h3 class="c-title">Opulent Essence</h3>
                                            <p class="c-amt">
                                                <span class="rupee-sign">₹</span>
                                                <span class="amount"
                                                    [text]="(productCatalog01.product2.qty*productCatalog01.product2.price).toFixed(2)">1500</span>
                                            </p>
                                            <input hidden name='102'
                                                [value]="productCatalog01.product2.variantId == 102 ? productCatalog01.product2.qty:1" />
                                        </div>
                                        <div class="c-wrap">
                                            <p class="c-desc">is simply dummy text of the new age fashion industry.</p>
                                            <div class="btn-wrap">
                                                <div class="product-count">
                                                    <div class="product-count-sign" tabindex="1" role on="tap:AMP.setState({
                                                            productCatalog01 : {
                                                                product2: {
                                                                    qty: productCatalog01.product2.qty > 0 ? productCatalog01.product2.qty - 1 : 0
                                                                }
                                                            }
                                                        })">
                                                        <amp-img layout="fixed"
                                                            src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/minsu-icon.png"
                                                            alt="minus-icon" class="icon" width="13" height="13" />
                                                    </div>
                                                    <div class="product-count-value"
                                                        [text]="productCatalog01.product2.qty">0</div>
                                                    <div class="product-count-sign" tabindex="1" on="tap:AMP.setState({
                                                            productCatalog01 :{
                                                                product2: {
                                                                    qty: productCatalog01.product2.qty < 5 ? productCatalog01.product2.qty + 1 : 5
                                                                }
                                                            }
                                                        })">
                                                        <amp-img layout="fixed"
                                                            src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/plus-icon.png"
                                                            alt="plus-icon" class="icon" width="13" height="13" />
                                                    </div>
                                                </div>
                                                <button type="button" class="catalog-cta"
                                                    on="tap:AMP.setState({productCatalog01 :{product2: {addedToCart:true}}})">
                                                    ADD TO CART
                                                </button>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                                <input hidden name="amount" [value]='(
                                    (productCatalog01.product1.qty * productCatalog01.product1.price) +
                                    (productCatalog01.product2.qty * productCatalog01.product2.price) +
                                    (productCatalog01.product3.qty * productCatalog01.product3.price) +
                                    (productCatalog01.product4.qty * productCatalog01.product4.price) +
                                    (productCatalog01.product5.qty * productCatalog01.product5.price)
                                ).toFixed(2)' />
                            </div>
                        </div>
                    </div>
                    <!-- product section -->
                    <div class="bs-sec typ-product">
                        <div class="sec-head">
                            <h3 class="sec-title">Product Suggestions</h3>
                        </div>
                        <div class="sec-body">
                            <div class="container">
                                <ul class="lyt-grid">
                                    <li class="grid-item">
                                        <div class="product-card">
                                            <div class="img-wrap">
                                                <!-- Change image src as per your requirements -->
                                                <amp-img layout="responsive"
                                                    src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/product-3.png"
                                                    alt="product" width="150" height="177" />
                                            </div>
                                            <button type="button" class="p-cart-icon"
                                                on="tap:AMP.setState({productCatalog01 :{product3: {addedToCart:true, qty:1}}})">
                                                <amp-img layout="fixed"
                                                    src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/icon-cart.png"
                                                    alt="cart-icon" class="icon" width="13" height="13"></amp-img>
                                            </button>
                                            <div class="product-info">
                                                <div class="p-wrap">
                                                    <h3 class="p-title">Product name</h3>
                                                    <p class="p-amt"><span class="rupee-sign">₹</span>1500</p>
                                                </div>
                                                <p class="p-desc">Is simply dummy text of the new age fashion industry.
                                                </p>
                                            </div>
                                        </div>
                                    </li>
                                    <li class="grid-item">
                                        <div class="product-card">
                                            <div class="img-wrap">
                                                <!-- Change image src as per your requirements -->
                                                <amp-img layout="responsive"
                                                    src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/product-2.png"
                                                    alt="product" width="150" height="177" />
                                            </div>
                                            <button type="button" class="p-cart-icon"
                                                on="tap:AMP.setState({productCatalog01 :{product4: {addedToCart:true, qty:1}}})">
                                                <amp-img layout="fixed"
                                                    src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/icon-cart.png"
                                                    alt="cart-icon" class="icon" width="13" height="13" />
                                            </button>
                                            <div class="product-info">
                                                <div class="p-wrap">
                                                    <h3 class="p-title">Product name</h3>
                                                    <p class="p-amt"><span class="rupee-sign">₹</span>1500</p>
                                                </div>
                                                <p class="p-desc">Is simply dummy text of the new age fashion industry.
                                                </p>
                                            </div>
                                        </div>
                                    </li>
                                    <li class="grid-item">
                                        <div class="product-card">
                                            <div class="img-wrap">
                                                <!-- Change image src as per your requirements -->
                                                <amp-img layout="responsive"
                                                    src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/product-1.png"
                                                    alt="product" width="150" height="177" />
                                            </div>
                                            <button type="button" class="p-cart-icon"
                                                on="tap:AMP.setState({productCatalog01 :{product5: {addedToCart:true, qty:1}}})">
                                                <amp-img layout="fixed"
                                                    src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/icon-cart.png"
                                                    alt="cart-icon" class="icon" width="13" height="13" />
                                            </button>
                                            <div class="product-info">
                                                <div class="p-wrap">
                                                    <h3 class="p-title">Product name</h3>
                                                    <p class="p-amt"><span class="rupee-sign">₹</span>1500</p>
                                                </div>
                                                <p class="p-desc">Is simply dummy text of the new age fashion industry.
                                                </p>
                                            </div>
                                        </div>
                                    </li>
                                </ul>
                                <div class="btn-wrap">
                                    <a href="https://google.com" class="shop-cta">Shop now
                                        <amp-img layout="fixed"
                                            src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/arrow.png"
                                            alt="arrow" width="17" height="10"
                                            style="margin-left: 10px; max-width: 17px" />
                                    </a>
                                </div>
                            </div>
                        </div>
                    </div>
                    <!-- product section -->
                    <!-- footer section -->
                    <footer class="cp-footer">
                        <div class="container">
                            <ul class="media-logo-list">
                                <li class="logo-item">
                                    <a href="https://www.google.co.in/" class="logo-link">
                                        <amp-img layout="responsive"
                                            src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/logo-insta.png"
                                            alt="instagram" class="media-logo" width="20" height="20"></amp-img>
                                    </a>
                                </li>
                                <li class="logo-item">
                                    <a href="https://www.google.co.in/" class="logo-link">
                                        <amp-img layout="responsive"
                                            src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/logo-facebook.png"
                                            alt="facebook" class="media-logo" width="20" height="20"></amp-img>
                                    </a>
                                </li>
                                <li class="logo-item">
                                    <a href="https://www.google.co.in/" class="logo-link">
                                        <amp-img layout="responsive"
                                            src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/logo-x.png"
                                            alt="x" class="media-logo" width="20" height="20"></amp-img>
                                    </a>
                                </li>
                            </ul>
                            <p class="f-desc">is simply dummy text of the printing and typesetting industry. Lorem Ipsum
                                has
                                been the industry's standard dummy </p>
                                <p class="f-desc" style="margin-top: 20px;">To stop receiving these emails, <a href="https://www.google.com" style="color:#ffff;font-weight:bold;text-decoration:none;">unsubscribe here</a></p>
                        </div>
                    </footer>
                    <!-- footer section -->
                </div>
                <div class="step2" hidden [hidden]="productCatalog01.currentStep != 2">
                    <div class="container">
                        <div class="bs-sec typ-bottom-padding-zero" [hidden]="
                            (productCatalog01.product1.qty <= 0 &&
                            productCatalog01.product2.qty <= 0 &&
                            productCatalog01.product3.qty <= 0 &&
                            productCatalog01.product4.qty <= 0 &&
                            productCatalog01.product5.qty <= 0)
                                    ">
                            <div class="sec-head">
                                <h3 class="sec-title typ-2">PRODUCTS</h3>
                            </div>
                            <div class="sec-body">
                                <ul class="product-list">
                                    <li class="product-item" [hidden]="productCatalog01.product1.qty == 0">
                                        <div class="lhs">
                                            <h3 class="p-name" [text]="productCatalog01.product1.title">Mystic Elixir
                                            </h3>
                                            <p class="p-desc"> is simply dummy text of the new age fashion industry.</p>
                                            <p class="p-quality">Qty : <span
                                                    [text]="productCatalog01.product1.qty"></span></p>
                                        </div>
                                        <div class="rhs">
                                            <button class="delete-icon" on="tap:AMP.setState({
                                                    productCatalog01 :{
                                                        product1: {addedToCart:false, qty:0}
                                                    }
                                                })">
                                                <amp-img
                                                    src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/delete-icon.png"
                                                    width="24" height="24" layout="fixed" alt="delete-icon">
                                                </amp-img>
                                            </button>
                                            <p class="p-amt">₹ <span
                                                    [text]="(productCatalog01.product1.qty*productCatalog01.product1.price).toFixed(2)"></span>
                                            </p>
                                        </div>
                                    </li>
                                    <li class="product-item" [hidden]="productCatalog01.product2.qty == 0">
                                        <div class="lhs">
                                            <h3 class="p-name" [text]="productCatalog01.product2.title">Mystic Elixir
                                            </h3>
                                            <p class="p-desc">is simply dummy text of the new age fashion industry.</p>
                                            <p class="p-quality">Qty : <span
                                                    [text]="productCatalog01.product2.qty"></span></p>
                                        </div>
                                        <div class="rhs">
                                            <button class="delete-icon" on="tap:AMP.setState({
                                                    productCatalog01 :{
                                                        product2: {addedToCart:false, qty:0}
                                                    }
                                                })">
                                                <amp-img
                                                    src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/delete-icon.png"
                                                    width="24" height="24" layout="fixed" alt="delete-icon">
                                                </amp-img>
                                            </button>
                                            <p class="p-amt">₹ <span
                                                    [text]="(productCatalog01.product2.qty*productCatalog01.product2.price).toFixed(2)"></span>
                                            </p>
                                        </div>
                                    </li>
                                    <li class="product-item" [hidden]="productCatalog01.product3.qty == 0">
                                        <div class="lhs">
                                            <h3 class="p-name" [text]="productCatalog01.product3.title">Product Name
                                            </h3>
                                            <p class="p-desc">is simply dummy text of the new age fashion industry.</p>
                                            <p class="p-quality">Qty : <span
                                                    [text]="productCatalog01.product3.qty"></span></p>
                                        </div>
                                        <div class="rhs">
                                            <button class="delete-icon" on="tap:AMP.setState({
                                                    productCatalog01 :{
                                                        product3: {addedToCart:false, qty:0}
                                                    }
                                                })">
                                                <amp-img
                                                    src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/delete-icon.png"
                                                    width="24" height="24" layout="fixed" alt="delete-icon">
                                                </amp-img>
                                            </button>
                                            <p class="p-amt">₹ <span
                                                    [text]="(productCatalog01.product3.qty*productCatalog01.product3.price).toFixed(2)"></span>
                                            </p>
                                        </div>
                                    </li>
                                    <li class="product-item" [hidden]="productCatalog01.product4.qty == 0">
                                        <div class="lhs">
                                            <h3 class="p-name" [text]="productCatalog01.product4.title">Product Name
                                            </h3>
                                            <p class="p-desc">is simply dummy text of the new age fashion industry.</p>
                                            <p class="p-quality">Qty : <span
                                                    [text]="productCatalog01.product4.qty"></span></p>
                                        </div>
                                        <div class="rhs">
                                            <button class="delete-icon" on="tap:AMP.setState({
                                                    productCatalog01 :{
                                                        product4: {addedToCart:false, qty:0}
                                                    }
                                                })">
                                                <amp-img
                                                    src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/delete-icon.png"
                                                    width="24" height="24" layout="fixed" alt="delete-icon">
                                                </amp-img>
                                            </button>
                                            <p class="p-amt">₹ <span
                                                    [text]="(productCatalog01.product4.qty*productCatalog01.product4.price).toFixed(2)"></span>
                                            </p>
                                        </div>
                                    </li>
                                    <li class="product-item" [hidden]="productCatalog01.product5.qty == 0">
                                        <div class="lhs">
                                            <h3 class="p-name" [text]="productCatalog01.product5.title">Product Name
                                            </h3>
                                            <p class="p-desc">is simply dummy text of the new age fashion industry.</p>
                                            <p class="p-quality">Qty : <span
                                                    [text]="productCatalog01.product5.qty"></span></p>
                                        </div>
                                        <div class="rhs">
                                            <button class="delete-icon" on="tap:AMP.setState({
                                                    productCatalog01 :{
                                                        product5: {addedToCart:false, qty:0}
                                                    }
                                                })">
                                                <amp-img
                                                    src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/delete-icon.png"
                                                    width="24" height="24" layout="fixed" alt="delete-icon">
                                                </amp-img>
                                            </button>
                                            <p class="p-amt">₹ <span
                                                    [text]="(productCatalog01.product5.qty*productCatalog01.product5.price).toFixed(2)"></span>
                                            </p>
                                        </div>
                                    </li>
                                    <li class="product-item typ-final">
                                        <div class="lhs">
                                            <h3 class="p-total">Amount Total</h3>
                                        </div>
                                        <div class="rhs">
                                            <p class="p-amt p-total-amt">₹
                                                <span [text]="(
                                                    (
                                                        (productCatalog01.product1.qty * productCatalog01.product1.price) +
                                                        (productCatalog01.product2.qty * productCatalog01.product2.price) +
                                                        (productCatalog01.product3.qty * productCatalog01.product3.price) +
                                                        (productCatalog01.product4.qty * productCatalog01.product4.price) +
                                                        (productCatalog01.product5.qty * productCatalog01.product5.price)
                                                    ) * (100 - 0) / 100
                                                ).toFixed(2) + ' '">0</span>
                                            </p>
                                        </div>
                                    </li>
                                </ul>
                            </div>
                        </div>
                        <div class="bs-sec">
                            <div class="sec-head ">
                                <h3 class="sec-title typ-2">ADD DETAILS</h3>
                            </div>
                            <div class="sec-body">
                                <ul class="form-list">
                                    <!-- First Name -->
                                    <li class="form-item">
                                        <input id="productCatalog01-first_name" required on="
                                            change:AMP.setState({
                                                productCatalog01: { first_name: event.value }
                                            });
                                            tap:AMP.setState({
                                                formValidation: { first_name_invalid: event.target.validity.valueMissing }
                                            })
                                        " type="text" name="first_name" class="input" placeholder="First name" [value]="productCatalog01.first_name" [aria-invalid]="formValidation.first_name_invalid" aria-describedby="productCatalog01.first_name">
                                        <div class="error-msg" visible-when-invalid="valueMissing" validation-for="productCatalog01-first_name" id="productCatalog01.first_name">
                                            First name is required.
                                        </div>
                                    </li>
                                    <!-- Last Name -->
                                    <li class="form-item">
                                        <input id="productCatalog01-last_name" required on="
                                            change:AMP.setState({
                                                productCatalog01: { last_name: event.value }
                                            });
                                            tap:AMP.setState({
                                                formValidation: { last_name_invalid: event.target.validity.valueMissing }
                                            })
                                        " type="text" name="last_name" class="input" placeholder="Last name" [value]="productCatalog01.last_name" [aria-invalid]="formValidation.last_name_invalid" aria-describedby="formValidation.last_name_invalid">
                                        <div class="error-msg" visible-when-invalid="valueMissing" validation-for="productCatalog01-last_name" id="formValidation.last_name_invalid">
                                            Last name is required.
                                        </div>
                                    </li>
                                    <!-- Phone Number -->
                                    <li class="form-item">
                                        <input id="productCatalog01-phoneNumber" required [pattern]="productCatalog01.currentStep==2 ? '\\d{10}' : '*'" on="
                                            change:AMP.setState({
                                                productCatalog01: { phoneNumber: event.value }
                                            });
                                            tap:AMP.setState({
                                                formValidation: { phoneNumber_invalid: event.target.validity.valueMissing || event.target.validity.patternMismatch }
                                            })
                                        " maxlength="10" type="text" name="phoneNumber" class="input" placeholder="Phone Number" [value]="productCatalog01.phoneNumber" pattern="\d{10}" [aria-invalid]="formValidation.phoneNumber_invalid" aria-describedby="productCatalog01.phoneNumber">
                                        <div class="error-msg" visible-when-invalid="valueMissing" validation-for="productCatalog01-phoneNumber" id="productCatalog01.phoneNumber">
                                            Phone number is required.
                                        </div>
                                        <div class="error-msg" visible-when-invalid="patternMismatch" validation-for="productCatalog01-phoneNumber">
                                            Please enter a valid phone number.
                                        </div>
                                    </li>
                                    <!-- Email -->
                                    <li class="form-item">
                                        <input id="productCatalog01-email" required type="email" on="
                                            change:AMP.setState({
                                                productCatalog01: { email: event.value }
                                            });
                                            tap:AMP.setState({
                                                formValidation: { email_invalid: event.target.validity.valueMissing || event.target.validity.typeMismatch }
                                            })
                                        " name="email" class="input" placeholder="E-mail" [value]="productCatalog01.email" [aria-invalid]="formValidation.email_invalid" aria-describedby="productCatalog01.email">
                                        <div class="error-msg" visible-when-invalid="valueMissing" validation-for="productCatalog01-email" id="productCatalog01.email">
                                            Email is required.
                                        </div>
                                        <div class="error-msg" visible-when-invalid="patternMismatch" validation-for="productCatalog01-email">
                                            Please enter a valid Email.
                                        </div>
                                    </li>
                                    <!-- Address -->
                                    <li class="form-item typ-full">
                                        <input id="productCatalog01-address" required on="
                                            change:AMP.setState({
                                                productCatalog01: { address: event.value }
                                            });
                                            tap:AMP.setState({
                                                formValidation: { address_invalid: event.target.validity.valueMissing }
                                            })
                                        " name="address" class="input" placeholder="Address" [value]="productCatalog01.address" [aria-invalid]="formValidation.address_invalid" aria-describedby="productCatalog01.address">
                                        <div class="error-msg" visible-when-invalid="valueMissing" validation-for="productCatalog01-address" id="productCatalog01.address">
                                            Address is required.
                                        </div>
                                    </li>
                                    <!-- Landmark -->
                                    <li class="form-item">
                                        <input id="productCatalog01-landmark" required on="
                                            change:AMP.setState({
                                                productCatalog01: { landmark: event.value }
                                            });
                                            tap:AMP.setState({
                                                formValidation: { landmark_invalid: event.target.validity.valueMissing }
                                            })
                                        " name="landmark" class="input" placeholder="Landmark" [value]="productCatalog01.landmark" [aria-invalid]="formValidation.landmark_invalid" aria-describedby="productCatalog01.landmark">
                                        <div class="error-msg" visible-when-invalid="valueMissing" validation-for="productCatalog01-landmark" id="productCatalog01.landmark">
                                            Landmark is required.
                                        </div>
                                    </li>
                                    <!-- Pincode -->
                                    <li class="form-item">
                                        <input id="productCatalog01-pincode" required on="
                                            change:AMP.setState({
                                                productCatalog01: { pincode: event.value }
                                            });
                                            tap:AMP.setState({
                                                formValidation: { pincode_invalid: event.target.validity.valueMissing }
                                            })
                                        " name="pincode" class="input" placeholder="Pincode" [value]="productCatalog01.pincode" maxlength="6" type="number" [aria-invalid]="formValidation.pincode_invalid" aria-describedby="productCatalog01.pincode">
                                        <div class="error-msg" visible-when-invalid="valueMissing" validation-for="productCatalog01-pincode" id="productCatalog01.pincode">
                                            Pincode is required.
                                        </div>
                                    </li>
                                    <!-- City -->
                                    <li class="form-item">
                                        <input id="productCatalog01-city" required on="
                                            change:AMP.setState({
                                                productCatalog01: { city: event.value }
                                            });
                                            tap:AMP.setState({
                                                formValidation: { city_invalid: event.target.validity.valueMissing }
                                            })
                                        " type="text" name="city" class="input" placeholder="City" [value]="productCatalog01.city" [aria-invalid]="formValidation.city_invalid" aria-describedby="productCatalog01.city">
                                        <div class="error-msg" visible-when-invalid="valueMissing" validation-for="productCatalog01-city" id="productCatalog01.city">
                                            City is required.
                                        </div>
                                    </li>
                                    <!-- State -->
                                    <li class="form-item">
                                        <input id="productCatalog01-state" required on="
                                            change:AMP.setState({
                                                productCatalog01: { state: event.value }
                                            });
                                            tap:AMP.setState({
                                                formValidation: { state_invalid: event.target.validity.valueMissing }
                                            })
                                        " type="text" name="state" class="input" placeholder="State" [value]="productCatalog01.state" [aria-invalid]="formValidation.state_invalid" aria-describedby="productCatalog01.state">
                                        <div class="error-msg" visible-when-invalid="valueMissing" validation-for="productCatalog01-state" id="productCatalog01.state">
                                            State is required.
                                        </div>
                                    </li>
                                    <!-- Payment Mode -->
                                    <li class="form-item typ-full mt-32">
                                        <label for="cod" class="field-wrap">
                                            <input type="radio" checked="checked" id="cod" name="payment" required on="
                                                change:AMP.setState({
                                                    productCatalog01: { payment_mode: 'cod' }
                                                })
                                            " [value]="productCatalog01.payment_mode" class="user-valid valid" value="">
                                            <span class="checkmark"></span>
                                            Cash on Delivery
                                        </label>
                                        <label class="field-wrap" for="online">
                                            <input type="radio" id="online" name="payment" on="
                                                change:AMP.setState({
                                                    productCatalog01: { payment_mode: 'online' }
                                                })
                                            " [value]="productCatalog01.payment_mode" class="user-valid valid" value="">
                                            <span class="checkmark"></span>
                                            Online
                                        </label>
                                    </li>
                                    <!-- Submit Button -->
                                    <li class="form-item typ-full">
                                        <button class="form-btn" on="
                                            tap:AMP.setState({
                                                formValidation: {
                                                    first_name_invalid: !productCatalog01.first_name,
                                                    last_name_invalid: !productCatalog01.last_name,
                                                    phoneNumber_invalid: !productCatalog01.phoneNumber || !/^\d{10}$/.test(productCatalog01.phoneNumber),
                                                    email_invalid: !productCatalog01.email,
                                                    address_invalid: !productCatalog01.address,
                                                    landmark_invalid: !productCatalog01.landmark,
                                                    pincode_invalid: !productCatalog01.pincode,
                                                    city_invalid: !productCatalog01.city,
                                                    state_invalid: !productCatalog01.state,
                                                },
                                                productCatalog01: { currentStep: 3 }
                                            })
                                        ">
                                            Next
                                        </button>
                                    </li>
                                </ul>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="step3" hidden [hidden]="productCatalog01.currentStep != 3">
                    <div class="modal-overlay">
                        <div class="modal">
                            <div class="modal-content">
                                <div class="modal-head">
                                    <span class="close">x</span>
                                </div>
                                <div class="modal-body">
                                    <h3 class="m-title">THANKS for shopping</h3>
                                    <p class="m-desc">
                                        is simply dummy text of the printing and typesetting industry. Lorem Ipsum has
                                        been the
                                        industry's standard dummy text ever since the 1500s
                                    </p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="step4" hidden submit-error>
                    <div class="modal-overlay">
                        <div class="modal hidden">
                            <div class="modal-content">
                                <div class="modal-head">
                                    <span class="close">x</span>
                                </div>
                                <div class="modal-body">
                                    <h3 class="m-title">Error</h3>
                                    <p class="m-desc">
                                        is simply dummy text of the printing and typesetting industry. Lorem Ipsum has
                                        been the
                                        industry's standard dummy text ever since the 1500s
                                    </p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </form>
        </div>
    </div>
</body>
</html>
```

</details>

## Cart Abandonment

This AMP email template is designed to help recover lost sales by reminding users about the products left in their shopping carts. With interactive AMP elements, users can view product details, scroll through images, and proceed to checkout, all within the email.

<details>

<summary>Expand to know more about the template.</summary>

### Use Case Examples

- Recover lost revenue by reminding users about items left in their shopping cart.
- Re-engage users with personalized product suggestions based on past purchases or browsing behavior.
- Promote urgency with limited-time offers or low stock alerts tied to abandoned items.
- Enhance the shopping experience by allowing users to interact with product carousels or resume checkout directly within the email

### Template Customization Options

- Replace the Logo
- Update Banner/Product Images
- Update Call-To-Actions (CTAs)
- Update Links in the Header/Footer
- Change the Theme or Background Color

### Template Code

```html
Jump to

Confluence navigation
Side navigation
Page

Home

Recent

Spaces

Teams

Apps
Templates

Create
Search

9+



Customer Success

Shortcuts

Content


Search by title
Results will update as you type.

Show more below

Create

Blogs


Apps



Customer Success
/
Email AMP & HTML Templates





Share


Email AMP & HTML Templates


Owned by Shruti Awasthi

Last updated: Feb 12, 2025
1 min read

105 people viewed
Objective: These are prebuilt HTML and AMP email templates that are designed to empower marketers with versatile, user-friendly solutions for their communication needs. These templates are fully customizable to reflect unique branding and cover common use cases such as cart abandonment, subscription confirmations, welcome emails, festive promotions, newsletters, etc.. 

For ease of use, a detailed readme section is included to enable marketers to customize the templates on their own.

Table of Content:

Table A: HTML Templates:

S.no

Template Name

Read Me

HTML File

S.no

Template Name

Read Me

HTML File

1

Welcome Mailer

Welcome Mailer-1.pdf 
	
Welcome.html 

2

Welcome Mailer-Option 2 

Welcome Mailers-2.pdf 

Welcome Mailer 2.html 

3

What's in the Store ?

What's in the store.pdf 

 Whats in Store.html 

4

First Purchase Incentive

First-Purchase-Incentive.pdf 

 First Purchase.html 

5

Newsletter

Newsletter.pdf 

 Newsletter.html 

6

Promotional Mailer

Promotional Template.pdf 

 Promotional.html 

7

Cart Abandonment 

_Cart Abandonment(HTML).pdf 

 Cart-Abandonment.html 

8

WinBack Mailer

WinBack.pdf

 Winback.html 

9

Flash Sale

FlashSale Template.pdf 

FlashSale.html 

10

Scratch Card - Festive (Diwali)

Scratch Card-HTML.pdf 

Scratch Card - Festive.html  

11

Informative Mailer

Informative-Mailer.pdf 

Informative.html 

12

Subscription Renewal

Subscription - HTML Template.pdf 

  Subscription.html 

13

Birthday Mailer

Birthday Template.pdf 

 Birthday.html 

14

Anniversary Mailer

Anniversary Template.pdf 

 Anniversary.html 

15

Loyalty Expiry

Loyalty Expiry Template.pdf 

 Loyalty Expiry.html 

16

Loyalty Points

Loyalty Points Template.pdf 

 Loyalty Points.html 

17

Feedback 

FeedBack HTML.pdf
	
Feedback.html 

18

Access to Early Sale

Access to Early Sales.pdf 

Access to Early Sales.html 

19

Account Verification

Accout Verification.pdf 

AccountVerification.html 

20

Order Placed

Order Placed HTML.pdf 

Order Placed.html 

21

Order Shipped

Order Shipped.pdf 

Order Shipped.html 

22

Order Delivered

Order Delivered.pdf 

Order Delivered.html 

23

Password Reset

Password Reset.pdf 

Password Reset.html  

24

Show Recommendation (White)

Show Recommendation(White).pdf 

Show Recommendation (White).html 

25

Show Recommendation (Black)

Show Recommendation (Black).pdf 

Show Recommendation Black.html 

26

Referral

Referral- HTML.pdf 

Referral.html 

Table B: AMP Templates:

S.no

Template Name

Read Me 

Code File

1

What's in the Store ?

What's in the store.pdf 

Whats in Store.html 

2

Cart Abandonment 

CART ABANDONMENT TEMPLATE-AMP.pdf 

Cart Abandonment AMP.html 

3

Diwali - GIF (Scratch Card) 

Scratch Card AMP Template.pdf 

Scratch- AMP.html 

4

Spin The Wheel 

Spin the wheel AMP.pdf 

Spin the Wheel.html 

5

AMP Form - Option 1

AMP Form Template 1.pdf 

AMP Form1.html 

6

AMP Form - Option 2

AMP Form Template 2.pdf 

AMP Form2.html 

7

AMP Form - Option 3

AMP Form Template 3.pdf 

Amp Form3.html 

8

EMI Calculator

EMI Calculator.pdf 

EMI Calculator.html 

9

SIP Calculator

SIP Calculator.pdf 

SIP Calculator.html 

10

Insurance Calculator

Insurance Calculator.pdf 

Insurance Calculator.html 

11

Relevant Products

Relevant Products - AMP.pdf 

Relevant Products.html 

12

Show Recommendations

Show Recommendations AMP.pdf 

Show Recommendations.html 

13

Show Recommendations with Notify Me

Show Recommendation With Notify Me AMP.pdf 

Show Recommendations - Notify Me.html 

14

Feedback 

Feedback Template AMP.pdf 

Feedback.html 

15

Zodiac

ZODIAC -  AMP.pdf 

Zodiac.html 

16

New Image on Click

New Image on click AMP.pdf 

New Image on Click.html 

Add label
Related content


Email Templates
Email Templates
Brendan Davies
More like this
NPS Sample Email Templates
NPS Sample Email Templates
Customer Success
Read with this
Expanded Out-of-the-box Email Template Library <WIP>
Expanded Out-of-the-box Email Template Library <WIP>
Product Universe
More like this
New OOTB Email Templates | UX Copy
New OOTB Email Templates | UX Copy
Product Universe
More like this
Scratch Card | Custom HTML InApp Template
Scratch Card | Custom HTML InApp Template
TSG Knowledge Base
Read with this
Stories In-App Custom HTML template
Stories In-App Custom HTML template
TSG Knowledge Base
Read with this

thumbs up

clapping hands

party popper

Be the first to add a reaction

Cart Abandonment AMP.html
html · 77 KB

<!doctype html>
<html ⚡4email>
<head>
    <meta charset="utf-8">
    <script async src="https://cdn.ampproject.org/v0.js"></script>
    <script async custom-element="amp-form" src="https://cdn.ampproject.org/v0/amp-form-0.1.js"></script>
    <script async custom-element="amp-bind" src="https://cdn.ampproject.org/v0/amp-bind-0.1.js"></script>
    <style amp4email-boilerplate>
        body {
            visibility: hidden
        }
    </style>
    <style amp-custom>
        * {
            margin: 0;
            padding: 0;
        }
        ul,
        li {
            list-style: none;
        }
        /* Change Theme */
        body {
            font-family: "Helvetica", arial, sans-serif;
            font-weight: 400;
            background-color: rgb(248, 250, 252);
        }
        /* Change Theme */
        img {
            width: 100%;
            height: 100%;
            object-fit: contain;
        }
        amp-img {
            position: relative;
        }
        .main {
            position: relative;
            width: 100%;
            max-width: 600px;
            overflow: hidden;
            margin: 0 auto;
            background: #FFFFFF;
        }
        .container {
            max-width: 85%;
            margin: 0 auto;
        }
        @media only screen and (max-width: 400px) {
            .container,
            .main {
                max-width: 95%;
            }
        }
        .cp-header {
            padding: 0 30px;
        }
        .cp-header.typ-shadow {
            box-shadow: 0px 4px 4px 0px #00000040;
        }
        .logo-wrap {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .logo-wrap .img-wrap {
            width: 127px;
            height: 58px;
            margin: 8.5px 0;
        }
        .nav-list {
            list-style: none;
            display: flex;
            align-items: center;
        }
        .nav-list .nav-item {
            padding: 25px 19px;
            border-left: 0.5px solid #919191;
            display: flex;
            align-items: center;
        }
        .nav-list .nav-item:last-child {
            padding-right: 0;
        }
        .cart-icon {
            border: 0;
            outline: 0;
            position: relative;
            background-color: transparent;
        }
        .cart-icon.active .dot {
            display: inline-block;
        }
        .dot {
            width: 6px;
            height: 6px;
            background: #FF533F;
            border-radius: 50%;
            display: none;
            position: absolute;
            top: 2px;
            right: 0px;
            z-index: 1;
        }
        .call-icon {
            width: 20px;
            height: 20px;
            margin-right: 5px;
        }
        .icon-text {
            font-size: 14px;
            font-weight: 400;
            line-height: 24px;
            text-align: center;
            color: #464646;
        }
        .cp-banner {
            width: 100%;
            max-height: 361px;
            margin-bottom: 22px;
        }
        .cp-footer {
            margin-top: 50px;
            background: #1E1E1E;
            padding: 32px 0 34px;
        }
        .media-logo-list {
            display: flex;
            justify-content: center;
            align-items: center;
            margin-bottom: 20px;
        }
        .media-logo-list .logo-item {
            padding: 6px 32px;
            border: 1px solid #FFFFFF;
        }
        .media-logo-list .logo-item .logo-link {
            display: inline-block;
        }
        .media-logo {
            width: 20px;
            height: 20px;
            display: inline-block;
        }
        .f-desc {
            font-size: 14px;
            font-weight: 400;
            line-height: 20px;
            text-align: center;
            color: #FFFFFF;
            margin: 0 auto;
            max-width: 84%;
            text-transform: capitalize;
        }
        .bs-sec {
            padding: 28px 0;
        }
        .bs-sec.typ-product {
            background: #F1F1F1;
        }
        .bs-sec .sec-title {
            padding: 0 26px 12px;
            text-transform: capitalize;
            font-size: 20px;
            font-weight: 400;
            line-height: 24px;
            text-align: center;
            position: relative;
            width: max-content;
            margin: 0 auto;
        }
        .bs-sec .sec-title.typ-2 {
            margin: 0;
            padding: 0 0 2px;
        }
        /* .bs-sec .sec-title.typ-2:after{
            display: none;
        } */
        .lyt-grid {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            gap: 15px;
            margin-top: 20px;
        }
        .lyt-grid .grid-item {
            width: 33%;
        }
        .product-card {
            padding: 5px;
            position: relative;
            background: #FFFFFF;
        }
        .product-card .img-wrap {
            max-height: 177px;
            max-width: 150px;
            margin: 0 auto;
            overflow: hidden;
        }
        .product-card .p-cart-icon {
            background: #FFFFFF;
            padding: 3px 5px;
            border: 0;
            outline: 0;
            position: absolute;
            top: 5px;
            right: 5px;
            cursor: pointer;
        }
        .product-card .p-wrap {
            display: flex;
            justify-content: space-between;
            align-items: baseline;
            margin: 5px 0;
        }
        .product-card .p-title {
            width: 60%;
            font-size: 14px;
            font-weight: 400;
            line-height: 18px;
            color: #252525;
            padding-right: 5px;
        }
        .product-card .p-amt {
            color: #252525;
            font-size: 12px;
            font-weight: 300;
            line-height: 15px;
            text-align: right;
            font-style: italic;
        }
        .product-card .rupee-sign {
            font-size: 10px;
        }
        .product-card .p-desc {
            text-transform: capitalize;
            font-size: 8px;
            font-weight: 400;
            line-height: 13px;
            color: #909090;
            overflow: hidden;
            text-overflow: ellipsis;
            -webkit-line-clamp: 2;
            display: -webkit-box;
            -webkit-box-orient: vertical;
        }
        .btn-wrap {
            text-align: right;
        }
        .shop-cta {
            font-size: 12px;
            font-weight: 400;
            text-transform: capitalize;
            line-height: 15px;
            color: #000000;
            text-decoration: none;
            display: inline-block;
            text-align: center;
            margin-top: 15px;
        }
        .catalog-card {
            margin-top: 30px;
        }
        .catalog-card .catalog-img {
            max-width: 506px;
            max-height: 316px;
            position: relative;
        }
        .catalog-card .offer-band {
            background: #1e1e1e;
            text-align: center;
            padding: 7px 20px;
            font-size: 12px;
            font-weight: 400;
            line-height: 13px;
            letter-spacing: 0.25em;
            position: absolute;
            top: 0;
            left: 0;
            z-index: 1;
            width: 92%;
            color: #fff;
        }
        .catalog-card .cart-wrap {
            position: absolute;
            bottom: 0;
            right: 0;
            padding: 8px 10px;
            background: #fff;
            z-index: 1;
        }
        .catalog-card .cart-wrap .count {
            position: absolute;
            top: 8px;
            right: 8px;
            width: 11px;
            height: 11px;
            background: #FF533F;
            border-radius: 50%;
            color: #FFFFFF;
            font-size: 7px;
            font-weight: 400;
            line-height: 11px;
            text-align: center;
            z-index: 1;
        }
        .catalog-card .catalog-body {
            background: #f1f1f1;
            padding: 12px 14px 10px;
        }
        .catalog-card .c-wrap {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
        }
        .catalog-card .c-title {
            margin-bottom: 5px;
            font-size: 20px;
            font-weight: 400;
            line-height: 24px;
            color: #252525;
            width: 50%;
        }
        .catalog-card .c-amt {
            font-size: 22px;
            font-style: italic;
            font-weight: 400;
            line-height: 15px;
            text-align: right;
        }
        .catalog-card .rupee-sign {
            font-size: 10px;
        }
        .catalog-card .c-desc {
            font-size: 10px;
            font-weight: 400;
            line-height: 13px;
            color: #545454;
            width: 40%;
            text-transform: capitalize;
        }
        .catalog-card .btn-wrap {
            width: 60%;
            display: flex;
            justify-content: flex-end;
        }
        .catalog-card .catalog-cta {
            font-size: 14px;
            font-weight: 400;
            text-transform: uppercase;
            line-height: 20px;
            color: #FFFFFF;
            text-decoration: none;
            background: #000000;
            padding: 4px 34px;
            display: inline-block;
            text-align: center;
            max-width: 167px;
            border: none;
            margin-left: 10px;
            cursor: pointer;
        }
        .product-count {
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 6px;
            background: #FFF;
            width: 60px;
        }
        .product-count .product-count-sign {
            background: transparent;
            border: 0;
            outline: none;
            cursor: pointer;
        }
        .product-count-value {
            font-size: 12px;
            font-weight: 400;
            line-height: 15px;
            text-align: center;
        }
        .input {
            border: 0.5px solid #000000;
            padding: 7px 10px;
            font-family: "Helvetica", arial, sans-serif;
            font-size: 16px;
            font-weight: 400;
            line-height: 24px;
            color: #000000;
            width: -webkit-fill-available;
        }
        .input::-webkit-input-placeholder,
        .input::-moz-placeholder,
        .input:-ms-input-placeholder,
        .input:-moz-placeholder {
            color: #919191;
        }
        @media only screen and (max-width: 480px) {
            .cp-header {
                max-width: 100%;
                padding: 0 10px;
            }
            .logo-wrap .img-wrap {
                width: 101px;
                height: 48px;
                margin: 5.5px 0;
            }
            .nav-list .nav-item {
                padding: 15px 10px;
            }
            .call-icon {
                width: 18px;
                height: 18px;
            }
            .icon-text {
                font-size: 12px;
                line-height: 20px;
            }
            .lyt-grid {
                gap: 5px;
            }
            .product-card .p-title {
                font-size: 12px;
                line-height: 16px;
            }
            .product-card .p-amt {
                font-size: 10px;
                line-height: 16px;
            }
            .bs-sec .sec-title {
                padding: 0 20px 12px;
                font-size: 18px;
                line-height: 20px;
            }
            .catalog-card .catalog-cta {
                font-size: 10px;
                line-height: 14px;
                padding: 5px;
            }
        }
        .form-list {
            margin-top: 20px;
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            gap: 10px;
        }
        .form-item {
            width: 49%;
            position: relative;
            padding-bottom: 20px;
        }
        .form-item.typ-full {
            width: 100%;
        }
        [visible-when-invalid]{
            display: block;
        }
        .error-msg{
            font-size: 10px;  
            display: none;   
            position: absolute;
            bottom: 0; left: 0;       
        }
        .error-msg.visible{
            display: block;   
        }
        .field-wrap {
            display: block;
            position: relative;
            padding-left: 25px;
            margin-bottom: 10px;
            cursor: pointer;
            -webkit-user-select: none;
            -moz-user-select: none;
            -ms-user-select: none;
            user-select: none;
            font-size: 16px;
            font-weight: 400;
            line-height: 24px;
        }
        .field-wrap input {
            position: absolute;
            opacity: 0;
            cursor: pointer;
        }
        .checkmark {
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
            left: 0;
            height: 17px;
            width: 17px;
            background-color: #0B0B0B;
            border-radius: 50%;
        }
        .field-wrap input:checked~.checkmark {
            background-color: #0B0B0B;
        }
        .checkmark:after {
            content: "";
            position: absolute;            
            display: block;
        }
        .field-wrap input:checked~.checkmark:after {
           display: none;
        }
        .field-wrap .checkmark:after {
            top: 2px;
            left: 2px;
            width: 13px;
            height: 13px;
            border-radius: 50%;
            background: #FFFFFF;
        }
        .mt-32 {
            margin-top: 32px;
        }
        .form-btn {
            font-size: 20px;
            font-weight: 400;
            line-height: 24px;
            text-align: center;
            width: 100%;
            background: #252525;
            border: 0;
            outline: none;
            color: #FFF;
            padding: 10px;
            cursor: pointer;
        }
        .tab-3 {
            position: relative;
        }
        .modal-overlay {
            width: 100%;
            height: 100%;
            background-color: #000000;
            padding: 100px 0;
        }
        .modal {
            width: 75%;
            margin: 40px auto;
            z-index: 12;
            background: #FFF;
            padding: 70px 30px;
            position: relative;
        }
        .close {
            width: 27px;
            height: 27px;
            display: inline-block;
            text-align: center;
            background: #000000;
            font-size: 13px;
            color: #FFFFFF;
            line-height: 27px;
            border-radius: 50%;
            position: absolute;
            top: 6px;
            right: 6px;
            cursor: pointer;
        }
        .m-title {
            font-size: 20px;
            font-weight: 400;
            line-height: 24px;
            text-align: center;
            margin-bottom: 20px;
            color: #000000;
            text-transform: uppercase;
        }
        .m-desc {
            font-size: 14px;
            font-weight: 400;
            line-height: 20px;
            text-align: center;
            color: #545454;
            text-transform: capitalize;
            max-width: 70%;
            margin: 0 auto;
        }
        .product-list {
            margin: 16px 0;
        }
        .product-list .product-item {
            display: flex;
            justify-content: space-between;
            padding: 16px 0;
            border-bottom: 1px solid #919191;
        }
        .product-list .product-item:last-child {
            border: 0;
            padding-bottom: 0;
        }
        .lhs {
            width: 80%;
        }
        .rhs {
            width: 20%;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            align-items: flex-end;
        }
        .product-item .p-name {
            font-size: 16px;
            font-weight: 400;
            line-height: 24px;
            color: #000000;
            margin-bottom: 6px;
        }
        .product-item .p-desc {
            font-size: 10px;
            font-weight: 400;
            line-height: 13px;
            color: #545454;
            margin-bottom: 6px;
        }
        .product-item .p-quality {
            font-size: 16px;
            font-weight: 400;
            line-height: 24px;
            color: #000000;
        }
        .product-item .delete-icon {
            background: transparent;
            outline: none;
            border: 0;
        }
        .product-item .p-amt {
            font-size: 22px;
            font-style: italic;
            font-weight: 300;
            line-height: 24px;
            color: #000000;
        }
        .product-item .p-total {
            font-size: 20px;
            font-weight: 400;
            line-height: 24px;
            color: #000000;
        }
        .typ-bottom-padding-zero {
            padding-bottom: 0;
        }
        .disabled {
            pointer-events: none;
            cursor: not-allowed;
            opacity: 0.7;
        }
        @media only screen and (max-width: 480px) {
            .catalog-card .offer-band {
                padding: 7px;
                font-size: 10px;
                line-height: 10px;
                width: 96%;
            }
            .catalog-card .c-title {
                font-size: 16px;
                line-height: 18px;
            }
            .catalog-card .c-amt {
                font-size: 18px;
                line-height: 20px;
            }
            .catalog-card .c-desc {
                margin-bottom: 7px;
            }
            .catalog-card .c-wrap {
                flex-wrap: wrap;
            }
            .catalog-card .btn-wrap,
            .catalog-card .c-desc {
                width: 100%;
            }
            .form-item {
                width: 100%;
            }
            .lhs,
            .rhs {
                width: 50%;
            }
            .product-item .p-total,
            .product-item .p-amt {
                font-size: 18px;
                line-height: 20px;
            }
        }
    </style>
</head>
<body>
    <div class="main">
        <div id="ProductCatalogform" on="tap:AMP.setState({productCatalog01: {fuuid: 01 }})" role="tab" tabindex="1"
            class="amp-html-block widget-container">
            <form class="form-container" method="post" id="productCatalog01Form" enctype="multipart/form-data"
                action-xhr="https://example.com" custom-validation-reporting="show-all-on-submit" on="submit:AMP.setState({
                    productCatalog01: {
                        currentStep: productCatalog01.currentStep == 2 : productCatalog01.currentStep + 1, 
                        submitting: true,
                        editAddress: false
                    }
                });
                submit-success:AMP.setState({
                    productCatalog01: {
                        submitting: false, 
                        paymentUrl: productCatalog01.paymentUrl || event.response.url
                    }
                });">
                <input hidden id="fuuid" name="fuuid" [value]="01" />
                <input hidden name="catalogType" value="STATIC" />
                <input hidden name="discountCouponCode" value="" />
                <amp-state id="productCatalog01">
                    <script type="application/json">
                        {
                            "first_name": "",
                            "last_name": "",
                            "address": "",
                            "landmark": "",
                            "city": "",
                            "country": "",
                            "pincode": "",
                            "phoneNumber": "",
                            "email": "",
                            "payment_mode": "",
                            "isFirstNameValid": false,
                            "isLastNameValid": false,
                            "isPhoneNumberValid": false,
                            "isEmailValid": false,
                            "isPincodeValid": false,
                            "isCityValid": false,
                            "editAddress": false,        
                            "paymentUrl": "",
                            "product1": {
                                "id": 1,
                                "qty": 0,
                                "title": "Mystic Elixir",
                                "price": 1500,
                                "selectedVariantId": 0,
                                "addedToCart": false,
                                "variantId": 101,
                                "variantTitle": "Default Title",
                                "comparePrice": "null",
                                "variants": {
                                    "101": {
                                        "id": 101,
                                        "price": 1500,
                                        "title": "Default Title",
                                        "comparePrice": "null"
                                    }
                                }
                            },
                            "product2": {
                                "id": 2,
                                "qty": 0,
                                "title": "Opulent Essence",
                                "price": 1500,
                                "selectedVariantId": 0,
                                "addedToCart": false,
                                "variantId": 102,
                                "variantTitle": "Default Title",
                                "comparePrice": "null",
                                "variants": {
                                    "102": {
                                        "id": 102,
                                        "price": 1500,
                                        "title": "Default Title",
                                        "comparePrice": "null"
                                    }
                                }
                            },
                            "product3": {
                                "id": 3,
                                "qty": 0,
                                "title": "Product Name 3",
                                "price": 1500,
                                "selectedVariantId": 0,
                                "addedToCart": false,
                                "variantId": 103,
                                "variantTitle": "Default Title",
                                "comparePrice": "null",
                                "variants": {
                                    "103": {
                                        "id": 103,
                                        "price": 1500,
                                        "title": "Default Title",
                                        "comparePrice": "null"
                                    }
                                }
                            },
                            "product4": {
                                "id": 4,
                                "qty": 0,
                                "title": "Product Name 4",
                                "price": 1500,
                                "selectedVariantId": 0,
                                "addedToCart": false,
                                "variantId": 104,
                                "variantTitle": "Default Title",
                                "comparePrice": "null",
                                "variants": {
                                    "104": {
                                        "id": 104,
                                        "price": 1500,
                                        "title": "Default Title",
                                        "comparePrice": "null"
                                    }
                                }
                            },
                            "product5": {
                                "id": 5,
                                "qty": 0,
                                "title": "Product Name 5",
                                "price": 1500,
                                "selectedVariantId": 0,
                                "addedToCart": false,
                                "variantId": 105,
                                "variantTitle": "Default Title",
                                "comparePrice": "null",
                                "variants": {
                                    "105": {
                                        "id": 105,
                                        "price": 1500,
                                        "title": "Default Title",
                                        "comparePrice": "null"
                                    }
                                }
                            },
                            "currentStep": 1
                        }
                    </script>
                </amp-state>
                <!-- <h1 [text]="productCatalog01.currentStep"></h1> -->
                <header class="cp-header typ-shadow" [hidden]="productCatalog01.currentStep == 3">
                    <div class="logo-wrap">
                        <div class="img-wrap">
                            <!-- Change Logo -->
                            <amp-img layout="responsive"
                                src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/logo.png"
                                alt="Logo" width="127" height="58" />
                            <!-- Change Logo -->
                        </div>
                        <ul class="nav-list">
                            <li class="nav-item">
                                <div class="cart-icon checkout-button"
                                    [class]="productCatalog01.currentStep == 2 ? 'cart-icon active' : 'cart-icon'"
                                    on="tap:AMP.setState({
                                        productCatalog01 : {
                                        currentStep:  2 ,
                                        editAddress: true,
                                        }
                                    })"
                                    >
                                    <amp-img layout="fixed"
                                        src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/icon-cart.png"
                                        alt="cart-icon" class="icon" width="22" height="22" />
                                    <span class="dot"></span>
                                </div>
                            </li>
                            <li class="nav-item">
                                <span class="icon-wrap">
                                    <amp-img class="call-icon" layout="responsive"
                                        src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/call-icon.png"
                                        alt="call icon" width="20" height="20" />
                                </span>
                                <p class="icon-text">9878725637</p>
                            </li>
                        </ul>
                    </div>
                </header>
                <div class="step1" [hidden]="productCatalog01.currentStep != 1">
                    <div class="bs-sec typ-look">
                        <div class="sec-head">
                            <h3 class="sec-title">PRODUCTS</h3>
                        </div>
                        <div class="sec-body">
                            <div class="container">
                                <div class="catalog-card">
                                    <div class="catalog-img">
                                        <h3 class="offer-band">Get 20% off for your first purchase.</h3>
                                        <!-- Change Product Image -->
                                        <amp-img
                                            src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/look-1.png"
                                            layout="responsive" alt="look" width="506" height="316" />
                                        <!-- Change Product Image -->
                                        <span class="cart-wrap">
                                            <span class="count" hidden [hidden]="productCatalog01.product1.qty <= 0"
                                                [text]="productCatalog01.product1.qty"></span>
                                            <amp-img layout="fixed"
                                                src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/icon-cart.png"
                                                alt="cart-icon" class="icon" width="27" height="27" />
                                        </span>
                                    </div>
                                    <div class="catalog-body">
                                        <div class="c-wrap">
                                            <h3 class="c-title">Mystic Elixir</h3>
                                            <p class="c-amt">
                                                <span class="rupee-sign">₹</span>
                                                <span class="amount"
                                                    [text]="(productCatalog01.product1.qty*productCatalog01.product1.price).toFixed(2)">1500.00</span>
                                            </p>
                                            <input hidden name='101'
                                                [value]="productCatalog01.product1.variantId == 101 ? productCatalog01.product1.qty:1" />
                                        </div>
                                        <div class="c-wrap">
                                            <p class="c-desc">is simply dummy text of the new age fashion industry.</p>
                                            <div class="btn-wrap">
                                                <div class="product-count">
                                                    <div class="product-count-sign" tabindex="1" role on="tap:AMP.setState({
                                                        productCatalog01 : {
                                                            product1: {
                                                                qty: productCatalog01.product1.qty > 0 ? productCatalog01.product1.qty - 1 : 0
                                                            }
                                                        }
                                                    })">
                                                        <amp-img layout="fixed"
                                                            src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/minsu-icon.png"
                                                            alt="minus-icon" class="icon" width="13" height="13" />
                                                    </div>
                                                    <div class="product-count-value"
                                                        [text]="productCatalog01.product1.qty">0</div>
                                                    <div class="product-count-sign" tabindex="1" on="tap:AMP.setState({
                                                            productCatalog01 :{
                                                                product1: {
                                                                    qty: productCatalog01.product1.qty < 5 ? productCatalog01.product1.qty + 1 : 5
                                                                }
                                                            }
                                                        })">
                                                        <amp-img layout="fixed"
                                                            src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/plus-icon.png"
                                                            alt="plus-icon" class="icon" width="13" height="13" />
                                                    </div>
                                                </div>
                                                <!-- Change CTA -->
                                                <button type="button" class="catalog-cta"
                                                    on="tap:AMP.setState({productCatalog01 :{product1: {addedToCart:true}}})">
                                                    ADD TO CART
                                                </button>
                                                          <!-- Change CTA -->
                                            </div>
                                        </div>
                                    </div>
                                </div>
                                <!-- Second product card -->
                                <div class="catalog-card">
                                    <div class="catalog-img">
                                        <h3 class="offer-band">Get 20% off for your first purchase.</h3>
                                        <amp-img
                                            src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/look-2.png"
                                            layout="responsive" alt="look" width="506" height="316" />
                                        <span class="cart-wrap">
                                            <span class="count" hidden [hidden]="productCatalog01.product2.qty <= 0"
                                                [text]="productCatalog01.product2.qty"></span>
                                            <amp-img layout="fixed"
                                                src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/icon-cart.png"
                                                alt="cart-icon" class="icon" width="27" height="27" />
                                        </span>
                                    </div>
                                    <div class="catalog-body">
                                        <div class="c-wrap">
                                            <h3 class="c-title">Opulent Essence</h3>
                                            <p class="c-amt">
                                                <span class="rupee-sign">₹</span>
                                                <span class="amount"
                                                    [text]="(productCatalog01.product2.qty*productCatalog01.product2.price).toFixed(2)">1500</span>
                                            </p>
                                            <input hidden name='102'
                                                [value]="productCatalog01.product2.variantId == 102 ? productCatalog01.product2.qty:1" />
                                        </div>
                                        <div class="c-wrap">
                                            <p class="c-desc">is simply dummy text of the new age fashion industry.</p>
                                            <div class="btn-wrap">
                                                <div class="product-count">
                                                    <div class="product-count-sign" tabindex="1" role on="tap:AMP.setState({
                                                            productCatalog01 : {
                                                                product2: {
                                                                    qty: productCatalog01.product2.qty > 0 ? productCatalog01.product2.qty - 1 : 0
                                                                }
                                                            }
                                                        })">
                                                        <amp-img layout="fixed"
                                                            src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/minsu-icon.png"
                                                            alt="minus-icon" class="icon" width="13" height="13" />
                                                    </div>
                                                    <div class="product-count-value"
                                                        [text]="productCatalog01.product2.qty">0</div>
                                                    <div class="product-count-sign" tabindex="1" on="tap:AMP.setState({
                                                            productCatalog01 :{
                                                                product2: {
                                                                    qty: productCatalog01.product2.qty < 5 ? productCatalog01.product2.qty + 1 : 5
                                                                }
                                                            }
                                                        })">
                                                        <amp-img layout="fixed"
                                                            src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/plus-icon.png"
                                                            alt="plus-icon" class="icon" width="13" height="13" />
                                                    </div>
                                                </div>
                                                <button type="button" class="catalog-cta"
                                                    on="tap:AMP.setState({productCatalog01 :{product2: {addedToCart:true}}})">
                                                    ADD TO CART
                                                </button>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                                <input hidden name="amount" [value]='(
                                    (productCatalog01.product1.qty * productCatalog01.product1.price) +
                                    (productCatalog01.product2.qty * productCatalog01.product2.price) +
                                    (productCatalog01.product3.qty * productCatalog01.product3.price) +
                                    (productCatalog01.product4.qty * productCatalog01.product4.price) +
                                    (productCatalog01.product5.qty * productCatalog01.product5.price)
                                ).toFixed(2)' />
                            </div>
                        </div>
                    </div>
                    <!-- product section -->
                    <div class="bs-sec typ-product">
                        <div class="sec-head">
                            <h3 class="sec-title">Product Suggestions</h3>
                        </div>
                        <div class="sec-body">
                            <div class="container">
                                <ul class="lyt-grid">
                                    <li class="grid-item">
                                        <div class="product-card">
                                            <div class="img-wrap">
                                                <!-- Change image src as per your requirements -->
                                                <amp-img layout="responsive"
                                                    src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/product-3.png"
                                                    alt="product" width="150" height="177" />
                                            </div>
                                            <button type="button" class="p-cart-icon"
                                                on="tap:AMP.setState({productCatalog01 :{product3: {addedToCart:true, qty:1}}})">
                                                <amp-img layout="fixed"
                                                    src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/icon-cart.png"
                                                    alt="cart-icon" class="icon" width="13" height="13"></amp-img>
                                            </button>
                                            <div class="product-info">
                                                <div class="p-wrap">
                                                    <h3 class="p-title">Product name</h3>
                                                    <p class="p-amt"><span class="rupee-sign">₹</span>1500</p>
                                                </div>
                                                <p class="p-desc">Is simply dummy text of the new age fashion industry.
                                                </p>
                                            </div>
                                        </div>
                                    </li>
                                    <li class="grid-item">
                                        <div class="product-card">
                                            <div class="img-wrap">
                                                <!-- Change image src as per your requirements -->
                                                <amp-img layout="responsive"
                                                    src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/product-2.png"
                                                    alt="product" width="150" height="177" />
                                            </div>
                                            <button type="button" class="p-cart-icon"
                                                on="tap:AMP.setState({productCatalog01 :{product4: {addedToCart:true, qty:1}}})">
                                                <amp-img layout="fixed"
                                                    src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/icon-cart.png"
                                                    alt="cart-icon" class="icon" width="13" height="13" />
                                            </button>
                                            <div class="product-info">
                                                <div class="p-wrap">
                                                    <h3 class="p-title">Product name</h3>
                                                    <p class="p-amt"><span class="rupee-sign">₹</span>1500</p>
                                                </div>
                                                <p class="p-desc">Is simply dummy text of the new age fashion industry.
                                                </p>
                                            </div>
                                        </div>
                                    </li>
                                    <li class="grid-item">
                                        <div class="product-card">
                                            <div class="img-wrap">
                                                <!-- Change image src as per your requirements -->
                                                <amp-img layout="responsive"
                                                    src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/product-1.png"
                                                    alt="product" width="150" height="177" />
                                            </div>
                                            <button type="button" class="p-cart-icon"
                                                on="tap:AMP.setState({productCatalog01 :{product5: {addedToCart:true, qty:1}}})">
                                                <amp-img layout="fixed"
                                                    src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/icon-cart.png"
                                                    alt="cart-icon" class="icon" width="13" height="13" />
                                            </button>
                                            <div class="product-info">
                                                <div class="p-wrap">
                                                    <h3 class="p-title">Product name</h3>
                                                    <p class="p-amt"><span class="rupee-sign">₹</span>1500</p>
                                                </div>
                                                <p class="p-desc">Is simply dummy text of the new age fashion industry.
                                                </p>
                                            </div>
                                        </div>
                                    </li>
                                </ul>
                                <div class="btn-wrap">
                                    <a href="https://google.com" class="shop-cta">Shop now
                                        <amp-img layout="fixed"
                                            src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/arrow.png"
                                            alt="arrow" width="17" height="10"
                                            style="margin-left: 10px; max-width: 17px" />
                                    </a>
                                </div>
                            </div>
                        </div>
                    </div>
                    <!-- product section -->
                    <!-- footer section -->
                    <footer class="cp-footer">
                        <div class="container">
                            <ul class="media-logo-list">
                                <li class="logo-item">
                                    <a href="https://www.google.co.in/" class="logo-link">
                                        <amp-img layout="responsive"
                                            src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/logo-insta.png"
                                            alt="instagram" class="media-logo" width="20" height="20"></amp-img>
                                    </a>
                                </li>
                                <li class="logo-item">
                                    <a href="https://www.google.co.in/" class="logo-link">
                                        <amp-img layout="responsive"
                                            src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/logo-facebook.png"
                                            alt="facebook" class="media-logo" width="20" height="20"></amp-img>
                                    </a>
                                </li>
                                <li class="logo-item">
                                    <a href="https://www.google.co.in/" class="logo-link">
                                        <amp-img layout="responsive"
                                            src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/logo-x.png"
                                            alt="x" class="media-logo" width="20" height="20"></amp-img>
                                    </a>
                                </li>
                            </ul>
                            <p class="f-desc">is simply dummy text of the printing and typesetting industry. Lorem Ipsum
                                has
                                been the industry's standard dummy </p>
                                <p class="f-desc" style="margin-top: 20px;">To stop receiving these emails, <a href="https://www.google.com" style="color:#ffff;font-weight:bold;text-decoration:none;">unsubscribe here</a></p>
                        </div>
                    </footer>
                    <!-- footer section -->
                </div>
                <div class="step2" hidden [hidden]="productCatalog01.currentStep != 2">
                    <div class="container">
                        <div class="bs-sec typ-bottom-padding-zero" [hidden]="
                            (productCatalog01.product1.qty <= 0 &&
                            productCatalog01.product2.qty <= 0 &&
                            productCatalog01.product3.qty <= 0 &&
                            productCatalog01.product4.qty <= 0 &&
                            productCatalog01.product5.qty <= 0)
                                    ">
                            <div class="sec-head">
                                <h3 class="sec-title typ-2">PRODUCTS</h3>
                            </div>
                            <div class="sec-body">
                                <ul class="product-list">
                                    <li class="product-item" [hidden]="productCatalog01.product1.qty == 0">
                                        <div class="lhs">
                                            <h3 class="p-name" [text]="productCatalog01.product1.title">Mystic Elixir
                                            </h3>
                                            <p class="p-desc"> is simply dummy text of the new age fashion industry.</p>
                                            <p class="p-quality">Qty : <span
                                                    [text]="productCatalog01.product1.qty"></span></p>
                                        </div>
                                        <div class="rhs">
                                            <button class="delete-icon" on="tap:AMP.setState({
                                                    productCatalog01 :{
                                                        product1: {addedToCart:false, qty:0}
                                                    }
                                                })">
                                                <amp-img
                                                    src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/delete-icon.png"
                                                    width="24" height="24" layout="fixed" alt="delete-icon">
                                                </amp-img>
                                            </button>
                                            <p class="p-amt">₹ <span
                                                    [text]="(productCatalog01.product1.qty*productCatalog01.product1.price).toFixed(2)"></span>
                                            </p>
                                        </div>
                                    </li>
                                    <li class="product-item" [hidden]="productCatalog01.product2.qty == 0">
                                        <div class="lhs">
                                            <h3 class="p-name" [text]="productCatalog01.product2.title">Mystic Elixir
                                            </h3>
                                            <p class="p-desc">is simply dummy text of the new age fashion industry.</p>
                                            <p class="p-quality">Qty : <span
                                                    [text]="productCatalog01.product2.qty"></span></p>
                                        </div>
                                        <div class="rhs">
                                            <button class="delete-icon" on="tap:AMP.setState({
                                                    productCatalog01 :{
                                                        product2: {addedToCart:false, qty:0}
                                                    }
                                                })">
                                                <amp-img
                                                    src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/delete-icon.png"
                                                    width="24" height="24" layout="fixed" alt="delete-icon">
                                                </amp-img>
                                            </button>
                                            <p class="p-amt">₹ <span
                                                    [text]="(productCatalog01.product2.qty*productCatalog01.product2.price).toFixed(2)"></span>
                                            </p>
                                        </div>
                                    </li>
                                    <li class="product-item" [hidden]="productCatalog01.product3.qty == 0">
                                        <div class="lhs">
                                            <h3 class="p-name" [text]="productCatalog01.product3.title">Product Name
                                            </h3>
                                            <p class="p-desc">is simply dummy text of the new age fashion industry.</p>
                                            <p class="p-quality">Qty : <span
                                                    [text]="productCatalog01.product3.qty"></span></p>
                                        </div>
                                        <div class="rhs">
                                            <button class="delete-icon" on="tap:AMP.setState({
                                                    productCatalog01 :{
                                                        product3: {addedToCart:false, qty:0}
                                                    }
                                                })">
                                                <amp-img
                                                    src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/delete-icon.png"
                                                    width="24" height="24" layout="fixed" alt="delete-icon">
                                                </amp-img>
                                            </button>
                                            <p class="p-amt">₹ <span
                                                    [text]="(productCatalog01.product3.qty*productCatalog01.product3.price).toFixed(2)"></span>
                                            </p>
                                        </div>
                                    </li>
                                    <li class="product-item" [hidden]="productCatalog01.product4.qty == 0">
                                        <div class="lhs">
                                            <h3 class="p-name" [text]="productCatalog01.product4.title">Product Name
                                            </h3>
                                            <p class="p-desc">is simply dummy text of the new age fashion industry.</p>
                                            <p class="p-quality">Qty : <span
                                                    [text]="productCatalog01.product4.qty"></span></p>
                                        </div>
                                        <div class="rhs">
                                            <button class="delete-icon" on="tap:AMP.setState({
                                                    productCatalog01 :{
                                                        product4: {addedToCart:false, qty:0}
                                                    }
                                                })">
                                                <amp-img
                                                    src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/delete-icon.png"
                                                    width="24" height="24" layout="fixed" alt="delete-icon">
                                                </amp-img>
                                            </button>
                                            <p class="p-amt">₹ <span
                                                    [text]="(productCatalog01.product4.qty*productCatalog01.product4.price).toFixed(2)"></span>
                                            </p>
                                        </div>
                                    </li>
                                    <li class="product-item" [hidden]="productCatalog01.product5.qty == 0">
                                        <div class="lhs">
                                            <h3 class="p-name" [text]="productCatalog01.product5.title">Product Name
                                            </h3>
                                            <p class="p-desc">is simply dummy text of the new age fashion industry.</p>
                                            <p class="p-quality">Qty : <span
                                                    [text]="productCatalog01.product5.qty"></span></p>
                                        </div>
                                        <div class="rhs">
                                            <button class="delete-icon" on="tap:AMP.setState({
                                                    productCatalog01 :{
                                                        product5: {addedToCart:false, qty:0}
                                                    }
                                                })">
                                                <amp-img
                                                    src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/delete-icon.png"
                                                    width="24" height="24" layout="fixed" alt="delete-icon">
                                                </amp-img>
                                            </button>
                                            <p class="p-amt">₹ <span
                                                    [text]="(productCatalog01.product5.qty*productCatalog01.product5.price).toFixed(2)"></span>
                                            </p>
                                        </div>
                                    </li>
                                    <li class="product-item typ-final">
                                        <div class="lhs">
                                            <h3 class="p-total">Amount Total</h3>
                                        </div>
                                        <div class="rhs">
                                            <p class="p-amt p-total-amt">₹
                                                <span [text]="(
                                                    (
                                                        (productCatalog01.product1.qty * productCatalog01.product1.price) +
                                                        (productCatalog01.product2.qty * productCatalog01.product2.price) +
                                                        (productCatalog01.product3.qty * productCatalog01.product3.price) +
                                                        (productCatalog01.product4.qty * productCatalog01.product4.price) +
                                                        (productCatalog01.product5.qty * productCatalog01.product5.price)
                                                    ) * (100 - 0) / 100
                                                ).toFixed(2) + ' '">0</span>
                                            </p>
                                        </div>
                                    </li>
                                </ul>
                            </div>
                        </div>
                        <div class="bs-sec">
                            <div class="sec-head ">
                                <h3 class="sec-title typ-2">ADD DETAILS</h3>
                            </div>
                            <div class="sec-body">
                                <ul class="form-list">
                                    <!-- First Name -->
                                    <li class="form-item">
                                        <input id="productCatalog01-first_name" required on="
                                            change:AMP.setState({
                                                productCatalog01: { first_name: event.value }
                                            });
                                            tap:AMP.setState({
                                                formValidation: { first_name_invalid: event.target.validity.valueMissing }
                                            })
                                        " type="text" name="first_name" class="input" placeholder="First name" [value]="productCatalog01.first_name" [aria-invalid]="formValidation.first_name_invalid" aria-describedby="productCatalog01.first_name">
                                        <div class="error-msg" visible-when-invalid="valueMissing" validation-for="productCatalog01-first_name" id="productCatalog01.first_name">
                                            First name is required.
                                        </div>
                                    </li>
                                    <!-- Last Name -->
                                    <li class="form-item">
                                        <input id="productCatalog01-last_name" required on="
                                            change:AMP.setState({
                                                productCatalog01: { last_name: event.value }
                                            });
                                            tap:AMP.setState({
                                                formValidation: { last_name_invalid: event.target.validity.valueMissing }
                                            })
                                        " type="text" name="last_name" class="input" placeholder="Last name" [value]="productCatalog01.last_name" [aria-invalid]="formValidation.last_name_invalid" aria-describedby="formValidation.last_name_invalid">
                                        <div class="error-msg" visible-when-invalid="valueMissing" validation-for="productCatalog01-last_name" id="formValidation.last_name_invalid">
                                            Last name is required.
                                        </div>
                                    </li>
                                    <!-- Phone Number -->
                                    <li class="form-item">
                                        <input id="productCatalog01-phoneNumber" required [pattern]="productCatalog01.currentStep==2 ? '\\d{10}' : '*'" on="
                                            change:AMP.setState({
                                                productCatalog01: { phoneNumber: event.value }
                                            });
                                            tap:AMP.setState({
                                                formValidation: { phoneNumber_invalid: event.target.validity.valueMissing || event.target.validity.patternMismatch }
                                            })
                                        " maxlength="10" type="text" name="phoneNumber" class="input" placeholder="Phone Number" [value]="productCatalog01.phoneNumber" pattern="\d{10}" [aria-invalid]="formValidation.phoneNumber_invalid" aria-describedby="productCatalog01.phoneNumber">
                                        <div class="error-msg" visible-when-invalid="valueMissing" validation-for="productCatalog01-phoneNumber" id="productCatalog01.phoneNumber">
                                            Phone number is required.
                                        </div>
                                        <div class="error-msg" visible-when-invalid="patternMismatch" validation-for="productCatalog01-phoneNumber">
                                            Please enter a valid phone number.
                                        </div>
                                    </li>
                                    <!-- Email -->
                                    <li class="form-item">
                                        <input id="productCatalog01-email" required type="email" on="
                                            change:AMP.setState({
                                                productCatalog01: { email: event.value }
                                            });
                                            tap:AMP.setState({
                                                formValidation: { email_invalid: event.target.validity.valueMissing || event.target.validity.typeMismatch }
                                            })
                                        " name="email" class="input" placeholder="E-mail" [value]="productCatalog01.email" [aria-invalid]="formValidation.email_invalid" aria-describedby="productCatalog01.email">
                                        <div class="error-msg" visible-when-invalid="valueMissing" validation-for="productCatalog01-email" id="productCatalog01.email">
                                            Email is required.
                                        </div>
                                        <div class="error-msg" visible-when-invalid="patternMismatch" validation-for="productCatalog01-email">
                                            Please enter a valid Email.
                                        </div>
                                    </li>
                                    <!-- Address -->
                                    <li class="form-item typ-full">
                                        <input id="productCatalog01-address" required on="
                                            change:AMP.setState({
                                                productCatalog01: { address: event.value }
                                            });
                                            tap:AMP.setState({
                                                formValidation: { address_invalid: event.target.validity.valueMissing }
                                            })
                                        " name="address" class="input" placeholder="Address" [value]="productCatalog01.address" [aria-invalid]="formValidation.address_invalid" aria-describedby="productCatalog01.address">
                                        <div class="error-msg" visible-when-invalid="valueMissing" validation-for="productCatalog01-address" id="productCatalog01.address">
                                            Address is required.
                                        </div>
                                    </li>
                                    <!-- Landmark -->
                                    <li class="form-item">
                                        <input id="productCatalog01-landmark" required on="
                                            change:AMP.setState({
                                                productCatalog01: { landmark: event.value }
                                            });
                                            tap:AMP.setState({
                                                formValidation: { landmark_invalid: event.target.validity.valueMissing }
                                            })
                                        " name="landmark" class="input" placeholder="Landmark" [value]="productCatalog01.landmark" [aria-invalid]="formValidation.landmark_invalid" aria-describedby="productCatalog01.landmark">
                                        <div class="error-msg" visible-when-invalid="valueMissing" validation-for="productCatalog01-landmark" id="productCatalog01.landmark">
                                            Landmark is required.
                                        </div>
                                    </li>
                                    <!-- Pincode -->
                                    <li class="form-item">
                                        <input id="productCatalog01-pincode" required on="
                                            change:AMP.setState({
                                                productCatalog01: { pincode: event.value }
                                            });
                                            tap:AMP.setState({
                                                formValidation: { pincode_invalid: event.target.validity.valueMissing }
                                            })
                                        " name="pincode" class="input" placeholder="Pincode" [value]="productCatalog01.pincode" maxlength="6" type="number" [aria-invalid]="formValidation.pincode_invalid" aria-describedby="productCatalog01.pincode">
                                        <div class="error-msg" visible-when-invalid="valueMissing" validation-for="productCatalog01-pincode" id="productCatalog01.pincode">
                                            Pincode is required.
                                        </div>
                                    </li>
                                    <!-- City -->
                                    <li class="form-item">
                                        <input id="productCatalog01-city" required on="
                                            change:AMP.setState({
                                                productCatalog01: { city: event.value }
                                            });
                                            tap:AMP.setState({
                                                formValidation: { city_invalid: event.target.validity.valueMissing }
                                            })
                                        " type="text" name="city" class="input" placeholder="City" [value]="productCatalog01.city" [aria-invalid]="formValidation.city_invalid" aria-describedby="productCatalog01.city">
                                        <div class="error-msg" visible-when-invalid="valueMissing" validation-for="productCatalog01-city" id="productCatalog01.city">
                                            City is required.
                                        </div>
                                    </li>
                                    <!-- State -->
                                    <li class="form-item">
                                        <input id="productCatalog01-state" required on="
                                            change:AMP.setState({
                                                productCatalog01: { state: event.value }
                                            });
                                            tap:AMP.setState({
                                                formValidation: { state_invalid: event.target.validity.valueMissing }
                                            })
                                        " type="text" name="state" class="input" placeholder="State" [value]="productCatalog01.state" [aria-invalid]="formValidation.state_invalid" aria-describedby="productCatalog01.state">
                                        <div class="error-msg" visible-when-invalid="valueMissing" validation-for="productCatalog01-state" id="productCatalog01.state">
                                            State is required.
                                        </div>
                                    </li>
                                    <!-- Payment Mode -->
                                    <li class="form-item typ-full mt-32">
                                        <label for="cod" class="field-wrap">
                                            <input type="radio" checked="checked" id="cod" name="payment" required on="
                                                change:AMP.setState({
                                                    productCatalog01: { payment_mode: 'cod' }
                                                })
                                            " [value]="productCatalog01.payment_mode" class="user-valid valid" value="">
                                            <span class="checkmark"></span>
                                            Cash on Delivery
                                        </label>
                                        <label class="field-wrap" for="online">
                                            <input type="radio" id="online" name="payment" on="
                                                change:AMP.setState({
                                                    productCatalog01: { payment_mode: 'online' }
                                                })
                                            " [value]="productCatalog01.payment_mode" class="user-valid valid" value="">
                                            <span class="checkmark"></span>
                                            Online
                                        </label>
                                    </li>
                                    <!-- Submit Button -->
                                    <li class="form-item typ-full">
                                        <button class="form-btn" on="
                                            tap:AMP.setState({
                                                formValidation: {
                                                    first_name_invalid: !productCatalog01.first_name,
                                                    last_name_invalid: !productCatalog01.last_name,
                                                    phoneNumber_invalid: !productCatalog01.phoneNumber || !/^\d{10}$/.test(productCatalog01.phoneNumber),
                                                    email_invalid: !productCatalog01.email,
                                                    address_invalid: !productCatalog01.address,
                                                    landmark_invalid: !productCatalog01.landmark,
                                                    pincode_invalid: !productCatalog01.pincode,
                                                    city_invalid: !productCatalog01.city,
                                                    state_invalid: !productCatalog01.state,
                                                },
                                                productCatalog01: { currentStep: 3 }
                                            })
                                        ">
                                            Next
                                        </button>
                                    </li>
                                </ul>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="step3" hidden [hidden]="productCatalog01.currentStep != 3">
                    <div class="modal-overlay">
                        <div class="modal">
                            <div class="modal-content">
                                <div class="modal-head">
                                    <span class="close">x</span>
                                </div>
                                <div class="modal-body">
                                    <h3 class="m-title">THANKS for shopping</h3>
                                    <p class="m-desc">
                                        is simply dummy text of the printing and typesetting industry. Lorem Ipsum has
                                        been the
                                        industry's standard dummy text ever since the 1500s
                                    </p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="step4" hidden submit-error>
                    <div class="modal-overlay">
                        <div class="modal hidden">
                            <div class="modal-content">
                                <div class="modal-head">
                                    <span class="close">x</span>
                                </div>
                                <div class="modal-body">
                                    <h3 class="m-title">Error</h3>
                                    <p class="m-desc">
                                        is simply dummy text of the printing and typesetting industry. Lorem Ipsum has
                                        been the
                                        industry's standard dummy text ever since the 1500s
                                    </p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </form>
        </div>
    </div>
</body>
</html>
```

</details>

## Scratch Card

This AMP template delivers a gamified experience within the email itself. It allows users to interact with a digital scratch card to reveal a hidden offer, discount, or reward, creating a sense of anticipation and delight. This interactive approach helps increase user engagement, click-through rates, and overall campaign excitement.

<details>

<summary>Expand to know more about the template.</summary>

### Use Case Examples

- Launch surprise reward campaigns to boost conversions.
- Drive festive or seasonal promotions with a gamified touch.
- Encourage user engagement with loyalty program perks.
- Re-engage inactive users with a “Scratch To Unlock” coupon or deal.

### Template Customization Options

- Replace the Logo
- Replace Background
- Update Banner/Product Images
- Update Call-To-Actions (CTAs)
- Update Links in the Header/Footer

### Template Code

```html
<!doctype html>
<html ⚡4email data-css-strict>
<head>
	<meta charset="utf-8">
	<script async src="https://cdn.ampproject.org/v0.js"></script>
	<script async custom-element="amp-form" src="https://cdn.ampproject.org/v0/amp-form-0.1.js"></script>
	<script async custom-element="amp-bind" src="https://cdn.ampproject.org/v0/amp-bind-0.1.js"></script>
	<script async src="https://cdn.ampproject.org/v0.js"></script>
	<style amp4email-boilerplate>
		body {
			visibility: hidden
		}
	</style>
	<style amp-custom>
		* {
			margin: 0;
			padding: 0;
		}
		body {
			font-family: "Helvetica", arial, sans-serif;
			font-weight: 400;
		}
		img {
			width: 100%;
			height: auto;
			object-fit: contain;
		}
		.main {
			max-width: 600px;
			margin: 0 auto;
			background: url(https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Scratch%20Card/bg.png);
			background-repeat: no-repeat;
			background-position: center;
			padding: 40px 40px 60px;
		}
		.hide {
			display: none;
		}
		.show {
			display: block;
		}
		.scratch-img-wrap {
			background: transparent;
			border: 0;
			outline: none;
			cursor: pointer;
		}
		@media screen and (max-width: 600px) {
			.main {
				padding: 20px;
			}
			.heading {
				font-size: 30px;
				line-height: 40px;
			}
			.coupon {
				font-size: 24px;
				line-height: 32px;
			}
			.scratch-img-wrap {
				width: 100%;
				height: auto;
			}
			.scratch-code {
				padding: 15px 10px;
			}
		}
		.promo {
			margin: 0 auto;
			position: relative;
			transform-style: preserve-3d;
			border-radius: 8px;
			border: 2px solid #d1d1d1;
			overflow: hidden;
			height: 120px;
			width: 450px;
			background-color: transparent;
		}
		.promo .scratch {
			position: absolute;
			top: 0;
			right: 0;
			bottom: 0;
			left: 0;
			display: flex;
			flex-wrap: wrap;
			overflow: hidden;
			cursor: pointer
		}
		.promo .scratch u {
			display: block;
			width: 10%;
			height: 10%;
			background: rgb(2, 0, 36);
			background: #e3e3e3;
			/* Golden color */
			transform: rotate(0) translateY(0) scale(1.7);
			transition: transform 0s;
			transition-delay: 9999s;
			opacity: .99;
		}
		.promo.auto .scratch u:nth-of-type(1n) {
			transition-delay: 2.25s
		}
		.promo.auto .scratch u:nth-of-type(10n-11) {
			transition-delay: 0s
		}
		.promo.auto .scratch u:nth-of-type(10n-8) {
			transition-delay: .25s
		}
		.promo.auto .scratch u:nth-of-type(10n-10) {
			transition-delay: .5s
		}
		.promo.auto .scratch u:nth-of-type(12n-9) {
			transition-delay: .75s
		}
		.promo.auto .scratch u:nth-of-type(12n-12) {
			transition-delay: 1s
		}
		.promo.auto .scratch u:nth-of-type(12n-7) {
			transition-delay: 1.25s
		}
		.promo.auto .scratch u:nth-of-type(13n-13) {
			transition-delay: 1.5s
		}
		.promo.auto .scratch u:nth-of-type(13n-6) {
			transition-delay: 1.75s
		}
		.promo.auto .scratch u:nth-of-type(13n-14) {
			transition-delay: 2s
		}
		.promo .scratch u:hover,
		.promo.auto .scratch u {
			transform: scale(0);
			transition-delay: 0s
		}
		.offer {
			justify-content: center;
			text-align: center;
			margin-top: 25px;
			/* Center aligns the content */
			color: white;
			/* Sets text color to white */
			font-weight: bold;
			/* Makes "You Won!" text bold */
			font-size: 20px;
			/* Adjust size if necessary */
		}
		.coupon-code {
			margin-top: 10px;
			/* Adds some space above the coupon code */
			font-size: 24px;
			/* Adjust coupon code font size */
			font-weight: bold;
			/* Makes the coupon code bold */
			color: white;
			/* White text for the coupon code */
			background-color: rgba(0, 0, 0, 0.7);
			/* Optional: add a semi-transparent background */
			padding: 5px 10px;
			/* Add padding for better visibility */
			border-radius: 4px;
			/* Rounded corners for the coupon box */
			display: inline-block;
			/* Ensures proper alignment and box behavior */
		}
		.black-but {
			margin-top: 20px;
			padding: 10px;
		}
		/* Additional Media Queries for smaller screens */
		@media screen and (max-width: 600px) {
			.main {
				padding: 20px;
			}
			.heading {
				font-size: 30px;
				line-height: 40px;
			}
			.coupon {
				font-size: 24px;
				line-height: 32px;
			}
			.scratch-img-wrap {
				width: 100%;
				height: auto;
			}
			.scratch-code {
				padding: 15px 10px;
			}
		}
		/* More media queries for smaller screens */
		@media screen and (max-width: 400px) {
			.main {
				padding: 15px;
			}
			.heading {
				font-size: 28px;
				line-height: 35px;
			}
			.coupon {
				font-size: 22px;
				line-height: 30px;
			}
			.scratch-img-wrap {
				width: 100%;
				height: auto;
			}
			.coupon-code {
				font-size: 20px;
				padding: 4px 8px;
			}
			.offer {
				font-size: 18px;
			}
			.promo {
				width: 100%;
				height: auto;
			}
		}
		/* Media queries for very small screens */
		@media screen and (max-width: 300px) {
			.promo {
				width: 100%;
				height: auto;
			}
			.offer {
				font-size: 16px;
			}
			.coupon-code {
				font-size: 18px;
				padding: 3px 6px;
			}
		}
	</style>
</head>
<body>
	<table border="0" cellpadding="0" cellspacing="0" class="main" role="presentation" width="100%">
		<!-- header start-->
		<tbody>
			<tr>
				<td style="text-align: center; vertical-align: middle; margin-bottom: 40px;">
					<!-- Logo Image-->
					<div class="logo"
						style="background: url(https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Scratch%20Card/logobg.png);background-repeat: no-repeat; background-position: center;">
						<amp-img layout="fixed" alt="Logo"
							src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/logo.png"
							width="127" height="60" />
					</div>
					<!-- Logo Image-->
				</td>
			</tr>
			<tr>
				<td style="text-align: center;">
					<h2 class="heading"
						style="color:#ffffff; font-family: 'Poppins', Arial, sans-serif; font-size: 45px; font-weight: 700; line-height: 68px; margin-top: 20px;">
						Mid-Season Sale</h2>
				</td>
			</tr>
			<tr>
				<!-- Banner Image -->
				<td>
					<amp-img layout="responsive" alt="banner image"
						src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Scratch%20Card/offer.png"
						width="407" height="462" />
				</td>
				<!-- Banner Image -->
			</tr>
			<tr>
				<td style="text-align: center;">
					<p class="coupon"
						style="color:#ffffff; font-family: 'Poppins', Arial, sans-serif; font-size: 34px; font-weight: 600; margin-bottom: 20px;">
						Scratch to GET</p>
				</td>
			</tr>
			<!-- Footer Section -->
			<tr>
				<td style="text-align: center;">
					<div class="container" id="&#x201D;scratch-card-widget&#x201D;">
						<div class="promo" [class]="auto == true ? &apos;promo auto&apos; : &apos;promo&apos;">
							<div class="scratch">
								<u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u>
							</div>
							<div class="offer">
								You Won! 🎉
								<div class="coupon-code">CODE1234</div>
							</div>
						</div>
						<p><button class="black-but" type="button" on="tap:AMP.setState({auto: true})">Scratch at
								once</button>
						</p>
					</div>
				</td>
			</tr>
			<!-- Footer Section -->
		</tbody>
	</table>
</body>
</html>
```

</details>

## Spin the Wheel

This AMP template adds a fun, gamified interaction to your email by letting users spin a virtual wheel to unlock a discount, reward, or surprise offer — directly within the email. This interactive format helps boost engagement and click-through rates while creating a sense of excitement and urgency.

<details>

<summary>Expand to know more about the template.</summary>

### Use Case Examples

- Drive conversions during sales events or festivals with spin-to-win deals.
- Run promotional campaigns that reward users with random offers.
- Re-engage dormant users with a playful incentive.
- Launch loyalty or referral-based programs with interactive rewards.

### Template Customization Options

- Replace the Logo
- Replace Background
- Update Banner/Product Images
- Update Call-To-Actions (CTAs)
- Update Links in the Header/Footer

### Template Code

```html
<!DOCTYPE html>
<html ⚡4email data-css-strict>
<head>
  <meta charset="utf-8" />
  <script async src="https://cdn.ampproject.org/v0.js"></script>
  <script async custom-element="amp-bind" src="https://cdn.ampproject.org/v0/amp-bind-0.1.js"></script>
  <style amp4email-boilerplate>
    body {
      visibility: hidden;
    }
  </style>
  <style amp-custom>
    * {
      margin: 0;
      padding: 0;
    }
    body {
      font-family: "Helvetica", arial, sans-serif;
      font-weight: 400;
      margin: 0;
      padding: 0;
      background: #939393;
    }
    img {
      width: 100%;
      height: 100%;
      object-fit: contain;
    }
    .main {
      font-family: "Helvetica", Arial, sans-serif;
      max-width: 600px;
      margin: 0 auto;
      background: #fe592c;
    }
    @media only screen and (max-width: 400px) {
      .main {
        max-width: 95%;
      }
    }
    .header-container {
      background: transparent url(https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/spinn/header-design.png);
      background-size: contain;
      background-repeat: repeat-x;
      background-position: bottom;
      padding-bottom: 18px;
    }
    .logo-wrap {
      background-color: #ffffff;
      padding: 20px 0;
    }
    .logo-wrap .img-wrap {
      width: 100%;
      max-width: 145px;
      max-height: 74px;
      margin: 0 auto;
    }
    .container,
    .wrapper {
      position: relative;
    }
    .main-content {
      position: relative;
    }
    .common-wrap .orange-triangle {
      width: 100%;
      height: 360px;
      background: #f34626;
      position: absolute;
      bottom: 0;
      left: 0;
      transform: rotate(180deg);
    }
    .common-wrap .content-wrap {
      max-width: 85%;
      margin: 90px auto 0;
      padding-bottom: 120px;
    }
    .top-content .title {
      font-family: "Helvetica", Arial, sans-serif;
      font-size: 42px;
      font-weight: 500;
      color: #ffffff;
      line-height: 46px;
      text-align: center;
      text-transform: uppercase;
      margin-bottom: 22px;
    }
    .top-content .sub-title {
      font-family: "Helvetica", Arial, sans-serif;
      font-size: 16px;
      font-weight: 500;
      line-height: 22px;
      text-align: center;
      color: #ffffff;
      text-transform: uppercase;
      margin-bottom: 11px;
    }
    .top-content .desc {
      font-family: "Helvetica", Arial, sans-serif;
      font-size: 12px;
      font-weight: 400;
      line-height: 18px;
      text-align: center;
      text-transform: capitalize;
      color: #ffffff;
      max-width: 70%;
      margin: 0 auto 55px;
    }
    .wheel-spin-gif-box,
    .wheel-spin-box {
      max-width: 450px;
      max-height: 450px;
      position: relative;
      overflow: hidden;
      margin: 0 auto;
    }
    .ticker {
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
      right: 0;
      z-index: 2;
    }
    .btn-wrap {
      text-align: center;
      position: relative;
    }
    .spin-btn {
      margin-top: -80px;
      background: #ffffff;
      box-shadow: 0px 3.29px 3.29px 0px #00000040;
      width: 100%;
      max-width: 242px;
      height: auto;
      max-height: 52px;
      display: inline-block;
      border-radius: 50px;
      padding: 18px 20px;
      font-size: 18px;
      font-weight: 400;
      line-height: 20px;
      text-align: center;
      text-decoration: none;
      text-transform: uppercase;
      color: #ffae97;
      border: 0;
      outline: none;
      cursor: pointer;
      position: absolute;
      top: -25px;
      left: 50%;
      transform: translateX(-50%);
    }
    @media (max-width: 768px) {
      .spin-btn {
        max-width: 200px;
        font-size: 16px;
        padding: 16px 18px;
      }
    }
    @media (max-width: 480px) {
      .spin-btn {
        max-width: 150px;
        font-size: 14px;
        padding: 12px 15px;
        margin-top: -40px;
      }
    }
    @media (max-width: 320px) {
      .spin-btn {
        max-width: 120px;
        font-size: 12px;
        padding: 10px 12px;
      }
    }
    .spin-btn.typ-2 {
      color: #FE592C;
    }
    .img-wrap {
      width: 73px;
      height: 93px;
    }
    .hidden {
      display: none;
    }
    .yellow-wrap {
      max-width: 401px;
      min-height: 300px;
      margin: 0 auto 14px;
    }
    .result-content {
      font-size: 28px;
      font-weight: 400;
      line-height: 38px;
      text-align: center;
      color: #ffffff;
      text-transform: capitalize;
      position: relative;
      z-index: 1;
    }
    .cm-bold {
      font-weight: 700;
      display: block;
    }
    .footer {
      border-top: 0.5px solid #ffff;
      background: #ffff;
    }
    .media-logo-list {
      display: flex;
      justify-content: center;
      align-items: center;
      list-style: none;
      gap: 23px;
      margin: 65px 0 17px;
    }
    .media-logo-list .logo-item {
      width: 20px;
      height: 20px;
    }
    .media-logo-list .logo-item .logo-link {
      width: 100%;
      height: 100%;
      display: inline-block;
    }
    .f-desc {
      font-size: 14px;
      font-weight: 400;
      line-height: 24px;
      color: #939393;
      text-align: center;
      max-width: 80%;
      margin: 0 auto;
      padding-bottom: 27px;
      text-transform: uppercase;
    }
    .f-nav-list {
      padding: 27px 0;
      display: flex;
      justify-content: center;
      align-items: center;
      list-style: none;
      border-top: 0.5px solid #979797;
    }
    .f-nav-list .f-nav-item {
      margin: 0 5px;
    }
    .f-nav-list .f-nav-item .f-nav-link {
      font-size: 14px;
      font-weight: 400;
      line-height: 24px;
      text-align: center;
      color: #939393;
      text-decoration: none;
    }
    @media only screen and (max-width: 480px) {
      .logo-wrap {
        padding: 25px 0;
      }
      .spin-btn {
        max-width: 200px;
        font-size: 14px;
        line-height: 18px;
      }
      .top-content .desc {
        margin: 0 auto 40px;
        max-width: 80%;
      }
      .header-container {
        background-size: auto;
      }
      .common-wrap .content-wrap {
        max-width: 90%;
        margin: 60px auto 0;
        padding-bottom: 80px;
      }
      .top-content .title {
        font-size: 30px;
        line-height: 40px;
        margin-bottom: 10px;
      }
      .f-desc {
        line-height: 20px;
      }
      .logo-wrap .img-wrap {
        width: 100%;
        max-width: 130px;
        max-height: 60px;
        margin: 0 auto;
      }
    }
  </style>
</head>
<body>
  <amp-state id="step">
    <script type="application/json">
        {
          "step": 1
        }
      </script>
  </amp-state>
  <div class="main">
    <!-- header section -->
    <header>
      <div class="header-container">
        <div class="logo-wrap">
          <div class="img-wrap">
            <amp-img layout="responsive"
              src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInStore-AMP/logo.png" alt="Logo"
              width="159" height="73" />
          </div>
        </div>
      </div>
    </header>
    <!-- header section -->
    <!-- main content section -->
    <div class="main-content">
      <div class="common-wrap">
        <div class="orange-triangle"></div>
        <div class="content-wrap">
          <div class="top-content">
            <h1 class="title">Spin the Wheel</h1>
            <h2 class="sub-title">And Win Free Products And More</h2>
            <p class="desc">
              Is simply dummy text of the printing and typesetting industry.
              Lorem Ipsum has been the industry's standard dummy.
            </p>
          </div>
          <div class="bottom-content">
            <div class="wrapper">
              <!--<div class="ticker">
                  <amp-img
                    layout="fixed"
                    src="./images/icon-arrow.png"
                    alt="ticker"
                    class="ticker-icon"
                    width="80"
                    height="50">
                  </amp-img>
                </div> -->
              <div class="step-1" [hidden]="step != 1">
                <div class="wheel-spin-box">
                  <amp-img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/spinn/wheel-start.png"
                    layout="responsive" width="450" height="450" role="button" tabindex="0" layout="responsive">
                  </amp-img>
                </div>
              </div>
              <div class="step-2" hidden [hidden]="step != 2">
                <div class="wheel-spin-gif-box">
                  <amp-img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/spinn/spin-wheel.gif"
                    layout="responsive" width="450" height="450" role="button" tabindex="0" layout="responsive">
                  </amp-img>
                </div>
              </div>
              <div class="step-3" hidden [hidden]="step != 3">
                <div class="wheel-spin-box">
                  <amp-img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/spinn/wheel-win.png"
                    layout="responsive" width="450" height="450" role="button" tabindex="0" layout="responsive">
                  </amp-img>
                </div>
              </div>
            </div>
            <!-- Result Section -->
            <div class="result-wrapper step-4" hidden [hidden]="step != 4">
              <div class="yellow-wrap">
                <amp-img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/spinn/result-tshirt.png"
                  width="490" height="350" layout="responsive" alt="result image">
                </amp-img>
              </div>
              <h2 class="result-content">
                Congratulations, you win
                <span class="cm-bold">A Half white T-Shirt!</span>
              </h2>
            </div>
          </div>
        </div>
      </div>
      <div class="btn-wrap">
        <button class="spin-btn typ-2" [hidden]="step != 1" on="tap:AMP.setState({ step: 2 })"> Spin the Wheel </button>
        <button class="spin-btn typ-2" hidden [hidden]="step != 2" on="tap:AMP.setState({ step: 3 })">Stop the
          Wheel</button>
        <button class="spin-btn typ-2" hidden [hidden]="step != 3" on="tap:AMP.setState({ step: 4 })">Get now</button>
        <a href="https://www.google.com" class="spin-btn typ-2" hidden [hidden]="step != 4"
          on="tap:AMP.setState({ step: 4 })">Shop now</a>
      </div>
    </div>
    <!-- main content section -->
    <!-- footer start  -->
    <footer class="footer">
      <ul class="media-logo-list">
        <li class="logo-item">
          <a href="https://www.google.co.in/" class="logo-link">
            <amp-img layout="fixed" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/spinn/logo-insta.png"
              alt="instagram" class="media-logo" width="20" height="20"></amp-img>
          </a>
        </li>
        <li class="logo-item">
          <a href="https://www.google.co.in/" class="logo-link">
            <amp-img layout="fixed"
              src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/spinn/logo-facebook.png" alt="facebook"
              class="media-logo" width="20" height="20"></amp-img>
          </a>
        </li>
        <li class="logo-item">
          <a href="https://www.google.co.in/" class="logo-link">
            <amp-img layout="fixed" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/spinn/logo-x.png"
              alt="x" class="media-logo" width="20" height="20"></amp-img>
          </a>
        </li>
      </ul>
      <p class="f-desc">
        This is just the beginning—count on us to support you every step.
        Welcome to the [community/family/team]!
      </p>
      <p class="f-desc">
        To stop receiving these emails, <a href="https://google.com"
          style="color:#fe592c;font-weight:bold;text-decoration:none;">unsubscribe here</a>
      </p>
    </footer>
    <!-- footer end  -->
  </div>
</body>
</html>
```

</details>

## Form

This AMP template enables you to collect user input directly within the email, allowing for quick interactions such as survey responses, feedback, or sign-ups. With AMP’s real-time interactivity, the form can be submitted without users needing to open a separate browser window, making the experience fast, seamless, and conversion-friendly.

<details>

<summary>Expand to know more about the template.</summary>

### Use Case Examples

- Gather user feedback post-purchase or post-interaction.
- Collect survey responses (for example, NPS survey, product ratings, and so on).
- Enable newsletter or webinar sign-ups within the email.
- Registration for events, contests, or loyalty programs.

### Template Customization Options

- Replace the Logo
- Update Banner/Product Images
- Update Call-To-Actions (CTAs)
- Update Links in the Header/Footer
- Change the Theme or Background Color
- Update Social Media and Download Links

### Template Code

```html Variant 1
<!DOCTYPE html>
<html ⚡4email data-css-strict>
<head>
  <meta charset="utf-8">
  <script async src="https://cdn.ampproject.org/v0.js"></script>
  <script async custom-element="amp-form" src="https://cdn.ampproject.org/v0/amp-form-0.1.js"></script>
  <script async custom-element="amp-bind" src="https://cdn.ampproject.org/v0/amp-bind-0.1.js"></script>
  <style amp4email-boilerplate>
    body {
      visibility: hidden;
    }
  </style>
  <style amp-custom>
    * {
      margin: 0;
      padding: 0;
    }
    body {
      font-family: "Helvetica", Arial, sans-serif;
      font-weight: 400;
    }
    img {
      width: 100%;
      height: 100%;
      object-fit: contain;
    }
    /* Change Theme */
    .main {
      width: 100%;
      max-width: 600px;
      overflow: hidden;
      margin: 0 auto;
      background: #cecece;
      position: relative;
    }
    /* Change Theme */
    @media only screen and (max-width: 400px) {
      body .main {
        max-width: 95%;
      }
    }
    .logo-wrap {
      padding: 16px 0;
      background-color: #ffffff;
    }
    .logo-wrap .img-wrap {
      max-width: 146px;
      max-height: 75px;
      margin: 0 auto;
    }
    .footer {
      border-top: 0.5px solid #ffff;
      background: #ffff;
    }
    .media-logo-list {
      display: flex;
      justify-content: center;
      align-items: center;
      list-style: none;
      gap: 16px;
      margin: 39px 0 14px;
    }
    .media-logo-list .logo-item {
      width: 28px;
      height: 28px;
    }
    .media-logo-list .logo-item .logo-link {
      width: 100%;
      height: 100%;
      display: inline-block;
    }
    .f-desc {
      font-size: 14px;
      font-weight: 400;
      line-height: 24px;
      color: #939393;
      text-align: center;
      max-width: 65%;
      margin: 0 auto 27px;
      padding-bottom: 47px;
    }
    .f-nav-list {
      padding: 27px 0;
      display: flex;
      justify-content: center;
      align-items: center;
      list-style: none;
      border-top: 0.5px solid #979797;
    }
    .f-nav-list .f-nav-item {
      margin: 0 5px;
    }
    .f-nav-list .f-nav-item .f-nav-link {
      font-size: 14px;
      font-weight: 400;
      line-height: 24px;
      text-align: center;
      color: #939393;
      text-decoration: none;
    }
    .banner .img-wrap {
      max-height: 361px;
      width: 100%;
    }
    .success-container {
      text-align: center;
      background-color: rgba(206, 206, 206, 0.5);
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: 10;
    }
    .success-container .success-wrap {
      max-width: 312px;
      width: 100%;
      position: relative;
      top: 20%;
      left: 50%;
      transform: translateX(-50%);
      background: #ffffff;
      padding: 60px 40px;
    }
    .success-wrap h4 {
      font-size: 16px;
      font-weight: 400;
      line-height: 27px;
      text-align: center;
      text-transform: uppercase;
      margin-bottom: 10px;
    }
    .success-wrap p {
      font-size: 12px;
      font-weight: 400;
      line-height: 20px;
      text-align: center;
      color: #909090;
      text-transform: capitalize;
    }
    .container {
      max-width: 555px;
      margin: -30px auto 42px;
      position: relative;
      z-index: 2;
    }
    .form-container {
      padding: 33px 22px 26px 23px;
      background-color: #ffffff;
      box-shadow: 0px 8.26px 3.3px 0px #00000040;
    }
    .form-container h2 {
      font-size: 16px;
      font-weight: 400;
      line-height: 22px;
      color: #000000;
      margin-bottom: 8px;
    }
    .form-container p {
      font-size: 12px;
      font-weight: 400;
      line-height: 16px;
      color: #909090;
      margin-bottom: 20px;
      text-transform: capitalize;
    }
    .form-container .form-field-wrap {
      display: flex;
      gap: 14px;
      flex-wrap: wrap;
    }
    .form-field-wrap .form-group {
      display: flex;
      flex-direction: column;
      max-width: 248px;
      width: 100%;
    }
    .form-group label {
      font-size: 12px;
      font-weight: 400;
      line-height: 16.52px;
      text-align: left;
      color: #000000;
      text-transform: capitalize;
      margin-bottom: 5px;
    }
    .form-group input {
      padding: 5px 0 5px 8px;
      max-width: 248.65px;
      height: 27.26px;
      margin-bottom: 2px;
      font-size: 12px;
      font-weight: 400;
      line-height: 16.52px;
      text-align: left;
      color: #000000;
      text-transform: capitalize;
      border: 0.83px solid #adadad;
    }
    .form-group input[type="date"] {
      text-transform: uppercase;
    }
    .form-group .label-wrap {
      display: flex;
      justify-content: space-between;
    }
    .form-group .label-wrap .remove .remove-logo {
      width: 16px;
      height: 16px;
    }
    .form-group.gender,
    .form-group.favorite,
    .form-group.purchase {
      margin-top: 16px;
      max-width: 100%;
    }
    .form-group select {
      flex-grow: 1;
      padding: 8px;
      border: 1px solid #ccc;
      border-radius: 4px;
    }
    .form-container .gender-options {
      display: flex;
      justify-content: space-between;
      margin-bottom: 16px;
      max-width: 130px;
    }
    .form-container .gender-options label {
      display: flex;
      align-items: center;
      max-width: 100px;
      width: 100%;
      margin: 0;
      font-size: 14px;
      font-weight: 400;
      line-height: 19.83px;
      text-align: center;
    }
    .gender-options input {
      margin-right: 6px;
    }
    .form-group.favorite {
      display: flex;
      flex-direction: column;
      margin-bottom: 5px;
    }
    .favorite select {
      font-size: 10px;
      font-weight: 400;
      line-height: 15px;
      text-align: left;
      background: #ffffff;
      color: #000000;
      border: 0.83px solid #ADADAD;
      border-radius: 0;
    }
    .favorite select option {
      width: 50px;
      font-size: 12px;
    }
    .form-container .checkbox {
      display: flex;
      flex-direction: column;
      margin-top: 5px;
    }
    .purchase .checkbox label {
      display: flex;
      align-items: center;
      max-width: 100px;
      width: 100%;
      font-size: 14px;
      font-weight: 400;
      line-height: 16.83px;
      text-align: center;
      margin-bottom: 11px;
    }
    .purchase .checkbox label input {
      margin-right: 6px;
      width: 14px;
      height: 14px;
      padding: 0;
    }
    .form-container .submit {
      padding: 7px 45px;
      background-color: #000000;
      color: #ffffff;
      border: none;
      cursor: pointer;
      text-transform: uppercase;
      font-size: 16px;
      font-weight: 400;
      line-height: 16.52px;
      text-align: left;
      position: relative;
      left: 50%;
      transform: translateX(-50%);
      margin-top: 10px;
    }
    .remove {
      background: transparent;
      border: none;
      outline: 0;
    }
    .hidden {
      display: none;
    }
    .show {
      display: block;
    }
    @media only screen and (max-width: 400px) {
      .f-desc {
        max-width: 80%;
      }
    }
    @media only screen and (max-width: 375px) {
      .form-field-wrap .form-group,
      .form-group input,
      .form-group input[type="date"],
      input#birth-date {
        max-width: 100%;
        width: 100%;
      }
      .favorite select {
        height: 27.26px;
      }
      input[type="radio"] {
        width: auto;
      }
    }
  </style>
</head>
<body>
  <div class="main">
    <header>
      <div class="logo-wrap">
        <div class="img-wrap">
          <!-- Change Logo Image src as per your requirements -->
          <amp-img layout="responsive"
            src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInStore-AMP/logo.png" alt="Logo"
            width="146" height="75"></amp-img>
          <!-- Change Logo Image src as per your requirements -->
        </div>
      </div>
    </header>
    <div class="banner">
      <div class="img-wrap">
        <!-- Change image src as per your requirements -->
        <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/AMP-FORM/banner.png"
          alt="Banner" width="600" height="361"></amp-img>
      </div>
    </div>
    <!-- Success Container - Initially Hidden -->
    <div class="success-container hidden"
      [class]="!successVisible ? 'success-container hidden' : 'success-container show'">
      <div class="success-wrap">
        <h4 class="title">Information saved</h4>
        <p class="para">
          is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard
          dummy .
        </p>
      </div>
    </div>
    <div class="container">
      <div class="form-container">
        <h2>Fill the form</h2>
        <p>
          is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard
          dummy.
        </p>
        <form method="post" class="form" action-xhr="https://example.com/submit"
          on="submit-success:AMP.setState({successVisible: false})">
          <div class="form-field-wrap">
            <!-- First Name -->
            <div class="form-group">
              <div class="label-wrap">
                <label for="first-name">Enter your first name</label>
              </div>
              <input type="text" id="first-name" name="firstName" placeholder="First name" [value]="firstName"
                on="input-debounced:AMP.setState({firstName: event.target.value}), change:AMP.setState({firstName: event.value})" />
            </div>
            <!-- Last Name -->
            <div class="form-group">
              <div class="label-wrap">
                <label for="last-name">Enter your last name</label>
              </div>
              <input type="text" id="last-name" name="lastName" placeholder="Last name" [value]="lastName"
                on="input-debounced:AMP.setState({lastName: event.target.value}), change:AMP.setState({lastName: event.value})" />
            </div>
            <!-- Phone Number -->
            <div class="form-group">
              <div class="label-wrap">
                <label for="phone-number">Enter your Phone number</label>
              </div>
              <input type="tel" id="phone-number" name="phoneNumber" placeholder="Phone number" [value]="phoneNumber"
                on="input-debounced:AMP.setState({phoneNumber: event.target.value}), change:AMP.setState({phoneNumber: event.value})" />
            </div>
            <!-- Birth Date -->
            <div class="form-group">
              <div class="label-wrap">
                <label for="birth-date">Enter your Birth date</label>
              </div>
              <input type="date" id="birth-date" name="birthDate" placeholder="Enter date" [value]="birthDate"
                on="input-debounced:AMP.setState({birthDate: event.target.value}), change:AMP.setState({birthDate: event.value})" />
            </div>
            <!-- Gender -->
            <div class="form-group gender">
              <div class="label-wrap">
                <label>Select your gender</label>
              </div>
              <div class="gender-options">
                <label>
                  <input type="radio" name="gender" value="Male"  checked /> Male
                </label>
                <label>
                  <input type="radio" name="gender" value="Female" /> Female
                </label>
              </div>
            </div>
            <!-- Favorite Clothing -->
            <div class="form-group favorite">
              <div class="label-wrap">
                <label for="clothing">Select your favorite type of clothing</label>
              </div>
              <select id="clothing" name="clothing" on="change:AMP.setState({clothing: event.value})">
                <option disabled selected>Select</option>
                <option value="Casual">Casual</option>
                <option value="Formal">Formal</option>
                <option value="Sportswear">Sportswear</option>
              </select>
            </div>
            <!-- Purchased Before -->
            <div class="form-group purchase">
              <div class="label-wrap">
                <label>Have you purchased from this brand before?</label>
              </div>
              <div class="checkbox">
                <label>
                  <input type="checkbox" name="purchasedBefore" value="Yes"
                    on="change:AMP.setState({purchasedBefore: event.target.checked ? 'Yes' : ''})" /> Yes
                </label>
                <label>
                  <input type="checkbox" name="purchasedBefore" value="No"
                    on="change:AMP.setState({purchasedBefore: event.target.checked ? 'No' : ''})" /> No
                </label>
              </div>
            </div>
            <div class="btn-wrap" style="width:100%">
              <!-- Change CTA -->
              <button type="submit" class="submit" on="tap:AMP.setState({successVisible: true})">Submit</button>
                            <!-- Change CTA -->
            </div>
          </div>
        </form>
      </div>
    </div>
    <!-- Footer Section -->
    <footer class="footer">
      <ul class="media-logo-list">
        <!-- Social Links -->
        <li class="logo-item">
          <a href="https://www.google.co.in/" class="logo-link">
            <amp-img layout="responsive"
              src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/AMP-FORM/b-insta.png" alt="instagram"
              class="media-logo" width="34" height="34"></amp-img>
          </a>
        </li>
        <li class="logo-item">
          <a href="https://www.google.co.in/" class="logo-link">
            <amp-img layout="responsive"
              src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/AMP-FORM/b-fb.png" alt="facebook"
              class="media-logo" width="34" height="34"></amp-img>
          </a>
        </li>
        <li class="logo-item">
          <a href="https://www.google.co.in/" class="logo-link">
            <amp-img layout="responsive"
              src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/AMP-FORM/b-x.png" alt="x"
              class="media-logo" width="34" height="34"></amp-img>
          </a>
        </li>
         <!-- Social Links -->
      </ul>
      <p class="f-desc">
        This is just the beginning—count on us to support you every step. Welcome to the [community/family/team]!
      </p>
      <p class="f-desc">
        To stop receiving these emails, <a href="https://google.com"
          style="color:#1E1E1E;font-weight:bold;text-decoration:none;">unsubscribe here</a>
      </p>
    </footer>
        <!-- Footer Section -->
  </div>
</body>
</html>
```
```html Variant 2
<!DOCTYPE html>
<html ⚡4email data-css-strict>
<head>
  <meta charset="utf-8">
  <script async src="https://cdn.ampproject.org/v0.js"></script>
  <script async custom-element="amp-form" src="https://cdn.ampproject.org/v0/amp-form-0.1.js"></script>
  <script async custom-element="amp-bind" src="https://cdn.ampproject.org/v0/amp-bind-0.1.js"></script>
  <style amp4email-boilerplate>
    body {
      visibility: hidden
    }
  </style>
  <style amp-custom>
    * {
      margin: 0;
      padding: 0;
    }
    body {
      font-family: "Helvetica", arial, sans-serif;
      font-weight: 400;
    }
    img {
      width: 100%;
      height: 100%;
      object-fit: contain;
    }
    /* Change Theme */
    .main {
      width: 100%;
      max-width: 600px;
      overflow: hidden;
      margin: 0 auto;
      background: #cecece;
      position: relative;
    }
    /* Change Theme */
    @media only screen and (max-width: 400px) {
      body .main {
        max-width: 95%;
      }
    }
    .logo-wrap {
      padding: 16px 0;
      background-color: #ffffff;
    }
    .logo-wrap .img-wrap {
      max-width: 146px;
      max-height: 75px;
      margin: 0 auto;
    }
    .footer {
      border-top: 0.5px solid #ffff;
      background: #ffff;
    }
    .media-logo-list {
      display: flex;
      justify-content: center;
      align-items: center;
      list-style: none;
      gap: 16px;
      margin: 39px 0 14px;
    }
    .media-logo-list .logo-item {
      width: 28px;
      height: 28px;
    }
    .media-logo-list .logo-item .logo-link {
      width: 100%;
      height: 100%;
      display: inline-block;
    }
    .f-desc {
      font-size: 14px;
      font-weight: 400;
      line-height: 24px;
      color: #939393;
      text-align: center;
      max-width: 65%;
      margin: 0 auto 27px;
      padding-bottom: 47px;
    }
    .f-nav-list {
      padding: 27px 0;
      display: flex;
      justify-content: center;
      align-items: center;
      list-style: none;
      border-top: 0.5px solid #979797;
    }
    .f-nav-list .f-nav-item {
      margin: 0 5px;
    }
    .f-nav-list .f-nav-item .f-nav-link {
      font-size: 14px;
      font-weight: 400;
      line-height: 24px;
      text-align: center;
      color: #939393;
      text-decoration: none;
    }
    .banner .img-wrap {
      max-height: 361px;
      width: 100%;
    }
    .success-container {
      text-align: center;
      background-color: rgba(206, 206, 206, 0.5);
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: 10;
    }
    .success-container .success-wrap {
      max-width: 312px;
      width: 100%;
      position: relative;
      top: 20%;
      left: 50%;
      transform: translateX(-50%);
      background: #ffffff;
      padding: 60px 40px;
    }
    .success-wrap h4 {
      font-size: 16px;
      font-weight: 400;
      line-height: 27px;
      text-align: center;
      text-transform: uppercase;
      margin-bottom: 10px;
    }
    .success-wrap p {
      font-size: 12px;
      font-weight: 400;
      line-height: 20px;
      text-align: center;
      color: #909090;
      text-transform: capitalize;
    }
    .container {
      max-width: 555px;
      margin: -30px auto 42px;
      position: relative;
      z-index: 2;
    }
    .form-container {
      padding: 33px 22px 26px 23px;
      background-color: #ffffff;
      box-shadow: 0px 8.26px 3.3px 0px #00000040;
    }
    .form-container h2 {
      font-size: 16px;
      font-weight: 400;
      line-height: 22px;
      color: #000000;
      margin-bottom: 8px;
    }
    .form-container p {
      font-size: 12px;
      font-weight: 400;
      line-height: 16px;
      color: #909090;
      margin-bottom: 20px;
      text-transform: capitalize;
    }
    .form-container .form-field-wrap {
      display: flex;
      gap: 14px;
      flex-wrap: wrap;
    }
    .form-field-wrap .form-group {
      display: flex;
      flex-direction: column;
      width: 48%;
    }
    .form-group label {
      font-size: 12px;
      font-weight: 400;
      line-height: 16.52px;
      text-align: left;
      color: #000000;
      text-transform: capitalize;
      margin-bottom: 5px;
    }
    .form-group input[type="text"],
    .form-group input[type="date"],
    .form-group input[type="tel"],
    .form-group input[type="number"] {
      padding: 5px 10px;
      width: 91%;
      height: 27.26px;
      margin-bottom: 2px;
      font-size: 12px;
      font-weight: 400;
      line-height: 16.52px;
      text-align: left;
      color: #000000;
      text-transform: capitalize;
      border: 0.83px solid #adadad;
    }
    .form-group input[type="date"] {
      text-transform: uppercase;
    }
    .form-group .label-wrap {
      display: flex;
      justify-content: space-between;
    }
    .form-group .label-wrap .remove .remove-logo {
      width: 16px;
      height: 16px;
    }
    .form-group.full-width {
      margin-bottom: 15px;
      width: 100%;
    }
    .form-group.full-width input[type="text"] {
      width: 96%;
    }
    .form-group.gender,
    .form-group.favorite,
    .form-group.purchase {
      margin-top: 16px;
      width: 100%;
    }
    .form-group select {
      flex-grow: 1;
      padding: 8px;
      border: 1px solid #ccc;
      border-radius: 4px;
    }
    .form-container .gender-options {
      display: flex;
      justify-content: space-between;
      max-width: 130px;
    }
    .form-container .gender-options label {
      display: flex;
      align-items: center;
      max-width: 100px;
      width: 100%;
      margin: 0;
      font-size: 14px;
      font-weight: 400;
      line-height: 19.83px;
      text-align: center;
    }
    .gender-options input[type="radio"] {
      margin-right: 6px;
    }
    .form-group.favorite {
      display: flex;
      flex-direction: column;
      margin-bottom: 5px;
    }
    .favorite select {
      font-size: 10px;
      font-weight: 400;
      line-height: 15px;
      text-align: left;
      background: #ffffff;
      color: #000000;
      border: 0.83px solid #ADADAD;
      border-radius: 0;
    }
    .favorite select option {
      width: 50px;
      font-size: 12px;
    }
    .form-container .checkbox {
      display: flex;
      flex-direction: column;
      margin-top: 5px;
    }
    .purchase .checkbox label {
      display: flex;
      align-items: center;
      max-width: 100px;
      width: 100%;
      font-size: 14px;
      font-weight: 400;
      line-height: 16.83px;
      text-align: center;
      margin-bottom: 11px;
    }
    .purchase .checkbox label input {
      margin-right: 6px;
      width: 14px;
      height: 14px;
      padding: 0;
    }
    .form-container .submit {
      padding: 7px 45px;
      background-color: #000000;
      color: #ffffff;
      border: none;
      cursor: pointer;
      text-transform: uppercase;
      font-size: 16px;
      font-weight: 400;
      line-height: 16.52px;
      position: relative;
      left: 50%;
      transform: translateX(-50%)
    }
    .remove {
      background: transparent;
      border: none;
      outline: 0;
    }
    .hidden {
      display: none;
    }
    .show {
      display: block;
    }
    @media only screen and (max-width: 400px) {
      .f-desc {
        max-width: 80%;
      }
    }
    .btn-wrap {
      margin-top: 35px;
      display: flex;
      justify-content: flex-end;
      align-items: center;
      width: 100%;
    }
    .btn-wrap.typ-evenly {
      justify-content: space-between;
    }
    .nav-cta {
      font-size: 16px;
      font-weight: 400;
      line-height: 19.76px;
      text-align: center;
      color: #000000;
      text-transform: uppercase;
      background: transparent;
      border: 0;
      display: flex;
      align-items: center;
    }
    .nav-cta {
      margin: 0 2px;
    }
    @media only screen and (max-width: 375px) {
      .form-field-wrap .form-group,
      .form-group input,
      .form-group input[type="date"],
      input#birth-date {
        max-width: 100%;
        width: 100%;
      }
      .favorite select {
        height: 27.26px;
      }
      input[type="radio"] {
        width: auto;
      }
    }
  </style>
</head>
<body>
  <div class="main">
    <header>
      <div class="logo-wrap">
        <div class="img-wrap">
          <!-- Change Logo Image src as per your requirements -->
          <amp-img layout="responsive"
            src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInStore-AMP/logo.png" alt="Logo"
            width="146" height="75" />
          <!-- Change Logo Image src as per your requirements -->
        </div>
      </div>
    </header>
    <div class="banner">
      <div class="img-wrap">
        <!-- Change Banner Image src as per your requirements -->
        <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/AMP-FORM/banner.png"
          alt="Banner" width="600" height="361"></amp-img>
        <!-- Change Banner Image src as per your requirements -->
      </div>
    </div>
    <!-- Success Container - Initially Hidden -->
    <div class="success-container" hidden [hidden]="!showSuccess">
      <div class="success-wrap">
        <h4 class="title">Information saved</h4>
        <p class="para">
          is simply dummy text of the printing and typesetting industry. Lorem
          Ipsum has been the industry's standard dummy .
        </p>
      </div>
    </div>
    <div class="container">
      <div class="form-container">
        <h2>Fill the form</h2>
        <p>
          is simply dummy text of the printing and typesetting industry. Lorem
          Ipsum has been the industry's standard dummy.
        </p>
        <form method="post" class="form" action-xhr="https://example.com/submit"
          on="submit-success:AMP.setState({showSuccess: false, showTab2: false})">
          <div class="tab-1" [class]="!showTab2 ? 'tab-1 show' : 'tab-1 hidden'">
            <div class="form-field-wrap">
              <!-- First Name -->
              <div class="form-group">
                <div class="label-wrap">
                  <label for="first-name">Enter your first name</label>
                </div>
                <input type="text" id="first-name" name="firstName" placeholder="First name" required
                  [value]="firstName"
                  on="input-debounced:AMP.setState({firstName: event.target.value}), change:AMP.setState({firstName: event.value})" />
              </div>
              <!-- Last Name -->
              <div class="form-group">
                <div class="label-wrap">
                  <label for="last-name">Enter your last name</label>
                </div>
                <input type="text" id="last-name" name="lastName" placeholder="Last name" required [value]="lastName"
                  on="input-debounced:AMP.setState({lastName: event.target.value}), change:AMP.setState({lastName: event.value})" />
              </div>
              <!-- Phone Number -->
              <div class="form-group">
                <div class="label-wrap">
                  <label for="phone-number">Enter your Phone number</label>
                </div>
                <input type="tel" id="phone-number" name="phoneNumber" placeholder="Phone number" required
                  [value]="phoneNumber"
                  on="input-debounced:AMP.setState({phoneNumber: event.target.value}), change:AMP.setState({phoneNumber: event.value})" />
              </div>
              <!-- Birth Date -->
              <div class="form-group">
                <div class="label-wrap">
                  <label for="birth-date">Enter your Birth date</label>
                </div>
                <input type="date" id="birth-date" name="birthDate" placeholder="Enter date" required
                  [value]="birthDate"
                  on="input-debounced:AMP.setState({birthDate: event.target.value}), change:AMP.setState({birthDate: event.value})" />
              </div>
              <!-- Gender -->
              <div class="form-group gender">
                <div class="label-wrap">
                  <label>Select your gender</label>
                </div>
                <div class="gender-options">
                  <label><input type="radio" name="gender" value="Male" required checked />
                    Male</label>
                  <label><input type="radio" name="gender" value="Female" />
                    Female</label>
                </div>
              </div>
              <!-- Favorite Clothing -->
              <div class="form-group favorite">
                <div class="label-wrap">
                  <label for="clothing">Select your favorite type of clothing</label>
                </div>
                <select id="clothing" name="clothing" required on="change:AMP.setState({clothing: event.value})">
                  <option value="">Select</option>
                  <option value="Casual">Casual</option>
                  <option value="Formal">Formal</option>
                  <option value="Sportswear">Sportswear</option>
                </select>
              </div>
              <!-- Purchased Before -->
              <div class="form-group purchase">
                <div class="label-wrap">
                  <label>Have you purchased from this brand before?</label>
                </div>
                <div class="checkbox">
                  <label>
                    <input type="checkbox" name="purchasedBefore" value="Yes"
                      on="change:AMP.setState({purchasedBefore: event.target.checked ? 'Yes' : ''})" />
                    Yes
                  </label>
                  <label>
                    <input type="checkbox" name="purchasedBefore" value="No"
                      on="change:AMP.setState({purchasedBefore: event.target.checked ? 'No' : ''})" />
                    No
                  </label>
                </div>
              </div>
              <div class="btn-wrap typ-right">
                <!-- Change CTA -->
                <button type="button" class="nav-cta" on="tap:AMP.setState({showTab2: true})">
                  Next <amp-img layout="fixed"
                    src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/AMP-FORM/icon-next.png" alt="remove"
                    class="nav-logo" width="14" height="12">
                </button>
                <!-- Change CTA -->
              </div>
            </div>
          </div>
          <div class="tab-2 hidden" [class]="!showTab2 ? 'tab-2 hidden' : 'tab-2 show'">
            <div class="form-field-wrap">
              <!-- Question 1-->
              <div class="form-group full-width">
                <div class="label-wrap">
                  <label for="first-name">Question </label>
                </div>
                <input type="text" id="question1" name="Question1" placeholder="Ans here" required
                  on="input-debounced:AMP.setState({question1: event.target.value}), change:AMP.setState({question1: event.value})" />
              </div>
              <!-- Question 2-->
              <div class="form-group full-width">
                <div class="label-wrap">
                  <label for="first-name">Question </label>
                </div>
                <input type="text" id="question2" name="Question2" placeholder="Ans here" required
                  on="input-debounced:AMP.setState({question2: event.target.value}), change:AMP.setState({question2: event.value})" />
              </div>
              <!-- Question 3 -->
              <div class="form-group full-width">
                <div class="label-wrap">
                  <label for="first-name">Question </label>
                </div>
                <input type="text" id="question3" name="Question3" placeholder="Ans here" required 
                  on="input-debounced:AMP.setState({question3: event.target.value}), change:AMP.setState({question3: event.value})" />
              </div>
              <!-- Question 4-->
              <div class="form-group full-width">
                <div class="label-wrap">
                  <label for="first-name">Question </label>
                </div>
                <input type="text" id="question4" name="Question4" placeholder="Ans here" required
                  on="input-debounced:AMP.setState({question4: event.target.value}), change:AMP.setState({question4: event.value})" />
              </div>
              <!-- Question 5-->
              <div class="form-group full-width">
                <div class="label-wrap">
                  <label for="first-name">Question </label>
                </div>
                <input type="text" id="question5" name="Question5" placeholder="Ans here" required
                  on="input-debounced:AMP.setState({question5: event.target.value}), change:AMP.setState({question5: event.value})" />
              </div>
              <div class="btn-wrap typ-evenly">
                <!-- Submit Button -->
                <button type="submit" class="submit" on="tap:AMP.setState({showSuccess: true})">Submit</button>
                <button type="button" class="nav-cta" on="tap:AMP.setState({showTab2: false})">
                  <amp-img layout="fixed"
                    src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/AMP-FORM/icon-back.png" alt="remove"
                    class="nav-logo" width="14" height="12"></amp-img> BACK
                </button>
              </div>
            </div>
          </div>
        </form>
      </div>
    </div>
    <footer class="footer">
      <ul class="media-logo-list">
        <li class="logo-item">
          <a href="https://www.google.co.in/" class="logo-link">
            <amp-img layout="responsive"
              src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/AMP-FORM/b-insta.png" alt="instagram"
              class="media-logo" width="34" height="34"></amp-img>
          </a>
        </li>
        <li class="logo-item">
          <a href="https://www.google.co.in/" class="logo-link">
            <amp-img layout="responsive"
              src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/AMP-FORM/b-fb.png" alt="facebook"
              class="media-logo" width="34" height="34"></amp-img>
          </a>
        </li>
        <li class="logo-item">
          <a href="https://www.google.co.in/" class="logo-link">
            <amp-img layout="responsive"
              src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/AMP-FORM/b-x.png" alt="x"
              class="media-logo" width="34" height="34"></amp-img>
          </a>
        </li>
      </ul>
      <p class="f-desc">
        This is just the beginning—count on us to support you every step.
        Welcome to the [community/family/team]!
      </p>
      <p class="f-desc">
        To stop receiving these emails, <a href="#"
          style="color:#1E1E1E;font-weight:bold;text-decoration:none;">unsubscribe here</a>
      </p>
    </footer>
  </div>
</body>
</html>
```
```html Variant 3
<!DOCTYPE html>
<html ⚡4email data-css-strict>
<head>
  <meta charset="utf-8">
  <script async src="https://cdn.ampproject.org/v0.js"></script>
  <script async custom-element="amp-form" src="https://cdn.ampproject.org/v0/amp-form-0.1.js"></script>
  <script async custom-element="amp-bind" src="https://cdn.ampproject.org/v0/amp-bind-0.1.js"></script>
  <style amp4email-boilerplate>
    body {
      visibility: hidden
    }
  </style>
  <style amp-custom>
    * {
      margin: 0;
      padding: 0;
    }
    body {
      font-family: "Helvetica", arial, sans-serif;
      font-weight: 400;
    }
    img {
      width: 100%;
      height: 100%;
      object-fit: contain;
    }
    /* Change Theme */
    .main {
      width: 100%;
      max-width: 600px;
      overflow: hidden;
      margin: 0 auto;
      background: #cecece;
      position: relative;
    }
    /* Change Theme */
    @media only screen and (max-width: 400px) {
      body .main {
        max-width: 95%;
      }
    }
    .logo-wrap {
      padding: 16px 0;
      background-color: #ffffff;
    }
    .logo-wrap .img-wrap {
      max-width: 146px;
      max-height: 75px;
      margin: 0 auto;
    }
    .footer {
      border-top: 0.5px solid #ffff;
      background: #ffff;
    }
    .media-logo-list {
      display: flex;
      justify-content: center;
      align-items: center;
      list-style: none;
      gap: 16px;
      margin: 39px 0 14px;
    }
    .media-logo-list .logo-item {
      width: 28px;
      height: 28px;
    }
    .media-logo-list .logo-item .logo-link {
      width: 100%;
      height: 100%;
      display: inline-block;
    }
    .f-desc {
      font-size: 14px;
      font-weight: 400;
      line-height: 24px;
      color: #939393;
      text-align: center;
      max-width: 65%;
      margin: 0 auto 27px;
      padding-bottom: 47px;
    }
    .f-nav-list {
      padding: 27px 0;
      display: flex;
      justify-content: center;
      align-items: center;
      list-style: none;
      border-top: 0.5px solid #979797;
    }
    .f-nav-list .f-nav-item {
      margin: 0 5px;
    }
    .f-nav-list .f-nav-item .f-nav-link {
      font-size: 14px;
      font-weight: 400;
      line-height: 24px;
      text-align: center;
      color: #939393;
      text-decoration: none;
    }
    .banner .img-wrap {
      max-height: 361px;
      width: 100%;
    }
    .success-container {
      text-align: center;
      background-color: rgba(206, 206, 206, 0.5);
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: 10;
    }
    .success-container .success-wrap {
      max-width: 312px;
      width: 100%;
      position: relative;
      top: 20%;
      left: 50%;
      transform: translateX(-50%);
      background: #ffffff;
      padding: 60px 40px;
    }
    .success-wrap h4 {
      font-size: 16px;
      font-weight: 400;
      line-height: 27px;
      text-align: center;
      text-transform: uppercase;
      margin-bottom: 10px;
    }
    .success-wrap p {
      font-size: 12px;
      font-weight: 400;
      line-height: 20px;
      text-align: center;
      color: #909090;
      text-transform: capitalize;
    }
    .container {
      max-width: 555px;
      margin: -30px auto 42px;
      position: relative;
      z-index: 2;
    }
    .form-container {
      padding: 33px 22px 26px 23px;
      background-color: #ffffff;
      box-shadow: 0px 8.26px 3.3px 0px #00000040;
    }
    .form-container h2 {
      font-size: 16px;
      font-weight: 400;
      line-height: 22px;
      color: #000000;
      margin-bottom: 8px;
    }
    .form-container p {
      font-size: 12px;
      font-weight: 400;
      line-height: 16px;
      color: #909090;
      margin-bottom: 20px;
      text-transform: capitalize;
    }
    .form-container .form-field-wrap {
      display: flex;
      gap: 14px;
      flex-wrap: wrap;
    }
    .form-field-wrap .form-group {
      display: flex;
      flex-direction: column;
      width: 48%;
    }
    .form-group label {
      font-size: 12px;
      font-weight: 400;
      line-height: 16.52px;
      text-align: left;
      color: #000000;
      text-transform: capitalize;
      margin-bottom: 8px;
    }
    .form-group input[type="text"],
    .form-group input[type="date"],
    .form-group input[type="tel"],
    .form-group input[type="number"] {
      padding: 5px 10px;
      width: 91%;
      height: 27.26px;
      margin-bottom: 2px;
      font-size: 12px;
      font-weight: 400;
      line-height: 16.52px;
      text-align: left;
      color: #000000;
      text-transform: capitalize;
      border: 0.83px solid #adadad;
    }
    .form-group input[type="date"] {
      text-transform: uppercase;
    }
    .form-group .label-wrap {
      display: flex;
      justify-content: space-between;
    }
    .form-group .label-wrap .remove .remove-logo {
      width: 16px;
      height: 16px;
    }
    .form-group.full-width {
      margin-bottom: 15px;
    }
    .form-group.full-width input[type="text"] {
      width: 96%;
    }
    .form-group.feedback,
    .form-group.gender,
    .form-group.favorite,
    .form-group.purchase {
      margin-top: 16px;
      width: 100%;
    }
    .form-group select {
      flex-grow: 1;
      padding: 8px;
      border: 1px solid #ccc;
      border-radius: 4px;
    }
    .form-container .gender-options {
      display: flex;
      justify-content: space-between;
      max-width: 130px;
    }
    .form-container .gender-options label {
      display: flex;
      align-items: center;
      max-width: 100px;
      width: 100%;
      margin: 0;
      font-size: 14px;
      font-weight: 400;
      line-height: 19.83px;
      text-align: center;
    }
    .gender-options input[type="radio"] {
      margin-right: 6px;
    }
    .form-group.favorite {
      display: flex;
      flex-direction: column;
      margin-bottom: 5px;
    }
    .favorite select {
      font-size: 10px;
      font-weight: 400;
      line-height: 15px;
      text-align: left;
      background: #ffffff;
      color: #000000;
      border: 0.83px solid #ADADAD;
      border-radius: 0;
    }
    .favorite select option {
      width: 50px;
      font-size: 12px;
    }
    .form-container .checkbox {
      display: flex;
      flex-direction: column;
      margin-top: 5px;
    }
    .purchase .checkbox label {
      display: flex;
      align-items: center;
      max-width: 100px;
      width: 100%;
      font-size: 14px;
      font-weight: 400;
      line-height: 16.83px;
      text-align: center;
      margin-bottom: 11px;
    }
    .purchase .checkbox label input {
      margin-right: 6px;
      width: 14px;
      height: 14px;
      padding: 0;
    }
    .form-container .submit {
      padding: 7px 45px;
      background-color: #000000;
      color: #ffffff;
      border: none;
      cursor: pointer;
      text-transform: uppercase;
      font-size: 16px;
      font-weight: 400;
      line-height: 16.52px;
      position: relative;
    }
    .remove {
      background: transparent;
      border: none;
      outline: 0;
    }
    .hidden {
      display: none;
    }
    .show {
      display: block;
    }
    @media only screen and (max-width: 400px) {
      .f-desc {
        max-width: 80%;
      }
    }
    .btn-wrap {
      width: 100%;
      margin-top: 35px;
      display: flex;
      justify-content: center;
      align-items: center;
    }
    .nav-cta {
      font-size: 16px;
      font-weight: 400;
      line-height: 19.76px;
      text-align: center;
      color: #000000;
      text-transform: uppercase;
      background: transparent;
      border: 0;
      display: flex;
      align-items: center;
    }
    .nav-cta {
      margin: 0 2px;
    }
    .feedback-options {
      display: flex;
      flex-direction: column;
    }
    .form-group .feedback-label {
      margin-bottom: 13px;
      display: flex;
      align-items: center;
      font-size: 14px;
      font-weight: 400;
      line-height: 19.83px;
    }
    .feedback-label input {
      margin-right: 10px;
    }
    .feedback-input input[type="text"] {
      margin-bottom: 20px;
    }
    .feedback-bad-group,
    .feedback-good-group {
      margin-left: 20px;
    }
    @media only screen and (max-width: 375px) {
      .form-field-wrap .form-group,
      .form-group input,
      .form-group input[type="date"],
      input#birth-date {
        max-width: 100%;
        width: 100%;
      }
      .favorite select {
        height: 27.26px;
      }
      input[type="radio"] {
        width: auto;
      }
    }
  </style>
</head>
<body>
  <div class="main">
    <header>
      <div class="logo-wrap">
        <div class="img-wrap">
          <!-- Change Logo Image src as per your requirements -->
          <amp-img layout="responsive"
            src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInStore-AMP/logo.png" alt="Logo"
            width="146" height="75" />
          <!-- Change Logo Image src as per your requirements -->
        </div>
      </div>
    </header>
    <div class="banner">
      <div class="img-wrap">
        <!-- Change Banner Image src as per your requirements -->
        <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/AMP-FORM/banner.png"
          alt="Banner" width="600" height="361"></amp-img>
        <!-- Change Banner Image src as per your requirements -->
      </div>
    </div>
    <!-- Success Container - Initially Hidden -->
    <div class="success-container" hidden [hidden]="!showSuccess">
      <div class="success-wrap">
        <h4 class="title">Information saved</h4>
        <p class="para">
          is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard
          dummy .
        </p>
      </div>
    </div>
    <div class="container">
      <div class="form-container">
        <h2>Fill the form</h2>
        <p>
          is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard
          dummy.
        </p>
        <form method="post" class="form" action-xhr="" on="submit-success:AMP.setState({showSuccess: false, feedbackType: '', selectedGoodQuestion: '', selectedBadQuestion: ''})">
          <div class="form-field-wrap">
            <!-- First Name -->
            <div class="form-group">
              <div class="label-wrap">
                <label for="first-name">Enter your first name</label>
              </div>
              <input type="text" id="first-name" name="firstName" placeholder="First name" required [value]="firstName"
                on="input-debounced:AMP.setState({firstName: event.target.value}), change:AMP.setState({firstName: event.value})" />
            </div>
            <!-- Last Name -->
            <div class="form-group">
              <div class="label-wrap">
                <label for="last-name">Enter your last name</label>
              </div>
              <input type="text" id="last-name" name="lastName" placeholder="Last name" required [value]="lastName"
                on="input-debounced:AMP.setState({lastName: event.target.value}), change:AMP.setState({lastName: event.value})" />
            </div>
            <!-- Phone Number -->
            <div class="form-group">
              <div class="label-wrap">
                <label for="phone-number">Enter your Phone number</label>
              </div>
              <input type="tel" id="phone-number" name="phoneNumber" placeholder="Phone number" required [value]="phoneNumber"
                on="input-debounced:AMP.setState({phoneNumber: event.target.value}), change:AMP.setState({phoneNumber: event.value})" />
            </div>
            <!-- Birth Date -->
            <div class="form-group">
              <div class="label-wrap">
                <label for="birth-date">Enter your Birth date</label>
              </div>
              <input type="date" id="birth-date" name="birthDate" [value]="birthDate" placeholder="Enter date" required
                on="change:AMP.setState({birthDate: event.value})" />
            </div>
            <!-- Gender -->
            <div class="form-group gender">
              <div class="label-wrap">
                <label>Select your gender</label>
              </div>
              <div class="gender-options">
                <label>
                  <input type="radio" name="gender" value="Male" required checked /> Male
                </label>
                <label>
                  <input type="radio" name="gender" value="Female" /> Female
                </label>
              </div>
            </div>
            <!-- Favorite Clothing -->
            <div class="form-group favorite">
              <div class="label-wrap">
                <label for="clothing">Select your favorite type of clothing</label>
              </div>
              <select id="clothing" name="clothing" required on="change:AMP.setState({clothing: event.value})">
                <option value="">Select</option>
                <option value="Casual">Casual</option>
                <option value="Formal">Formal</option>
                <option value="Sportswear">Sportswear</option>
              </select>
            </div>
            <!-- Purchased Before -->
            <div class="form-group purchase">
              <div class="label-wrap">
                <label>Have you purchased from this brand before?</label>
              </div>
              <div class="checkbox">
                <label>
                  <input type="checkbox" name="purchasedBefore" value="Yes" required
                    on="change:AMP.setState({purchasedBefore: event.target.checked ? 'Yes' : ''})" /> Yes
                </label>
                <label>
                  <input type="checkbox" name="purchasedBefore" value="No"
                    on="change:AMP.setState({purchasedBefore: event.target.checked ? 'No' : ''})" /> No
                </label>
              </div>
            </div>
            <!-- Please give feedback on our brand. -->
            <div class="form-group feedback">
              <div class="label-wrap">
                <label>Please give feedback on our brand.</label>
              </div>
              <div class="feedback-options">
                <label class="feedback-label">
                  <input type="radio" name="feedback" value="Good"  [value]="feedback"
                    on="change:AMP.setState({feedbackType: 'Good', selectedGoodQuestion: '', selectedBadQuestion: ''})" /> Good
                </label>
                <div class="feedback-good-group" hidden [hidden]="feedbackType != 'Good'">
                  <label class="feedback-label">
                    <input type="radio" name="goodFeedback"  [value]="goodFeedback"
                      on="change:AMP.setState({selectedGoodQuestion: 'Question1'})" /> Question 1
                  </label>
                  <div class="feedback-input" hidden [hidden]="selectedGoodQuestion != 'Question1'">
                    <input type="text" id="goodFeedback1" name="goodFeedback1" [value]="goodFeedback1" placeholder="Answer Here" />
                  </div>
                  <label class="feedback-label">
                    <input type="radio" name="goodFeedback"
                      on="change:AMP.setState({selectedGoodQuestion: 'Question2'})" /> Question 2
                  </label>
                  <div class="feedback-input" hidden [hidden]="selectedGoodQuestion != 'Question2'">
                    <input type="text" id="goodFeedback2" name="goodFeedback2" [value]="goodFeedback2" placeholder="Answer Here" />
                  </div>
                </div>
                <label class="feedback-label">
                  <input type="radio" name="feedback" value="Bad" [value]="feedback"
                    on="change:AMP.setState({feedbackType: 'Bad', selectedBadQuestion: '', selectedGoodQuestion: ''})" /> Bad
                </label>
                <div class="feedback-bad-group" hidden [hidden]="feedbackType != 'Bad'">
                  <label class="feedback-label">
                    <input type="radio" name="badFeedback" [value]="badFeedback"
                      on="change:AMP.setState({selectedBadQuestion: 'Question1'})"  /> Question 1
                  </label>
                  <div class="feedback-input" hidden [hidden]="selectedBadQuestion != 'Question1'">
                    <input type="text" id="badFeedback1" [value]="badFeedback1" name="badFeedback1" placeholder="Answer Here" />
                  </div>
                  <label class="feedback-label">
                    <input type="radio" name="badFeedback" [value]="badFeedback"
                      on="change:AMP.setState({selectedBadQuestion: 'Question2'})" /> Question 2
                  </label>
                  <div class="feedback-input" hidden [hidden]="selectedBadQuestion != 'Question2'">
                    <input type="text" id="badFeedback2" name="badFeedback2" placeholder="Answer Here" [value]="badFeedback2"  />
                  </div>
                </div>
              </div>
            </div>
          <!-- Please give feedback on our brand. -->
            <div class="btn-wrap">
              <button type="submit" class="submit" on="tap:AMP.setState({showSuccess: true})">Submit</button>
            </div>
          </div>
        </form>
      </div>
    </div>
    <!-- <script type="application/json" id="amp-state">
{
"showSuccess": false,
"feedbackType": ""
}
</script> -->
    <footer class="footer">
      <ul class="media-logo-list">
        <li class="logo-item">
          <a href="https://www.google.co.in/" class="logo-link">
            <amp-img layout="responsive"
              src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/AMP-FORM/b-insta.png" alt="instagram"
              class="media-logo" width="34" height="34"></amp-img>
          </a>
        </li>
        <li class="logo-item">
          <a href="https://www.google.co.in/" class="logo-link">
            <amp-img layout="responsive"
              src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/AMP-FORM/b-fb.png" alt="facebook"
              class="media-logo" width="34" height="34"></amp-img>
          </a>
        </li>
        <li class="logo-item">
          <a href="https://www.google.co.in/" class="logo-link">
            <amp-img layout="responsive"
              src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/AMP-FORM/b-x.png" alt="x"
              class="media-logo" width="34" height="34"></amp-img>
          </a>
        </li>
      </ul>
      <p class="f-desc">
        This is just the beginning—count on us to support you every step. Welcome to the [community/family/team]!
      </p>
      <p class="f-desc">
        To stop receiving these emails, <a href="https://google.com"
          style="color:#1E1E1E;font-weight:bold;text-decoration:none;">unsubscribe here</a>
      </p>
    </footer>
  </div>
</body>
</html>
```

</details>

## EMI Calculator

This AMP template offers users an embedded calculator directly within the email, allowing them to input loan details and instantly view their EMI (Equated Monthly Installment) amount, without needing to leave the inbox. This interactive feature enhances the user journey by making decision-making quicker, simpler, and more engaging.

<details>

<summary>Expand to know more about the template.</summary>

### Use Case Examples

- Promote new loan or credit products with an embedded EMI estimator.
- Assist users in planning repayments based on tenure and interest rate.
- Offer personalized finance tools in engagement campaigns.
- Support comparison scenarios between multiple loan products.

### Template Customization Options

- Find the SRC attribute in the code
- Update Banner/Product Images
- Update Call-To-Actions (CTAs)
- Update Links in the Header/Footer
- Change the Theme or Background Color
- Update Social Media Links and Download Links

### Template Code

```html
<!DOCTYPE html>
<html ⚡4email data-css-strict>
<head>
  <meta charset="utf-8">
  <script async src="https://cdn.ampproject.org/v0.js"></script>
  <script async custom-element="amp-form" src="https://cdn.ampproject.org/v0/amp-form-0.1.js"></script>
  <script async custom-element="amp-bind" src="https://cdn.ampproject.org/v0/amp-bind-0.1.js"></script>
  <style amp4email-boilerplate>
    body {
      visibility: hidden
    }
  </style>
  <style amp-custom>
    * {
      margin: 0;
      padding: 0;
    }
    body {
      font-family: "Helvetica", arial, sans-serif;
      font-weight: 400;
      background-color: #f5f5f5;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
    }
    img {
      width: 100%;
      height: 100%;
      object-fit: contain;
    }
    /* Change Theme */
    .main {
      width: 100%;
      max-width: 600px;
      overflow: hidden;
      margin: 0 auto;
      background: #f5f5f5;
      flex: 1;
    }
    /* Change Theme */
    @media only screen and (max-width: 400px) {
      .main {
        max-width: 100%;
      }
    }
    .logo-wrap {
      padding: 12px 24px;
      background-color: #F5F5F5;
      border-radius: 0 0 41px 41px;
      text-align: center;
      z-index: 2;
      position: relative;
    }
    .logo-wrap .img-wrap {
      max-width: 145.78px;
      max-height: 74.89px;
    }
    .footer {
      width: 90%;
      margin: 45px auto 0;
      background: #ffffff;
      border-radius: 24px 24px 0 0;
      background-color: #ffffff;
      padding: 1px 0 33px;
    }
    .media-logo-list {
      display: flex;
      justify-content: center;
      align-items: center;
      list-style: none;
      gap: 16px;
      margin: 32px 0 17px;
    }
    .media-logo-list .logo-item {
      width: 20px;
      height: 20px;
    }
    .media-logo-list .logo-item .logo-link {
      width: 100%;
      height: 100%;
      display: inline-block;
    }
    .f-desc {
      font-size: 12px;
      font-weight: 400;
      line-height: 20px;
      color: #6f6f6f;
      text-align: center;
      max-width: 95%;
      margin: 0 auto;
      text-transform: uppercase;
    }
    .banner {
      margin: -35px;
    }
    .banner .img-wrap {
      max-height: 381px;
      width: 100%;
    }
    .calculator-wrap {
      width: 90%;
      position: relative;
      border-radius: 24px;
      background-color: #ffffff;
      margin: -62px auto 0;
    }
    .calculator-wrap .form-wrap {
      padding: 24px 26px 40px;
    }
    .form-wrap .text {
      font-size: 20px;
      line-height: 28px;
      font-weight: 400;
      color: #3D3D3D;
      align-items: center;
    }
    .form-wrap .calculator-title {
      padding: 8px 0 32px;
      font-size: 32px;
      font-weight: 400;
      line-height: 38px;
    }
    .form-wrap .calculator-title span {
      color: #4140FF;
    }
    .form-wrap label,
    .question h2 {
      display: block;
      padding-bottom: 13px;
      font-size: 16px;
      font-weight: 400;
      line-height: 20px;
    }
    .field-wrap .answer {
      margin-bottom: 32px;
    }
    .field-wrap .input-wrap {
      border-radius: 79px;
      border: 0.82px solid #5a5959;
      padding: 15px;
    }
    .form-wrap input,
    .input-style {
      width: 95%;
      text-indent: 5px;
      color: #000000;
      font-size: 16px;
      line-height: 23px;
      border: 0;
      outline: 0;
    }
    .form-wrap button,
    .button {
      width: 100%;
      border-radius: 50px;
      padding: 13px;
      background: #3e3cf9;
      color: #ffffff;
      font-weight: 400;
      font-size: 16px;
      line-height: 23px;
      border: 0.82px solid #5a5959;
      text-decoration: none;
      text-align: center;
      display: block;
      text-transform: uppercase;
    }
    .form-wrap button:disabled,
    .disabled {
      background: #D8D8FE;
    }
    .calculator-wrap .result-wrap {
      padding: 64px 0 0;
    }
    .result-wrap .result-title {
      padding: 0 0 12px;
      font-size: 32px;
      font-weight: 400;
      line-height: 38px;
    }
    .result-wrap .result-output {
      display: flex;
      justify-content: space-between;
      max-width: 464px;
      height: 76px;
      align-items: center;
      border-radius: 0 0 41px 41px;
      border-bottom: 0.82px solid #5a5959;
      margin-bottom: 29px;
      padding: 0 22px;
    }
    .result-output .total-text {
      font-size: 16px;
      font-weight: 400;
      line-height: 19.36px;
      text-align: center;
    }
    .result-output .total-value {
      font-size: 24px;
      font-weight: 400;
      line-height: 29.05px;
      text-align: center;
    }
    .result-wrap button {
      width: 100%;
      border-radius: 79.98px;
      padding: 13px;
      background: #3e3cf9;
      color: #ffffff;
      font-weight: 400;
      font-size: 16px;
      line-height: 23px;
      border: 0.82px solid #5a5959;
      margin-bottom: 11px;
      cursor: pointer;
    }
    .result-wrap button.disabled,
    .result-wrap button:disabled,
    .result-wrap .button.disabled,
    .result-wrap .button:disabled {
      opacity: 0.5;
    }
    @media only screen and (max-width: 480px) {
      .logo-wrap .img-wrap {
        max-width: 130px;
        max-height: 60px;
      }
      .form-wrap input,
      .input-style {
        width: 90%;
      }
      .calculator-wrap .form-wrap {
        padding: 20px 20px 40px;
      }
      .calculator-wrap .result-wrap {
        padding: 40px 0 0;
      }
      .result-wrap .result-title {
        font-size: 25px;
        line-height: 30px;
      }
      .form-wrap .calculator-title {
        padding: 8px 0 25px;
        font-size: 25px;
        line-height: 30px;
      }
      .field-wrap .input-wrap {
        padding: 10px;
      }
      .form-wrap .text {
        font-size: 15px;
        line-height: 20px;
      }
      .result-output .total-value {
        font-size: 20px;
        line-height: 24px;
      }
      .result-wrap .result-output {
        padding: 20px 15px;
        height: auto;
      }
      .form-wrap .question {
        padding-bottom: 8px;
      }
    }
    @media only screen and (max-width: 300px) {
      .product-wrap {
        padding: 40px 5px 20px;
      }
    }
  </style>
</head>
<body>
  <div class="main">
    <header>
      <div class="logo-wrap">
        <div class="img-wrap">
          <!-- Change Logo Image src as per your requirements -->
          <amp-img layout="responsive"
            src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/SIP-Calculator/CleverTap%202.png" alt="Logo"
            width="159" height="73" />
          <!-- Change Logo Image src as per your requirements -->
        </div>
      </div>
    </header>
    <div class="banner">
      <div class="img-wrap">
        <!-- Change Banner Image src as per your requirements -->
        <amp-img layout="responsive"
          src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/SIP-Calculator/stacks-coins-arranged-bar-graph%201.png"
          alt="Banner" width="600" height="381"></amp-img>
        <!-- Change Banner Image src as per your requirements -->
      </div>
    </div>
    <div class="calculator-wrap">
      <div on="tap:AMP.setState({
          formxo5j8158: {
              fuuid: formxo5j8158.fuuid || floor(random() * 100000),
              responses: {
          stepra77z1:{
                      elementzzr6o10:elementzzr6o10Formula(formxo5j8158.responses.stepv119k145.element232766,formxo5j8158.responses.stepv119k145.elementaa3vl4,formxo5j8158.responses.stepv119k145.elementst0oh2)
                  }
      }
          }
      })" role="tab" tabindex="1" class="form-wrap amp-form-block amp-html-block formxo5j8158-wrapper"
        style="margin:auto;text-align:left">
        <div class="data"><amp-state id="formxo5j8158">
            <script type="application/json">{"currentStep":"stepv119k145","responses":{},"formHistory":[]}</script>
          </amp-state></div>
        <p class="text">Present</p>
        <h2 class="calculator-title">
          EMI Investment <span> Calculator </span>
        </h2>
        <form id="formWidgetFallbackAnchorLinkformxo5j8158" class="formxo5j8158"
          style="display:flex;flex-direction:column" method="post" custom-validation-reporting="show-all-on-submit" on="submit:AMP.setState({formxo5j8158:{formHistory: formxo5j8158.formHistory.splice(formxo5j8158.formHistory.length,0,formxo5j8158.currentStep) 
          , currentStep: &apos;stepra77z1&apos;}})" action-xhr="">
          <div class="overall screen current_screen" style="box-sizing:border-box">
            <div class="element-wrapper field-wrap">
              <div class="question">
                <h2>Principal Amount</h2>
              </div>
              <div class="answer">
                <div class="input-outer input-wrap" style="display:flex;flex-direction:row; align-items: center;">
                  <span class="prefix">$ </span>
                  <input class="input-style" required type="number" name="PrincipalAmount" id="elementst0oh2"
                    placeholder="Enter your Principal Amount" style="box-sizing:border-box"
                    [value]="formxo5j8158.responses.stepv119k145.elementst0oh2 || &apos;&apos;"
                    pattern="[-]?[\d\.]{0,200}" on="input-throttled:AMP.setState({formxo5j8158:{
                  responses: {stepv119k145:{elementst0oh2: event.value}}}})">
                </div>
                <div visible-when-invalid="valueMissing" style="font-size:13px;padding-top:4px"
                  validation-for="elementst0oh2">This field is required</div>
                <div visible-when-invalid="patternMismatch" validation-for="elementst0oh2"
                  style="font-size:13px;margin-top:4px">Please enter a number of length 0 - 200 digits</div>
                <div visible-when-invalid="badInput" style="font-size:13px;margin-top:4px"
                  validation-for="elementst0oh2">Invalid input, number expected</div>
              </div>
            </div>
            <div class="element-wrapper field-wrap">
              <div class="question">
                <h2>Interest Rate (in %)</p>
              </div>
              <div class="answer">
                <div class="input-outer input-wrap" style="display:flex;flex-direction:column">
                  <input class="input-style" required type="number" name="InterestRate" id="elementaa3vl4"
                    placeholder="Annual rate of interest" style="box-sizing:border-box"
                    [value]="formxo5j8158.responses.stepv119k145.elementaa3vl4 || &apos;&apos;"
                    pattern="[-]?[\d\.]{0,200}" on="input-throttled:AMP.setState({formxo5j8158:{
                  responses: {stepv119k145:{elementaa3vl4: event.value}}}})">
                </div>
                <div visible-when-invalid="valueMissing" style="font-size:13px;padding-top:4px"
                  validation-for="elementaa3vl4">This field is required</div>
                <div visible-when-invalid="patternMismatch" validation-for="elementaa3vl4"
                  style="font-size:13px;margin-top:4px">Please enter a number of length 0 - 200 digits</div>
                <div visible-when-invalid="badInput" style="font-size:13px;margin-top:4px"
                  validation-for="elementaa3vl4">Invalid input, number expected</div>
              </div>
            </div>
            <div class="element-wrapper field-wrap">
              <div class="question">
                <h2>Loan Tenure ( in Years )</h2>
              </div>
              <div class="answer">
                <div class="input-outer input-wrap" style="display:flex;flex-direction:column">
                  <input class="input-style" required type="number" name="LoanTenure" id="element232766"
                    placeholder="In years" style="box-sizing:border-box"
                    [value]="formxo5j8158.responses.stepv119k145.element232766 || &apos;&apos;"
                    pattern="[-]?[\d\.]{0,200}" on="input-throttled:AMP.setState({formxo5j8158:{
                  responses: {stepv119k145:{element232766: event.value}}}})">
                </div>
                <div visible-when-invalid="valueMissing" style="font-size:13px;padding-top:4px"
                  validation-for="element232766">This field is required</div>
                <div visible-when-invalid="patternMismatch" validation-for="element232766"
                  style="font-size:13px;margin-top:4px">Please enter a number of length 0 - 200 digits</div>
                <div visible-when-invalid="badInput" style="font-size:13px;margin-top:4px"
                  validation-for="element232766">Invalid input, number expected</div>
              </div>
            </div>
            <input hidden id="fuuid" name="fuuid" [value]="formxo5j8158.fuuid"> <input hidden id="next-step-id"
              name="next-step-id" [value]="&apos;stepra77z1&apos;"> <input hidden id="total-steps" name="total-steps"
              value="3">
            <div class="navigation-button-wrapper">
              <!-- Change CTA-->
              <button class="button" type="submit">
                <p>Calculate EMI</p>
              </button>
              <!-- Change CTA-->
            </div>
          </div>
        </form>
        <form id="formWidgetFallbackAnchorLinkformxo5j8158" class="formxo5j8158 result-wrap"
          style="display:flex;flex-direction:column" method="post" custom-validation-reporting="show-all-on-submit"
          on="submit-success:AMP.setState({formxo5j8158:{currentStep: &apos;success&apos;}})"
          action-xhr="">
          <div class="overall screen current_screen" style="box-sizing:border-box" hidden
            [hidden]="formxo5j8158.currentStep != &apos;stepra77z1&apos;">
            <div class="element-wrapper field-wrap">
              <div class="question"></div>
              <div class="answer">
                <amp-bind-macro id="elementzzr6o10Formula" arguments="element232766,elementaa3vl4,elementst0oh2"
                  expression="((((+elementst0oh2 * (+elementaa3vl4 / 1200)) * pow((1 + (+elementaa3vl4 / 1200)), (+element232766 * 12))) / (pow((1 + (+elementaa3vl4 / 1200)), (+element232766 * 12)) - 1)) || 0).toFixed(2)"></amp-bind-macro>
                <h2 class="result-title">Result</h2>
                <div class="result-output">
                  <h3 class="total-text">EMI Per Month</h3>
                  <input hidden id="elementzzr6o10" name="elementzzr6o10"
                    [value]="elementzzr6o10Formula(formxo5j8158.responses.stepv119k145.element232766,formxo5j8158.responses.stepv119k145.elementaa3vl4,formxo5j8158.responses.stepv119k145.elementst0oh2)">
                  <span class="formula-result total-value"
                    [text]="elementzzr6o10Formula(formxo5j8158.responses.stepv119k145.element232766,formxo5j8158.responses.stepv119k145.elementaa3vl4,formxo5j8158.responses.stepv119k145.elementst0oh2)">0</span>
                </div>
              </div>
            </div>
            <input hidden id="fuuid" name="fuuid" [value]="formxo5j8158.fuuid"> <input hidden id="next-step-id"
              name="next-step-id" [value]="&apos;success&apos;"> <input hidden id="total-steps" name="total-steps"
              value="3">
            <div class="navigation-button-wrapper">
              <button class="button" type="submit">
                Go to website
              </button>
              <button class="button" type="button" on="tap:AMP.setState({
                formxo5j8158: {
                  responses: {
                    stepv119k145: {
                      elementst0oh2: '',
                      elementaa3vl4: '',
                      element232766: ''
                    }
                  },
                  currentStep: 'stepv119k145'
                }
              })">
                Calculate AGAIN
              </button>
            </div>
          </div>
        </form>
      </div>
    </div>
    <!-- Footer Section -->
    <footer class="footer">
      <ul class="media-logo-list">
        <!-- Footer Link -->
        <!-- Social Links -->
        <li class="logo-item">
          <a href="https://www.google.co.in/" class="logo-link">
            <amp-img layout="responsive"
              src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/SIP-Calculator/insta.png" alt="instagram"
              class="media-logo" width="20" height="20"></amp-img>
          </a>
        </li>
        <li class="logo-item">
          <a href="https://www.google.co.in/" class="logo-link">
            <amp-img layout="responsive"
              src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/SIP-Calculator/facebook.png" alt="facebook"
              class="media-logo" width="20" height="20"></amp-img>
          </a>
        </li>
        <li class="logo-item">
          <a href="https://www.google.co.in/" class="logo-link">
            <amp-img layout="responsive"
              src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/SIP-Calculator/x.png" alt="x"
              class="media-logo" width="20" height="20"></amp-img>
          </a>
        </li>
        <!-- Social Links -->
        <!-- Footer Link -->
      </ul>
      <p class="f-desc">
        is simply dummy text of the printing and typesetting is simply dummy text of the printing and typesetting
        industry.g industry.
      </p>
      <p class="f-desc" style="margin-top: 50px;">To stop receiving these emails, <a href="#"
          style="color:#1E1E1E;font-weight:bold;text-decoration:none;">unsubscribe here</a></p>
    </footer>
  </div>
</body>
</html>
```

</details>

## SIP Calculator

This AMP template allows users to calculate the potential returns of their Systematic Investment Plan (SIP) right within the email. By entering basic investment details such as monthly contribution, duration, and expected return rate, users get instant projections, creating a smooth, informative experience that supports smarter financial decisions.

<details>

<summary>Expand to know more about the template.</summary>

### Use Case Examples

- Educate users about SIP benefits while promoting mutual fund products.
- Encourage investment planning by allowing quick in-email projections.
- Enable financial goal-based marketing through interactive calculators.
- Re-engage users by helping them visualize long-term returns.

### Template Customization Options

- Replace the Logo
- Update Banner/Product Images
- Update Call-To-Actions (CTAs)
- Update Links in the Header/Footer
- Change the Theme or Background Color
- Update Social Media Links and Download Links

### Template Code

```html
<!DOCTYPE html>
<html ⚡4email data-css-strict>
<head>
  <meta charset="utf-8">
  <script async src="https://cdn.ampproject.org/v0.js"></script>
  <script async custom-element="amp-form" src="https://cdn.ampproject.org/v0/amp-form-0.1.js"></script>
  <script async custom-element="amp-bind" src="https://cdn.ampproject.org/v0/amp-bind-0.1.js"></script>
  <style amp4email-boilerplate>
    body {
      visibility: hidden
    }
  </style>
  <style amp-custom>
    * {
      margin: 0;
      padding: 0;
    }
    body {
      font-family: "Helvetica", arial, sans-serif;
      font-weight: 400;
      background-color: #f5f5f5;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
    }
    img {
      width: 100%;
      height: 100%;
      object-fit: contain;
    }
    /* Change Theme */
    .main {
      width: 100%;
      max-width: 600px;
      overflow: hidden;
      margin: 0 auto;
      background: #f5f5f5;
      flex: 1;
    }
    /* Change Theme */
    @media only screen and (max-width: 400px) {
      .main {
        max-width: 100%;
      }
    }
    .logo-wrap {
      padding: 12px 24px;
      background-color: #F5F5F5;
      border-radius: 0 0 41px 41px;
      text-align: center;
      z-index: 2;
      position: relative;
    }
    .logo-wrap .img-wrap {
      max-width: 145.78px;
      max-height: 74.89px;
    }
    .footer {
      width: 90%;
      margin: 45px auto 0;
      background: #ffffff;
      border-radius: 24px 24px 0 0;
      background-color: #ffffff;
      padding: 1px 0 33px;
    }
    .media-logo-list {
      display: flex;
      justify-content: center;
      align-items: center;
      list-style: none;
      gap: 16px;
      margin: 32px 0 17px;
    }
    .media-logo-list .logo-item {
      width: 20px;
      height: 20px;
    }
    .media-logo-list .logo-item .logo-link {
      width: 100%;
      height: 100%;
      display: inline-block;
    }
    .f-desc {
      font-size: 12px;
      font-weight: 400;
      line-height: 20px;
      color: #6f6f6f;
      text-align: center;
      max-width: 95%;
      margin: 0 auto;
      text-transform: uppercase;
    }
    .banner {
      margin: -35px;
    }
    .banner .img-wrap {
      max-height: 381px;
      width: 100%;
    }
    .calculator-wrap {
      width: 90%;
      position: relative;
      border-radius: 24px;
      background-color: #ffffff;
      margin: -62px auto 0;
    }
    .calculator-wrap .form-wrap {
      padding: 24px 26px 40px;
    }
    .form-wrap .text {
      font-size: 20px;
      line-height: 28px;
      font-weight: 400;
      color: #3D3D3D;
      align-items: center;
    }
    .form-wrap .calculator-title {
      padding: 8px 0 32px;
      font-size: 32px;
      font-weight: 400;
      line-height: 38px;
    }
    .form-wrap .calculator-title span {
      color: #4140FF;
    }
    .form-wrap label,
    .question h2 {
      display: block;
      padding-bottom: 13px;
      font-size: 16px;
      font-weight: 400;
      line-height: 20px;
    }
    .field-wrap .answer {
      margin-bottom: 32px;
    }
    .field-wrap .input-wrap {
      border-radius: 79px;
      border: 0.82px solid #5a5959;
      padding: 15px;
    }
    .form-wrap input,
    .input-style {
      width: 95%;
      text-indent: 5px;
      color: #000000;
      font-size: 16px;
      line-height: 23px;
      border: 0;
      outline: 0;
    }
    .form-wrap button,
    .button {
      width: 100%;
      border-radius: 50px;
      padding: 13px;
      background: #3e3cf9;
      color: #ffffff;
      font-weight: 400;
      font-size: 16px;
      line-height: 23px;
      border: 0.82px solid #5a5959;
      text-decoration: none;
      text-align: center;
      display: block;
      text-transform: uppercase;
    }
    .form-wrap button:disabled,
    .disabled {
      background: #D8D8FE;
    }
    .calculator-wrap .result-wrap {
      padding: 64px 0 0;
    }
    .result-wrap .result-title {
      padding: 0 0 12px;
      font-size: 32px;
      font-weight: 400;
      line-height: 38px;
    }
    .result-wrap .result-output {
      display: flex;
      justify-content: space-between;
      max-width: 464px;
      height: 76px;
      align-items: center;
      border-radius: 0 0 41px 41px;
      border-bottom: 0.82px solid #5a5959;
      margin-bottom: 29px;
      padding: 0 22px;
    }
    .result-output .total-text {
      font-size: 16px;
      font-weight: 400;
      line-height: 19.36px;
      text-align: center;
    }
    .result-output .total-value {
      font-size: 24px;
      font-weight: 400;
      line-height: 29.05px;
      text-align: center;
    }
    .result-wrap button {
      width: 100%;
      border-radius: 79.98px;
      padding: 13px;
      background: #3e3cf9;
      color: #ffffff;
      font-weight: 400;
      font-size: 16px;
      line-height: 23px;
      border: 0.82px solid #5a5959;
      margin-bottom: 11px;
      cursor: pointer;
    }
    .result-wrap button.disabled,
    .result-wrap button:disabled,
    .result-wrap .button.disabled,
    .result-wrap .button:disabled {
      opacity: 0.5;
    }
    @media only screen and (max-width: 480px) {
      .logo-wrap .img-wrap {
        max-width: 130px;
        max-height: 60px;
      }
      .form-wrap input,
      .input-style {
        width: 90%;
      }
      .calculator-wrap .form-wrap {
        padding: 20px 20px 40px;
      }
      .calculator-wrap .result-wrap {
        padding: 40px 0 0;
      }
      .result-wrap .result-title {
        font-size: 25px;
        line-height: 30px;
      }
      .form-wrap .calculator-title {
        padding: 8px 0 25px;
        font-size: 25px;
        line-height: 30px;
      }
      .field-wrap .input-wrap {
        padding: 10px;
      }
      .form-wrap .text {
        font-size: 15px;
        line-height: 20px;
      }
      .result-output .total-value {
        font-size: 20px;
        line-height: 24px;
      }
      .result-wrap .result-output {
        padding: 20px 15px;
        height: auto;
      }
      .form-wrap .question {
        padding-bottom: 8px;
      }
    }
    @media only screen and (max-width: 300px) {
      .product-wrap {
        padding: 40px 5px 20px;
      }
    }
  </style>
</head>
<body>
  <div class="main">
    <header>
      <div class="logo-wrap">
        <div class="img-wrap">
          <!-- Change Logo -->
          <amp-img layout="responsive"
            src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/SIP-Calculator/CleverTap%202.png" alt="Logo"
            width="159" height="73"></amp-img>
          <!-- Change Logo -->
        </div>
      </div>
    </header>
    <div class="banner">
      <div class="img-wrap">
        <!-- Change Banner -->
        <amp-img layout="responsive"
          src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/SIP-Calculator/stacks-coins-arranged-bar-graph%201.png"
          alt="Banner" width="600" height="381"></amp-img>
        <!-- Change Banner -->
      </div>
    </div>
    <div class="calculator-wrap">
      <div on="tap:AMP.setState({
        form6850m49: {
          fuuid: form6850m49.fuuid || floor(random() * 100000),
          responses: {
          stepag3y745:{
                  elementvw5q7629:elementvw5q7629Formula(form6850m49.responses.steprj7lv44.element4b6vf626,form6850m49.responses.steprj7lv44.elementhwgbp628),elementa1mgz630:elementa1mgz630Formula(form6850m49.responses.steprj7lv44.element4b6vf626,form6850m49.responses.steprj7lv44.elementhwgbp628,form6850m49.responses.steprj7lv44.elementwikv1627),element4q9av631:element4q9av631Formula(form6850m49.responses.stepag3y745.elementa1mgz630,form6850m49.responses.stepag3y745.elementvw5q7629)
              }
            }
          }
      })" role="tab" tabindex="1" class="form-wrap amp-form-block amp-html-block form6850m49-wrapper"
        style="margin:auto;text-align:left">
        <div class="data">
          <amp-state id="form6850m49">
            <script type="application/json">{"currentStep":"steprj7lv44","responses":{},"formHistory":[]}</script>
          </amp-state>
        </div>
        <p class="text">Present</p>
        <h2 class="calculator-title">SIP Investment <span> Calculator </span></h2>
        <form action-xhr="https://google.com" id="formWidgetFallbackAnchorLinkform6850m49" class="form6850m49"
          style="display:flex;flex-direction:column" method="post" custom-validation-reporting="show-all-on-submit" on="submit:AMP.setState({form6850m49:{formHistory: form6850m49.formHistory.splice(form6850m49.formHistory.length,0,form6850m49.currentStep) 
          , currentStep: &apos;stepag3y745&apos;}})">
          <div class="overall screen current_screen" style="box-sizing:border-box">
            <div class="field-wrap">
              <div class="question">
                <h2>Monthly Investment</h2>
              </div>
              <div class="answer">
                <div class="input-outer input-wrap" style="display:flex;flex-direction:row">
                  <span class="prefix">$ </span>
                  <input class="input-style" required type="number" name="element4b6vf626" id="element4b6vf626"
                    placeholder="Your total monthly investment" style="box-sizing:border-box"
                    [value]="form6850m49.responses.steprj7lv44.element4b6vf626 || &apos;&apos;"
                    pattern="[-]?[\d\.]{0,200}" on="input-throttled:AMP.setState({form6850m49:{
                  responses: {steprj7lv44:{element4b6vf626: event.value}}}})">
                </div>
                <div visible-when-invalid="valueMissing" style="font-size:13px;padding-top:4px"
                  validation-for="element4b6vf626">This field is required</div>
                <div visible-when-invalid="patternMismatch" validation-for="element4b6vf626"
                  style="font-size:13px;margin-top:4px">Please enter a number of length 0 - 200 digits</div>
                <div visible-when-invalid="badInput" style="font-size:13px;margin-top:4px"
                  validation-for="element4b6vf626">Invalid input, number expected</div>
              </div>
            </div>
            <div class="field-wrap">
              <div class="question">
                <h2>Rate of Return ( in % )</h2>
              </div>
              <div class="answer">
                <div class="input-outer input-wrap" style="display:flex;flex-direction:column">
                  <input class="input-style" required type="number" name="elementwikv1627" id="elementwikv1627"
                    placeholder="Annual Rate of Interest" style="box-sizing:border-box"
                    [value]="form6850m49.responses.steprj7lv44.elementwikv1627 || &apos;&apos;"
                    pattern="[-]?[\d\.]{0,200}" on="input-throttled:AMP.setState({form6850m49:{
                  responses: {steprj7lv44:{elementwikv1627: event.value}}}})">
                </div>
                <div visible-when-invalid="valueMissing" style="font-size:13px;padding-top:4px"
                  validation-for="elementwikv1627">This field is required</div>
                <div visible-when-invalid="patternMismatch" validation-for="elementwikv1627"
                  style="font-size:13px;margin-top:4px">Please enter a number of length 0 - 200 digits</div>
                <div visible-when-invalid="badInput" style="font-size:13px;margin-top:4px"
                  validation-for="elementwikv1627">Invalid input, number expected</div>
              </div>
            </div>
            <div class="field-wrap">
              <div class="question">
                <h2>Investment Duration</h2>
              </div>
              <div class="answer">
                <div class="input-outer input-wrap" style="display:flex;flex-direction:column"><input
                    class="input-style" required type="number" name="elementhwgbp628" id="elementhwgbp628"
                    placeholder="In years" style="box-sizing:border-box"
                    [value]="form6850m49.responses.steprj7lv44.elementhwgbp628 || &apos;&apos;"
                    pattern="[-]?[\d\.]{0,200}" on="input-throttled:AMP.setState({form6850m49:{
                  responses: {steprj7lv44:{elementhwgbp628: event.value}}}})"></div>
                <div visible-when-invalid="valueMissing" style="font-size:13px;padding-top:4px"
                  validation-for="elementhwgbp628">This field is required</div>
                <div visible-when-invalid="patternMismatch" validation-for="elementhwgbp628"
                  style="font-size:13px;margin-top:4px">Please enter a number of length 0 - 200 digits</div>
                <div visible-when-invalid="badInput" style="font-size:13px;margin-top:4px"
                  validation-for="elementhwgbp628">Invalid input, number expected</div>
              </div>
            </div>
            <input hidden id="fuuid" name="fuuid" [value]="form6850m49.fuuid"> <input hidden id="next-step-id"
              name="next-step-id" [value]="&apos;stepag3y745&apos;"> <input hidden id="total-steps" name="total-steps"
              value="3">
            <div class="navigation-button-wrapper">
              <!-- Change CTA -->
              <button class="button" type="submit">
                <p>Calculate SIP</p>
              </button>
              <!-- Change CTA -->
            </div>
          </div>
        </form>
        <form action-xhr="https://google.com" id="formWidgetFallbackAnchorLinkform6850m49" class="form6850m49"
          style="display:flex;flex-direction:column" method="post" custom-validation-reporting="show-all-on-submit"
          on="submit-success:AMP.setState({form6850m49:{currentStep: &apos;success&apos;}})">
          <div class="result-wrap" style="box-sizing:border-box" hidden
            [hidden]="form6850m49.currentStep != &apos;stepag3y745&apos;">
            <h2 class="result-title">Result</h2>
            <div class="element-wrapper">
              <div class="answer"><amp-bind-macro id="elementvw5q7629Formula"
                  arguments="element4b6vf626,elementhwgbp628"
                  expression="(((+element4b6vf626 * +elementhwgbp628) * 12) || 0).toFixed(2)"></amp-bind-macro>
                <div class="result-output"><span class="formula-sub-heading">
                    <p>Total Investment</p>
                  </span><input hidden id="elementvw5q7629" name="elementvw5q7629"
                    [value]="elementvw5q7629Formula(form6850m49.responses.steprj7lv44.element4b6vf626,form6850m49.responses.steprj7lv44.elementhwgbp628)">
                  <span class="formula-result total-value" style="font-family:Helvetica,Helvetica"
                    [text]="elementvw5q7629Formula(form6850m49.responses.steprj7lv44.element4b6vf626,form6850m49.responses.steprj7lv44.elementhwgbp628)">0</span>
                </div>
              </div>
            </div>
            <div class="element-wrapper">
              <div class="answer"><amp-bind-macro id="elementa1mgz630Formula"
                  arguments="element4b6vf626,elementhwgbp628,elementwikv1627"
                  expression="(((+element4b6vf626 * ((pow((1 + (+elementwikv1627 / 1200)), ((12 * +elementhwgbp628) + 1)) - 1) / (+elementwikv1627 / 1200))) - +element4b6vf626) || 0).toFixed(2)"></amp-bind-macro>
                <div class="result-output"><span class="formula-sub-heading">
                    <p>Total Maturity Amount</p>
                  </span><input hidden id="elementa1mgz630" name="elementa1mgz630"
                    [value]="elementa1mgz630Formula(form6850m49.responses.steprj7lv44.element4b6vf626,form6850m49.responses.steprj7lv44.elementhwgbp628,form6850m49.responses.steprj7lv44.elementwikv1627)">
                  <span class="formula-result total-value" style="font-family:Helvetica,Helvetica"
                    [text]="elementa1mgz630Formula(form6850m49.responses.steprj7lv44.element4b6vf626,form6850m49.responses.steprj7lv44.elementhwgbp628,form6850m49.responses.steprj7lv44.elementwikv1627)">0</span>
                </div>
              </div>
            </div>
            <div class="element-wrapper">
              <div class="answer"><amp-bind-macro id="element4q9av631Formula"
                  arguments="elementa1mgz630,elementvw5q7629"
                  expression="((+elementa1mgz630 - +elementvw5q7629) || 0).toFixed(2)"></amp-bind-macro>
                <div class="result-output"><span class="formula-sub-heading">
                    <p>Interest Earned</p>
                  </span><input hidden id="element4q9av631" name="element4q9av631"
                    [value]="element4q9av631Formula(form6850m49.responses.stepag3y745.elementa1mgz630,form6850m49.responses.stepag3y745.elementvw5q7629)">
                  <span class="formula-result total-value" style="font-family:Helvetica,Helvetica"
                    [text]="element4q9av631Formula(form6850m49.responses.stepag3y745.elementa1mgz630,form6850m49.responses.stepag3y745.elementvw5q7629)">0</span>
                </div>
              </div>
            </div><input hidden id="fuuid" name="fuuid" [value]="form6850m49.fuuid"> <input hidden id="next-step-id"
              name="next-step-id" [value]="&apos;success&apos;"> <input hidden id="total-steps" name="total-steps"
              value="3">
            <div class="navigation-button-wrapper">
              <button class="button" type="submit">
                Go to website
              </button>
              <button class="button" type="button" on="tap:AMP.setState({
                    form6850m49: {
                      responses: {
                        steprj7lv44: {
                          element4b6vf626: '',
                          elementwikv1627: '',
                          elementhwgbp628: ''
                        }
                      },
                      currentStep: 'steprj7lv44'
                    }
                  })">
                Calculate AGAIN
              </button>
            </div>
          </div>
        </form>
      </div>
    </div>
    <!-- Footer Section -->
    <footer class="footer">
      <ul class="media-logo-list">
        <!-- Footer Link -->
        <!-- Social Links -->
        <li class="logo-item"><a href="https://www.google.co.in/" class="logo-link"><amp-img layout="responsive"
              src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/SIP-Calculator/insta.png" alt="instagram"
              class="media-logo" width="20" height="20"></amp-img></a></li>
        <li class="logo-item"><a href="https://www.google.co.in/" class="logo-link"><amp-img layout="responsive"
              src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/SIP-Calculator/facebook.png" alt="facebook"
              class="media-logo" width="20" height="20"></amp-img></a></li>
        <li class="logo-item"><a href="https://www.google.co.in/" class="logo-link"><amp-img layout="responsive"
              src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/SIP-Calculator/x.png" alt="x"
              class="media-logo" width="20" height="20"></amp-img></a></li>
        <!-- Footer Link -->
      <!-- Social Links -->
      </ul>
      <p class="f-desc">is simply dummy text of the printing and typesetting is simply dummy text of the printing and
        typesetting industry.g industry.</p>
      <p class="f-desc" style="margin-top: 50px;">To stop receiving these emails, <a href="#"
          style="color:#1E1E1E;font-weight:bold;text-decoration:none;">unsubscribe here</a></p>
    </footer>
    <!-- Footer Section -->
  </div>
</body>
</html>
```

</details>

## Insurance Calculator

This AMP template empowers users to estimate insurance premiums based on parameters such as coverage amount, age, and policy term right within their inbox. It also enables users to explore coverage options and assess affordability instantly, making the research and decision-making process much more convenient and personalized.

<details>

<summary>Expand to know more about the template.</summary>

### Use Case Examples

- Promote insurance plans with embedded quote estimators.
- Help users calculate premiums before applying for a policy.
- Improve lead conversion by reducing drop-offs during research.

### Template Customization Options

- Replace the Logo
- Update Banner/Product Images
- Update Call-To-Actions (CTAs)
- Update Links in the Header/Footer
- Change the Theme or Background Color
- Update Social Media and Download Links

### Template Code

```html
<!DOCTYPE html>
<html ⚡4email data-css-strict>
<head>
  <meta charset="utf-8">
  <script async src="https://cdn.ampproject.org/v0.js"></script>
  <script async custom-element="amp-form" src="https://cdn.ampproject.org/v0/amp-form-0.1.js"></script>
  <script async custom-element="amp-bind" src="https://cdn.ampproject.org/v0/amp-bind-0.1.js"></script>
  <script async custom-element="amp-selector" src="https://cdn.ampproject.org/v0/amp-selector-0.1.js"></script>
  <style amp4email-boilerplate>
    body {
      visibility: hidden
    }
  </style>
  <style amp-custom>
    * {
      margin: 0;
      padding: 0;
    }
    body {
      font-family: "Helvetica", arial, sans-serif;
      font-weight: 400;
      background-color: #f5f5f5;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
    }
    img {
      width: 100%;
      height: 100%;
      object-fit: contain;
    }
    /* Change Theme */
    .main {
      width: 100%;
      max-width: 600px;
      overflow: hidden;
      margin: 0 auto;
      background: #f5f5f5;
      flex: 1;
    }
    /* Change Theme */
    @media only screen and (max-width: 400px) {
      .main {
        max-width: 100%;
      }
    }
    .logo-wrap {
      padding: 12px 24px;
      background-color: #F5F5F5;
      border-radius: 0 0 41px 41px;
      text-align: center;
      z-index: 2;
      position: relative;
    }
    .logo-wrap .img-wrap {
      max-width: 145.78px;
      max-height: 74.89px;
    }
    .footer {
      width: 90%;
      margin: 45px auto 0;
      background: #ffffff;
      border-radius: 24px 24px 0 0;
      background-color: #ffffff;
      padding: 1px 0 33px;
    }
    .media-logo-list {
      display: flex;
      justify-content: center;
      align-items: center;
      list-style: none;
      gap: 16px;
      margin: 32px 0 17px;
    }
    .media-logo-list .logo-item {
      width: 20px;
      height: 20px;
    }
    .media-logo-list .logo-item .logo-link {
      width: 100%;
      height: 100%;
      display: inline-block;
    }
    .f-desc {
      font-size: 12px;
      font-weight: 400;
      line-height: 20px;
      color: #6f6f6f;
      text-align: center;
      max-width: 95%;
      margin: 0 auto;
      text-transform: uppercase;
    }
    .banner {
      margin: -35px;
    }
    .banner .img-wrap {
      max-height: 381px;
      width: 100%;
    }
    .calculator-wrap {
      width: 90%;
      position: relative;
      border-radius: 24px;
      background-color: #ffffff;
      margin: -62px auto 0;
    }
    .calculator-wrap .form-wrap {
      padding: 24px 26px 40px;
    }
    .form-wrap .text {
      font-size: 20px;
      line-height: 28px;
      font-weight: 400;
      color: #3D3D3D;
      align-items: center;
    }
    .form-wrap .calculator-title {
      padding: 8px 0 32px;
      font-size: 32px;
      font-weight: 400;
      line-height: 38px;
    }
    .form-wrap .calculator-title span {
      color: #4140FF;
    }
    .form-wrap label {
      display: block;
      padding-bottom: 13px;
      font-size: 16px;
      font-weight: 400;
      line-height: 20px;
    }
    .field-wrap {
      margin-bottom: 32px;
    }
    .field-wrap .input-wrap {
      border-radius: 79px;
      border: 0.82px solid #5a5959;
      padding: 15px;
    }
    .form-wrap input,
    .form-wrap select {
      width: 95%;
      text-indent: 5px;
      color: #000000;
      background: #ffffff;
      font-size: 16px;
      line-height: 23px;
      border: 0;
      outline: 0;
    }
    .form-wrap select option {
      margin-top: 10px;
      padding: 15px 5px;
      font-size: 16px;
      line-height: 23px;
    }
    .form-wrap button,
    .button {
      width: 100%;
      border-radius: 50px;
      padding: 13px;
      background: #3e3cf9;
      color: #ffffff;
      font-weight: 400;
      font-size: 16px;
      line-height: 23px;
      border: 0.82px solid #5a5959;
      text-decoration: none;
      text-align: center;
      display: block;
      text-transform: uppercase;
    }
    .form-wrap button:disabled,
    .disabled {
      background: #D8D8FE;
    }
    .calculator-wrap .result-wrap {
      padding: 64px 0 0;
    }
    .result-wrap .result-title {
      padding: 0 0 12px;
      font-size: 32px;
      font-weight: 400;
      line-height: 38px;
    }
    .result-wrap .result-output {
      display: flex;
      justify-content: space-between;
      max-width: 464px;
      height: 76px;
      align-items: center;
      border-radius: 0 0 41px 41px;
      border-bottom: 0.82px solid #5a5959;
      margin-bottom: 29px;
      padding: 0 22px;
    }
    .result-output .total-text {
      font-size: 16px;
      font-weight: 400;
      line-height: 19.36px;
      text-align: center;
    }
    .result-output .total-value {
      font-size: 24px;
      font-weight: 400;
      line-height: 29.05px;
      text-align: center;
    }
    .result-wrap button {
      width: 100%;
      border-radius: 79.98px;
      padding: 13px;
      background: #3e3cf9;
      color: #ffffff;
      font-weight: 400;
      font-size: 16px;
      line-height: 23px;
      border: 0.82px solid #5a5959;
      margin-bottom: 11px;
      cursor: pointer;
    }
    .result-wrap button.disabled,
    .result-wrap button:disabled {
      opacity: 0.5;
    }
    @media only screen and (max-width: 480px) {
      .result-output .total-text {
        margin-bottom: 10px;
      }
      .logo-wrap .img-wrap {
        max-width: 130px;
        max-height: 60px;
      }
      .form-wrap input {
        width: 90%;
      }
      .calculator-wrap .form-wrap {
        padding: 20px 20px 40px;
      }
      .calculator-wrap .result-wrap {
        padding: 40px 0 0;
      }
      .result-wrap .result-title {
        font-size: 25px;
        line-height: 30px;
      }
      .form-wrap .calculator-title {
        padding: 8px 0 25px;
        font-size: 25px;
        line-height: 30px;
      }
      .field-wrap .input-wrap {
        padding: 10px;
      }
      .form-wrap .text {
        font-size: 15px;
        line-height: 20px;
      }
      .result-output .total-value {
        font-size: 20px;
        line-height: 24px;
      }
      .result-wrap .result-output {
        padding: 20px 15px;
        height: auto;
        flex-wrap: wrap;
      }
      .form-wrap label {
        padding-bottom: 8px;
      }
    }
    @media only screen and (max-width: 300px) {
      .product-wrap {
        padding: 40px 5px 20px;
      }
    }
  </style>
</head>
<body>
  <div class="main">
    <header>
      <div class="logo-wrap">
        <div class="img-wrap">
          <!-- Change Logo image src as per your requirements -->
          <amp-img layout="responsive"
            src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/SIP-Calculator/CleverTap%202.png" alt="Logo"
            width="159" height="73" />
          <!-- Change Logo image src as per your requirements -->
        </div>
      </div>
    </header>
    <div class="banner">
      <div class="img-wrap">
        <!-- Change Banner image src as per your requirements -->
        <amp-img layout="responsive"
          src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/SIP-Calculator/stacks-coins-arranged-bar-graph%201.png"
          alt="Banner" width="600" height="381"></amp-img>
        <!-- Change Banner image src as per your requirements -->
      </div>
    </div>
    <div class="calculator-wrap">
      <div on="tap:AMP.setState({
            formInsuranceCalc: {
              fuuid: formInsuranceCalc.fuuid || floor(random() * 100000),
              responses: {
                stepInsuranceResult: {
                  insuranceResult: insuranceFormula(
                    formInsuranceCalc.responses.stepInsuranceInput.sumInsured,
                    formInsuranceCalc.responses.stepInsuranceInput.premium,
                    formInsuranceCalc.responses.stepInsuranceInput.policyTenure,
                    formInsuranceCalc.responses.stepInsuranceInput.age,
                    formInsuranceCalc.responses.stepInsuranceInput.coverageType
                  )
                }
              }
            }
          })" class="form-wrap amp-form-block amp-html-block formInsuranceCalc-wrapper" style="margin:auto;text-align:left">
        <!-- Initial form state -->
        <amp-state id="formInsuranceCalc">
          <script type="application/json">{"currentStep":"stepInsuranceInput","responses":{},"formHistory":[]}</script>
        </amp-state>
        <h2 class="calculator-title">Insurance Premium Calculator</h2>
        <form id="formWidgetInsuranceCalc" method="post" custom-validation-reporting="show-all-on-submit"
          on="submit:AMP.setState({formInsuranceCalc:{formHistory: formInsuranceCalc.formHistory.splice(formInsuranceCalc.formHistory.length,0,formInsuranceCalc.currentStep) , currentStep: 'stepInsuranceResult'}})"
          action-xhr="https://google.com">
          <!-- Sum Insured -->
          <div class="field-wrap">
            <label>Sum Insured ($)</label>
            <div class="input-wrap">
              <span class="prefix">$ </span>
              <input type="number" class="input-style" name="sumInsured" id="sumInsured"
                placeholder="Enter the sum insured" required
                [value]="formInsuranceCalc.responses.stepInsuranceInput.sumInsured || ''"
                on="input-throttled:AMP.setState({formInsuranceCalc:{responses:{stepInsuranceInput:{sumInsured: event.value}}}})">
            </div>
            <div visible-when-invalid="valueMissing" validation-for="sumInsured" style="font-size:13px;padding-top:4px">
              This field is required</div>
          </div>
          <!-- Premium -->
          <div class="field-wrap">
            <label>Premium Amount ($)</label>
            <div class="input-wrap">
              <span class="prefix">$ </span>
              <input type="number" class="input-style" name="premium" id="premium" placeholder="Enter premium amount"
                required pattern="[-]?[\d\.]{0,200}"
                [value]="formInsuranceCalc.responses.stepInsuranceInput.premium || ''"
                on="input-throttled:AMP.setState({formInsuranceCalc:{responses:{stepInsuranceInput:{premium: event.value}}}})">
            </div>
            <div visible-when-invalid="valueMissing" validation-for="premium" style="font-size:13px;padding-top:4px">
              This field is required</div>
          </div>
          <!-- Policy Tenure -->
          <div class="field-wrap">
            <label>Policy Tenure (Years)</label>
            <div class="input-wrap">
              <input type="number" class="input-style" name="policyTenure" id="policyTenure"
                placeholder="Enter policy tenure" required pattern="[-]?[\d\.]{0,200}"
                [value]="formInsuranceCalc.responses.stepInsuranceInput.policyTenure || ''"
                on="input-throttled:AMP.setState({formInsuranceCalc:{responses:{stepInsuranceInput:{policyTenure: event.value}}}})">
            </div>
            <div visible-when-invalid="valueMissing" validation-for="policyTenure"
              style="font-size:13px;padding-top:4px">
              This field is required</div>
          </div>
          <!-- Age -->
          <div class="field-wrap">
            <label>Your Age</label>
            <div class="input-wrap">
              <input type="number" class="input-style" name="age" id="age" placeholder="Enter your age" required
                pattern="[-]?[\d\.]{0,200}" [value]="formInsuranceCalc.responses.stepInsuranceInput.age || ''"
                on="input-throttled:AMP.setState({formInsuranceCalc:{responses:{stepInsuranceInput:{age: event.value}}}})">
            </div>
            <div visible-when-invalid="valueMissing" validation-for="age" style="font-size:13px;padding-top:4px">
              This field is required</div>
          </div>
          <!-- Coverage Type -->
          <div class="field-wrap">
            <label>Coverage Type</label>
            <div class="input-wrap">
              <select id="coverageType" name="coverageType"
                on="change:AMP.setState({formInsuranceCalc:{responses:{stepInsuranceInput:{coverageType: event.value}}}})">
                <option value="Health insurance">Health insurance</option>
                <option value="Life insurance">Life insurance</option>
              </select>
            </div>
          </div>
          <input hidden id="fuuid" name="fuuid" [value]="formInsuranceCalc.fuuid">
          <input hidden id="next-step-id" name="next-step-id" value="stepInsuranceResult">
          <div class="navigation-button-wrapper">
            <!-- Change CTA -->
            <button class="button" type="submit">Calculate</button>
            <!-- Change CTA -->
          </div>
        </form>
        <!-- Result screen -->
        <form class="result-wrap" method="post" hidden action-xhr="https://google.com"
          [hidden]="formInsuranceCalc.currentStep != 'stepInsuranceResult'">
          <div class="field-wrap">
            <amp-bind-macro id="insuranceFormula" arguments="sumInsured,premium,policyTenure,age, coverageType"
              expression="(((((+sumInsured * +premium) / (+policyTenure + +age)) * (coverageType == 'Life insurance' ? 1.1 : 1)) || 0).toFixed(2))">
            </amp-bind-macro>
            <h2 class="result-title">Insurance Premium Result</h2>
            <div class="result-output">
              <h3 class="total-text">Total Premium:</h3>
              <span class="formula-result total-value"
                [text]="insuranceFormula(formInsuranceCalc.responses.stepInsuranceInput.sumInsured,formInsuranceCalc.responses.stepInsuranceInput.premium,formInsuranceCalc.responses.stepInsuranceInput.policyTenure,formInsuranceCalc.responses.stepInsuranceInput.age,formInsuranceCalc.responses.stepInsuranceInput.coverageType)">
                0
              </span>
            </div>
          </div>
          <input hidden id="fuuid" name="fuuid" [value]="formInsuranceCalc.fuuid">
          <div class="navigation-button-wrapper">
            <button class="button" type="submit">
              Go to website
            </button>
            <button class="button" type="button" on="tap:AMP.setState({
                formInsuranceCalc: {
                  responses: {
                    stepInsuranceInput: {
                      sumInsured: '', premium: '', policyTenure: '', age: '', coverageType: 'Health insurance'
                    }
                  },
                  currentStep: 'stepInsuranceInput'
                }
              })">
              Calculate Again
            </button>
          </div>
        </form>
      </div>
    </div>
    <!-- Footer Section -->
    <footer class="footer">
      <ul class="media-logo-list">
        <!-- Footer Links -->
        <!-- Social Links -->
        <li class="logo-item">
          <a href="https://www.google.co.in/" class="logo-link">
            <amp-img layout="responsive"
              src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/SIP-Calculator/insta.png" alt="instagram"
              class="media-logo" width="20" height="20"></amp-img>
          </a>
        </li>
        <li class="logo-item">
          <a href="https://www.google.co.in/" class="logo-link">
            <amp-img layout="responsive"
              src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/SIP-Calculator/facebook.png" alt="facebook"
              class="media-logo" width="20" height="20"></amp-img>
          </a>
        </li>
        <li class="logo-item">
          <a href="https://www.google.co.in/" class="logo-link">
            <amp-img layout="responsive"
              src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/SIP-Calculator/x.png" alt="x"
              class="media-logo" width="20" height="20"></amp-img>
          </a>
        </li>
        <!-- Footer Links -->
        <!-- Social Links -->
      </ul>
      <p class="f-desc">
        is simply dummy text of the printing and typesetting is simply dummy text of the printing and typesetting
        industry.g industry.
      </p>
      <p class="f-desc" style="margin-top: 50px;">To stop receiving these emails, <a href="https://google.com"
          style="color:#1E1E1E;font-weight:bold;text-decoration:none;">unsubscribe here</a></p>
    </footer>
    <!-- Footer Section -->
  </div>
</body>
</html>
```

</details>

## Relevant Products

This AMP template dynamically showcases relevant products based on a user’s past browsing or purchase behavior. It displays collections or personalized categories and allows users to apply filters and explore product grids without leaving the email. With built-in interactivity and clear CTAs such as Shop Now and See More, this template is designed to drive high engagement and product discovery.

<details>

<summary>Expand to know more about the template.</summary>

### Use Case Examples

- Recommend products personalized to users’ past interactions or preferences.
- Launch seasonal or trending collections in an interactive format.
- Encourage repeat purchases with dynamic product carousels and filters.
- Promote gender- or category-specific catalogs (for example, Men/Women collections).

### Template Customization Options

- Replace the Logo
- Update Banner/Product Images
- Update Call-To-Actions (CTAs)
- Update Links in the Header/Footer
- Change the Theme or Background Color
- Update the Privacy Policy
- Update Social Media Links and Download Links
- Add More Filters: Add or modify product filters

### Template Code

```html
<!doctype html>
<html ⚡4email data-css-strict>
<head>
	<meta charset="utf-8">
	<script async src="https://cdn.ampproject.org/v0.js"></script>
	<script async custom-element="amp-carousel" src="https://cdn.ampproject.org/v0/amp-carousel-0.1.js"></script>
	<script async custom-element="amp-bind" src="https://cdn.ampproject.org/v0/amp-bind-0.1.js"></script>
	<script async custom-element="amp-form" src="https://cdn.ampproject.org/v0/amp-form-0.1.js"></script>
	<script async custom-element="amp-selector" src="https://cdn.ampproject.org/v0/amp-selector-0.1.js"></script>
	<style amp4email-boilerplate>
		body {
			visibility: hidden
		}
	</style>
	<style amp-custom>
		* {
			margin: 0;
			padding: 0;
		}
		body {
			font-family: "Helvetica", arial, sans-serif;
			font-weight: 400;
			background: #F5F5F5;
		}
		@media only screen and (max-width: 400px) {
			.main {
				max-width: 95%;
			}
		}
		.logo-wrap {
			padding: 5px 0;
		}
		.logo-wrap .logo {
			max-width: 159px;
			max-height: 73px;
			margin: 0 auto;
		}
		.title {
			margin: 31px 0 10px;
			font-size: 30px;
			font-weight: 400;
			line-height: 43.35px;
			text-align: center;
			color: #000000;
			text-transform: uppercase;
		}
		.para {
			margin: 0 auto;
			font-size: 14px;
			font-weight: 400;
			line-height: 24px;
			text-align: center;
			color: #6F6F6F;
			text-transform: uppercase;
			max-width: 70%;
		}
		.category-btn-wrap {
			margin: 30px 0 40px;
			display: flex;
			align-items: center;
			justify-content: center;
		}
		.wrapper {
			padding: 0 25px;
		}
		.btn {
			border: 1px solid #1DBF73;
			background: #1DBF73;
			color: #FFFFFF;
			font-size: 14px;
			font-weight: 400;
			line-height: 25px;
			text-transform: uppercase;
			text-align: center;
			padding: 6px;
			margin: 0 5px;
			max-width: 95px;
			width: 100%;
			display: inline-block;
			text-decoration: none;
		}
		.btn.typ-secondary {
			color: #1DBF73;
			background: #FFFFFF;
		}
		.sec-title {
			margin: 0 0 15px;
			font-size: 22px;
			font-weight: 400;
			line-height: 25px;
			text-transform: uppercase;
			color: #1E1E1E;
		}
		.product-list {
			padding: 0;
			display: flex;
			justify-content: space-between;
			align-items: flex-start;
			gap: 15px;
			flex-wrap: wrap;
			list-style: none;
		}
		.product-list .product-item {
			width: 48%;
		}
		.product-card {
			padding: 5px;
			background: #EFEFEF;
		}
		.product-card .img-wrap {
			max-width: 258px;
			max-height: 174px;
			margin-bottom: 5px;
			width: 100%;
			height: 100%;
		}
		.product-card .content-wrap {
			display: flex;
			justify-content: space-between;
			align-items: flex-start;
		}
		.product-card .content-wrap .lhs {
			width: 80%;
		}
		.product-card .content-wrap .rhs {
			width: 20%;
			display: flex;
			flex-direction: column;
			align-items: flex-end;
		}
		.p-title {
			font-size: 14px;
			font-weight: 400;
			line-height: 25px;
			color: #1E1E1E;
			text-transform: uppercase;
		}
		.p-desc {
			color: #909090;
			font-size: 8px;
			font-weight: 400;
			line-height: 13px;
			text-transform: capitalize;
		}
		.p-amt {
			font-size: 12px;
			font-style: italic;
			font-weight: 400;
			line-height: 25px;
			text-align: right;
			color: #252525;
		}
		.rupee {
			font-size: 10px;
		}
		.p-link {
			max-width: 92%;
			margin: 5px 0 0;
			border: 1px solid #1DBF73;
			background: #1DBF73;
			color: #1E1E1E;
			font-size: 10px;
			font-weight: 400;
			line-height: 13px;
			text-transform: uppercase;
			text-align: center;
			padding: 6px 10px;
			display: block;
			text-decoration: none;
		}
		.btn-wrap {
			text-align: center;
			margin: 28px 0 50px;
		}
		.media-logo {
			width: 20px;
			height: 20px;
		}
		.color-list{
			display: flex;
			justify-items: flex-end;
			align-items: center;
			list-style: none;
			gap: 5px;
		}
		amp-selector [option]{
			outline: 1px solid #00000033;
		}
		amp-selector [option][selected]{
			outline: 1px solid #1DBF73;
		}
		@media screen and (max-width: 480px) {
			.wrapper {
				padding: 0 10px;
			}
			.product-list {
				gap: 10px;
			}
			.product-card .content-wrap .lhs {
				width: 70%;
			}
			.product-card .content-wrap .rhs {
				width: 30%;
			}
			.p-title {
				line-height: 18px;
			}
		}
		@media screen and (max-width: 300px) {
			.product-list .product-item {
				width: 100%;
			}
		}
	</style>
</head>
<body>
	<!-- AMP state for handling category selection -->
	<amp-state id="selectedCategory">
		<script type="application/json">
			{
				"value": "men" 
			}
		</script>
	</amp-state>
	<table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%"
		style="max-width: 600px; margin: 0 auto; background-color: #FFFFFF;" class="main">
		<!-- header start-->
		<tr>
			<td align="center" style="padding: 5px 0;">
				<div class="logo-wrap">
					<!-- Change logo src as per your requirements -->
					<amp-img layout="responsive"
						src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/relevant/logo.png" alt="Logo"
						width="157" height="81" class="logo" />
					<!-- Change logo src as per your requirements -->
				</div>
			</td>
		</tr>
		<!-- header end-->
		<!-- Banner slider start-->
		<tr>
			<td align="center">
				<div class="banner">
					<amp-carousel width="600" height="400" layout="responsive" type="slides" autoplay loop delay="10000"
						role="region" aria-label="banner carousel with autoplay">
						<amp-img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/relevant/banner-1.png"
							width="600" height="400" layout="responsive" alt="a sample image"></amp-img>
						<amp-img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/relevant/banner-2.png"
							width="600" height="400" layout="responsive" alt="another sample image"></amp-img>
					</amp-carousel>
				</div>
			</td>
		</tr>
		<!-- Banner slider end-->
		<!-- Change CTA -->
		<tr>
			<td align="center">
				<h1 class="title">new collection</h1>
				<p class="para">is simply dummy text of the printing and typesetting. is simply dummy text of the
					printing.</p>
				<div class="category-btn-wrap">
					<button class="btn" [class]="'btn ' + (selectedCategory.value == 'men' ? '' : 'typ-secondary')"
						value="men" on="tap:AMP.setState({selectedCategory: {value: 'men'}})">
						Men
					</button>
					<button class="btn typ-secondary"
						[class]="'btn ' + (selectedCategory.value == 'women' ? '' : 'typ-secondary')" value="women"
						on="tap:AMP.setState({selectedCategory: {value: 'women'}})">
						Women
					</button>
				</div>
			</td>
		</tr>
		<!-- Change CTA -->
		<tr>
			<td class="wrapper">
				<!-- Title changes dynamically based on selected category -->
				<form id="order" method="POST"
				action-xhr="/"
				target="_top">
					<h2 class="sec-title" [text]="selectedCategory.value">Men</h2>
					<!-- Men category product list -->
					<div class="category category-men" [hidden]="selectedCategory.value != 'men'">	
						<ul class="product-list">
							<li class="product-item">
								<amp-state id="selectedMenProduct1">
									<script type="application/json">
									  {
										"value": "option1"
									  }
									</script>
								  </amp-state>
								<!-- Men Product 1 Option 1 -->
								<div class="product-card" [hidden]="selectedMenProduct1.value != 'option1'">
									<div class="img-wrap">
										<amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/relevant/men-product-1.png" alt="Product Image" width="258" height="174"></amp-img>
									</div>
									<div class="content-wrap">
										<div class="lhs">
											<h3 class="p-title">Hoodies</h3>
											<p class="p-desc">is simply dummy text of the new age fashion industry.</p>
										</div>
										<div class="rhs">
											<p class="p-amt"><span class="rupee">₹</span>1500</p>
											<amp-selector layout="container" name="men-product-1" on="select:AMP.setState({selectedMenProduct1: { value: event.targetOption }})">
												<ul class="color-list">
													<li class="color-item">
													<div class="color" style="width: 15px; height: 14px; background: #000000;" option="option1"></div>
													</li>
													<li class="color-item">
													<div class="color" style="width: 15px; height: 14px; background: #1DBF73" option="option2"></div>
													</li>
												</ul>
											</amp-selector>
										</div>
									</div>
									<a href="https://www.google.co.in/" class="p-link">Shop now</a>
							  	</div>
					  			<!-- Men Product 1 Option 2 -->
								<div class="product-card" hidden [hidden]="selectedMenProduct1.value != 'option2'">
									<div class="img-wrap">
										<amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/relevant/men-product-2.png" alt="Product Image" width="258" height="174"></amp-img>
									</div>
									<div class="content-wrap">
										<div class="lhs">
											<h3 class="p-title">Hoodies 2</h3>
											<p class="p-desc">is simply dummy text of the new age fashion industry.</p>
										</div>
										<div class="rhs">
											<p class="p-amt"><span class="rupee">₹</span>2500</p>
											<amp-selector layout="container" name="men-product-1" on="select:AMP.setState({selectedMenProduct1: { value: event.targetOption }})">
												<ul class="color-list">
													<li class="color-item">
													<div class="color" style="width: 15px; height: 14px; background: #000000;" option="option1"></div>
													</li>
													<li class="color-item">
													<div class="color" style="width: 15px; height: 14px; background: #1DBF73" option="option2"></div>
													</li>
												</ul>
											</amp-selector>
										</div>
									</div>
									<a href="https://www.google.co.in/" class="p-link">Shop now</a>
								</div>
							</li>
							<li class="product-item">
								<amp-state id="selectedMenProduct2">
									<script type="application/json">
									  {
										"value": "men2option1"
									  }
									</script>
								</amp-state>
								<!-- Men Product 2 Option 1 -->
								<div class="product-card" [hidden]="selectedMenProduct2.value != 'men2option1'">
									<div class="img-wrap">
										<amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/relevant/men-product-2.png" alt="Product Image" width="258" height="174"></amp-img>
									</div>
									<div class="content-wrap">
										<div class="lhs">
											<h3 class="p-title">Product name</h3>
											<p class="p-desc">is simply dummy text of the new age fashion industry.</p>
										</div>
										<div class="rhs">
											<p class="p-amt"><span class="rupee">₹</span>1500</p>
											<amp-selector layout="container" name="men-product-2" on="select:AMP.setState({selectedMenProduct2: { value: event.targetOption }})">
												<ul class="color-list">
													<li class="color-item">
														<div class="color" style="width: 15px; height: 14px; background: #000000;" option="men2option1"></div>
													</li>
													<li class="color-item">
														<div class="color" style="width: 15px; height: 14px; background: #DFDAD4" option="men2option2"></div>
													</li>
												</ul>
											</amp-selector>
										</div>
									</div>
									<a href="https://www.google.co.in/" class="p-link">Shop now</a>
								</div>
								<!-- Men Product 2 Option 2 -->
								<div class="product-card" hidden [hidden]="selectedMenProduct2.value != 'men2option2'">
									<div class="img-wrap">
										<amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/relevant/men-product-3.png" alt="Product Image" width="258" height="174"></amp-img>
									</div>
									<div class="content-wrap">
										<div class="lhs">
											<h3 class="p-title">Product name 2</h3>
											<p class="p-desc">is simply dummy text of the new age fashion industry.</p>
										</div>
										<div class="rhs">
											<p class="p-amt"><span class="rupee">₹</span>2500</p>
											<amp-selector layout="container" name="men-product-2" on="select:AMP.setState({selectedMenProduct2: { value: event.targetOption }})">
												<ul class="color-list">
													<li class="color-item">
														<div class="color" style="width: 15px; height: 14px; background: #000000;" option="men2option1"></div>
													</li>
													<li class="color-item">
														<div class="color" style="width: 15px; height: 14px; background: #DFDAD4" option="men2option2"></div>
													</li>
												</ul>
											</amp-selector>
										</div>
									</div>
									<a href="https://www.google.co.in/" class="p-link">Shop now</a>
								</div>
							</li>
							<li class="product-item">
								<amp-state id="selectedMenProduct3">
									<script type="application/json">
									  {
										"value": "men3option1"
									  }
									</script>
								</amp-state>
								<!-- Men Product 3 Option 1 -->
								<div class="product-card" [hidden]="selectedMenProduct3.value != 'men3option1'">
									<div class="img-wrap">
										<amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/relevant/men-product-3.png" alt="Product Image" width="258" height="174"></amp-img>
									</div>
									<div class="content-wrap">
										<div class="lhs">
											<h3 class="p-title">T-shirt</h3>
											<p class="p-desc">is simply dummy text of the new age fashion industry.</p>
										</div>
										<div class="rhs">
											<p class="p-amt"><span class="rupee">$</span>1500</p>
											<amp-selector layout="container" name="men-product-3" on="select:AMP.setState({selectedMenProduct3: { value: event.targetOption }})">
												<ul class="color-list">
													<li class="color-item">
														<div class="color" style="width: 15px; height: 14px; background: #8C1F34;" option="men3option1"></div>
													</li>
													<li class="color-item">
														<div class="color" style="width: 15px; height: 14px; background: #EBEBEB" option="men3option2"></div>
													</li>
												</ul>
											</amp-selector>
										</div>
									</div>
									<a href="https://www.google.co.in/" class="p-link">Shop now</a>
								</div>
								<!-- Men Product 3 Option 2 -->
								<div class="product-card" hidden [hidden]="selectedMenProduct3.value != 'men3option2'">
									<div class="img-wrap">
										<amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/relevant/men-product-4.png" alt="Product Image" width="258" height="174"></amp-img>
									</div>
									<div class="content-wrap">
										<div class="lhs">
											<h3 class="p-title">T-shirt 2</h3>
											<p class="p-desc">is simply dummy text of the new age fashion industry.</p>
										</div>
										<div class="rhs">
											<p class="p-amt"><span class="rupee">$</span>2500</p>
											<amp-selector layout="container" name="men-product-3" on="select:AMP.setState({selectedMenProduct3: { value: event.targetOption }})">
												<ul class="color-list">
													<li class="color-item">
														<div class="color" style="width: 15px; height: 14px; background: #8C1F34;" option="men3option1"></div>
													</li>
													<li class="color-item">
														<div class="color" style="width: 15px; height: 14px; background: #EBEBEB" option="men3option2"></div>
													</li>
												</ul>
											</amp-selector>
										</div>
									</div>
									<a href="https://www.google.co.in/" class="p-link">Shop now</a>
								</div>
							</li>	
							<li class="product-item">
								<amp-state id="selectedMenProduct4">
									<script type="application/json">
									  {
										"value": "men4option1"
									  }
									</script>
								</amp-state>
								<!-- Men Product 4 Option 1 -->
								<div class="product-card" [hidden]="selectedMenProduct4.value != 'men4option1'">
									<div class="img-wrap">
										<amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/relevant/men-product-4.png" alt="Product Image" width="258" height="174"></amp-img>
									</div>
									<div class="content-wrap">
										<div class="lhs">
											<h3 class="p-title">Product Name 1</h3>
											<p class="p-desc">is simply dummy text of the new age fashion industry.</p>
										</div>
										<div class="rhs">
											<p class="p-amt"><span class="rupee">$</span>1500</p>
											<amp-selector layout="container" name="men-product-4" on="select:AMP.setState({selectedMenProduct4: { value: event.targetOption }})">
												<ul class="color-list">
													<li class="color-item">
														<div class="color" style="width: 15px; height: 14px; background: #D4D9DD;" option="men4option1"></div>
													</li>
													<li class="color-item">
														<div class="color" style="width: 15px; height: 14px; background: #0A0B0D" option="men4option2"></div>
													</li>
												</ul>
											</amp-selector>
										</div>
									</div>
									<a href="https://www.google.co.in/" class="p-link">Shop now</a>
								</div>
								<!-- Men Product 4 Option 2 -->
								<div class="product-card" hidden [hidden]="selectedMenProduct4.value != 'men4option2'">
									<div class="img-wrap">
										<amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/relevant/men-product-1.png" alt="Product Image" width="258" height="174"></amp-img>
									</div>
									<div class="content-wrap">
										<div class="lhs">
											<h3 class="p-title">Product Name  2</h3>
											<p class="p-desc">is simply dummy text of the new age fashion industry.</p>
										</div>
										<div class="rhs">
											<p class="p-amt"><span class="rupee">$</span>2500</p>
											<amp-selector layout="container" name="men-product-4" on="select:AMP.setState({selectedMenProduct4: { value: event.targetOption }})">
												<ul class="color-list">
													<li class="color-item">
														<div class="color" style="width: 15px; height: 14px; background: #D4D9DD;" option="men4option1"></div>
													</li>
													<li class="color-item">
														<div class="color" style="width: 15px; height: 14px; background: #0A0B0D" option="men4option2"></div>
													</li>
												</ul>
											</amp-selector>
										</div>
									</div>
									<a href="https://www.google.co.in/" class="p-link">Shop now</a>
								</div>
							</li>						
						</ul>
					</div>
					<!-- Women category product list -->
					<div class="category category-women" hidden [hidden]="selectedCategory.value != 'women'">
						<ul class="product-list">
							<li class="product-item">
								<amp-state id="selectedWomenProduct1">
									<script type="application/json">
									  {
										"value": "women1option1"
									  }
									</script>
								</amp-state>
								<!-- Women Product 1 Option 1 -->
								<div class="product-card" [hidden]="selectedWomenProduct1.value != 'women1option1'">
									<div class="img-wrap">
										<amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/relevant/women-product-1.png" alt="Product Image" width="258" height="174"></amp-img>
									</div>
									<div class="content-wrap">
										<div class="lhs">
											<h3 class="p-title">Product name 1</h3>
											<p class="p-desc">is simply dummy text of the new age fashion industry.</p>
										</div>
										<div class="rhs">
											<p class="p-amt"><span class="rupee">$</span>1500</p>
											<amp-selector layout="container" name="women-product-1" on="select:AMP.setState({selectedWomenProduct1: { value: event.targetOption }})">
												<ul class="color-list">
													<li class="color-item">
														<div class="color" style="width: 15px; height: 14px; background: #000000;" option="women1option1"></div>
													</li>
													<li class="color-item">
														<div class="color" style="width: 15px; height: 14px; background: #DFDAD4" option="women1option2"></div>
													</li>
												</ul>
											</amp-selector>
										</div>
									</div>
									<a href="https://www.google.co.in/" class="p-link">Shop now</a>
								</div>
								<!-- Women Product 1 Option 2 -->
								<div class="product-card" hidden [hidden]="selectedWomenProduct1.value != 'women1option2'">
									<div class="img-wrap">
										<amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/relevant/women-product-2.png" alt="Product Image" width="258" height="174"></amp-img>
									</div>
									<div class="content-wrap">
										<div class="lhs">
											<h3 class="p-title">Product name 2</h3>
											<p class="p-desc">is simply dummy text of the new age fashion industry.</p>
										</div>
										<div class="rhs">
											<p class="p-amt"><span class="rupee">$</span>2500</p>
											<amp-selector layout="container" name="women-product-1" on="select:AMP.setState({selectedWomenProduct1: { value: event.targetOption }})">
												<ul class="color-list">
													<li class="color-item">
														<div class="color" style="width: 15px; height: 14px; background: #000000;" option="women1option1"></div>
													</li>
													<li class="color-item">
														<div class="color" style="width: 15px; height: 14px; background: #DFDAD4" option="women1option2"></div>
													</li>
												</ul>
											</amp-selector>
										</div>
									</div>
									<a href="https://www.google.co.in/" class="p-link">Shop now</a>
								</div>
							</li>
							<li class="product-item">
								<amp-state id="selectedWomenProduct2">
									<script type="application/json">
									  {
										"value": "women2option1"
									  }
									</script>
								</amp-state>
								<!-- Women Product 2 Option 1 -->
								<div class="product-card" [hidden]="selectedWomenProduct2.value != 'women2option1'">
									<div class="img-wrap">
										<amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/relevant/women-product-2.png" alt="Product Image" width="258" height="174"></amp-img>
									</div>
									<div class="content-wrap">
										<div class="lhs">
											<h3 class="p-title">Product name 1</h3>
											<p class="p-desc">is simply dummy text of the new age fashion industry.</p>
										</div>
										<div class="rhs">
											<p class="p-amt"><span class="rupee">$</span>1500</p>
											<amp-selector layout="container" name="women-product-2" on="select:AMP.setState({selectedWomenProduct2: { value: event.targetOption }})">
												<ul class="color-list">
													<li class="color-item">
														<div class="color" style="width: 15px; height: 14px; background: #000000;" option="women2option1"></div>
													</li>
													<li class="color-item">
														<div class="color" style="width: 15px; height: 14px; background: #DFDAD4" option="women2option2"></div>
													</li>
												</ul>
											</amp-selector>
										</div>
									</div>
									<a href="https://www.google.co.in/" class="p-link">Shop now</a>
								</div>
								<!-- Women Product 2 Option 2 -->
								<div class="product-card" hidden [hidden]="selectedWomenProduct2.value != 'women2option2'">
									<div class="img-wrap">
										<amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/relevant/women-product-3.png" alt="Product Image" width="258" height="174"></amp-img>
									</div>
									<div class="content-wrap">
										<div class="lhs">
											<h3 class="p-title">Product name 2</h3>
											<p class="p-desc">is simply dummy text of the new age fashion industry.</p>
										</div>
										<div class="rhs">
											<p class="p-amt"><span class="rupee">$</span>2500</p>
											<amp-selector layout="container" name="women-product-2" on="select:AMP.setState({selectedWomenProduct2: { value: event.targetOption }})">
												<ul class="color-list">
													<li class="color-item">
														<div class="color" style="width: 15px; height: 14px; background: #000000;" option="women2option1"></div>
													</li>
													<li class="color-item">
														<div class="color" style="width: 15px; height: 14px; background: #DFDAD4" option="women2option2"></div>
													</li>
												</ul>
											</amp-selector>
										</div>
									</div>
									<a href="https://www.google.co.in/" class="p-link">Shop now</a>
								</div>
							</li>
							<li class="product-item">
								<amp-state id="selectedWomenProduct3">
									<script type="application/json">
									  {
										"value": "women3option1"
									  }
									</script>
								</amp-state>
								<!-- Women Product 3 Option 1 -->
								<div class="product-card" [hidden]="selectedWomenProduct3.value != 'women3option1'">
									<div class="img-wrap">
										<amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/relevant/women-product-3.png" alt="Product Image" width="258" height="174"></amp-img>
									</div>
									<div class="content-wrap">
										<div class="lhs">
											<h3 class="p-title">Product name 1</h3>
											<p class="p-desc">is simply dummy text of the new age fashion industry.</p>
										</div>
										<div class="rhs">
											<p class="p-amt"><span class="rupee">$</span>1500</p>
											<amp-selector layout="container" name="women-product-3" on="select:AMP.setState({selectedWomenProduct3: { value: event.targetOption }})">
												<ul class="color-list">
													<li class="color-item">
														<div class="color" style="width: 15px; height: 14px; background: #000000;" option="women3option1"></div>
													</li>
													<li class="color-item">
														<div class="color" style="width: 15px; height: 14px; background: #DFDAD4" option="women3option2"></div>
													</li>
												</ul>
											</amp-selector>
										</div>
									</div>
									<a href="https://www.google.co.in/" class="p-link">Shop now</a>
								</div>
								<!-- Women Product 3 Option 2 -->
								<div class="product-card" hidden [hidden]="selectedWomenProduct3.value != 'women3option2'">
									<div class="img-wrap">
										<amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/relevant/women-product-4.png" alt="Product Image" width="258" height="174"></amp-img>
									</div>
									<div class="content-wrap">
										<div class="lhs">
											<h3 class="p-title">Product name 2</h3>
											<p class="p-desc">is simply dummy text of the new age fashion industry.</p>
										</div>
										<div class="rhs">
											<p class="p-amt"><span class="rupee">$</span>2500</p>
											<amp-selector layout="container" name="women-product-3" on="select:AMP.setState({selectedWomenProduct3: { value: event.targetOption }})">
												<ul class="color-list">
													<li class="color-item">
														<div class="color" style="width: 15px; height: 14px; background: #000000;" option="women3option1"></div>
													</li>
													<li class="color-item">
														<div class="color" style="width: 15px; height: 14px; background: #DFDAD4" option="women3option2"></div>
													</li>
												</ul>
											</amp-selector>
										</div>
									</div>
									<a href="https://www.google.co.in/" class="p-link">Shop now</a>
								</div>
							</li>
							<li class="product-item">
								<amp-state id="selectedWomenProduct4">
									<script type="application/json">
									  {
										"value": "women4option1"
									  }
									</script>
								</amp-state>
								<!-- Women Product 4 Option 1 -->
								<div class="product-card" [hidden]="selectedWomenProduct4.value != 'women4option1'">
									<div class="img-wrap">
										<amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/relevant/women-product-4.png" alt="Product Image" width="258" height="174"></amp-img>
									</div>
									<div class="content-wrap">
										<div class="lhs">
											<h3 class="p-title">Product name 1</h3>
											<p class="p-desc">is simply dummy text of the new age fashion industry.</p>
										</div>
										<div class="rhs">
											<p class="p-amt"><span class="rupee">$</span>1500</p>
											<amp-selector layout="container" name="women-product-4" on="select:AMP.setState({selectedWomenProduct4: { value: event.targetOption }})">
												<ul class="color-list">
													<li class="color-item">
														<div class="color" style="width: 15px; height: 14px; background: #000000;" option="women4option1"></div>
													</li>
													<li class="color-item">
														<div class="color" style="width: 15px; height: 14px; background: #DFDAD4" option="women4option2"></div>
													</li>
												</ul>
											</amp-selector>
										</div>
									</div>
									<a href="https://www.google.co.in/" class="p-link">Shop now</a>
								</div>
								<!-- Women Product 4 Option 2 -->
								<div class="product-card" hidden [hidden]="selectedWomenProduct4.value != 'women4option2'">
									<div class="img-wrap">
										<amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/relevant/women-product-1.png" alt="Product Image" width="258" height="174"></amp-img>
									</div>
									<div class="content-wrap">
										<div class="lhs">
											<h3 class="p-title">Product name 2</h3>
											<p class="p-desc">is simply dummy text of the new age fashion industry.</p>
										</div>
										<div class="rhs">
											<p class="p-amt"><span class="rupee">$</span>2500</p>
											<amp-selector layout="container" name="women-product-4" on="select:AMP.setState({selectedWomenProduct4: { value: event.targetOption }})">
												<ul class="color-list">
													<li class="color-item">
														<div class="color" style="width: 15px; height: 14px; background: #000000;" option="women4option1"></div>
													</li>
													<li class="color-item">
														<div class="color" style="width: 15px; height: 14px; background: #DFDAD4" option="women4option2"></div>
													</li>
												</ul>
											</amp-selector>
										</div>
									</div>
									<a href="https://www.google.co.in/" class="p-link">Shop now</a>
								</div>
							</li>
						</ul>
					</div>
					<div class="btn-wrap">
						<button class="btn ">See more</button>
					</div>
				</form>
			</td>
		</tr>
		<!-- product section end-->
		<!-- footer start-->
		<tr>
			<td style="text-align: center;">
				<table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%" class="container"
					style="background: #EFEFEF; padding: 40px 0;">
					<tr>
						<td>
							<table align="center" cellpadding="0" cellspacing="0" width="100%"
								style="text-align: center; margin-bottom: 30px;">
								<!-- Footer Link-->
								<!-- Social Links -->
								<tr>
									<td style="padding: 7px 39px; border: 1px solid #1DBF73; display: inline-block;">
										<a href="https://www.google.co.in/">
											<amp-img layout="responsive"
												src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/relevant/logo-insta.png"
												alt="Social Icon" class="media-logo" width="20" height="20">
											</amp-img>
										</a>
									</td>
									<td style="padding: 7px 39px; border: 1px solid #1DBF73; display: inline-block;">
										<a href="https://www.google.co.in/"><amp-img layout="responsive"
												src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/relevant/logo-facebook.png"
												alt="Social Icon" class="media-logo" width="20" height="20"></amp-img>	</a>
									</td>
									<td style="padding: 7px 39px; border: 1px solid #1DBF73; display: inline-block;">
										<a href="https://www.google.co.in/"><amp-img layout="responsive"
												src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/relevant/logo-x.png"
												alt="Social Icon" class="media-logo" width="20" height="20">	</a></amp-img>
									</td>
								</tr>
								<!-- Social Links -->
								<!-- Footer Link-->
							</table>
						</td>
					</tr>
					<tr>
						<td>
							<p
								style="font-family: 'Helvetica', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 24px; color: #4F4F4F; text-align: center; max-width: 90%; margin: 0 auto; text-transform: uppercase;">
								is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the
								industry's standard dummy text ever.</p>
						</td>
					</tr>
				</table>
			</td>
		</tr>
		<tr>
			<td>
				<p
					style="font-family: 'Helvetica', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 22px; text-align: center; color: #909090; text-transform: capitalize;  margin: 15px 0; ">
					To stop receiving these emails, <a href="https://www.google.co.in/"
						style="color: #1DBF73 ; font-weight: 700; text-transform: capitalize; text-decoration: none;">unsubscribe
						here</a></p>
			</td>
		</tr>
		<!-- footer end-->
	</table>
</body>
</html>
```

</details>

## Show Recommendations

This AMP template introduces users to personalized product suggestions using interactive email content. It can be used for onboarding new subscribers or re-engaging recent visitors by showcasing curated products tailored to their interests. This template typically includes featured products, category filters, and direct Shop Now CTAs, all rendered dynamically within the inbox.

<details>

<summary>Expand to know more about the template.</summary>

### Use Case Examples

- Introduce new users to relevant collections based on browsing behavior.
- Highlight bestsellers or staff picks to increase discovery.
- Re-engage dormant users with personalized product nudges.
- Encourage first purchases through category filters and CTAs.

### Template Customization Options

- Replace the Logo
- Update Banner/Product Images
- Update Call-To-Actions (CTAs)
- Update Links in the Header/Footer
- Change the Theme or Background Color
- Update Social Media Links and Download Links
- How to Add More Filters

### Template Code

```html Recommendations
<!doctype html>
<html ⚡4email data-css-strict>
<head>
	<meta charset="utf-8">
	<script async src="https://cdn.ampproject.org/v0.js"></script>
	<script async custom-element="amp-bind" src="https://cdn.ampproject.org/v0/amp-bind-0.1.js"></script>
	<script async custom-element="amp-form" src="https://cdn.ampproject.org/v0/amp-form-0.1.js"></script>
	<script async custom-element="amp-carousel" src="https://cdn.ampproject.org/v0/amp-carousel-0.1.js"></script>
	<style amp4email-boilerplate>
		body {
			visibility: hidden
		}
	</style>
	<style amp-custom>
		* {
			margin: 0;
			padding: 0;
		}
		body {
			font-family: "Helvetica", arial, sans-serif;
			font-weight: 400;
			background: #F5F5F5;
		}
		img {
			object-fit: cover;
		}
		@media only screen and (max-width: 400px) {
			.main {
				max-width: 95%;
			}
		}
		.logo-wrap {
			padding: 15px 0;
			position: relative;
		}
		.line {
			position: absolute;
			width: 100%;
			height: 1px;
			background: #F04444;
			top: 50%;
			left: 0;
			transform: translateY(-50%);
		}
		.logo-wrap .logo {
			max-width: 157px;
			max-height: 81px;
			margin: 0 auto;
			background: #FFFFFF;
			z-index: 1;
			padding: 0 30px;
		}
		.logo-wrap img {
			object-fit: contain;
		}
		.play-btn {
			border: 1px solid #F04444;
			background: #F04444;
			font-size: 14px;
			font-weight: 400;
			line-height: 25px;
			text-transform: capitalize;
			text-align: center;
			padding: 6px 15px 6px 6px;
			display: inline-block;
			text-decoration: none;
			border-radius: 50px;
			color: #FFFFFF;
			display: flex;
			align-items: center;
		}
		.play-btn .play-icon {
			width: 31px;
			height: 31px;
			margin-right: 10px;
		}
		.banner {
			margin-bottom: 25px;
		}
		.media-logo {
			width: 25px;
			height: 25px;
		}
		.section {
			padding-bottom: 60px;
		}
		.sec-title {
			position: relative;
			margin-bottom: 12px;
		}
		.sec-title .text {
			background: #FFFFFF;
			padding: 0 25px;
			font-size: 24px;
			font-weight: 400;
			line-height: 39px;
			text-align: center;
			color: #000000;
			text-transform: uppercase;
			z-index: 1;
			display: inline-block;
			position: relative;
		}
		.sec-desc {
			font-size: 14px;
			font-weight: 400;
			line-height: 25px;
			color: #6F6F6F;
			text-align: center;
			text-transform: capitalize;
			max-width: 85%;
			margin: 0 auto 25px;
		}
		.btn {
			border: 1px solid #F04444;
			background: #FFFFFF;
			font-size: 14px;
			font-weight: 400;
			line-height: 25px;
			text-transform: capitalize;
			text-align: center;
			padding: 6px;
			display: inline-block;
			text-align: center;
			text-decoration: none;
			border-radius: 50px;
			color: #F04444;
			max-width: 113px;
			width: 100%;
			margin: 5px;
		}
		.btn.typ-active {
			background: #F04444;
			color: #FFFFFF;
		}
		.category-btn-wrap {
			margin: 0 0 38px;
		}
		.img-wrap,
		.card {
			position: relative;
		}
		.btn-play {
			position: absolute;
			width: 74px;
			height: 74px;
			top: 50%;
			left: 50%;
			transform: translate(-50%, -50%);
		}
		.card .card-body {
			position: absolute;
			bottom: 0;
			left: 0;
			width: 100%;
			background: #00000080;
			padding: 18px 0
		}
		.card .card-title {
			font-size: 20px;
			font-weight: 400;
			line-height: 25px;
			text-align: left;
			color: #FFFFFF;
			margin: 0 18px 5px;
			text-transform: uppercase;
		}
		.card .card-desc {
			font-size: 14px;
			font-weight: 400;
			line-height: 25px;
			text-align: left;
			color: #FFFFFF;
			margin: 0 18px;
			text-transform: capitalize;
		}
		.movie-list {
			list-style: none;
			display: flex;
			justify-content: space-between;
			gap: 20px;
			max-width: 88%;
			margin: 0 auto;
		}
		.movie-list .movie-item {
			width: 48%;
		}
		.weekly-card .weekly-body {
			padding: 7px 0;
		}
		.weekly-card .weekly-title {
			font-size: 14px;
			font-weight: 400;
			line-height: 25px;
			color: #000000;
			text-align: left;
			text-transform: uppercase;
		}
		.weekly-card .weekly-desc {
			font-size: 10px;
			font-weight: 400;
			line-height: 15px;
			color: #6F6F6F;
			text-align: left;
			text-transform: capitalize;
		}
		.btn-wrap {
			margin-top: 30px;
		}
		@media only screen and (max-width: 400px) {
			.logo-wrap .logo {
				max-width: 130px;
				max-height: 70px;
			}
			.sec-title .text {
				font-size: 20px;
				font-weight: 400;
				padding: 0 10px;
			}
			.sec-desc {
				line-height: 20px;
			}
			.card .card-title {
				font-size: 18px;
				line-height: 20px;
				margin: 0 10px 5px;
			}
			.card .card-desc {
				font-size: 12px;
				line-height: 18px;
				margin: 0 10px;
			}
		}
	</style>
</head>
<body>
	<!-- AMP state for handling category selection -->
	<!-- Change Theme -->
	<table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%"
		style="max-width: 600px; margin: 0 auto; background-color: #FFFFFF;" class="main">
		<!-- header start-->
		<tr>
			<td align="center" style="padding: 5px 0;">
				<div class="logo-wrap">
					<div class="line"></div>
					<!-- Change Logo Image src as per your requirements -->
					<amp-img layout="responsive"
						src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/logo.png"
						alt="Logo" width="157" height="81" class="logo" />
					<!-- Change Logo Image src as per your requirements -->
				</div>
			</td>
		</tr>
		<!-- header end-->
		<!-- Banner start-->
		<tr>
			<td align="center">
				<div class="banner">
					<amp-img
						src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/banner.png"
						width="600" height="280" layout="responsive" alt="a sample image"></amp-img>
				</div>
			</td>
		</tr>
		<!-- Banner end-->
		<!-- new episodes start-->
		<tr>
			<td align="center">
				<div class="section">
					<div class="sec-head">
						<div class="sec-title">
							<h2 class="text">new episodes</h2>
							<div class="line"></div>
						</div>
						<p class="sec-desc">is simply dummy text of the printing and typesetting industry. is simply
							dummy text of the printing and typesetting industry.</p>
						<button class="play-btn">
							<amp-img layout="responsive"
								src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png"
								alt="Play Icon" class="play-icon" width="31" height="31"></amp-img> Watch now
						</button>
					</div>
				</div>
			</td>
		</tr>
		<!-- new episodes end-->
		<!-- product section start-->
		<amp-state id="selectedCategory">
			<script type="application/json">
				{
					"value": "action" 
				}
			</script>
		</amp-state>
		<tr>
			<td align="center">
				<div class="section">
					<div class="sec-head">
						<div class="sec-title">
							<h2 class="text">new collection</h2>
							<div class="line"></div>
						</div>
						<p class="sec-desc">is simply dummy text of the printing and typesetting industry. is simply
							dummy text of the printing and typesetting industry.</p>
						<div class="category-btn-wrap">
							<!-- Change CTA -->
							<button class="btn typ-active"
								[class]="'btn ' + (selectedCategory.value == 'action' ? 'typ-active' : '')"
								value="action" on="tap:AMP.setState({selectedCategory: {value: 'action'}})">
								Action
							</button>
							<button class="btn"
								[class]="'btn ' + (selectedCategory.value == 'horror' ? 'typ-active' : '')"
								value="horror" on="tap:AMP.setState({selectedCategory: {value: 'horror'}})">
								Horror
							</button>
							<button class="btn"
								[class]="'btn ' + (selectedCategory.value == 'drama' ? 'typ-active' : '')" value="drama"
								on="tap:AMP.setState({selectedCategory: {value: 'drama'}})">
								Drama
							</button>
							<button class="btn"
							[class]="'btn ' + (selectedCategory.value == 'Comedy' ? 'typ-active' : '')" value="Comedy"
							on="tap:AMP.setState({selectedCategory: {value: 'Comedy'}})">
							Comedy
						</button>
												<!-- Change CTA -->
						</div>
					</div>
					<!-- action cards start-->
					<div class="sec-content" [hidden]="selectedCategory.value != 'action'">
						<amp-carousel loop width="600" height="375" layout="responsive" type="slides" role="region"
							aria-label="action carousel">
							<div class="card">
								<div class="img-wrap">
									<amp-img
										src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/action-1.png"
										width="600" height="375" layout="responsive" alt="a sample image"></amp-img>
									<div class="btn-play">
										<amp-img layout="responsive"
											src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png"
											alt="Play Icon" class="play-icon" width="74" height="74"></amp-img>
									</div>
								</div>
								<div class="card-body">
									<h3 class="card-title">Season 1</h3>
									<p class="card-desc">is simply dummy text of the printing and typesetting.</p>
								</div>
							</div>
							<div class="card">
								<div class="img-wrap">
									<amp-img
										src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/action-2.png"
										width="600" height="375" layout="responsive" alt="a sample image"></amp-img>
									<div class="btn-play">
										<amp-img layout="responsive"
											src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png"
											alt="Play Icon" class="play-icon" width="74" height="74"></amp-img>
									</div>
								</div>
								<div class="card-body">
									<h3 class="card-title">Season 2</h3>
									<p class="card-desc">is simply dummy text of the printing and typesetting.</p>
								</div>
							</div>
							<div class="card">
								<div class="img-wrap">
									<amp-img
										src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/action-3.png"
										width="600" height="375" layout="responsive" alt="a sample image"></amp-img>
									<div class="btn-play">
										<amp-img layout="responsive"
											src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png"
											alt="Play Icon" class="play-icon" width="74" height="74"></amp-img>
									</div>
								</div>
								<div class="card-body">
									<h3 class="card-title">Season 3</h3>
									<p class="card-desc">is simply dummy text of the printing and typesetting.</p>
								</div>
							</div>
						</amp-carousel>
					</div>
					<!-- action cards end-->
					<!-- horror cards start-->
					<div class="sec-content" hidden [hidden]="selectedCategory.value != 'horror'">
						<amp-carousel width="600" loop height="375" layout="responsive" type="slides" role="region"
							aria-label="horror carousel">
							<div class="card">
								<div class="img-wrap">
									<amp-img
										src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/horror-1.png"
										width="600" height="375" layout="responsive" alt="a sample image"></amp-img>
									<div class="btn-play">
										<amp-img layout="responsive"
											src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png"
											alt="Play Icon" class="play-icon" width="74" height="74"></amp-img>
									</div>
								</div>
								<div class="card-body">
									<h3 class="card-title">Season 1</h3>
									<p class="card-desc">is simply dummy text of the printing and typesetting.</p>
								</div>
							</div>
							<div class="card">
								<div class="img-wrap">
									<amp-img
										src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/horror-2.png"
										width="600" height="375" layout="responsive" alt="a sample image"></amp-img>
									<div class="btn-play">
										<amp-img layout="responsive"
											src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png"
											alt="Play Icon" class="play-icon" width="74" height="74"></amp-img>
									</div>
								</div>
								<div class="card-body">
									<h3 class="card-title">Season 2</h3>
									<p class="card-desc">is simply dummy text of the printing and typesetting.</p>
								</div>
							</div>
							<div class="card">
								<div class="img-wrap">
									<amp-img
										src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/horror-3.png"
										width="600" height="375" layout="responsive" alt="a sample image"></amp-img>
									<div class="btn-play">
										<amp-img layout="responsive"
											src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png"
											alt="Play Icon" class="play-icon" width="74" height="74"></amp-img>
									</div>
								</div>
								<div class="card-body">
									<h3 class="card-title">Season 3</h3>
									<p class="card-desc">is simply dummy text of the printing and typesetting.</p>
								</div>
							</div>
						</amp-carousel>
					</div>
					<!-- horror cards end-->
					<!-- drama cards start-->
					<div class="sec-content" hidden [hidden]="selectedCategory.value != 'drama'">
						<amp-carousel width="600" loop height="375" layout="responsive" type="slides" role="region"
							aria-label="drama carousel">
							<div class="card">
								<div class="img-wrap">
									<amp-img
										src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/drama-1.png"
										width="600" height="375" layout="responsive" alt="a sample image"></amp-img>
									<div class="btn-play">
										<amp-img layout="responsive"
											src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png"
											alt="Play Icon" class="play-icon" width="74" height="74"></amp-img>
									</div>
								</div>
								<div class="card-body">
									<h3 class="card-title">Season 1</h3>
									<p class="card-desc">is simply dummy text of the printing and typesetting.</p>
								</div>
							</div>
							<div class="card">
								<div class="img-wrap">
									<amp-img
										src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/drama-2.png"
										width="600" height="375" layout="responsive" alt="a sample image"></amp-img>
									<div class="btn-play">
										<amp-img layout="responsive"
											src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png"
											alt="Play Icon" class="play-icon" width="74" height="74"></amp-img>
									</div>
								</div>
								<div class="card-body">
									<h3 class="card-title">Season 2</h3>
									<p class="card-desc">is simply dummy text of the printing and typesetting.</p>
								</div>
							</div>
							<div class="card">
								<div class="img-wrap">
									<amp-img
										src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/drama-3.png"
										width="600" height="375" layout="responsive" alt="a sample image"></amp-img>
									<div class="btn-play">
										<amp-img layout="responsive"
											src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png"
											alt="Play Icon" class="play-icon" width="74" height="74"></amp-img>
									</div>
								</div>
								<div class="card-body">
									<h3 class="card-title">Season 3</h3>
									<p class="card-desc">is simply dummy text of the printing and typesetting.</p>
								</div>
							</div>
						</amp-carousel>
					</div>
					<!-- comedy cards start-->
					<div class="sec-content" [hidden]="selectedCategory.value != 'action'">
						<amp-carousel loop width="600" height="375" layout="responsive" type="slides" role="region"
							aria-label="action carousel">
							<div class="card">
								<div class="img-wrap">
									<amp-img
										src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/action-1.png"
										width="600" height="375" layout="responsive" alt="a sample image"></amp-img>
									<div class="btn-play">
										<amp-img layout="responsive"
											src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png"
											alt="Play Icon" class="play-icon" width="74" height="74"></amp-img>
									</div>
								</div>
								<div class="card-body">
									<h3 class="card-title">Season 1</h3>
									<p class="card-desc">is simply dummy text of the printing and typesetting.</p>
								</div>
							</div>
							<div class="card">
								<div class="img-wrap">
									<amp-img
										src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/action-2.png"
										width="600" height="375" layout="responsive" alt="a sample image"></amp-img>
									<div class="btn-play">
										<amp-img layout="responsive"
											src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png"
											alt="Play Icon" class="play-icon" width="74" height="74"></amp-img>
									</div>
								</div>
								<div class="card-body">
									<h3 class="card-title">Season 2</h3>
									<p class="card-desc">is simply dummy text of the printing and typesetting.</p>
								</div>
							</div>
							<div class="card">
								<div class="img-wrap">
									<amp-img
										src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/action-3.png"
										width="600" height="375" layout="responsive" alt="a sample image"></amp-img>
									<div class="btn-play">
										<amp-img layout="responsive"
											src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png"
											alt="Play Icon" class="play-icon" width="74" height="74"></amp-img>
									</div>
								</div>
								<div class="card-body">
									<h3 class="card-title">Season 3</h3>
									<p class="card-desc">is simply dummy text of the printing and typesetting.</p>
								</div>
							</div>
						</amp-carousel>
					</div>
				</div>
				<!-- drama cards end-->
			</td>
		</tr>
		<!-- product section end-->
		<tr>
			<td align="center">
				<div class="section">
					<div class="sec-head">
						<div class="sec-title">
							<h2 class="text">weekly recommendations</h2>
							<div class="line"></div>
						</div>
					</div>
					<div class="sec-content">
						<ul class="movie-list">
							<li class="movie-item">
								<div class="weekly-card">
									<div class="img-wrap">
										<amp-img
											src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/weekly-1.png"
											width="245" height="161" layout="responsive" alt="weekly image"></amp-img>
									</div>
									<div class="weekly-body">
										<h3 class="weekly-title">Season Name</h3>
										<p class="weekly-desc">is simply dummy text of the printing and typesetting.</p>
									</div>
								</div>
							</li>
							<li class="movie-item">
								<div class="weekly-card">
									<div class="img-wrap">
										<amp-img
											src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/weekly-2.png"
											width="245" height="161" layout="responsive" alt="weekly image"></amp-img>
									</div>
									<div class="weekly-body">
										<h3 class="weekly-title">Season Name</h3>
										<p class="weekly-desc">is simply dummy text of the printing and typesetting.</p>
									</div>
								</div>
							</li>
						</ul>
						<div class="btn-wrap">
							<button class="btn typ-active">
								Watch More
							</button>
						</div>
					</div>
				</div>
			</td>
		</tr>
		<!-- Footer Link -->
		<tr>
			<td style="text-align: center;">
				<table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%" class="container"
					style="border-top: 2px solid #D33C3C; padding: 30px 0 40px;">
					<tr>
						<!-- Social Links -->
						<td>
							<table align="center" cellpadding="0" cellspacing="0" width="100%"
								style="text-align: center; margin-bottom: 30px;">
								<tr>
									<td style="padding: 0 16px; display: inline-block;">
										<a href="https://www.google.co.in/"><amp-img layout="responsive"
												src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/logo-insta.png"
												alt="Social Icon" class="media-logo" width="25" height="25"></amp-img>
									</td>
									<td style="padding: 0 16px; display: inline-block;">
										<a href="https://www.google.co.in/"><amp-img layout="responsive"
												src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/logo-facebook.png"
												alt="Social Icon" class="media-logo" width="25" height="25"></amp-img>
									</td>
									<td style="padding: 0 16px; display: inline-block;">
										<a href="https://www.google.co.in/"><amp-img layout="responsive"
												src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/logo-x.png"
												alt="Social Icon" class="media-logo" width="25" height="25"></amp-img>
									</td>
								</tr>
							</table>
						</td>
								<!-- Social Links -->
					</tr>
					<tr>
						<td>
							<p
								style="font-family: 'Helvetica', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 24px; color: #4F4F4F; text-align: center; max-width: 80%; margin: 0 auto; text-transform: uppercase;">
								is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the
								industry's standard dummy text ever.</p>
						</td>
					</tr>
				</table>
			</td>
		</tr>
		<tr>
			<td style="border-top: 2px solid #D33C3C">
				<p
					style="font-family: 'Helvetica', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 22px; text-align: center; color: #909090; text-transform: capitalize;  margin: 15px 0; ">
					To stop receiving these emails, <a href="https://www.google.co.in/"
						style="color: #F04444 ; font-weight: 700; text-transform: capitalize; text-decoration: none;">unsubscribe
						here</a></p>
			</td>
		</tr>
		<!-- Footer Link -->
	</table>
</body>
</html>
```
```html Resommendations with CTA
<!doctype html>
<html ⚡4email data-css-strict>
<head>
	<meta charset="utf-8">
	<script async src="https://cdn.ampproject.org/v0.js"></script>
	<script async custom-element="amp-bind" src="https://cdn.ampproject.org/v0/amp-bind-0.1.js"></script>
	<script async custom-element="amp-form" src="https://cdn.ampproject.org/v0/amp-form-0.1.js"></script>
	<script async custom-element="amp-carousel" src="https://cdn.ampproject.org/v0/amp-carousel-0.1.js"></script>
	<style amp4email-boilerplate>
		body {
			visibility: hidden
		}
	</style>
	<style amp-custom>
		* {
			margin: 0;
			padding: 0;
		}
		/* Change Theme */
		body {
			font-family: "Helvetica", arial, sans-serif;
			font-weight: 400;
			background: #F5F5F5;
		}
		/* Change Theme */
		img {
			object-fit: cover;
		}
		@media only screen and (max-width: 400px) {
			.main {
				max-width: 95%;
			}
		}
		.logo-wrap {
			padding: 15px 0;
			position: relative;
		}
		.line {
			position: absolute;
			width: 100%;
			height: 1px;
			background: #F04444;
			top: 50%;
			left: 0;
			transform: translateY(-50%);
		}
		.logo-wrap .logo {
			max-width: 157px;
			max-height: 81px;
			margin: 0 auto;
			background: #FFFFFF;
			z-index: 1;
			padding: 0 30px;
		}
		.logo-wrap img {
			object-fit: contain;
		}
		.play-btn {
			border: 1px solid #F04444;
			background: #F04444;
			font-size: 14px;
			font-weight: 400;
			line-height: 25px;
			text-transform: capitalize;
			text-align: center;
			padding: 6px 15px 6px 6px;
			display: inline-block;
			text-decoration: none;
			border-radius: 50px;
			color: #FFFFFF;
			display: flex;
			align-items: center;
		}
		.play-btn .play-icon {
			width: 31px;
			height: 31px;
			margin-right: 10px;
		}
		.banner {
			margin-bottom: 25px;
		}
		.media-logo {
			width: 25px;
			height: 25px;
		}
		.section {
			padding-bottom: 60px;
		}
		.sec-title {
			position: relative;
			margin-bottom: 12px;
		}
		.sec-title .text {
			background: #FFFFFF;
			padding: 0 25px;
			font-size: 24px;
			font-weight: 400;
			line-height: 39px;
			text-align: center;
			color: #000000;
			text-transform: uppercase;
			z-index: 1;
			display: inline-block;
			position: relative;
		}
		.sec-desc {
			font-size: 14px;
			font-weight: 400;
			line-height: 25px;
			color: #6F6F6F;
			text-align: center;
			text-transform: capitalize;
			max-width: 85%;
			margin: 0 auto 25px;
		}
		.btn {
			border: 1px solid #F04444;
			background: #FFFFFF;
			font-size: 14px;
			font-weight: 400;
			line-height: 25px;
			text-transform: capitalize;
			text-align: center;
			padding: 6px;
			display: inline-block;
			text-align: center;
			text-decoration: none;
			border-radius: 50px;
			color: #F04444;
			max-width: 113px;
			width: 100%;
			margin: 5px;
		}
		.btn.typ-active {
			background: #F04444;
			color: #FFFFFF;
		}
		.category-btn-wrap {
			margin: 0 0 38px;
		}
		.img-wrap,
		.card {
			position: relative;
		}
		.btn-play {
			position: absolute;
			width: 74px;
			height: 74px;
			top: 50%;
			left: 50%;
			transform: translate(-50%, -50%);
		}
		.btn-play img {
			object-fit: contain;
		}
		.card .card-body {
			position: absolute;
			bottom: 0;
			left: 0;
			width: 100%;
			background: #00000080;
			padding: 18px 0;
			display: flex;
			justify-content: space-between;
			align-items: flex-start;
		}
		.card .card-body .lhs {
			width: 70%;
		}
		.card .card-body .rhs {
			width: 30%;
			position: relative;
		}
		.card .card-title {
			font-size: 20px;
			font-weight: 400;
			line-height: 25px;
			text-align: left;
			color: #FFFFFF;
			margin: 0 18px 5px;
			text-transform: uppercase;
		}
		.card .card-desc {
			font-size: 14px;
			font-weight: 400;
			line-height: 25px;
			text-align: left;
			color: #FFFFFF;
			margin: 0 18px;
			text-transform: capitalize;
		}
		.movie-list {
			list-style: none;
			display: flex;
			justify-content: space-between;
			gap: 20px;
			max-width: 88%;
			margin: 0 auto;
		}
		.movie-list .movie-item {
			width: 48%;
		}
		.weekly-card .weekly-body {
			padding: 7px 0;
		}
		.weekly-card .weekly-title {
			font-size: 14px;
			font-weight: 400;
			line-height: 25px;
			color: #000000;
			text-align: left;
			text-transform: uppercase;
		}
		.weekly-card .weekly-desc {
			font-size: 10px;
			font-weight: 400;
			line-height: 15px;
			color: #6F6F6F;
			text-align: left;
			text-transform: capitalize;
		}
		.btn-wrap {
			margin-top: 30px;
		}
		.notify-btn {
			border: 1px solid #F04444;
			background: #F04444;
			font-size: 14px;
			font-weight: 400;
			line-height: 25px;
			text-transform: capitalize;
			text-align: center;
			padding: 6px 12px;
			text-align: center;
			border-radius: 50px;
			color: #FFFFFF;
			text-transform: uppercase;
			margin: 5px;
			display: flex;
			align-items: center;
		}
		.notify-btn .notify-icon {
			width: 19px;
			height: 21px;
			margin-left: 10px;
		}
		.notify-btn.typ-opacity {
			border: 1px solid #FFB8B8;
			background: #FFB8B8;
		}
		.notify-note {
			position: absolute;
			top: -56px;
			right: 15px;
			background: #FFFFFF;
			border-radius: 10px;
			border-bottom: 2px solid #F04444;
			padding: 5px 10px;
		}
		.notify-note .n-title {
			font-size: 14px;
			font-weight: 500;
			line-height: 29px;
			color: #000000;
			text-align: center;
			text-transform: uppercase;
		}
		.notify-note .n-desc {
			font-size: 12px;
			font-weight: 400;
			line-height: 18px;
			text-align: center;
			color: #606060;
		}
		@media only screen and (max-width: 400px) {
			.logo-wrap .logo {
				max-width: 130px;
				max-height: 70px;
			}
			.sec-title .text {
				font-size: 20px;
				font-weight: 400;
				padding: 0 10px;
			}
			.sec-desc {
				line-height: 20px;
			}
			.card .card-title {
				font-size: 18px;
				line-height: 20px;
				margin: 0 10px 5px;
			}
			.card .card-desc {
				font-size: 12px;
				line-height: 18px;
				margin: 0 10px;
			}
		}
	</style>
</head>
<body>
	<!-- AMP state for handling category selection -->
	<amp-state id="selectedCategory">
		<script type="application/json">
			{
				"value": "action" 
			}
		</script>
	</amp-state>
	<!-- Change Theme -->
	<table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%"
		style="max-width: 600px; margin: 0 auto; background-color: #FFFFFF;" class="main">
		<!-- header start-->
		<tr>
			<td align="center" style="padding: 5px 0;">
				<div class="logo-wrap">
					<div class="line"></div>
					<!-- Change Logo Image src as per your requirements -->
					<amp-img layout="responsive"
						src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/logo.png"
						alt="Logo" width="157" height="81" class="logo" />
					<!-- Change Logo Image src as per your requirements -->
				</div>
			</td>
		</tr>
		<!-- header end-->
		<!-- Banner Image-->
		<tr>
			<td align="center">
				<div class="banner">
					<amp-img
						src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/banner.png"
						width="600" height="280" layout="responsive" alt="a sample image"></amp-img>
				</div>
			</td>
		</tr>
		<!-- Banner Image-->
		<!-- new episodes start-->
		<tr>
			<td align="center">
				<div class="section">
					<div class="sec-head">
						<div class="sec-title">
							<h2 class="text">new episodes</h2>
							<div class="line"></div>
						</div>
						<p class="sec-desc">is simply dummy text of the printing and typesetting industry. is simply
							dummy text of the printing and typesetting industry.</p>
						<button class="play-btn">
							<amp-img layout="responsive"
								src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png"
								alt="Play Icon" class="play-icon" width="31" height="31"></amp-img> Watch now
						</button>
					</div>
				</div>
			</td>
		</tr>
		<!-- new episodes end-->
		<!-- product section start-->
		<tr>
			<td align="center">
				<div class="section">
					<div class="sec-head">
						<div class="sec-title">
							<h2 class="text">new collection</h2>
							<div class="line"></div>
						</div>
						<p class="sec-desc">is simply dummy text of the printing and typesetting industry. is simply
							dummy text of the printing and typesetting industry.</p>
						<div class="category-btn-wrap">
							<button class="btn typ-active"
								[class]="'btn ' + (selectedCategory.value == 'action' ? 'btn typ-active' : '')"
								value="action" on="tap:AMP.setState({selectedCategory: {value: 'action'}})">
								Action
							</button>
							<button class="btn"
								[class]="'btn ' + (selectedCategory.value == 'horror' ? 'btn typ-active' : '')"
								value="horror" on="tap:AMP.setState({selectedCategory: {value: 'horror'}})">
								Horror
							</button>
							<button class="btn"
								[class]="'btn ' + (selectedCategory.value == 'drama' ? 'btn typ-active' : '')"
								value="drama" on="tap:AMP.setState({selectedCategory: {value: 'drama'}})">
								Drama
							</button>
							<button class="btn"
								[class]="'btn ' + (selectedCategory.value == 'Comedy' ? 'btn typ-active' : '')"
								value="Comedy" on="tap:AMP.setState({selectedCategory: {value: 'Comedy'}})">
								Comedy
							</button>
						</div>
					</div>
					<!-- action cards start-->
					<div class="sec-content" [hidden]="selectedCategory.value != 'action'">
						<!-- Change Carousel Image -->
						<amp-carousel width="600" height="375" layout="responsive" type="slides" role="region"
							aria-label="action carousel">
							<div class="card">
								<div class="img-wrap">
									<!-- Carousel Image  -->
									<amp-img
										src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/action-1.png"
										width="600" height="375" layout="responsive" alt="a sample image"></amp-img>
									<div class="btn-play">
										<amp-img layout="responsive"
											src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png"
											alt="Play Icon" class="play-icon" width="18" height="21"></amp-img>
									</div>
								</div>
								<div class="card-body">
									<div class="lhs">
										<h3 class="card-title">Season 1</h3>
										<p class="card-desc">is simply dummy text of the printing and typesetting.</p>
									</div>
									<div class="rhs">
										<button class="notify-btn"
											[class]="'notify-btn ' + (showNotify ? 'typ-opacity' : '')"
											on="tap:AMP.setState({ showNotify: true })"> notify me <amp-img
												layout="responsive"
												src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/bell-icon.png"
												alt="Bell Icon" class="notify-icon" width="18" height="21"></amp-img>
										</button>
										<div class="notify-note" hidden [hidden]="!showNotify">
											<h3 class="n-title">Thank you</h3>
											<p class="n-desc">You'll get all notifications</p>
										</div>
									</div>
								</div>
							</div>
							<div class="card">
								<div class="img-wrap">
									<amp-img
										src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/action-2.png"
										width="600" height="375" layout="responsive" alt="a sample image"></amp-img>
									<div class="btn-play">
										<amp-img layout="responsive"
											src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png"
											alt="Play Icon" class="play-icon" width="74" height="74"></amp-img>
									</div>
								</div>
								<div class="card-body">
									<div class="lhs">
										<h3 class="card-title">Season 2</h3>
										<p class="card-desc">is simply dummy text of the printing and typesetting.</p>
									</div>
									<div class="rhs">
										<button class="notify-btn" on="tap:AMP.setState({ showNotify1: true })"
											[class]="'notify-btn ' + (showNotify1 ? 'typ-opacity' : '')"
											on="tap:AMP.setState({ showNotify: true })"> notify me <amp-img
												layout="responsive"
												src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/bell-icon.png"
												alt="Bell Icon" class="notify-icon" width="18" height="21"></amp-img>
										</button>
										<div class="notify-note" hidden [hidden]="!showNotify1">
											<h3 class="n-title">Thank you</h3>
											<p class="n-desc">You'll get all notifications</p>
										</div>
									</div>
								</div>
							</div>
							<div class="card">
								<div class="img-wrap">
									<amp-img
										src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/action-3.png"
										width="600" height="375" layout="responsive" alt="a sample image"></amp-img>
									<div class="btn-play">
										<amp-img layout="responsive"
											src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png"
											alt="Play Icon" class="play-icon" width="74" height="74"></amp-img>
									</div>
								</div>
								<div class="card-body">
									<div class="lhs">
										<h3 class="card-title">Season 3</h3>
										<p class="card-desc">is simply dummy text of the printing and typesetting.</p>
									</div>
									<div class="rhs">
										<button class="notify-btn" on="tap:AMP.setState({ showNotify2: true })"
											[class]="'notify-btn ' + (showNotify2 ? 'typ-opacity' : '')"
											on="tap:AMP.setState({ showNotify: true })"> notify me <amp-img
												layout="responsive"
												src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/bell-icon.png"
												alt="Bell Icon" class="notify-icon" width="18" height="21"></amp-img>
										</button>
										<div class="notify-note" hidden [hidden]="!showNotify2">
											<h3 class="n-title">Thank you</h3>
											<p class="n-desc">You'll get all notifications</p>
										</div>
									</div>
								</div>
							</div>
						</amp-carousel>
						<!-- Change Carousel Image -->
					</div>
					<!-- action cards end-->
					<!-- horror cards start-->
					<div class="sec-content" hidden [hidden]="selectedCategory.value != 'horror'">
						<amp-carousel width="600" height="375" layout="responsive" type="slides" role="region"
							aria-label="horror carousel">
							<div class="card">
								<div class="img-wrap">
									<amp-img
										src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/horror-1.png"
										width="600" height="375" layout="responsive" alt="a sample image"></amp-img>
									<div class="btn-play">
										<amp-img layout="responsive"
											src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png"
											alt="Play Icon" class="play-icon" width="74" height="74"></amp-img>
									</div>
								</div>
								<div class="card-body">
									<div class="lhs">
										<h3 class="card-title">Season 1</h3>
										<p class="card-desc">is simply dummy text of the printing and typesetting.</p>
									</div>
									<div class="rhs">
										<button class="notify-btn" on="tap:AMP.setState({ showNotifyHorror1: true })"
											[class]="'notify-btn ' + (showNotifyHorror1 ? 'typ-opacity' : '')"
											on="tap:AMP.setState({ showNotifyHorror1: true })">notify me <amp-img
												layout="responsive"
												src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/bell-icon.png"
												alt="Bell Icon" class="notify-icon" width="18" height="21"></amp-img>
										</button>
										<div class="notify-note" hidden [hidden]="!showNotifyHorror1">
											<h3 class="n-title">Thank you</h3>
											<p class="n-desc">You'll get all notifications</p>
										</div>
									</div>
								</div>
							</div>
							<div class="card">
								<div class="img-wrap">
									<amp-img
										src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/horror-2.png"
										width="600" height="375" layout="responsive" alt="a sample image"></amp-img>
									<div class="btn-play">
										<amp-img layout="responsive"
											src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png"
											alt="Play Icon" class="play-icon" width="74" height="74"></amp-img>
									</div>
								</div>
								<div class="card-body">
									<div class="lhs">
										<h3 class="card-title">Season 2</h3>
										<p class="card-desc">is simply dummy text of the printing and typesetting.</p>
									</div>
									<div class="rhs">
										<button class="notify-btn" on="tap:AMP.setState({ showNotifyHorror2: true })"
											[class]="'notify-btn ' + (showNotifyHorror2 ? 'typ-opacity' : '')"> notify
											me <amp-img layout="responsive"
												src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/bell-icon.png"
												alt="Bell Icon" class="notify-icon" width="18" height="21"></amp-img>
										</button>
										<div class="notify-note" hidden [hidden]="!showNotifyHorror2">
											<h3 class="n-title">Thank you</h3>
											<p class="n-desc">You'll get all notifications</p>
										</div>
									</div>
								</div>
							</div>
							<div class="card">
								<div class="img-wrap">
									<amp-img
										src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/horror-3.png"
										width="600" height="375" layout="responsive" alt="a sample image"></amp-img>
									<div class="btn-play">
										<amp-img layout="responsive"
											src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png"
											alt="Play Icon" class="play-icon" width="74" height="74"></amp-img>
									</div>
								</div>
								<div class="card-body">
									<div class="lhs">
										<h3 class="card-title">Season 3</h3>
										<p class="card-desc">is simply dummy text of the printing and typesetting.</p>
									</div>
									<div class="rhs">
										<button class="notify-btn" on="tap:AMP.setState({ showNotifyHorror3: true })"
											[class]="'notify-btn ' + (showNotifyHorror3 ? 'typ-opacity' : '')"> notify
											me <amp-img layout="responsive"
												src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/bell-icon.png"
												alt="Bell Icon" class="notify-icon" width="18" height="21"></amp-img>
										</button>
										<div class="notify-note" hidden [hidden]="!showNotifyHorror3">
											<h3 class="n-title">Thank you</h3>
											<p class="n-desc">You'll get all notifications</p>
										</div>
									</div>
								</div>
							</div>
						</amp-carousel>
					</div>
					<!-- horror cards end-->
					<!-- drama cards start-->
					<div class="sec-content" hidden [hidden]="selectedCategory.value != 'drama'">
						<amp-carousel width="600" height="375" layout="responsive" type="slides" role="region"
							aria-label="drama carousel">
							<div class="card">
								<div class="img-wrap">
									<amp-img
										src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/drama-1.png"
										width="600" height="375" layout="responsive" alt="a sample image"></amp-img>
									<div class="btn-play">
										<amp-img layout="responsive"
											src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png"
											alt="Play Icon" class="play-icon" width="74" height="74"></amp-img>
									</div>
								</div>
								<div class="card-body">
									<div class="lhs">
										<h3 class="card-title">Season 1</h3>
										<p class="card-desc">is simply dummy text of the printing and typesetting.</p>
									</div>
									<div class="rhs">
										<button class="notify-btn" on="tap:AMP.setState({ showNotifyDrama1: true })"
											[class]="'notify-btn ' + (showNotifyDrama1 ? 'typ-opacity' : '')"> notify me
											<amp-img layout="responsive"
												src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/bell-icon.png"
												alt="Bell Icon" class="notify-icon" width="18" height="21"></amp-img>
										</button>
										<div class="notify-note" hidden [hidden]="!showNotifyDrama1">
											<h3 class="n-title">Thank you</h3>
											<p class="n-desc">You'll get all notifications</p>
										</div>
									</div>
								</div>
							</div>
							<div class="card">
								<div class="img-wrap">
									<amp-img
										src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/drama-2.png"
										width="600" height="375" layout="responsive" alt="a sample image"></amp-img>
									<div class="btn-play">
										<amp-img layout="responsive"
											src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png"
											alt="Play Icon" class="play-icon" width="74" height="74"></amp-img>
									</div>
								</div>
								<div class="card-body">
									<div class="lhs">
										<h3 class="card-title">Season 2</h3>
										<p class="card-desc">is simply dummy text of the printing and typesetting.</p>
									</div>
									<div class="rhs">
										<button class="notify-btn" on="tap:AMP.setState({ showNotifyDrama2: true })"
											[class]="'notify-btn ' + (showNotifyDrama2 ? 'typ-opacity' : '')"> notify me
											<amp-img layout="responsive"
												src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/bell-icon.png"
												alt="Bell Icon" class="notify-icon" width="18" height="21"></amp-img>
										</button>
										<div class="notify-note" hidden [hidden]="!showNotifyDrama2">
											<h3 class="n-title">Thank you</h3>
											<p class="n-desc">You'll get all notifications</p>
										</div>
									</div>
								</div>
							</div>
							<div class="card">
								<div class="img-wrap">
									<amp-img
										src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/drama-3.png"
										width="600" height="375" layout="responsive" alt="a sample image"></amp-img>
									<div class="btn-play">
										<amp-img layout="responsive"
											src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png"
											alt="Play Icon" class="play-icon" width="74" height="74"></amp-img>
									</div>
								</div>
								<div class="card-body">
									<div class="lhs">
										<h3 class="card-title">Season 3</h3>
										<p class="card-desc">is simply dummy text of the printing and typesetting.</p>
									</div>
									<div class="rhs">
										<button class="notify-btn" on="tap:AMP.setState({ showNotifyDrama3: true })"
											[class]="'notify-btn ' + (showNotifyDrama3 ? 'typ-opacity' : '')"> notify me
											<amp-img layout="responsive"
												src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/bell-icon.png"
												alt="Bell Icon" class="notify-icon" width="18" height="21"></amp-img>
										</button>
										<div class="notify-note" hidden [hidden]="!showNotifyDrama3">
											<h3 class="n-title">Thank you</h3>
											<p class="n-desc">You'll get all notifications</p>
										</div>
									</div>
								</div>
							</div>
						</amp-carousel>
					</div>
							<!-- Comedy cards start-->
							<div class="sec-content" [hidden]="selectedCategory.value != 'action'">
								<!-- Change Carousel Image -->
								<amp-carousel width="600" height="375" layout="responsive" type="slides" role="region"
									aria-label="action carousel">
									<div class="card">
										<div class="img-wrap">
											<!-- Carousel Image  -->
											<amp-img
												src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/action-1.png"
												width="600" height="375" layout="responsive" alt="a sample image"></amp-img>
											<div class="btn-play">
												<amp-img layout="responsive"
													src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png"
													alt="Play Icon" class="play-icon" width="18" height="21"></amp-img>
											</div>
										</div>
										<div class="card-body">
											<div class="lhs">
												<h3 class="card-title">Season 1</h3>
												<p class="card-desc">is simply dummy text of the printing and typesetting.</p>
											</div>
											<div class="rhs">
												<button class="notify-btn"
													[class]="'notify-btn ' + (showNotify ? 'typ-opacity' : '')"
													on="tap:AMP.setState({ showNotify: true })"> notify me <amp-img
														layout="responsive"
														src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/bell-icon.png"
														alt="Bell Icon" class="notify-icon" width="18" height="21"></amp-img>
												</button>
												<div class="notify-note" hidden [hidden]="!showNotify">
													<h3 class="n-title">Thank you</h3>
													<p class="n-desc">You'll get all notifications</p>
												</div>
											</div>
										</div>
									</div>
									<div class="card">
										<div class="img-wrap">
											<amp-img
												src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/action-2.png"
												width="600" height="375" layout="responsive" alt="a sample image"></amp-img>
											<div class="btn-play">
												<amp-img layout="responsive"
													src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png"
													alt="Play Icon" class="play-icon" width="74" height="74"></amp-img>
											</div>
										</div>
										<div class="card-body">
											<div class="lhs">
												<h3 class="card-title">Season 2</h3>
												<p class="card-desc">is simply dummy text of the printing and typesetting.</p>
											</div>
											<div class="rhs">
												<button class="notify-btn" on="tap:AMP.setState({ showNotify1: true })"
													[class]="'notify-btn ' + (showNotify1 ? 'typ-opacity' : '')"
													on="tap:AMP.setState({ showNotify: true })"> notify me <amp-img
														layout="responsive"
														src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/bell-icon.png"
														alt="Bell Icon" class="notify-icon" width="18" height="21"></amp-img>
												</button>
												<div class="notify-note" hidden [hidden]="!showNotify1">
													<h3 class="n-title">Thank you</h3>
													<p class="n-desc">You'll get all notifications</p>
												</div>
											</div>
										</div>
									</div>
									<div class="card">
										<div class="img-wrap">
											<amp-img
												src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/action-3.png"
												width="600" height="375" layout="responsive" alt="a sample image"></amp-img>
											<div class="btn-play">
												<amp-img layout="responsive"
													src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png"
													alt="Play Icon" class="play-icon" width="74" height="74"></amp-img>
											</div>
										</div>
										<div class="card-body">
											<div class="lhs">
												<h3 class="card-title">Season 3</h3>
												<p class="card-desc">is simply dummy text of the printing and typesetting.</p>
											</div>
											<div class="rhs">
												<button class="notify-btn" on="tap:AMP.setState({ showNotify2: true })"
													[class]="'notify-btn ' + (showNotify2 ? 'typ-opacity' : '')"
													on="tap:AMP.setState({ showNotify: true })"> notify me <amp-img
														layout="responsive"
														src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/bell-icon.png"
														alt="Bell Icon" class="notify-icon" width="18" height="21"></amp-img>
												</button>
												<div class="notify-note" hidden [hidden]="!showNotify2">
													<h3 class="n-title">Thank you</h3>
													<p class="n-desc">You'll get all notifications</p>
												</div>
											</div>
										</div>
									</div>
								</amp-carousel>
								<!-- Change Carousel Image -->
							</div>
							 		<!-- Comedy cards start-->
				</div>
				<!-- drama cards end-->
			</td>
		</tr>
		<!-- product section end-->
		<tr>
			<td align="center">
				<div class="section">
					<div class="sec-head">
						<div class="sec-title">
							<h2 class="text">weekly recommendations</h2>
							<div class="line"></div>
						</div>
					</div>
					<div class="sec-content">
						<ul class="movie-list">
							<li class="movie-item">
								<div class="weekly-card">
									<div class="img-wrap">
										<amp-img
											src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/weekly-1.png"
											width="245" height="161" layout="responsive" alt="weekly image"></amp-img>
									</div>
									<div class="weekly-body">
										<h3 class="weekly-title">Season Name</h3>
										<p class="weekly-desc">is simply dummy text of the printing and typesetting.</p>
									</div>
								</div>
							</li>
							<li class="movie-item">
								<div class="weekly-card">
									<div class="img-wrap">
										<amp-img
											src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/weekly-2.png"
											width="245" height="161" layout="responsive" alt="weekly image"></amp-img>
									</div>
									<div class="weekly-body">
										<h3 class="weekly-title">Season Name</h3>
										<p class="weekly-desc">is simply dummy text of the printing and typesetting.</p>
									</div>
								</div>
							</li>
						</ul>
						<div class="btn-wrap">
							<!-- Change CTA -->
							<button class="btn typ-active">
								Watch More
							</button>
							<!-- Change CTA -->
						</div>
					</div>
				</div>
			</td>
		</tr>
		<!-- Footer Section-->
		<tr>
			<td style="text-align: center;">
				<table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%" class="container"
					style="border-top: 2px solid #D33C3C; padding: 30px 0 40px;">
					<tr>
						<td>
							<table align="center" cellpadding="0" cellspacing="0" width="100%"
								style="text-align: center; margin-bottom: 30px;">
								<!-- Social Link -->
								<tr>
									<td style="padding: 0 16px; display: inline-block;">
										<a href="https://www.google.co.in/"><amp-img layout="responsive"
												src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/logo-insta.png"
												alt="Social Icon" class="media-logo" width="25" height="25"></amp-img>
									</td>
									<td style="padding: 0 16px; display: inline-block;">
										<a href="https://www.google.co.in/"><amp-img layout="responsive"
												src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/logo-facebook.png"
												alt="Social Icon" class="media-logo" width="25" height="25"></amp-img>
									</td>
									<td style="padding: 0 16px; display: inline-block;">
										<a href="https://www.google.co.in/"><amp-img layout="responsive"
												src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/logo-x.png"
												alt="Social Icon" class="media-logo" width="25" height="25"></amp-img>
									</td>
								</tr>
								<!-- Social Link -->
							</table>
						</td>
					</tr>
					<tr>
						<td>
							<p
								style="font-family: 'Helvetica', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 24px; color: #4F4F4F; text-align: center; max-width: 80%; margin: 0 auto; text-transform: uppercase;">
								is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the
								industry's standard dummy text ever.</p>
						</td>
					</tr>
				</table>
			</td>
		</tr>
		<tr>
			<td style="border-top: 2px solid #D33C3C">
				<p
					style="font-family: 'Helvetica', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 22px; text-align: center; color: #909090; text-transform: capitalize;  margin: 15px 0; ">
					To stop receiving these emails, <a href="https://www.google.co.in/"
						style="color: #F04444 ; font-weight: 700; text-transform: capitalize; text-decoration: none;">unsubscribe
						here</a></p>
			</td>
		</tr>
		<!-- Footer Section-->
	</table>
</body>
</html>
```

</details>

## Feedback

This AMP template enables brands to collect real-time customer feedback directly from within the email. With an embedded form and AMP-powered interactivity, users can respond to surveys, ratings, or open-ended feedback requests without leaving their inbox, improving response rates and offering a smoother user experience.

<details>

<summary>Expand to know more about the template.</summary>

### Use Case Examples

- Collect post-purchase feedback to improve product or service quality.
- Trigger surveys after support interactions or delivery completion.
- Capture Net Promoter Score (NPS) and satisfaction scores.
- Gather insights during product beta testing or soft launches.

### Template Customization Options

- Replace the Logo
- Update Banner/Product Images
- Update Call-To-Actions (CTAs)
- Update Links in the Header/Footer
- Change the Theme or Background Color
- Update Social Media Links and Download Links

### Template Code

```html
<!DOCTYPE html>
<html ⚡4email data-css-strict>
<head>
    <meta charset="utf-8">
    <script async src="https://cdn.ampproject.org/v0.js"></script>
    <script async custom-element="amp-form" src="https://cdn.ampproject.org/v0/amp-form-0.1.js"></script>
    <script async custom-element="amp-bind" src="https://cdn.ampproject.org/v0/amp-bind-0.1.js"></script>
    <style amp4email-boilerplate>
        body {
            visibility: hidden
        }
    </style>
    <style amp-custom>
        * {
            margin: 0;
            padding: 0;
        }
        /* Change Theme */
        body {
            font-family: "Helvetica", arial, sans-serif;
            font-weight: 400;
            background-color: #f5f5f5;
        }
        /* Change Theme */
        img {
            width: 100%;
            height: 100%;
            object-fit: contain;
        }
        .table-container {
            max-width: 90%;
            background: #FFFFFF;
            margin-top: -60px;
        }
        .container {
            max-width: 85%;
            margin: 0 auto;
        }
        @media screen and (max-width: 480px) {
            .container {
                max-width: 90%;
            }
            .table-container {
                max-width: 95%;
            }
            .logo {
                width: 150px;
                height: 60px;
            }
        }
        .form-container {
            padding: 34px 20px;
            position: relative;
        }
        .field-wrap {
            padding: 40px 0;
            border-bottom: 1px solid #ADADAD;
        }
        .field-wrap.typ-last {
            border-bottom: none;
        }
        .field-wrap .field-label {
            font-size: 16px;
            font-weight: 400;
            line-height: 20px;
            color: #000000;
            text-transform: capitalize;
            margin-bottom: 25px;
            display: flex;
            align-items: center;
        }
        .field-wrap .marker {
            width: 20px;
            height: 20px;
            background: #5A3D2B;
            margin-right: 15px;
            display: inline-block;
        }
        .field-wrap .input-list {
            margin-left: 30px;
            list-style: none;
            display: flex;
            align-items: center;
            justify-content: flex-start;
            flex-wrap: wrap;
        }
        .radio-input {
            display: none;
            visibility: hidden;
            appearance: none;
        }
        .radio-field {
            cursor: pointer;
        }
        .field-wrap .input-list .input-item {
            margin-right: 25px;
        }
        .field-wrap .input-list .input-item.full-width {
            width: 100%;
        }
        .field-wrap .radio-field.thumb {
            display: flex;
            align-items: center;
        }
        .field-wrap .radio-field.thumb .radio-img {
            width: 34px;
            height: 34px;
            display: inline-block;
            background: transparent url('https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/feedback-html/icon-thumbsUp.png');
            background-position: 0 0;
            background-repeat: no-repeat;
            background-size: contain;
        }
        .field-wrap .radio-field.thumb input[type=radio]:checked+.radio-img {
            background: transparent url('https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/feedback-html/icon-fill-thumbsUp.png');
            background-size: contain;
        }
        .field-wrap .radio-field.thumb.thumb-down .radio-img {
            transform: rotate(180deg);
        }
        .field-wrap .radio-field.thumb .text {
            font-size: 16px;
            font-weight: 400;
            line-height: 20px;
            color: #595959;
            margin-left: 10px;
        }
        /* styling for rating */
        .field-wrap .radio-field.star .radio-img {
            width: 28px;
            height: 28px;
            display: inline-block;
            background: transparent url('https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/feedback-html/icon-star.png');
            background-position: 0 0;
            background-repeat: no-repeat;
            background-size: contain;
        }
        .field-wrap .radio-field.star input[type=radio]:checked+.radio-img {
            background: transparent url('https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/feedback-html/icon-fill-star.png');
            background-size: contain;
        }
        /* styling for smiley */
        .field-wrap .radio-field.smiley .radio-img {
            width: 38px;
            height: 38px;
            display: inline-block;
            background: transparent url('https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/feedback-html/icon-smile3.png');
            background-position: 0 0;
            background-repeat: no-repeat;
            background-size: contain;
        }
        .field-wrap .radio-field.smiley input[type=radio]:checked+.radio-img {
            background: transparent url('https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/feedback-html/icon-fill-smile3.png');
            background-size: contain;
        }
        .field-wrap .radio-field.smiley.smiley-normal .radio-img {
            background: transparent url('https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/feedback-html/icon-smile2.png');
            background-size: contain;
        }
        .field-wrap .radio-field.smiley.smiley-normal input[type=radio]:checked+.radio-img {
            background: transparent url('https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/feedback-html/icon-fill-smile2.png');
            background-size: contain;
        }
        .field-wrap .radio-field.smiley.smiley-sad .radio-img {
            background: transparent url('https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/feedback-html/icon-smile1.png');
            background-size: contain;
        }
        .field-wrap .radio-field.smiley.smiley-sad input[type=radio]:checked+.radio-img {
            background: transparent url('https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/feedback-html/icon-fill-smile1.png');
            background-size: contain;
        }
        .field-wrap .input {
            width: 100%;
            height: 81px;
            border: 1px solid #A9A9A9;
            border-radius: 5px;
            resize: none;
            padding: 10px;
            font-size: 14px;
            font-weight: 400;
            line-height: 20.56px;
            color: #A2A2A2;
            ;
        }
        .field-wrap .field-head {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
        }
        .field-wrap .field-head .remove {
            border: none;
            background: transparent;
        }
        .field-wrap .field-head .remove .remove-logo {
            width: 22px;
            height: 22px;
        }
        .submit-cta {
            display: inline-block;
            background-color: #5A3D2B;
            font-size: 20px;
            font-weight: 400;
            line-height: 22px;
            text-align: center;
            color: #FFFFFF;
            text-transform: uppercase;
            border-radius: 5px;
            text-decoration: none;
            padding: 14px 10px;
            width: 100%;
            border: 0;
            outline: 0;
        }
        .submit-cta.disable {
            background: #D1D1D1;
        }
        .success-container {
            border: 1px solid #5A3D2B;
            text-align: center;
            padding: 10px 30px;
            box-shadow: 2px 4px 4px 0px #00000040;
            z-index: 2;
            position: absolute;
            left: 50%;
            bottom: -72px;
            width: 80%;
            transform: translateX(-50%);
            background: #FFFFFF;
        }
        .success-container .title {
            font-size: 20px;
            font-weight: 400;
            line-height: 28px;
            color: #000000;
            text-transform: capitalize;
            margin-bottom: 5px;
        }
        .success-container .para {
            font-size: 10px;
            font-weight: 400;
            line-height: 15px;
            color: #7D7D7D;
            text-transform: capitalize;
        }
        .hidden {
            display: none;
        }
        .show {
            display: block;
        }
        .main-title {
            margin: 0 0 8px;
            font-family: 'Helvetica', Arial, sans-serif;
            font-size: 32px;
            font-weight: 400;
            color: #FFFFFF;
            line-height: 32px;
            text-align: center;
            text-transform: uppercase;
        }
        .main-desc {
            margin: 0;
            text-transform: uppercase;
            font-family: 'Helvetica', Arial, sans-serif;
            font-size: 12px;
            font-weight: 400;
            line-height: 20px;
            text-align: center;
            color: #FFFFFF;
        }
        .form-title {
            text-transform: capitalize;
            font-size: 32px;
            font-weight: 400;
            line-height: 46px;
            text-align: center;
            color: #000000;
            margin-bottom: 9px;
        }
        @media screen and (max-width: 480px) {
            .main-title,
            .form-title {
                font-size: 28px;
                line-height: 38px;
            }
            .field-wrap {
                padding: 20px 0;
            }
            .field-wrap .marker {
                width: 10px;
                height: 10px;
            }
            .field-wrap .field-label {
                font-size: 14px;
                line-height: 18px;
                margin-bottom: 20px;
            }
            .field-wrap .input-list .input-item {
                margin-right: 15px;
            }
            .field-wrap .radio-field.thumb .radio-img,
            .field-wrap .radio-field.star .radio-img,
            .field-wrap .radio-field.smiley .radio-img {
                width: 25px;
                height: 25px;
            }
            .submit-cta {
                font-size: 16px;
                line-height: 18px;
                padding: 10px;
            }
        }
    </style>
</head>
<body style="font-family: 'Helvetica', Arial, sans-serif; font-weight: 400; margin: 0; padding: 0;">
    <table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%"
        style="max-width: 600px; margin: 0 auto; background-color: #FFFFFF; border-spacing: 0;">
        <!-- header start-->
        <tr>
            <td align="center" style="display: block; padding: 20px 0; max-width: 90%; margin: 0 auto;"
                class="container">
                <div class="logo-wrap">
                    <!-- Change Logo image src as per your requirements -->
                    <amp-img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/feedback-html/logo.png"
                        width="159" height="73" layout="fixed" class="logo" alt="Logo">
                    </amp-img>
                    <!-- Change Logo image src as per your requirements -->
                </div>
            </td>
        </tr>
        <!-- header end-->
        <tr>
            <td style="background: #5A3D2B;">
                <!-- Change banner image src as per your requirements -->
                <amp-img layout="responsive"
                    src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/feedback-html/banner.jpg"
                    alt="Banner" width="600" height="360" />
                <!-- Change banner image src as per your requirements -->
            </td>
        </tr>
        <tr>
            <td align="center" style="padding: 28px 0 96px; background: #5A3D2B;">
                <div class="container">
                    <h2 class="main-title"
                        style="margin: 0 0 8px; font-family: 'Helvetica', Arial, sans-serif; font-size: 32px; font-weight: 400; color: #FFFFFF; line-height: 32px; text-align: center; text-transform: uppercase;">
                        Feedback form</h2>
                    <p class="main-desc">is simply dummy text of the printing and typesetting is simply dummy text of
                        the printing and typesetting industry.</p>
                </div>
            </td>
        </tr>
        <tr>
            <td align="center" style="background: gray; padding-bottom: 30px;">
                <table role="presentation" cellspacing="0" cellpadding="0" border="0" align="center" width="100%"
                    class="table-container">
                    <tr>
                        <td>
                            <div class="form-container">
                                <h2 class="form-title">questions</h2>
                                <form method="post" action-xhr="https://example.com/submit" id="feedbackForm"
                                    enctype="multipart/form-data"
                                    on="submit-success:AMP.setState({successVisible: false})">
                                    <!-- Question 1 -->
                                    <div class="field-wrap">
                                        <h3 class="field-label"><span class="marker"></span>Are you satisfied with the
                                            comfort level of our shoes?</h3>
                                        <ul class="input-list">
                                            <li class="input-item">
                                                <label class="radio-field thumb thumb-up" for="thumbUp">
                                                    <input type="radio" name="satisfied" value="thumb-up"
                                                        class="radio-input" id="thumbUp">
                                                    <span class="radio-img"></span>
                                                    <span class="text">Yes</span>
                                                    </lab>
                                            </li>
                                            <li class="input-item">
                                                <label class="radio-field thumb thumb-down" for="thumbDown">
                                                    <input type="radio" name="satisfied" value="thumb-down"
                                                        class="radio-input" id="thumbDown">
                                                    <span class="radio-img"></span>
                                                    <span class="text">No</span>
                                                </label>
                                            </li>
                                        </ul>
                                    </div>
                                    <!-- Question 2 -->
                                    <div class="field-wrap">
                                        <h3 class="field-label"><span class="marker"></span>How would you rate the
                                            quality of our shoes?</h3>
                                        <ul class="input-list">
                                            <li class="input-item">
                                                <label class="radio-field star" for="star1">
                                                    <input type="radio" name="rate" value="star1" class="radio-input"
                                                        id="star1">
                                                    <span class="radio-img"></span>
                                                </label>
                                            </li>
                                            <li class="input-item">
                                                <label class="radio-field star" for="star2">
                                                    <input type="radio" name="rate" value="star2" class="radio-input"
                                                        id="star2">
                                                    <span class="radio-img"></span>
                                                </label>
                                            </li>
                                            <li class="input-item">
                                                <label class="radio-field star" for="star3">
                                                    <input type="radio" name="rate" value="star3" class="radio-input"
                                                        id="star3">
                                                    <span class="radio-img"></span>
                                                </label>
                                            </li>
                                            <li class="input-item">
                                                <label class="radio-field star" for="star4">
                                                    <input type="radio" name="rate" value="star4" class="radio-input"
                                                        id="star4">
                                                    <span class="radio-img"></span>
                                                </label>
                                            </li>
                                            <li class="input-item">
                                                <label class="radio-field star" for="star5">
                                                    <input type="radio" name="rate" value="star5" class="radio-input"
                                                        id="star5">
                                                    <span class="radio-img"></span>
                                                </label>
                                            </li>
                                        </ul>
                                    </div>
                                    <!-- Question 3 -->
                                    <div class="field-wrap">
                                        <h3 class="field-label"><span class="marker"></span>How do you feel about the
                                            design of the shoes?</h3>
                                        <ul class="input-list">
                                            <li class="input-item">
                                                <label class="radio-field smiley smiley-happy" for="happy">
                                                    <input type="radio" name="feel" value="happy" class="radio-input"
                                                        id="happy">
                                                    <span class="radio-img"></span>
                                                    </lab>
                                            </li>
                                            <li class="input-item">
                                                <label class="radio-field smiley smiley-normal " for="normal">
                                                    <input type="radio" name="feel" value="thumb-down"
                                                        class="radio-input" id="normal">
                                                    <span class="radio-img"></span>
                                                </label>
                                            </li>
                                            <li class="input-item">
                                                <label class="radio-field smiley smiley-sad" for="sad">
                                                    <input type="radio" name="feel" value="smiley-sad"
                                                        class="radio-input" id="sad">
                                                    <span class="radio-img"></span>
                                                </label>
                                            </li>
                                        </ul>
                                    </div>
                                    <!-- Question 4 -->
                                    <div class="field-wrap typ-last">
                                        <div class="field-head">
                                            <h3 class="field-label"><span class="marker"></span>How do you feel about
                                                the quality of our shoes?</h3>
                                            <button class="remove" on="tap:AMP.setState({feedbackInput: ''})">
                                                <amp-img layout="responsive"
                                                    src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/feedback-html/icon-trash.png"
                                                    alt="remove" class="remove-logo" width="20" height="20"></amp-img>
                                            </button>
                                        </div>
                                        <ul class="input-list">
                                            <li class="input-item full-width">
                                                <textarea class="input" id="feedback-input" name="feedbackInput"
                                                    placeholder="Please explain here" [text]="feedbackInput"
                                                    on="input-debounced:AMP.setState({feedbackInput: event.target.value})"> </textarea>
                                            </li>
                                        </ul>
                                    </div>
                                    <div class="btn-wrap">
                                        <!-- Change CTA -->
                                        <button type="submit" class="submit-cta"
                                            [class]="!successVisible ? 'submit-cta' : 'submit-cta disable'"
                                            on="tap:AMP.setState({successVisible: true})">Submit</button>
                                        <!-- Change CTA -->
                                    </div>
                                </form>
                                <!-- Success Container - Initially Hidden -->
                                <div class="success-container hidden"
                                    [class]="!successVisible ? 'success-container hidden' : 'success-container show'">
                                    <h4 class="title">Thank you</h4>
                                    <p class="para">
                                        is simply dummy text of the printing and typesetting is simply dummy text of the
                                        printing and typesetting industry.g industry. is simply dummy text of the
                                        printing and typesetting is simply dummy.
                                    </p>
                                </div>
                            </div>
                        </td>
                    </tr>
                    <!-- Footer Section-->
                    <tr>
                        <td align="center">
                            <table role="presentation" cellspacing="0" cellpadding="0" border="0" align="center"
                                style="padding: 50px 0; border-top: 1px solid #ADADAD">
                                <tr>
                                    <td style="padding: 0 0 18px;">
                                        <table align="center" cellpadding="0" cellspacing="0" width="100%"
                                            style="text-align: center;">
                                            <tr>
                                                <!-- Social Links -->
                                                <td style="padding: 0 15px; display: inline-block;">
                                                    <a href="https://www.google.co.in/"
                                                        style="vertical-align: middle;display: inline-block; width: 34px; height: 34px;">
                                                        <!-- Change image src as per your requirements -->
                                                        <amp-img
                                                            src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/feedback-html/logo-insta.png"
                                                            alt="instagram" width="34" height="34">
                                                    </a>
                                                </td>
                                                <td style="padding: 0 15px; display: inline-block;">
                                                    <a href="https://www.google.co.in/"
                                                        style="vertical-align: middle;display: inline-block; width: 34px; height: 34px;">
                                                        <!-- Change image src as per your requirements -->
                                                        <amp-img
                                                            src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/feedback-html/logo-facebook.png"
                                                            alt="facebook" width="34" height="34">
                                                    </a>
                                                </td>
                                                <td style="padding: 0 15px; display: inline-block;">
                                                    <a href="https://www.google.co.in/"
                                                        style="vertical-align: middle;display: inline-block; width: 34px; height: 34px;">
                                                        <!-- Change image src as per your requirements -->
                                                        <amp-img
                                                            src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/feedback-html/logo-x.png"
                                                            alt="x" width="34" height="34">
                                                    </a>
                                                </td>
                                                <!-- Social Links -->
                                            </tr>
                                        </table>
                                    </td>
                                </tr>
                                <tr>
                                    <td>
                                        <p
                                            style="color: #939393; font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; margin: 0 auto; max-width: 80%;">
                                            We're only getting started—rely on us to guide you every step of the way.
                                            Welcome to the [community/family/team]!
                                        </p>
                                    </td>
                                </tr>
                                <tr>
                                    <td>
                                        <p
                                            style="color: #939393; font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; margin: 20px auto; max-width: 80%;">
                                            To stop receiving these emails, <a href="#"
                                                style="color:#1E1E1E;font-weight:bold;text-decoration:none;">unsubscribe
                                                here</a>
                                        </p>
                                    </td>
                                </tr>
                            </table>
                        </td>
                    </tr>
                    <!-- Footer Section-->
                </table>
            </td>
        </tr>
    </table>
</body>
</html>
```

</details>

## Interactive Grid

This AMP template features a clickable tile-based layout where each tile reveals a contextual popup within the email. Originally themed around zodiac signs, this template is fully customizable — tiles can represent categories like product types, service plans, travel destinations, or user personas.

When clicked, each tile displays an offer, message, or interactive form, enabling brands to deliver multiple personalized micro-experiences inside a single email.

<details>

<summary>Expand to know more about the template.</summary>

### Use Case Examples

- Zodiac-based Offer Engagement: Display tailored offers by the user’s zodiac sign.
- Product Category Showcases: Let users explore offers based on product types (for example, electronics, apparel, beauty).
- Festival/Seasonal Gifting: Show different recommendations for occasions (for example, Diwali gifts, Summer picks).
- User Personas or Interests: Target users with content that aligns with their interests (for example, Fitness, Fashion, Tech).

### Template Customization Options

- Replace tile icons/text with your categories or offerings.
- Configure the pop-up content per tile.
- Update CTAs within the popups (e.g., View Deal, Claim Offer, Remind Me).
- Modify header/footer with brand elements and policy links.
- Adjust background colors and fonts to suit campaign tone.

### Template Code

```html
<!doctype html>
<html ⚡4email data-css-strict>
<head>
	<meta charset="utf-8">
	<script async src="https://cdn.ampproject.org/v0.js"></script>
	<script async custom-element="amp-bind" src="https://cdn.ampproject.org/v0/amp-bind-0.1.js"></script>
	<script async custom-element="amp-form" src="https://cdn.ampproject.org/v0/amp-form-0.1.js"></script>
	<script async custom-element="amp-lightbox" src="https://cdn.ampproject.org/v0/amp-lightbox-0.1.js"></script>
	<style amp4email-boilerplate>
		body {
			visibility: hidden
		}
	</style>
	<style amp-custom>
		* {
			margin: 0;
			padding: 0;
		}
		body {
			font-family: "Helvetica", arial, sans-serif;
			font-weight: 400;
		}
		img {
			width: 100%;
			height: 100%;
			object-fit: cover;
		}
		.main {
			width: 100%;
			max-width: 600px;
			overflow: hidden;
			margin: 0 auto;
			background: #FFFFFF;
		}
		.sec-title {
			font-size: 50px;
			font-weight: 500;
			line-height: 50px;
			text-align: center;
			color: #FFFFFF;
			text-transform: uppercase;
			margin-bottom: 40px;
		}
		.sec-desc {
			max-width: 70%;
			margin: 0 auto 42px;
			font-size: 18px;
			font-weight: 400;
			line-height: 20px;
			text-align: center;
			text-transform: capitalize;
			color: #FFFFFF;
		}
		.z-list {
			list-style: none;
			display: flex;
			justify-content: space-between;
			flex-wrap: wrap;
			gap: 10px;
			margin-bottom: -100px;
		}
		.z-item {
			background: #FFFFFF;
			box-shadow: 0px 3.57px 3.57px 0px #00000040;
			width: 32%;
		}
		.z-card {
			background: #FECD2C;
			box-shadow: 0px 3.57px 3.57px 0px #00000040;
			margin: 8px;
			padding: 10px 8px;
			display: flex;
			justify-content: center;
			align-items: center;
			flex-direction: column;
			min-height: 222px;
		}
		.z-card .z-title {
			text-transform: capitalize;
			font-weight: 600;
			font-size: 26px;
			line-height: 26px;
			color: #FFFFFF;
			margin-bottom: 5px;
		}
		.z-card .data {
			text-transform: capitalize;
			font-weight: 400;
			font-size: 14px;
			line-height: 24px;
			color: #FFFFFF;
			text-align: center;
			margin-bottom: 8px;
		}
		.z-card .border {
			width: 135px;
			height: 0.9px;
			background: #FFFFFF;
			margin: 0 auto 13px;
		}
		.z-card .img-wrap {
			width: 73px;
			height: 73px;
			margin: 0 auto;
		}
		.z-card .animals {
			margin-top: 5px;
			text-transform: capitalize;
			color: #FFFFFF;
			font-weight: 400;
			font-size: 18px;
			line-height: 24px;
		}
		.sec-title {
			font-size: 35px;
			line-height: 40px;
			margin-bottom: 20px;
		}
		.sec-desc {
			max-width: 90%;
			margin: 0 auto 32px;
			font-size: 16px;
		}
		.container {
			padding: 72px 0 40px;
			background-color: #FE592C;
		}
		.lightbox {
			background: rgba(0, 0, 0, 0.8);
			width: 100%;
			height: 100%;
			position: absolute;
			display: flex;
			align-items: center;
			justify-content: center;
		}
		.zodiac-popup {
			padding: 10px 10px 20px;
			max-width: 80%;
			background: #FFFFFF;
			position: relative;
		}
		.zodiac-popup .img-wrap {
			overflow: hidden;
		}
		.d-title {
			font-size: 30px;
			font-weight: 400;
			line-height: 36px;
			text-align: center;
			color: #FE592C;
			margin: 20px 0;
			text-transform: uppercase;
		}
		.d-title .discount {
			font-size: 45px;
			line-height: 50px;
		}
		.cm-bold {
			font-weight: 400;
		}
		.wrap {
			position: relative;
		}
		.input-wrap {
			max-width: 80%;
			margin: 0 auto;
		}
		.input {
			border: 1px dashed #FE592C;
			background-color: #F5F5F5;
			padding: 8px 20px;
			border-radius: 31px;
			font-size: 28px;
			font-weight: 500;
			line-height: 30px;
			text-align: left;
			width: 87%;
			margin-bottom: 28px;
			text-transform: uppercase;
		}
		.icon-cta {
			border: 0;
			position: absolute;
			background: transparent;
			top: 17px;
			right: 15px;
		}
		.redeem-cta {
			background: #FE592C;
			border: 1px solid #FE592C;
			font-size: 30px;
			font-weight: 400;
			line-height: 43px;
			text-align: center;
			color: #FFFFFF;
			vertical-align: middle;
			width: 100%;
			padding: 8px 0;
			border-radius: 21px;
			display: inline-block;
			text-decoration: none;
		}
		@media only screen and (max-width: 480px) {
			body .main {
				max-width: 100%;
			}
			.logo-wrap {
				padding: 17px 0;
			}
			.logo-wrap .img-wrap {
				max-width: 130px;
				max-height: 60px;
				margin: 0 auto;
			}
			.footer {
				padding-top: 100px;
			}
			.z-item {
				background: #FFFFFF;
				box-shadow: 0px 3.57px 3.57px 0px #00000040;
				width: 48%;
			}
			.container {
				padding: 50px 0 40px;
			}
			.z-card .z-title {
				font-size: 20px;
				line-height: 22px;
			}
			.z-card .border {
				width: 94px;
			}
			.z-card .img-wrap {
				width: 55px;
				height: 56px;
			}
			.z-card .animals {
				font-size: 16px;
				line-height: 20px;
			}
			.z-card {
				min-height: 180px;
			}
			.border-line {
				width: 20%;
			}
			.zodiac-popup {
				max-width: 80%;
			}
			.d-title {
				font-size: 25px;
				line-height: 30px;
				margin-bottom: 20px;
				margin-top: 10px;
			}
			.d-title .discount {
				font-size: 30px;
				line-height: 40px;
			}
			.input {
				padding: 12px;
				font-size: 20px;
				line-height: 26px;
				margin-bottom: 20px;
			}
			.redeem-cta {
				font-size: 20px;
				line-height: 30px;
				padding: 5px;
				border-radius: 10px;
			}
		}
	</style>
</head>
<body>
	<!-- Change Theme-->
	<table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%"
		style="max-width: 600px; margin: 0 auto; background-color: #FFFFFF; position: relative;" class="main">
		<!-- Change Theme-->
		<tbody>
			<!-- header start-->
			<tr>
				<td style="text-align: center; vertical-align: middle; padding: 20px">
					<!-- Change Logo Image src as per your requirements -->
					<amp-img width="127" height="58"
						src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/logo.png"
						class="logo" alt="Logo" style="display: inline-block; object-fit: cover;" />
					<!-- Change Logo Image src as per your requirements -->
				</td>
			</tr>
			<!-- header end-->
			<tr>
				<td class="container">
					<table role="presentation" cellspacing="0" cellpadding="0" border="0" align="center"
						style=" width:95%; margin: 0 auto;">
						<tbody>
							<tr>
								<td>
									<h2 class="sec-title">Headline</h2>
									<p class="sec-desc">is simply dummy text of the printing and typesetting industry.
										Lorem Ipsum has been the industry's standard dummy.</p>
								</td>
							</tr>
							<tr>
								<td>
									<form id="formZodio" class="result-wrap" method="post"
										action-xhr="https://www.google.com/">
										<input type="hidden" name="selectedZodiac" [value]="selectedZodiac" />
										<ul class="z-list">
											<li class="z-item">
												<div class="z-card"
													on="tap:AMP.setState({ selectedZodiac: 'Aries' }), zodiac-1.open"
													role="button" tabindex="0">
													<h2 class="z-title">Aries</h2>
													<p class="data">March 21–April 19</p>
													<div class="border"></div>
													<div class="img-wrap">
														<amp-img layout="responsive" width="73" height="73"
															src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/zodiac-1.png"
															alt="zodiac" class="z-img" />
													</div>
													<p class="animals">ram</p>
												</div>
											</li>
											<li class="z-item">
												<div class="z-card"
													on="tap:AMP.setState({ selectedZodiac: 'Taurus' }), zodiac-2.open"
													role="button" tabindex="0">
													<h2 class="z-title">Taurus</h2>
													<p class="data">April 20–May 20</p>
													<div class="border"></div>
													<div class="img-wrap">
														<amp-img layout="responsive" width="73" height="73"
															src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/zodiac-2.png"
															alt="zodiac" class="z-img" />
													</div>
													<p class="animals">Bull</p>
												</div>
											</li>
											<li class="z-item">
												<div class="z-card"
													on="tap:AMP.setState({ selectedZodiac: 'Gemini' }), zodiac-3.open"
													role="button" tabindex="0">
													<h2 class="z-title">Gemini</h2>
													<p class="data">May 21–June 21</p>
													<div class="border"></div>
													<div class="img-wrap">
														<amp-img layout="responsive" width="73" height="73"
															src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/zodiac-3.png"
															alt="zodiac" class="z-img" />
													</div>
													<p class="animals">Twins</p>
												</div>
											</li>
											<li class="z-item">
												<div class="z-card"
													on="tap:AMP.setState({ selectedZodiac: 'Cancer' }), zodiac-4.open"
													role="button" tabindex="0">
													<h2 class="z-title">Cancer</h2>
													<p class="data">June 22–July 22</p>
													<div class="border"></div>
													<div class="img-wrap">
														<amp-img layout="responsive" width="73" height="73"
															src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/zodiac-4.png"
															alt="zodiac" class="z-img" />
													</div>
													<p class="animals">Crab</p>
												</div>
											</li>
											<li class="z-item">
												<div class="z-card"
													on="tap:AMP.setState({ selectedZodiac: 'Leo' }), zodiac-5.open"
													role="button" tabindex="0">
													<h2 class="z-title">Leo</h2>
													<p class="data">July 23–August 22</p>
													<div class="border"></div>
													<div class="img-wrap">
														<amp-img layout="responsive" width="73" height="73"
															src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/zodiac-5.png"
															alt="zodiac" class="z-img" />
													</div>
													<p class="animals">Lion</p>
												</div>
											</li>
											<li class="z-item">
												<div class="z-card"
													on="tap:AMP.setState({ selectedZodiac: 'Virgo' }), zodiac-6.open"
													role="button" tabindex="0">
													<h2 class="z-title">Virgo</h2>
													<p class="data">August 23–September 22</p>
													<div class="border"></div>
													<div class="img-wrap">
														<amp-img layout="responsive" width="73" height="73"
															src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/zodiac-6.png"
															alt="zodiac" class="z-img" />
													</div>
													<p class="animals">Twins</p>
												</div>
											</li>
											<li class="z-item">
												<div class="z-card"
													on="tap:AMP.setState({ selectedZodiac: 'Libra' }), zodiac-7.open"
													role="button" tabindex="0">
													<h2 class="z-title">Libra</h2>
													<p class="data">September 23–October 23</p>
													<div class="border"></div>
													<div class="img-wrap">
														<amp-img layout="responsive" width="73" height="73"
															src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/zodiac-7.png"
															alt="zodiac" class="z-img" />
													</div>
													<p class="animals">Balance</p>
												</div>
											</li>
											<li class="z-item">
												<div class="z-card"
													on="tap:AMP.setState({ selectedZodiac: 'Scorpio' }), zodiac-8.open"
													role="button" tabindex="0">
													<h2 class="z-title">Scorpio</h2>
													<p class="data">October 24–November 21</p>
													<div class="border"></div>
													<div class="img-wrap">
														<amp-img layout="responsive" width="73" height="73"
															src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/zodiac-8.png"
															alt="zodiac" class="z-img" />
													</div>
													<p class="animals">Scorpio</p>
												</div>
											</li>
											<li class="z-item">
												<div class="z-card"
													on="tap:AMP.setState({ selectedZodiac: 'Sagittarius' }), zodiac-9.open"
													role="button" tabindex="0">
													<h2 class="z-title">Sagittarius</h2>
													<p class="data">November 22–December 21</p>
													<div class="border"></div>
													<div class="img-wrap">
														<amp-img layout="responsive" width="73" height="73"
															src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/zodiac-9.png"
															alt="zodiac" class="z-img" />
													</div>
													<p class="animals">Archer</p>
												</div>
											</li>
											<li class="z-item">
												<div class="z-card"
													on="tap:AMP.setState({ selectedZodiac: 'Capricorn' }), zodiac-10.open"
													role="button" tabindex="0">
													<h2 class="z-title">Capricorn</h2>
													<p class="data">December 22–January 19</p>
													<div class="border"></div>
													<div class="img-wrap">
														<amp-img layout="responsive" width="73" height="73"
															src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/zodiac-10.png"
															alt="zodiac" class="z-img" />
													</div>
													<p class="animals">Goat</p>
												</div>
											</li>
											<li class="z-item">
												<div class="z-card"
													on="tap:AMP.setState({ selectedZodiac: 'Aquarius' }), zodiac-11.open"
													role="button" tabindex="0">
													<h2 class="z-title">Aquarius </h2>
													<p class="data">January 20–February 18</p>
													<div class="border"></div>
													<div class="img-wrap">
														<amp-img layout="responsive" width="73" height="73"
															src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/zodiac-11.png"
															alt="zodiac" class="z-img" />
													</div>
													<p class="animals">Water Bearer</p>
												</div>
											</li>
											<li class="z-item">
												<div class="z-card"
													on="tap:AMP.setState({ selectedZodiac: 'Pisces' }), zodiac-12.open"
													role="button" tabindex="0">
													<h2 class="z-title"> Pisces </h2>
													<p class="data">February 19–March 20</p>
													<div class="border"></div>
													<div class="img-wrap">
														<amp-img layout="responsive" width="73" height="73"
															src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/zodiac-12.png"
															alt="zodiac" class="z-img" />
													</div>
													<p class="animals">Fish</p>
												</div>
											</li>
										</ul>
									</form>
								</td>
							</tr>
						</tbody>
					</table>
				</td>
			</tr>
			<amp-lightbox id="zodiac-1" layout="nodisplay">
				<div class="lightbox">
					<div class="zodiac-popup">
						<button on="tap:zodiac-1.close" role="button" tabindex="0"
							style=" width: 40px;height: 40px;outline: 0;border: 0;position: absolute;top: -10px;right: -10px; background: transparent; z-index: 2;">
							<amp-img layout="fixed" width="30" height="30"
								src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/close-icon.png"
								alt="close-img" />
						</button>
						<div class="img-wrap">
							<amp-img layout="responsive" width="500" height="300"
								src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/pop-img.png"
								alt="pop-img" />
						</div>
						<div class="zodiac-popup-content">
							<h4 class="d-title">
								get <br /><span class="discount">10% <span class="bold">Off</span></span><br /> On your
								purchase
							</h4>
							<div class="input-wrap">
								<div class="wrap">
									<input class="input" disabled value="#@556t66y6">
									<button class="icon-cta">
										<amp-img layout="fixed" width="20" height="20"
											src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/copy-icon.png"
											alt="copy-icon" />
									</button>
								</div>
								<a href="https://google.com" class="redeem-cta">Redeem now</a>
							</div>
						</div>
					</div>
				</div>
			</amp-lightbox>
			<amp-lightbox id="zodiac-2" layout="nodisplay">
				<div class="lightbox">
					<div class="zodiac-popup">
						<button on="tap:zodiac-2.close" role="button" tabindex="0"
							style=" width: 40px;height: 40px;outline: 0;border: 0;position: absolute;top: -20px;right: -10px; background: transparent; z-index: 2;">
							<amp-img layout="fixed" width="30" height="30"
								src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/close-icon.png"
								alt="close-img" />
						</button>
						<div class="img-wrap">
							<amp-img layout="responsive" width="500" height="300"
								src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/pop-img.png"
								alt="pop-img" />
						</div>
						<div class="zodiac-popup-content">
							<h4 class="d-title">
								get <br /><span class="discount">20% <span class="bold">Off</span></span><br /> On your
								purchase
							</h4>
							<div class="input-wrap">
								<div class="wrap">
									<input class="input" disabled value="#@556t66y6">
									<button class="icon-cta">
										<amp-img layout="fixed" width="20" height="20"
											src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/copy-icon.png"
											alt="copy-icon" />
									</button>
								</div>
								<a href="https://google.com" class="redeem-cta">Redeem now</a>
							</div>
						</div>
					</div>
				</div>
			</amp-lightbox>
			<amp-lightbox id="zodiac-3" layout="nodisplay">
				<div class="lightbox">
					<div class="zodiac-popup">
						<button on="tap:zodiac-3.close" role="button" tabindex="0"
							style=" width: 40px;height: 40px;outline: 0;border: 0;position: absolute;top: -20px;right: -10px; background: transparent; z-index: 2;">
							<amp-img layout="fixed" width="30" height="30"
								src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/close-icon.png"
								alt="close-img" />
						</button>
						<div class="img-wrap">
							<amp-img layout="responsive" width="500" height="300"
								src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/pop-img.png"
								alt="pop-img" />
						</div>
						<div class="zodiac-popup-content">
							<h4 class="d-title">
								get <br /><span class="discount">30% <span class="bold">Off</span></span><br /> On your
								purchase
							</h4>
							<div class="input-wrap">
								<div class="wrap">
									<input class="input" disabled value="#@556t66y6">
									<!-- Change CTA -->
									<button class="icon-cta">
										<amp-img layout="fixed" width="20" height="20"
											src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/copy-icon.png"
											alt="copy-icon" />
									</button>
									<!-- Change CTA -->
								</div>
								<a href="https://google.com" class="redeem-cta">Redeem now</a>
							</div>
						</div>
					</div>
				</div>
			</amp-lightbox>
			<amp-lightbox id="zodiac-4" layout="nodisplay">
				<div class="lightbox">
					<div class="zodiac-popup">
						<button on="tap:zodiac-4.close" role="button" tabindex="0"
							style=" width: 40px;height: 40px;outline: 0;border: 0;position: absolute;top: -20px;right: -10px; background: transparent; z-index: 2;">
							<amp-img layout="fixed" width="30" height="30"
								src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/close-icon.png"
								alt="close-img" />
						</button>
						<div class="img-wrap">
							<amp-img layout="responsive" width="500" height="300"
								src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/pop-img.png"
								alt="pop-img" />
						</div>
						<div class="zodiac-popup-content">
							<h4 class="d-title">
								get <br /><span class="discount">40% <span class="bold">Off</span></span><br /> On your
								purchase
							</h4>
							<div class="input-wrap">
								<div class="wrap">
									<input class="input" disabled value="#@556t66y6">
									<button class="icon-cta">
										<amp-img layout="fixed" width="20" height="20"
											src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/copy-icon.png"
											alt="copy-icon" />
									</button>
								</div>
								<a href="https://google.com" class="redeem-cta">Redeem now</a>
							</div>
						</div>
					</div>
				</div>
			</amp-lightbox>
			<amp-lightbox id="zodiac-5" layout="nodisplay">
				<div class="lightbox">
					<div class="zodiac-popup">
						<button on="tap:zodiac-5.close" role="button" tabindex="0"
							style=" width: 40px;height: 40px;outline: 0;border: 0;position: absolute;top: -20px;right: -10px; background: transparent; z-index: 2;">
							<amp-img layout="fixed" width="30" height="30"
								src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/close-icon.png"
								alt="close-img" />
						</button>
						<div class="img-wrap">
							<amp-img layout="responsive" width="500" height="300"
								src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/pop-img.png"
								alt="pop-img" />
						</div>
						<div class="zodiac-popup-content">
							<h4 class="d-title">
								get <br /><span class="discount">50% <span class="bold">Off</span></span><br /> On your
								purchase
							</h4>
							<div class="input-wrap">
								<div class="wrap">
									<input class="input" disabled value="#@556t66y6">
									<button class="icon-cta">
										<amp-img layout="fixed" width="20" height="20"
											src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/copy-icon.png"
											alt="copy-icon" />
									</button>
								</div>
								<a href="https://google.com" class="redeem-cta">Redeem now</a>
							</div>
						</div>
					</div>
				</div>
			</amp-lightbox>
			<amp-lightbox id="zodiac-6" layout="nodisplay">
				<div class="lightbox">
					<div class="zodiac-popup">
						<button on="tap:zodiac-6.close" role="button" tabindex="0"
							style=" width: 40px;height: 40px;outline: 0;border: 0;position: absolute;top: -20px;right: -10px; background: transparent; z-index: 2;">
							<amp-img layout="fixed" width="30" height="30"
								src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/close-icon.png"
								alt="close-img" />
						</button>
						<div class="img-wrap">
							<amp-img layout="responsive" width="500" height="300"
								src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/pop-img.png"
								alt="pop-img" />
						</div>
						<div class="zodiac-popup-content">
							<h4 class="d-title">
								get <br /><span class="discount">60% <span class="bold">Off</span></span><br /> On your
								purchase
							</h4>
							<div class="input-wrap">
								<div class="wrap">
									<input class="input" disabled value="#@556t66y6">
									<button class="icon-cta">
										<amp-img layout="fixed" width="20" height="20"
											src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/copy-icon.png"
											alt="copy-icon" />
									</button>
								</div>
								<a href="https://google.com" class="redeem-cta">Redeem now</a>
							</div>
						</div>
					</div>
				</div>
			</amp-lightbox>
			<amp-lightbox id="zodiac-7" layout="nodisplay">
				<div class="lightbox">
					<div class="zodiac-popup">
						<button on="tap:zodiac-7.close" role="button" tabindex="0"
							style=" width: 40px;height: 40px;outline: 0;border: 0;position: absolute;top: -20px;right: -10px; background: transparent; z-index: 2;">
							<amp-img layout="fixed" width="30" height="30"
								src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/close-icon.png"
								alt="close-img" />
						</button>
						<div class="img-wrap">
							<amp-img layout="responsive" width="500" height="300"
								src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/pop-img.png"
								alt="pop-img" />
						</div>
						<div class="zodiac-popup-content">
							<h4 class="d-title">
								get <br /><span class="discount">70% <span class="bold">Off</span></span><br /> On your
								purchase
							</h4>
							<div class="input-wrap">
								<div class="wrap">
									<input class="input" disabled value="#@556t66y6">
									<button class="icon-cta">
										<amp-img layout="fixed" width="20" height="20"
											src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/copy-icon.png"
											alt="copy-icon" />
									</button>
								</div>
								<a href="https://google.com" class="redeem-cta">Redeem now</a>
							</div>
						</div>
					</div>
				</div>
			</amp-lightbox>
			<amp-lightbox id="zodiac-8" layout="nodisplay">
				<div class="lightbox">
					<div class="zodiac-popup">
						<button on="tap:zodiac-8.close" role="button" tabindex="0"
							style=" width: 40px;height: 40px;outline: 0;border: 0;position: absolute;top: -20px;right: -10px; background: transparent; z-index: 2;">
							<amp-img layout="fixed" width="30" height="30"
								src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/close-icon.png"
								alt="close-img" />
						</button>
						<div class="img-wrap">
							<amp-img layout="responsive" width="500" height="300"
								src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/pop-img.png"
								alt="pop-img" />
						</div>
						<div class="zodiac-popup-content">
							<h4 class="d-title">
								get <br /><span class="discount">80% <span class="bold">Off</span></span><br /> On your
								purchase
							</h4>
							<div class="input-wrap">
								<div class="wrap">
									<input class="input" disabled value="#@556t66y6">
									<button class="icon-cta">
										<amp-img layout="fixed" width="20" height="20"
											src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/copy-icon.png"
											alt="copy-icon" />
									</button>
								</div>
								<a href="https://google.com" class="redeem-cta">Redeem now</a>
							</div>
						</div>
					</div>
				</div>
			</amp-lightbox>
			<amp-lightbox id="zodiac-9" layout="nodisplay">
				<div class="lightbox">
					<div class="zodiac-popup">
						<button on="tap:zodiac-9.close" role="button" tabindex="0"
							style=" width: 40px;height: 40px;outline: 0;border: 0;position: absolute;top: -20px;right: -10px; background: transparent; z-index: 2;">
							<amp-img layout="fixed" width="30" height="30"
								src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/close-icon.png"
								alt="close-img" />
						</button>
						<div class="img-wrap">
							<amp-img layout="responsive" width="500" height="300"
								src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/pop-img.png"
								alt="pop-img" />
						</div>
						<div class="zodiac-popup-content">
							<h4 class="d-title">
								get <br /><span class="discount">90% <span class="bold">Off</span></span><br /> On your
								purchase
							</h4>
							<div class="input-wrap">
								<div class="wrap">
									<input class="input" disabled value="#@556t66y6">
									<button class="icon-cta">
										<amp-img layout="fixed" width="20" height="20"
											src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/copy-icon.png"
											alt="copy-icon" />
									</button>
								</div>
								<a href="https://google.com" class="redeem-cta">Redeem now</a>
							</div>
						</div>
					</div>
				</div>
			</amp-lightbox>
			<amp-lightbox id="zodiac-10" layout="nodisplay">
				<div class="lightbox">
					<div class="zodiac-popup">
						<button on="tap:zodiac-10.close" role="button" tabindex="0"
							style=" width: 40px;height: 40px;outline: 0;border: 0;position: absolute;top: -20px;right: -10px; background: transparent; z-index: 2;">
							<amp-img layout="fixed" width="30" height="30"
								src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/close-icon.png"
								alt="close-img" />
						</button>
						<div class="img-wrap">
							<amp-img layout="responsive" width="500" height="300"
								src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/pop-img.png"
								alt="pop-img" />
						</div>
						<div class="zodiac-popup-content">
							<h4 class="d-title">
								get <br /><span class="discount">10% <span class="bold">Off</span></span><br /> On your
								purchase
							</h4>
							<div class="input-wrap">
								<div class="wrap">
									<input class="input" disabled value="#@556t66y6">
									<button class="icon-cta">
										<amp-img layout="fixed" width="20" height="20"
											src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/copy-icon.png"
											alt="copy-icon" />
									</button>
								</div>
								<a href="https://google.com" class="redeem-cta">Redeem now</a>
							</div>
						</div>
					</div>
				</div>
			</amp-lightbox>
			<amp-lightbox id="zodiac-11" layout="nodisplay">
				<div class="lightbox">
					<div class="zodiac-popup">
						<button on="tap:zodiac-11.close" role="button" tabindex="0"
							style=" width: 40px;height: 40px;outline: 0;border: 0;position: absolute;top: -20px;right: -10px; background: transparent; z-index: 2;">
							<amp-img layout="fixed" width="30" height="30"
								src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/close-icon.png"
								alt="close-img" />
						</button>
						<div class="img-wrap">
							<amp-img layout="responsive" width="500" height="300"
								src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/pop-img.png"
								alt="pop-img" />
						</div>
						<div class="zodiac-popup-content">
							<h4 class="d-title">
								get <br /><span class="discount">11% <span class="bold">Off</span></span><br /> On your
								purchase
							</h4>
							<div class="input-wrap">
								<div class="wrap">
									<input class="input" disabled value="#@556t66y6">
									<button class="icon-cta">
										<amp-img layout="fixed" width="20" height="20"
											src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/copy-icon.png"
											alt="copy-icon" />
									</button>
								</div>
								<a href="https://google.com" class="redeem-cta">Redeem now</a>
							</div>
						</div>
					</div>
				</div>
			</amp-lightbox>
			<amp-lightbox id="zodiac-12" layout="nodisplay">
				<div class="lightbox">
					<div class="zodiac-popup">
						<button on="tap:zodiac-12.close" role="button" tabindex="0"
							style=" width: 40px;height: 40px;outline: 0;border: 0;position: absolute;top: -20px;right: -10px; background: transparent; z-index: 2;">
							<amp-img layout="fixed" width="30" height="30"
								src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/close-icon.png"
								alt="close-img" />
						</button>
						<div class="img-wrap">
							<amp-img layout="responsive" width="500" height="300"
								src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/pop-img.png"
								alt="pop-img" />
						</div>
						<div class="zodiac-popup-content">
							<h4 class="d-title">
								get <br /><span class="discount">12% <span class="bold">Off</span></span><br /> On your
								purchase
							</h4>
							<div class="input-wrap">
								<div class="wrap">
									<input class="input" disabled value="#@556t66y6">
									<button class="icon-cta">
										<amp-img layout="fixed" width="20" height="20"
											src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/copy-icon.png"
											alt="copy-icon" />
									</button>
								</div>
								<a href="https://google.com" class="redeem-cta">Redeem now</a>
							</div>
						</div>
					</div>
				</div>
			</amp-lightbox>
			<!-- footer start-->
			<tr>
				<td colspan="2" align="center" class="footer" style="padding: 60px 0 10px;">
					<table role="presentation" cellspacing="0" cellpadding="0" border="0" align="center"
						style="width:100%;">
						<tbody>
							<tr>
								<td style="padding: 30px 0;">
									<p
										style="font-size: 14px; font-weight: 400; line-height: 25px; text-align: center; color: #6F6F6F; text-transform: uppercase; max-width: 90%; margin: 0 auto;">
										is simply dummy text of the printing and typesetting industry. is simply dummy
										text of the printing and typesetting industry.</p>
								</td>
							</tr>
							<tr>
								<td style="padding-bottom: 30px 0;">
									<table align="center" cellpadding="0" cellspacing="0" width="100%"
										style="text-align: center;">
										<tbody>
											<!-- Social Links -->
											<tr>
												<td style="width:32%;" class="border-line">
													<div style="display: block; border:0.5px solid #FE592C;"></div>
												</td>
												<td style="padding: 10px 10px; display: inline-block;">
													<a href="https://google.com"
														style="vertical-align: middle;display: inline-block; width: 25px; height: 25px; ">
														<!-- Change image src as per your requirements -->
														<amp-img layout="fixed" width="20" height="20"
															src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/logo-insta.png"
															alt="instagram" />
													</a>
												</td>
												<td style="padding: 10px 10px; display: inline-block; ">
													<a href="https://google.com"
														style="vertical-align: middle;display: inline-block; width: 25px; height: 25px;">
														<amp-img layout="fixed" width="20" height="20"
															src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/logo-facebook.png"
															alt="facebook" />
													</a>
												</td>
												<td style="padding: 10px 10px; display: inline-block;">
													<a href="https://google.com"
														style="vertical-align: middle;display: inline-block; width: 25px; height: 25px;">
														<amp-img layout="fixed" width="20" height="20"
															src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/logo-x.png"
															alt="x" />
													</a>
												</td>
												<td style="width:32%;" class="border-line">
													<div style="display: block; border:0.5px solid #FE592C;"></div>
												</td>
											</tr>
										</tbody>
									</table>
								</td>
							</tr>
						</tbody>
					</table>
				</td>
			</tr>
			<tr>
				<td style="padding: 20px 0;">
					<p
						style="font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; color: #6F6F6F;">
						To stop receiving these emails, <a href="https://google.com"
							style="color:#FE592C;font-weight:bold;text-decoration:none;">unsubscribe here</a>
					</p>
				</td>
			</tr>
			<!-- footer end-->
		</tbody>
	</table>
</body>
</html>
```

</details>

## Click To Reveal

This AMP template allows users to engage with an email by clicking on an image to reveal a surprise offer or discount. This interactive format helps create a fun, suspense-driven experience that encourages action and drives higher conversion rates.

<details>

<summary>Expand to know more about the template.</summary>

### Use Case Examples

- Unlock hidden discounts in flash sales or festival campaigns.
- Gamify email experiences with “scratch-to-reveal” like formats.
- Increase engagement during limited-time promotions.
- Run surprise loyalty rewards or exclusive unlockable content.

### Template Customization Options

- Replace the Logo
- Update Banner/Product Images
- Update Call-To-Actions (CTAs)
- Update Links in the Header/Footer
- Modify Image Swapping Logic

### Template Code

```html
<!DOCTYPE html>
<html ⚡4email data-css-strict>
<head>
  <meta charset="utf-8">
  <script async src="https://cdn.ampproject.org/v0.js"></script>
  <script async custom-element="amp-bind" src="https://cdn.ampproject.org/v0/amp-bind-0.1.js"></script>
  <script async custom-element="amp-form" src="https://cdn.ampproject.org/v0/amp-form-0.1.js"></script>
  <style amp4email-boilerplate>
    body {
      visibility: hidden
    }
  </style>
  <style amp-custom>
    * {
      margin: 0;
      padding: 0;
    }
    body {
      font-family: "Helvetica", arial, sans-serif;
      font-weight: 400;
      background-color: #f5f5f5;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
    }
    img {
      width: 100%;
      height: 100%;
      object-fit: contain;
    }
    .main {
      width: 100%;
      max-width: 600px;
      overflow: hidden;
      margin: 0 auto;
      background: #527B66;
      border-bottom: 8px solid #FFFFFF;
    }
    @media only screen and (max-width: 400px) {
      .main {
        max-width: 100%;
      }
    }
    .logo-wrap {
      padding: 12px 24px;
      background-color: #FFFFFF;
      border-radius: 0 0 41px 41px;
      text-align: center;
      z-index: 2;
      position: relative;
    }
    .logo-wrap .img-wrap {
      max-width: 145.78px;
      max-height: 74.89px;
      margin: 0 auto;
    }
    .container {
      width: 90%;
      margin: 53px auto 18px;
      border-top: 2px solid #93784A;
      border-bottom: 2px solid #93784A;
    }
    .wrapper {
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      padding: 48px 0 40px;
    }
    .title {
      font-family: "Helvetica", arial, sans-serif;
      font-size: 32px;
      font-weight: 500;
      line-height: 52px;
      color: #FFFFFF;
      text-transform: uppercase;
      margin-bottom: 5px;
      text-align: center;
    }
    .cm-light {
      font-weight: 300;
    }
    .desc {
      font-family: "Helvetica", arial, sans-serif;
      font-size: 14px;
      font-weight: 400;
      line-height: 20px;
      color: #CECBD1;
      text-align: center;
      text-transform: capitalize;
    }
    .card {
      width: 65%;
      margin: 40px auto;
      height: 381px;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      background: #FFFFFF;
      border-radius: 50%;
      padding: 0 25px;
    }
    .c-title {
      font-family: "Helvetica", arial, sans-serif;
      font-size: 30px;
      font-weight: 400;
      line-height: 32px;
      text-align: center;
      margin-bottom: 20px;
      color: #000000;
      text-transform: capitalize;
    }
    .c-desc {
      font-family: "Helvetica", arial, sans-serif;
      font-size: 10px;
      font-weight: 400;
      line-height: 16px;
      text-align: center;
      text-transform: capitalize;
      color: #525252;
      margin-bottom: 20px;
    }
    .c-cta {
      font-family: "Helvetica", arial, sans-serif;
      font-size: 16px;
      font-weight: 500;
      line-height: 20px;
      text-align: center;
      color: #FFFFFF;
      border-radius: 100px;
      background: #527B66;
      outline: none;
      border: 0;
      padding: 11px;
      max-width: 176px;
      display: inline-block;
      width: 100%;
      text-transform: capitalize;
      cursor: pointer;
    }
    .card-img-wrap {
      padding: 18px;
      width: 65%;
      max-height: 350px;
      background-color: #FFFFFF;
      margin: 40px auto;
    }
    .card-img-wrap .image {
      width: 100%;
      height: 100%;
    }
    .cta {
      font-family: "Helvetica", arial, sans-serif;
      font-size: 16px;
      font-weight: 500;
      line-height: 20px;
      text-align: center;
      color: #527B66;
      border-radius: 100px;
      background: #FFFFFF;
      outline: none;
      border: 0;
      padding: 11px;
      max-width: 350px;
      display: inline-block;
      width: 100%;
      text-transform: capitalize;
      cursor: pointer;
    }
    .wave-wrap {
      display: flex;
      align-items: center;
      margin: 40px 0;
    }
    @media only screen and (max-width: 480px) {
      .title {
        font-size: 25px;
        line-height: 35px;
      }
      .card {
        width: 75%;
        height: 300px;
      }
      .c-title {
        font-size: 20px;
        line-height: 25px;
        margin-bottom: 10px;
      }
      .c-cta {
        font-size: 14px;
        line-height: 18px;
        padding: 10px;
        max-width: 150px;
      }
      .wave-wrap {
        margin: 140px 0;
      }
      .wave-wrap .wave {
        width: 10px;
        height: 60px;
      }
      .card-img-wrap {
        padding: 10px;
        width: 85%;
      }
    }
  </style>
</head>
<body>
  <amp-state id="step">
    <script type="application/json">
{
"step": 1
}
</script>
  </amp-state>
  <div class="main">
    <header>
      <div class="logo-wrap">
        <div class="img-wrap">
          <amp-img layout="responsive"
            src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/SIP-Calculator/CleverTap%202.png" alt="Logo"
            width="159" height="73"></amp-img>
        </div>
      </div>
    </header>
    <div class="container">
      <!-- Step 1 -->
      <form custom-validation-reporting="show-all-on-submit"
        on="submit:AMP.setState({form6850m49:{formHistory: form6850m49.formHistory.splice(form6850m49.formHistory.length,0,form6850m49.currentStep)}})"
        action-xhr="https://t.mmtrkr.com/submissions/8598e13a-92af-5ed4-a239-989e988e1a88/93a0f936-f5fd-4d94-8bf1-43d8e6571405?sender=hello@amp.mailmodo.net&formId=123"
        method="post">
        <div class="wrapper step-1" [hidden]="step != 1">
          <h2 class="title">INTRODUCTION</h2>
          <p class="desc">is simply dummy text of the printing and typesetting industry</p>
          <div class="card">
            <h3 class="c-title">Click to get discount</h3>
            <p class="c-desc">is simply dummy text of the printing and typesetting industry.</p>
            <button type="submit" class="c-cta" on="tap:AMP.setState({ step: 2 })">
              click here
            </button>
          </div>
        </div>
        <div [hidden]="(('success') != 'success' || (form6850m49.currentStep == 'step3' && 'success' != 'success'))">
          <div submitting>
            <!-- Add Loading Image Here -->
            <div class="wrapper step-2">
              <div class="wave-wrap">
                <amp-img width="245" height="300"
                  src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/image-on-click/ezgif-3-b33d1ab799.gif"
                  alt="wave animation">
                </amp-img>
              </div>
            </div>
            <!-- Add Loading Image Here -->
          </div>
          <div submit-success>
            <div class="wrapper step-3">
              <h2 class="title"><span class="cm-light">Congratulations you get</span> 30% off</h2>
              <div class="card-img-wrap">
                <amp-img layout="responsive"
                  src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/image-on-click/pexels-karolina-grabowska-4202325%203.png"
                  alt="Banner" width="320" height="320" class="image"></amp-img>
              </div>
              <button type="button" class="cta">
                Shop now
              </button>
            </div>
          </div>
          <div submit-error>
            <div class="wrapper step-3">
              <h2 class="title"><span class="cm-light">Congratulations you get</span> 30% off</h2>
              <div class="card-img-wrap">
                <amp-img layout="responsive"
                  src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/image-on-click/pexels-karolina-grabowska-4202325%203.png"
                  alt="Banner" width="320" height="320" class="image"></amp-img>
              </div>
              <button type="button" class="cta">
                Shop now
              </button>
            </div>
          </div>
        </div>
      </form>
    </div>
  </div>
</body>
</html>
```

</details>