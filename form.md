---
layout: form
title: Form Helper
excerpt: form to help you build out your config.yml
---

<main style="width: 90vw;">
  <section id="input">
    <form id="config-form" onchange="submitConfig(); event.preventDefault();">
      <h2>General Configuration Form</h2>
      <p>Input the following information and see the output on the right</p>
      <section id="info">
        <h3>Required Information</h3>
        <p>
          <label for="name">Full Name </label>
          <input id="name" name="name" type="text" placeholder="River Campus Libraries" required>
        </p>
        <p>
          <label>UR Email </label>
          <input id="email" name="email" type="email" placeholder="rclfeedback@library.rochester.edu" required>
        </p>
        <p>
          <label for="github">Github </label>
          <input id="github" name="github" type="text" placeholder="rochester-rcl" required>
        </p>
        <p>
          <label for="role">Role at UofR</label>
          <select id="role" required>
            <option>Undergraduate Student</option>
            <option>Graduate Student</option>
            <option>Researcher</option>
            <option>Professor</option>
            <option>Staff</option>
          </select>
        </p>
        <p>
          <label for="field">Field/Department/Specialty </label>
          <input id="field" name="field" type="text" placeholder="Chemistry" required>
        </p>
      </section>
      <section id="accounts">
        <h3>Additional Links</h3>
        <p>
          <label for="website">Website </label>
          <input id="website" name="website" type="text" placeholder="https://library.rochester.edu">
        </p>
        <p>
          <label for="resume">Resume </label>
          <input id="resume" name="resume" type="text" placeholder="https://website.com/resume.pdf">
        </p>
        <p>
          <label for="orcid">Orcid </label>
          <input id="orcid" name="orcid" type="text" placeholder="0000-0001-1234-567B">
        </p>
        <p>
          <label for="scholar">Google Scholar ID </label>
          <input id="scholar" name="scholar" type="text" placeholder="rcl21UofRAAAB">
        </p>
        <p>
          <label for="twitter">Twitter @</label>
          <input id="twitter" name="twitter" type="text" placeholder="RCLibraries">
        </p>
        <p>
          <label for="linkedin">LinkedIn </label>
          <input id="linkedin" name="linkedin" type="text" placeholder="fname-lname-1234567a">
        </p>
        <p>
          <label for="mendeley">Mendeley </label>
          <input id="mendeley" name="mendeley" type="text" placeholder="">
        </p>
        <p>
          <label for="researchgate">ResearchGate </label>
          <input id="researchgate" name="researchgate" type="text" placeholder="">
        </p>
      </section>
    </form>
    <br><br><br>
  </section>

  <section id="output">
    <h2>Output Configuration</h2>
    <button id="copy-btn" disabled onclick="copyToClipboard('#config-yml')">copy output</button>
    <br><br>
    <p>
      A copy of the config will appear after all required fields are filled in.
      Once it appears, click on the "copy output" button to add it to your clipboard, 
      then use it to replace the existing contents of 
      <strong><a href="https://github.com/{{ author.github }}/{{ author.github }}.github.io/edit/master/_config.yml" 
        target="blank">your <code>_config.yml</code> file</a></strong>.
    </p>
    <textarea readonly id="config-yml">Please fill in all required fields!</textarea>
  </section>
</main>
