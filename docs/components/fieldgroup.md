# FieldGroup

[`FieldGroup`](https://github.com/zakness/birchbox-gitbook/tree/1ad9356b440d8ffd191f6222475ef6f0c15444b0/src/components/Form/FieldGroup/index.js) is a simple wrapper for dividing a Form into parts that each offer hooks for edit mode, validation, save, next, and cancel.

## Props

| Prop | Type | Description | Default |
| :--- | :--- | :--- | :--- |
| cancelButtonProps | object |  | {} |
| className | string | Cancel button class name |  |
| onClick | function | Cancel button click handler |  |
| isEdit | boolean | Optional. Use edit mode \(i.e., show Cancel button, only allow save when `props.isEdited`\) |  |
| isEdited | boolean | Optional. During edit mode, enable the Save button. |  |
| nextButtonProps | object |  | {} |
| className | string | Cancel button class name |  |
| label | String | Cancel button label |  |
| onClick | function | Next button click handler |  |
| onSave | function | Field Group Save Handler |  |
| validator | function | Optional. Field Group validation handler with callback |  |

## Example

```text
const fieldGroupProps = {
  isEdit: this.state.isEditMode,
  isEdited: this.state.changesMade,
  onSave: this.saveData,
  cancelButtonProps: {
    className: buttonStyles.dark,
    onClick: this.handleCancel,
  },
  validator: this.state.needsValidation ? this.validateSection : undefined,
  nextButtonProps: {
    label: this.state.isEditMode ? 'Save' : 'Next',
    className: buttonStyles.default,
    onClick: this.changeSection,
  },
}

<Form>
  <FieldGroup {...fieldGroupProps}>
    <Input type='text' label='name' />
    <Input type='email' label='email' />
  </FieldGroup>
</Form>
```

