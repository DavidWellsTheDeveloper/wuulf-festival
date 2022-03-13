<template>
    <v-container>
        <v-row justify="center">
            <v-col>
        <script src="https://cdn03.jotfor.ms/static/prototype.forms.js" type="text/javascript"></script>
        <script src="https://cdn01.jotfor.ms/static/jotform.forms.js?3.3.31676" type="text/javascript"></script>
        <script defer src="https://cdnjs.cloudflare.com/ajax/libs/punycode/1.4.1/punycode.js"></script>
        <script src="https://cdn02.jotfor.ms/js/stripeSCA.js?v=3.3.31676" type="text/javascript"></script>
        <script src="https://cdn03.jotfor.ms/js/stripe.js?v=3.3.31676" type="text/javascript"></script>
        <script src="https://js.jotform.com/vendor/postMessage.js?3.3.31676" type="text/javascript"></script>
        <script src="https://js.jotform.com/WidgetsServer.js?v=1646880650629" type="text/javascript"></script>
        <script type="text/javascript">	JotForm.newDefaultTheme = false;
            JotForm.extendsNewTheme = false;
            JotForm.newPaymentUIForNewCreatedForms = false;
            JotForm.clearFieldOnHide="disable";
            JotForm.submitError="jumpToFirstError";

            JotForm.init(function(){
            /*INIT-START*/
            setTimeout(function() {
                $('input_10').hint('ex: 3');
            }, 20);
            productID = {"0":"input_9_1006","1":"input_9_1007","2":"input_9_1008","3":"input_9_1009","4":"input_9_1010"};
            paymentType = "product";
            JotForm.setCurrencyFormat('USD',true, 'point');
            JotForm.totalCounter({"input_9_1006_0":{"price":"0","child":true,"specialPriceField":"input_9_1006_0","specialPriceList":["270","240","210","840","540"],"quantityField":"input_9_quantity_1006_0_0"},"input_9_1006_1":{"price":"0","child":true,"specialPriceField":"input_9_1006_1","specialPriceList":["270","240","210","840","540"],"quantityField":"input_9_quantity_1006_1_0"},"input_9_1006_2":{"price":"0","child":true,"specialPriceField":"input_9_1006_2","specialPriceList":["270","240","210","840","540"],"quantityField":"input_9_quantity_1006_2_0"},"input_9_1006_3":{"price":"0","child":true,"specialPriceField":"input_9_1006_3","specialPriceList":["270","240","210","840","540"],"quantityField":"input_9_quantity_1006_3_0"},"input_9_1006_4":{"price":"0","child":true,"specialPriceField":"input_9_1006_4","specialPriceList":["270","240","210","840","540"],"quantityField":"input_9_quantity_1006_4_0"},"input_9_1007_0":{"price":"0","child":true,"specialPriceField":"input_9_1007_0","specialPriceList":["204","102"],"quantityField":"input_9_quantity_1007_0_0"},"input_9_1007_1":{"price":"0","child":true,"specialPriceField":"input_9_1007_1","specialPriceList":["204","102"],"quantityField":"input_9_quantity_1007_1_0"},"input_9_1008_0":{"price":"0","child":true,"specialPriceField":"input_9_1008_0","specialPriceList":["260","175","125","0.00"],"quantityField":"input_9_quantity_1008_0_0"},"input_9_1008_1":{"price":"0","child":true,"specialPriceField":"input_9_1008_1","specialPriceList":["260","175","125","0.00"],"quantityField":"input_9_quantity_1008_1_0"},"input_9_1008_2":{"price":"0","child":true,"specialPriceField":"input_9_1008_2","specialPriceList":["260","175","125","0.00"],"quantityField":"input_9_quantity_1008_2_0"},"input_9_1008_3":{"price":"0","child":true,"specialPriceField":"input_9_1008_3","specialPriceList":["260","175","125","0.00"],"quantityField":"input_9_quantity_1008_3_0"},"input_9_1009_0":{"price":"0","child":true,"specialPriceField":"input_9_1009_0","specialPriceList":["105","100","45.00","17","49","39","115.00","62.25","0"],"quantityField":"input_9_quantity_1009_0_0"},"input_9_1009_1":{"price":"0","child":true,"specialPriceField":"input_9_1009_1","specialPriceList":["105","100","45.00","17","49","39","115.00","62.25","0"],"quantityField":"input_9_quantity_1009_1_0"},"input_9_1009_2":{"price":"0","child":true,"specialPriceField":"input_9_1009_2","specialPriceList":["105","100","45.00","17","49","39","115.00","62.25","0"],"quantityField":"input_9_quantity_1009_2_0"},"input_9_1009_3":{"price":"0","child":true,"specialPriceField":"input_9_1009_3","specialPriceList":["105","100","45.00","17","49","39","115.00","62.25","0"],"quantityField":"input_9_quantity_1009_3_0"},"input_9_1009_4":{"price":"0","child":true,"specialPriceField":"input_9_1009_4","specialPriceList":["105","100","45.00","17","49","39","115.00","62.25","0"],"quantityField":"input_9_quantity_1009_4_0"},"input_9_1009_5":{"price":"0","child":true,"specialPriceField":"input_9_1009_5","specialPriceList":["105","100","45.00","17","49","39","115.00","62.25","0"],"quantityField":"input_9_quantity_1009_5_0"},"input_9_1009_6":{"price":"0","child":true,"specialPriceField":"input_9_1009_6","specialPriceList":["105","100","45.00","17","49","39","115.00","62.25","0"],"quantityField":"input_9_quantity_1009_6_0"},"input_9_1009_7":{"price":"0","child":true,"specialPriceField":"input_9_1009_7","specialPriceList":["105","100","45.00","17","49","39","115.00","62.25","0"],"quantityField":"input_9_quantity_1009_7_0"},"input_9_1009_8":{"price":"0","child":true,"specialPriceField":"input_9_1009_8","specialPriceList":["105","100","45.00","17","49","39","115.00","62.25","0"],"quantityField":"input_9_quantity_1009_8_0"},"input_9_1010_0":{"price":"0","child":true,"specialPriceField":"input_9_1010_0","specialPriceList":["2","5","1"],"quantityField":"input_9_quantity_1010_0_0"},"input_9_1010_1":{"price":"0","child":true,"specialPriceField":"input_9_1010_1","specialPriceList":["2","5","1"],"quantityField":"input_9_quantity_1010_1_0"},"input_9_1010_2":{"price":"0","child":true,"specialPriceField":"input_9_1010_2","specialPriceList":["2","5","1"],"quantityField":"input_9_quantity_1010_2_0"}});
            $$('.form-product-custom_quantity').each(function(el, i){el.observe('blur', function(){isNaN(this.value) || this.value < 1 ? this.value = '0' : this.value = parseInt(this.value)})});
            $$('.form-product-custom_quantity').each(function(el, i){el.observe('focus', function(){this.value == 0 ? this.value = '' : this.value})});
        if(typeof PaymentStock !== "undefined") { PaymentStock.orderedSubproductOptionNames = {"1006":["Room Type"],"1007":["Meal Type"],"1008":["Registration Type"],"1009":["Activity"],"1010":["Activity"]} } 
            JotForm.setStripeSettings('pk_live_mjpaQ0pivO0fCZ0aaDjwgCJM', '5', '5', '4', '6', '0');
            JotForm.handleProductLightbox();
        if (window.JotForm && JotForm.accessible) $('input_17').setAttribute('tabindex',0);
            JotForm.alterTexts(undefined);
            JotForm.alterTexts({"couponApply":"Apply","couponBlank":"Please enter a coupon.","couponChange":"","couponEnter":"Enter coupon","couponExpired":"Coupon is expired. Please try another one.","couponInvalid":"Coupon is invalid.","couponValid":"Coupon is valid.","shippingShipping":"Shipping","taxTax":"Tax","totalSubtotal":"Subtotal","totalTotal":"Total"}, true);
            /*INIT-END*/
            });

        JotForm.prepareCalculationsOnTheFly([null,{"name":"heading","qid":"1","text":"WUULF Registration","type":"control_head"},null,{"description":"","name":"name","qid":"3","text":"Name","type":"control_fullname"},{"description":"","name":"email","qid":"4","subLabel":"example@example.com","text":"Email","type":"control_email"},{"description":"","name":"address","qid":"5","text":"Address","type":"control_address"},{"description":"","name":"phoneNumber","qid":"6","text":"Phone Number","type":"control_phone"},{"name":"divider","qid":"7","type":"control_divider"},null,{"description":"","name":"paymentDetails","qid":"9","text":"Payment Details","type":"control_stripe"},{"description":"","name":"number","qid":"10","subLabel":"Insert Attendeee Details Below","text":"Number of Attendees","type":"control_number"},null,null,null,null,null,{"name":"attendeeDetails","qid":"16","text":"Attendee Details (Enter for Each Attendee and Click Save Below)","type":"control_widget"},{"description":"","name":"specialRequests17","qid":"17","subLabel":"","text":"Special Requests or Comments (Request a Specific Roommate, etc.)","type":"control_textarea"},null,{"name":"clickTo","qid":"19","text":"\u003C!--The main portion of registration has ended. If you would still like to join us, you will need to sign up for your WUULF registration below and coordinate your housing and meals directly with the ranch. Ghost Ranch can be contacted at 505-685-1000 for that purpose.--\u003E\nIf you have any questions on this form, please contact Dave at dave1twells@gmail.com\n&nbsp;\n&nbsp;Checks can be mailed to&nbsp;\nWUULF c\u002Fo Ariel Stokes, 2262 Trestle Road, Fort Collins, CO 80525\nIf mailing a check, please include Itemized information about what you are paying for along with your payment.","type":"control_text"},{"name":"clickTo20","qid":"20","text":"Welcome to WUULF 2020! \nWe are glad you will be joining us from June 15th-June 21st!\nIf you would like to see the&nbsp;schedule for this year to help in your decisions, please Click Here.\n\u003C!-- The main portion of registration has ended. If you would still like to join us, you will need to sign up for your WUULF registration through this web page and coordinate your housing and meals directly with the ranch. Ghost Ranch can be contacted at 505-685-1000. --\u003E","type":"control_text"},{"name":"submit","qid":"21","text":"Submit","type":"control_button"}]);
        setTimeout(function() {
        JotForm.paymentExtrasOnTheFly([null,{"name":"heading","qid":"1","text":"WUULF Registration","type":"control_head"},null,{"description":"","name":"name","qid":"3","text":"Name","type":"control_fullname"},{"description":"","name":"email","qid":"4","subLabel":"example@example.com","text":"Email","type":"control_email"},{"description":"","name":"address","qid":"5","text":"Address","type":"control_address"},{"description":"","name":"phoneNumber","qid":"6","text":"Phone Number","type":"control_phone"},{"name":"divider","qid":"7","type":"control_divider"},null,{"description":"","name":"paymentDetails","qid":"9","text":"Payment Details","type":"control_stripe"},{"description":"","name":"number","qid":"10","subLabel":"Insert Attendeee Details Below","text":"Number of Attendees","type":"control_number"},null,null,null,null,null,{"name":"attendeeDetails","qid":"16","text":"Attendee Details (Enter for Each Attendee and Click Save Below)","type":"control_widget"},{"description":"","name":"specialRequests17","qid":"17","subLabel":"","text":"Special Requests or Comments (Request a Specific Roommate, etc.)","type":"control_textarea"},null,{"name":"clickTo","qid":"19","text":"\u003C!--The main portion of registration has ended. If you would still like to join us, you will need to sign up for your WUULF registration below and coordinate your housing and meals directly with the ranch. Ghost Ranch can be contacted at 505-685-1000 for that purpose.--\u003E\nIf you have any questions on this form, please contact Dave at dave1twells@gmail.com\n&nbsp;\n&nbsp;Checks can be mailed to&nbsp;\nWUULF c\u002Fo Ariel Stokes, 2262 Trestle Road, Fort Collins, CO 80525\nIf mailing a check, please include Itemized information about what you are paying for along with your payment.","type":"control_text"},{"name":"clickTo20","qid":"20","text":"Welcome to WUULF 2020! \nWe are glad you will be joining us from June 15th-June 21st!\nIf you would like to see the&nbsp;schedule for this year to help in your decisions, please Click Here.\n\u003C!-- The main portion of registration has ended. If you would still like to join us, you will need to sign up for your WUULF registration through this web page and coordinate your housing and meals directly with the ranch. Ghost Ranch can be contacted at 505-685-1000. --\u003E","type":"control_text"},{"name":"submit","qid":"21","text":"Submit","type":"control_button"}]);}, 20); 
        </script>
        <link href="https://cdn01.jotfor.ms/static/formCss.css?3.3.31676" rel="stylesheet" type="text/css" />
        <link type="text/css" rel="stylesheet" href="https://cdn02.jotfor.ms/css/styles/nova.css?3.3.31676" />
        <style type="text/css">@media print{.form-section{display:inline!important}.form-pagebreak{display:none!important}.form-section-closed{height:auto!important}.page-section{position:initial!important}}</style>
        <link type="text/css" rel="stylesheet" href="https://cdn03.jotfor.ms/themes/CSS/566a91c2977cdfcd478b4567.css?"/>
        <link type="text/css" rel="stylesheet" href="https://cdn01.jotfor.ms/css/styles/payment/payment_feature.css?3.3.31676" />
        <style type="text/css">
            .form-label-left{
                width:160px;
            }
            .form-line{
                padding-top:20px;
                padding-bottom:20px;
            }
            .form-label-right{
                width:160px;
            }
            .form-all{
                width:690px;
                color:#555 !important;
                font-family:"Lucida Grande", "Lucida Sans Unicode", "Lucida Sans", Verdana, sans-serif;
                font-size:14px;
            }
        </style>

        <style type="text/css" id="form-designer-style">
            /* Injected CSS Code */
        .form-label.form-label-auto {
                
                display: inline-block;
                float: left;
                text-align: left;
            
            } /*PREFERENCES STYLE*/
            .form-all {
            font-family: Lucida Grande, sans-serif;
            }
            .form-all .qq-upload-button,
            .form-all .form-submit-button,
            .form-all .form-submit-reset,
            .form-all .form-submit-print {
            font-family: Lucida Grande, sans-serif;
            }
            .form-all .form-pagebreak-back-container,
            .form-all .form-pagebreak-next-container {
            font-family: Lucida Grande, sans-serif;
            }
            .form-header-group {
            font-family: Lucida Grande, sans-serif;
            }
            .form-label {
            font-family: Lucida Grande, sans-serif;
            }
        
            .form-label.form-label-auto {
            
            display: inline-block;
            float: left;
            text-align: left;
        
            }
        
            .form-line {
            margin-top: 20px;
            margin-bottom: 20px;
            }
        
            .form-all {
            max-width: 690px;
            width: 100%;
            }
        
            .form-label.form-label-left,
            .form-label.form-label-right,
            .form-label.form-label-left.form-label-auto,
            .form-label.form-label-right.form-label-auto {
            width: 160px;
            }
        
            .form-all {
            font-size: 14px
            }
            .form-all .qq-upload-button,
            .form-all .qq-upload-button,
            .form-all .form-submit-button,
            .form-all .form-submit-reset,
            .form-all .form-submit-print {
            font-size: 14px
            }
            .form-all .form-pagebreak-back-container,
            .form-all .form-pagebreak-next-container {
            font-size: 14px
            }
        
            .supernova {
            background-color: #f5f5f5;
            }
            .supernova body {
            background: transparent;
            }
        
            .supernova .form-all, .form-all {
            background-color: #fff;
            }
        
            .form-all {
            color: #555;
            }
            .form-header-group .form-header {
            color: #555;
            }
            .form-header-group .form-subHeader {
            color: #555;
            }
            .form-label-top,
            .form-label-left,
            .form-label-right,
            .form-html,
            .form-checkbox-item label,
            .form-radio-item label {
            color: #555;
            }
            .form-sub-label {
            color: #6f6f6f;
            }
        
            .form-textbox,
            .form-textarea,
            .form-dropdown,
            .form-radio-other-input,
            .form-checkbox-other-input,
            .form-captcha input,
            .form-spinner input {
            background-color: #fff;
            }
        
            .form-line-error {
            overflow: hidden;
            transition: none;
            background-color: #FFF4F4;
            }

            .form-line-error .form-error-message {
            background-color: #FF3200;
            clear: both;
            float: none;
            }

            .form-line-error .form-error-arrow {
            border-bottom-color: #FF3200;
            }

            .form-line-error input:not(#coupon-input),
            .form-line-error textarea,
            .form-line-error .form-validation-error {
            border: 1px solid #FF3200;
            .box-shadow(0 0 3px #FF3200);
            }
        
            .supernova {
            background-image: none;
            }
            #stage {
            background-image: none;
            }
        
            .form-all {
            background-image: none;
            }
        
            .form-all {
            position: relative;
            }
            .form-all:before {
            content: "";
            background-image: url("https://www.jotform.com/uploads/WesternUULifeFestival/form_files/logoNew.5c16d1bfd218a2.92103068.jpg");
            display: inline-block;
            height: 134px;
            position: absolute;
            background-size: 690px 134px;
            background-repeat: no-repeat;
            width: 100%;
            }
            .form-all {
            margin-top: 144px !important;
            }
            .form-all:before {
            top: -144px;
            left: 0;
            background-position: top left;
            }
                
        .ie-8 .form-all:before { display: none; }
        .ie-8 {
            margin-top: auto;
            margin-top: initial;
        }
        
        /*PREFERENCES STYLE*//*__INSPECT_SEPERATOR__*/
            /* Injected CSS Code */
        </style>

        <link type="text/css" rel="stylesheet" href="https://cdn02.jotfor.ms/css/styles/buttons/form-submit-button-simple_black.css?3.3.31676"/>
        <form class="jotform-form" action="https://submit.jotform.com/submit/220645832594158/" method="post" name="form_220645832594158" id="220645832594158" accept-charset="utf-8" autocomplete="on">
        <input type="hidden" name="formID" value="220645832594158" />
        <input type="hidden" id="JWTContainer" value="" />
        <input type="hidden" id="cardinalOrderNumber" value="" />
        <div style="margin:auto;" role="main" class="form-all">
            <ul class="form-section page-section">
            <li id="cid_1" class="form-input-wide" data-type="control_head">
                <div class="form-header-group  header-default">
                <div class="header-text httal htvam">
                    <h2 id="header_1" class="form-header" data-component="header">
                    WUULF Registration
                    </h2>
                </div>
                </div>
            </li>
            <li class="form-line" data-type="control_text" id="id_20">
                <div id="cid_20" class="form-input-wide">
                <div id="text_20" class="form-html" data-component="text">
                    <p><span style="font-size: 12pt;"><strong>Welcome to WUULF 2020! </strong></span></p>
                    <p>We are glad you will be joining us from June 15th-June 21st!</p>
                    <p>If you would like to see the schedule for this year to help in your decisions, please <a href="https://wuulf.org/2020-schedule/" target="_blank" rel="nofollow">Click Here.</a></p>
                </div>
                </div>
            </li>
            <li class="form-line" data-type="control_fullname" id="id_3">
                <label class="form-label form-label-left form-label-auto" id="label_3" for="first_3"> Name </label>
                <div id="cid_3" class="form-input">
                <div data-wrapper-react="true">
                    <span class="form-sub-label-container" style="vertical-align:top" data-input-type="first">
                    <input type="text" id="first_3" name="q3_name[first]" class="form-textbox" data-defaultvalue="" autoComplete="section-input_3 given-name" size="10" value="" data-component="first" aria-labelledby="label_3 sublabel_3_first" />
                    <label class="form-sub-label" for="first_3" id="sublabel_3_first" style="min-height:13px" aria-hidden="false"> First Name </label>
                    </span>
                    <span class="form-sub-label-container" style="vertical-align:top" data-input-type="last">
                    <input type="text" id="last_3" name="q3_name[last]" class="form-textbox" data-defaultvalue="" autoComplete="section-input_3 family-name" size="15" value="" data-component="last" aria-labelledby="label_3 sublabel_3_last" />
                    <label class="form-sub-label" for="last_3" id="sublabel_3_last" style="min-height:13px" aria-hidden="false"> Last Name </label>
                    </span>
                </div>
                </div>
            </li>
            <li class="form-line" data-type="control_email" id="id_4">
                <label class="form-label form-label-left form-label-auto" id="label_4" for="input_4"> Email </label>
                <div id="cid_4" class="form-input">
                <span class="form-sub-label-container" style="vertical-align:top">
                    <input type="email" id="input_4" name="q4_email" class="form-textbox validate[Email]" data-defaultvalue="" size="30" value="" data-component="email" aria-labelledby="label_4 sublabel_input_4" />
                    <label class="form-sub-label" for="input_4" id="sublabel_input_4" style="min-height:13px" aria-hidden="false"> example@example.com </label>
                </span>
                </div>
            </li>
            <li class="form-line" data-type="control_address" id="id_5">
                <label class="form-label form-label-left form-label-auto" id="label_5" for="input_5_addr_line1"> Address </label>
                <div id="cid_5" class="form-input">
                <div summary="" class="form-address-table jsTest-addressField">
                    <div class="form-address-line-wrapper jsTest-address-line-wrapperField">
                    <span class="form-address-line form-address-street-line jsTest-address-lineField">
                        <span class="form-sub-label-container" style="vertical-align:top">
                        <input type="text" id="input_5_addr_line1" name="q5_address[addr_line1]" class="form-textbox form-address-line" data-defaultvalue="" autoComplete="section-input_5 address-line1" value="" data-component="address_line_1" aria-labelledby="label_5 sublabel_5_addr_line1" />
                        <label class="form-sub-label" for="input_5_addr_line1" id="sublabel_5_addr_line1" style="min-height:13px" aria-hidden="false"> Street Address </label>
                        </span>
                    </span>
                    </div>
                    <div class="form-address-line-wrapper jsTest-address-line-wrapperField">
                    <span class="form-address-line form-address-street-line jsTest-address-lineField">
                        <span class="form-sub-label-container" style="vertical-align:top">
                        <input type="text" id="input_5_addr_line2" name="q5_address[addr_line2]" class="form-textbox form-address-line" data-defaultvalue="" autoComplete="section-input_5 address-line2" value="" data-component="address_line_2" aria-labelledby="label_5 sublabel_5_addr_line2" />
                        <label class="form-sub-label" for="input_5_addr_line2" id="sublabel_5_addr_line2" style="min-height:13px" aria-hidden="false"> Street Address Line 2 </label>
                        </span>
                    </span>
                    </div>
                    <div class="form-address-line-wrapper jsTest-address-line-wrapperField">
                    <span class="form-address-line form-address-city-line jsTest-address-lineField ">
                        <span class="form-sub-label-container" style="vertical-align:top">
                        <input type="text" id="input_5_city" name="q5_address[city]" class="form-textbox form-address-city" data-defaultvalue="" autoComplete="section-input_5 address-level2" value="" data-component="city" aria-labelledby="label_5 sublabel_5_city" />
                        <label class="form-sub-label" for="input_5_city" id="sublabel_5_city" style="min-height:13px" aria-hidden="false"> City </label>
                        </span>
                    </span>
                    <span class="form-address-line form-address-state-line jsTest-address-lineField ">
                        <span class="form-sub-label-container" style="vertical-align:top">
                        <input type="text" id="input_5_state" name="q5_address[state]" class="form-textbox form-address-state" data-defaultvalue="" autoComplete="section-input_5 address-level1" value="" data-component="state" aria-labelledby="label_5 sublabel_5_state" />
                        <label class="form-sub-label" for="input_5_state" id="sublabel_5_state" style="min-height:13px" aria-hidden="false"> State / Province </label>
                        </span>
                    </span>
                    </div>
                    <div class="form-address-line-wrapper jsTest-address-line-wrapperField">
                    <span class="form-address-line form-address-zip-line jsTest-address-lineField ">
                        <span class="form-sub-label-container" style="vertical-align:top">
                        <input type="text" id="input_5_postal" name="q5_address[postal]" class="form-textbox form-address-postal" data-defaultvalue="" autoComplete="section-input_5 postal-code" value="" data-component="zip" aria-labelledby="label_5 sublabel_5_postal" />
                        <label class="form-sub-label" for="input_5_postal" id="sublabel_5_postal" style="min-height:13px" aria-hidden="false"> Postal / Zip Code </label>
                        </span>
                    </span>
                    </div>
                </div>
                </div>
            </li>
            <li class="form-line" data-type="control_phone" id="id_6">
                <label class="form-label form-label-left form-label-auto" id="label_6" for="input_6_area"> Phone Number </label>
                <div id="cid_6" class="form-input">
                <div data-wrapper-react="true">
                    <span class="form-sub-label-container" style="vertical-align:top" data-input-type="areaCode">
                    <input type="tel" id="input_6_area" name="q6_phoneNumber[area]" class="form-textbox" data-defaultvalue="" autoComplete="section-input_6 tel-area-code" value="" data-component="areaCode" aria-labelledby="label_6 sublabel_6_area" />
                    <span class="phone-separate" aria-hidden="true">
                        -
                    </span>
                    <label class="form-sub-label" for="input_6_area" id="sublabel_6_area" style="min-height:13px" aria-hidden="false"> Area Code </label>
                    </span>
                    <span class="form-sub-label-container" style="vertical-align:top" data-input-type="phone">
                    <input type="tel" id="input_6_phone" name="q6_phoneNumber[phone]" class="form-textbox" data-defaultvalue="" autoComplete="section-input_6 tel-local" value="" data-component="phone" aria-labelledby="label_6 sublabel_6_phone" />
                    <label class="form-sub-label" for="input_6_phone" id="sublabel_6_phone" style="min-height:13px" aria-hidden="false"> Phone Number </label>
                    </span>
                </div>
                </div>
            </li>
            <li class="form-line" data-type="control_number" id="id_10">
                <label class="form-label form-label-left form-label-auto" id="label_10" for="input_10"> Number of Attendees </label>
                <div id="cid_10" class="form-input">
                <span class="form-sub-label-container" style="vertical-align:top">
                    <input type="number" id="input_10" name="q10_number" data-type="input-number" class=" form-number-input form-textbox" data-defaultvalue="" style="width:60px" size="5" value="" placeholder="ex: 3" data-component="number" aria-labelledby="label_10 sublabel_input_10" step="any" />
                    <label class="form-sub-label" for="input_10" id="sublabel_input_10" style="min-height:13px" aria-hidden="false"> Insert Attendeee Details Below </label>
                </span>
                </div>
            </li>
            <li class="form-line jf-required" data-type="control_widget" id="id_16">
                <label class="form-label form-label-top" id="label_16" for="input_16">
                Attendee Details (Enter for Each Attendee and Click Save Below)
                <span class="form-required">
                    *
                </span>
                </label>
                <div id="cid_16" class="form-input-wide jf-required">
                <div data-widget-name="Infinite List" style="width:100%;text-align:Left;overflow-x:auto" data-component="widget-field">
                    <iframe data-client-id="52987bda949b78ac2b000009" title="Infinite List" frameBorder="0" scrolling="no" allowtransparency="true" allow="geolocation; microphone; camera; autoplay; encrypted-media; fullscreen" data-type="iframe" class="custom-field-frame" id="customFieldFrame_16" src="" style="max-width:500px;border:none;width:100%;height:120px" data-width="500" data-height="120">
                    </iframe>
                    <div class="widget-inputs-wrapper">
                    <input type="hidden" id="input_16" class="form-hidden form-widget widget-required " name="q16_attendeeDetails" value="" />
                    <input type="hidden" id="widget_settings_16" class="form-hidden form-widget-settings" value="%5B%7B%22name%22%3A%22columns%22%2C%22value%22%3A%22Camper%20Name%2C%20Camper%20Age%20at%20time%20of%20camp%2C%20Vegetarian%3F%20(Yes%2FNo)%2C%20Pronowns%20(he-she-they%20etc)%22%7D%2C%7B%22name%22%3A%22labelSave%22%2C%22value%22%3A%22Save%22%7D%2C%7B%22name%22%3A%22showCountOfListItems%22%2C%22value%22%3A%22Yes%22%7D%5D" data-version="2" />
                    </div>
                    <script type="text/javascript">
                    setTimeout(function()
        {
        var _cFieldFrame = document.getElementById("customFieldFrame_16");
        if (_cFieldFrame)
        {
            _cFieldFrame.onload = function()
            {
            if (typeof widgetFrameLoaded !== 'undefined')
            {
                widgetFrameLoaded(16, {
                "formID": 220645832594158
                })
            }
            };
            _cFieldFrame.src = "//widgets.jotform.io/list/?qid=16&ref=" + encodeURIComponent(window.location.protocol + "//" + window.location.host) + '' + '' + '&injectCSS=' + encodeURIComponent(window.location.search.indexOf("ndt=1") > -1);
            _cFieldFrame.addClassName("custom-field-frame-rendered");
        }
        }, 0);
                    </script>
                </div>
                </div>
            </li>
            <li class="form-line" data-type="control_divider" id="id_7">
                <div id="cid_7" class="form-input-wide">
                <div class="divider" aria-label="Divider" data-component="divider" style="border-bottom-width:1px;border-bottom-style:solid;border-color:#f5f5f5;height:1px;margin-left:0px;margin-right:0px;margin-top:5px;margin-bottom:5px">
                </div>
                </div>
            </li>
            <li class="form-line" data-type="control_text" id="id_19">
                <div id="cid_19" class="form-input-wide">
                <div id="text_19" class="form-html" data-component="text">
                    <p>If you have any questions on this form, please contact Dave at <a href="mailto:dave1.t.wells@gmail.com" target="_blank" rel="nofollow">dave1twells@gmail.com</a></p>
                    <p> </p>
                    <p> Checks can be mailed to </p>
                    <p>WUULF c/o Ariel Stokes, <br />2262 Trestle Road, <br />Fort Collins, CO 80525</p>
                    <p><br />If mailing a check, please include Itemized information about what you are paying for along with your payment.</p>
                </div>
                </div>
            </li>
            <li class="form-line" data-type="control_stripe" id="id_9" data-payment="true">
                <label class="form-label form-label-top" id="label_9" for="input_9"> Payment Details </label>
                <div id="cid_9" class="form-input-wide">
                <div data-wrapper-react="true" class="stripe-payment-wrapper" data-stripe-currency="USD">
                    <div data-wrapper-react="true" class="product-container-wrapper">
                    <div class="filter-container">
                    </div>
                    <input type="hidden" name="simple_fpc" data-payment_type="stripe" data-component="payment1" value="9" />
                    <input type="hidden" name="payment_total_checksum" id="payment_total_checksum" data-component="payment2" />
                    <div id="image-overlay" class="overlay-content" style="display:none">
                        <img id="current-image" />
                        <span class="lb-prev-button">
                        prev
                        </span>
                        <span class="lb-next-button">
                        next
                        </span>
                        <span class="lb-close-button">
                        ( X )
                        </span>
                        <span class="image-overlay-product-container">
                        <ul class="form-overlay-item" pid="1006" hasicon="false" hasimages="false" iconvalue="">
                        </ul>
                        <ul class="form-overlay-item" pid="1007" hasicon="false" hasimages="false" iconvalue="">
                        </ul>
                        <ul class="form-overlay-item" pid="1008" hasicon="false" hasimages="false" iconvalue="">
                        </ul>
                        <ul class="form-overlay-item" pid="1009" hasicon="false" hasimages="false" iconvalue="">
                        </ul>
                        <ul class="form-overlay-item" pid="1010" hasicon="false" hasimages="false" iconvalue="">
                        </ul>
                        </span>
                    </div>
                    <div data-wrapper-react="true">
                        <span class="form-product-item hover-product-item " categories="non-categorized" pid="1006">
                        <div data-wrapper-react="true" class="form-product-item-detail">
                            <input type="checkbox" class="form-checkbox form-product-has-subproducts form-product-input" id="input_9_1006" name="q9_paymentDetails[][id]" value="1006_expanded" checked="" disabled="" />
                            <label for="input_9_1006" class="form-product-container">
                            <span data-wrapper-react="true">
                                <span class="form-product-name" id="product-name-input_9_1006">
                                Lodging (If you would like other accommodations contact Ghost Ranch directly)
                                </span>
                                <span class="form-product-details">
                                </span>
                            </span>
                            <div class="form-product-description" id="product-name-description-input_9_1006">
                                For more information on lodging accomodations visit the ghost ranch website. https://www.ghostranch.org/visit/lodging/
                            </div>
                            </label>
                            <table id="input_9_1006_subproducts" class="form-product-child-table">
                            <tbody>
                                <tr>
                                <th style="text-align:left">
                                    <span class="form-sub-label">
                                    Room Type
                                    </span>
                                </th>
                                <th style="text-align:left">
                                    <span class="form-product-options-text form-sub-label">
                                    Quantity
                                    </span>
                                </th>
                                <th style="text-align:right">
                                    <span class="form-sub-label">
                                    Price
                                    </span>
                                </th>
                                </tr>
                                <tr>
                                <th style="text-align:left">
                                    <span class="form-product-child-label" style="font-size:0.786em">
                                    RV Site Full Hook-Ups
                                    </span>
                                </th>
                                <td style="text-align:center" data-title="Quantity">
                                    <input type="text" size="3" value="0" class="form-textbox form-subproduct-quantity form-subproduct-option form-product-custom_quantity" name="q9_paymentDetails[special_1006_0][item_0]" id="input_9_quantity_1006_0_0" />
                                </td>
                                <td style="text-align:left">
                                    <span class="form-product-child-price form-product-child-label">
                                    <span data-wrapper-react="true">
                                        $
                                        <span id="input_9_1006_0_price">
                                        270.00
                                        </span>
                                    </span>
                                    </span>
                                </td>
                                <td>
                                    <input type="hidden" value="RV Site Full Hook-Ups" name="q9_paymentDetails[special_1006_0][item_1]" />
                                    <input type="checkbox" checked="" id="input_9_1006_0" style="display:none" name="q9_paymentDetails[][id]" value="1006_0" />
                                </td>
                                </tr>
                                <tr>
                                <th style="text-align:left">
                                    <span class="form-product-child-label" style="font-size:0.786em">
                                    Tent/RV Site- Electric Only
                                    </span>
                                </th>
                                <td style="text-align:center" data-title="Quantity">
                                    <input type="text" size="3" value="0" class="form-textbox form-subproduct-quantity form-subproduct-option form-product-custom_quantity" name="q9_paymentDetails[special_1006_1][item_0]" id="input_9_quantity_1006_1_0" />
                                </td>
                                <td style="text-align:left">
                                    <span class="form-product-child-price form-product-child-label">
                                    <span data-wrapper-react="true">
                                        $
                                        <span id="input_9_1006_1_price">
                                        240.00
                                        </span>
                                    </span>
                                    </span>
                                </td>
                                <td>
                                    <input type="hidden" value="Tent/RV Site- Electric Only" name="q9_paymentDetails[special_1006_1][item_1]" />
                                    <input type="checkbox" checked="" id="input_9_1006_1" style="display:none" name="q9_paymentDetails[][id]" value="1006_1" />
                                </td>
                                </tr>
                                <tr>
                                <th style="text-align:left">
                                    <span class="form-product-child-label" style="font-size:0.786em">
                                    Tent Site- Non-Electric
                                    </span>
                                </th>
                                <td style="text-align:center" data-title="Quantity">
                                    <input type="text" size="3" value="0" class="form-textbox form-subproduct-quantity form-subproduct-option form-product-custom_quantity" name="q9_paymentDetails[special_1006_2][item_0]" id="input_9_quantity_1006_2_0" />
                                </td>
                                <td style="text-align:left">
                                    <span class="form-product-child-price form-product-child-label">
                                    <span data-wrapper-react="true">
                                        $
                                        <span id="input_9_1006_2_price">
                                        210.00
                                        </span>
                                    </span>
                                    </span>
                                </td>
                                <td>
                                    <input type="hidden" value="Tent Site- Non-Electric" name="q9_paymentDetails[special_1006_2][item_1]" />
                                    <input type="checkbox" checked="" id="input_9_1006_2" style="display:none" name="q9_paymentDetails[][id]" value="1006_2" />
                                </td>
                                </tr>
                                <tr>
                                <th style="text-align:left">
                                    <span class="form-product-child-label" style="font-size:0.786em">
                                    Semi-Private Room
                                    </span>
                                </th>
                                <td style="text-align:center" data-title="Quantity">
                                    <input type="text" size="3" value="0" class="form-textbox form-subproduct-quantity form-subproduct-option form-product-custom_quantity" name="q9_paymentDetails[special_1006_3][item_0]" id="input_9_quantity_1006_3_0" />
                                </td>
                                <td style="text-align:left">
                                    <span class="form-product-child-price form-product-child-label">
                                    <span data-wrapper-react="true">
                                        $
                                        <span id="input_9_1006_3_price">
                                        840.00
                                        </span>
                                    </span>
                                    </span>
                                </td>
                                <td>
                                    <input type="hidden" value="Semi-Private Room" name="q9_paymentDetails[special_1006_3][item_1]" />
                                    <input type="checkbox" checked="" id="input_9_1006_3" style="display:none" name="q9_paymentDetails[][id]" value="1006_3" />
                                </td>
                                </tr>
                                <tr>
                                <th style="text-align:left">
                                    <span class="form-product-child-label" style="font-size:0.786em">
                                    Dorm/Communal
                                    </span>
                                </th>
                                <td style="text-align:center" data-title="Quantity">
                                    <input type="text" size="3" value="0" class="form-textbox form-subproduct-quantity form-subproduct-option form-product-custom_quantity" name="q9_paymentDetails[special_1006_4][item_0]" id="input_9_quantity_1006_4_0" />
                                </td>
                                <td style="text-align:left">
                                    <span class="form-product-child-price form-product-child-label">
                                    <span data-wrapper-react="true">
                                        $
                                        <span id="input_9_1006_4_price">
                                        540.00
                                        </span>
                                    </span>
                                    </span>
                                </td>
                                <td>
                                    <input type="hidden" value="Dorm/Communal" name="q9_paymentDetails[special_1006_4][item_1]" />
                                    <input type="checkbox" checked="" id="input_9_1006_4" style="display:none" name="q9_paymentDetails[][id]" value="1006_4" />
                                </td>
                                </tr>
                            </tbody>
                            </table>
                            <br/>
                            <span class="form-special-subtotal">
                            <span class="form-item-subtotal">
                                Item subtotal:
                            </span>
                            <span data-wrapper-react="true">
                                $
                                <span id="input_9_1006_item_subtotal">
                                0.00
                                </span>
                            </span>
                            </span>
                        </div>
                        </span>
                        <br/>
                        <span class="form-product-item hover-product-item " categories="non-categorized" pid="1007">
                        <div data-wrapper-react="true" class="form-product-item-detail">
                            <input type="checkbox" class="form-checkbox form-product-has-subproducts form-product-input" id="input_9_1007" name="q9_paymentDetails[][id]" value="1007_expanded" checked="" />
                            <label for="input_9_1007" class="form-product-container">
                            <span data-wrapper-react="true">
                                <span class="form-product-name" id="product-name-input_9_1007">
                                Meals (Recommended)
                                </span>
                                <span class="form-product-details">
                                </span>
                            </span>
                            </label>
                            <table id="input_9_1007_subproducts" class="form-product-child-table">
                            <tbody>
                                <tr>
                                <th style="text-align:left">
                                    <span class="form-sub-label">
                                    Meal Type
                                    </span>
                                </th>
                                <th style="text-align:left">
                                    <span class="form-product-options-text form-sub-label">
                                    Quantity
                                    </span>
                                </th>
                                <th style="text-align:right">
                                    <span class="form-sub-label">
                                    Price
                                    </span>
                                </th>
                                </tr>
                                <tr>
                                <th style="text-align:left">
                                    <span class="form-product-child-label" style="font-size:0.786em">
                                    Adult
                                    </span>
                                </th>
                                <td style="text-align:center" data-title="Quantity">
                                    <input type="text" size="3" value="0" class="form-textbox form-subproduct-quantity form-subproduct-option form-product-custom_quantity" name="q9_paymentDetails[special_1007_0][item_0]" id="input_9_quantity_1007_0_0" />
                                </td>
                                <td style="text-align:left">
                                    <span class="form-product-child-price form-product-child-label">
                                    <span data-wrapper-react="true">
                                        $
                                        <span id="input_9_1007_0_price">
                                        204.00
                                        </span>
                                    </span>
                                    </span>
                                </td>
                                <td>
                                    <input type="hidden" value="Adult" name="q9_paymentDetails[special_1007_0][item_1]" />
                                    <input type="checkbox" checked="" id="input_9_1007_0" style="display:none" name="q9_paymentDetails[][id]" value="1007_0" />
                                </td>
                                </tr>
                                <tr>
                                <th style="text-align:left">
                                    <span class="form-product-child-label" style="font-size:0.786em">
                                    Youth (12 and Under)
                                    </span>
                                </th>
                                <td style="text-align:center" data-title="Quantity">
                                    <input type="text" size="3" value="0" class="form-textbox form-subproduct-quantity form-subproduct-option form-product-custom_quantity" name="q9_paymentDetails[special_1007_1][item_0]" id="input_9_quantity_1007_1_0" />
                                </td>
                                <td style="text-align:left">
                                    <span class="form-product-child-price form-product-child-label">
                                    <span data-wrapper-react="true">
                                        $
                                        <span id="input_9_1007_1_price">
                                        102.00
                                        </span>
                                    </span>
                                    </span>
                                </td>
                                <td>
                                    <input type="hidden" value="Youth (12 and Under)" name="q9_paymentDetails[special_1007_1][item_1]" />
                                    <input type="checkbox" checked="" id="input_9_1007_1" style="display:none" name="q9_paymentDetails[][id]" value="1007_1" />
                                </td>
                                </tr>
                            </tbody>
                            </table>
                            <br/>
                            <span class="form-special-subtotal">
                            <span class="form-item-subtotal">
                                Item subtotal:
                            </span>
                            <span data-wrapper-react="true">
                                $
                                <span id="input_9_1007_item_subtotal">
                                0.00
                                </span>
                            </span>
                            </span>
                        </div>
                        </span>
                        <br/>
                        <span class="form-product-item hover-product-item " categories="non-categorized" pid="1008">
                        <div data-wrapper-react="true" class="form-product-item-detail">
                            <input type="checkbox" class="form-checkbox form-product-has-subproducts form-product-input" id="input_9_1008" name="q9_paymentDetails[][id]" value="1008_expanded" checked="" disabled="" />
                            <label for="input_9_1008" class="form-product-container">
                            <span data-wrapper-react="true">
                                <span class="form-product-name" id="product-name-input_9_1008">
                                WUULF Registration (Required)
                                </span>
                                <span class="form-product-details">
                                </span>
                            </span>
                            <div class="form-product-description" id="product-name-description-input_9_1008">
                                Because of administrative costs to process credit cards we&#x27;ve had to increase registration prices slightly. If you are able to pay by check, we will happily reimburse you the difference in cost ($20 per adult)
                            </div>
                            </label>
                            <table id="input_9_1008_subproducts" class="form-product-child-table">
                            <tbody>
                                <tr>
                                <th style="text-align:left">
                                    <span class="form-sub-label">
                                    Registration Type
                                    </span>
                                </th>
                                <th style="text-align:left">
                                    <span class="form-product-options-text form-sub-label">
                                    Quantity
                                    </span>
                                </th>
                                <th style="text-align:right">
                                    <span class="form-sub-label">
                                    Price
                                    </span>
                                </th>
                                </tr>
                                <tr>
                                <th style="text-align:left">
                                    <span class="form-product-child-label" style="font-size:0.786em">
                                    Adult
                                    </span>
                                </th>
                                <td style="text-align:center" data-title="Quantity">
                                    <input type="text" size="3" value="0" class="form-textbox form-subproduct-quantity form-subproduct-option form-product-custom_quantity" name="q9_paymentDetails[special_1008_0][item_0]" id="input_9_quantity_1008_0_0" />
                                </td>
                                <td style="text-align:left">
                                    <span class="form-product-child-price form-product-child-label">
                                    <span data-wrapper-react="true">
                                        $
                                        <span id="input_9_1008_0_price">
                                        260.00
                                        </span>
                                    </span>
                                    </span>
                                </td>
                                <td>
                                    <input type="hidden" value="Adult" name="q9_paymentDetails[special_1008_0][item_1]" />
                                    <input type="checkbox" checked="" id="input_9_1008_0" style="display:none" name="q9_paymentDetails[][id]" value="1008_0" />
                                </td>
                                </tr>
                                <tr>
                                <th style="text-align:left">
                                    <span class="form-product-child-label" style="font-size:0.786em">
                                    Young Adult (High School Grad - Age 24)
                                    </span>
                                </th>
                                <td style="text-align:center" data-title="Quantity">
                                    <input type="text" size="3" value="0" class="form-textbox form-subproduct-quantity form-subproduct-option form-product-custom_quantity" name="q9_paymentDetails[special_1008_1][item_0]" id="input_9_quantity_1008_1_0" />
                                </td>
                                <td style="text-align:left">
                                    <span class="form-product-child-price form-product-child-label">
                                    <span data-wrapper-react="true">
                                        $
                                        <span id="input_9_1008_1_price">
                                        175.00
                                        </span>
                                    </span>
                                    </span>
                                </td>
                                <td>
                                    <input type="hidden" value="Young Adult (High School Grad - Age 24)" name="q9_paymentDetails[special_1008_1][item_1]" />
                                    <input type="checkbox" checked="" id="input_9_1008_1" style="display:none" name="q9_paymentDetails[][id]" value="1008_1" />
                                </td>
                                </tr>
                                <tr>
                                <th style="text-align:left">
                                    <span class="form-product-child-label" style="font-size:0.786em">
                                    Youth (Kindergarten-12th Grade)
                                    </span>
                                </th>
                                <td style="text-align:center" data-title="Quantity">
                                    <input type="text" size="3" value="0" class="form-textbox form-subproduct-quantity form-subproduct-option form-product-custom_quantity" name="q9_paymentDetails[special_1008_2][item_0]" id="input_9_quantity_1008_2_0" />
                                </td>
                                <td style="text-align:left">
                                    <span class="form-product-child-price form-product-child-label">
                                    <span data-wrapper-react="true">
                                        $
                                        <span id="input_9_1008_2_price">
                                        125.00
                                        </span>
                                    </span>
                                    </span>
                                </td>
                                <td>
                                    <input type="hidden" value="Youth (Kindergarten-12th Grade)" name="q9_paymentDetails[special_1008_2][item_1]" />
                                    <input type="checkbox" checked="" id="input_9_1008_2" style="display:none" name="q9_paymentDetails[][id]" value="1008_2" />
                                </td>
                                </tr>
                                <tr>
                                <th style="text-align:left">
                                    <span class="form-product-child-label" style="font-size:0.786em">
                                    Young Child (0-5) *Sadly, we cannot offer childcare for children under Kindergarten Age
                                    </span>
                                </th>
                                <td style="text-align:center" data-title="Quantity">
                                    <input type="text" size="3" value="0" class="form-textbox form-subproduct-quantity form-subproduct-option form-product-custom_quantity" name="q9_paymentDetails[special_1008_3][item_0]" id="input_9_quantity_1008_3_0" />
                                </td>
                                <td style="text-align:left">
                                    <span class="form-product-child-price form-product-child-label">
                                    <span data-wrapper-react="true">
                                        $
                                        <span id="input_9_1008_3_price">
                                        0.00
                                        </span>
                                    </span>
                                    </span>
                                </td>
                                <td>
                                    <input type="hidden" value="Young Child (0-5) *Sadly, we cannot offer childcare for children under Kindergarten Age" name="q9_paymentDetails[special_1008_3][item_1]" />
                                    <input type="checkbox" checked="" id="input_9_1008_3" style="display:none" name="q9_paymentDetails[][id]" value="1008_3" />
                                </td>
                                </tr>
                            </tbody>
                            </table>
                            <br/>
                            <span class="form-special-subtotal">
                            <span class="form-item-subtotal">
                                Item subtotal:
                            </span>
                            <span data-wrapper-react="true">
                                $
                                <span id="input_9_1008_item_subtotal">
                                0.00
                                </span>
                            </span>
                            </span>
                        </div>
                        </span>
                        <br/>
                        <span class="form-product-item hover-product-item " categories="non-categorized" pid="1009">
                        <div data-wrapper-react="true" class="form-product-item-detail">
                            <input type="checkbox" class="form-checkbox form-product-has-subproducts form-product-input" id="input_9_1009" name="q9_paymentDetails[][id]" value="1009_expanded" checked="" />
                            <label for="input_9_1009" class="form-product-container">
                            <span data-wrapper-react="true">
                                <span class="form-product-name" id="product-name-input_9_1009">
                                Ghost Ranch and Beyond As Seen In The 2020 Catalog (Optional)
                                </span>
                                <span class="form-product-details">
                                </span>
                            </span>
                            <div class="form-product-description" id="product-name-description-input_9_1009">
                            </div>
                            </label>
                            <table id="input_9_1009_subproducts" class="form-product-child-table">
                            <tbody>
                                <tr>
                                <th style="text-align:left">
                                    <span class="form-sub-label">
                                    Activity
                                    </span>
                                </th>
                                <th style="text-align:left">
                                    <span class="form-product-options-text form-sub-label">
                                    Quantity
                                    </span>
                                </th>
                                <th style="text-align:right">
                                    <span class="form-sub-label">
                                    Price
                                    </span>
                                </th>
                                </tr>
                                <tr>
                                <th style="text-align:left">
                                    <span class="form-product-child-label" style="font-size:0.786em">
                                    Adult Rafting (12 and Up)
                                    </span>
                                </th>
                                <td style="text-align:center" data-title="Quantity">
                                    <input type="text" size="3" value="0" class="form-textbox form-subproduct-quantity form-subproduct-option form-product-custom_quantity" name="q9_paymentDetails[special_1009_0][item_0]" id="input_9_quantity_1009_0_0" />
                                </td>
                                <td style="text-align:left">
                                    <span class="form-product-child-price form-product-child-label">
                                    <span data-wrapper-react="true">
                                        $
                                        <span id="input_9_1009_0_price">
                                        105.00
                                        </span>
                                    </span>
                                    </span>
                                </td>
                                <td>
                                    <input type="hidden" value="Adult Rafting (12 and Up)" name="q9_paymentDetails[special_1009_0][item_1]" />
                                    <input type="checkbox" checked="" id="input_9_1009_0" style="display:none" name="q9_paymentDetails[][id]" value="1009_0" />
                                </td>
                                </tr>
                                <tr>
                                <th style="text-align:left">
                                    <span class="form-product-child-label" style="font-size:0.786em">
                                    Youth Rafting (6-11)
                                    </span>
                                </th>
                                <td style="text-align:center" data-title="Quantity">
                                    <input type="text" size="3" value="0" class="form-textbox form-subproduct-quantity form-subproduct-option form-product-custom_quantity" name="q9_paymentDetails[special_1009_1][item_0]" id="input_9_quantity_1009_1_0" />
                                </td>
                                <td style="text-align:left">
                                    <span class="form-product-child-price form-product-child-label">
                                    <span data-wrapper-react="true">
                                        $
                                        <span id="input_9_1009_1_price">
                                        100.00
                                        </span>
                                    </span>
                                    </span>
                                </td>
                                <td>
                                    <input type="hidden" value="Youth Rafting (6-11)" name="q9_paymentDetails[special_1009_1][item_1]" />
                                    <input type="checkbox" checked="" id="input_9_1009_1" style="display:none" name="q9_paymentDetails[][id]" value="1009_1" />
                                </td>
                                </tr>
                                <tr>
                                <th style="text-align:left">
                                    <span class="form-product-child-label" style="font-size:0.786em">
                                    Georgia O&#x27;Keefe Home Tour
                                    </span>
                                </th>
                                <td style="text-align:center" data-title="Quantity">
                                    <input type="text" size="3" value="0" class="form-textbox form-subproduct-quantity form-subproduct-option form-product-custom_quantity" name="q9_paymentDetails[special_1009_2][item_0]" id="input_9_quantity_1009_2_0" />
                                </td>
                                <td style="text-align:left">
                                    <span class="form-product-child-price form-product-child-label">
                                    <span data-wrapper-react="true">
                                        $
                                        <span id="input_9_1009_2_price">
                                        45.00
                                        </span>
                                    </span>
                                    </span>
                                </td>
                                <td>
                                    <input type="hidden" value="Georgia O&#x27;Keefe Home Tour" name="q9_paymentDetails[special_1009_2][item_1]" />
                                    <input type="checkbox" checked="" id="input_9_1009_2" style="display:none" name="q9_paymentDetails[][id]" value="1009_2" />
                                </td>
                                </tr>
                                <tr>
                                <th style="text-align:left">
                                    <span class="form-product-child-label" style="font-size:0.786em">
                                    Earth Ship Community Tour
                                    </span>
                                </th>
                                <td style="text-align:center" data-title="Quantity">
                                    <input type="text" size="3" value="0" class="form-textbox form-subproduct-quantity form-subproduct-option form-product-custom_quantity" name="q9_paymentDetails[special_1009_3][item_0]" id="input_9_quantity_1009_3_0" />
                                </td>
                                <td style="text-align:left">
                                    <span class="form-product-child-price form-product-child-label">
                                    <span data-wrapper-react="true">
                                        $
                                        <span id="input_9_1009_3_price">
                                        17.00
                                        </span>
                                    </span>
                                    </span>
                                </td>
                                <td>
                                    <input type="hidden" value="Earth Ship Community Tour" name="q9_paymentDetails[special_1009_3][item_1]" />
                                    <input type="checkbox" checked="" id="input_9_1009_3" style="display:none" name="q9_paymentDetails[][id]" value="1009_3" />
                                </td>
                                </tr>
                                <tr>
                                <th style="text-align:left">
                                    <span class="form-product-child-label" style="font-size:0.786em">
                                    Ghost Ranch Archaeology Tour
                                    </span>
                                </th>
                                <td style="text-align:center" data-title="Quantity">
                                    <input type="text" size="3" value="0" class="form-textbox form-subproduct-quantity form-subproduct-option form-product-custom_quantity" name="q9_paymentDetails[special_1009_4][item_0]" id="input_9_quantity_1009_4_0" />
                                </td>
                                <td style="text-align:left">
                                    <span class="form-product-child-price form-product-child-label">
                                    <span data-wrapper-react="true">
                                        $
                                        <span id="input_9_1009_4_price">
                                        49.00
                                        </span>
                                    </span>
                                    </span>
                                </td>
                                <td>
                                    <input type="hidden" value="Ghost Ranch Archaeology Tour" name="q9_paymentDetails[special_1009_4][item_1]" />
                                    <input type="checkbox" checked="" id="input_9_1009_4" style="display:none" name="q9_paymentDetails[][id]" value="1009_4" />
                                </td>
                                </tr>
                                <tr>
                                <th style="text-align:left">
                                    <span class="form-product-child-label" style="font-size:0.786em">
                                    O&#x27;Keefe Landscape Tour
                                    </span>
                                </th>
                                <td style="text-align:center" data-title="Quantity">
                                    <input type="text" size="3" value="0" class="form-textbox form-subproduct-quantity form-subproduct-option form-product-custom_quantity" name="q9_paymentDetails[special_1009_5][item_0]" id="input_9_quantity_1009_5_0" />
                                </td>
                                <td style="text-align:left">
                                    <span class="form-product-child-price form-product-child-label">
                                    <span data-wrapper-react="true">
                                        $
                                        <span id="input_9_1009_5_price">
                                        39.00
                                        </span>
                                    </span>
                                    </span>
                                </td>
                                <td>
                                    <input type="hidden" value="O&#x27;Keefe Landscape Tour" name="q9_paymentDetails[special_1009_5][item_1]" />
                                    <input type="checkbox" checked="" id="input_9_1009_5" style="display:none" name="q9_paymentDetails[][id]" value="1009_5" />
                                </td>
                                </tr>
                                <tr>
                                <th style="text-align:left">
                                    <span class="form-product-child-label" style="font-size:0.786em">
                                    Adult Toltec Steam Train (13 and up)
                                    </span>
                                </th>
                                <td style="text-align:center" data-title="Quantity">
                                    <input type="text" size="3" value="0" class="form-textbox form-subproduct-quantity form-subproduct-option form-product-custom_quantity" name="q9_paymentDetails[special_1009_6][item_0]" id="input_9_quantity_1009_6_0" />
                                </td>
                                <td style="text-align:left">
                                    <span class="form-product-child-price form-product-child-label">
                                    <span data-wrapper-react="true">
                                        $
                                        <span id="input_9_1009_6_price">
                                        115.00
                                        </span>
                                    </span>
                                    </span>
                                </td>
                                <td>
                                    <input type="hidden" value="Adult Toltec Steam Train (13 and up)" name="q9_paymentDetails[special_1009_6][item_1]" />
                                    <input type="checkbox" checked="" id="input_9_1009_6" style="display:none" name="q9_paymentDetails[][id]" value="1009_6" />
                                </td>
                                </tr>
                                <tr>
                                <th style="text-align:left">
                                    <span class="form-product-child-label" style="font-size:0.786em">
                                    Children Toltec Steam Train (2-12)
                                    </span>
                                </th>
                                <td style="text-align:center" data-title="Quantity">
                                    <input type="text" size="3" value="0" class="form-textbox form-subproduct-quantity form-subproduct-option form-product-custom_quantity" name="q9_paymentDetails[special_1009_7][item_0]" id="input_9_quantity_1009_7_0" />
                                </td>
                                <td style="text-align:left">
                                    <span class="form-product-child-price form-product-child-label">
                                    <span data-wrapper-react="true">
                                        $
                                        <span id="input_9_1009_7_price">
                                        62.25
                                        </span>
                                    </span>
                                    </span>
                                </td>
                                <td>
                                    <input type="hidden" value="Children Toltec Steam Train (2-12)" name="q9_paymentDetails[special_1009_7][item_1]" />
                                    <input type="checkbox" checked="" id="input_9_1009_7" style="display:none" name="q9_paymentDetails[][id]" value="1009_7" />
                                </td>
                                </tr>
                                <tr>
                                <th style="text-align:left">
                                    <span class="form-product-child-label" style="font-size:0.786em">
                                    Ghost Ranch History Walk
                                    </span>
                                </th>
                                <td style="text-align:center" data-title="Quantity">
                                    <input type="text" size="3" value="0" class="form-textbox form-subproduct-quantity form-subproduct-option form-product-custom_quantity" name="q9_paymentDetails[special_1009_8][item_0]" id="input_9_quantity_1009_8_0" />
                                </td>
                                <td style="text-align:left">
                                    <span class="form-product-child-price form-product-child-label">
                                    <span data-wrapper-react="true">
                                        $
                                        <span id="input_9_1009_8_price">
                                        0.00
                                        </span>
                                    </span>
                                    </span>
                                </td>
                                <td>
                                    <input type="hidden" value="Ghost Ranch History Walk" name="q9_paymentDetails[special_1009_8][item_1]" />
                                    <input type="checkbox" checked="" id="input_9_1009_8" style="display:none" name="q9_paymentDetails[][id]" value="1009_8" />
                                </td>
                                </tr>
                            </tbody>
                            </table>
                            <br/>
                            <span class="form-special-subtotal">
                            <span class="form-item-subtotal">
                                Item subtotal:
                            </span>
                            <span data-wrapper-react="true">
                                $
                                <span id="input_9_1009_item_subtotal">
                                0.00
                                </span>
                            </span>
                            </span>
                        </div>
                        </span>
                        <br/>
                        <span class="form-product-item hover-product-item " categories="non-categorized" pid="1010">
                        <div data-wrapper-react="true" class="form-product-item-detail">
                            <input type="checkbox" class="form-checkbox form-product-has-subproducts form-product-input" id="input_9_1010" name="q9_paymentDetails[][id]" value="1010_expanded" checked="" />
                            <label for="input_9_1010" class="form-product-container">
                            <span data-wrapper-react="true">
                                <span class="form-product-name" id="product-name-input_9_1010">
                                Scholarship Fund/ Donation (Optional)
                                </span>
                                <span class="form-product-details">
                                </span>
                            </span>
                            <div class="form-product-description" id="product-name-description-input_9_1010">
                            </div>
                            </label>
                            <table id="input_9_1010_subproducts" class="form-product-child-table">
                            <tbody>
                                <tr>
                                <th style="text-align:left">
                                    <span class="form-sub-label">
                                    Activity
                                    </span>
                                </th>
                                <th style="text-align:left">
                                    <span class="form-product-options-text form-sub-label">
                                    Quantity
                                    </span>
                                </th>
                                <th style="text-align:right">
                                    <span class="form-sub-label">
                                    Price
                                    </span>
                                </th>
                                </tr>
                                <tr>
                                <th style="text-align:left">
                                    <span class="form-product-child-label" style="font-size:0.786em">
                                    1 Raffle Ticket
                                    </span>
                                </th>
                                <td style="text-align:center" data-title="Quantity">
                                    <input type="text" size="3" value="0" class="form-textbox form-subproduct-quantity form-subproduct-option form-product-custom_quantity" name="q9_paymentDetails[special_1010_0][item_0]" id="input_9_quantity_1010_0_0" />
                                </td>
                                <td style="text-align:left">
                                    <span class="form-product-child-price form-product-child-label">
                                    <span data-wrapper-react="true">
                                        $
                                        <span id="input_9_1010_0_price">
                                        2.00
                                        </span>
                                    </span>
                                    </span>
                                </td>
                                <td>
                                    <input type="hidden" value="1 Raffle Ticket" name="q9_paymentDetails[special_1010_0][item_1]" />
                                    <input type="checkbox" checked="" id="input_9_1010_0" style="display:none" name="q9_paymentDetails[][id]" value="1010_0" />
                                </td>
                                </tr>
                                <tr>
                                <th style="text-align:left">
                                    <span class="form-product-child-label" style="font-size:0.786em">
                                    3 Raffle Tickets (1 set of 3)
                                    </span>
                                </th>
                                <td style="text-align:center" data-title="Quantity">
                                    <input type="text" size="3" value="0" class="form-textbox form-subproduct-quantity form-subproduct-option form-product-custom_quantity" name="q9_paymentDetails[special_1010_1][item_0]" id="input_9_quantity_1010_1_0" />
                                </td>
                                <td style="text-align:left">
                                    <span class="form-product-child-price form-product-child-label">
                                    <span data-wrapper-react="true">
                                        $
                                        <span id="input_9_1010_1_price">
                                        5.00
                                        </span>
                                    </span>
                                    </span>
                                </td>
                                <td>
                                    <input type="hidden" value="3 Raffle Tickets (1 set of 3)" name="q9_paymentDetails[special_1010_1][item_1]" />
                                    <input type="checkbox" checked="" id="input_9_1010_1" style="display:none" name="q9_paymentDetails[][id]" value="1010_1" />
                                </td>
                                </tr>
                                <tr>
                                <th style="text-align:left">
                                    <span class="form-product-child-label" style="font-size:0.786em">
                                    Tax Deductible Donation
                                    </span>
                                </th>
                                <td style="text-align:center" data-title="Quantity">
                                    <input type="text" size="3" value="0" class="form-textbox form-subproduct-quantity form-subproduct-option form-product-custom_quantity" name="q9_paymentDetails[special_1010_2][item_0]" id="input_9_quantity_1010_2_0" />
                                </td>
                                <td style="text-align:left">
                                    <span class="form-product-child-price form-product-child-label">
                                    <span data-wrapper-react="true">
                                        $
                                        <span id="input_9_1010_2_price">
                                        1.00
                                        </span>
                                    </span>
                                    </span>
                                </td>
                                <td>
                                    <input type="hidden" value="Tax Deductible Donation" name="q9_paymentDetails[special_1010_2][item_1]" />
                                    <input type="checkbox" checked="" id="input_9_1010_2" style="display:none" name="q9_paymentDetails[][id]" value="1010_2" />
                                </td>
                                </tr>
                            </tbody>
                            </table>
                            <br/>
                            <span class="form-special-subtotal">
                            <span class="form-item-subtotal">
                                Item subtotal:
                            </span>
                            <span data-wrapper-react="true">
                                $
                                <span id="input_9_1010_item_subtotal">
                                0.00
                                </span>
                            </span>
                            </span>
                        </div>
                        </span>
                        <br/>
                        <div id="coupon-container" style="border:1px solid lightgray;padding:5px;border-radius:6px;width:200px;margin-top:8px">
                        <table id="coupon-table">
                            <tr>
                            <th colSpan="2" style="text-align:left">
                                <label id="coupon-header" for="coupon-input"> Enter coupon </label>
                            </th>
                            </tr>
                            <tr>
                            <td>
                                <input type="text" name="coupon-input" id="coupon-input" data-stripe="false" size="15" autoComplete="off" aria-labelledby="coupon-header coupon-message" />
                            </td>
                            <td width="40%" style="text-align:center">
                                <img src="https://cdn.jotfor.ms//images/ajax-loader.gif" alt="coupon loading" id="coupon-loader" style="display:none;vertical-align:top" />
                                <button type="button" id="coupon-button" data-qid="input_9" value="">
                                Apply
                                </button>
                            </td>
                            </tr>
                            <tr>
                            <th colSpan="2" style="text-align:left">
                                <span id="coupon-message" role="alert">
                                </span>
                            </th>
                            </tr>
                        </table>
                        </div>
                        <br/>
                        <input type="hidden" id="input_9_coupon" name="coupon" />
                        <span class="form-payment-total">
                        <b>
                            <span id="total-text">
                            Total
                            </span>
                            
                            <span class="form-payment-price">
                            <span data-wrapper-react="true">
                                $
                                <span id="payment_total">
                                0.00
                                </span>
                            </span>
                            </span>
                        </b>
                        </span>
                    </div>
                    <hr/>
                    </div>
                    <div id="stripe-templates">
                    <div class="stripe-sca-template">
                        <div>
                        <table class="payment-up-form-table" style="border:0;margin-bottom:10px" cellPadding="0" cellSpacing="0">
                            <tbody>
                            <tr>
                                <td width="50%">
                                </td>
                            </tr>
                            </tbody>
                        </table>
                        <table class="form-address-table payment-form-table" style="border:0" cellPadding="0" cellSpacing="0">
                            <tbody>
                            <tr>
                                <th colSpan="2" style="text-align:left" id="ccTitle9">
                                Credit Card Details
                                </th>
                            </tr>
                            <tr>
                                <td width="50%">
                                <span class="form-sub-label-container" style="vertical-align:top">
                                    <input type="text" id="input_9_cc_firstName" name="q9_paymentDetails[cc_firstName]" class="form-textbox cc_firstName" data-defaultvalue="" size="20" value="" data-component="cc_firstName" />
                                    <label class="form-sub-label" for="input_9_cc_firstName" id="sublabel_cc_firstName" style="min-height:13px;margin:0 0 3px 0" aria-hidden="false"> First Name </label>
                                </span>
                                </td>
                                <td width="50%">
                                <span class="form-sub-label-container" style="vertical-align:top">
                                    <input type="text" id="input_9_cc_lastName" name="q9_paymentDetails[cc_lastName]" class="form-textbox cc_lastName" data-defaultvalue="" size="20" value="" data-component="cc_lastName" />
                                    <label class="form-sub-label" for="input_9_cc_lastName" id="sublabel_cc_lastName" style="min-height:13px;margin:0 0 3px 0" aria-hidden="false"> Last Name </label>
                                </span>
                                </td>
                            </tr>
                            <tr class="if_cc_field">
                                <td width="50%">
                                <span class="form-sub-label-container" style="vertical-align:top">
                                    <div class="form-textbox cc_numberMount ">
                                    </div>
                                    <label class="form-sub-label" for="input_9_cc_number" id="sublabel_cc_number" style="min-height:13px;margin:0 0 3px 0" aria-hidden="false"> Credit Card Number </label>
                                </span>
                                </td>
                                <td width="50%">
                                <span class="form-sub-label-container" style="vertical-align:top">
                                    <div class="form-textbox cc_ccvMount ">
                                    </div>
                                    <label class="form-sub-label" for="input_9_cc_ccv" id="sublabel_cc_ccv" style="min-height:13px;margin:0 0 3px 0" aria-hidden="false"> Security Code </label>
                                </span>
                                </td>
                            </tr>
                            <tr>
                                <td width="50%">
                                <span class="form-sub-label-container" style="vertical-align:top">
                                    <div class="form-textbox cc_cardExpiryMount ">
                                    </div>
                                    <label class="form-sub-label" for="input_9_cc_card_expiry" id="sublabel_cc_card_expiry" style="min-height:13px;margin:0 0 3px 0" aria-hidden="false"> Card Expiration </label>
                                </span>
                                </td>
                                <td width="50%">
                                <tr style="display:none">
                                    <td>
                                    <input id="stripesca_dummy" style="display:none" />
                                    </td>
                                </tr>
                                </td>
                            </tr>
                            </tbody>
                        </table>
                        </div>
                    </div>
                    </div>
                </div>
                </div>
            </li>
            <li class="form-line" data-type="control_textarea" id="id_17">
                <label class="form-label form-label-left form-label-auto" id="label_17" for="input_17"> Special Requests or Comments (Request a Specific Roommate, etc.) </label>
                <div id="cid_17" class="form-input">
                <textarea id="input_17" class="form-textarea" name="q17_specialRequests17" cols="40" rows="6" data-component="textarea" aria-labelledby="label_17"></textarea>
                </div>
            </li>
            <li class="form-line" data-type="control_button" id="id_21">
                <div id="cid_21" class="form-input-wide">
                <div style="margin-left:156px" data-align="auto" class="form-buttons-wrapper form-buttons-auto   jsTest-button-wrapperField">
                    <button id="input_21" type="submit" class="form-submit-button form-submit-button-simple_black submit-button jf-form-buttons jsTest-submitField" data-component="button" data-content="">
                    Submit
                    </button>
                </div>
                </div>
            </li>
            <li style="display:none">
                Should be Empty:
                <input type="text" name="website" value="" />
            </li>
            </ul>
        </div>
        <script>
        JotForm.showJotFormPowered = "new_footer";
        </script>
        <script>
        JotForm.poweredByText = "Powered by Jotform";
        </script>
        <input type="hidden" class="simple_spc" id="simple_spc" name="simple_spc" value="220645832594158" />
        <script type="text/javascript">
        var all_spc = document.querySelectorAll("form[id='220645832594158'] .si" + "mple" + "_spc");
        for (var i = 0; i < all_spc.length; i++)
        {
        all_spc[i].value = "220645832594158-220645832594158";
        }
        </script>
        <div class="formFooter-heightMask">
        </div>
        <div class="formFooter f6 branding21">
            <div class="formFooter-wrapper formFooter-leftSide">
            <a href="https://www.jotform.com/?utm_source=formfooter&utm_medium=banner&utm_term=220645832594158&utm_content=jotform_logo&utm_campaign=powered_by_jotform_le" target="_blank" class="formFooter-logoLink"><img class="formFooter-logo" src="https://cdn.jotfor.ms/assets/img/logo2021/jotform-logo-white.svg" alt="Jotform Logo" style="height: 44px;"></a>
            </div>
            <div class="formFooter-wrapper formFooter-rightSide">
            <span class="formFooter-text">
                Now create your own Jotform - It's free!
            </span>
            <a class="formFooter-button" href="https://www.jotform.com/?utm_source=formfooter&utm_medium=banner&utm_term=220645832594158&utm_content=jotform_button&utm_campaign=powered_by_jotform_le" target="_blank">Create your own Jotform</a>
            </div>
        </div>
        </form>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss" scoped>

</style>