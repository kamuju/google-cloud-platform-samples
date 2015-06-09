# How to become a contributor and submit your own code #

## Contributor License Agreements ##

We'd love to accept your sample apps and patches! However, before we can take them, we have to jump a couple of legal hurdles.

Please fill out either the individual or corporate Contributor License Agreement.

  * If you are an individual writing original source code and you're sure you own the intellectual property, then you'll need to sign an [individual CLA](http://code.google.com/legal/individual-cla-v1.0.html).
  * If you work for a company that wants to allow you to contribute your work to Google Data Python Client Library, then you'll need to sign a [corporate CLA](http://code.google.com/legal/corporate-cla-v1.0.html).

Follow either of the two links above to access the appropriate CLA and instructions for how to sign and return it. Once we receive it, we'll add you to the official list of contributors and be able to accept your patches.

## Submitting Patches ##

  1. Decide which code you want to submit. A submission should be a set of changes that addresses one issue in the Google Cloud Platform Samples repo [issue tracker](http://code.google.com/p/google-cloud-platform-samples/issues/list). Please don't mix more than one logical change per submittal, because it makes the history hard to follow. If you want to make a change that doesn't have a corresponding issue in the issue tracker, please create one.
  1. Also, coordinate with team members that are listed on the issue in question. This ensures that work isn't being duplicated and communicating your plan early also generally leads to better patches.
  1. Ensure that your code adheres to the existing style in the sample to which you are contributing.
  1. Ensure that there are unit tests for your code.
  1. Sign a Contributor License Agreement.
  1. Use the `upload.py` script to upload your patches to [codereview.appspot.com](http://codereview.appspot.com) for review.


## Submitting a sample ##

Same procedure as for submitting patches, but with the additional provisions:

  1. Add a README file following the format below.
  1. Start with the Try-Prediction sample as a template for how your sample should be structured.

### Using `upload.py` and the code review site ###

**Note** that if you have 2-factor authentication turned on for your account then you will need to go to https://google.com/accounts, Select Security Tab, then Edit "Authorizing applications and sites" and add an application specific password for upload.py.

The following command:

```
$ python upload.py
```

will prompt you for any required input and submit your code to the review site. `upload.py` is created by the [Rietveldt project](http://code.google.com/p/rietveld), and the documents on their wiki plus `upload.py --help` can help if you need more detailed instructions. There is also an article [here](http://code.google.com/p/rietveld/wiki/CodeReviewHelp) on how to go through the code review process.

Once the code review has started you may be asked to make changes to your code. Once you have made those changes run `upload.py` again to update the patch. You will need to know the codereview issue number. Assuming it is 123456:

```
$ python upload.py -i 123456
```

## Submitting Your Approved Code ##

When you submit make sure to add a link to where the code was reviewed in the commit message, along with a good description of the change:

```
This change blah blah blah.

Reviewed in http://codereview.appspot.com/123456/.
```

If there is an associated issue also add this line
to the commit message, which will automatically mark
the issue as closed.

```
Fixes issue #nnnn.
```

Once the issue is committed, go back and add a link to the commit to
the review, and mark the review as completed.