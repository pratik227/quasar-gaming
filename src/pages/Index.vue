<template>
  <q-page class="" style="background-color: #1e1d32">
    <q-card class="bg-transparent">
      <q-card-section class="q-pa-none">
        <div class="row">
          <div class="col-lg-12 col-sm-12 col-xs-12 col-md-12">
            <q-carousel
              v-model="slide"
              transition-prev="slide-right"
              transition-next="slide-left"
              swipeable infinite
              animated
              control-color="primary"
              auto-play
              arrows autoplay
              height="300px"
              class="rounded-borders bg-transparent"
            >
              <q-carousel-slide :name="1" class="column no-wrap">
                <div class="row fit justify-start items-center q-gutter-xs q-col-gutter no-wrap">
                  <q-img class="rounded-borders  full-height" :src="require('src/assets/slide-1.jpg')"/>
                  <div class="absolute-center text-center  full-width text-white">
                    <div class="text-h4 text-stroke q-pa-sm">Welcome to GamePlay</div>
                    <div class="text-h2 text-stroke q-pa-sm">Games Just for You</div>
                    <div class="text-h2">
                      <q-btn class="text-capitalize bg-white text-grey-8 text-weight-bolder" label="Read More"></q-btn>
                    </div>
                  </div>
                </div>
              </q-carousel-slide>
              <q-carousel-slide :name="2" class="column no-wrap">

                <div class="row fit justify-start items-center q-gutter-xs q-col-gutter no-wrap">
                  <q-img class="rounded-borders  full-height" :src="require('src/assets/slide-2.jpg')"/>
                  <div class="absolute-center text-center  full-width text-white">
                    <div class="text-h4 text-stroke q-pa-sm">Welcome to GamePlay</div>
                    <div class="text-h2 text-stroke q-pa-sm">Games Just for You</div>
                    <div class="text-h2">
                      <q-btn class="text-capitalize bg-white text-grey-8 text-weight-bolder" label="Read More"></q-btn>
                    </div>
                  </div>
                </div>
              </q-carousel-slide>
              <q-carousel-slide :name="3" class="column no-wrap">
                <div class="row fit justify-start items-center q-gutter-xs q-col-gutter no-wrap">
                  <q-img class="rounded-borders  full-height" :src="require('src/assets/slide-3.jpg')"/>
                  <div class="absolute-center text-center  full-width text-white">
                    <div class="text-h4 text-stroke q-pa-sm">Welcome to GamePlay</div>
                    <div class="text-h2 text-stroke q-pa-sm">Games Just for You</div>
                    <div class="text-h2">
                      <q-btn class="text-capitalize bg-white text-grey-8 text-weight-bolder" label="Read More"></q-btn>
                    </div>
                  </div>
                </div>
              </q-carousel-slide>
              <q-carousel-slide :name="4" class="column no-wrap">
                <div class="row fit justify-start items-center q-gutter-xs q-col-gutter no-wrap">
                  <q-img class="rounded-borders  full-height" :src="require('src/assets/slide-1.jpg')"/>
                  <div class="absolute-center text-center  full-width text-white">
                    <div class="text-h4 text-stroke q-pa-sm">Welcome to GamePlay</div>
                    <div class="text-h2 text-stroke q-pa-sm">Games Just for You</div>
                    <div class="text-h2">
                      <q-btn class="text-capitalize bg-white text-grey-8 text-weight-bolder" label="Read More"></q-btn>
                    </div>
                  </div>
                </div>
              </q-carousel-slide>
            </q-carousel>
          </div>
        </div>
      </q-card-section>
      <q-card-section>

        <div class="text-center q-mt-xl text-white text-h4 text-weight-bolder q-mb-md">
          Upcoming Games
        </div>
        <div class="row q-mt-xl q-col-gutter-sm">
          <div class="col-lg-3 col-md-3 col-sm-12 col-xs-12" v-for="data in card_data">
            <q-card class="no-border bg-transparent text-white no-shadow">
              <q-card-section class="text-center">
                <q-avatar size="130px" class="shadow-10">
                  <img :src="data.img">
                </q-avatar>
              </q-card-section>

              <q-card-section class="q-pt-none text-center ">
                <div class="text-h5">
                  {{data.title}}
                </div>
                <div class="text-caption text-h6 ">
                  {{data.date}}
                </div>
              </q-card-section>
            </q-card>
          </div>
        </div>
      </q-card-section>
      <q-card-section class="q-mx-xl">
        <div class="text-center q-mt-xl text-white text-h4 text-weight-bolder q-mb-md">
          My Latest Post
        </div>
        <div class="row q-mt-xl q-col-gutter-lg">
          <div class="col-lg-4 col-md-4 col-sm-12 col-xs-12" v-for="data in post_data">
            <q-card style="background-color: #292845" class="text-white">
              <q-img
                :src="data.img"
              />
              <q-separator></q-separator>
              <q-card-section class="text-subtitle1 q-px-xl">
                Bar XYZ
                <div class="float-right">
                  MAR 12 2020
                </div>
              </q-card-section>
              <q-card-section class="text-h5 q-px-xl">
                Our Changing Planet
              </q-card-section>
              <q-card-section class="q-px-xl">
                <div>
                  {{text}}
                </div>
              </q-card-section>
              <q-card-section class="text-subtitle1  q-px-lg">
                <q-btn color="" icon="person" class="bg-transparent text-capitalize" flat label="By Admin"/>
                <div class="float-right">
                  <q-btn color="" icon="chat_bubble" class="bg-transparent" flat label="56"/>
                </div>
              </q-card-section>
            </q-card>
          </div>
        </div>
      </q-card-section>
      <q-card-section class="q-mx-xl">
        <div class="text-center q-mt-xl text-white text-h4 text-weight-bolder q-mb-md">
          <q-tabs
            v-model="tab"
            dense
            align="justify"
            class="bg-transparent text-white rounded-borders"
            :breakpoint="0"
          >
            <q-tab name="Most Popular Streams" label="Most Popular Streams"/>
            <q-tab name="Upcoming Competition" label="Upcoming Competition"/>
            <q-tab name="Prosciutto Meatball Flank" label="Prosciutto Meatball Flank"/>
          </q-tabs>
        </div>
        <q-tab-panels v-model="tab" animated class="bg-transparent text-white ">
          <q-tab-panel name="Most Popular Streams" class="q-pa-none">
            <q-card class="q-pa-none bg-transparent row">
              <q-card-section horizontal class="col-lg-6 col-md-6 col-sm-12 col-xs-12">
                <q-img
                  :src="require('src/assets/download.jpg')"
                />

              </q-card-section>

              <q-card-section class="q-px-lg col-lg-6 col-md-6 col-sm-12 col-xs-12 text-justify">
                  <div class="text-h6"> CREATE YOUR OWN CHANNEL AND START TO STREAM GAMES NOW</div>

                  <div class="q-mt-sm">
                    Drumstick meatloaf capicola short ribs, pork chop cupim kielbasa jerky porchetta pancetta chicken
                    pastrami turkey tenderloin sausage. Pig buffalo alcatra meatball. T-bone hamburger bresaola kevin
                    shank porchetta ground. Round beef tail tri-tip. Short loin pork strip steak venison.

                  </div>
                  <div class="q-mt-md">
                    <q-btn label="Get Started Now"
                           style="background-image: linear-gradient(to right, #89f7fe 0%, #66a6ff 100%) !important;"></q-btn>
                  </div>

                  <div class="q-mt-md">

                    <div class="text-h6">9 136 STREAMS FROM MOST RECENT GAMES</div>
                    <div class="text-caption">267 347 watching now</div>
                  </div>
                </q-card-section>
            </q-card>
          </q-tab-panel>

          <q-tab-panel name="Upcoming Competition" class="q-pa-none">
            <q-card class="q-pa-none bg-transparent row">
              <q-card-section horizontal class="col-lg-6 col-md-6 col-sm-12 col-xs-12">
                <q-img
                  :src="require('src/assets/download.jpg')"
                />
              </q-card-section>
                <q-card-section class="q-pa-none col-lg-6 col-md-6 col-sm-12 col-xs-12 text-justify">
                  <div class="text-h6">
                    <q-list class="full-width">
                      <q-item class="full-width">
                        <q-item-section top avatar>
                          <q-avatar rounded size="60px">
                            <img src="https://cdn.quasar.dev/img/boy-avatar.png">
                          </q-avatar>
                        </q-item-section>

                        <q-item-section>
                          <q-item-label class="text-weight-bolder">SHANKLE RIBEYE BACON</q-item-label>
                          <q-item-label caption class="text-white">267 347 participants
                          </q-item-label>
                        </q-item-section>
                      </q-item>
                      <q-separator color="white" inset="item"></q-separator>
                      <q-item class="full-width">
                        <q-item-section top avatar>
                          <q-avatar rounded size="60px">
                            <img src="https://cdn.quasar.dev/img/boy-avatar.png">
                          </q-avatar>
                        </q-item-section>

                        <q-item-section>
                          <q-item-label class="text-weight-bolder">BACON TENDERLOIN DRUMSTICK MEATBALL</q-item-label>
                          <q-item-label caption class="text-white">267 347 participants
                          </q-item-label>
                        </q-item-section>
                      </q-item>
                      <q-separator color="white" inset="item"></q-separator>
                      <q-item class="full-width">
                        <q-item-section top avatar>
                          <q-avatar rounded size="60px">
                            <img src="https://cdn.quasar.dev/img/boy-avatar.png">
                          </q-avatar>
                        </q-item-section>

                        <q-item-section>
                          <q-item-label class="text-weight-bolder">DONER BRESAOLA PORK KIELBASA</q-item-label>
                          <q-item-label caption class="text-white">267 347 participants
                          </q-item-label>
                        </q-item-section>
                      </q-item>
                      <q-separator color="white" inset="item"></q-separator>
                      <q-item class="full-width">
                        <q-item-section top avatar>
                          <q-avatar rounded size="60px">
                            <img src="https://cdn.quasar.dev/img/boy-avatar.png">
                          </q-avatar>
                        </q-item-section>

                        <q-item-section>
                          <q-item-label class="text-weight-bolder">KIELBASA FATBACK ALCATR</q-item-label>
                          <q-item-label caption class="text-white">267 347 participants
                          </q-item-label>
                        </q-item-section>
                      </q-item>
                    </q-list>
                  </div>
                </q-card-section>
            </q-card>
          </q-tab-panel>

          <q-tab-panel name="Prosciutto Meatball Flank" class="q-pa-none">
            <q-card class="q-pa-none bg-transparent row">
              <q-card-section horizontal class="col-lg-6 col-md-6 col-sm-12 col-xs-12">
                <q-img
                  :src="require('src/assets/download.jpg')"
                />
              </q-card-section>


                <q-card-section class="q-pa-none col-lg-6 col-md-6 col-sm-12 col-xs-12 text-justify">
                  <div class="text-h6">
                    <q-list class="full-width">
                      <q-item class="full-width">
                        <q-item-section top avatar>
                          <q-avatar rounded size="60px">
                            <img src="https://cdn.quasar.dev/img/boy-avatar.png">
                          </q-avatar>
                        </q-item-section>

                        <q-item-section>
                          <q-item-label class="text-weight-bolder">SHANKLE RIBEYE BACON</q-item-label>
                          <q-item-label caption class="text-white">267 347 participants
                          </q-item-label>
                        </q-item-section>
                      </q-item>
                      <q-separator color="white" inset="item"></q-separator>
                      <q-item class="full-width">
                        <q-item-section top avatar>
                          <q-avatar rounded size="60px">
                            <img src="https://cdn.quasar.dev/img/boy-avatar.png">
                          </q-avatar>
                        </q-item-section>

                        <q-item-section>
                          <q-item-label class="text-weight-bolder">BACON TENDERLOIN DRUMSTICK MEATBALL</q-item-label>
                          <q-item-label caption class="text-white">267 347 participants
                          </q-item-label>
                        </q-item-section>
                      </q-item>
                      <q-separator color="white" inset="item"></q-separator>
                      <q-item class="full-width">
                        <q-item-section top avatar>
                          <q-avatar rounded size="60px">
                            <img src="https://cdn.quasar.dev/img/boy-avatar.png">
                          </q-avatar>
                        </q-item-section>

                        <q-item-section>
                          <q-item-label class="text-weight-bolder">DONER BRESAOLA PORK KIELBASA</q-item-label>
                          <q-item-label caption class="text-white">267 347 participants
                          </q-item-label>
                        </q-item-section>
                      </q-item>
                      <q-separator color="white" inset="item"></q-separator>
                      <q-item class="full-width">
                        <q-item-section top avatar>
                          <q-avatar rounded size="60px">
                            <img src="https://cdn.quasar.dev/img/boy-avatar.png">
                          </q-avatar>
                        </q-item-section>

                        <q-item-section>
                          <q-item-label class="text-weight-bolder">KIELBASA FATBACK ALCATR</q-item-label>
                          <q-item-label caption class="text-white">267 347 participants
                          </q-item-label>
                        </q-item-section>
                      </q-item>
                    </q-list>
                  </div>
                </q-card-section>
            </q-card>
          </q-tab-panel>
        </q-tab-panels>
      </q-card-section>


      <q-card-section>


        <div class="text-center q-mt-xl text-white text-h4 text-weight-bolder q-mb-md">
          Team
        </div>
        <div class="row q-mt-xl">
          <div class="col-lg-12 col-sm-12 col-xs-12 col-md-12">
            <q-carousel
              v-model="slide"
              transition-prev="slide-right"
              transition-next="slide-left"
              swipeable
              animated auto-play
              control-color="primary"
              padding
              arrows autoplay=""
              height="300px"
              class="rounded-borders bg-transparent"
            >
              <q-carousel-slide :name="1" class="column no-wrap">
                <div class="row fit justify-start items-center q-gutter-sm q-col-gutter no-wrap">
                  <card></card>
                  <card v-if="!$q.screen.lt.sm"></card>
                </div>
              </q-carousel-slide>
              <q-carousel-slide :name="2" class="column no-wrap">
                <div class="row fit justify-start items-center q-gutter-sm q-col-gutter no-wrap">
                  <card></card>
                  <card v-if="!$q.screen.lt.sm"></card>
                </div>
              </q-carousel-slide>
              <q-carousel-slide :name="3" class="column no-wrap">
                <div class="row fit justify-start items-center q-gutter-sm q-col-gutter no-wrap">
                  <card></card>
                  <card v-if="!$q.screen.lt.sm"></card>
                </div>
              </q-carousel-slide>
              <q-carousel-slide :name="4" class="column no-wrap">
                <div class="row fit justify-start items-center q-gutter-sm q-col-gutter no-wrap">
                  <card></card>
                  <card v-if="!$q.screen.lt.sm"></card>
                </div>
              </q-carousel-slide>
            </q-carousel>
          </div>
        </div>
      </q-card-section>


      <q-card-section>
        <div class="text-center q-mt-xl text-white text-h4 text-weight-bolder q-mb-md">
          Our Pricing Plans
        </div>
        <div class="row justify-center q-col-gutter-lg q-pa-lg">
          <div class="col-lg-4 col-sm-12 col-xs-12 col-md-4">

            <q-intersection
              once
              transition="scale"
            >
              <q-card style="background-color: #181728" class="text-white">
                <q-card-section class="text-center text-h6 q-pa-lg">
                  STANDARD PLAN
                </q-card-section>
                <q-card-section class="text-center"
                                style="background-image: linear-gradient(to top, #a8edea 0%, #fed6e3 100%);">
                  <div class="text-weight-bolder">
                    <span class="text-h6">$</span><span class="text-h3">39.</span><span class="text-h6">99</span>
                  </div>
                </q-card-section>

                <q-card-section class="text-center">
                  <q-item class="text-center">
                    <q-item-section>
                      Pork Ground Found Biltong
                    </q-item-section>
                  </q-item>
                  <q-separator color="white"/>
                  <q-item>
                    <q-item-section>
                      Capicola Sausage Beef Ribs
                    </q-item-section>
                  </q-item>
                  <q-separator color="white"/>
                  <q-item>
                    <q-item-section>
                      Pork Doner Frankfurter
                    </q-item-section>
                  </q-item>
                </q-card-section>

                <q-card-actions vertical align="center">
                  <q-btn class="text-capitalize q-mb-md q-pa-xs" style="background-color: #181728" outline color="">Buy
                    Plan Now
                  </q-btn>
                </q-card-actions>
              </q-card>
            </q-intersection>
          </div>
          <div class="col-lg-4 col-sm-12 col-xs-12 col-md-4">
            <q-intersection
              once
              transition="scale"
            >
              <q-card style="background-color: #181728" class="text-white">
                <q-card-section class="text-center text-h6 q-pa-lg">
                  GOLDEN PLAN
                </q-card-section>

                <q-card-section class="text-center"
                                style="background-image: linear-gradient(to right, #74ebd5 0%, #9face6 100%);">
                  <div class="text-weight-bolder">
                    <span class="text-h6">$</span><span class="text-h3">59.</span><span class="text-h6">59</span>
                  </div>
                </q-card-section>

                <q-card-section class="text-center">
                  <q-item class="text-center">
                    <q-item-section>
                      Doner Boudin Rump Picanha
                    </q-item-section>
                  </q-item>
                  <q-separator color="white"/>
                  <q-item>
                    <q-item-section>
                      Leberkas Kevin Drumstick
                    </q-item-section>
                  </q-item>
                  <q-separator color="white"/>
                  <q-item>
                    <q-item-section>
                      Beef Mignon Bresaola
                    </q-item-section>
                  </q-item>
                </q-card-section>
                <q-card-actions vertical align="center">
                  <q-btn class="text-capitalize q-mb-md q-pa-xs" style="background-color: #181728" outline color="">Buy
                    Plan Now
                  </q-btn>
                </q-card-actions>
              </q-card>
            </q-intersection>
          </div>
          <div class="col-lg-4 col-sm-12 col-xs-12 col-md-4">
            <q-intersection
              once
              transition="scale"
            >
              <q-card style="background-color: #181728" class="text-white">
                <q-card-section class=" text-center text-h6 q-pa-lg">
                  PLATINUM PLAN
                </q-card-section>

                <q-card-section class="text-center"
                                style="background-image: linear-gradient(135deg, #667eea 0%, #764ba2 100%);">
                  <div class="text-weight-bolder">
                    <span class="text-h6">$</span><span class="text-h3">109.</span><span class="text-h6">99</span>
                  </div>
                </q-card-section>

                <q-card-section class="text-center">
                  <q-item class="text-center">
                    <q-item-section>
                      Bresaola Shoulder Venison
                    </q-item-section>
                  </q-item>
                  <q-separator color="white"/>
                  <q-item>
                    <q-item-section>
                      Frankfurter Cow Ribeye Kielbasa
                    </q-item-section>
                  </q-item>
                  <q-separator color="white"/>
                  <q-item>
                    <q-item-section>
                      Cupim Drumstick Tail Pancetta
                    </q-item-section>
                  </q-item>
                </q-card-section>
                <q-card-actions vertical align="center">
                  <q-btn class="text-capitalize q-mb-md q-pa-xs" size="md" style="background-color: #181728" outline
                         color="">
                    Buy
                    Plan Now
                  </q-btn>
                </q-card-actions>

              </q-card>
            </q-intersection>
          </div>
        </div>
      </q-card-section>

      <q-card-section>
        <section style="min-height: 25vh;">
          <div class="row justify-center q-col-gutter-lg q-pa-lg items-center">
            <div class="col-lg-6 col-sm-12 col-xs-12 col-md-6 items-center">
              <div class="text-h4 text-white">Register for our Newsletter now</div>
            </div>
            <div class="col-lg-5 col-sm-12 col-xs-12 col-md-5 items-center">
              <div class="text-h6 text-white">
                <q-input dark outlined v-model="email" type="email" suffix="@gmail.com">
                  <template v-slot:before>
                    <q-icon name="mail" color="white"/>
                  </template>
                </q-input>
              </div>
            </div>
          </div>
        </section>
      </q-card-section>


    </q-card>

  </q-page>
</template>

<script>
    import Card from "../components/Card";

    export default {
        name: 'PageIndex',
        components: {Card},
        data() {
            return {
                email: '',
                tab: 'Most Popular Streams',
                slide: 1,
                card_data: [
                    {
                        title: 'Final 2019',
                        date: 'Mar 18-23, 2019',
                        img: require('src/assets/closeup-photo-of-bulbs-1293266.jpg')
                    },
                    {
                        title: 'No Man\'s sky',
                        date: 'DEC 18-23, 2020',
                        img: require('src/assets/close-up-photo-of-playing-cards-1796794.jpg')
                    },
                    {
                        title: 'Mix Combination 2020',
                        date: 'DEC 18-23, 2020',
                        img: require('src/assets/closeup-photo-of-bulbs-1293266.jpg')
                    },
                    {
                        title: 'Final 2020',
                        date: 'DEC 18-23, 2020',
                        img: require('src/assets/close-up-photo-of-playing-cards-1796794.jpg')
                    }
                ],
                post_data: [{img: require('src/assets/blog-img-1.jpg')}, {img: require('src/assets/blog-img-2.jpg')}, {img: require('src/assets/blog-img-3.jpg')}],
                text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.'

            }
        },
    }
</script>
<style>

  .text-stroke {
    color: white;
    -webkit-text-stroke: 1px #F8F8F8;
    text-shadow: 0px 1px 4px #23430C;
  }

  .q-carousel__slide, .q-carousel .q-carousel--padding{
    padding: 0px;
  }
</style>
