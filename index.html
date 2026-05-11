import { useState, useEffect, useRef, useCallback } from "react";

const Fonts = () => {
  useEffect(() => {
    const l = document.createElement("link");
    l.href = "https://fonts.googleapis.com/css2?family=DM+Sans:ital,wght@0,300;0,400;0,500;0,600;0,700;1,400&family=DM+Mono:wght@400;500&family=DM+Serif+Display:ital@0;1&display=swap";
    l.rel = "stylesheet"; document.head.appendChild(l);
    const s = document.createElement("style");
    s.textContent = `
      *{box-sizing:border-box;margin:0;padding:0}
      :root{
        --bg:#F5F4F0; --white:#FFFFFF; --s1:#F0EEE9; --s2:#E8E5DE; --s3:#DEDAD2;
        --border:#D8D5CC; --border2:#C8C5BA;
        --ink:#16150E; --ink2:#2C2B22; --ink3:#585650; --ink4:#888678; --ink5:#B8B6AE;
        --navy:#162C54; --navy2:#1E3A6E; --nb:#EAF0FA; --nm:#B4C8F0; --nlight:#F0F4FD;
        --teal:#0B6858; --tb:#E4F3F0; --tm:#88CAC0;
        --amber:#8A5000; --ab:#FAF4E4; --am:#DFC060;
        --red:#B02E18; --rb:#FBF0EC; --rm:#E8B0A0;
        --green:#1A5630; --gb:#EAF5EE; --gm:#98D0A8;
        --gold:#7A4800; --goldb:#FBF5E4; --goldm:#D4A840;
        --font:'DM Sans',sans-serif;
        --font-m:'DM Mono',monospace;
        --font-d:'DM Serif Display',serif;
      }
      @keyframes fadeUp{from{opacity:0;transform:translateY(7px)}to{opacity:1;transform:translateY(0)}}
      @keyframes pulse{0%,100%{opacity:.4}50%{opacity:1}}
      @keyframes slideIn{from{opacity:0;transform:translateX(-5px)}to{opacity:1;transform:translateX(0)}}
      @keyframes shimmer{0%{background-position:-200% 0}100%{background-position:200% 0}}
      .au{animation:fadeUp .26s ease forwards}
      .si{animation:slideIn .2s ease forwards}
      .pulse{animation:pulse 2s ease infinite}
      ::-webkit-scrollbar{width:5px;height:5px}
      ::-webkit-scrollbar-track{background:var(--s1)}
      ::-webkit-scrollbar-thumb{background:var(--border2);border-radius:3px}
      button:focus-visible{outline:2px solid var(--navy);outline-offset:2px}
    `;
    document.head.appendChild(s);
  }, []);
  return null;
};

// ─── GLOSSARY ─────────────────────────────────────────────────────────────────
const GLOSSARY = [
  { term:"API",              plain:"The channel through which different software systems automatically send and receive data. When Gong finishes a call recording, it sends data to this pipeline via an API.", category:"Infrastructure" },
  { term:"Webhook",          plain:"An automatic notification one system sends to another the moment something happens. Gong 'knocks on the door' to say a call just ended, Intercom 'knocks' when a ticket closes.", category:"Infrastructure" },
  { term:"LLM",              plain:"Large Language Model — the AI (Claude) that reads and understands text the way a skilled analyst would. It finds meaning, identifies patterns, and extracts structured information from raw transcripts.", category:"AI" },
  { term:"Root Cause",       plain:"The real underlying problem, not just what the customer asked for. A customer saying 'we need a dashboard' has a root cause: they can't access or trust their data without leaving the platform.", category:"AI" },
  { term:"Confidence Score", plain:"How certain the AI is about a finding, shown as a percentage. 90% means the system is very sure. Below 70% means a human should review before trusting the result.", category:"AI" },
  { term:"Pattern Frequency",plain:"How many separate companies are describing the same underlying problem. One customer is a data point. Five different customers saying the same thing is a pattern — that's what moves roadmaps.", category:"Intelligence" },
  { term:"Velocity",         plain:"How quickly a problem is growing. A pattern appearing in 2 conversations this week vs. 1 last week has 2× velocity — it's accelerating and needs attention before it becomes widespread.", category:"Intelligence" },
  { term:"Solo Signal",      plain:"A serious complaint from one customer that deserves Product Leadership attention even though it hasn't appeared from others yet. A compliance requirement is just as urgent if only one customer raised it.", category:"Intelligence" },
  { term:"PM Validation",    plain:"A Product Manager reviewing and confirming what the AI found. Each approval or correction teaches the system to be more accurate — so it gets smarter over time.", category:"Quality" },
  { term:"Golden Test Set",  plain:"A group of 20 pre-verified conversations used to check system accuracy before every change. If accuracy drops, the change is blocked. This protects the quality of everything Product Leadership sees.", category:"Quality" },
  { term:"Semantic Clustering",plain:"Grouping similar ideas together even when customers use different words. 'Jira keeps breaking' and 'integration instability' get recognized as the same problem.", category:"AI" },
  { term:"Outcome Confidence",plain:"Did the fix actually work? After a product change ships, the system tracks whether customers stop mentioning the problem. This tells Product Leadership whether their decision had the intended impact.", category:"Intelligence" },
];

// ─── CORE DATA ────────────────────────────────────────────────────────────────
const PM_VALUE_PROPS = [
  { icon:"📌", plain:"Evidence for every roadmap decision", technical:"Frequency-ranked pattern registry with verbatim quote anchors",
    before:"Roadmap priorities are driven by whoever talks loudest in the room, or by the most recent customer complaint.", after:"Every priority is backed by how many separate customers raised the same underlying problem, with their exact words attached.", color:"var(--navy)", bg:"var(--nb)" },
  { icon:"🔍", plain:"The real problem, not just the feature request", technical:"LLM root cause extraction via structured prompt classification",
    before:"Product hears 'we need a better dashboard' and builds a dashboard. The underlying problem never gets solved.", after:"The system translates 'we need a dashboard' into 'customers cannot access or trust their data without leaving the platform' — the actual thing to fix.", color:"var(--teal)", bg:"var(--tb)" },
  { icon:"⚡", plain:"Early warning before problems become widespread", technical:"14-day and 90-day velocity windows with rising pattern alerting",
    before:"Product learns about a growing problem when 8 customers have already been affected and one is about to churn.", after:"A pattern appearing 3× faster than usual triggers an alert before it becomes the dominant complaint in every discovery call.", color:"var(--amber)", bg:"var(--ab)" },
  { icon:"✅", plain:"Proof that what shipped actually worked", technical:"Outcome confidence loop — post-ship sentiment tracking vs. baseline",
    before:"A feature ships. Product Leadership assumes it solved the problem because nobody complained immediately.", after:"60 days after shipping, the system checks: are customers still mentioning this? If yes — the root cause wasn't addressed. If no — confirmed impact.", color:"var(--green)", bg:"var(--gb)" },
];

const ROADMAP_PATTERNS = [
  { rank:1, plain:"Customers can't verify hours before invoices go out", technical:"Approval Workflow Gap — Severity 3, Frequency 4 accounts",
    urgency:"immediate", why_matters:"Every wrong invoice is a trust event between your customer and their client. This isn't an internal ops issue — it's a direct threat to your customer's business relationship.",
    evidence:4, segments:["Mid-market × 2","Enterprise × 2"], competitors:"Harvest already solves this. It comes up in 3 of 4 competitive evaluations.",
    first_action:"Ship multi-level approval routing before Q3. Praxis Group has a September deadline and is comparing Laurel to Harvest head-to-head.",
    workaround:"Senior partners manually review every invoice at month-end — outside Laurel entirely", color:"var(--red)", icon:"🔴",
    quotes:[{ co:"Meridian Law", q:"The approval workflow is table stakes. If you don't have that, this is a short conversation." },{ co:"Praxis Group", q:"Harvest already has the multi-level routing we need. What's your timeline?" }] },
  { rank:2, plain:"The Jira connection breaks quietly — customers find out when invoices are wrong", technical:"Integration Failure — Silent Sync Drop, Severity 3, Frequency 3 accounts",
    urgency:"immediate", why_matters:"The failure pattern is predictable — every Atlassian update breaks it. Holloway & Reed explicitly mentioned Clockify as an alternative. This is an active churn risk, not a future roadmap discussion.",
    evidence:3, segments:["SMB × 2","Mid-market × 1"], competitors:"Clockify is being evaluated as a direct replacement by one account.",
    first_action:"Fix the integration architecture so it doesn't break on Atlassian updates. Add sync failure alerting so customers know before invoices go out.",
    workaround:"DevOps engineers 'babysit' the integration after every Atlassian release; manual CSV re-entry after each outage", color:"var(--red)", icon:"🔴",
    quotes:[{ co:"Holloway & Reed", q:"Second time in a month. Last time took 3 days to fix — can't run a billing team this way." },{ co:"Vantage Studio", q:"Our DevOps person has to babysit it every time Atlassian ships a release." }] },
  { rank:3, plain:"No way to see if a project is going over budget until it's too late", technical:"Budget Visibility Gap — Severity 2–3, Frequency 3 accounts",
    urgency:"this_quarter", why_matters:"Two accounts (Acme Corp, Terrace Analytics) are holding $60,000 in expansion ARR until this ships. The basic burn rate feature exists — but custom thresholds per project type are what's blocking growth.",
    evidence:3, segments:["Mid-market × 1","SMB × 2"], competitors:"No direct competitive threat — this is a Laurel product depth opportunity.",
    first_action:"Ship configurable alert thresholds by engagement type. This unlocks $60k in identified expansion revenue from accounts that are otherwise satisfied.",
    workaround:"PMs build weekly spreadsheets manually; fixed-fee projects tracked entirely outside Laurel", color:"var(--amber)", icon:"🟡",
    quotes:[{ co:"Acme Corp", q:"If we could set 50% and 90% alerts per engagement type, we'd expand to three more teams." },{ co:"Terrace Analytics", q:"Custom thresholds by project type is what's blocking us from bringing our fixed-fee team onto Laurel." }] },
  { rank:4, plain:"Laurel reports by project, but customers bill by client", technical:"Data Model Mismatch — Reporting & Analytics, Severity 2, Frequency 2 accounts",
    urgency:"next_quarter", why_matters:"Professional services firms organize their business around clients, not projects. Every billing cycle requires a manual step outside Laurel to aggregate hours by client. Low urgency today — but it compounds over time as a 'why do we even use this?' frustration.",
    evidence:2, segments:["SMB × 2"], competitors:"No direct churn risk yet — but reduces perceived platform value.",
    first_action:"Add a client-level roll-up view as the default billing report. Two accounts would immediately move their monthly reconciliation back into Laurel.",
    workaround:"Monthly Excel export with manual client aggregation — 30 minutes of extra work per billing cycle per PM", color:"var(--navy)", icon:"🔵",
    quotes:[{ co:"Bricklane Consulting", q:"I have to export to Excel every month to get hours by client. It adds 30 minutes each billing cycle." }] },
];

const PIPELINE_STEPS = [
  { num:"01", plain:"Every customer conversation is captured automatically",
    technical:"Webhook Ingestion → POST /api/v1/interactions",
    tech_plain:"When a Gong call ends or an Intercom ticket closes, that system automatically notifies the pipeline (via webhook) and the conversation is sent for processing. No manual uploads.",
    pm_value:"Product Leadership stops missing signals that happen between quarterly reviews. Every conversation — not just the ones that get escalated — feeds the intelligence layer.",
    what_comes_in:["Gong: Sales calls, discovery calls, QBRs","Intercom: Support tickets, chat threads","Email threads from Customer Success","Slack account channel messages"],
    icon:"📥", color:"var(--navy)" },
  { num:"02", plain:"The system checks whether the conversation is worth analyzing",
    technical:"Quality Gate — Pre-Extraction Scoring (word count · coherence · signal density)",
    tech_plain:"A quick quality check scores the transcript before any AI processing. Conversations below the threshold (too short, no product mentions, incoherent) go to manual review instead of AI extraction.",
    pm_value:"Product Leadership only sees findings from conversations that actually contain signal. Low-quality inputs don't inflate pattern frequency or waste PM review time.",
    checks:["Long enough to contain useful information?","Does it mention Laurel products specifically?","Are customer statements identifiable (not just agent responses)?","Has this exact conversation been processed before?"],
    icon:"🔎", color:"var(--teal)" },
  { num:"03", plain:"The AI finds the real problem underneath what the customer said",
    technical:"LLM Root Cause Extraction via Claude Sonnet — structured JSON output",
    tech_plain:"Claude processes the transcript using a prompt that requires it to identify root causes (not feature requests), extract verbatim quotes, score severity, and document what the customer is doing as a workaround today.",
    pm_value:"Product Leadership receives the structural problem, not a wishlist. When customers ask for a dashboard, the system tells Product the real issue: they can't access or trust their data without leaving the platform.",
    translation:{ surface:"'We need a better dashboard'", root:"Customers cannot access or trust their operational data without leaving the platform", why:"Solving the root cause might mean better data availability, not a new dashboard feature" },
    extracts:["The structural problem — not the customer's proposed solution","Severity: minor friction → deal-breaker (1, 2, or 3)","What the customer is doing right now as a workaround","An exact verbatim quote — never paraphrased or compressed","Business impact: churn risk, expansion blocked, adoption friction, onboarding delay"],
    icon:"🧠", color:"var(--amber)" },
  { num:"04", plain:"The same problem appearing across multiple customers becomes a pattern",
    technical:"Semantic Clustering → Pattern Registry with Velocity Calculation (14d + 90d windows)",
    tech_plain:"Each new finding is compared against the pattern registry using embedding similarity. Matching findings increment the frequency counter. Velocity tracks how quickly each pattern is growing over 14-day rolling windows.",
    pm_value:"Product Leadership sees problems sorted by how many different customers are experiencing them — not by how loudly one customer complained. The pattern that appears at 4 companies is more important than the one company screaming about something else.",
    frequency_logic:"4 companies with the same problem → frequency = 4 (each company counted once regardless of how many times they raised it). This prevents one very vocal customer from artificially inflating a pattern's rank.",
    solo_note:{ plain:"One serious complaint from a single customer gets its own separate track — not filtered by frequency. If Kestrel Advisory has a FINRA compliance requirement, it surfaces to Product Leadership regardless of whether any other customer has mentioned it.", technical:"Solo Signal: severity=3 extractions from accounts with no existing pattern match → independent Signal Track" },
    icon:"🔗", color:"var(--green)" },
  { num:"05", plain:"Product Leadership gets the right signals at the right time",
    technical:"Alert Engine → Slack Webhook notifications + Weekly PM Digest + Quarterly Brief generation",
    tech_plain:"Three delivery mechanisms: real-time Slack alerts for urgent signals (velocity ≥ 1.5×, solo critical signals), a weekly digest surfacing what changed, and a quarterly PM roadmap brief auto-generated from all validated patterns.",
    pm_value:"Product Leadership doesn't have to remember to check the dashboard. Urgent signals come to them. The quarterly brief becomes the evidence base they bring into planning meetings.",
    deliverables:[
      { label:"Real-time Slack alert", desc:"A pattern is appearing 2× faster than usual across multiple customers → Product team is notified immediately", tech:"velocity ≥ 1.5× threshold" },
      { label:"Solo signal escalation", desc:"One company raised a compliance requirement that doesn't match any known pattern → Product Leadership is notified regardless of frequency", tech:"Severity 3 + no pattern match" },
      { label:"Weekly PM digest", desc:"Every Monday: what changed last week, which patterns moved, which accounts flagged new concerns", tech:"Scheduled Slack Workflow + pattern delta computation" },
      { label:"Quarterly roadmap brief", desc:"Auto-generated document: top 4 priorities, frequency evidence, verbatim quotes, recommended first action for each", tech:"Claude API synthesis of validated pattern registry" },
    ],
    icon:"📋", color:"var(--red)" },
  { num:"06", plain:"The system learns whether the decisions Product Leadership made actually worked",
    technical:"Outcome Confidence Loop → PM post-ship prompt → severity weight recalibration",
    tech_plain:"60 days after a Linear issue linked to a pattern closes, PMs receive a prompt: 'Did this fix reduce the frequency of this complaint?' The response updates an outcome_confidence score that feeds back into how the system weights future signals.",
    pm_value:"Product Leadership gets proof of impact — not just completion. If the fix didn't actually reduce the pattern frequency, the team knows immediately rather than discovering it in the next quarterly review.",
    icon:"✅", color:"var(--navy)" },
];

const IMPL_PHASES = [
  { num:"01", label:"Prove the AI reads Laurel conversations accurately", dur:"Weeks 1–2", color:"var(--amber)", bg:"var(--ab)",
    technical:"Extraction Validation + Golden Test Set",
    goal:"Before automating anything, Product Leadership needs to trust the system's output. Two senior PMs grade 10 real conversations — the system must hit 80% accuracy before anything else is built.",
    pm_gets:"Visibility into exactly how accurate the system is on real Laurel conversations before a single thing is automated. No surprises later.",
    what_happens:["Build the basic version — paste a transcript, get structured findings","2 senior PMs grade 10 real Laurel conversations using their own notes as the benchmark","Each finding is graded: right problem? accurate severity? verbatim quote?","80% PM agreement required — not a soft target","20-conversation golden test set locked in: used to check accuracy before every future change"],
    gate:{ plain:"80% PM agreement on 20 test conversations. Zero paraphrased quotes.", technical:"pmConfidence baseline ≥ 0.80 on golden test set. Source type quality floors calibrated. Zero verbatim violations." },
    who:"1 AI engineer + 2 senior PMs", risk:"If we skip this and go straight to automation, we get a fast machine producing the wrong answers — and Product Leadership stops trusting the output after the first planning meeting." },

  { num:"02", label:"Build PM trust before any automation runs", dur:"Weeks 3–6", color:"var(--navy)", bg:"var(--nb)",
    technical:"PM Validation Loop + Empirical Confidence Calibration",
    goal:"Product Managers use the system manually before anything is automated. This is intentional — PMs who paste transcripts themselves understand the system deeply, become internal advocates, and catch problems early.",
    pm_gets:"Direct control over what enters the pattern database. Every finding that influences future roadmap decisions has been reviewed and confirmed by a PM before it counts.",
    what_happens:["PMs paste conversations manually — no automatic processing yet","Every finding is reviewed by a PM before it counts as real data","Each agreement or correction teaches the system to be more accurate over time","Confidence thresholds are calibrated from real data: the auto-approve threshold is set at the level where actual PM agreement is ≥90%, not a guessed number","Legal review of whether sending customer conversation data through AI is permissible — required before automation"],
    gate:{ plain:"At least 3 confirmed patterns. PMs reviewing findings weekly. Legal sign-off in progress.", technical:"pmConfidence scores diverging from 0.5 baseline. Calibration analysis complete. Auto-approve threshold empirically derived. Legal DPA review underway." },
    who:"3 PMs + Legal + PM Ops", risk:"Skipping PM review at this stage means unverified AI findings could contaminate the pattern database that will later drive roadmap decisions." },

  { num:"03", label:"Connect to Gong and Intercom — go fully automatic", dur:"Month 2", color:"var(--teal)", bg:"var(--tb)",
    technical:"Webhook Automation + Duplicate Fingerprinting + PII Redaction Gate",
    goal:"Remove the manual step. Every Gong call and Intercom ticket now flows into the pipeline automatically the moment it ends. Nothing gets missed because someone forgot to paste it.",
    pm_gets:"Coverage of 85%+ of all Gong calls. No more gaps. No more depending on someone's memory. Product Leadership sees signals from conversations they didn't even know happened.",
    what_happens:["Gong sends the pipeline an automatic notification when a call recording is ready — processed within 15 minutes","Intercom sends a notification when a support ticket closes","Duplicate detection: if the same conversation arrives twice, it's flagged and not double-counted","If the AI is slow or a connection fails, the system retries automatically — 3 times, waiting longer between each","Legal sign-off is required before this step — customer conversation data through AI must be cleared","Daily coverage check: how many Gong calls were available yesterday vs. how many were processed"],
    gate:{ plain:"85% of Gong calls processed within 30 minutes. Legal sign-off complete. No silent failures in 48 hours.", technical:"Coverage rate ≥85%. Legal DPA signed. Retry logic validated. PII redaction verified. Webhook health monitoring active." },
    who:"1 engineer + PM Ops + Legal", risk:"The most important thing here is that nothing fails silently. If Gong stops sending notifications, Product Leadership needs to know — not discover a gap three weeks later." },

  { num:"04", label:"Give Product Leadership their dashboard and brief", dur:"Month 3", color:"var(--navy)", bg:"var(--nb)",
    technical:"Pattern Intelligence Layer + Account Threading + Solo Signal Track + Quarterly Brief Engine",
    goal:"This is when the investment pays off for Product Leadership. The dashboard they've requested is live. The quarterly brief they can bring to planning meetings is auto-generated. The system proves its value in a real decision.",
    pm_gets:"A frequency-ranked pattern view. An individual voice track for single-company critical signals. The first auto-generated quarterly roadmap brief. Account-level intelligence for any company they want to investigate.",
    what_happens:["Pattern Intelligence dashboard goes live — patterns ranked by how many different customers raised the same root cause","Solo Signal track — severity-3 individual company concerns surfaced regardless of frequency","First quarterly PM brief auto-generated from the validated pattern database","Account profiles: all conversations with a single company threaded chronologically with sentiment over time","Product Leadership uses the dashboard in a real planning meeting — this is the proof-of-value gate"],
    gate:{ plain:"Product Leadership uses the dashboard in a real planning meeting. At least one pattern influences an actual roadmap decision.", technical:"CPO/VP Product endorsement in planning session. Pattern Track + Solo Signal Track live and validated. First quarterly brief generated and reviewed." },
    who:"Product Leadership (must be in the planning meeting) + CS lead + PM Ops", risk:"If the dashboard doesn't change a real decision, it hasn't done its job. The gate exists specifically to make this non-optional." },

  { num:"05", label:"Connect findings directly to the engineering roadmap", dur:"Months 4–5", color:"var(--gold)", bg:"var(--goldb)",
    technical:"Linear Integration + Outcome Feedback Loop + Quarterly Brief Automation",
    goal:"Eliminate the gap between 'we identified a pattern' and 'there's a task in Linear with supporting evidence.' Product Leadership should be able to trace every roadmap item back to customer evidence, and vice versa.",
    pm_gets:"Patterns automatically create Linear tasks with evidence bundles attached. Quarterly briefs auto-generated with 4 priorities, evidence, quotes, and recommended first actions. Outcome tracking that tells Product Leadership whether what they shipped actually worked.",
    what_happens:["High-priority patterns automatically create tasks in Linear with all supporting evidence attached","Quarterly PM Roadmap Brief auto-generated: 4 priorities max, each with root cause, how many customers raised it, verbatim quote, and a specific first recommended action","60 days after a fix ships, Product Leadership is asked: are customers still raising this? Yes/Partially/No","Expansion revenue from customer signals tracked and reportable — e.g., '$60k in expansion unlocks if custom thresholds ship'"],
    gate:{ plain:"At least 2 of the top 4 quarterly priorities appear on the roadmap. Outcome tracking is actively happening.", technical:"Linear VoC label ≥5 issues reviewed bi-weekly. Outcome confidence updating on closed issues. Expansion ARR reportable to Finance." },
    who:"Product Leadership + Engineering (Linear) + Finance (ARR reporting)", risk:"The outcome loop is the most important long-term investment. Start tagging outcomes now — you need 12 months of data before the scoring formula can recalibrate based on what actually moved the needle." },

  { num:"06", label:"Full deployment — the system gets smarter from its own decisions", dur:"Month 6+", color:"var(--green)", bg:"var(--gb)",
    technical:"Adaptive Calibration + Semantic Deduplication + System Ownership Documentation",
    goal:"Every sales call, support ticket, and customer message is processed automatically. The scoring formula recalibrates based on which high-priority patterns, when fixed, actually improved customer outcomes.",
    pm_gets:"A system that learns what matters from the decisions Product Leadership already made. Patterns that led to successful product fixes score higher in future. Patterns the market stopped raising after a fix score as resolved.",
    what_happens:["All 50 sales reps' calls processed automatically — no coverage gaps","Severity weights adjusted based on 12 months of outcome data: which problems, when fixed, actually made customers happier?","Pattern deduplication: similar root causes clustered automatically so the registry stays clean","Database upgraded to production scale as volume grows","Named system owner with monthly responsibilities — this system needs care to stay reliable"],
    gate:{ plain:"90%+ Gong coverage. Outcome recalibration run. System owner named and onboarded.", technical:"Coverage ≥90%. Outcome recalibration with ≥15 closed outcomes per product area. Semantic dedup active. Named owner with documented runbook." },
    who:"PM Ops (system owner) + Product Leadership (quarterly review)", risk:"Without a named owner, this system slowly degrades. A 2-hour monthly check is all it needs — but someone has to own those 2 hours permanently." },
];

// ─── ATOMS ───────────────────────────────────────────────────────────────────
function TechChip({ term }) {
  const [show, setShow] = useState(false);
  const ref = useRef(null);
  const g = GLOSSARY.find(x => x.term.toLowerCase() === term.toLowerCase() || x.term.toLowerCase().includes(term.toLowerCase().split(" ")[0]));
  useEffect(() => {
    const h = e => { if (ref.current && !ref.current.contains(e.target)) setShow(false); };
    document.addEventListener("mousedown", h); return () => document.removeEventListener("mousedown", h);
  }, []);
  return (
    <span ref={ref} style={{ position:"relative", display:"inline-flex", alignItems:"center", gap:4 }}>
      <code style={{ fontFamily:"var(--font-m)", fontSize:10.5, color:"var(--navy)", background:"var(--nb)", padding:"2px 8px", borderRadius:4, letterSpacing:"0.01em", border:"0.5px solid var(--nm)", fontWeight:500 }}>{term}</code>
      <button onMouseEnter={()=>setShow(true)} onMouseLeave={()=>setShow(false)} onClick={()=>setShow(s=>!s)}
        style={{ width:15, height:15, borderRadius:"50%", background:"var(--nb)", border:"0.5px solid var(--nm)", cursor:"pointer", color:"var(--navy)", fontSize:9, fontFamily:"var(--font-m)", fontWeight:700, display:"inline-flex", alignItems:"center", justifyContent:"center", flexShrink:0 }}>i</button>
      {show && g && (
        <div style={{ position:"absolute", bottom:"calc(100% + 8px)", left:0, zIndex:50, background:"var(--ink)", color:"#fff", borderRadius:10, padding:"0.9rem 1rem", width:290, boxShadow:"0 4px 24px rgba(0,0,0,0.2)" }}>
          <div style={{ fontFamily:"var(--font-m)", fontSize:10, color:"rgba(255,255,255,.4)", marginBottom:4, textTransform:"uppercase", letterSpacing:"0.08em" }}>Technical term</div>
          <div style={{ fontFamily:"var(--font-m)", fontSize:12, color:"rgba(255,255,255,.85)", marginBottom:8, fontWeight:500 }}>{g.term}</div>
          <div style={{ fontFamily:"var(--font)", fontSize:13, color:"rgba(255,255,255,.7)", lineHeight:1.65 }}>{g.plain}</div>
        </div>
      )}
    </span>
  );
}

const Card = ({ children, style, left, bg }) => (
  <div style={{ background:bg||"var(--white)", border:"1px solid var(--border)", borderLeft:left?`4px solid ${left}`:undefined, borderRadius:12, padding:"1.25rem 1.4rem", boxShadow:"0 1px 4px rgba(0,0,0,0.04)", ...style }}>{children}</div>
);
const SL = ({ children, color }) => (
  <div style={{ fontFamily:"var(--font-m)", fontSize:10, fontWeight:500, color:color||"var(--ink4)", textTransform:"uppercase", letterSpacing:"0.12em", marginBottom:7 }}>{children}</div>
);
const Tag = ({ children, bg, color, sm }) => (
  <span style={{ background:bg||"var(--s2)", color:color||"var(--ink4)", fontSize:sm?11:12, fontWeight:600, padding:sm?"3px 9px":"4px 12px", borderRadius:20, whiteSpace:"nowrap", display:"inline-block", fontFamily:"var(--font)" }}>{children}</span>
);
const UTag = ({ u }) => {
  const m = { immediate:["var(--rb)","var(--red)","🔴 Act now"], this_quarter:["var(--ab)","var(--amber)","🟡 This quarter"], next_quarter:["var(--nb)","var(--navy)","🔵 Next quarter"] };
  const [bg,c,l]=m[u]||m.next_quarter; return <Tag bg={bg} color={c} sm>{l}</Tag>;
};
const BL = ({ items, color }) => (
  <div style={{ display:"flex", flexDirection:"column", gap:7 }}>
    {items.map((item,i)=>(
      <div key={i} style={{ display:"flex", gap:10, alignItems:"flex-start" }}>
        <span style={{ color:color||"var(--navy)", fontSize:15, flexShrink:0, lineHeight:1.2 }}>→</span>
        <span style={{ fontFamily:"var(--font)", fontSize:14, color:"var(--ink2)", lineHeight:1.65 }}>{item}</span>
      </div>
    ))}
  </div>
);
const Div = () => <div style={{ height:"1px", background:"var(--border)", margin:"1rem 0" }}/>;
const TabBtn = ({ active, onClick, children }) => (
  <button onClick={onClick} style={{ padding:"9px 20px", fontSize:14, fontWeight:active?700:500, fontFamily:"var(--font)", background:active?"var(--navy)":"transparent", borderRadius:active?8:0, border:"none", cursor:"pointer", color:active?"#fff":"var(--ink4)", transition:"all .18s", whiteSpace:"nowrap" }}>{children}</button>
);

// ─── TAB 1: OVERVIEW ─────────────────────────────────────────────────────────
function OverviewTab() {
  const [openPattern, setOpenPattern] = useState(null);
  const [showGloss, setShowGloss] = useState(false);
  const [glossCat, setGlossCat] = useState("All");
  const cats = ["All",...Array.from(new Set(GLOSSARY.map(g=>g.category)))];

  return (
    <div>
      {/* Hero: built for Product Leadership */}
      <Card style={{ marginBottom:"1.5rem", background:"var(--navy)", border:"none", position:"relative", overflow:"hidden" }}>
        <div style={{ position:"absolute", top:0, right:0, width:200, height:200, background:"rgba(255,255,255,.03)", borderRadius:"50%", transform:"translate(60px,-60px)" }}/>
        <div style={{ position:"relative" }}>
          <div style={{ display:"flex", gap:10, alignItems:"center", marginBottom:12 }}>
            <span style={{ fontFamily:"var(--font-m)", fontSize:11, color:"rgba(255,255,255,.4)", letterSpacing:"0.14em", textTransform:"uppercase" }}>Built specifically for</span>
            <div style={{ padding:"3px 12px", background:"rgba(255,255,255,.12)", borderRadius:20, fontFamily:"var(--font)", fontSize:12, fontWeight:700, color:"rgba(255,255,255,.9)" }}>🏗️ Product Leadership at Laurel</div>
          </div>
          <div style={{ fontFamily:"var(--font-d)", fontSize:26, color:"#fff", lineHeight:1.25, marginBottom:14 }}>
            How do you know you're building the right things?
          </div>
          <div style={{ fontFamily:"var(--font)", fontSize:15, color:"rgba(255,255,255,.82)", lineHeight:1.85, marginBottom:14 }}>
            This system gives Product Leadership a continuous, evidence-backed view of what customers are actually experiencing — sorted by how often the same problem appears across different companies, not by who complained loudest. Every roadmap decision can now be traced back to real customer signal.
          </div>
          <div style={{ display:"grid", gridTemplateColumns:"repeat(3,1fr)", gap:12 }}>
            {[["Before","Roadmap priorities set by whoever's loudest in the room, or the most recent customer complaint","var(--rb)","var(--red)"],["After","Every priority backed by how many different customers raised the same root cause, with their exact words","var(--gb)","var(--green)"],["Ongoing","Proof that what shipped actually solved the problem — tracked through real customer conversations 60 days later","var(--nb)","var(--nm)"]].map(([l,d,bg,c])=>(
              <div key={l} style={{ padding:"0.85rem 1rem", background:"rgba(255,255,255,.08)", borderRadius:9, border:`1px solid rgba(255,255,255,.12)` }}>
                <div style={{ fontFamily:"var(--font-m)", fontSize:10, fontWeight:500, color:c, textTransform:"uppercase", letterSpacing:"0.1em", marginBottom:5 }}>{l}</div>
                <div style={{ fontFamily:"var(--font)", fontSize:13, color:"rgba(255,255,255,.8)", lineHeight:1.65 }}>{d}</div>
              </div>
            ))}
          </div>
        </div>
      </Card>

      {/* What Product Leadership gets */}
      <div style={{ marginBottom:"1.5rem" }}>
        <SL>What this gives Product Leadership — four core capabilities</SL>
        <div style={{ display:"grid", gridTemplateColumns:"1fr 1fr", gap:"0.75rem" }}>
          {PM_VALUE_PROPS.map((v,i)=>(
            <Card key={i} bg={v.bg} style={{ border:`1px solid ${v.color}22` }}>
              <div style={{ fontSize:22, marginBottom:8 }}>{v.icon}</div>
              <div style={{ fontFamily:"var(--font)", fontSize:16, fontWeight:700, color:v.color, marginBottom:5, lineHeight:1.3 }}>{v.plain}</div>
              <TechChip term={v.technical}/>
              <Div/>
              <div style={{ display:"grid", gridTemplateColumns:"1fr 1fr", gap:8 }}>
                <div style={{ padding:"8px 10px", background:"var(--rb)", borderRadius:7 }}>
                  <div style={{ fontFamily:"var(--font-m)", fontSize:10, color:"var(--red)", textTransform:"uppercase", letterSpacing:"0.1em", marginBottom:4 }}>Without this</div>
                  <div style={{ fontFamily:"var(--font)", fontSize:12.5, color:"var(--ink2)", lineHeight:1.6 }}>{v.before}</div>
                </div>
                <div style={{ padding:"8px 10px", background:"var(--gb)", borderRadius:7 }}>
                  <div style={{ fontFamily:"var(--font-m)", fontSize:10, color:"var(--green)", textTransform:"uppercase", letterSpacing:"0.1em", marginBottom:4 }}>With this</div>
                  <div style={{ fontFamily:"var(--font)", fontSize:12.5, color:"var(--ink2)", lineHeight:1.6 }}>{v.after}</div>
                </div>
              </div>
            </Card>
          ))}
        </div>
      </div>

      {/* Roadmap Intelligence Brief */}
      <div style={{ marginBottom:"1.5rem" }}>
        <div style={{ display:"flex", justifyContent:"space-between", alignItems:"center", marginBottom:"0.75rem", flexWrap:"wrap", gap:8 }}>
          <div>
            <SL>Product Leadership's roadmap intelligence — ranked by frequency</SL>
            <div style={{ fontFamily:"var(--font)", fontSize:13, color:"var(--ink4)" }}>
              Sorted by how many separate companies raised the same underlying problem — <TechChip term="Pattern Frequency"/> not by how loudly one customer complained
            </div>
          </div>
        </div>
        <div style={{ display:"flex", flexDirection:"column", gap:"0.6rem" }}>
          {ROADMAP_PATTERNS.map((p,i)=>(
            <div key={i}>
              <Card left={p.color} style={{ cursor:"pointer" }} bg={openPattern===i?"var(--s1)":"var(--white)"}>
                <div onClick={()=>setOpenPattern(openPattern===i?null:i)}>
                  <div style={{ display:"flex", gap:12, alignItems:"flex-start" }}>
                    <div style={{ display:"flex", flexDirection:"column", alignItems:"center", gap:3, flexShrink:0, minWidth:32 }}>
                      <div style={{ fontFamily:"var(--font-d)", fontSize:28, color:"var(--ink5)", lineHeight:1 }}>#{p.rank}</div>
                    </div>
                    <div style={{ flex:1 }}>
                      <div style={{ display:"flex", gap:7, marginBottom:7, flexWrap:"wrap", alignItems:"center" }}>
                        <UTag u={p.urgency}/>
                        <Tag bg="var(--s2)" color="var(--ink3)" sm>{p.evidence} companies reporting this</Tag>
                        <TechChip term={p.technical}/>
                        {p.competitors && <Tag bg="var(--rb)" color="var(--red)" sm>⚠ Competitive risk</Tag>}
                      </div>
                      <div style={{ fontFamily:"var(--font)", fontSize:16, fontWeight:700, color:"var(--ink)", lineHeight:1.35, marginBottom:4 }}>{p.plain}</div>
                      <div style={{ display:"flex", gap:6, flexWrap:"wrap" }}>
                        {p.segments.map((s,j)=><Tag key={j} bg="var(--nb)" color="var(--navy)" sm>{s}</Tag>)}
                      </div>
                    </div>
                    <span style={{ fontSize:14, color:"var(--ink5)", flexShrink:0 }}>{openPattern===i?"▲":"▼"}</span>
                  </div>
                </div>
                {openPattern===i && (
                  <div className="au" style={{ marginTop:"1rem" }}>
                    <Div/>
                    <div style={{ display:"grid", gridTemplateColumns:"1fr 1fr 1fr", gap:"0.75rem", marginBottom:"1rem" }}>
                      <div style={{ padding:"0.85rem", background:`${p.color}10`, borderRadius:9, border:`1px solid ${p.color}22` }}>
                        <SL color={p.color}>Why this matters to Product</SL>
                        <div style={{ fontFamily:"var(--font)", fontSize:13.5, color:"var(--ink2)", lineHeight:1.75 }}>{p.why_matters}</div>
                      </div>
                      <div style={{ padding:"0.85rem", background:"var(--ab)", borderRadius:9 }}>
                        <SL color="var(--amber)">What customers are doing instead</SL>
                        <div style={{ fontFamily:"var(--font)", fontSize:13.5, color:"var(--ink2)", lineHeight:1.75 }}>{p.workaround}</div>
                      </div>
                      <div style={{ padding:"0.85rem", background:"var(--gb)", borderRadius:9 }}>
                        <SL color="var(--green)">Recommended first action</SL>
                        <div style={{ fontFamily:"var(--font)", fontSize:13.5, color:"var(--ink2)", lineHeight:1.75 }}>{p.first_action}</div>
                      </div>
                    </div>
                    {p.competitors && (
                      <div style={{ padding:"0.75rem 1rem", background:"var(--rb)", borderRadius:8, marginBottom:"0.75rem", fontFamily:"var(--font)", fontSize:13.5, color:"var(--ink2)", lineHeight:1.7 }}>
                        <strong style={{ color:"var(--red)" }}>⚠ Competitive context: </strong>{p.competitors}
                      </div>
                    )}
                    <div>
                      <SL>What customers actually said — verbatim</SL>
                      <div style={{ display:"flex", flexDirection:"column", gap:6 }}>
                        {p.quotes.map((q,j)=>(
                          <div key={j} style={{ padding:"10px 12px", background:"var(--s1)", borderRadius:8, borderLeft:`2px solid ${p.color}` }}>
                            <div style={{ fontFamily:"var(--font-d)", fontSize:14, fontStyle:"italic", color:"var(--ink)", lineHeight:1.65, marginBottom:4 }}>"{q.q}"</div>
                            <div style={{ fontFamily:"var(--font-m)", fontSize:11, color:"var(--ink5)", textTransform:"uppercase", letterSpacing:"0.05em" }}>{q.co}</div>
                          </div>
                        ))}
                      </div>
                    </div>
                  </div>
                )}
              </Card>
            </div>
          ))}
        </div>
      </div>

      {/* Glossary */}
      <div>
        <div style={{ display:"flex", justifyContent:"space-between", alignItems:"center", marginBottom:"0.75rem" }}>
          <SL>Glossary — technical terms explained</SL>
          <button onClick={()=>setShowGloss(s=>!s)} style={{ fontFamily:"var(--font)", fontSize:13, fontWeight:600, color:"var(--navy)", background:"var(--nb)", border:"1px solid var(--nm)", borderRadius:7, padding:"5px 14px", cursor:"pointer" }}>
            {showGloss?"Hide ↑":"Show glossary ↓"}
          </button>
        </div>
        {showGloss && (
          <div className="au">
            <div style={{ display:"flex", gap:6, marginBottom:"1rem", flexWrap:"wrap" }}>
              {cats.map(c=><button key={c} onClick={()=>setGlossCat(c)} style={{ padding:"5px 13px", borderRadius:6, border:`1px solid ${glossCat===c?"var(--navy)":"var(--border)"}`, background:glossCat===c?"var(--navy)":"var(--white)", color:glossCat===c?"#fff":"var(--ink4)", cursor:"pointer", fontFamily:"var(--font)", fontSize:13, fontWeight:600 }}>{c}</button>)}
            </div>
            <div style={{ border:"1px solid var(--border)", borderRadius:12, overflow:"hidden" }}>
              {(glossCat==="All"?GLOSSARY:GLOSSARY.filter(g=>g.category===glossCat)).map((g,i,arr)=>(
                <div key={g.term} style={{ display:"grid", gridTemplateColumns:"1fr 1.8fr auto", gap:0, borderBottom:i<arr.length-1?"1px solid var(--border)":"none" }}>
                  <div style={{ padding:"11px 14px", background:"var(--nlight)", borderRight:"1px solid var(--border)" }}>
                    <code style={{ fontFamily:"var(--font-m)", fontSize:12, color:"var(--navy)", fontWeight:500, lineHeight:1.4, display:"block" }}>{g.term}</code>
                  </div>
                  <div style={{ padding:"11px 14px" }}>
                    <div style={{ fontFamily:"var(--font)", fontSize:13.5, color:"var(--ink2)", lineHeight:1.65 }}>{g.plain}</div>
                  </div>
                  <div style={{ padding:"11px 14px", display:"flex", alignItems:"center", background:"var(--s1)", borderLeft:"1px solid var(--border)" }}>
                    <Tag bg="var(--s2)" color="var(--ink4)" sm>{g.category}</Tag>
                  </div>
                </div>
              ))}
            </div>
          </div>
        )}
      </div>
    </div>
  );
}

// ─── TAB 2: PIPELINE ─────────────────────────────────────────────────────────
function PipelineTab() {
  const [sel, setSel] = useState(0);
  const [running, setRunning] = useState(false);
  const [processed, setProcessed] = useState([]);
  const [currentIdx, setCurrentIdx] = useState(-1);
  const timer = useRef(null);
  const step = PIPELINE_STEPS[sel];

  const DEMO = [
    { co:"Meridian Law", src:"Sales call", tech:"gong_call", result:"Pattern updated: Approval Workflow Gap now at 4 companies", sev:"urgent",
      meaning:"Meridian Law is the 4th separate company to raise the same underlying problem — managers cannot approve hours before invoices go out. This is no longer a one-off complaint from a single customer. Four different companies experiencing the same structural gap is a clear signal that something is missing from the product.",
      action:"This pattern is ranked #1 in the roadmap briefing. Product Leadership should prioritise multi-level approval routing. Praxis Group has a September deadline and is actively comparing Laurel to Harvest on this exact feature — every week without it is competitive exposure.",
      actor:"Product team", urgency:"Act now" },

    { co:"Holloway & Reed", src:"Support ticket", tech:"support_ticket", result:"Pattern updated: Jira Integration Failure — velocity now 2.1×", sev:"urgent",
      meaning:"The Jira integration problem has appeared more than twice as fast in the last two weeks compared to the two weeks before. It is not staying the same — it is getting worse. Holloway & Reed has already mentioned Clockify by name as an alternative they are considering. This is an active retention risk, not a future roadmap item.",
      action:"Engineering needs to fix the integration architecture so it does not break every time Atlassian releases an update. Separately, the product needs to alert customers the moment a sync fails — right now they only find out when invoice hours are already missing, which is too late.",
      actor:"Engineering (fix) + Product (alerting feature)", urgency:"Act now" },

    { co:"Acme Corp", src:"QBR call", tech:"qbr_call", result:"Expansion signal: $42k unlocks if custom thresholds ship", sev:"good",
      meaning:"Acme Corp has confirmed directly that they would expand to three additional internal teams the moment Laurel supports custom budget alert thresholds — meaning alerts set at different percentages for different types of projects, not just the current fixed 75%. The $42,000 in expansion revenue is identified and waiting. It is not speculative.",
      action:"Prioritise configurable alert thresholds as an expansion unlock, not just a product improvement. Terrace Analytics is in the same situation, bringing the total identified expansion to approximately $60,000. This is a Finance conversation as much as a Product one.",
      actor:"Product team + Finance", urgency:"This quarter" },

    { co:"Kestrel Advisory", src:"Discovery call", tech:"gong_call", result:"Solo signal escalated: FINRA audit trail — compliance requirement", sev:"solo",
      meaning:"Only one company has raised this, but Kestrel Advisory is a regulated financial firm and FINRA compliance is a legal requirement — not a preference. They need a complete, uneditable record of every change made to a logged hour. Laurel does not currently have this feature. They are actively evaluating Replicon as an alternative.",
      action:"Product Leadership needs to make a strategic decision: does Laurel want to serve regulated financial services firms? If yes, an immutable audit trail is the minimum feature required to be in the conversation. If no, this is out of scope and Kestrel should be redirected. Either answer is valid — but the decision cannot be postponed while an enterprise deal sits open.",
      actor:"Product Leadership (strategic decision)", urgency:"Decision required now" },

    { co:"Unknown", src:"Support ticket", tech:"support_ticket", result:"Quality check failed — 12 words, no product mention → manual review", sev:"manual",
      meaning:"This support ticket was 12 words long and contained no reference to any Laurel product or feature. The AI cannot extract meaningful or reliable information from it. If it were processed automatically, it could introduce inaccurate data into the pattern database — which would undermine the signals Product Leadership relies on.",
      action:"PM Ops should open this ticket, read it, and take one of two paths: write a one-sentence summary so the system can categorize it correctly, or archive it if it contains no useful signal. This typically takes less than 60 seconds and protects the accuracy of everything else in the pipeline.",
      actor:"PM Ops (manual review queue)", urgency:"Low — handle within 48 hours" },

    { co:"Terrace Analytics", src:"QBR call", tech:"qbr_call", result:"Outcome confirmed: Budget alerts fix reduced complaints to zero ✓", sev:"resolved",
      meaning:"The budget alerts feature that Product shipped last quarter worked. Terrace Analytics confirmed in their quarterly review that budget overruns have dropped to zero since the feature went live. The pattern that drove that product decision is now marked as resolved — not because a ticket was closed, but because real customers stopped mentioning the problem in new conversations.",
      action:"No immediate action needed — this is a confirmed win. The pipeline will use this outcome to improve future prioritisation: when similar budget-visibility problems appear from other customers, they will score higher because there is now evidence that solving this type of problem delivers measurable impact.",
      actor:"Product team — record the outcome", urgency:"No action required" },
  ];

  const [expanded, setExpanded] = useState(new Set());
  const toggleExpand = (i) => setExpanded(prev => { const n = new Set(prev); n.has(i) ? n.delete(i) : n.add(i); return n; });

  const startDemo = useCallback(()=>{ setRunning(true); setProcessed([]); setCurrentIdx(0); setExpanded(new Set()); }, []);
  useEffect(() => {
    if (!running||currentIdx<0) return;
    if (currentIdx>=DEMO.length) { setRunning(false); setCurrentIdx(-1); return; }
    timer.current = setTimeout(() => { setProcessed(p=>[...p,DEMO[currentIdx]]); setCurrentIdx(i=>i+1); }, 1900);
    return () => clearTimeout(timer.current);
  }, [running, currentIdx]);

  const sev_map = { urgent:["var(--rb)","var(--red)","🔴"], good:["var(--goldb)","var(--gold)","💰"], solo:["var(--nb)","var(--navy)","🏴"], manual:["var(--s2)","var(--ink4)","👤"], resolved:["var(--gb)","var(--green)","✅"] };

  return (
    <div>
      {/* Step selector */}
      <Card style={{ marginBottom:"1.5rem" }}>
        <div style={{ fontFamily:"var(--font-d)", fontSize:20, color:"var(--ink)", marginBottom:4 }}>How the pipeline works — step by step</div>
        <div style={{ fontFamily:"var(--font)", fontSize:14, color:"var(--ink4)", marginBottom:"1rem" }}>Each step is explained in plain English and shows what Product Leadership gets from it. Click any step to explore.</div>
        <div style={{ display:"flex", gap:6, flexWrap:"wrap" }}>
          {PIPELINE_STEPS.map((s,i)=>(
            <button key={i} onClick={()=>setSel(i)} style={{ padding:"8px 14px", borderRadius:8, border:`1px solid ${sel===i?s.color:"var(--border)"}`, background:sel===i?s.color:"var(--s1)", color:sel===i?"#fff":"var(--ink3)", cursor:"pointer", fontFamily:"var(--font)", fontSize:13, fontWeight:600, transition:"all .15s" }}>
              {s.icon} {s.num}
            </button>
          ))}
        </div>

        {/* ── Step icon key */}
        <div style={{ marginTop:"1rem", paddingTop:"1rem", borderTop:"1px solid var(--border)" }}>
          <div style={{ fontFamily:"var(--font-m)", fontSize:10, fontWeight:500, color:"var(--ink5)", textTransform:"uppercase", letterSpacing:"0.12em", marginBottom:8 }}>What each step icon means</div>
          <div style={{ display:"flex", gap:0, flexWrap:"wrap", border:"1px solid var(--border)", borderRadius:9, overflow:"hidden" }}>
            {PIPELINE_STEPS.map((s,i)=>(
              <div key={s.num} style={{ display:"flex", gap:10, alignItems:"center", padding:"8px 14px", borderRight:i<PIPELINE_STEPS.length-1?"1px solid var(--border)":"none", flex:"1 1 0", minWidth:100 }}>
                <span style={{ fontSize:18, flexShrink:0 }}>{s.icon}</span>
                <div>
                  <div style={{ fontFamily:"var(--font-m)", fontSize:10, color:"var(--navy)", fontWeight:500, marginBottom:2 }}>Step {s.num}</div>
                  <div style={{ fontFamily:"var(--font)", fontSize:12, color:"var(--ink3)", lineHeight:1.4 }}>{s.plain}</div>
                </div>
              </div>
            ))}
          </div>
        </div>
      </Card>

      {step && (
        <div key={sel} className="au" style={{ marginBottom:"1.5rem" }}>
          <Card left={step.color}>
            <div style={{ display:"flex", gap:12, alignItems:"flex-start", marginBottom:"1.25rem" }}>
              <span style={{ fontSize:36, flexShrink:0 }}>{step.icon}</span>
              <div style={{ flex:1 }}>
                <div style={{ fontFamily:"var(--font-m)", fontSize:11, color:step.color, textTransform:"uppercase", letterSpacing:"0.12em", marginBottom:4 }}>Step {step.num}</div>
                <div style={{ fontFamily:"var(--font-d)", fontSize:22, color:"var(--ink)", lineHeight:1.2, marginBottom:8 }}>{step.plain}</div>
                <TechChip term={step.technical}/>
              </div>
            </div>

            <div style={{ display:"grid", gridTemplateColumns:"1fr 1fr", gap:"1rem" }}>
              <div>
                {/* What Product Leadership gets */}
                <div style={{ padding:"1rem", background:"var(--nlight)", border:"1px solid var(--nm)", borderRadius:9, marginBottom:"0.75rem" }}>
                  <div style={{ display:"flex", gap:6, alignItems:"center", marginBottom:6 }}>
                    <span style={{ fontSize:14 }}>🏗️</span>
                    <SL color="var(--navy)">What Product Leadership gets from this step</SL>
                  </div>
                  <div style={{ fontFamily:"var(--font)", fontSize:14, color:"var(--ink2)", lineHeight:1.8 }}>{step.pm_value}</div>
                </div>
                {/* Plain meaning */}
                <div style={{ padding:"1rem", background:`${step.color}0D`, border:`1px solid ${step.color}22`, borderRadius:9 }}>
                  <SL color={step.color}>In plain terms</SL>
                  <div style={{ fontFamily:"var(--font)", fontSize:14, color:"var(--ink2)", lineHeight:1.8 }}>
                    {step.what_comes_in && <><BL items={step.what_comes_in} color={step.color}/></>}
                    {step.checks && <BL items={step.checks} color={step.color}/>}
                    {step.extracts && <BL items={step.extracts} color={step.color}/>}
                    {step.deliverables && step.deliverables.map((d,i)=>(
                      <div key={i} style={{ padding:"8px 10px", background:"var(--white)", borderRadius:7, marginBottom:6, borderLeft:`3px solid ${step.color}` }}>
                        <div style={{ fontFamily:"var(--font)", fontSize:13, fontWeight:700, color:"var(--ink)", marginBottom:2 }}>{d.label}</div>
                        <div style={{ fontFamily:"var(--font)", fontSize:13, color:"var(--ink2)", marginBottom:4 }}>{d.desc}</div>
                        <TechChip term={d.tech}/>
                      </div>
                    ))}
                  </div>
                </div>
              </div>
              <div>
                {/* Technical detail */}
                <div style={{ padding:"1rem", background:"var(--s1)", border:"1px solid var(--border)", borderRadius:9, marginBottom:"0.75rem" }}>
                  <div style={{ display:"flex", gap:8, alignItems:"center", marginBottom:8 }}>
                    <SL color="var(--ink4)">Technical process</SL>
                    <TechChip term={step.technical.split("→")[0].trim()}/>
                  </div>
                  <div style={{ fontFamily:"var(--font)", fontSize:13.5, color:"var(--ink3)", lineHeight:1.75 }}>{step.tech_plain}</div>
                </div>
                {step.translation && (
                  <div style={{ marginBottom:"0.75rem" }}>
                    <div style={{ padding:"10px 12px", background:"var(--rb)", borderRadius:"9px 9px 0 0", borderBottom:"none" }}>
                      <SL color="var(--red)">Customer's words</SL>
                      <div style={{ fontFamily:"var(--font-d)", fontSize:14, fontStyle:"italic", color:"var(--ink)" }}>{step.translation.surface}</div>
                    </div>
                    <div style={{ padding:"10px 12px", background:"var(--gb)", borderRadius:"0 0 9px 9px" }}>
                      <SL color="var(--green)">What the system tells Product Leadership</SL>
                      <div style={{ fontFamily:"var(--font)", fontSize:14, color:"var(--ink2)", marginBottom:5 }}>{step.translation.root}</div>
                      <div style={{ fontFamily:"var(--font)", fontSize:12.5, color:"var(--green)", fontStyle:"italic" }}>{step.translation.why}</div>
                    </div>
                  </div>
                )}
                {step.solo_note && (
                  <div style={{ padding:"0.85rem 1rem", background:"var(--rb)", border:"1px solid var(--red)22", borderRadius:9 }}>
                    <div style={{ display:"flex", gap:8, marginBottom:6, flexWrap:"wrap", alignItems:"center" }}>
                      <SL color="var(--red)">One voice still matters to Product Leadership</SL>
                      <TechChip term={step.solo_note.technical}/>
                    </div>
                    <div style={{ fontFamily:"var(--font)", fontSize:14, color:"var(--ink2)", lineHeight:1.75 }}>{step.solo_note.plain}</div>
                  </div>
                )}
              </div>
            </div>
          </Card>
        </div>
      )}

      {/* Demo */}
      <Card>
        <div style={{ display:"flex", justifyContent:"space-between", alignItems:"center", marginBottom:"1rem", flexWrap:"wrap", gap:10 }}>
          <div>
            <div style={{ fontFamily:"var(--font-d)", fontSize:18, color:"var(--ink)", marginBottom:3 }}>Watch the pipeline deliver intelligence to Product Leadership</div>
            <div style={{ fontFamily:"var(--font)", fontSize:13, color:"var(--ink4)" }}>Each conversation shows the plain English outcome and the technical source type</div>
          </div>
          <button onClick={startDemo} disabled={running} style={{ padding:"9px 22px", background:running?"var(--s2)":"var(--navy)", color:running?"var(--ink4)":"#fff", border:"none", borderRadius:8, cursor:running?"not-allowed":"pointer", fontFamily:"var(--font)", fontWeight:700, fontSize:14 }}>
            {running?"Processing…":"▶ Run demo"}
          </button>
        </div>
        {processed.length===0&&!running && <div style={{ textAlign:"center", padding:"1.5rem", color:"var(--ink5)", fontFamily:"var(--font)", fontSize:14 }}>Press Run demo to see conversations turning into Product Leadership intelligence in real time</div>}

        {/* ── Result icon key */}
        <div style={{ marginBottom:"1rem", padding:"0.9rem 1rem", background:"var(--s1)", border:"1px solid var(--border)", borderRadius:9 }}>
          <div style={{ fontFamily:"var(--font-m)", fontSize:10, fontWeight:500, color:"var(--ink5)", textTransform:"uppercase", letterSpacing:"0.12em", marginBottom:10 }}>Icon key — what each result means</div>
          <div style={{ display:"grid", gridTemplateColumns:"repeat(auto-fit, minmax(220px, 1fr))", gap:"6px 16px" }}>
            {[
              { icon:"🔴", bg:"var(--rb)", c:"var(--red)", label:"Urgent pattern", desc:"The same problem is appearing faster across multiple companies — needs immediate Product Leadership attention" },
              { icon:"💰", bg:"var(--goldb)", c:"var(--gold)", label:"Expansion opportunity", desc:"A customer revealed revenue waiting to be unlocked if a specific feature is built" },
              { icon:"🏴", bg:"var(--nb)", c:"var(--navy)", label:"Solo signal", desc:"One company raised something critical — surfaced to Product Leadership regardless of whether others mentioned it" },
              { icon:"👤", bg:"var(--s2)", c:"var(--ink4)", label:"Manual review needed", desc:"Conversation was too short or unclear for the AI to analyze reliably — a human needs to review it instead" },
              { icon:"✅", bg:"var(--gb)", c:"var(--green)", label:"Outcome confirmed", desc:"A previous product fix actually worked — customers stopped raising this problem in new conversations" },
              { icon:"●", bg:"var(--nb)", c:"var(--navy)", label:"Currently processing", desc:"The pipeline is actively analyzing this conversation right now — result will appear within seconds", pulse:true },
            ].map((k,i)=>(
              <div key={i} style={{ display:"flex", gap:10, alignItems:"flex-start", padding:"6px 0", borderBottom:i<5?"0.5px solid var(--border)":"none" }}>
                <div style={{ width:28, height:28, borderRadius:7, background:k.bg, display:"flex", alignItems:"center", justifyContent:"center", flexShrink:0, border:`1px solid ${k.c}22` }}>
                  {k.pulse
                    ? <span className="pulse" style={{ width:9, height:9, borderRadius:"50%", background:k.c, display:"block" }}/>
                    : <span style={{ fontSize:14 }}>{k.icon}</span>}
                </div>
                <div style={{ flex:1 }}>
                  <div style={{ fontFamily:"var(--font)", fontSize:12.5, fontWeight:700, color:k.c, marginBottom:2 }}>{k.label}</div>
                  <div style={{ fontFamily:"var(--font)", fontSize:12, color:"var(--ink4)", lineHeight:1.5 }}>{k.desc}</div>
                </div>
              </div>
            ))}
          </div>
        </div>
        <div style={{ display:"flex", flexDirection:"column", gap:8 }}>
          {processed.map((item,i)=>{
            const [bg,c,icon]=sev_map[item.sev]||sev_map.manual;
            const isOpen = expanded.has(i);
            return (
              <div key={i} className="si" style={{ background:"var(--white)", border:`1px solid var(--border)`, borderLeft:`4px solid ${c}`, borderRadius:10, overflow:"hidden" }}>
                {/* Summary row — always visible */}
                <button onClick={()=>toggleExpand(i)} style={{ width:"100%", padding:"12px 14px", display:"grid", gridTemplateColumns:"auto 1fr auto auto", gap:12, alignItems:"center", background:"transparent", border:"none", cursor:"pointer", textAlign:"left" }}>
                  <span style={{ fontSize:20 }}>{icon}</span>
                  <div>
                    <div style={{ fontFamily:"var(--font)", fontWeight:700, color:"var(--ink)", fontSize:14, marginBottom:3 }}>
                      {item.co}
                      <span style={{ fontFamily:"var(--font)", fontSize:12, fontWeight:400, color:"var(--ink4)", marginLeft:10 }}>{item.src}</span>
                    </div>
                    <div style={{ fontFamily:"var(--font)", fontSize:13, color:"var(--ink2)" }}>{item.result}</div>
                  </div>
                  <TechChip term={item.tech}/>
                  <div style={{ display:"flex", alignItems:"center", gap:6 }}>
                    <span style={{ fontFamily:"var(--font)", fontSize:11, color:"var(--ink5)" }}>{isOpen?"Hide detail":"See what to do"}</span>
                    <span style={{ fontSize:12, color:"var(--ink5)" }}>{isOpen?"▲":"▼"}</span>
                  </div>
                </button>

                {/* Expanded detail */}
                {isOpen && (
                  <div className="au" style={{ padding:"0 14px 14px" }}>
                    <div style={{ height:"1px", background:"var(--border)", marginBottom:12 }}/>
                    <div style={{ display:"grid", gridTemplateColumns:"1fr 1fr", gap:"0.75rem", marginBottom:"0.75rem" }}>

                      {/* What this means */}
                      <div style={{ padding:"0.85rem 1rem", background:"var(--s1)", borderRadius:9 }}>
                        <div style={{ fontFamily:"var(--font-m)", fontSize:10, fontWeight:500, color:"var(--ink4)", textTransform:"uppercase", letterSpacing:"0.1em", marginBottom:7 }}>What this means</div>
                        <div style={{ fontFamily:"var(--font)", fontSize:13.5, color:"var(--ink2)", lineHeight:1.8 }}>{item.meaning}</div>
                      </div>

                      {/* What to act on */}
                      <div style={{ padding:"0.85rem 1rem", background:`${c}0F`, border:`1px solid ${c}22`, borderRadius:9 }}>
                        <div style={{ fontFamily:"var(--font-m)", fontSize:10, fontWeight:500, color:c, textTransform:"uppercase", letterSpacing:"0.1em", marginBottom:7 }}>What to act on</div>
                        <div style={{ fontFamily:"var(--font)", fontSize:13.5, color:"var(--ink2)", lineHeight:1.8 }}>{item.action}</div>
                      </div>
                    </div>

                    {/* Who acts + urgency */}
                    <div style={{ display:"flex", gap:8, alignItems:"center" }}>
                      <div style={{ padding:"5px 12px", background:"var(--nb)", borderRadius:20, display:"flex", gap:7, alignItems:"center" }}>
                        <span style={{ fontFamily:"var(--font-m)", fontSize:10, color:"var(--navy)", textTransform:"uppercase", letterSpacing:"0.08em" }}>Who acts</span>
                        <span style={{ fontFamily:"var(--font)", fontSize:12.5, fontWeight:600, color:"var(--navy)" }}>{item.actor}</span>
                      </div>
                      <div style={{ padding:"5px 12px", background:`${c}15`, borderRadius:20, display:"flex", gap:7, alignItems:"center" }}>
                        <span style={{ fontFamily:"var(--font-m)", fontSize:10, color:c, textTransform:"uppercase", letterSpacing:"0.08em" }}>Urgency</span>
                        <span style={{ fontFamily:"var(--font)", fontSize:12.5, fontWeight:600, color:c }}>{item.urgency}</span>
                      </div>
                    </div>
                  </div>
                )}
              </div>
            );
          })}
          {running&&currentIdx>=0&&currentIdx<DEMO.length && (
            <div style={{ display:"flex", gap:10, padding:"10px 14px", background:"var(--nb)", borderRadius:9, border:"1px dashed var(--navy)", alignItems:"center" }}>
              <span className="pulse" style={{ width:9,height:9,borderRadius:"50%",background:"var(--navy)",display:"block" }}/>
              <span style={{ fontFamily:"var(--font)",fontSize:13,color:"var(--navy)",fontWeight:600 }}>Processing: {DEMO[currentIdx]?.co} ({DEMO[currentIdx]?.src}) — finding what matters for Product</span>
            </div>
          )}
        </div>
      </Card>
    </div>
  );
}

// ─── TAB 3: PLAN ─────────────────────────────────────────────────────────────
function PlanTab() {
  const [active, setActive] = useState("01");
  const [section, setSection] = useState("what");
  const phase = IMPL_PHASES.find(p=>p.num===active);

  return (
    <div>
      <Card style={{ marginBottom:"1.5rem", background:"var(--navy)", border:"none" }}>
        <div style={{ fontFamily:"var(--font-d)", fontSize:20, color:"#fff", marginBottom:8 }}>The rollout plan — built around when Product Leadership benefits</div>
        <div style={{ fontFamily:"var(--font)", fontSize:14, color:"rgba(255,255,255,.8)", lineHeight:1.75, maxWidth:640, marginBottom:"1rem" }}>
          Six phases. Each has one job and one test it must pass before the next begins. Product Leadership requested this pipeline — so every phase is evaluated by when and how it changes what Product Leadership can do.
        </div>
        <div style={{ display:"grid", gridTemplateColumns:"repeat(3,1fr)", gap:10 }}>
          {[["Phase 01–02","Product Leadership validates accuracy — before any automation"],["Phase 03–04","Product Leadership gets their dashboard and uses it in a real planning meeting"],["Phase 05–06","Product Leadership sees evidence that what they shipped actually worked"]].map(([p,d])=>(
            <div key={p} style={{ padding:"0.85rem 1rem", background:"rgba(255,255,255,.08)", borderRadius:9 }}>
              <div style={{ fontFamily:"var(--font-m)", fontSize:10, color:"rgba(255,255,255,.4)", marginBottom:4, textTransform:"uppercase", letterSpacing:"0.08em" }}>{p}</div>
              <div style={{ fontFamily:"var(--font)", fontSize:13, color:"rgba(255,255,255,.8)", lineHeight:1.6 }}>{d}</div>
            </div>
          ))}
        </div>
      </Card>

      <div style={{ display:"grid", gridTemplateColumns:"200px 1fr", gap:"1.25rem" }}>
        <div>
          {IMPL_PHASES.map((p,i)=>(
            <div key={p.num} style={{ display:"flex", gap:0 }}>
              <div style={{ display:"flex", flexDirection:"column", alignItems:"center", width:26, flexShrink:0 }}>
                <button onClick={()=>{setActive(p.num);setSection("what");}} style={{ width:24, height:24, borderRadius:"50%", border:`2px solid ${active===p.num?p.color:"var(--border)"}`, background:active===p.num?p.color:"var(--white)", cursor:"pointer", display:"flex", alignItems:"center", justifyContent:"center", transition:"all .15s" }}>
                  <span style={{ fontFamily:"var(--font-m)", fontSize:9, fontWeight:700, color:active===p.num?"#fff":"var(--ink5)" }}>{p.num}</span>
                </button>
                {i<IMPL_PHASES.length-1 && <div style={{ width:2, flex:1, minHeight:14, background:"var(--border)", margin:"3px 0" }}/>}
              </div>
              <button onClick={()=>{setActive(p.num);setSection("what");}} style={{ flex:1, padding:"2px 10px 16px", textAlign:"left", background:"transparent", border:"none", cursor:"pointer" }}>
                <div style={{ fontFamily:"var(--font-m)", fontSize:10, color:active===p.num?p.color:"var(--ink5)", fontWeight:500 }}>{p.dur}</div>
                <div style={{ fontFamily:"var(--font)", fontSize:12.5, fontWeight:active===p.num?700:500, color:active===p.num?"var(--ink)":"var(--ink3)", lineHeight:1.3 }}>{p.label}</div>
              </button>
            </div>
          ))}
        </div>

        {phase && (
          <div key={active} className="au">
            <div style={{ padding:"1.25rem 1.4rem", background:phase.bg, border:`1px solid ${phase.color}33`, borderLeft:`4px solid ${phase.color}`, borderRadius:12, marginBottom:"1rem" }}>
              <div style={{ display:"flex", gap:8, marginBottom:8, flexWrap:"wrap", alignItems:"center" }}>
                <Tag bg={`${phase.color}22`} color={phase.color} sm>Phase {phase.num}</Tag>
                <Tag bg={`${phase.color}22`} color={phase.color} sm>{phase.dur}</Tag>
                <TechChip term={phase.technical}/>
              </div>
              <div style={{ fontFamily:"var(--font-d)", fontSize:20, color:"var(--ink)", marginBottom:5, lineHeight:1.2 }}>{phase.label}</div>
              <div style={{ fontFamily:"var(--font)", fontSize:14, color:"var(--ink2)", lineHeight:1.75 }}>{phase.goal}</div>
            </div>

            {/* Product Leadership callout */}
            <div style={{ padding:"0.85rem 1.1rem", background:"var(--nlight)", border:"1px solid var(--nm)", borderRadius:9, marginBottom:"1rem", display:"flex", gap:10, alignItems:"flex-start" }}>
              <span style={{ fontSize:18, flexShrink:0 }}>🏗️</span>
              <div>
                <div style={{ fontFamily:"var(--font-m)", fontSize:10, color:"var(--navy)", textTransform:"uppercase", letterSpacing:"0.1em", marginBottom:4 }}>What Product Leadership gets from this phase</div>
                <div style={{ fontFamily:"var(--font)", fontSize:14, color:"var(--ink2)", lineHeight:1.7 }}>{phase.pm_gets}</div>
              </div>
            </div>

            <div style={{ display:"flex", gap:6, marginBottom:"1rem" }}>
              {[["what","What happens"],["tech","Technical goal"],["gate","Must pass before next phase"]].map(([id,lbl])=>(
                <button key={id} onClick={()=>setSection(id)} style={{ padding:"6px 14px", borderRadius:7, border:`1px solid ${section===id?"var(--navy)":"var(--border)"}`, background:section===id?"var(--navy)":"var(--s1)", color:section===id?"#fff":"var(--ink3)", cursor:"pointer", fontFamily:"var(--font)", fontWeight:600, fontSize:12.5, transition:"all .15s" }}>{lbl}</button>
              ))}
            </div>

            {section==="what" && (
              <div style={{ display:"grid", gridTemplateColumns:"1fr 1fr", gap:"0.75rem" }}>
                <Card>
                  <SL>What happens</SL>
                  <BL items={phase.what_happens} color={phase.color}/>
                </Card>
                <div style={{ display:"flex", flexDirection:"column", gap:"0.75rem" }}>
                  <Card style={{ background:phase.bg, border:`1px solid ${phase.color}33` }}>
                    <SL>Who is involved</SL>
                    <div style={{ fontFamily:"var(--font)", fontSize:14, color:"var(--ink2)", lineHeight:1.65 }}>{phase.who}</div>
                  </Card>
                  <Card style={{ background:"var(--rb)", border:"1px solid var(--red)22" }}>
                    <SL color="var(--red)">Risk if this phase is skipped</SL>
                    <div style={{ fontFamily:"var(--font)", fontSize:14, color:"var(--ink2)", lineHeight:1.65 }}>{phase.risk}</div>
                  </Card>
                </div>
              </div>
            )}

            {section==="tech" && (
              <Card style={{ background:"var(--s1)" }}>
                <div style={{ display:"flex", gap:8, alignItems:"center", marginBottom:"1rem", flexWrap:"wrap" }}>
                  <SL>Technical goal</SL><TechChip term={phase.technical}/>
                </div>
                <div style={{ fontFamily:"var(--font)", fontSize:14, color:"var(--ink2)", lineHeight:1.85 }}>{phase.technical_detail||phase.goal}</div>
              </Card>
            )}

            {section==="gate" && (
              <div style={{ display:"grid", gridTemplateColumns:"1fr 1fr", gap:"0.75rem" }}>
                <Card style={{ background:phase.bg, border:`1px solid ${phase.color}33`, borderLeft:`4px solid ${phase.color}` }}>
                  <SL color={phase.color}>In plain English — the test that must pass</SL>
                  <div style={{ fontFamily:"var(--font)", fontSize:14, color:"var(--ink2)", lineHeight:1.75 }}>{phase.gate.plain}</div>
                </Card>
                <Card style={{ background:"var(--s1)" }}>
                  <div style={{ display:"flex", gap:6, marginBottom:8, flexWrap:"wrap" }}>
                    <SL>Technical criteria</SL><TechChip term="Quality Gate"/>
                  </div>
                  <div style={{ fontFamily:"var(--font-m)", fontSize:12, color:"var(--ink3)", lineHeight:1.85 }}>{phase.gate.technical}</div>
                </Card>
              </div>
            )}

            <div style={{ display:"flex", justifyContent:"space-between", marginTop:"1rem" }}>
              <button onClick={()=>{ const i=IMPL_PHASES.findIndex(p=>p.num===active); if(i>0){setActive(IMPL_PHASES[i-1].num);setSection("what");} }} disabled={IMPL_PHASES[0].num===active} style={{ padding:"8px 18px", background:"var(--s2)", border:"1px solid var(--border)", borderRadius:8, cursor:IMPL_PHASES[0].num===active?"not-allowed":"pointer", color:"var(--ink3)", fontFamily:"var(--font)", fontWeight:600, fontSize:13, opacity:IMPL_PHASES[0].num===active?.4:1 }}>← Previous</button>
              <button onClick={()=>{ const i=IMPL_PHASES.findIndex(p=>p.num===active); if(i<IMPL_PHASES.length-1){setActive(IMPL_PHASES[i+1].num);setSection("what");} }} disabled={IMPL_PHASES[IMPL_PHASES.length-1].num===active} style={{ padding:"8px 18px", background:"var(--navy)", border:"none", borderRadius:8, cursor:IMPL_PHASES[IMPL_PHASES.length-1].num===active?"not-allowed":"pointer", color:"#fff", fontFamily:"var(--font)", fontWeight:600, fontSize:13, opacity:IMPL_PHASES[IMPL_PHASES.length-1].num===active?.4:1 }}>Next →</button>
            </div>
          </div>
        )}
      </div>
    </div>
  );
}

// ─── ROOT ─────────────────────────────────────────────────────────────────────
export default function App() {
  const [tab, setTab] = useState("overview");
  const tabs = [{ id:"overview",label:"🏗️  Product Intelligence" },{ id:"pipeline",label:"⚡  How It Works" },{ id:"plan",label:"📋  Rollout Plan" }];

  return (
    <>
      <Fonts/>
      <div style={{ fontFamily:"var(--font)", background:"var(--bg)", minHeight:"100vh" }}>
        <div style={{ background:"var(--white)", borderBottom:"1px solid var(--border)", padding:"1.1rem 1.5rem 0", position:"sticky", top:0, zIndex:20, boxShadow:"0 2px 8px rgba(0,0,0,0.04)" }}>
          <div style={{ maxWidth:980, margin:"0 auto" }}>
            <div style={{ display:"flex", justifyContent:"space-between", alignItems:"flex-end", marginBottom:"0.85rem", flexWrap:"wrap", gap:12 }}>
              <div>
                <div style={{ fontFamily:"var(--font-m)", fontSize:10, fontWeight:500, color:"var(--ink5)", letterSpacing:"0.14em", textTransform:"uppercase", marginBottom:4 }}>Laurel · AI Operations · Option 4 — Requested by Product Leadership</div>
                <div style={{ fontFamily:"var(--font-d)", fontSize:22, color:"var(--navy)", lineHeight:1 }}>Voice of Customer Intelligence Pipeline</div>
                <div style={{ fontFamily:"var(--font)", fontSize:13, color:"var(--ink4)", marginTop:4 }}>Turning every customer conversation into actionable Product Intelligence — continuously, automatically, and in plain English</div>
              </div>
              <div style={{ display:"flex", gap:8, alignItems:"center" }}>
                <span className="pulse" style={{ width:9,height:9,borderRadius:"50%",background:"var(--green)",display:"block" }}/>
                <span style={{ fontFamily:"var(--font)", fontSize:13, fontWeight:600, color:"var(--green)" }}>Live</span>
                <TechChip term="Continuous async pipeline"/>
              </div>
            </div>
            <div style={{ display:"flex", gap:4, padding:"4px", background:"var(--s2)", borderRadius:10, width:"fit-content" }}>
              {tabs.map(t=><TabBtn key={t.id} active={tab===t.id} onClick={()=>setTab(t.id)}>{t.label}</TabBtn>)}
            </div>
          </div>
        </div>

        <div style={{ maxWidth:980, margin:"0 auto", padding:"1.75rem 1.5rem 3rem" }}>
          <div key={tab} className="au">
            {tab==="overview" && <OverviewTab/>}
            {tab==="pipeline" && <PipelineTab/>}
            {tab==="plan"     && <PlanTab/>}
          </div>
        </div>
      </div>
    </>
  );
}
