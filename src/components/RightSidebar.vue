<template>
  <v-navigation-drawer color="#14141C" right width="290" app dark>
    <v-toolbar flat>
      <v-icon color="#7C7C7F" class="mr-5" size="20">fas fa-search</v-icon>
      <v-badge color="red" dot overlap width="2" class="mr-8">
        <v-icon color="#7C7C7F" size="20">far fa-bell</v-icon>
      </v-badge>

      <v-divider vertical color="#7C7C7F" class="mr-5"></v-divider>
      <v-badge
        bordered
        bottom
        color="green lighten-4"
        dot
        offset-x="10"
        offset-y="10"
      >
        <v-avatar size="30" color="grey">
          <v-icon>mdi-account</v-icon>
        </v-avatar>
      </v-badge>
      <v-btn text class="grey--text lighten-4 ">
        APERIO
      </v-btn >
      <v-btn icon dark >
        <v-icon x-small color="#7C7C7F" >
        fas fa-chevron-down
      </v-icon>
      </v-btn>
    </v-toolbar>
    <strong class="white--text ml-3 ">Overall Progress</strong><br>
    <strong class="grey--text caption ml-3 ">Betty First Vuetify</strong>

    <div class="text-center mb-6 mt-2">
    <v-progress-circular
      :rotate="360"
      :size="100"
      :width="15"
      :value="70"
      color="orange"
    >
      70%
    </v-progress-circular>
    </div>

    <strong class="white--text ml-3  ">Recent Activities</strong><br>
    <strong class="grey--text caption ml-3 ">11 August 2022</strong>

    
    <v-list three-line>
      <template v-for="(item, index) in files">
        <v-subheader
          v-if="item.tile"
          :key="index"
          v-text="item.title"
        ></v-subheader>

        
        <v-list-item
          v-else
          :key="item.title"
        >
          <v-list-item-avatar>
            <v-img :src="item.avatar"></v-img>
          </v-list-item-avatar>

          <v-list-item-content>
            <v-list-item-title v-html="item.title"></v-list-item-title>
            <v-list-item-subtitle v-html="item.subtitle"></v-list-item-subtitle>
            <v-list-item-subtitle v-html="item.time"></v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>
      </template>
    </v-list>
    <v-row>
        <v-col cols="12" sm="6">
            <v-card class="d-flex align-center ml-5 " color="#21212B" width="120" height="60" >
                <v-row>
                    <v-col cols="12" sm="12">
                        <v-list two-line class="text-center">
                            <v-list-item >
                                <v-list-item-content>
                                    <v-list-item-title class="white--text ">
                                        550
                                    </v-list-item-title>
                                    <v-list-item-subtitle class="gray--text caption">
                                        Total Project
                                    </v-list-item-subtitle>
                                </v-list-item-content>
                            </v-list-item>
                        </v-list>
                    </v-col>
                </v-row>
            </v-card>
        </v-col>
        <v-col cols="12" sm="6">
            <v-card class="d-flex align-center mr-5" color="#A9DDD8" width="120" height="60" >
                <v-row>
                    <v-col cols="12" sm="12">
                        <v-list two-line class="text-center">
                            <v-list-item >
                                <v-list-item-content>
                                    <v-list-item-title class="black--text ">
                                        650
                                    </v-list-item-title>
                                    <v-list-item-subtitle class="black--text caption">
                                        Up Coming
                                    </v-list-item-subtitle>
                                </v-list-item-content>
                            </v-list-item>
                        </v-list>
                    </v-col>
                </v-row>
            </v-card>
        </v-col>
        <v-col cols="12" sm="6">
            <v-card class="d-flex align-center ml-5"  color="#21212B" width="120" height="60" >
                <v-row>
                    <v-col cols="12" sm="12">
                        <v-list two-line class="text-center">
                            <v-list-item >
                                <v-list-item-content>
                                    <v-list-item-title class="white--text ">
                                        350
                                    </v-list-item-title>
                                    <v-list-item-subtitle class="gray--text caption">
                                        In Progress
                                    </v-list-item-subtitle>
                                </v-list-item-content>
                            </v-list-item>
                        </v-list>
                    </v-col>
                </v-row>
            </v-card>
        </v-col>
        <v-col cols="12" sm="6">
            <v-card class="d-flex align-center mr-5" color="#21212B" width="120" height="60" >
                <v-row>
                    <v-col cols="12" sm="12">
                        <v-list two-line class="text-center">
                            <v-list-item >
                                <v-list-item-content>
                                    <v-list-item-title class="white--text ">
                                        450
                                    </v-list-item-title>
                                    <v-list-item-subtitle class="gray--text caption">
                                        Completed
                                    </v-list-item-subtitle>
                                </v-list-item-content>
                            </v-list-item>
                        </v-list>
                    </v-col>
                </v-row>
            </v-card>
        </v-col>
    </v-row>

  </v-navigation-drawer>
</template>

<script>
export default {
    data: () => ({
files :[
        {
          avatar: 'https://cdn.vuetifyjs.com/images/lists/1.jpg',
          time: '5 Mins Ago',
          subtitle: `Backend Developer`,
          title: `<strong>Mike Loke</strong>`,
        },
        {
           avatar: 'https://cdn.vuetifyjs.com/images/lists/2.jpg',
           time: '15 Mins Ago',
          subtitle: `Senior Quality Assurance`,
          title: `<strong>Sarah Hosten</strong>`,
        },
        {
           avatar: 'https://cdn.vuetifyjs.com/images/lists/3.jpg',
          time: '30 Mins Ago',
          subtitle: `Business Development`,
          title: `<strong>Dena Thompson</strong>`,
        },
       
      
      ],
})
};
</script>

<style></style>
