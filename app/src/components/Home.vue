<template>
    <span>   
        <!-- HEADER -->
        <header-vue>
            <span slot="image">
                <img src="@/assets/perfil.jpg" />
            </span>
            <span slot="principal">
                <h2>Thiago Studier</h2>
                <h3>fullstack developer</h3>
                <div class="info">
                    <div class="row-info">
                        <span class="info-title">Age:</span>
                        <span class="info-desc">23</span>
                    </div>
                    <div class="row-info">
                        <span class="info-title">Phone:</span>
                        <span class="info-desc">+55 (51) 99236-5609</span>
                    </div>
                    <div class="row-info">
                        <span class="info-title">EMAIL:</span>
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
        <!-- INTRODUÇÃO -->
        <section-content>
            <h2 class="title">Introdução</h2>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptate quidem ab explicabo pariatur molestias facilis, et impedit suscipit doloremque dolor obcaecati soluta, necessitatibus quo architecto vitae animi accusantium voluptates fugit.</p>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptate quidem ab explicabo pariatur molestias facilis, et impedit suscipit doloremque dolor obcaecati soluta, necessitatibus quo architecto vitae animi accusantium voluptates fugit.</p>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptate quidem ab explicabo pariatur molestias facilis, et impedit suscipit doloremque dolor obcaecati soluta, necessitatibus quo architecto vitae animi accusantium voluptates fugit.</p>
        </section-content>
        <hr>
        <section-content>
            <h3 class="subtitle" style="margin-top: 0px;">Educação</h3>
            <timeline>
                <span slot="university">Uniritter Canoas</span>
                <span slot="date">2016 - 2020</span>
                <span slot="course">Tecnólogo em Análise e Desenvolvimento de Sistemas</span>
            </timeline>
            <timeline>
                <span slot="university">QI Escolas e Faculdades</span>
                <span slot="date">2015 - 2016</span>
                <span slot="course">Técnico em Informática</span>
            </timeline>
            <timeline>
                <span slot="university">La Salle Niterói</span>
                <span slot="date">2011 - 2014</span>
                <span slot="course">Ensino médio</span>
            </timeline>            
        </section-content>
        <hr>
        <section-content>            
            <h3 class="subtitle">Experiência</h3>
            <timeline>
                <span slot="university">Hospital Moinhos de Vento</span>
                <span slot="date">desde 10/2020</span>
                <span slot="course">Desenvolvedor II</span>
            </timeline>
            <timeline>
                <span slot="university">Hospital Moinhos de Vento</span>
                <span slot="date">05/2018 - 10/2020</span>
                <span slot="course">Desenvolvedor I</span>
            </timeline>
            <timeline>
                <span slot="university">Hospital Moinhos de Vento</span>
                <span slot="date">04/2017 - 05/2018</span>
                <span slot="course">Estagiário</span>
            </timeline>
        </section-content>
        <hr />
        <section-content>
            <h3 class="subtitle">Skills</h3>
            <grid-items columns="7" columns_mobile="2">
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
            </grid-items>
        </section-content>
        <hr />
        <section-content>
            <h3 class="subtitle">Projetos</h3>
            <grid-items columns="3" columns_mobile="1">
                <card-project>
                    <span slot="image"><img src="@/assets/images/sistema-de-selecao.png" /></span>
                    <span slot="title">Site | Thiago Studier</span>
                    <span slot="desc">Projeto de portifólio/currículo para apresentar minhas habilidades, experiências, formação e etc.</span>
                    <span slot="link"><a href="http://www.thiagostudier.com.br" target="_blank" rel="noopener noreferrer">Visualizar projeto</a></span>
                    <span slot="link-github"><a href="https://github.com/thiagostudier/thiago-studier" target="_blank" rel="noopener noreferrer"><i class="fab fa-github"></i></a></span>
                    <span slot="list">VueJs, HTML, CSS</span>
                </card-project>
                <card-project>
                    <span slot="image"><img src="@/assets/images/sistema-de-selecao.png" /></span>
                    <span slot="title">Move It</span>
                    <span slot="desc">O projeto alerta o usuário para fazer um intervalo no seu trabalho e fazer um exercício para o corpo ou para os olhos. Ao realizar essa atividade, o usuário ganha XP.</span>
                    <span slot="link"><a href="https://moveit-five-beta.vercel.app/" target="_blank" rel="noopener noreferrer">Visualizar projeto</a></span>
                    <span slot="link-github"><a href="https://github.com/thiagostudier/moveit-nlw" target="_blank" rel="noopener noreferrer"><i class="fab fa-github"></i></a></span>
                    <span slot="list">React, Next.js, HTML, CSS</span>
                </card-project>
                <card-project>
                    <span slot="image"><img src="@/assets/images/sistema-de-selecao.png" /></span>
                    <span slot="title">Sistema de seleção</span>
                    <span slot="desc">Aplicação desenvolvida no Hospital Moinhos de Vento.<br />Sistema que possibilita aos administradores da aplicação criarem seleções/editais para captação de público.</span>
                    <span slot="link"><a href="https://responsabilidadesocial.hospitalmoinhos.org.br/" target="_blank" rel="noopener noreferrer">Visualizar projeto</a></span>
                    <span slot="list">Laravel, PHP, HTML, CSS, JS, Bootstrap, JS, MySQL</span>
                </card-project>
                <card-project>
                    <span slot="image"><img src="@/assets/images/sistema-de-selecao.png" /></span>
                    <span slot="title">AdotaPets</span>
                    <span slot="desc">Aplicação que permite que ONGs possam divulgar seus pets que estão para adoção.</span>
                    <span slot="link"><a href="http://adotapets.com.br/" target="_blank" rel="noopener noreferrer">Visualizar projeto</a></span>
                    <span slot="list">PHP, HTML, CSS, JS, Bootstrap, JS, MySQL</span>
                </card-project>
                <card-project>
                    <span slot="image"><img src="@/assets/images/sistema-de-selecao.png" /></span>
                    <span slot="title">Faculdade Moinhos</span>
                    <span slot="desc">Aplicação desenvolvida no Hospital Moinhos de Vento.</span>
                    <span slot="link"><a href="http://faculdademoinhos.com.br/" target="_blank" rel="noopener noreferrer">Visualizar projeto</a></span>
                    <span slot="list">PHP, HTML, CSS, JS, Bootstrap, JS, MySQL</span>
                </card-project>
                <card-project>
                    <span slot="image"><img src="@/assets/images/sistema-de-selecao.png" /></span>
                    <span slot="title">Healthcare Alliance</span>
                    <span slot="desc">Projeto desenvolvido para uma empresa (freelancer). <br />Foi fornecido o layout em psd, e a entrega foram os arquivos em html. <br />Layout adaptado para responsivo.</span>
                    <span slot="link"><a href="https://healthcare.vercel.app/" target="_blank" rel="noopener noreferrer">Visualizar projeto</a></span>
                    <span slot="link-github"><a href="https://github.com/thiagostudier/healthcare-alliance" target="_blank" rel="noopener noreferrer"><i class="fab fa-github"></i></a></span>
                    <span slot="list">HTML, CSS, Bootstrap, JS, Jquery</span>
                </card-project>
            </grid-items>
        </section-content>
        <hr />
        <section-content>
            <h3 class="subtitle">Cursos de extensão</h3>
            <timeline>
                <span slot="university">Rockeatseat</span>
                <span slot="date">02/2021</span>
                <span slot="course">Next Level Week #4</span>
            </timeline>
            <timeline>
                <span slot="university">Udemy</span>
                <span slot="date">02/2021</span>
                <span slot="course">SPA com Vue js e Api com Laravel</span>
            </timeline>
            <timeline>
                <span slot="university">School of Net</span>
                <span slot="date">01/2021</span>
                <span slot="course">Iniciando com MongoDB</span>
            </timeline>
            <timeline>
                <span slot="university">School of Net</span>
                <span slot="date">01/2021</span>
                <span slot="course">Node com Express.js</span>
            </timeline>
            <timeline>
                <span slot="university">School of Net</span>
                <span slot="date">01/2021</span>
                <span slot="course">Node básico</span>
            </timeline>
            <timeline>
                <span slot="university">School of Net</span>
                <span slot="date">04/2020</span>
                <span slot="course">Criando um fórum real-time com Laravel</span>
            </timeline>
             <timeline>
                <span slot="university">School of Net</span>
                <span slot="date">01/2020</span>
                <span slot="course">Javascript avançado</span>
            </timeline>
            <timeline>
                <span slot="university">School of Net</span>
                <span slot="date">10/2019</span>
                <span slot="course">PHP Avançado com OO</span>
            </timeline>
            <timeline>
                <span slot="university">School of Net</span>
                <span slot="date">10/2019</span>
                <span slot="course">Composer</span>
            </timeline>
            <timeline>
                <span slot="university">School of Net</span>
                <span slot="date">07/2019</span>
                <span slot="course">Criando um site administrável com PHP</span>
            </timeline>
            <timeline>
                <span slot="university">School of Net</span>
                <span slot="date">07/2019</span>
                <span slot="course">Avançando com PHP e Mysql</span>
            </timeline>
            <timeline>
                <span slot="university">Udemy</span>
                <span slot="date">02/2018</span>
                <span slot="course">PHP with Laravel for beginners - Become a Master in Laravel</span>
            </timeline>
            <timeline>
                <span slot="university">Udemy</span>
                <span slot="date">09/2017</span>
                <span slot="course">Curso Completo de Desenvolvimento Web</span>
            </timeline>
        </section-content>
        <hr />
        <section-content>
            <h3 class="subtitle">Idiomas</h3>
            <grid-items columns="7" columns_mobile="1">
                <skill-item>
                    <img src="@/assets/images/portugues.png" />
                    <span>Português - Nativo</span>
                </skill-item>
                <skill-item>
                    <img src="@/assets/images/ingles.png" />
                    <span>Inglês - Intermediário</span>
                </skill-item>
                <skill-item>
                    <img src="@/assets/images/frances.png" />
                    <span>Francês - Básico</span>
                </skill-item>
            </grid-items>
            <br />
            <timeline>
                <span slot="university">English Live</span>
                <span slot="date">desde 03/2021</span>
                <span slot="course">Curso Básico de Inglês - Básico 4</span>
            </timeline>
            <timeline>
                <span slot="university">Duoling</span>
                <span slot="date">desde 01/2021</span>
                <span slot="course">Inglês</span>
            </timeline>
            <timeline>
                <span slot="university">Duoling</span>
                <span slot="date">desde 01/2021</span>
                <span slot="course">Francês</span>
            </timeline>
            <timeline>
                <span slot="university">Lincoln Idiomas</span>
                <span slot="date">2013</span>
                <span slot="course">Curso Básico de Inglês</span>
            </timeline>
        </section-content>
        <footer-vue>
            © 2021 • Todos os direitos reservador • Thiago Studier
        </footer-vue>
    </span>
</template>

<script>

import HeaderVue from '@/components/includes/HeaderVue';
import SectionContent from '@/components/includes/SectionContent';
import Timeline from '@/components/includes/Timeline.vue';
import SkillItem from '@/components/includes/SkillItem.vue';
import GridItems from '@/components/includes/GridItems.vue';
import CardProject from '@/components/includes/CardProject.vue';
import FooterVue from '@/components/includes/FooterVue.vue';

export default {
    name: 'Home',
    components:{
        HeaderVue,
        SectionContent,
        Timeline,
        SkillItem,
        GridItems,
        CardProject,
        FooterVue
    },
    data () {
        return {
      
        }
    }
}
</script>

<style scoped>
</style>
