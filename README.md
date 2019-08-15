This is a free and open-source tool that sets up a product analytics data pipeline in your AWS account and helps you manage it. With floppr, you can set up a data pipeline within minutes, without having DevOps or data engineers. 

It offers an API to report event from your product, and a command line tool to manage the data pipeline and. Once the data starts streamed from your product, you can use the AWS resources for analytics: AWS Athena, AWS QuickSight and AWS EMR (if needed).

## How does it works

1. Make sure you have a AWS account. If not, [create](https://aws.amazon.com/premiumsupport/knowledge-center/create-and-activate-aws-account/) one.
2. Install the `floppr` command line tool.
3. Run the `init` floppr command:

```bash
floppr init
AWS Access Key ID: ****
AWS Secret Access Key: ****
```

tba (elaborate on the organisation domain)

This command sets up a data pipeline within your AWS account. The pipeline includes an HTTP ingestion endpoint, a nightly batch ETL job, Athena database and table, AWS EMR (if needed), etc

4. Download the reporting API
5. Call the API from your product

tba (elaborate on the organisation domain)

That's it! Your product events get to S3 and are available via AWS Athena, AWS QuickSight, and AWS EMR (if needed).

## Why it works

1. It sets up and help you manage a data pipeline with your AWS account. You don't need DevOps or Data Engineers.
2. It is free. You're charged with your AWS account only for wht you use and according to the pricing of the AWS Firehose, AWS Glue, AWS Athena, and AWS EMR (if needed).
3. It is open-source. It means you can fork it, send PRs, and rely on the community of developers.
4. We will keep on adding additional features according to your feedback.

## When do I need it

tba

## Command line

### Installation

```bash
pip install floppr
```

### How to use the command line

## Reporting API

### JavaScript

#### Installation


Add the following code you your page:

```html
tba
```

#### Usage

Event can be reported from your product this way:

```javascript
floppr.event({
    subsystem: '<subsystem you report an event from, e.g. "Login form">',
    id: '<event id, e.g. "Login button is clicked"',
    properties: {
        '<an additional event property name, e.g. "User type">': '<the property value, e.g. "Paid">',
    }
});
```

tba (elaborate on the organisation domain)

### Usage

tba

## How much does it cost

tba
