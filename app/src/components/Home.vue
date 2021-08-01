<template>
    <span>   
        <!-- INPUT DATE -->
        <input-languages :language="language" :changeLanguage="changeLanguage"></input-languages>
        <!-- HEADER -->
        <header-vue>
            <span slot="image">
                <img src="@/assets/images/perfil.png" />
            </span>
            <span slot="principal">
                <h2>Thiago Studier</h2>
                <h3>{{titles.role}}</h3>
                <div class="info">
                    <div class="row-info">
                        <span class="info-title">{{titles.age}}:</span>
                        <span class="info-desc">23</span>
                    </div>
                    <div class="row-info">
                        <span class="info-title">{{titles.phone}}:</span>
                        <span class="info-desc">+55 (51) 99236-5609</span>
                    </div>
                    <div class="row-info">
                        <span class="info-title">{{titles.email}}:</span>
                        <span class="info-desc">thiago.studier9@gmail.com</span>
                    </div>
                </div>
                <span class="links">
                    <!-- FACEBOOK -->
                    <a class="link-icon" href="https://www.facebook.com/thiago.studier/" target="_blank" rel="noopener noreferrer"><i class="fab fa-facebook-f"></i></a>
                    <!-- INSTAGRAM -->
                    <a class="link-icon" href="https://www.instagram.com/thiagostudier/" target="_blank" rel="noopener noreferrer"><i class="fab fa-instagram"></i></a>
                    <!-- LINKEDIN -->
                    <a class="link-icon" href="https://www.linkedin.com/in/thiago-studier/" target="_blank" rel="noopener noreferrer"><i class="fab fa-linkedin-in"></i></a>
                    <!-- GITHUB -->
                    <a class="link-icon" href="https://github.com/thiagostudier" target="_blank" rel="noopener noreferrer"><i class="fab fa-github"></i></a>
                    <!-- BITBUCKET -->
                    <a class="link-icon" href="https://bitbucket.org/thiagostudier/" target="_blank" rel="noopener noreferrer"><i class="fab fa-bitbucket"></i></a>
                </span>
            </span>
        </header-vue>
        <section-content>
            <h3 class="subtitle" style="margin-top: 0px;">{{titles.education}}</h3>
            <timeline v-for="item in educations" :key="item.id">
                <span slot="university">{{item.university}}</span>
                <span slot="date">{{item.date}}</span>
                <span slot="course">{{item.course}}</span>
            </timeline>
        </section-content>
        <hr>
        <section-content>            
            <h3 class="subtitle">{{titles.experience}}</h3>
            <timeline v-for="item in experiences" :key="item.id">
                <span slot="university">{{item.company}}</span>
                <span slot="date">{{item.date}}</span>
                <span slot="course">{{item.role}}</span>
            </timeline>
        </section-content>
        <hr />
        <section-content>
            <h3 class="subtitle">{{titles.skills}}</h3>
            <grid-items columns="8" columns_tablet="4" columns_mobile="2">
                <skill-item>
                    <img src="@/assets/images/html-css-js.png" />
                    <span>HTML5, CSS3 e JS</span>
                </skill-item>
                <skill-item>
                    <img src="@/assets/images/vuejs.png" />
                    <span>VueJs</span>
                </skill-item>
                <skill-item>
                    <img src="@/assets/images/php.png" />
                    <span>PHP</span>
                </skill-item>
                <skill-item>
                    <img src="@/assets/images/laravel.png" />
                    <span>Laravel</span>
                </skill-item>
                <skill-item>
                    <img src="@/assets/images/mysql.png" />
                    <span>MySQL</span>
                </skill-item>
                <skill-item>
                    <img src="@/assets/images/react.png" />
                    <span>React</span>
                </skill-item>
                <skill-item>
                    <img src="@/assets/images/git.png" />
                    <span>Git</span>
                </skill-item>
                <skill-item>
                    <img src="@/assets/images/graphql.png" />
                    <span>GraphQL</span>
                </skill-item>
            </grid-items>
        </section-content>
        <hr />
        <section-content>
            <h3 class="subtitle">{{titles.projects}}</h3>
            <grid-items columns="3" columns_tablet="2" columns_mobile="1">
                <card-project v-for="item in projects" :key="item.title">
                    <span v-if="item.title" slot="title">{{item.title}}</span>
                    <span v-if="item.desc" slot="desc" v-html="item.desc"></span>
                    <span v-if="item.link" slot="link"><a :href="item.link" target="_blank" rel="noopener noreferrer">{{titles.view_projects}}</a></span>
                    <span v-if="item.link_github" slot="link-github"><a :href="item.link_github" target="_blank" rel="noopener noreferrer"><i class="fab fa-github"></i></a></span>
                    <span v-if="item.list" slot="list">{{item.list}}</span>
                </card-project>
            </grid-items>
        </section-content>
        <hr />
        <section-content>
            <h3 class="subtitle">{{titles.courses}}</h3>
            <timeline v-for="item in courses" :key="item.course">
                <span slot="university">{{item.university}}</span>
                <span slot="date">{{item.date}}</span>
                <span slot="course">{{item.course}}</span>
            </timeline>            
        </section-content>
        <hr />
        <section-content>
            <h3 class="subtitle">{{titles.languages}}</h3>
            <timeline v-for="item in courses_languages" :key="item.course">
                <span slot="university">{{item.university}}</span>
                <span slot="date">{{item.date}}</span>
                <span slot="course">{{item.course}}</span>
            </timeline>
        </section-content>
        <footer-vue>
            © 2021 • Thiago Studier
        </footer-vue>
    </span>
</template>

<script>

import HeaderVue from '@/components/includes/HeaderVue';
import SectionContent from '@/components/includes/SectionContent';
import Timeline from '@/components/includes/Timeline';
import SkillItem from '@/components/includes/SkillItem';
import GridItems from '@/components/includes/GridItems';
import CardProject from '@/components/includes/CardProject';
import FooterVue from '@/components/includes/FooterVue';
import InputLanguages from '@/components/includes/InputLanguages';
import { api } from '@/services/api.js';

export default {
    name: 'Home',
    components:{
        HeaderVue,
        SectionContent,
        Timeline,
        SkillItem,
        GridItems,
        CardProject,
        FooterVue,
        InputLanguages
    },
    data () {
        return {
            language: localStorage.getItem('language') == 'pt' ? 'pt' : 'en',
            titles: [],
            educations: [],
            experiences: [],
            projects: [],
            courses: [],
            courses_languages: []
        }
    },
    created(){
        console.log(localStorage.getItem('language'));
        this.getValues();
    },
    methods:{
        getValues(){
            // MÉTODO AXIOS - PEGAR INDICAÇÕES
            api.get(`/static/data.json`)
            .then(response => {
                this.titles = response.data[this.language].titles;
                this.educations = response.data[this.language].educations;
                this.experiences = response.data[this.language].experiences;
                this.projects = response.data[this.language].projects;
                this.courses = response.data[this.language].courses;
                this.courses_languages = response.data[this.language].courses_languages;
            })
            .catch(e => {
                // NOTIFICAÇÃO
                console.log('oi');
            });
        },
        changeLanguage(value){
            this.language = value;
            localStorage.setItem('language', value);
            this.getValues();
        }
    }
}
</script>