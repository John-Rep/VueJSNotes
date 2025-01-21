<script lang="ts" setup>
import Card from "../components/layouts/CardView.vue"
import Annonce from "../components/layouts/AnnouncementView.vue"
import TrendCard from "../components/layouts/TrendingView.vue"
import type { Project } from "@/models/project"
import type { Announcement } from "@/models/announcement"
import type { Trend } from "@/models/trend"
const projectsData: Project[] = [
  { title: 'Super Cool Project', content: 'Lorem ipsum dolor sit amet, officia excepteur ex fugiat reprehenderit enim labore culpa sint ad nisi Lorem pariatur mollit ex esse exercitation amet. Nisi anim cupidatat Lorem ipsum dolor sit amet, officia excepteur ex fugiat reprehenderit enim labore culpa sint ad nisi Lorem pariatur mollit ex esse exercitation amet. Nisi anim cupidatat' },
  { title: 'Super Cool Project', content: 'Lorem ipsum dolor sit amet, officia excepteur ex fugiat reprehenderit enim labore culpa sint ad nisi Lorem pariatur mollit ex esse exercitation amet. Nisi anim cupidatat Lorem ipsum dolor sit amet, officia excepteur ex fugiat reprehenderit enim labore culpa sint ad nisi Lorem pariatur mollit ex esse exercitation amet. Nisi anim cupidatat' },
  { title: 'Super Cool Project', content: 'Lorem ipsum dolor sit amet, officia excepteur ex fugiat reprehenderit enim labore culpa sint ad nisi Lorem pariatur mollit ex esse exercitation amet. Nisi anim cupidatat Lorem ipsum dolor sit amet, officia excepteur ex fugiat reprehenderit enim labore culpa sint ad nisi Lorem pariatur mollit ex esse exercitation amet. Nisi anim cupidatat' },
  { title: 'Super Cool Project', content: 'Lorem ipsum dolor sit amet, officia excepteur ex fugiat reprehenderit enim labore culpa sint ad nisi Lorem pariatur mollit ex esse exercitation amet. Nisi anim cupidatat Lorem ipsum dolor sit amet, officia excepteur ex fugiat reprehenderit enim labore culpa sint ad nisi Lorem pariatur mollit ex esse exercitation amet. Nisi anim cupidatat' },
  { title: 'Super Cool Project', content: 'Lorem ipsum dolor sit amet, officia excepteur ex fugiat reprehenderit enim labore culpa sint ad nisi Lorem pariatur mollit ex esse exercitation amet. Nisi anim cupidatat Lorem ipsum dolor sit amet, officia excepteur ex fugiat reprehenderit enim labore culpa sint ad nisi Lorem pariatur mollit ex esse exercitation amet. Nisi anim cupidatat' },
  { title: 'Super Cool Project', content: 'Lorem ipsum dolor sit amet, officia excepteur ex fugiat reprehenderit enim labore culpa sint ad nisi Lorem pariatur mollit ex esse exercitation amet. Nisi anim cupidatat Lorem ipsum dolor sit amet, officia excepteur ex fugiat reprehenderit enim labore culpa sint ad nisi Lorem pariatur mollit ex esse exercitation amet. Nisi anim cupidatat' },
]
const announcementsData: Announcement[] = [
  { title: 'Site Maintenance', content: 'Lorem ipsum dolor sit amet, officia excepteur ex fugiat reprehenderit enim labore culpa sint ad nisi Lorem pariatur mollit ex esse exercitation amet. Nisi anim cupidatat Lorem ipsum dolor sit amet, officia excepteur ex fugiat reprehenderit enim labore culpa sint ad nisi Lorem pariatur mollit ex esse exercitation amet. Nisi anim cupidatat' },
  { title: 'Community Share Day', content: 'Lorem ipsum dolor sit amet, officia excepteur ex fugiat reprehenderit enim labore culpa sint ad nisi Lorem pariatur mollit ex esse exercitation amet. Nisi anim cupidatat Lorem ipsum dolor sit amet, officia excepteur ex fugiat reprehenderit enim labore culpa sint ad nisi Lorem pariatur mollit ex esse exercitation amet. Nisi anim cupidatat' },
  { title: 'Updated Privacy Policy', content: 'Lorem ipsum dolor sit amet, officia excepteur ex fugiat reprehenderit enim labore culpa sint ad nisi Lorem pariatur mollit ex esse exercitation amet. Nisi anim cupidatat Lorem ipsum dolor sit amet, officia excepteur ex fugiat reprehenderit enim labore culpa sint ad nisi Lorem pariatur mollit ex esse exercitation amet. Nisi anim cupidatat' },
]
const trendData: Trend[] = [
  { name: "@tegan", title: "World Peace Builder", image: "https://robohash.org/irwi32.png?set=set4"},
  { name: "@morgan", title: "Super Cool Project", image: "https://robohash.org/ijrwi32.png?set=set4"},
  { name: "@kindall", title: "Life Changing App", image: "https://robohash.org/irw2.png?set=set4"},
  { name: "@alex", title: "No Traffic Maker", image: "https://robohash.org/ireqwe2.png?set=set4"},
]
</script>
<template>
<div class="container project-box">
        <section class="dashboard">
          <div class="project">
            <h4>Your Projects</h4>
            <div class="project-grid">
              <span v-for="(project) in projectsData">
                <Card :project="project"/>
              </span>
            </div>
          </div>
          <section class="side">
            <div class="announcement">
              <h4>Announcements</h4>
              <div class="background-box">
                <span v-for="(announcement) in announcementsData">
                  <Annonce :announcement="announcement"/>
                  <hr />
                </span>
              </div>
            </div>
            <div>
              <h4>Trending</h4>
              <div class="background-box trending">
                <span v-for="(trend) in trendData">
                  <TrendCard :trend="trend"/>
                </span>
              </div>
            </div>
          </section>
        </section>
      </div>
</template>
<style></style>