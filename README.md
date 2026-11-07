# teaching-philosophy
<meta name="claude:viewport-fit-sides" content="cover">
<title>Teaching Philosophy Inventory</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Newsreader:opsz,wght@6..72,400;6..72,600&family=IBM+Plex+Sans:wght@400;500;600&family=IBM+Plex+Mono:wght@500&display=swap">
<style>
/* Layout: one reading column, a single steel-blue accent, five muted philosophy hues. */
:root {
  --bg: #f5f5f2;
  --surface: #ffffff;
  --ink: #1c2230;
  --muted: #5b6474;
  --line: #d9dce3;
  --accent: #2e4a6b;
  --on-accent: #ffffff;
  --L: #3f5a80;
  --B: #8a6a2f;
  --P: #2f7a58;
  --H: #9a4a6e;
  --R: #a13d2b;
  --display: "Newsreader", Georgia, "Times New Roman", serif;
  --body: "IBM Plex Sans", system-ui, -apple-system, "Segoe UI", sans-serif;
  --mono: "IBM Plex Mono", ui-monospace, Menlo, monospace;
  color-scheme: light;
}
@media (prefers-color-scheme: dark) {
  :root:not([data-theme="light"]) {
    --bg: #14171e;
    --surface: #1c2129;
    --ink: #e7e9ef;
    --muted: #9ba3b3;
    --line: #343c4c;
    --accent: #8fb0d6;
    --on-accent: #10141c;
    --L: #8aa6cf;
    --B: #d4ab62;
    --P: #7fc4a0;
    --H: #d593b3;
    --R: #e38d7a;
    color-scheme: dark;
  }
}
:root[data-theme="dark"] {
  --bg: #14171e;
  --surface: #1c2129;
  --ink: #e7e9ef;
  --muted: #9ba3b3;
  --line: #343c4c;
  --accent: #8fb0d6;
  --on-accent: #10141c;
  --L: #8aa6cf;
  --B: #d4ab62;
  --P: #7fc4a0;
  --H: #d593b3;
  --R: #e38d7a;
  color-scheme: dark;
}

* { box-sizing: border-box; }
body {
  margin: 0;
  background: var(--bg);
  color: var(--ink);
  font: 400 15px/1.6 var(--body);
  padding-left: max(16px, env(safe-area-inset-left, 0px));
  padding-right: max(16px, env(safe-area-inset-right, 0px));
  padding-top: 24px;
  padding-bottom: 64px;
}
main { max-width: 740px; margin: 0 auto; }
h1, h2, h3 { font-family: var(--display); font-weight: 600; text-wrap: balance; margin: 0; }
h1 { font-size: 2.1rem; line-height: 1.15; }
p { margin: 0; }
.eyebrow { font: 500 12px/1 var(--mono); letter-spacing: .08em; text-transform: uppercase; color: var(--muted); }
.lede { color: var(--muted); max-width: 62ch; margin-top: 12px; }

/* Sticky progress band */
.progress {
  position: sticky;
  top: env(safe-area-inset-top, 0px);
  z-index: 5;
  background: var(--bg);
  padding: 12px 0 10px;
  border-bottom: 1px solid var(--line);
  margin-top: 24px;
}
.progress-row { display: flex; justify-content: space-between; gap: 12px; align-items: baseline; flex-wrap: wrap; }
.track { height: 6px; background: var(--line); border-radius: 3px; margin-top: 10px; overflow: hidden; }
#fill { height: 100%; width: 0; background: var(--accent); transition: width .25s ease; }
.count { font: 500 13px/1 var(--mono); color: var(--muted); }

/* How-to key */
.key {
  display: grid; grid-template-columns: repeat(7, minmax(0, 1fr)); gap: 4px;
  margin: 20px 0 6px; font: 500 12px/1.2 var(--mono); color: var(--muted); text-align: center;
}
.key-labels { display: flex; justify-content: space-between; font: 400 13px/1.3 var(--body); color: var(--muted); margin-bottom: 4px; gap: 8px; }

/* Items */
.item { padding: 26px 0; border-bottom: 1px solid var(--line); }
.item h2 { font-size: 1.3rem; line-height: 1.3; display: flex; gap: 12px; align-items: baseline; }
.num { font: 500 13px/1 var(--mono); color: var(--muted); min-width: 2ch; }
.opt { margin-top: 16px; min-width: 0; }
.opt p { margin-bottom: 8px; }
.scale { display: grid; grid-template-columns: repeat(7, minmax(0, 1fr)); gap: 4px; }
.scale button {
  min-height: 40px; border: 1px solid var(--line); background: var(--surface); color: var(--ink);
  border-radius: 6px; font: 500 14px/1 var(--mono); cursor: pointer; padding: 0;
}
.scale button:hover { border-color: var(--accent); }
.scale button:focus-visible { outline: 2px solid var(--accent); outline-offset: 2px; }
.scale button[aria-pressed="true"] { background: var(--accent); border-color: var(--accent); color: var(--on-accent); }

/* Actions */
.actions { display: flex; gap: 12px; align-items: center; flex-wrap: wrap; padding: 28px 0 8px; }
.btn {
  font: 600 15px/1 var(--body); padding: 14px 20px; border-radius: 6px; cursor: pointer;
  border: 1px solid var(--accent); background: var(--accent); color: var(--on-accent);
}
.btn:disabled { opacity: .4; cursor: not-allowed; }
.btn.ghost { background: transparent; color: var(--accent); }
.btn:focus-visible { outline: 2px solid var(--accent); outline-offset: 2px; }
.hint { color: var(--muted); font-size: 14px; }

/* Results */
#results { padding-top: 32px; }
#results[hidden] { display: none; }
.summary { margin-top: 12px; font-size: 16px; }
.rank { margin-top: 22px; display: grid; gap: 12px; }
.rank-row { display: grid; grid-template-columns: minmax(0, 150px) minmax(0, 1fr) 64px; gap: 12px; align-items: center; }
.rank-name { font: 600 14px/1.2 var(--body); }
.rank-bar { height: 14px; background: var(--line); border-radius: 3px; overflow: hidden; }
.rank-bar span { display: block; height: 100%; width: 0; background: var(--ph); transition: width .4s ease; }
.rank-score { font: 500 13px/1 var(--mono); text-align: right; color: var(--muted); }

.note {
  margin-top: 22px; padding: 14px 16px; border-left: 3px solid var(--accent);
  background: var(--surface); border-radius: 0 6px 6px 0; font-size: 14px; line-height: 1.55;
}
.note strong { font-weight: 600; }

.phil {
  margin-top: 20px; padding: 22px 22px 20px; background: var(--surface);
  border: 1px solid var(--line); border-radius: 8px; border-top: 4px solid var(--ph);
  min-width: 0;
}
.phil-head { display: flex; flex-wrap: wrap; gap: 8px 12px; align-items: baseline; justify-content: space-between; }
.phil-title { font-size: 1.6rem; color: var(--ph); }
.badge {
  font: 500 12px/1 var(--mono); letter-spacing: .04em; text-transform: uppercase;
  color: var(--muted); border: 1px solid var(--line); border-radius: 999px; padding: 6px 10px;
}
.phil-focus { font-style: italic; color: var(--muted); margin-top: 6px; }
.phil-desc { margin-top: 12px; max-width: 62ch; }
.lists { display: grid; grid-template-columns: repeat(2, minmax(0, 1fr)); gap: 20px; margin-top: 18px; }
.lists h3 { font: 600 13px/1.2 var(--body); text-transform: uppercase; letter-spacing: .06em; color: var(--muted); margin-bottom: 8px; }
.lists ul { margin: 0; padding-left: 18px; font-size: 14px; line-height: 1.55; }
.lists li + li { margin-top: 6px; }
@media (max-width: 560px) { .lists { grid-template-columns: minmax(0, 1fr); } }
@media (max-width: 480px) {
  .rank-row { grid-template-columns: minmax(0, 1fr) 52px; }
  .rank-bar { grid-column: 1 / -1; grid-row: 2; }
  .rank-name { grid-row: 1; }
}

.why { margin-top: 28px; padding: 22px 22px 20px; background: var(--surface); border: 1px solid var(--line); border-radius: 8px; }
.why h2 { font-size: 1.35rem; }
.why h3 { font: 600 16px/1.3 var(--display); margin-top: 18px; }
.why p { margin-top: 10px; max-width: 64ch; }
.blend { margin-top: 26px; padding: 20px 22px; border: 1px solid var(--line); border-radius: 8px; background: var(--surface); }
.blend h3 { font-size: 1.3rem; }
.blend p { margin-top: 10px; max-width: 64ch; }
.footer-note { margin-top: 36px; color: var(--muted); font-size: 13px; line-height: 1.55; }

@media (prefers-reduced-motion: reduce) { #fill, .rank-bar span { transition: none; } }
</style>

<main>
  <header>
    <p class="eyebrow">Adult education · Philosophy of education</p>
    <h1>Teaching Philosophy Inventory</h1>
    <p class="lede">This short survey helps you see what you believe about how adults learn. There are 15 questions. Each has five possible answers. For each answer, rate how much you agree on a scale from 1 to 7. Think about what you usually do, or about one course you teach. There are no right or wrong answers.</p>

    <section class="why" aria-labelledby="why-title">
      <h2 id="why-title">Why your teaching philosophy matters</h2>
      <p>Every teacher has beliefs about learning, even if they have never named them. Those beliefs decide what you teach first, how you run class, what counts as success, and how you respond when a learner gets lost or loses interest.</p>
      <p>When you know your philosophy, your choices become deliberate instead of accidental. You can explain why you did something, notice when a method is not working, and change course with a reason. New instructors often copy the teacher they had, which may not fit their learners. Knowing your beliefs gives you a starting point you can test and improve.</p>
    </section>

    <div class="key-labels"><span>1 · Strongly disagree</span><span>4 · Neutral</span><span>7 · Strongly agree</span></div>
    <div class="key" aria-hidden="true"><span>1</span><span>2</span><span>3</span><span>4</span><span>5</span><span>6</span><span>7</span></div>
  </header>

  <div class="progress">
    <div class="progress-row">
      <span class="count" id="count">0 of 75 rated</span>
      <span class="hint">Every option needs a rating to see results.</span>
    </div>
    <div class="track"><div id="fill"></div></div>
  </div>

  <form id="items" onsubmit="return false"></form>

  <div class="actions">
    <button class="btn" id="submit" type="button" disabled>See my results</button>
    <span class="hint" id="remaining">75 options left to rate</span>
  </div>

  <section id="results" hidden aria-live="polite">
    <p class="eyebrow">Your results</p>
    <h2 style="font-size:1.8rem; margin-top:8px;">Where you place</h2>
    <p class="summary" id="summary"></p>
    <div class="rank" id="rank"></div>
    <div id="note"></div>
    <div id="cards"></div>
    <div class="actions">
      <button class="btn ghost" id="retake" type="button">Retake the inventory</button>
    </div>
    <section class="blend" aria-labelledby="blend-title">
      <h3 id="blend-title">What this means for you: a blended approach</h3>
      <p>Your results are a mix, not a single label. Your top one or two philosophies show your natural style. Use them as your home base. Then draw on the others when the class calls for it. For example, if you lean toward structure, you can still invite learners to share real experiences. If you lean toward discussion, you can add clear practice when a new skill needs repetition.</p>
      <p>Adults usually learn best when a class uses several approaches. Start with what they need to do, connect it to problems they face at work or home, give them room to choose their path, and check that they can actually do the thing by the end.</p>
    </section>
    <p class="footer-note">Each score ranges from 15 to 105. Most teachers lean toward one or two philosophies. Your highest score is the view closest to your beliefs, and your lowest is the view furthest from them. The survey describes what you believe. It does not judge it. Use the results to see how your beliefs shape your choices, and where they fit the adults you teach.</p>
  </section>
</main>

<script>
// Each option is [text, code]. Codes: L liberal, B behaviorist, P progressive, H humanistic, R radical.
const PHIL = {
  L: { name: "Liberal", focus: "Teaching for understanding", color: "var(--L)" },
  B: { name: "Behaviorist", focus: "Teaching for skills and results", color: "var(--B)" },
  P: { name: "Progressive", focus: "Teaching by solving real problems", color: "var(--P)" },
  H: { name: "Humanistic", focus: "Teaching for personal growth", color: "var(--H)" },
  R: { name: "Radical", focus: "Teaching for social change", color: "var(--R)" }
};

const DETAIL = {
  L: {
    desc: "The teacher is an expert who explains ideas in a clear order. The goal is to help learners understand the big ideas behind a subject and think carefully about them. “Liberal” here means the traditional arts and sciences approach to education, not political views.",
    strengths: [
      "Gives learners a solid, well-organized understanding of a subject",
      "Teaches learners to think clearly and reason through problems",
      "Keeps content accurate and thorough",
      "Prepares learners to keep studying on their own"
    ],
    weaknesses: [
      "Can feel far away from what adults need on the job right now",
      "May not give learners enough chances to practice or apply ideas",
      "Puts the teacher at the center of the room",
      "Can leave out voices and experiences that are not in the standard materials"
    ]
  },
  B: {
    desc: "Learning means being able to do something specific. The teacher sets clear goals, gives plenty of practice, and tells learners right away how they did. The aim is for everyone to reach the same standard.",
    strengths: [
      "Goals are clear, so learners know what success looks like",
      "Works well for teaching steps, procedures, and hands-on skills",
      "Regular practice and feedback lead to steady results",
      "Good for training where safety or certification matters"
    ],
    weaknesses: [
      "Can focus so much on doing that learners do not understand why",
      "Leaves little room for learners' own interests or choices",
      "Learners may follow the steps without being able to adapt them",
      "Skills can fade if learners do not keep practicing in new settings"
    ]
  },
  P: {
    desc: "Learning starts with a real problem. The teacher finds out what learners need, then builds activities that let them solve problems like the ones they face. Adults learn by using what they know in situations they already deal with.",
    strengths: [
      "Learners see right away how the lesson helps them at work or home",
      "Skills carry over to new situations",
      "Builds problem-solving skills by doing",
      "Uses the experience adults already bring to the room"
    ],
    weaknesses: [
      "Basic facts and background knowledge can get skipped",
      "Harder to measure the same results across every group",
      "Depends on choosing good problems, and weak ones waste time",
      "Usually takes longer than a straight lecture"
    ]
  },
  H: {
    desc: "Learning is about the whole person and their own growth. The teacher acts as a guide or helper, not the boss. The class feels safe, learners choose much of what they study, and they take charge of their own progress.",
    strengths: [
      "Learners feel more motivated because they chose the goals",
      "Matches how adults prefer to learn: on their own terms and from their own experience",
      "Pays attention to how learners feel, which keeps them engaged",
      "Easy to adjust for different people"
    ],
    weaknesses: [
      "Hard to tell objectively whether learners have mastered something",
      "Important content or skills can get missed",
      "Works best when learners are ready to guide themselves",
      "Hard to use in required training with set rules"
    ]
  },
  R: {
    desc: "Learning looks at how society works, including who has power and who does not. The teacher helps learners question what they take for granted and think about how to make things better, in their work and their communities.",
    strengths: [
      "Connects lessons to fairness and to learners' role in their communities",
      "Helps learners question assumptions they have never examined",
      "Draws on learners' own experiences and values",
      "Prepares learners to speak up and improve the systems they work in"
    ],
    weaknesses: [
      "Can drift into pushing the teacher's own views",
      "Often uncomfortable in workplaces and military settings with set rules",
      "Less focus on building specific technical skills",
      "Hard to measure, and learners who disagree may tune out"
    ]
  }
};

// 15 items. Each has five options, in the order printed on the inventory.
const ITEMS = [
  { stem: "In planning an educational activity, I am most likely to:", opts: [
    ["Identify, in conjunction with learners, significant social and/or political issues and plan learning activities around them.", "R"],
    ["Clearly identify the results I want and develop a program that will achieve those results.", "B"],
    ["Begin with a lesson plan that organizes what I plan to teach, and how.", "L"],
    ["Assess learners’ needs and develop valid learning activities based on those needs.", "P"],
    ["Consider the areas of greatest interest to the learners and plan to deal with them, regardless of what they may be.", "H"]] },
  { stem: "People learn best:", opts: [
    ["When the new knowledge is presented from a problem-solving approach.", "P"],
    ["When the learning activity is clearly structured and provides for practice and repetition.", "B"],
    ["Through dialogue or discussion with other learners and a group coordinator.", "R"],
    ["When they are free to explore, without the constraints of a “system”.", "H"],
    ["From an “expert” who knows what s/he is talking about.", "L"]] },
  { stem: "The primary purpose of education is:", opts: [
    ["To facilitate personal development on the part of the learner.", "H"],
    ["To increase learners’ awareness of the need for social change and to enable them to effect such change.", "R"],
    ["To develop conceptual or theoretical understanding.", "L"],
    ["To establish the learners’ capacity to solve individual and societal problems.", "P"],
    ["To develop the learners’ competency and mastery of specific knowledge and skills.", "B"]] },
  { stem: "Most of what people know:", opts: [
    ["Is a result of consciously pursuing their goals, solving problems as they go.", "P"],
    ["They have learned through critical or reflective thinking focused on important social and political issues.", "R"],
    ["They have learned through a trial-and-feedback process.", "B"],
    ["They have gained through self-discovery rather than some “teaching process”.", "H"],
    ["They have acquired through a systematic or comprehensive process.", "L"]] },
  { stem: "Decisions about what to include in a lesson or learning activity:", opts: [
    ["Should be made mostly by the learner in consultation with a facilitator.", "H"],
    ["Should be based on what learners know and what the teacher believes they should know at the end of the activity.", "B"],
    ["Should be based on a consideration of key social, political, and/or cultural situations.", "R"],
    ["Should be based on a consideration of the learners’ needs, interests, and problems.", "P"],
    ["Should be based on careful analysis by the teacher of the material to be covered and the concepts to be taught.", "L"]] },
  { stem: "Good educators start planning instruction:", opts: [
    ["By considering the end behaviors or specific outcomes they are looking for and the most efficient ways of producing them in learners.", "B"],
    ["By identifying everyday problems (or other problems) that can be solved as a result of the instruction.", "P"],
    ["By clarifying the content, concepts, and/or theoretical principles to be taught.", "L"],
    ["By clarifying key social and political issues that affect the lives of the learners.", "R"],
    ["By asking learners to identify what they want to learn and how they want to learn it.", "H"]] },
  { stem: "As an educator, I am most successful in situations:", opts: [
    ["That are unstructured and flexible enough to follow learners’ interests.", "H"],
    ["That are fairly structured, with clear learning objectives and built-in feedback to the learners.", "B"],
    ["Where I can focus on practical skills and knowledge that can be put to use in solving problems.", "P"],
    ["Where the scope of the new material is fairly clear and the subject matter is logically organized.", "L"],
    ["Where the learners have some awareness of social and political issues and are willing to explore the impact of such issues on their daily lives.", "R"]] },
  { stem: "In planning an educational activity, I try to create:", opts: [
    ["The real world – problems and all – and to develop learners’ capacities for dealing with it.", "P"],
    ["A setting in which learners are encouraged to examine their beliefs and values and to raise critical questions.", "R"],
    ["A controlled environment that attracts and holds the learners, moving them systematically toward the objectives.", "B"],
    ["A clear outline of the content and the concepts to be taught or learned.", "L"],
    ["A supportive climate that facilitates self-discovery and interaction.", "H"]] },
  { stem: "The learners’ feelings during the learning process:", opts: [
    ["Must be brought to the surface in order for learners to become truly involved in their learning.", "R"],
    ["Provide energy that can be focused on problems or questions.", "P"],
    ["Will probably have a great deal to do with the way they approach their learning.", "H"],
    ["Are used by the skillful adult educator to accomplish the learning objectives.", "B"],
    ["Are likely to get in the way of teaching and learning by diverting the learners’ attention.", "L"]] },
  { stem: "The teaching methods I prefer to use:", opts: [
    ["Focus on problem solving and present real challenges to the learner.", "P"],
    ["Emphasize practice and feedback to the learner.", "B"],
    ["Are mostly non-directive, encouraging the learner to take responsibility for his/her own learning.", "H"],
    ["Involve learners in dialogue or discussion and critical examination of controversial issues.", "R"],
    ["Are determined primarily by the subject or content to be covered.", "L"]] },
  { stem: "When learners are uninterested in a subject, it is probably because:", opts: [
    ["They do not realize how serious the consequences of not understanding or not learning the subject may be.", "R"],
    ["They do not see any benefit for their daily lives.", "P"],
    ["The teacher does not know enough about the subject or is unable to make it interesting to the learner.", "L"],
    ["They are not getting adequate practice or feedback during the learning process.", "B"],
    ["They are not ready to learn it or it is not a high priority for them personally.", "H"]] },
  { stem: "Differences among learners:", opts: [
    ["Are relatively unimportant as long as the learners gain a common base of understanding through the learning experience.", "L"],
    ["Enable them to learn best on their own over time and in their own way.", "H"],
    ["Are primarily due to the differences in their life experiences, and will usually lead them to make different applications of new knowledge and skills to their own situations.", "P"],
    ["Arise from their particular cultural and social situations and should not be minimized even as they recognize common needs and problems.", "R"],
    ["Will not interfere with their learning if each learner is given adequate opportunity for practice and reinforcement.", "B"]] },
  { stem: "Evaluation of learning outcomes:", opts: [
    ["Is not of great importance and may not be possible, because the impact of learning may not be evident until much later.", "R"],
    ["Should be built into the system, so that learners will continually receive feedback and can adjust their performance accordingly.", "B"],
    ["Is best done by the learners themselves, for their own purposes.", "H"],
    ["Lets me know how much learners have increased their conceptual understanding of the new material.", "L"],
    ["Is best accomplished when the learner encounters a problem, either in the learning setting or the real world, and successfully resolves it.", "P"]] },
  { stem: "My primary role as a teacher is to:", opts: [
    ["Guide students through structured learning with well directed feedback.", "B"],
    ["Systematically lead students in acquiring new information and understanding underlying theories and concepts.", "L"],
    ["Help learners to identify and solve problems, or solve them better.", "P"],
    ["Help learners’ awareness of environmental, social, and/or political issues and help them learn how to have an impact on these situations.", "R"],
    ["Facilitate, but not direct, learning activities.", "H"]] },
  { stem: "In the end, if learners have not learned what was taught:", opts: [
    ["The teacher has not actually “taught”.", "L"],
    ["The need to repeat the experience, or a portion of it.", "B"],
    ["They may have learned something else which they consider just as interesting or useful.", "H"],
    ["They do not realize how learning will enable them to significantly influence society.", "R"],
    ["It is probably because they are unable to make practical application of the new knowledge to problems in their daily lives.", "P"]] }
];

// Flatten to 75 options; each item has exactly one option per philosophy.
const OPT_PHIL = [];
ITEMS.forEach(item => item.opts.forEach(o => OPT_PHIL.push(o[1])));
const TOTAL = OPT_PHIL.length; // 75
const answers = new Array(TOTAL).fill(null);

const form = document.getElementById("items");
ITEMS.forEach((item, i) => {
  const sec = document.createElement("section");
  sec.className = "item";
  sec.setAttribute("aria-labelledby", "item-" + i);
  let html = `<h2 id="item-${i}"><span class="num">${String(i + 1).padStart(2, "0")}</span><span>${item.stem}</span></h2>`;
  item.opts.forEach((o, j) => {
    const id = i * 5 + j;
    let scale = "";
    for (let n = 1; n <= 7; n++) {
      scale += `<button type="button" data-id="${id}" data-v="${n}" aria-pressed="false" aria-label="${n} for option ${j + 1}">${n}</button>`;
    }
    html += `<div class="opt"><p>${o[0]}</p><div class="scale" role="group" aria-label="Rating, 1 to 7">${scale}</div></div>`;
  });
  sec.innerHTML = html;
  form.appendChild(sec);
});

form.addEventListener("click", e => {
  const b = e.target.closest("button[data-id]");
  if (!b) return;
  const id = Number(b.dataset.id);
  answers[id] = Number(b.dataset.v);
  b.parentNode.querySelectorAll("button").forEach(x => x.setAttribute("aria-pressed", String(x === b)));
  updateProgress();
});

const submitBtn = document.getElementById("submit");
function updateProgress() {
  const done = answers.filter(v => v !== null).length;
  document.getElementById("count").textContent = `${done} of ${TOTAL} rated`;
  document.getElementById("fill").style.width = (done / TOTAL * 100) + "%";
  document.getElementById("remaining").textContent = done === TOTAL
    ? "All options rated"
    : `${TOTAL - done} option${TOTAL - done === 1 ? "" : "s"} left to rate`;
  submitBtn.disabled = done !== TOTAL;
}

// Scoring: each philosophy's score is the sum of its 15 ratings (15 to 105).
function scoreAll() {
  const totals = { L: 0, B: 0, P: 0, H: 0, R: 0 };
  answers.forEach((v, id) => { totals[OPT_PHIL[id]] += v; });
  return totals;
}

const INCOMPATIBLE = [["L", "R"], ["B", "H"]];
const COMPATIBLE = [["L", "B"], ["P", "H"], ["P", "R"], ["H", "R"]];

function renderResults() {
  const totals = scoreAll();
  const order = Object.keys(totals).sort((a, b) => totals[b] - totals[a]);
  const [first, second] = order;

  document.getElementById("summary").textContent =
    `Your strongest orientation is ${PHIL[first].name.toLowerCase()} (${PHIL[first].focus.toLowerCase()}), with ${PHIL[second].name.toLowerCase()} as the next strongest.`;

  document.getElementById("rank").innerHTML = order.map(k => `
    <div class="rank-row" style="--ph:${PHIL[k].color}">
      <span class="rank-name">${PHIL[k].name}</span>
      <div class="rank-bar" role="img" aria-label="${PHIL[k].name} score ${totals[k]} of 105"><span data-w="${(totals[k] / 105 * 100).toFixed(1)}"></span></div>
      <span class="rank-score">${totals[k]} / 105</span>
    </div>`).join("");

  // Notes on the pattern of scores, following the inventory's guidance.
  const pair = [first, second].sort().join("");
  const notes = [];
  const isIncompat = INCOMPATIBLE.some(p => p.slice().sort().join("") === pair);
  const isCompat = COMPATIBLE.some(p => p.slice().sort().join("") === pair);
  if (isIncompat) {
    notes.push(`<strong>Your top two pull in different directions.</strong> ${PHIL[first].name} and ${PHIL[second].name} hold beliefs that often clash. Think about which one should guide you when they disagree, such as when a class wants structure but the learners want freedom.`);
  } else if (isCompat) {
    notes.push(`<strong>Your top two work well together.</strong> ${PHIL[first].name} and ${PHIL[second].name} are a common pairing, and their ideas tend to support each other in the classroom.`);
  }
  const spread = totals[order[0]] - totals[order[2]];
  if (spread <= 5) {
    notes.push(`<strong>Your top three scores are close.</strong> Your beliefs may still be taking shape. Think about what matters most to you as a teacher, and which answers felt hardest to rate.`);
  }
  const noteEl = document.getElementById("note");
  noteEl.innerHTML = notes.map(n => `<div class="note">${n}</div>`).join("");

  document.getElementById("cards").innerHTML = order.map((k, idx) => {
    const d = DETAIL[k];
    const label = idx === 0 ? "Primary" : idx === 1 ? "Secondary" : `Rank ${idx + 1}`;
    return `
    <article class="phil" style="--ph:${PHIL[k].color}">
      <div class="phil-head">
        <h3 class="phil-title">${PHIL[k].name}</h3>
        <span class="badge">${label} · ${totals[k]} / 105</span>
      </div>
      <p class="phil-focus">${PHIL[k].focus}</p>
      <p class="phil-desc">${d.desc}</p>
      <div class="lists">
        <div><h3>Strengths</h3><ul>${d.strengths.map(s => `<li>${s}</li>`).join("")}</ul></div>
        <div><h3>Weaknesses</h3><ul>${d.weaknesses.map(s => `<li>${s}</li>`).join("")}</ul></div>
      </div>
    </article>`;
  }).join("");

  const res = document.getElementById("results");
  res.hidden = false;
  res.querySelectorAll(".rank-bar span").forEach(s => {
    requestAnimationFrame(() => { s.style.width = s.dataset.w + "%"; });
  });
  res.scrollIntoView({ behavior: "smooth", block: "start" });
}

submitBtn.addEventListener("click", renderResults);

document.getElementById("retake").addEventListener("click", () => {
  answers.fill(null);
  form.querySelectorAll("button[aria-pressed='true']").forEach(b => b.setAttribute("aria-pressed", "false"));
  document.getElementById("results").hidden = true;
  updateProgress();
  window.scrollTo({ top: 0, behavior: "smooth" });
});

updateProgress();
</script>
