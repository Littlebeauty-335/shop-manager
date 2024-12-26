<template>
  <v-app>
    <v-app-bar color="primary">
      <v-btn icon @click.stop="drawer = !drawer">
        <img src="/assets/images/store.png" alt="Custom Icon" />
      </v-btn>
      <v-toolbar-title>Shop Manager</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn icon="mdi-bell" variant="text" class="bell"></v-btn>
      <v-btn icon="mdi-account-circle" variant="text" class="profile"></v-btn>
    </v-app-bar>

    <v-navigation-drawer v-model="drawer" temporary>
      <v-list :items="items"></v-list>
    </v-navigation-drawer>

    <v-main>
      <v-container>
        <v-card class="mb-4">
          <v-card-title>
            Coffee Corner
            <v-chip class="green" color="green" label>Open</v-chip>
          </v-card-title>
          <v-card-subtitle>123 Main St, Cityville, State 12345</v-card-subtitle>
          <v-card-actions>
            <v-btn color="primary" class="addItem">+ Add New Item</v-btn>
            <v-btn class="edit">
              <img src="/assets/images/editing.png" alt="" />Edit Shop Details
            </v-btn>
            <v-btn class="edit">
              <img src="/assets/images/order.png" alt="" />View Orders
            </v-btn>
            <v-spacer></v-spacer>
          </v-card-actions>
        </v-card>

        <v-row>
          <v-col cols="12" md="6">
            <v-card class="recent-orders">
              <v-card-title>Recent Orders</v-card-title>

              <v-row class="mb-2" style="margin-bottom: 8px;">
                <v-col cols="6">
                  <v-select label="All Orders"></v-select>
                </v-col>
                <v-col cols="6">
                  <v-text-field prepend-inner-icon="mdi-calendar" label="mm/dd/yyyy"></v-text-field>
                </v-col>
              </v-row>

              <v-list class="mt-0">
                <v-list-item>
                  <v-row justify="space-between" align="center" no-gutters>
                    <v-col>
                      <v-list-item-title>John Doe</v-list-item-title>
                    </v-col>
                    <v-col class="text-right">
                      <span>$15.50</span>
                    </v-col>
                  </v-row>
                  <v-row justify="space-between" align="center" no-gutters>
                    <v-col>
                      <v-list-item-subtitle>2 x Cappuccino, 1 x Croissant</v-list-item-subtitle>
                    </v-col>
                    <v-col class="text-right">
                      <v-chip color="green" label>Completed</v-chip>
                    </v-col>
                  </v-row>
                </v-list-item>

                <v-list-item>
                  <v-row justify="space-between" align="center" no-gutters>
                    <v-col>
                      <v-list-item-title>Jane Smith</v-list-item-title>
                    </v-col>
                    <v-col class="text-right">
                      <span>$9.75</span>
                    </v-col>
                  </v-row>
                  <v-row justify="space-between" align="center" no-gutters>
                    <v-col>
                      <v-list-item-subtitle>1 x Latte, 1 x Muffin</v-list-item-subtitle>
                    </v-col>
                    <v-col class="text-right">
                      <v-chip color="orange" label>Pending</v-chip>
                    </v-col>
                  </v-row>
                </v-list-item>
              </v-list>
            </v-card>
          </v-col>

          <v-col cols="12" md="6">
            <v-card class="analytics">
              <v-card-title>Analytics</v-card-title>
              <v-select label="Daily" :items="['Daily', 'Weekly', 'Monthly']"></v-select>
              <v-row>
                <v-col cols="12">
                  <v-sheet height="100px" class="pa-4">Sales Graph Placeholder</v-sheet>
                </v-col>
                <v-col cols="12">
                  <v-sheet height="100px" class="pa-4">Popular Items Chart Placeholder</v-sheet>
                </v-col>
                <v-col cols="12">
                  <v-sheet height="100px" class="pa-4">Feedback Chart Placeholder</v-sheet>
                </v-col>
              </v-row>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      drawer: false,
      items: [
        { title: "Dashboard", icon: "mdi-view-dashboard" },
        { title: "Orders", icon: "mdi-package-variant" },
        { title: "Settings", icon: "mdi-cog" },
      ],
    };
  },
};
</script>

<style src="~/assets/css/dashboard.css"></style>
