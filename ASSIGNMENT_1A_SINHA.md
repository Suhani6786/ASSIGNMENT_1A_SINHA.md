## Section 1: User Journey

Page loads. User sees the logo, navigation links, and "Deploy Free Cluster" button.
Action 1: User clicks "Pricing" and goes to the pricing section.
Action 2: User compares the three plans and picks a plan.
Action 3: User puts in the node count and log amount and email.
Action 4: User clicks Generate API Keys.
Terminal State: User will see a message that confirms it.

## Section 2: Norman Usability & Constraint Audit
Signifier – Main CTA Button: Use an <a href="#register"> link so users know they can click it.
Signifier – Most Popular Plan: Use <strong> for the “Most Popular” text to show that it is important.
Physical/System Constraint – Node Count: Use type="number", min="1", max="500", and step="1" to limit the numbers the user can enter.
Physical/System Constraint – Email Field: Use type="email" and required so the user must enter an email.
Feedback Loop – Form and Navigation: The browser shows a message when the form is not filled correctly. Clicking a navigation link takes the user to that section.

##Section 3: Semantic Component & Layout Tree

body
  header
    a<logo, links to home>
    nav
      a<Features>
      a<Pricing>
      a<Calculator>
      a<Deploy Free Cluster>

  main
    section<hero>
      div<badge>
      h1<Primary Value Proposition>
      p<lead text>
      div<cta-group>
        a<Deploy Free Cluster>
        a<Read Documentation>

    section<features>
      header
        h2<Platform Capabilities>
        p<section subtitle>
      article<Latency Tracking>
        h3<feature name>
        p<describe feature>
      article<Log Aggregation>
        h3<feature name>
        p<describe feature>
      article<Auto-Remediation>
        h3<feature name>
        p<describe feature>

    section<pricing>
      header
        h2<Compute Tier Comparison>
        p<section subtitle>
      article<Developer>
        h3<tier name>
        p<tier description>
        div<tier price>
        ul<feature list>
        a<select plan>
      article<Pro Cluster>
        strong<Most Popular>
        h3<tier name>
        p<tier description>
        div<tier price>
        ul<feature list>
        a<select plan>
      article<Enterprise Dedicated>
        h3<tier name>
        p<tier description>
        div<tier price>
        ul<feature list>
        a<select plan>

    section<register>
      header
        h2<Claim API Sandbox Keys>
        p<section subtitle>
      form
        label + input<email, type email, required>
        label + input<node count, type number, min 1, max 500, step 1, optional>
        label + input<log throughput, type number, min 100, max 1000000, step 100, optional>
        button<Generate API Keys>

  footer
    div<footer container>
      p<copyright text>
      nav<footer links>
        a<Back to Top>
        a<Features>
        a<Pricing>
        a<Calculator>
