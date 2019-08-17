This is a free and open-source tool that sets up a product analytics data pipeline in your AWS account and helps you manage it. With floppr, you can set up a data pipeline within minutes, without having DevOps or data engineers. 

It offers an API to report event from your product, and a command line tool to manage the data pipeline and. Once the data starts streamed from your product, you can use the AWS resources for analytics: AWS Athena, AWS QuickSight and AWS EMR (optional).

## How does it works

[![Join the chat at https://gitter.im/flopprhq/community](https://badges.gitter.im/flopprhq/community.svg)](https://gitter.im/flopprhq/community?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

1. Make sure you have a AWS account. If not, [create](https://aws.amazon.com/premiumsupport/knowledge-center/create-and-activate-aws-account/) one.
2. Install the `floppr` command line tool.
3. Run the `init` floppr command:

```bash
floppr init
AWS Access Key ID: ****
AWS Secret Access Key: ****
AWS Region: ****
```

This command sets up a data pipeline within your AWS account. The pipeline includes an HTTP ingestion endpoint, a nightly batch ETL job, Athena database and table, AWS EMR (optional), etc

4. Download the reporting API
5. Call the API from your product

tba (elaborate on the organisation domain)

That's it! Your product events get to S3 and are available via AWS Athena, AWS QuickSight, and AWS EMR (optional).

## Why it works

1. It sets up and help you manage a data pipeline with your AWS account. You don't need DevOps or Data Engineers.
2. It is free. You're charged with your AWS account only for wht you use and according to the pricing of the AWS Firehose, AWS Glue, AWS Athena, and AWS EMR (optional).
3. It is open-source. It means you can fork it, send PRs, and rely on the community of developers.
4. We will keep on adding additional features according to your feedback.

## When do I need it

tba

## Command line

### Installation

```bash
pip install floppr
```

### Command line options

* `floppr init`: Sets up the data pipeline.
* `floppr init --emr`: Sets up the data pipeline along with AWS EMR.
* `floppr destroy`: Tears down the data pipeline.
* `floppr destroy --data`: Tears down the data pipeline and deletes all data.

## Reporting API

### JavaScript

#### Installation

Add the following code you your page:

```html
<script>
     !function(){window.floppr=window.floppr||function(){(window.floppr.query=window.floppr.query||[]).push(arguments)};var e=document.createElement("script");e.async=!0,e.src="https://floppr.github.io/api.js";var r=document.getElementsByTagName("script")[0];r.parentNode.insertBefore(e,r)}();
</script>
```
Call the following code when the page is loaded:

```javascript
floppr.init({
    account: '<your AWS account id, e.g. "938015383264">',
    product: {
       code: '<product code>',
       build: '<product build>'
    }
});
```

#### Reporting

To report an event, call the following code:

```javascript
floppr.event({
    subsystem: '<subsystem you report an event from, e.g. "Login form">',
    id: '<event id, e.g. "Login button is clicked"',
    properties: {
        '<an additional event property name, e.g. "User type">': '<the property value, e.g. "Paid">'
    }
});
```

### Usage

tba

## How much does it cost

With floppr, you pay only for what you use according to AWS's pricing:

* [AWS S3](https://aws.amazon.com/s3/pricing/)
* [AWS Glue](https://aws.amazon.com/glue/pricing/)
* [AWS Athena](https://aws.amazon.com/athena/pricing/)
* [AWS EMR](https://aws.amazon.com/emr/pricing/) (optional)

## How the pipeline works

tba

## How to access the data

### S3

tba

### AWS Athena

tba

### AWS EMR

tba
