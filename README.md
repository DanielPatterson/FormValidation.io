# FormValidation.io
Form Validation with FormValidation.io

#### JS Dependencies:
- formValidation.min.js
- formValidationframework.min.js

#### The Validation Script:
```js
$(document).ready(function() {
    $('#contactForm').formValidation({
        framework: 'bootstrap',
        err: {
            container: '#messages'
        },
        icon: {
            valid: 'glyphicon glyphicon-ok',
            invalid: 'glyphicon glyphicon-remove',
            validating: 'glyphicon glyphicon-refresh'
        },
        fields: {
            fullName: {
                validators: {
                    notEmpty: {
                        message: 'The full name is required and cannot be empty'
                    }
                }
            },
            email: {
                validators: {
                    notEmpty: {
                        message: 'The email address is required and cannot be empty'
                    },
                    emailAddress: {
                        message: 'The email address is not valid'
                    }
                }
            },
            title: {
                validators: {
                    notEmpty: {
                        message: 'The title is required and cannot be empty'
                    },
                    stringLength: {
                        max: 100,
                        message: 'The title must be less than 100 characters long'
                    }
                }
            },
            content: {
                validators: {
                    notEmpty: {
                        message: 'The content is required and cannot be empty'
                    },
                    stringLength: {
                        max: 500,
                        message: 'The content must be less than 500 characters long'
                    }
                }
            }
        }
    });
});
```
