<template>
    <ResumeHeader />
    <div class="h-full flex flex-row-reverse grow text-sm">
        <div class="p-6 xl:p-8 grow text-slate-800">
            <h3 class="text-lg font-semibold text-slate-900">
                Experience
            </h3>

            <JobHeader
                company="Lurn Inc"
                title="Senior Full Stack Engineer"
                :active="[2017, 2022]"
                class="mt-4"
            />

            <ResponsibilityList class="mt-4">
                <ResponsibilityItem>
                    Worked on various platform features and projects from conception to launch, with an integral role in the
                    architectural design and implementation details.
                </ResponsibilityItem>

                <ResponsibilityItem>
                    Planned and implemented initiatives around code quality, standards, and automated testing, including
                    integrating automations into our build pipeline and commit hooks for both frontend and backend code.
                </ResponsibilityItem>

                <ResponsibilityItem>
                    Updated, expanded, and maintained several open source libraries that were previously out-of-date so we could
                    use them to support business operations.
                </ResponsibilityItem>

                <ResponsibilityItem>
                    Used New Relic and other debugging tools to find and fix performance issues on the platform and educated
                    developers on how to avoid and fix framework-specific performance pitfalls.
                </ResponsibilityItem>
            </ResponsibilityList>

            <JobHeader
                company="Ibex Data Services"
                title="Full Stack Engineer"
                :active="[2015, 2017]"
                class="mt-8"
            />

            <ResponsibilityList class="mt-4">
                <ResponsibilityItem>
                    Tasked with reducing the load time of webpages, often reducing the execution time of a script or database
                    queries from minutes to seconds.
                </ResponsibilityItem>

                <ResponsibilityItem>
                    Worked on a variety of projects, both as part of a team and as a solo developer, in multiple frameworks and
                    languages (PHP, Python).
                </ResponsibilityItem>

                <ResponsibilityItem>
                    Worked on projects that required the ability to deep-dive into third party source code to extend the
                    functionality of a Python CMS solution.
                </ResponsibilityItem>
            </ResponsibilityList>

            <JobHeader
                company="Independent Work"
                title="Full Stack Engineer"
                :active="[2010]"
                class="mt-8"
            />

            <ResponsibilityList class="mt-4">
                <ResponsibilityItem>
                    <a
                        href="https://soontm.com/calendar"
                        target="_blank"
                    >SoonTM.com</a>, a calendar for video games, has been an ongoing passion project of mine since 2017. I have
                    used it to hone my design skills and as a playground to learn and thrive in the web development field.
                </ResponsibilityItem>

                <ResponsibilityItem>
                    In 2013, I designed and implemented a customer management portal for Flying High In-Home Tutoring. It helped
                    to modernize the company's record keeping and gave tutors a direct connection to client information.
                </ResponsibilityItem>

                <ResponsibilityItem>
                    Worked on web projects for various clients as a freelance web developer mainly focused on delivering custom
                    themes for Wordpress websites.
                </ResponsibilityItem>
            </ResponsibilityList>
        </div>

        <div class="max-w-[17rem] w-full p-6 xl:p-8 bg-slate-200/75 text-slate-800">
            <p class="text-xs leading-relaxed">
                <span class="mr-1 font-medium text-sm tracking-wide">Hello!</span>
                I'm a full stack engineer from Virginia with over 10 years of experience delivering high quality software.
                I'm passionate about developer experience and writing code for humans, with a keen eye for the details.
            </p>

            <h3 class="mt-8 text-lg font-semibold text-slate-900">
                Tech Toolbelt
            </h3>

            <ToolList
                :items="['PHP', 'Javascript', 'Typescript', 'SQL', 'Python', 'Ruby', 'Go']"
                title="Languages"
                class="mt-4"
            />

            <ToolList
                :items="['Laravel', 'Codeigniter', 'Vue.js', 'InertiaJS', 'Ruby on Rails', 'Tailwind CSS', 'Less', 'SCSS']"
                title="Features &amp; Abstractions"
                etc
                class="mt-6"
            />

            <ToolList
                :items="['AWS (S3, EC2, ALB, Cloudwatch, DynamoDB, Lambda)', 'Docker', 'Vagrant', 'Nginx', 'Apache', 'New Relic', 'Storybook']"
                title="Tools &amp; Services"
                etc
                class="mt-6"
            />
        </div>
    </div>
</template>

<script setup>
import JobHeader from './components/JobHeader.vue'
import ResumeHeader from './components/ResumeHeader.vue'
import ResponsibilityList from './components/ResponsibilityList.vue'
import ResponsibilityItem from './components/ResponsibilityItem.vue'
import ToolList from './components/ToolList.vue'
</script>
