
<!DOCTYPE html>
<html lang="en">



<head>

<script src="/shared/jquery.min.js"></script>

    <script>
    function set_validator_errors(){
        orderValidator.errorTitle = 'Please correct the following errors'; 

        orderValidator.errorNameField = 'Your Name'; 
        orderValidator.errorNameMess = 'Enter your name'; 
        
        orderValidator.errorPhoneField = 'Your phone'; 
        orderValidator.errorPhoneMess = 'Enter the correct phone number'; 
        
        orderValidator.errorAddress = 'Enter the correct address'; 
        orderValidator.errorRequired = 'required field'; 
        orderValidator.errorMaxLength = 'valid maximum {1} character'; 
        orderValidator.errorMinLength = 'valid minimum {1} character'; 
        orderValidator.errorEmailField = 'E-mail';
        orderValidator.errorEmail = 'Invalid email specified';
        }
    </script>
    
<script>


window.app = {
    timestamp: parseInt((new Date()).getTime() / 1000),
    jq: jQuery,
    formAction: window.location.href,
    leadToken: '5f7b792c703988.54000100',
    offers: {"18739":{"country":{"name":"\u0411\u0430\u043d\u0433\u043b\u0430\u0434\u0435\u0448","code":"BD"},"delivery_price":"","discount":"","currency":{"name":"\u09ac\u09be\u0982\u09b2\u09be\u09a6\u09c7\u09b6\u09bf \u099f\u09be\u0995\u09be","code":"BDT"},"price2":"5998","id":18739,"link":"","prepaid_info_html":"","product_sku":"","price":"2999"}},
    currentOffer: {"country":{"name":"\u0411\u0430\u043d\u0433\u043b\u0430\u0434\u0435\u0448","code":"BD"},"delivery_price":"","discount":"","currency":{"name":"\u09ac\u09be\u0982\u09b2\u09be\u09a6\u09c7\u09b6\u09bf \u099f\u09be\u0995\u09be","code":"BDT"},"price2":"5998","id":18739,"link":"","prepaid_info_html":"","product_sku":"","price":"2999"},
    allowedCountries: ["BD"],
    _setOfferId: false,
    
    setOffer: function (offerId) {
        if (offerId == this._setOfferId) {
            return ;
        }
        this._setOfferId = offerId;
        if (offerId) {
            var offer = app.offers[offerId];
            var previousOffer = app.currentOffer;
            app.currentOffer = offer;
            var event = this.jq.Event("offerchange");
            event.previousOffer = previousOffer;
            event.currentOffer = app.currentOffer;
            this.jq(document).trigger(event);
            this.updatePage(offer);
        } else {
            $('input[name=country]').val('');
        }
    },
    
    updatePage: function(offer) {
        $('x-newprice').html(offer.price);
        $('x-oldprice').html(offer.price2);
        $('x-currency').html(offer.currency.name);
        $('input[name=offer], select[name=offer]').val(offer.id);
        $('input[name=country]').val(offer.country.code);
    },

    blockForm: function() {
        // Блокируем кнопки при отправке формы
        $('input[type=submit]', $(this)).prop( 'disabled', true ).attr( 'disabled', true );
        $('button', $(this)).prop( 'disabled', true ).attr( 'disabled', true );
        app.incompleteOrder.lock = true;
        clearTimeout(app.incompleteOrder.timer);
    },

    unblockForm: function() {
        $('input[type=submit]', $(this)).prop( 'disabled', false ).attr( 'disabled', false );
        $('button[type=submit]', $(this)).prop( 'disabled', false ).attr( 'disabled', false );
        app.incompleteOrder.lock = false;
        clearTimeout(app.incompleteOrder.timer);
    }

};


</script><script src="/shared/form.validate.js?10"></script>
<script src="/shared/form.incomplete.js?10"></script>
<script src="/shared/main2.js?14"></script>



    <meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
    <title>Filorga Meso-Mask</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="css/styles.css" type="text/css" media="screen">

    <link rel="shortcut icon" href="favicon.png" type="image/png">
   
</head>

<body id="layout-body" class="layout-body m1modal-show">
    <svg version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink"
        x="0px" y="0px" width="0" height="0" xml:space="preserve" display="none">
        <defs>
            <symbol id="order-ic" viewBox="0 0 82 75">
                <image x="0px" y="0px" width="82px" height="75px"
                    xlink:href="data:img/png;base64,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">
                </image>
            </symbol>
            <symbol id="call-ic" viewBox="0 0 69 73">
                <image x="0px" y="0px" width="69px" height="73px"
                    xlink:href="data:img/png;base64,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">
                </image>
            </symbol>
            <symbol id="box-ic" viewBox="0 0 82 83">
                <image x="0px" y="0px" width="82px" height="83px"
                    xlink:href="data:img/png;base64,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">
                </image>
            </symbol>
            <symbol id="hand-ic" viewBox="0 0 68 92">
                <image x="0px" y="0px" width="68px" height="92px"
                    xlink:href="data:img/png;base64,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">
                </image>
            </symbol>
            <symbol id="select-arrow-ic" viewBox="0 0 21.5 14.5">
                <path fill-rule="evenodd" stroke-width="1px" stroke-linecap="butt" stroke-linejoin="miter"
                    d="M1.610,12.747 C2.053,12.747 6.010,8.363 10.079,8.363 C14.494,8.363 19.041,12.747 19.373,12.747 C20.199,12.747 20.813,12.153 20.330,11.565 C19.943,11.094 12.134,1.687 11.466,0.884 C11.028,0.356 9.981,0.366 9.542,0.884 C9.052,1.462 1.204,10.905 0.659,11.590 C0.259,12.091 0.700,12.747 1.610,12.747 Z">
                </path>
            </symbol>
        </defs>
    </svg>
    <section class="main-container">
        <header id="header" class="header">
            <div class="header-inner">
                <div class="wrapper">
                    <div class="header-nav">
                        <div class="header-nav__logo">
                            <a href="#header">Filorga Meso-Mask</a>
                        </div>
                        <ul class="header-nav__list js-mobileMenuList">
                            <li>
                                <a href="#reasons" class="js-scrollTo">Aging causes</a>
                            </li>
                            <li>
                                <a href="#how" class="js-scrollTo">How Filorga Meso-Mask works</a>
                            </li>
                            <li>
                                <a href="#usage" class="js-scrollTo">How to use</a>
                            </li>
                            <li>
                                <a href="#testimonials" class="js-scrollTo">Recommendations</a>
                            </li>
                            <li>
                                <a href="#questions" class="js-scrollTo">Question-answer</a>
                            </li>
                        </ul>
                        <div class="menu-button">
                            <span class="hamb"></span>
                        </div>
                    </div>
                </div>
            </div>
            <section class="header-section section-arrow">
                <div class="wrapper clearfix">
                    <div class="header-section__inner">
                        <div class="header-title">Young and healthy skin in a few days</div>
                        <div class="header-mabel">
                            <div class="header-mabel__content">
                                <div class="header-mabel__title">
                                    <span> Sales </span>
                                    <br> <span> Hit </span>
                                </div>
                                <div class="header-mabel__year">
                                    <script>
                                        document.write((new Date()).getFullYear());
                                    </script>
                                </div>
                                <div class="header-mabel__countries">In Europa<br>In the USA</div>
                            </div>
                        </div>
                        <ul class="header-list">
                            <li>
                                <span>• Without injections</span>
                            </li>
                            <li>
                                <span>• Without plastics</span>
                            </li>
                            <li>
                                <span>• Without expensive procedures</span>
                            </li>
                        </ul>
                        <div class="header-order">
                            <div class="TLorder">
                                <div class="head edge">
                                    <div class="head__discount"></div>
                                    <div class="price bb">
                                        <div class="price__old price__old-crossed">
                                            <span class="al-raw-cost-promo"><x-oldprice>5998</x-oldprice></span>
                                            <span class="al-raw-currency"><x-currency>বাংলাদেশি টাকা</x-currency> </span>
                                        </div>
                                        <div class="price__new">
                                            <span class="al-raw-cost"><x-newprice>2999</x-newprice></span>
                                            <span class="al-raw-currency"><x-currency>বাংলাদেশি টাকা</x-currency> </span>
                                        </div>
                                    </div>
                                    <h3 class="head__title">FILL IN THE FORM AND WE WILL CONTACT YOU</h3>
                                </div>

                                <form action="" method="post" class="al-form form">
                                            <input name="csrf_token" type="hidden" value="8a02c14ee024aba1b7a55c294a1ecf64:1601927468" />
    <select name="offer" class="form-control country_chang" style="display: none;">
        <option
                data-country-code="BD"
                selected="selected"
                value="18739"
        >
            Бангладеш        </option>
    </select>

      

                                    <div class="input-wrapper">
                                        <input type="text" name="name" class="form__input" placeholder="Name" id="name">
                                        <label for="name"></label>
                                    </div>
                                    <div class="input-wrapper">
                                        <input type="tel" name="phone" class="form__input" placeholder="Phone"
                                            id="phone">
                                        <label for="phone"></label>
                                    </div>
                                    <button type="submit" class="form__submit js-submit">ORDER&nbsp;<i
                                            class="arrow"></i>
                                    </button>
                                    <div class="icons-secure">
                                        <i class="norton"></i>
                                        <i class="mcAfee"></i>
                                    </div>
                                </form>
                            </div>
                        </div>
                    </div>
                </div>
            </section>
        </header>
        <div id="content" class="content">
            <section id="why" class="why-section section-common section-arrow">
                <div class="wrapper">
                    <div class="custom-title">
                        <span class="custom-title__inner">
                            Why <span class="bold">Filorga Meso-Mask?</span>
                        </span>
                    </div>
                    <div class="why-section__inner">
                        <div class="why-section__image text-center">
                            <!-- <img src="img/mabel_1.jpg"> -->
                            <img src="img/u/Edit-01.png" alt="">
                        </div>
                        <div class="why-section__text">
                            <p>We believe that your skin has every right to look dazzling.</p>
                            <p>We know that the skin of your face can exude health, be elastic, tender and velvety.</p>
                            <p>Your skin will be radiant, because for this we have created a unique serum that will
                                ensure saturation of your skin with vitamins and healthful moisture that will protect
                                your tender and sensitive skin from adverse external influences.</p>
                            <p>
                                <a href="#order-footer" class="red-link js-scrollTo">You will see the result after the
                                    first application.</a>
                            </p>
                        </div>
                    </div>
                </div>
            </section>
            <section id="reasons" class="reasons-section section-common section-arrow">
                <div class="wrapper">
                    <div class="custom-title">
                        <span class="custom-title__inner">
                            Causes of skin <span class="bold">aging</span>
                        </span>
                    </div>
                    <div class="reasons-section__inner">
                        <div class="reasons-section__image">
                            <img src="img/women_1.jpg">
                        </div>
                        <div class="reasons-section__text">
                            <div class="text-block">
                                <div class="text-block__title">Ultraviolet aging</div>
                                <div class="text-block__caption">Under the influence of sunlight, the structure of skin
                                    cells is destroyed, elasticity is lost, wrinkles appear.</div>
                            </div>
                            <div class="text-block">
                                <div class="text-block__title">Lack of moisture</div>
                                <div class="text-block__caption">Dehydration of the skin leads to peeling, a feeling of
                                    tightness, the appearance of grooves and wrinkles.</div>
                            </div>
                            <div class="text-block">
                                <div class="text-block__title">Intoxication</div>
                                <div class="text-block__caption">Connective tissues suffers from toxic overload,
                                    therefore the skin loses elasticity, loses its ability to withstand external
                                    effects.</div>
                            </div>
                            <div class="text-block">
                                <div class="text-block__title">Stress</div>
                                <div class="text-block__caption">The disorder of the nervous system leads to aging of
                                    the whole organism, which is reflected in the skin in the form of dryness, earthy
                                    color, various types of pigmentation.</div>
                            </div>
                        </div>
                    </div>
                </div>
            </section>
            <section id="how" class="how-section section-common section-arrow">
                <div class="wrapper">
                    <div class="custom-title">
                        <span class="custom-title__inner">
                            How does <span class="bold">Filorga Meso-Mask</span> work?
                        </span>
                    </div>
                    <div class="how-section__inner">
                        <div class="how-section__text">
                            <div class="text-block">
                                <div class="text-block__title">Retains moisture</div>
                                <div class="text-block__caption">The skin becomes soft and supple, acquires a smooth,
                                    velvety texture.</div>
                            </div>
                            <div class="text-block">
                                <div class="text-block__title">Protects from harmful rays</div>
                                <div class="text-block__caption">Helps lighten the skin and protect it from the harmful
                                    effects of free radicals that cause premature aging</div>
                            </div>
                            <div class="text-block">
                                <div class="text-block__title">Does not leave greasy stains</div>
                                <div class="text-block__caption">Serum is easily absorbed during application. Ideal for
                                    people with any type of skin.</div>
                            </div>
                        </div>
                        <div class="how-section__image">
                            <!-- <img src="img/mabel_2.jpg" alt="Filorga Meso-Mask"> -->
                            <img src="img/u/Edit-02.png" alt="Filorga Meso-Mask">
                        </div>
                    </div>
                </div>
            </section>
            <section id="problems" class="problems-section section-common section-arrow">
                <div class="wrapper">
                    <div class="custom-title">
                        <span class="custom-title__inner">
                            What problems does <span class="bold">Filorga Meso-Mask</span> fix?
                        </span>
                    </div>
                    <div class="problems-section__text">
                        <p>A unique development based on the extract of blueberries, hyaluronic acid and verbena
                            extract, created specifically for anti-aging skin care.</p>
                        <p>Extract of blueberry resists aging of skin cells, contributes to the production of collagen,
                            prevents the formation of wrinkles, improves complexion, and also removes pigment spots.</p>
                        <p>Hyaluronic acid saturates the skin cells with moisture, which stimulates the synthesis of
                            collagen. The skin becomes elastic and soft. As a result, wrinkles are smoothed.</p>
                    </div>
                    <div class="problems-section__inner">
                        <ul class="problems-list problems-list_left">
                            <li>
                                <span>Wrinkles on the forehead and in the brow</span>
                            </li>
                            <li>
                                <span>Nasolabial folds</span>
                            </li>
                            <li>
                                <span>Pigmentation</span>
                            </li>
                        </ul>
                        <img src="img/face.jpg" class="problems-section__image" alt="">
                        <ul class="problems-list problems-list_right">
                            <li>
                                <span>Wrinkle</span>
                            </li>
                            <li>
                                <span>Laxity and loss of elasticity</span>
                            </li>
                            <li>
                                <span>Wrinkles in the neck</span>
                            </li>
                        </ul>
                    </div>
                </div>
            </section>
            <section id="usage" class="usage-section section-common section-arrow">
                <div class="wrapper">
                    <div class="custom-title">
                        <span class="custom-title__inner">
                            How to use the <span class="bold">Filorga Meso-Mask?</span>
                        </span>
                    </div>
                    <div class="usage-section__text">
                        <p> Filorga Meso-Mask affects the skin throughout your day!</p>
                        <p>A soft, velvety texture, radiant color, smooth elastic surface - this is the result of the
                            application of serum, visible from the first days of application!</p>
                    </div>
                    <ul class="usage-list">
                        <li class="usage-list__text">
                            <div class="usage-list__text-inner">
                                <div class="usage-list__text-caption">
                                    <p>
                                        1.
                                        <br>Clean your skin of the face in the usual way.
                                    </p>
                                    <p>
                                        2.
                                        <br>Prepare the skin by treating with a suitable tonic for you.
                                    </p>
                                </div>
                            </div>
                        </li>
                        <li class="usage-list__image">
                            <div class="usage-list__num">1</div>
                            <img src="img/steps_1.jpg" alt="">
                        </li>
                        <li class="usage-list__image">
                            <div class="usage-list__num">2</div>
                            <img src="img/steps_2.jpg" alt="">
                        </li>
                        <li class="usage-list__image ">
                            <div class="usage-list__num">3</div>
                            <!-- <img src="img/steps_3.jpg" alt=""> -->
                            <img src="img/u/Edit-03_up.png" alt="">
                        </li>
                        <li class="usage-list__image">
                            <div class="usage-list__num">4</div>
                            <img src="img/steps_4.jpg" alt="">
                        </li>
                        <li class="usage-list__text">
                            <div class="usage-list__text-inner usage-list__text-inner_gold">
                                <div class="usage-list__text-caption">
                                    <p>
                                        3.
                                        <br>Apply evenly 4-5 drops of whey over the entire surface of the whole face,
                                        eyes contour, neck and chest.
                                    </p>
                                    <p>
                                        4.
                                        <br>Leave on for 15 to 30 minutes. Remove by abundantly rinsing with fresh
                                        water.
                                    </p>
                                </div>
                            </div>
                        </li>
                    </ul>
                    <div class="usage-section__bottom">
                        After that, you can apply any decorative cosmetics to your face.
                        <br>
                        <span class="bold">It works all the time!</span>
                    </div>
                </div>
            </section>
            <section id="testimonials" class="testimonials-section section-common section-arrow">
                <div class="wrapper">
                    <div class="custom-title">
                        <span class="custom-title__inner">
                            Reviews of women who use <span class="bold">Filorga Meso-Mask?</span>
                        </span>
                    </div>
                    <div class="testimonials js-testimonialsSlider">
                        <div class="testimonials__item">
                            <div class="testimonials__image">
                                <img src="img/user_1.jpg" alt="">
                            </div>
                            <div class="testimonials__name">
                                Diana
                            </div>
                            <div class="testimonials__age">
                                43 years
                            </div>
                            <div class="testimonials__text">It's unpleasant to see so many new wrinkles on your face.
                                Tried various means, expensive enough, but wrinkles did not disappear anywhere. Filorga
                                Meso-Mask tried already without much hope. The more incredible was the effect. When just
                                a week later I looked carefully at myself in the mirror - I could not believe my eyes!
                                <span class="wow bg-text">Net of wrinkles somehow disappeared! And deep creases on the
                                    forehead became barely noticeable! A blush on the face appeared!</span> Everyone
                                tells me that I am younger. Yes, I can see for myself!</div>
                        </div>
                        <div class="testimonials__item">
                            <div class="testimonials__image">
                                <img src="img/user_2.jpg" alt="">
                            </div>
                            <div class="testimonials__name">
                                Lera
                            </div>
                            <div class="testimonials__age">
                                37 years
                            </div>
                            <div class="testimonials__text">They say that stresses age more than years. In my case, it
                                was true. Tried to paint the gray skin with decorative cosmetics - it looked even worse.
                                Tried Filorga Meso-Mask. <span class="wow bg-text">A couple of days later I saw that the
                                    skin had acquired a healthy shade, the grayness had disappeared and the face had
                                    become very fresh.</span> And in a month I was just not to know! Smooth skin,
                                beautiful color, returned a blush. Beauty! And when a woman feels beautiful she feels
                                that she is alive!</div>
                        </div>
                        <div class="testimonials__item">
                            <div class="testimonials__image">
                                <img src="img/user_3.jpg" alt="">
                            </div>
                            <div class="testimonials__name">
                                Valentine
                            </div>
                            <div class="testimonials__age">
                                45 years
                            </div>
                            <div class="testimonials__text">I regret that I learned so late about the Filorga Meso-Mask
                                serum! All the age-related skin problems I felt on myself. Wrinkles, stains, dryness.
                                And the salvation was serum. She returned the feeling of youth to her skin. <span
                                    class="wow bg-text">Spots disappear, wrinkles began to disappear. I feel and look
                                    much younger.</span> I am glowed with happiness and I give it to others.</div>
                        </div>
                        <div class="testimonials__item">
                            <div class="testimonials__image">
                                <img src="img/user_4.jpg" alt="">
                            </div>
                            <div class="testimonials__name">
                                Mary
                            </div>
                            <div class="testimonials__age">
                                29 years
                            </div>
                            <div class="testimonials__text">I was sick a lot this fall. And after such a shake-up of the
                                body began to notice that the skin of the face became disgusting and somewhat faded.
                                Cosmetics did not help much. I was advised by a friend to try the serum of Filorga
                                Meso-Mask. The effect was seen immediately, almost in a couple of days after
                                application. <span class="wow bg-text">The skin became very tender to the touch, filled
                                    with moisture, and somehow even lit up from the inside. Just awesome!</span></div>
                        </div>
                        <div class="testimonials__item">
                            <div class="testimonials__image">
                                <img src="img/user_5.jpg" alt="">
                            </div>
                            <div class="testimonials__name">
                                Vita
                            </div>
                            <div class="testimonials__age">
                                35 years
                            </div>
                            <div class="testimonials__text">I have a very sensitive skin and not every cosmetic product
                                is suitable for it. I can not stand cosmetics, which lies on the face with a thick layer
                                of fat! And the Filorga Meso-Mask proved to be exactly the means that is just perfect
                                for me! <span class="wow bg-text">Light, without chemical odor, well absorbed and does
                                    not leave greasy stains!</span> And the skin after the application directly shines!
                                Well, just a magic cream!</div>
                        </div>
                        <div class="testimonials__item">
                            <div class="testimonials__image">
                                <img src="img/user_6.jpg" alt="">
                            </div>
                            <div class="testimonials__name">
                                Nataly
                            </div>
                            <div class="testimonials__age">
                                27 years
                            </div>
                            <div class="testimonials__text">It is unfortunate that the Filorga Meso-Mask serum did not
                                hit me before! I'm very sick of winter cold! My skin from the wind and frost becomes
                                disgustingly dry and begins to peel off. By spring, I'm becoming like a monster with
                                spots of acne and I have to undergo a long recovery course. And this magic serum
                                literally saved my face this winter! <span class="wow bg-text">Beautiful fresh skin
                                    without the slightest sign of dryness and stains!</span></div>
                        </div>
                    </div>
                    <div class="testimonials-control"></div>
                    <div class="custom-title custom-title_recommendations">
                        <span class="custom-title__inner">We are recommended by</span>
                    </div>
                    <div class="recommendations">
                        <div class="recommendations__item">
                            <img src="img/marie_claire.png" alt="Marie Claire">
                        </div>
                        <div class="recommendations__item">
                            <img src="img/vogue.png" alt="Vogue">
                        </div>
                        <div class="recommendations__item">
                            <img src="img/cosmopolitan.png" alt="COSMOPOLITAN">
                        </div>
                    </div>
                </div>
            </section>
            <section id="doctor" class="doctor-section section-common section-arrow">
                <div class="wrapper">
                    <div class="custom-title">
                        <span class="custom-title__inner">
                            Specialists opinion about <span class="bold">Filorga Meso-Mask</span>
                        </span>
                    </div>
                    <div class="doctor-section__inner">
                        <div class="doctor-section__image">
                            <img src="img/doctor.jpg" alt="">
                        </div>
                        <div class="doctor-section__text">
                            <div class="doctor-section__title">N.I. Stevenson</div>
                            <div class="doctor-section__sub-title">Cosmetologist</div>
                            <div class="doctor-section__caption">Our face is most exposed to external factors - wind,
                                cold, sunlight. As a result, the skin on the face loses moisture, elasticity, and, as a
                                result, grows old. Therefore, it constantly needs to be recharged. What is good about
                                Filorga Meso-Mask? It has components that contain everything you need to restore skin
                                cells. Bilberry extract starts regeneration processes, resists aging of skin cells and
                                smoothes wrinkles. Hyaluronic acid is the main builder of the epidermis and the skin
                                youth element. Nothing extra! Skin cells, saturated with bilberry extract and hyaluronic
                                acid, become younger. Fade wrinkles. Verbena extract, which is a powerful natural
                                antioxidant, struggles with acne and stains, gently exfoliates the skin, making it clean
                                and sparkling and tightening pores.</div>
                        </div>
                    </div>
                    <div class="certificates">
                        <img src="img/cert_3.png" alt="">
                        <img src="img/cert_4.png" alt="">
                    </div>
                </div>
            </section>
            <section id="questions" class="questions-section section-common section-arrow">
                <div class="wrapper">
                    <div class="custom-title">
                        <span class="custom-title__inner">Question-answer</span>
                    </div>
                    <div class="questions-section__inner">
                        <div class="questions-section__cell">
                            <div class="questions-item">
                                <div class="questions-item__title">How fast there will be a result?</div>
                                <div class="questions-item__caption">You will feel the comfort of moisturized skin after
                                    the first use. After several applications, the skin will become radiant, fine
                                    wrinkles will be smoothed. The longer you use serum, the brighter the result.</div>
                            </div>
                        </div>
                        <div class="questions-section__cell">
                            <div class="questions-item">
                                <div class="questions-item__title">Does serum burns?</div>
                                <div class="questions-item__caption">No! We use ingredients that are as gentle to your
                                    skin as possible.<br />But there is a small percentage of people with sensitivity to
                                    verbena extract. Therefore, if you experience discomfort - pause between
                                    applications for a day or two.<br />This will allow your skin to adapt to the serum
                                    formula.</div>
                            </div>
                            <div class="questions-item">
                                <div class="questions-item__title">What is in it?</div>
                                <div class="questions-item__caption">
                                    <p>We have developed a unique formula to create a product that will be convenient
                                        and effective. Our serum does not contain parabens, essential oils or
                                        fragrances.</p>
                                    COMPOSITION: blueberry extract, hyaluronic acid, verbena extract, resin extract
                                    "Draconic Blood", biosaccharide resin - 1, water, glycerin
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </section>
        </div>
        <!--#content-->
        <section class="work">
            <section id="work" class="work-section section-common">
                <div class="wrapper">
                    <div class="custom-title">
                        <span class="custom-title__inner">How are we working?</span>
                    </div>
                    <ul class="work-list">
                        <li>
                            <div class="work-list__inner">
                                <span>1</span>
                                <div class="work-list__icon">
                                    <svg class="svg" version="1.1" xmlns="http://www.w3.org/2000/svg"
                                        xmlns:xlink="http://www.w3.org/1999/xlink" xml:space="preserve">
                                        <use xlink:href="#order-ic"></use>
                                    </svg>
                                </div>
                            </div>
                            <div class="work-list__caption">You need to place an order-request on this site.</div>
                        </li>
                        <li>
                            <div class="work-list__inner">
                                <span>2</span>
                                <div class="work-list__icon">
                                    <svg class="svg" version="1.1" xmlns="http://www.w3.org/2000/svg"
                                        xmlns:xlink="http://www.w3.org/1999/xlink" xml:space="preserve">
                                        <use xlink:href="#call-ic"></use>
                                    </svg>
                                </div>
                            </div>
                            <div class="work-list__caption">We will contact you!</div>
                        </li>
                        <li>
                            <div class="work-list__inner">
                                <span>3</span>
                                <div class="work-list__icon">
                                    <svg class="svg" version="1.1" xmlns="http://www.w3.org/2000/svg"
                                        xmlns:xlink="http://www.w3.org/1999/xlink" xml:space="preserve">
                                        <use xlink:href="#box-ic"></use>
                                    </svg>
                                </div>
                            </div>
                            <div class="work-list__caption">Send your order!</div>
                        </li>
                        <li>
                            <div class="work-list__inner">
                                <span>4</span>
                                <div class="work-list__icon">
                                    <svg class="svg" version="1.1" xmlns="http://www.w3.org/2000/svg"
                                        xmlns:xlink="http://www.w3.org/1999/xlink" xml:space="preserve">
                                        <use xlink:href="#hand-ic"></use>
                                    </svg>
                                </div>
                            </div>
                            <div class="work-list__caption">You pay for the parcel upon receipt.</div>
                        </li>
                    </ul>
                </div>
            </section>
        </section>

        <footer id="footer" class="header-section">
            <div class="wrapper clearfix">
                <div class="header-section__inner">
                    <div class="header-title">Young and healthy skin in a few days</div>
                    <div class="header-mabel">
                        <div class="header-mabel__content">
                            <div class="header-mabel__title">
                                <span> Sales </span>
                                <br>
                                <span> Hit </span>
                            </div>
                            <div class="header-mabel__year">
                                <script>
                                    document.write((new Date()).getFullYear());
                                </script>
                            </div>
                            <div class="header-mabel__countries">In Europa<br>In the USA</div>
                        </div>
                    </div>
                    <ul class="header-list">
                        <li>
                            <span>• Without injections</span>
                        </li>
                        <li>
                            <span>• Without plastics</span>
                        </li>
                        <li>
                            <span>• Without expensive procedures</span>
                        </li>
                    </ul>
                    <div class="header-order">
                        <div id="order-footer" class="TLorder">
                            <div class="head edge">
                                <div class="head__discount"></div>
                                <div class="price bb">
                                    <div class="price__old price__old-crossed">
                                        <span class="al-raw-cost-promo"><x-oldprice>5998</x-oldprice></span>
                                        <span class="al-raw-currency"><x-currency>বাংলাদেশি টাকা</x-currency> </span>
                                    </div>
                                    <div class="price__new">
                                        <span class="al-raw-cost"><x-newprice>2999</x-newprice></span>
                                        <span class="al-raw-currency"><x-currency>বাংলাদেশি টাকা</x-currency> </span>
                                    </div>
                                </div>
                                <h3 class="head__title">FILL IN THE FORM AND WE WILL CONTACT YOU</h3>
                            </div>

                            <form action="" method="post" class="al-form form">
                                        <input name="csrf_token" type="hidden" value="8a02c14ee024aba1b7a55c294a1ecf64:1601927468" />
    <select name="offer" class="form-control country_chang" style="display: none;">
        <option
                data-country-code="BD"
                selected="selected"
                value="18739"
        >
            Бангладеш        </option>
    </select>

      
                                <div class="input-wrapper">
                                    <input type="text" name="name" class="form__input" placeholder="Name" id="name2">
                                    <label for="name2"></label>
                                </div>
                                <div class="input-wrapper">
                                    <input type="tel" name="phone" class="form__input" placeholder="Phone" id="phone2">
                                    <label for="phone2"></label>
                                </div>
                                <button type="submit" class="form__submit js-submit">ORDER&nbsp;<i class="arrow"></i>
                                </button>
                                <div class="icons-secure">
                                    <i class="norton"></i>
                                    <i class="mcAfee"></i>
                                </div>
                            </form>
                        </div>
                    </div>
                </div>
            </div>
        </footer>
    </section>
    <script src="js/jquery.min.js"></script>
    <script src="js/wow.js"></script>
    <script type="text/javascript">
        $(function () {
            var menu = $(".js-mobileMenuList");
            var menuBtn = $(".menu-button");
            $("div.footer").appendTo("#footer");
            $("a[href^='#']").click(function () {
                var _href = $(this).attr("href");
                $("html, body").animate({
                    scrollTop: $(_href).offset().top + "px"
                });
                return false;
            });
            menuBtn.click(function () {
                menu.toggleClass("active");
                menuBtn.toggleClass("active");
            });
            var a = new WOW({
                boxClass: 'wow',
                animateClass: 'animate',
                offset: 100
            });
            a.init();
        });
    </script>


</body>



</html>
