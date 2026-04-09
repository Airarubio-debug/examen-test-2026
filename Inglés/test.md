
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

  <div class="pregunta">
    <p><strong>51. Where does she usually ( … ) during the week?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. works</button>
    <button class="opcion" onclick="verificar(this, true)">b. work</button>
    <button class="opcion" onclick="verificar(this, false)">c. working</button>
    <button class="opcion" onclick="verificar(this, false)">d. worked</button>
  </div>

  <div class="pregunta">
    <p><strong>52. Right now, he (…) an important meeting with the clients.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. attend</button>
    <button class="opcion" onclick="verificar(this, false)">b. attends</button>
    <button class="opcion" onclick="verificar(this, false)">c. attended</button>
    <button class="opcion" onclick="verificar(this, true)">d. is attending</button>
  </div>

  <div class="pregunta">
    <p><strong>53. She decided (…) a course to enhance her skills.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. taking</button>
    <button class="opcion" onclick="verificar(this, false)">b. takes</button>
    <button class="opcion" onclick="verificar(this, false)">c. taken</button>
    <button class="opcion" onclick="verificar(this, true)">d. to take</button>
  </div>

  <div class="pregunta">
    <p><strong>54. What is the (…) for submitting the project report?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. deadlines</button>
    <button class="opcion" onclick="verificar(this, true)">b. deadline</button>
    <button class="opcion" onclick="verificar(this, false)">c. vacations</button>
    <button class="opcion" onclick="verificar(this, false)">d. vacation</button>
  </div>

  <div class="pregunta">
    <p><strong>55. He usually earns a good (…) for his hard work.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. salaries</button>
    <button class="opcion" onclick="verificar(this, false)">b. promotion</button>
    <button class="opcion" onclick="verificar(this, false)">c. promotions</button>
    <button class="opcion" onclick="verificar(this, true)">d. salary</button>
  </div>

  <div class="pregunta">
    <p><strong>56. At this moment, the team (…) in the conference room to discuss the project.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. meets</button>
    <button class="opcion" onclick="verificar(this, true)">b. is meeting</button>
    <button class="opcion" onclick="verificar(this, false)">c. meet</button>
    <button class="opcion" onclick="verificar(this, false)">d. meeting</button>
  </div>

  <div class="pregunta">
    <p><strong>57. They have plans (…) their business to new markets.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. expands</button>
    <button class="opcion" onclick="verificar(this, false)">b. expanding</button>
    <button class="opcion" onclick="verificar(this, true)">c. to expand</button>
    <button class="opcion" onclick="verificar(this, false)">d. expand</button>
  </div>

  <div class="pregunta">
    <p><strong>58. His colleagues helped him prepare for the (…).</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a. interview</button>
    <button class="opcion" onclick="verificar(this, false)">b. interviews</button>
    <button class="opcion" onclick="verificar(this, false)">c. workspaces</button>
    <button class="opcion" onclick="verificar(this, false)">d. workplace</button>
  </div>

  <div class="pregunta">
    <p><strong>59. The company provides its employees with paid (…).</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. vacations</button>
    <button class="opcion" onclick="verificar(this, false)">b. sick leave</button>
    <button class="opcion" onclick="verificar(this, true)">c. vacation days</button>
    <button class="opcion" onclick="verificar(this, false)">d. sick leaves</button>
  </div>

  <div class="pregunta">
    <p><strong>60. Right now, she (…) candidates for the new job position.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. interview</button>
    <button class="opcion" onclick="verificar(this, false)">b. interviews</button>
    <button class="opcion" onclick="verificar(this, false)">c. interviewed</button>
    <button class="opcion" onclick="verificar(this, true)">d. is interviewing</button>
  </div>

  <div class="pregunta">
    <p><strong>61. He (…) (deliver) the project report before the deadline.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. was delivering</button>
    <button class="opcion" onclick="verificar(this, false)">b. has delivered</button>
    <button class="opcion" onclick="verificar(this, true)">c. had delivered</button>
    <button class="opcion" onclick="verificar(this, false)">d. delivered</button>
  </div>

  <div class="pregunta">
    <p><strong>62. By the time we arrived, they (…) (finish) the task.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a. had finished</button>
    <button class="opcion" onclick="verificar(this, false)">b. were finishing</button>
    <button class="opcion" onclick="verificar(this, false)">c. finished</button>
    <button class="opcion" onclick="verificar(this, false)">d. has finished</button>
  </div>

  <div class="pregunta">
    <p><strong>63. I can’t believe I ( … ) (never/visit) that museum before.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. was never visiting</button>
    <button class="opcion" onclick="verificar(this, false)">b. never visited</button>
    <button class="opcion" onclick="verificar(this, true)">c. have never visited</button>
    <button class="opcion" onclick="verificar(this, false)">d. had never visited</button>
  </div>

  <div class="pregunta">
    <p><strong>64. In project management, a ( … ) is a significant achievement or event that helps track progress.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. timeline</button>
    <button class="opcion" onclick="verificar(this, true)">b. milestone</button>
    <button class="opcion" onclick="verificar(this, false)">c. budget</button>
    <button class="opcion" onclick="verificar(this, false)">d. risk</button>
  </div>

  <div class="pregunta">
    <p><strong>65. The project manager needed to clarify the project’s ( … ) to ensure everyone knew their roles and responsibilities.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. brainstorm</button>
    <button class="opcion" onclick="verificar(this, false)">b. prioritize</button>
    <button class="opcion" onclick="verificar(this, false)">c. issue</button>
    <button class="opcion" onclick="verificar(this, true)">d. scope</button>
  </div>

  <div class="pregunta">
    <p><strong>66. It’s essential to identify and mitigate potential ( … ) that could affect the project’s success.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a. risks</button>
    <button class="opcion" onclick="verificar(this, false)">b. timelines</button>
    <button class="opcion" onclick="verificar(this, false)">c. milestones</button>
    <button class="opcion" onclick="verificar(this, false)">d. budgets</button>
  </div>

  <div class="pregunta">
    <p><strong>67. The team held a ( … ) session to generate creative solutions to a complex problem.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. deliverable</button>
    <button class="opcion" onclick="verificar(this, false)">b. milestone</button>
    <button class="opcion" onclick="verificar(this, true)">c. brainstorm</button>
    <button class="opcion" onclick="verificar(this, false)">d. scope</button>
  </div>

  <div class="pregunta">
    <p><strong>68. They ( … ) the project yesterday.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. were finishing</button>
    <button class="opcion" onclick="verificar(this, false)">b. finish</button>
    <button class="opcion" onclick="verificar(this, true)">c. finished</button>
    <button class="opcion" onclick="verificar(this, false)">d. have finished</button>
  </div>

  <div class="pregunta">
    <p><strong>69. She (…) on many projects.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. works</button>
    <button class="opcion" onclick="verificar(this, false)">b. was working</button>
    <button class="opcion" onclick="verificar(this, true)">c. has worked</button>
    <button class="opcion" onclick="verificar(this, false)">d. worked</button>
  </div>

  <div class="pregunta">
    <p><strong>70. Before starting the project, we should ( … ) the tasks to determine which ones are most critical.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. risk</button>
    <button class="opcion" onclick="verificar(this, false)">b. deliverable</button>
    <button class="opcion" onclick="verificar(this, false)">c. issue</button>
    <button class="opcion" onclick="verificar(this, true)">d. prioritize</button>
  </div>

  <div class="pregunta">
    <p><strong>71. Select the appropriate article: She bought ( … ) refund policy.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. an refund policy</button>
    <button class="opcion" onclick="verificar(this, true)">b. a refund policy</button>
    <button class="opcion" onclick="verificar(this, false)">c. the refund policy</button>
    <button class="opcion" onclick="verificar(this, false)">d. refund policy (no article)</button>
  </div>

  <div class="pregunta">
    <p><strong>72. Identify the correct form of the verb.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. The call center representative quick solve the issue.</button>
    <button class="opcion" onclick="verificar(this, true)">b. The call center representative will solve the issue quickly.</button>
    <button class="opcion" onclick="verificar(this, false)">c. The call center representative quickly solves the issue.</button>
    <button class="opcion" onclick="verificar(this, false)">d. The call center representative quickly solving the issue.</button>
  </div>

  <div class="pregunta">
    <p><strong>73. The company implemented a ( … ) to reward loyal customers.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. refund</button>
    <button class="opcion" onclick="verificar(this, true)">b. loyalty program</button>
    <button class="opcion" onclick="verificar(this, false)">c. assistance</button>
    <button class="opcion" onclick="verificar(this, false)">d. courtesy</button>
  </div>

  <div class="pregunta">
    <p><strong>74. Choose the grammatically correct sentence.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. The response times of a customer service team are crucial.</button>
    <button class="opcion" onclick="verificar(this, false)">b. A response time of a customer service team is crucial.</button>
    <button class="opcion" onclick="verificar(this, false)">c. The response time of a customer service team are crucial.</button>
    <button class="opcion" onclick="verificar(this, true)">d. The response time of the customer service team is crucial.</button>
  </div>

  <div class="pregunta">
    <p><strong>75. Select the correct sentence.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. Companies should listening to complaints, even if it doesn't concern them directly.</button>
    <button class="opcion" onclick="verificar(this, false)">b. Companies should listens to complaints, even if it doesn't concern them directly.</button>
    <button class="opcion" onclick="verificar(this, false)">c. Companies should listen to a complaints, even if it doesn't concern them directly.</button>
    <button class="opcion" onclick="verificar(this, true)">d. Companies should listen to complaints, even if it doesn't concern them directly.</button>
  </div>

  <div class="pregunta">
    <p><strong>76. The ( … ) provided by the customer service team greatly influences customer satisfaction.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. courtesy</button>
    <button class="opcion" onclick="verificar(this, false)">b. issue</button>
    <button class="opcion" onclick="verificar(this, false)">c. complaint</button>
    <button class="opcion" onclick="verificar(this, true)">d. feedback</button>
  </div>

  <div class="pregunta">
    <p><strong>77. Choose the correct sentence.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. The satisfaction of resolved customer problems is important.</button>
    <button class="opcion" onclick="verificar(this, true)">b. The satisfaction of resolving customer problems is important.</button>
    <button class="opcion" onclick="verificar(this, false)">c. The satisfaction of resolving customers' problems is important.</button>
    <button class="opcion" onclick="verificar(this, false)">d. The satisfactions of resolving customer problems are important.</button>
  </div>

  <div class="pregunta">
    <p><strong>78. Employees … to adhere to strict … measures to protect sensitive data.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. mustn't, cybersecurity</button>
    <button class="opcion" onclick="verificar(this, false)">b. could, online platform</button>
    <button class="opcion" onclick="verificar(this, true)">c. have to, telecommuting</button>
    <button class="opcion" onclick="verificar(this, false)">d. will, digital nomad</button>
  </div>

  <div class="pregunta">
    <p><strong>79. Now, the company _ its products online and in physical stores.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. sold</button>
    <button class="opcion" onclick="verificar(this, true)">b. sells</button>
    <button class="opcion" onclick="verificar(this, false)">c. will sell</button>
  </div>

  <div class="pregunta">
    <p><strong>80. What technology is commonly used for effective ( … ) ?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. freelancer</button>
    <button class="opcion" onclick="verificar(this, false)">b. flexible hours</button>
    <button class="opcion" onclick="verificar(this, true)">c. virtual meetings</button>
    <button class="opcion" onclick="verificar(this, false)">d. cloud computing</button>
  </div>

  <div class="pregunta">
    <p><strong>81. To enhance collaboration, teams should embrace …tools to work together on projects.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. mustn't</button>
    <button class="opcion" onclick="verificar(this, false)">b. flexible hours</button>
    <button class="opcion" onclick="verificar(this, false)">c. don't need</button>
    <button class="opcion" onclick="verificar(this, true)">d. virtual meetings</button>
  </div>

  <div class="pregunta">
    <p><strong>82. What is a common technology used for remote training sessions?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. Cloud computing</button>
    <button class="opcion" onclick="verificar(this, false)">b. May</button>
    <button class="opcion" onclick="verificar(this, false)">c. Telecommuting</button>
    <button class="opcion" onclick="verificar(this, true)">d. Webinar</button>
  </div>

  <div class="pregunta">
    <p><strong>83. Embracing flexible hours means employees can't adjust their work schedules.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. True</button>
    <button class="opcion" onclick="verificar(this, true)">b. False</button>
  </div>

  <div class="pregunta">
    <p><strong>84. Employees may prioritise cybersecurity to protect sensitive data.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. False</button>
    <button class="opcion" onclick="verificar(this, true)">b. True</button>
  </div>

  <div class="pregunta">
    <p><strong>85. Last week, she ( … ) (to work) in healthcare for three years.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. has worked</button>
    <button class="opcion" onclick="verificar(this, false)">b. working</button>
    <button class="opcion" onclick="verificar(this, true)">c. had worked</button>
    <button class="opcion" onclick="verificar(this, false)">d. worked</button>
  </div>

  <div class="pregunta">
    <p><strong>86. In which sentence is the Past Continuous tense used correctly?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. The finance conference had starting when I arrived.</button>
    <button class="opcion" onclick="verificar(this, true)">b. The hospitality event was starting when I arrived.</button>
    <button class="opcion" onclick="verificar(this, false)">c. The telecommunications meeting is starting when I arrive.</button>
    <button class="opcion" onclick="verificar(this, false)">d. The agriculture fair started when I arrive.</button>
  </div>

  <div class="pregunta">
    <p><strong>87. Choose the correct sentence with both Past Perfect and Past Continuous.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a. While I was working, I had received an urgent call from the energy company.</button>
    <button class="opcion" onclick="verificar(this, false)">b. While I working, I had received an urgent call from the energy company.</button>
    <button class="opcion" onclick="verificar(this, false)">c. While I worked, I receive an urgent call from the energy company.</button>
    <button class="opcion" onclick="verificar(this, false)">d. While I worked, I had receiving an urgent call from the energy company.</button>
  </div>

  <div class="pregunta">
    <p><strong>88. Before joining the energy team, he (…) (to work) in retail for five years.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a. had worked</button>
    <button class="opcion" onclick="verificar(this, false)">b. has worked</button>
    <button class="opcion" onclick="verificar(this, false)">c. worked</button>
    <button class="opcion" onclick="verificar(this, false)">d. working</button>
  </div>

  <div class="pregunta">
    <p><strong>89. In which sentence is the Past Continuous tense used correctly?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. While she work, she realises a mistake in the hospitality project.</button>
    <button class="opcion" onclick="verificar(this, true)">b. While she was working, she had realised a mistake in the hospitality project.</button>
    <button class="opcion" onclick="verificar(this, false)">c. While she working, she had realised a mistake in the hospitality project.</button>
    <button class="opcion" onclick="verificar(this, false)">d. While she worked, she had realising a mistake in the hospitality project.</button>
  </div>

  <div class="pregunta">
    <p><strong>90. Choose the correct sentence.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. The retail store had built a new branch last year.</button>
    <button class="opcion" onclick="verificar(this, false)">b. The retail store building a new branch last year.</button>
    <button class="opcion" onclick="verificar(this, true)">c. The retail store built a new branch last year.</button>
    <button class="opcion" onclick="verificar(this, false)">d. The retail store has built a new branch last year.</button>
  </div>

  <div class="pregunta">
    <p><strong>91. By the time we arrived, the telecommunications team ( … ) (to finish) the project.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. finished</button>
    <button class="opcion" onclick="verificar(this, false)">b. is finishing</button>
    <button class="opcion" onclick="verificar(this, false)">c. finishes</button>
    <button class="opcion" onclick="verificar(this, true)">d. had finished</button>
  </div>

  <div class="pregunta">
    <p><strong>92. Convert the direct question into indirect question: «Can you explain the benefits of our new procurement system?».</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. Can you benefit the new procurement system?</button>
    <button class="opcion" onclick="verificar(this, false)">b. What are the benefits of our new procurement system?</button>
    <button class="opcion" onclick="verificar(this, false)">c. How much are the benefits of our new procurement system?</button>
    <button class="opcion" onclick="verificar(this, true)">d. Would you mind explaining the benefits of our new procurement system?</button>
  </div>

  <div class="pregunta">
    <p><strong>93. Convert the direct question into indirect question: «Is the company planning to invest in venture capital for expansion?».</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. Is the planning company to invest in venture capital for expansion?</button>
    <button class="opcion" onclick="verificar(this, false)">b. How much is the company planning to invest in venture capital for expansion?</button>
    <button class="opcion" onclick="verificar(this, false)">c. What the company planning to invest in venture capital for expansion?</button>
    <button class="opcion" onclick="verificar(this, true)">d. Could you tell me if the company is planning to invest in venture capital for expansion?</button>
  </div>

  <div class="pregunta">
    <p><strong>94. Choose the correct superlative form: «Out of all the options available, this software is considered the ( … )».</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. user-friendliest</button>
    <button class="opcion" onclick="verificar(this, false)">b. more user-friendly</button>
    <button class="opcion" onclick="verificar(this, true)">c. most user-friendly</button>
    <button class="opcion" onclick="verificar(this, false)">d. user-friendlyest</button>
  </div>

  <div class="pregunta">
    <p><strong>95. Choose the correct superlative form: «Maria is known as the ( … ) salesperson on the team».</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. more productive</button>
    <button class="opcion" onclick="verificar(this, true)">b. most productive</button>
    <button class="opcion" onclick="verificar(this, false)">c. productiveest</button>
    <button class="opcion" onclick="verificar(this, false)">d. productiveer</button>
  </div>

  <div class="pregunta">
    <p><strong>96. What economic system involves private ownership and operation of trade and industry for profit?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. Arbitrage</button>
    <button class="opcion" onclick="verificar(this, false)">b. Stockholder</button>
    <button class="opcion" onclick="verificar(this, true)">c. Capitalism</button>
    <button class="opcion" onclick="verificar(this, false)">d. Globalization</button>
  </div>

  <div class="pregunta">
    <p><strong>97. Which term refers to the increased interaction and integration among countries, businesses, and people on a global scale?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. Arbitrage</button>
    <button class="opcion" onclick="verificar(this, false)">b. Stockholder</button>
    <button class="opcion" onclick="verificar(this, true)">c. Globalization</button>
    <button class="opcion" onclick="verificar(this, false)">d. Capitalism</button>
  </div>

  <div class="pregunta">
    <p><strong>98. What practice involves buying and selling goods or services in different markets to take advantage of price differences?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. Capitalism</button>
    <button class="opcion" onclick="verificar(this, false)">b. Globalization</button>
    <button class="opcion" onclick="verificar(this, true)">c. Arbitrage</button>
    <button class="opcion" onclick="verificar(this, false)">d. Stockholder</button>
  </div>

  <div class="pregunta">
    <p><strong>99. Who is an individual who owns shares in a company and has a financial interest in its success?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. Capitalism</button>
    <button class="opcion" onclick="verificar(this, false)">b. Arbitrage</button>
    <button class="opcion" onclick="verificar(this, true)">c. Stockholder</button>
    <button class="opcion" onclick="verificar(this, false)">d. Globalization</button>
  </div>

  <div class="pregunta">
    <p><strong>100. If we invest in research and development, more people ( … ) discover new innovative solutions.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a. will</button>
    <button class="opcion" onclick="verificar(this, false)">b. can</button>
    <button class="opcion" onclick="verificar(this, false)">c. would</button>
    <button class="opcion" onclick="verificar(this, false)">d. should</button>
  </div>

  <div class="pregunta">
    <p><strong>101. If we challenged the status quo, we ( … ) break new ground in innovation.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. can</button>
    <button class="opcion" onclick="verificar(this, false)">b. could</button>
    <button class="opcion" onclick="verificar(this, false)">c. must</button>
    <button class="opcion" onclick="verificar(this, true)">d. would</button>
  </div>

  <div class="pregunta">
    <p><strong>102. If the government encourages entrepreneurship and innovation, more businesses ( … ) start.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. should</button>
    <button class="opcion" onclick="verificar(this, false)">b. would</button>
    <button class="opcion" onclick="verificar(this, true)">c. will</button>
    <button class="opcion" onclick="verificar(this, false)">d. can</button>
  </div>

  <div class="pregunta">
    <p><strong>103. If we collaborate with people from different disciplines, we ( … ) come up with more creative solutions.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. could</button>
    <button class="opcion" onclick="verificar(this, false)">b. should</button>
    <button class="opcion" onclick="verificar(this, true)">c. will</button>
    <button class="opcion" onclick="verificar(this, false)">d. can</button>
  </div>

  <div class="pregunta">
    <p><strong>104. If we developed new technologies, we ( … ) reduce our environmental impact.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. must</button>
    <button class="opcion" onclick="verificar(this, false)">b. can</button>
    <button class="opcion" onclick="verificar(this, true)">c. would</button>
    <button class="opcion" onclick="verificar(this, false)">d. should</button>
  </div>

  <div class="pregunta">
    <p><strong>105. The company is using ( … ) innovation to quickly develop new products and services.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. reliable</button>
    <button class="opcion" onclick="verificar(this, false)">b. dynamic</button>
    <button class="opcion" onclick="verificar(this, true)">c. agile</button>
    <button class="opcion" onclick="verificar(this, false)">d. fast</button>
  </div>

  <div class="pregunta">
    <p><strong>106. The team is working on a ( … ) innovation that will transform the way people interact with technology.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. innovative</button>
    <button class="opcion" onclick="verificar(this, true)">b. disruptive</button>
    <button class="opcion" onclick="verificar(this, false)">c. established</button>
    <button class="opcion" onclick="verificar(this, false)">d. groundbreaking</button>
  </div>

  <div class="pregunta">
    <p><strong>107. The company is open to ( … ) by collaborating with other companies and individuals to generate new ideas.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. collaborative</button>
    <button class="opcion" onclick="verificar(this, true)">b. innovation</button>
    <button class="opcion" onclick="verificar(this, false)">c. exclusive</button>
    <button class="opcion" onclick="verificar(this, false)">d. individualistic</button>
  </div>

  <div class="pregunta">
    <p><strong>108. The company is using ( … ) design to ensure that its products meet the needs of its customers.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a. user-centred</button>
    <button class="opcion" onclick="verificar(this, false)">b. standardised</button>
    <button class="opcion" onclick="verificar(this, false)">c. generic</button>
    <button class="opcion" onclick="verificar(this, false)">d. personalised</button>
  </div>

  <div class="pregunta">
    <p><strong>109. The company is creating a ( … ) of the new product to test it with potential customers.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. imitation</button>
    <button class="opcion" onclick="verificar(this, false)">b. replica</button>
    <button class="opcion" onclick="verificar(this, true)">c. prototype</button>
    <button class="opcion" onclick="verificar(this, false)">d. blueprint</button>
  </div>

  <div class="pregunta">
    <p><strong>110. The door ( … ) I was trying to open was locked.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. who</button>
    <button class="opcion" onclick="verificar(this, false)">b. where</button>
    <button class="opcion" onclick="verificar(this, true)">c. which</button>
    <button class="opcion" onclick="verificar(this, false)">d. whose</button>
  </div>

  <div class="pregunta">
    <p><strong>111. The police officer ( … ) arrested the suspect was praised for his bravery.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. which</button>
    <button class="opcion" onclick="verificar(this, true)">b. who</button>
    <button class="opcion" onclick="verificar(this, false)">c. whose</button>
    <button class="opcion" onclick="verificar(this, false)">d. where</button>
  </div>

  <div class="pregunta">
    <p><strong>112. The computer ( … ) was stolen contained confidential information.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a. which</button>
    <button class="opcion" onclick="verificar(this, false)">b. who</button>
    <button class="opcion" onclick="verificar(this, false)">c. where</button>
    <button class="opcion" onclick="verificar(this, false)">d. whose</button>
  </div>

  <div class="pregunta">
    <p><strong>113. The security guard said: «I saw a suspicious person entering the building».</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. The security guard said that he had been robbed at gunpoint.</button>
    <button class="opcion" onclick="verificar(this, false)">b. The security guard asked if a suspicious person was entering the building.</button>
    <button class="opcion" onclick="verificar(this, true)">c. The security guard reported that he had seen a suspicious person entering the building.</button>
    <button class="opcion" onclick="verificar(this, false)">d. The security guard warned that a suspicious person was entering the building.</button>
  </div>

  <div class="pregunta">
    <p><strong>114. The police officer warned: «Be careful, the area is not safe».</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. The police officer said that he had been robbed at gunpoint.</button>
    <button class="opcion" onclick="verificar(this, false)">b. The police officer reported that the area was not safe.</button>
    <button class="opcion" onclick="verificar(this, false)">c. The police officer warned that he had seen a suspicious person entering the building.</button>
    <button class="opcion" onclick="verificar(this, true)">d. The police officer said that the area was not safe.</button>
  </div>

  <div class="pregunta">
    <p><strong>115. ( … ) is a technique used by attackers to trick users into revealing confidential information or taking actions that compromise their security.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. Password policy</button>
    <button class="opcion" onclick="verificar(this, false)">b. Firewall</button>
    <button class="opcion" onclick="verificar(this, false)">c. Intrusion prevention system</button>
    <button class="opcion" onclick="verificar(this, true)">d. Social engineering</button>
  </div>

  <div class="pregunta">
    <p><strong>116. ( … ) is the process of scrambling data so that it cannot be read by unauthorised individuals.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. Authentication</button>
    <button class="opcion" onclick="verificar(this, true)">b. Data encryption</button>
    <button class="opcion" onclick="verificar(this, false)">c. Intrusion detection system</button>
    <button class="opcion" onclick="verificar(this, false)">d. Authorisation</button>
  </div>

  <div class="pregunta">
    <p><strong>117. ( … ) is a network security device that filters incoming and outgoing traffic to prevent unauthorised access to a network.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a. Firewall</button>
    <button class="opcion" onclick="verificar(this, false)">b. Authentication</button>
    <button class="opcion" onclick="verificar(this, false)">c. Data encryption</button>
    <button class="opcion" onclick="verificar(this, false)">d. Intrusion detection system</button>
  </div>

  <div class="pregunta">
    <p><strong>118. ( … ) is a set of rules that govern the creation and use of passwords.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. Authentication</button>
    <button class="opcion" onclick="verificar(this, false)">b. Data encryption</button>
    <button class="opcion" onclick="verificar(this, true)">c. Password policy</button>
    <button class="opcion" onclick="verificar(this, false)">d. Authorisation</button>
  </div>

  <div class="pregunta">
    <p><strong>119. The new policy ( … ) by the board of directors last week.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. implemented</button>
    <button class="opcion" onclick="verificar(this, true)">b. was implemented</button>
    <button class="opcion" onclick="verificar(this, false)">c. was implementing</button>
    <button class="opcion" onclick="verificar(this, false)">d. implementing</button>
  </div>

  <div class="pregunta">
    <p><strong>120. Our team needs to ( … ) the issues before we can move forward with the project.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. sign off</button>
    <button class="opcion" onclick="verificar(this, false)">b. break even</button>
    <button class="opcion" onclick="verificar(this, false)">c. follow up</button>
    <button class="opcion" onclick="verificar(this, true)">d. iron out</button>
  </div>

  <div class="pregunta">
    <p><strong>121. The report ( … ) by the marketing department next Monday.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a. will be prepared</button>
    <button class="opcion" onclick="verificar(this, false)">b. prepares</button>
    <button class="opcion" onclick="verificar(this, false)">c. is preparing</button>
    <button class="opcion" onclick="verificar(this, false)">d. prepared</button>
  </div>

  <div class="pregunta">
    <p><strong>122. The company decided to ( … ) the project due to budget constraints.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. jump on board</button>
    <button class="opcion" onclick="verificar(this, false)">b. move forward</button>
    <button class="opcion" onclick="verificar(this, false)">c. wrap up</button>
    <button class="opcion" onclick="verificar(this, true)">d. hold off on</button>
  </div>

  <div class="pregunta">
    <p><strong>123. Important decisions ( … ) during yesterday’s meeting.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a. were made</button>
    <button class="opcion" onclick="verificar(this, false)">b. were making</button>
    <button class="opcion" onclick="verificar(this, false)">c. made</button>
    <button class="opcion" onclick="verificar(this, false)">d. make</button>
  </div>

  <div class="pregunta">
    <p><strong>124. Our team uses ( … ) to store and share documents securely.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. instant messaging</button>
    <button class="opcion" onclick="verificar(this, false)">b. social media</button>
    <button class="opcion" onclick="verificar(this, true)">c. project management software</button>
    <button class="opcion" onclick="verificar(this, false)">d. webinar</button>
  </div>

  <div class="pregunta">
    <p><strong>125. The marketing department regularly hosts (…) to promote new products.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. collaboration platform</button>
    <button class="opcion" onclick="verificar(this, true)">b. podcast</button>
    <button class="opcion" onclick="verificar(this, false)">c. video conferencing</button>
    <button class="opcion" onclick="verificar(this, false)">d. intranet</button>
  </div>

  <div class="pregunta">
    <p><strong>126. The CEO announced the new company strategy through a ( … ) series.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. podcast</button>
    <button class="opcion" onclick="verificar(this, false)">b. intranet</button>
    <button class="opcion" onclick="verificar(this, false)">c. cloud storage</button>
    <button class="opcion" onclick="verificar(this, true)">d. webinar</button>
  </div>

  <div class="pregunta">
    <p><strong>127. Employees can access company news and resources through the (…).</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. collaboration platform</button>
    <button class="opcion" onclick="verificar(this, false)">b. email</button>
    <button class="opcion" onclick="verificar(this, false)">c. social media</button>
    <button class="opcion" onclick="verificar(this, true)">d. intranet</button>
  </div>

  <div class="pregunta">
    <p><strong>128. We rely on ( … ) to conduct virtual meetings with clients.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a. project management software</button>
    <button class="opcion" onclick="verificar(this, false)">b. cloud storage</button>
    <button class="opcion" onclick="verificar(this, true)">c. video conferencing</button>
    <button class="opcion" onclick="verificar(this, false)">d. instant messaging</button>
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
