<template>
    <section class="container">
        <h2 id="work-history">
            <a href="#work-history">Work History</a>
        </h2>

        <section>
            <h3>
                <span><time datetime="2023">2023</time> - <time datetime="2025">2025</time> </span>
                <br />
                ExxonMobil
            </h3>

            <h4>Salesforce Analyst and Developer (Sales and Marketing IT)</h4>

            <p>
                As a
                <a
                    href="https://www.salesforce.com/products/what-is-salesforce/"
                    target="_blank"
                    rel="noopener noreferrer"
                >
                    Salesforce
                </a>
                Analyst and Developer for
                <a
                    href="https://corporate.exxonmobil.com/locations/brazil"
                    target="_blank"
                    rel="noopener noreferrer"
                >
                    ExxonMobil </a
                >, I had the privilege to work in different Salesforce orgs and projects. I
                developed solutions for both the Fuels and Lubricants Value Chains. Some of the
                technologies I worked with are:
            </p>

            <ul>
                <li>Sales Cloud</li>
                <li>Service Cloud</li>
                <li>Field Service</li>
                <li>Flosum</li>
            </ul>

            <p>
                I brought awareness to the Analyst teams about both Salesforce's
                <strong>Lightning Design System</strong>, which should be followed for solutions
                that are displayed directly in the system, and <strong>Developer Tooling</strong>,
                which helps developers write readable quality code.
            </p>

            <p>
                By the end of my time in this role, I was the go-to reference for many of the
                development-related questions our analysts and developers had. From tool
                configuration in their machines, which is company specific due to a lot of security
                controls, to connection to external APIs, either company owned or from vendors, such
                as Medallia.
            </p>

            <p>
                I was both instructor and designer for a Salesforce-related learning initiative we
                had internally. <strong>Salesforce Academy</strong> is a face-to-face course
                covering content from Trailhead's Admin Beginner and Intermediate modules bringing
                technical challenges and examples from the actual internal Salesforce Orgs.
            </p>

            <p>
                During all these years in the company, I was part of a committee composed by Design
                enthusiasts, who research and develop communication and souvenirs for local events
                and other committees. The committee was called <strong>Agência Criativa</strong>, or
                Creative Agency. We made Visual Identities, Website Prototypes, Souvenirs, Totems,
                Stickers and more.
            </p>
        </section>

        <section>
            <h3>
                <span><time datetime="2022">2022</time> - <time datetime="2023">2023</time> </span>
                <br />
                ExxonMobil
            </h3>

            <h4>Trainee (DBAM Automation)</h4>

            <p>
                As a trainee, I worked as a Full Stack Web Developer on a team dedicated to Database
                Management Automation. The team's main product is a portal offering different
                resources and applications to DBAs, such as Health Check and Server Mapping.
            </p>

            <p>
                Managed a few internal Packages for Web Development, most notably a
                <a href="https://vuejs.org/" target="_blank" rel="noopener noreferrer">Vue</a>
                Component Library based on the company's Design System and a helper for the
                <strong>Sharepoint REST API</strong>, which helps a lot with smaller projects
                (especially those from organizations that lack the development experience).
            </p>

            <p>
                I was also part of different initiatives inside the company, helping internal
                committees with their email communications and web development, both as a developer,
                designer and consultant.
            </p>
        </section>
    </section>
</template>

<style scoped>
h3 > span {
    font-size: 1rem;
    color: var(--color-umber);
}

h3:has(span) {
    line-height: 1;
}

h4 {
    color: var(--color-primary);
}

ul {
    list-style-type: square;
    margin-bottom: 1rem;
}

li::marker {
    color: var(--color-primary);
}
</style>
