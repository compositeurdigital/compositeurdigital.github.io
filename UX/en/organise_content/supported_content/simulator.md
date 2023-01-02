# Mortgage Simulator

## Summary
* [Description](#description)
* [Actions within Compositeur Digital UX](#actions-within-compositeur-digital-ux)
* [Content extension](#content-extension)
* [Create a mortgage simulator](#create-a-mortgage-simulator)
* [Metadata available](#metadata-available)
* [Download a sample](#download-a-sample)

## Description

This content type allows you to display an interactive mortgage simulator with editable parameters.

![Content Mortgage Simulator](../../img/content_mortgage_simulator.JPG)

## Actions within Compositeur Digital UX

Mortgage simulator supports the following action. To have a complete overview of each action, [see the section Actions](actions.md)

**Actions menu**

| Annotate | Capture  | Duplicate | Open in native app | Save as  | Selection | Share    |
|:--------:|:--------:|:---------:|:------------------:|:--------:|:---------:|:--------:|
| &#x2716; | &#x2714; | &#x2714;  | &#x2714;           | &#x2714; | &#x2714;  | &#x2714; |

## Content extension

To use a mortgage simulator, add the extension `.simupret` at the end of the name of your folder.

## Create a mortgage simulator

1. In your environment folder, create a folder named `<Name of your mortgage simulator>.simupret` (e.g. `My simulator.simupret`).
1. (Optional) You can change the preview of the mortgage simulator. In your `.simupret` folder, put an image (`.jpg` or `.png`) named `_preview`. If you don't provide a `_preview`, the item will have a default preview (shown below).

![Mortgage simulator folder](../../img/content_mortgage_simulator_folder.JPG) ![Mortgage simulator preview](../../img/content_mortgage_simulator_preview.JPG)

## Metadata available

| Metadata Key                                 | Type     | Default            | Description |
|:-------------------------------------------- |:---------|:-------------------|:-|
| `simulator.additionalCostsRateDefaultValue`  | `number` | 0                  | sets the default value of the addtional costs rate |
| `simulator.additionalCostsRateLabel`         | `text`   | `Additional costs` | sets the label of the additional costs line | 
| `simulator.additionalCostsRateMinValue`      | `number` | 0                  | sets the min value for the additional costs rate |
| `simulator.additionalCostsRateMaxValue`      | `number` | 50                 | sets the max value for the additional costs rate |
| `simulator.additionalCostsRateTickFrequency` | `number` | 1                  | sets the interval between two values for the additional costs rate |
| `simulator.creditMaxValue`                   | `number` | 800000             | sets the maximum value of a loan |
| `simulator.creditTickFrequency`              | `number` | 5000               | sets the interval between two values for a loan |
| `simulator.creditDefaultValue`               | `number` | 300000             | sets the default loan value |
| `simulator.durationMinValue`                 | `number` | 5                  | sets the shortest duration of a loan |
| `simulator.durationMaxValue`                 | `number` | 30                 | sets the longest duration of a loan |
| `simulator.durationTickFrequency`            | `number` | 1                  | sets the interval between two values for a loan duration |
| `simulator.durationDefaultValue`             | `number` | 20                 | sets the default duration of a loan |
| `simulator.hideInfine`                       | `number` | false              | hide the "in Fine" option |
| `simulator.infineDefaultValue`               | `number` | false              | sets the default value of a In Fine option |

[Access common metadatas](../advanced_setting.md#summary)

## Download a sample

A Demo Universe which contains samples for a mortgage simulator is available, [give it a try!](../Demo-Universe.zip) &#x1f604;


Next : [Savings simulator](savings_simulator.md)

[Back to Supported Content](index.md)
