
<style>
  body { font-family: sans-serif; }
  .pregunta { display: none; margin-bottom: 20px; }
  .pregunta.activa { display: block; animation: fadein 0.5s; }
  @keyframes fadein { from { opacity: 0; } to { opacity: 1; } }
  .opcion { display: block; width: 100%; text-align: left; padding: 15px; margin: 10px 0; font-size: 16px; border: 1px solid #d0d7de; border-radius: 8px; background: #ffffff; cursor: pointer; transition: 0.2s; }
  .opcion:hover:not(:disabled) { background: #f3f4f6; }
  .correcta { background: #dafbe1 !important; border-color: #4ac26b !important; color: #1a7f37; font-weight: bold; }
  .incorrecta { background: #ffebe9 !important; border-color: #ff8182 !important; color: #cf222e; font-weight: bold; }
  #btn-siguiente { display: none; margin-top: 20px; padding: 12px 24px; font-size: 16px; background-color: #0969da; color: white; border: none; border-radius: 6px; cursor: pointer; float: right; font-weight: bold; }
  #btn-siguiente:hover { background-color: #0550ae; }
  #resultados { display: none; text-align: center; padding: 40px 20px; }
  #btn-repetir { margin-top: 20px; padding: 12px 24px; font-size: 16px; background-color: #2da44e; color: white; border: none; border-radius: 6px; cursor: pointer; font-weight: bold; }
  details { background: #f6f8fa; padding: 10px; border-radius: 5px; margin-bottom: 15px; font-size: 14px; }
  summary { font-weight: bold; cursor: pointer; }
</style>

<div id="contenedor-test">

  <template id="reading-text">
    <details>
      <summary>📖 Click to read the text: "How to Keep Clients"</summary>
      <p>In today's competitive market, keeping existing clients is more important than ever. Companies know that finding new clients costs more money and time than keeping current ones happy. Because of this, businesses are using different methods to make sure their clients stay with them and become more loyal.</p>
      <p><strong>(1)</strong> The first step in keeping clients is knowing what they want and need. Companies that ask clients for feedback regularly can make their services and products better. Using surveys, face-to-face meetings, and regular updates helps businesses understand what matters most to their clients.</p>
      <p><strong>(2)</strong> Good service is key to keeping clients long-term. This means more than just fixing problems when they happen. Companies need to make sure every time they talk to a client, it feels personal and positive. Quick replies, following up, and solving problems before they happen shows clients the company cares.</p>
      <p><strong>(3)</strong> Special programs that reward loyal clients work well. Giving clients special offers, letting them try new products first, or even sending a personal thank-you message shows that their business matters. Some companies offer different levels of rewards based on how long clients have stayed with them or how much they buy.</p>
      <p><strong>(4)</strong> Clients like to hear from companies regularly, even when there's nothing new to say. Sending newsletters, updates about products, and friendly check-in messages keeps clients interested and makes them feel valued. Regular contact helps clients remember the company and shows that the business is always working to help them.</p>
      <p><strong>(5)</strong> What clients need can change, and companies must be ready to change too. This might mean using new technology, changing how they work, or offering different services when the market changes. Companies that can adjust what they offer to match what clients want are more likely to keep those clients.</p>
      <p><strong>(6)</strong> Using these methods helps businesses keep their clients longer and build better relationships with them. When companies focus on understanding their clients, giving excellent service, and rewarding loyalty, they're more likely to succeed in the long run.</p>
    </details>
  </template>

  <div class="pregunta reading-q">
    <p><strong>1. Choose the correct heading for Paragraph 1:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. Summary</button>
    <button class="opcion" onclick="verificar(this, true)">b. Getting to Know Your Clients</button>
    <button class="opcion" onclick="verificar(this, false)">c. Going Beyond Basic Service</button>
    <button class="opcion" onclick="verificar(this, false)">d. Moving with the Times</button>
    <button class="opcion" onclick="verificar(this, false)">e. Staying in Touch</button>
    <button class="opcion" onclick="verificar(this, false)">f. Making Loyalty Worth It</button>
  </div>

  <div class="pregunta reading-q">
    <p><strong>2. Choose the correct heading for Paragraph 2:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. Summary</button>
    <button class="opcion" onclick="verificar(this, false)">b. Getting to Know Your Clients</button>
    <button class="opcion" onclick="verificar(this, true)">c. Going Beyond Basic Service</button>
    <button class="opcion" onclick="verificar(this, false)">d. Moving with the Times</button>
    <button class="opcion" onclick="verificar(this, false)">e. Staying in Touch</button>
    <button class="opcion" onclick="verificar(this, false)">f. Making Loyalty Worth It</button>
  </div>

  <div class="pregunta reading-q">
    <p><strong>3. Choose the correct heading for Paragraph 3:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. Summary</button>
    <button class="opcion" onclick="verificar(this, false)">b. Getting to Know Your Clients</button>
    <button class="opcion" onclick="verificar(this, false)">c. Going Beyond Basic Service</button>
    <button class="opcion" onclick="verificar(this, false)">d. Moving with the Times</button>
    <button class="opcion" onclick="verificar(this, false)">e. Staying in Touch</button>
    <button class="opcion" onclick="verificar(this, true)">f. Making Loyalty Worth It</button>
  </div>

  <div class="pregunta reading-q">
    <p><strong>4. Choose the correct heading for Paragraph 4:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. Summary</button>
    <button class="opcion" onclick="verificar(this, false)">b. Getting to Know Your Clients</button>
    <button class="opcion" onclick="verificar(this, false)">c. Going Beyond Basic Service</button>
    <button class="opcion" onclick="verificar(this, false)">d. Moving with the Times</button>
    <button class="opcion" onclick="verificar(this, true)">e. Staying in Touch</button>
    <button class="opcion" onclick="verificar(this, false)">f. Making Loyalty Worth It</button>
  </div>

  <div class="pregunta reading-q">
    <p><strong>5. Choose the correct heading for Paragraph 5:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. Summary</button>
    <button class="opcion" onclick="verificar(this, false)">b. Getting to Know Your Clients</button>
    <button class="opcion" onclick="verificar(this, false)">c. Going Beyond Basic Service</button>
    <button class="opcion" onclick="verificar(this, true)">d. Moving with the Times</button>
    <button class="opcion" onclick="verificar(this, false)">e. Staying in Touch</button>
    <button class="opcion" onclick="verificar(this, false)">f. Making Loyalty Worth It</button>
  </div>

  <div class="pregunta reading-q">
    <p><strong>6. Choose the correct heading for Paragraph 6:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a. Summary</button>
    <button class="opcion" onclick="verificar(this, false)">b. Getting to Know Your Clients</button>
    <button class="opcion" onclick="verificar(this, false)">c. Going Beyond Basic Service</button>
    <button class="opcion" onclick="verificar(this, false)">d. Moving with the Times</button>
    <button class="opcion" onclick="verificar(this, false)">e. Staying in Touch</button>
    <button class="opcion" onclick="verificar(this, false)">f. Making Loyalty Worth It</button>
  </div>

  <div class="pregunta reading-q">
    <p><strong>7. Based on the text, which approach would likely have the biggest impact on client loyalty?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. offering the lowest prices</button>
    <button class="opcion" onclick="verificar(this, false)">b. having the most advanced technology</button>
    <button class="opcion" onclick="verificar(this, true)">c. combining personal service with regular communication</button>
    <button class="opcion" onclick="verificar(this, false)">d. hiring more staff</button>
  </div>

  <div class="pregunta reading-q">
    <p><strong>8. What does the text suggest about successful companies?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. they focus mainly on getting new clients</button>
    <button class="opcion" onclick="verificar(this, false)">b. they keep their services the same to maintain consistency</button>
    <button class="opcion" onclick="verificar(this, false)">c. they communicate only when there are updates</button>
    <button class="opcion" onclick="verificar(this, true)">d. they anticipate and respond to change rather than just react to problems</button>
  </div>

  <div class="pregunta reading-q">
    <p><strong>9. What role does feedback play in client retention according to the text?</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a. it helps shape both current services and future business direction</button>
    <button class="opcion" onclick="verificar(this, false)">b. it only helps with fixing current problems</button>
    <button class="opcion" onclick="verificar(this, false)">c. it's mainly useful for marketing purposes</button>
    <button class="opcion" onclick="verificar(this, false)">d. it's less important than loyalty programs</button>
  </div>

  <div class="pregunta reading-q">
    <p><strong>10. Which statement best reflects the text's view on client communication?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. companies should only contact clients with important updates</button>
    <button class="opcion" onclick="verificar(this, true)">b. regular contact matters more than having new information to share</button>
    <button class="opcion" onclick="verificar(this, false)">c. digital newsletters are the best way to stay in touch</button>
    <button class="opcion" onclick="verificar(this, false)">d. communication should focus on selling new services</button>
  </div>

  <div class="pregunta reading-q">
    <p><strong>11. Why does the text emphasize personal interaction with clients?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. it's cheaper than running loyalty programs</button>
    <button class="opcion" onclick="verificar(this, false)">b. it helps companies sell more products</button>
    <button class="opcion" onclick="verificar(this, true)">c. it builds emotional connections that make clients less likely to leave</button>
    <button class="opcion" onclick="verificar(this, false)">d. it reduces the need for other retention strategies</button>
  </div>

  <div class="pregunta reading-q">
    <p><strong>12. What can we learn about the cost of business growth from this text?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. all business growth requires significant investment</button>
    <button class="opcion" onclick="verificar(this, false)">b. new clients always generate more profit</button>
    <button class="opcion" onclick="verificar(this, false)">c. marketing to new clients is the best use of resources</button>
    <button class="opcion" onclick="verificar(this, true)">d. keeping existing clients is more cost-effective than finding new ones</button>
  </div>

  <div class="pregunta">
    <p><strong>13. Last year I (go) _________ to America for my holidays</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a. went</button>
    <button class="opcion" onclick="verificar(this, false)">b. have been</button>
    <button class="opcion" onclick="verificar(this, false)">c. was</button>
    <button class="opcion" onclick="verificar(this, false)">d. gone</button>
  </div>

  <div class="pregunta">
    <p><strong>14. Josh ________________ in Southampton since 2017</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. lives</button>
    <button class="opcion" onclick="verificar(this, true)">b. has lived</button>
    <button class="opcion" onclick="verificar(this, false)">c. lived</button>
    <button class="opcion" onclick="verificar(this, false)">d. is living</button>
  </div>

  <div class="pregunta">
    <p><strong>15. Jim .......................... the laptop 2 hours ago</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a. broke</button>
    <button class="opcion" onclick="verificar(this, false)">b. has broken</button>
    <button class="opcion" onclick="verificar(this, false)">c. break</button>
    <button class="opcion" onclick="verificar(this, false)">d. is breaking</button>
  </div>

  <div class="pregunta">
    <p><strong>16. Someone ................ on the road now.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. walk</button>
    <button class="opcion" onclick="verificar(this, false)">b. walked</button>
    <button class="opcion" onclick="verificar(this, true)">c. is walking</button>
    <button class="opcion" onclick="verificar(this, false)">d. walks</button>
  </div>

  <div class="pregunta">
    <p><strong>17. William often.............. cycling to keep fit and healthy.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. is going</button>
    <button class="opcion" onclick="verificar(this, true)">b. goes</button>
    <button class="opcion" onclick="verificar(this, false)">c. went</button>
    <button class="opcion" onclick="verificar(this, false)">d. has gone</button>
  </div>

  <div class="pregunta">
    <p><strong>18. My friend and I .............. guitar course every Saturday at 16:00.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. have taken</button>
    <button class="opcion" onclick="verificar(this, false)">b. are taking</button>
    <button class="opcion" onclick="verificar(this, true)">c. take</button>
    <button class="opcion" onclick="verificar(this, false)">d. took</button>
  </div>

  <div class="pregunta">
    <p><strong>19. The bus .................. at 8 am.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. left</button>
    <button class="opcion" onclick="verificar(this, true)">b. leaves</button>
    <button class="opcion" onclick="verificar(this, false)">c. is leaving</button>
    <button class="opcion" onclick="verificar(this, false)">d. has left</button>
  </div>

  <div class="pregunta">
    <p><strong>20. I …………………….(not meet) him for three months.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a. haven't met</button>
    <button class="opcion" onclick="verificar(this, false)">b. am not meeting</button>
    <button class="opcion" onclick="verificar(this, false)">c. didn't meet</button>
    <button class="opcion" onclick="verificar(this, false)">d. don't meet</button>
  </div>

  <div class="pregunta">
    <p><strong>21. My schedule is full. For example, on Monday…</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. I will go to the dentist at 9.</button>
    <button class="opcion" onclick="verificar(this, false)">b. I go to the dentist.</button>
    <button class="opcion" onclick="verificar(this, false)">c. I am going to go to the dentist at 9.</button>
    <button class="opcion" onclick="verificar(this, true)">d. I am going to the dentist at 9.</button>
  </div>

  <div class="pregunta">
    <p><strong>22. I think she is the fastest at school. She….</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a. will win the tournament.</button>
    <button class="opcion" onclick="verificar(this, false)">b. is going to win the tournament.</button>
    <button class="opcion" onclick="verificar(this, false)">c. will be winning the tournament.</button>
    <button class="opcion" onclick="verificar(this, false)">d. wins the tournament.</button>
  </div>

  <div class="pregunta">
    <p><strong>23. It is cloudy and the sky is overcast. It…</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. will rain.</button>
    <button class="opcion" onclick="verificar(this, true)">b. is going to rain.</button>
    <button class="opcion" onclick="verificar(this, false)">c. is raining.</button>
    <button class="opcion" onclick="verificar(this, false)">d. rains.</button>
  </div>

  <div class="pregunta">
    <p><strong>24. It’s a good idea you visit a doctor. You ____________ visit a doctor.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. Must</button>
    <button class="opcion" onclick="verificar(this, true)">b. Should</button>
    <button class="opcion" onclick="verificar(this, false)">c. Can</button>
    <button class="opcion" onclick="verificar(this, false)">d. Don’t have to</button>
  </div>

  <div class="pregunta">
    <p><strong>25. I’m allowed to stay out late. I ____________ stay out late.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. Can’t</button>
    <button class="opcion" onclick="verificar(this, false)">b. Must</button>
    <button class="opcion" onclick="verificar(this, false)">c. Should</button>
    <button class="opcion" onclick="verificar(this, true)">d. Can</button>
  </div>

  <div class="pregunta">
    <p><strong>26. I don’t know how to speak German. I _____________ speak German.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. I’m not allowed to</button>
    <button class="opcion" onclick="verificar(this, false)">b. Mustn’t</button>
    <button class="opcion" onclick="verificar(this, false)">c. Don’t have to</button>
    <button class="opcion" onclick="verificar(this, true)">d. Can’t</button>
  </div>

  <div class="pregunta">
    <p><strong>27. It’s obligatory to clean schools in Japan. You ____________ clean schools in Japan.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. Don’t have to</button>
    <button class="opcion" onclick="verificar(this, false)">b. Should</button>
    <button class="opcion" onclick="verificar(this, true)">c. Must</button>
    <button class="opcion" onclick="verificar(this, false)">d. Can</button>
  </div>

  <div class="pregunta">
    <p><strong>28. It was not necessary to do homework yesterday because we had a bank holiday. We _____________ do homework yesterday...</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. Don’t have to</button>
    <button class="opcion" onclick="verificar(this, false)">b. Had to</button>
    <button class="opcion" onclick="verificar(this, true)">c. Didn’t have to</button>
    <button class="opcion" onclick="verificar(this, false)">d. Didn’t had to</button>
  </div>

  <div class="pregunta">
    <p><strong>29. It’s not a good idea to eat so much fat. You ____________ eat so much fat.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. Mustn’t</button>
    <button class="opcion" onclick="verificar(this, true)">b. ought not to</button>
    <button class="opcion" onclick="verificar(this, false)">c. Should</button>
    <button class="opcion" onclick="verificar(this, false)">d. Can’t</button>
  </div>

  <div class="pregunta">
    <p><strong>30. An individual who works on a project basis for various clients, often as an independent contractor.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) freelancer</button>
    <button class="opcion" onclick="verificar(this, false)">b) colleague</button>
    <button class="opcion" onclick="verificar(this, false)">c) IT consultant</button>
  </div>

  <div class="pregunta">
    <p><strong>31. The ability to adjust working hours to suit one’s preferences or needs.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) flexible schedule</button>
    <button class="opcion" onclick="verificar(this, false)">b) deadline</button>
    <button class="opcion" onclick="verificar(this, false)">c) timeline</button>
  </div>

  <div class="pregunta">
    <p><strong>32. Online gatherings where participants can communicate and collaborate using video conferencing tools.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) telecommuting</button>
    <button class="opcion" onclick="verificar(this, true)">b) virtual meetings</button>
    <button class="opcion" onclick="verificar(this, false)">c) cybersecurity</button>
  </div>

  <div class="pregunta">
    <p><strong>33. He usually earns a good (…) for his hard work.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a. salary</button>
    <button class="opcion" onclick="verificar(this, false)">b. promotions</button>
    <button class="opcion" onclick="verificar(this, false)">c. promotion</button>
    <button class="opcion" onclick="verificar(this, false)">d. salaries</button>
  </div>

  <div class="pregunta">
    <p><strong>34. What is the (…) for submitting the project report?</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a. deadline</button>
    <button class="opcion" onclick="verificar(this, false)">b. deadlines</button>
    <button class="opcion" onclick="verificar(this, false)">c. vacation</button>
    <button class="opcion" onclick="verificar(this, false)">d. vacations</button>
  </div>

  <div class="pregunta">
    <p><strong>35. It’s essential to identify and mitigate potential ( … ) that could affect the project’s success.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a. risks</button>
    <button class="opcion" onclick="verificar(this, false)">b. timelines</button>
    <button class="opcion" onclick="verificar(this, false)">c. budgets</button>
    <button class="opcion" onclick="verificar(this, false)">d. milestones</button>
  </div>

  <div class="pregunta">
    <p><strong>36. Before starting the project, we should ( … ) the tasks to determine which ones are most critical.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a. prioritize</button>
    <button class="opcion" onclick="verificar(this, false)">b. risk</button>
    <button class="opcion" onclick="verificar(this, false)">c. deliverable</button>
    <button class="opcion" onclick="verificar(this, false)">d. issue</button>
  </div>

  <div class="pregunta">
    <p><strong>37. The company implemented a ( … ) to reward loyal customers.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. courtesy</button>
    <button class="opcion" onclick="verificar(this, false)">b. assistance</button>
    <button class="opcion" onclick="verificar(this, true)">c. loyalty program</button>
    <button class="opcion" onclick="verificar(this, false)">d. refund</button>
  </div>

  <div class="pregunta">
    <p><strong>38. The ( … ) provided by the customer service team greatly influences customer satisfaction.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. complaint</button>
    <button class="opcion" onclick="verificar(this, false)">b. courtesy</button>
    <button class="opcion" onclick="verificar(this, false)">c. issue</button>
    <button class="opcion" onclick="verificar(this, true)">d. feedback</button>
  </div>

  <div class="pregunta">
    <p><strong>39. What technology is commonly used for effective … ?</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a. cloud computing</button>
    <button class="opcion" onclick="verificar(this, false)">b. freelancer</button>
    <button class="opcion" onclick="verificar(this, false)">c. virtual meetings</button>
    <button class="opcion" onclick="verificar(this, false)">d. flexible hours</button>
  </div>

  <div class="pregunta">
    <p><strong>40. What is a common technology used for remote training sessions?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. Telecommuting</button>
    <button class="opcion" onclick="verificar(this, false)">b. Cloud computing</button>
    <button class="opcion" onclick="verificar(this, false)">c. May</button>
    <button class="opcion" onclick="verificar(this, true)">d. Webinar</button>
  </div>

  <template id="listening-link">
    <div style="background: #eef5ff; padding: 10px; border-radius: 5px; margin-bottom: 15px; font-size: 14px;">
      🎧 <strong>Listening Section:</strong> <a href="https://www.youtube.com/watch?v=HuR-LNZ7bUU&t=130s" target="_blank">Click here to listen to the audio on YouTube</a>
    </div>
  </template>

  <div class="pregunta listening-q">
    <p><strong>41. Daniel has worked from home for longer than Kate.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. True</button>
    <button class="opcion" onclick="verificar(this, true)">b. False</button>
  </div>

  <div class="pregunta listening-q">
    <p><strong>42. Kate started working from home after her son was born.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. True</button>
    <button class="opcion" onclick="verificar(this, true)">b. False</button>
  </div>

  <div class="pregunta listening-q">
    <p><strong>43. Kate used to be a teacher.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a. True</button>
    <button class="opcion" onclick="verificar(this, false)">b. False</button>
  </div>

  <div class="pregunta listening-q">
    <p><strong>44. Kate’s work writing a geography book was very well-paid.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. True</button>
    <button class="opcion" onclick="verificar(this, true)">b. False</button>
  </div>

  <div class="pregunta listening-q">
    <p><strong>45. Daniel started working from home after losing his job.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. True</button>
    <button class="opcion" onclick="verificar(this, true)">b. False</button>
  </div>

  <div class="pregunta listening-q">
    <p><strong>46. Daniel doesn’t enjoy working from home because it isn’t sociable.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a. True</button>
    <button class="opcion" onclick="verificar(this, false)">b. False</button>
  </div>

  <div class="pregunta listening-q">
    <p><strong>47. Daniel used to play badminton and cards with his colleagues.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a. True</button>
    <button class="opcion" onclick="verificar(this, false)">b. False</button>
  </div>

  <div class="pregunta listening-q">
    <p><strong>48. Daniel has recently made friends with a new colleague.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. True</button>
    <button class="opcion" onclick="verificar(this, true)">b. False</button>
  </div>

  <div class="pregunta listening-q">
    <p><strong>49. Kate didn’t use to socialise with colleagues because she was too tired.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a. True</button>
    <button class="opcion" onclick="verificar(this, false)">b. False</button>
  </div>

  <div class="pregunta listening-q">
    <p><strong>50. Kate spends time with some friends from her art class.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a. True</button>
    <button class="opcion" onclick="verificar(this, false)">b. False</button>
  </div>

</div> <button id="btn-siguiente" onclick="siguientePregunta()">Next Question ➡️</button>

<div id="resultados">
  <h2>¡Test completed! 🎉</h2>
  <p style="font-size: 18px;">You scored <strong id="aciertos">0</strong> out of <strong id="total">0</strong> questions.</p>
  <button id="btn-repetir" onclick="location.reload()">↻ Repeat test</button>
</div>

<script>
  let indexActual = 0;
  let aciertos = 0;
  const contenedorTest = document.getElementById('contenedor-test');
  const btnSiguiente = document.getElementById('btn-siguiente');
  const divResultados = document.getElementById('resultados');

  // Insertar los textos de Reading y Listening dinámicamente
  const readingText = document.getElementById('reading-text').innerHTML;
  document.querySelectorAll('.reading-q').forEach(q => {
    q.insertAdjacentHTML('afterbegin', readingText);
  });

  const listeningLink = document.getElementById('listening-link').innerHTML;
  document.querySelectorAll('.listening-q').forEach(q => {
    q.insertAdjacentHTML('afterbegin', listeningLink);
  });

  let preguntasArray = Array.from(document.querySelectorAll('.pregunta'));

  // Borrar números
  preguntasArray.forEach(pregunta => {
    let textoPregunta = pregunta.querySelector('p strong');
    if (textoPregunta) {
      textoPregunta.innerHTML = textoPregunta.innerHTML.replace(/^\d+\.\s*/, '');
    }
  });

  // Crear contador visual
  const progresoDiv = document.createElement('div');
  progresoDiv.style.cssText = 'text-align: center; font-weight: bold; font-size: 16px; color: #57606a; margin-bottom: 20px; background: #f6f8fa; padding: 10px; border-radius: 8px; border: 1px solid #d0d7de;';
  contenedorTest.parentNode.insertBefore(progresoDiv, contenedorTest);

  // Barajar
  function mezclarPreguntas(array) {
    for (let i = array.length - 1; i > 0; i--) {
      const j = Math.floor(Math.random() * (i + 1));
      [array[i], array[j]] = [array[j], array[i]];
    }
  }
  mezclarPreguntas(preguntasArray);

  // Reordenar DOM
  preguntasArray.forEach(pregunta => {
    pregunta.classList.remove('activa');
    contenedorTest.appendChild(pregunta); 
  });
  preguntasArray[0].classList.add('activa');

  const preguntas = preguntasArray;

  function actualizarProgreso() {
    progresoDiv.innerText = `Question ${indexActual + 1} of ${preguntas.length}`;
  }
  actualizarProgreso();

  function verificar(boton, esCorrecto) {
    let contenedor = boton.parentElement;
    let botones = contenedor.querySelectorAll('button.opcion');
    
    botones.forEach(b => {
      b.disabled = true;
      b.style.cursor = 'default';
    });

    if (esCorrecto) {
      boton.classList.add('correcta');
      boton.innerHTML += " ✅";
      aciertos++;
    } else {
      boton.classList.add('incorrecta');
      boton.innerHTML += " ❌";
      botones.forEach(b => {
        if(b.getAttribute("onclick").includes("true")) {
          b.classList.add('correcta');
        }
      });
    }
    
    btnSiguiente.style.display = 'block';
  }

  function siguientePregunta() {
    preguntas[indexActual].classList.remove('activa');
    btnSiguiente.style.display = 'none';
    
    indexActual++;

    if (indexActual < preguntas.length) {
      preguntas[indexActual].classList.add('activa');
      actualizarProgreso();
    } else {
      progresoDiv.style.display = 'none';
      contenedorTest.style.display = 'none';
      divResultados.style.display = 'block';
      document.getElementById('aciertos').innerText = aciertos;
      document.getElementById('total').innerText = preguntas.length;
    }
  }
</script>
