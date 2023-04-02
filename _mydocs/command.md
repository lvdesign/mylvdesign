

bundle install

bundle exec jekyll serve --livereload

bundle exec jekyll build --trace



git status

// https://lea.verou.me/2011/10/easily-keep-gh-pages-in-sync-with-master/
git checkout gh-pages // go to the gh-pages branch
git rebase master // bring gh-pages up to date with master
git push origin gh-pages // commit the changes
git checkout master // return to the master branch

git push

My suggestion would be to create gh-pages as an --orphan branch and only include the publication-ready material in it. You would have to clone from your master in a different local directory, use git checkout --orphan gh-pages to create gh-pages and then delete all the unnecessary files using git rm -rf .. From there you can go on and push to gh-pages after having added your publish-only files. Refer to Github docs for more info:
https://help.github.com/articles/creating-project-pages-manually/



Mettre _site dans _docs pour mise en ligne de gh_pages avec root _docs


formspree.io
mqkwavnb


<!-- Contact -->
<section id="contact">
    <div class="container">
        <div class="row">
            <div class="col-lg-12 text-center">
                <h2 class="section-heading">Contactez Moi</h2>
                <h3 class="section-subheading text-muted">Pour un renseignement, un devis… </h3>
            </div>
        </div>
        <div class="row">

            <div class="col-lg-12">
                <!-- mail Formspree -->
                <form action="" method="POST" id="contactForm" name="sentMessage">

                    <div class="row">
                        <div class="col-md-6">

                            <div class="form-group">
                                <label class="sr-only" for="name">Name</label>
                                <input class="form-control" name="name" id="name" type="text" placeholder="Votre nom *"
                                    required data-validation-required-message="SVP, votre nom.">
                                <p class="help-block text-danger"></p>
                            </div>

                            <div class="form-group">
                                <label class="sr-only" for="email">Email</label>
                                <input class="form-control" name="email" id="email" type="email"
                                    placeholder="Votre email *" required
                                    data-validation-required-message="SVP, votre email.">
                                <p class="help-block text-danger"></p>
                            </div>

                            <div class="form-group">
                                <label class="sr-only" for="phone">Téléphone</label>
                                <input class="form-control" name="phone" id="phone" type="tel"
                                    placeholder="Votre Téléphone *" required
                                    data-validation-required-message="SVP, votre numéro de téléphone.">
                                <p class="help-block text-danger"></p>
                            </div>
                        </div>

                        <div class="col-md-6">
                            <div class="form-group">
                                <label class="sr-only" for="message">Message</label>
                                <textarea class="form-control" name="message" id="message" placeholder="Votre message *"
                                    required data-validation-required-message="SVP, votre message."></textarea>
                                <p class="help-block text-danger"></p>
                            </div>

                            <div class="form-group">
                                <label class="sr-only" for="captcha">Captcha : 2 + 2 </label>
                                <input class="form-control" id="captcha" name="captcha" type="number"
                                    placeholder="La somme de 2 + 2  *" required
                                    data-validation-required-message="SVP, votre nombre.">
                                <p class="help-block text-danger"></p>
                            </div>
                        </div>

                    </div>

                    <div class="clearfix"></div>
                    <div class="col-md-12 text-center">
                        <div id="success"></div>
                        <button id="sendMessageButton" class="btn btn-xl" type="submit"><i class="fa fa-paper-plane-o"
                                aria-hidden="true"></i> Message</button>
                    </div>
            </div>
            </form>
        </div>
    </div>
    </div>
</section>
<!-- fin contact -->




   <div class="row">
            <div class="col-lg-8 mx-auto text-center">


                <h4>In the mood Twitter…</h4>
                <a class="twitter-timeline" href="https://twitter.com/lvdesign" data-widget-id="352010766683082754"
                    alt="le compte de lvdesign sur twitter, venez tweeter…"
                    title="le compte de lvdesign sur twitter, venez tweeter…">Tweets de @lvdesign</a>
                <!--tweet js-->
                <script>!function (d, s, id) { var js, fjs = d.getElementsByTagName(s)[0], p = /^http:/.test(d.location) ? 'http' : 'https'; if (!d.getElementById(id)) { js = d.createElement(s); js.id = id; js.src = p + "://platform.twitter.com/widgets.js"; fjs.parentNode.insertBefore(js, fjs); } }(document, "script", "twitter-wjs");</script>
            </div>
        </div>