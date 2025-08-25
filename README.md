# Dohyun
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Your Story to a Sales Machine</title>
    <style>
        :root {
            --primary-bg: #121212;
            --secondary-bg: #1e1e1e;
            --text-color: #e0e0e0;
            --accent-color: #ff5722;
            --button-hover: #e64a19;
            --divider-color: #333;
            --border-radius: 8px;
            --font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol";
        }

        /* CSS Reset and Normalization */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html, body {
            font-family: var(--font-family);
            background-color: var(--primary-bg);
            color: var(--text-color);
            line-height: 1.6;
            overflow-x: hidden;
            width: 100%;
        }

        .container {
            width: 100%;
            max-width: 900px;
            margin: 0 auto;
            padding: 0 1rem;
        }

        h1, h2, h3, h4, h5, h6 {
            color: var(--text-color);
            line-height: 1.2;
            margin-bottom: 0.5em;
        }

        p {
            margin-bottom: 1em;
            font-size: 1.1rem;
        }
        
        strong, b {
            font-weight: 700;
        }

        em {
            font-style: italic;
        }

        a {
            color: var(--accent-color);
            text-decoration: none;
            transition: color 0.3s ease;
        }

        a:hover {
            color: var(--button-hover);
        }

        .text-center {
            text-align: center;
        }

        /* Utility classes for styling */
        .section {
            padding: 4rem 0;
            border-bottom: 1px solid var(--divider-color);
        }

        .hero-section {
            padding: 6rem 0;
            text-align: center;
        }

        .preheader {
            font-size: 1rem;
            text-transform: uppercase;
            letter-spacing: 2px;
            color: var(--accent-color);
            font-weight: 600;
            margin-bottom: 1rem;
        }

        .hero-header {
            font-size: clamp(2rem, 6vw, 4rem);
            font-weight: 800;
            margin-bottom: 0.5rem;
        }

        .hero-subheader {
            font-size: clamp(1.25rem, 3vw, 1.75rem);
            font-weight: 400;
            max-width: 700px;
            margin: 0 auto 2rem;
        }

        .vsl-container {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            gap: 0.75rem;
            cursor: pointer;
            margin-bottom: 2rem;
            position: relative;
        }

        .vsl-icon {
            width: 100%;
            max-width: 650px;
            aspect-ratio: 16/9;
            background-color: var(--secondary-bg);
            border: 2px solid var(--divider-color);
            border-radius: var(--border-radius);
            position: relative;
            display: flex;
            justify-content: center;
            align-items: center;
            transition: transform 0.3s ease;
        }

        .vsl-icon:hover {
            transform: scale(1.02);
        }
        
        .play-button {
            width: 70px;
            height: 70px;
            background-color: rgba(255, 255, 255, 0.2);
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            backdrop-filter: blur(10px);
            -webkit-backdrop-filter: blur(10px);
        }
        
        .play-button::after {
            content: '';
            width: 0;
            height: 0;
            border-top: 15px solid transparent;
            border-bottom: 15px solid transparent;
            border-left: 20px solid var(--text-color);
            margin-left: 5px;
        }
        
        .cta-text {
            font-size: 1rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            color: var(--text-color);
            font-weight: 600;
        }

        .cta-button {
            display: inline-block;
            background-color: var(--accent-color);
            color: var(--primary-bg);
            padding: 1rem 2rem;
            font-size: 1.25rem;
            font-weight: 700;
            border-radius: 50px;
            transition: background-color 0.3s ease, transform 0.3s ease;
            text-align: center;
        }

        .cta-button:hover {
            background-color: var(--button-hover);
            transform: translateY(-2px);
        }
        
        .subtle-text {
            font-size: 0.9rem;
            margin-top: 1rem;
            color: #888;
        }

        /* Problem Section */
        .problem-section {
            background-color: var(--secondary-bg);
        }
        
        .problem-container {
            width: 100%;
            max-width: 700px;
            margin: 0 auto;
        }

        .problem-container h2 {
            font-size: clamp(1.5rem, 4vw, 2.5rem);
            text-align: center;
            margin-bottom: 2rem;
        }
        
        .problem-list {
            list-style: none;
        }

        .problem-list li {
            font-size: 1.15rem;
            line-height: 1.6;
            margin-bottom: 1.5rem;
            position: relative;
            padding-left: 1.5em;
        }
        
        .problem-list li::before {
            content: '•';
            color: var(--accent-color);
            font-size: 1.5em;
            position: absolute;
            left: 0;
            top: -0.1em;
        }

        /* Story Section */
        .story-section {
            background-color: var(--primary-bg);
        }

        /* Solution Section */
        .solution-section {
            background-color: var(--secondary-bg);
        }

        .solution-section h2 {
            font-size: clamp(1.5rem, 4vw, 2.5rem);
            text-align: center;
            margin-bottom: 2rem;
        }

        .solution-grid {
            display: grid;
            gap: 2rem;
            grid-template-columns: 1fr;
        }
        
        @media (min-width: 768px) {
            .solution-grid {
                grid-template-columns: repeat(2, 1fr);
            }
        }
        
        .solution-card {
            background-color: var(--primary-bg);
            padding: 2rem;
            border-radius: var(--border-radius);
            text-align: center;
        }

        .solution-card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
        }

        .solution-card p {
            font-size: 1rem;
        }
        
        .benefit-list {
            list-style: none;
            text-align: left;
            margin-top: 2rem;
        }

        .benefit-list li {
            background-color: var(--primary-bg);
            padding: 1rem;
            border-radius: var(--border-radius);
            margin-bottom: 1rem;
            border-left: 4px solid var(--accent-color);
        }

        .benefit-list li strong {
            display: block;
            margin-bottom: 0.5em;
            font-size: 1.15rem;
        }

        /* Offer Section */
        .offer-section {
            background-color: var(--primary-bg);
        }
        
        .offer-container {
            width: 100%;
            max-width: 700px;
            margin: 0 auto;
        }

        .offer-container h2 {
            font-size: clamp(1.5rem, 4vw, 2.5rem);
            text-align: center;
            margin-bottom: 2rem;
        }
        
        .offer-cards {
            display: flex;
            flex-direction: column;
            gap: 1.5rem;
        }
        
        @media (min-width: 768px) {
            .offer-cards {
                flex-direction: row;
            }
        }

        .offer-card {
            background-color: var(--secondary-bg);
            border-radius: var(--border-radius);
            padding: 2.5rem;
            text-align: center;
            flex: 1;
            border: 2px solid transparent;
            transition: border-color 0.3s ease;
        }
        
        .offer-card:hover {
            border-color: var(--accent-color);
        }

        .offer-card h3 {
            font-size: 1.75rem;
            color: var(--accent-color);
            margin-bottom: 0.5rem;
        }
        
        .offer-card .price {
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 0.5rem;
        }
        
        .offer-card .period {
            font-size: 1rem;
            color: #888;
            display: block;
            margin-bottom: 1.5rem;
        }

        .offer-list {
            list-style: none;
            text-align: left;
            margin-bottom: 2rem;
        }

        .offer-list li {
            margin-bottom: 0.75rem;
            position: relative;
            padding-left: 1.5em;
            font-size: 1rem;
        }
        
        .offer-list li::before {
            content: '✓';
            color: var(--accent-color);
            position: absolute;
            left: 0;
            font-weight: bold;
        }

        /* CTA section */
        .cta-section {
            background-color: var(--accent-color);
            padding: 4rem 1rem;
            text-align: center;
            color: var(--primary-bg);
            border-radius: var(--border-radius);
        }
        
        .cta-section h2 {
            color: var(--primary-bg);
            font-size: clamp(1.5rem, 4vw, 2.5rem);
            margin-bottom: 1rem;
        }
        
        .cta-section p {
            font-size: 1.25rem;
            max-width: 600px;
            margin: 0 auto 2rem;
            color: rgba(0,0,0,0.8);
        }
        
        .cta-section .cta-button {
            background-color: var(--primary-bg);
            color: var(--accent-color);
            font-size: 1.5rem;
            padding: 1.25rem 2.5rem;
        }
        
        .cta-section .cta-button:hover {
            background-color: #333;
            color: #fff;
        }
        
        /* FAQ Section */
        .faq-section {
            background-color: var(--primary-bg);
        }
        
        .faq-section h2 {
            font-size: clamp(1.5rem, 4vw, 2.5rem);
            text-align: center;
            margin-bottom: 2rem;
        }
        
        .faq-item {
            background-color: var(--secondary-bg);
            border-radius: var(--border-radius);
            padding: 1.5rem;
            margin-bottom: 1rem;
        }
        
        .faq-question {
            font-size: 1.25rem;
            font-weight: 600;
            margin-bottom: 0.75rem;
        }

        /* Footer */
        .footer {
            text-align: center;
            padding: 2rem 0;
            font-size: 0.9rem;
            color: #666;
            border-top: 1px solid var(--divider-color);
        }

        @media (max-width: 768px) {
            .section {
                padding: 3rem 0;
            }
        }
    </style>
</head>
<body>
    
    <header class="hero-section">
        <div class="container">
            <p class="preheader">For the Aspiring SaaS Creator</p>
            <h1 class="hero-header">Turn Your Idea Into An App That Makes You Money… In 20 Days.</h1>
            <p class="hero-subheader">…Without wasting years figuring it all out alone or paying a developer a fortune.</p>
            
            <a href="https://docs.google.com/document/d/16BGvfUQ2HCK-Ro2146yZTtvY6K5NR3nWXXyGy-U4xb8/edit?usp=sharing" target="_blank" class="vsl-container">
                <div class="vsl-icon">
                    <div class="play-button"></div>
                </div>
                <div class="cta-text">Click Here To See The: VSL I WROTE FOR YOU</div>
            </a>
            
            <a href="#offer" class="cta-button">Secure Your Spot</a>
        </div>
    </header>

    <section class="section problem-section">
        <div class="container problem-container">
            <h2>The silent frustration of building something you can't sell.</h2>
            <p>You’ve seen people do it. A simple idea, a weekend project, and then suddenly… they’re making a few hundred, maybe even a few thousand dollars a month. It looks easy from the outside. So you started building, too.</p>
            <p>You downloaded tutorials. You bought a few online courses. You spent late nights coding, trying to make sense of documentation, and piecing together forums... </p>
            <p>But every time you get close to launching, you hit a wall.</p>
            <ul class="problem-list">
                <li>You feel stuck, staring at your code, with a gut feeling that something is broken—but you don’t even know what questions to ask.</li>
                <li>You get overwhelmed, paralyzed by a thousand decisions on what to build next, which feature to add, or how to even get your first user.</li>
                <li>The real fear? You finish the app… you get it live… and then nothing happens. No users. No revenue. Just the sound of crickets after all that work.</li>
            </ul>
            <p>It’s a lonely place to be. You're smart. You're resourceful. But you feel like you’re on a rudderless boat, just waiting for the storm to hit. And it's costing you more than just time... it's costing you the confidence that you can actually do this.</p>
        </div>
    </section>

    <section class="section story-section">
        <div class="container">
            <h2>How I went from "stuck" to shipping 13 apps that made money.</h2>
            <p>Look, I'm not a tech guru. I'm just a normal guy who's been through the same struggles you're going through now. I spent years on the sidelines, trying to get my first app off the ground. I bought the courses. I watched the YouTube videos. I read all the "how-to" blogs.</p>
            <p>I built a handful of projects that never saw the light of day. They just sat there, unfinished, a constant reminder of what I couldn’t quite finish.</p>
            <p>The biggest problem wasn't my coding skill. It was the lack of a clear path. The free content is a mile wide and an inch deep. The courses are too generic. They teach you to build <em>their</em> project, but they don't teach you how to build <em>yours</em>.</p>
            <p>And when you get stuck, you're on your own.</p>
            <p>I realized I needed more than just information. I needed a co-pilot. Someone who could look at <strong>my</strong> specific roadblocks, call out my blind spots, and show me the fastest path forward. I needed someone who had already done it. Not a "millionaire expert," just a normal guy who had shipped apps that people actually used.</p>
            <p>So I created the support system I wish I had back then.</p>
        </div>
    </section>

    <section class="section solution-section">
        <div class="container">
            <h2>The solution isn't another course. It’s a coach.</h2>
            <p>My method is simple. It's not a framework or a 10-step process. It’s personalized, 1:1 guidance from someone who has shipped 13+ apps—four of which have made over $1,000/mo at their peak.</p>
            <p>I give you the exact, tailored feedback you need, when you need it.</p>
            <div class="solution-grid">
                <div class="solution-card">
                    <h3>Stop Guessing, Start Building</h3>
                    <p>Instead of trying to find the answer on Stack Overflow, you ask me directly. No more hours lost to Google searches. Just a quick message and a clear path forward.</p>
                </div>
                <div class="solution-card">
                    <h3>Launch With Confidence</h3>
                    <p>We'll work together to define your minimal viable product (MVP), so you know exactly what to build, and more importantly, what NOT to build. You'll launch with purpose, not just hope.</p>
                </div>
                <div class="solution-card">
                    <h3>Find Your First Users</h3>
                    <p>Most developers neglect marketing. We'll find a social media growth strategy that works for you, so your app gets seen by real people, not just your friends and family.</p>
                </div>
                <div class="solution-card">
                    <h3>Get Unstuck, Instantly</h3>
                    <p>When you hit a bug or a mental block, you won't have to wait. With unlimited messaging on Discord, you get quick feedback and solutions, so you can keep your momentum.</p>
                </div>
            </div>
            
            <ul class="benefit-list">
                <li>
                    <strong>Get Direct Access To Me.</strong>
                    My personal Discord inbox is open to you. This is where you get unlimited, on-the-spot support so you never feel alone or stuck again.
                </li>
                <li>
                    <strong>Launch a Viable App.</strong>
                    You'll learn to build an app that users actually want, not just what you think they want. This leads to a higher chance of success and real revenue.
                </li>
                <li>
                    <strong>Find Your First Paying Customers.</strong>
                    You'll get an action plan for marketing your app on social media, so you can build a community and see your first sign-ups.
                </li>
            </ul>
        </div>
    </section>

    <section class="section offer-section" id="offer">
        <div class="container offer-container">
            <h2>Here’s what our coaching looks like.</h2>
            <p>Choose the option that best fits where you are right now. Both are designed to get you moving quickly and confidently.</p>
            
            <div class="offer-cards">
                <div class="offer-card">
                    <h3>One-Time Deep Dive</h3>
                    <p class="price">$299</p>
                    <p class="period">For a 1-Hour Call</p>
                    <ul class="offer-list">
                        <li>1-hour personalized video call</li>
                        <li>Ask me anything about your idea, code, or marketing</li>
                        <li>Get a custom action plan for the next 30 days</li>
                        <li>No long-term commitment</li>
                    </ul>
                    <a href="#" class="cta-button">Book a Call</a>
                </div>

                <div class="offer-card">
                    <h3>Ongoing Monthly Support</h3>
                    <p class="price">$499</p>
                    <p class="period">Per Month</p>
                    <ul class="offer-list">
                        <li>4 one-hour calls per month</li>
                        <li>Unlimited 1:1 Discord messaging support</li>
                        <li>Continuous feedback on your progress</li>
                        <li>Accountability and guidance through every stage</li>
                    </ul>
                    <a href="#" class="cta-button">Join Now</a>
                </div>
            </div>
            <p class="subtle-text text-center" style="margin-top: 2rem;">Both options come with a 100% money-back guarantee if you're not satisfied. No questions asked.</p>
        </div>
    </section>
    
    <section class="section faq-section">
        <div class="container">
            <h2>Still have questions? Let's clear them up.</h2>
            <div class="faq-item">
                <p class="faq-question">Why is it priced this way?</p>
                <p>This isn't a cheap course. It’s direct, one-on-one access to someone who has gone through the exact journey you're on. You’re not just paying for a call; you’re paying to save months or even years of trial-and-error. Think of the time and frustration you’ll avoid. That's what this cost is for.</p>
            </div>
            <div class="faq-item">
                <p class="faq-question">What if I don't know how to code at all?</p>
                <p>That's fine. We'll start with the basics. My goal is to get you comfortable with the process of building and shipping. We'll focus on what you need to know to get your specific app off the ground, not every single coding language in existence. We'll get you to a place where you're not just following tutorials, but actually building something of your own.</p>
            </div>
            <div class="faq-item">
                <p class="faq-question">I'm worried about the time commitment.</p>
                <p>This coaching is designed to fit your schedule. We can schedule calls at a time that works for you, and the Discord messaging is there for quick questions whenever you have a few minutes. The entire point is to make your journey more efficient, not add more to your plate. We'll focus on the highest-impact actions you can take to make the fastest progress.</p>
            </div>
            <div class="faq-item">
                <p class="faq-question">What if I'm a seasoned developer already?</p>
                <p>Then this is perfect for you. You already know how to build, but you might be stuck on the business and marketing side. We can use our time to focus on product-market fit, social media strategy, and getting your app in front of the right audience. You'll move from being a developer to being a founder.</p>
            </div>
            
            <div class="cta-section" style="margin-top: 4rem;">
                <h2>It's time to build the thing you've been dreaming of.</h2>
                <p>Stop putting it off. The only thing standing between you and a launched, profitable app is a clear path forward. Let's build one together.</p>
                <a href="#offer" class="cta-button">Get Started Now</a>
            </div>
        </div>
    </section>

    <footer class="footer">
        <div class="container">
            <p>&copy; 2025. All Rights Reserved.</p>
        </div>
    </footer>

</body>
</html>
