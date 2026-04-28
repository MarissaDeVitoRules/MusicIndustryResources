<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>There's no such thing as an Industry Plant 🌱</title>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=DM+Sans:ital,opsz,wght@0,9..40,300;0,9..40,400;0,9..40,500;1,9..40,300&display=swap" rel="stylesheet">
<style>
  :root {
    --black: #0a0a0a;
    --white: #f5f2ee;
    --accent: #e8471c;
    --accent2: #f7b731;
    --muted: #7a7469;
    --border: rgba(245,242,238,0.1);
  }
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  body { background: var(--black); color: var(--white); font-family: 'DM Sans', sans-serif; min-height: 100vh; overflow-x: hidden; }

  /* HEADER */
  header { position: relative; padding: 80px 48px 60px; border-bottom: 1px solid var(--border); overflow: hidden; }
  header::before {
    content: ''; position: absolute; inset: 0;
    background: radial-gradient(ellipse 70% 80% at 10% 50%, rgba(232,71,28,0.12) 0%, transparent 60%),
                radial-gradient(ellipse 40% 60% at 90% 20%, rgba(247,183,49,0.06) 0%, transparent 50%);
    pointer-events: none;
  }
  .header-eyebrow {
    font-size: 11px; font-weight: 500; letter-spacing: 0.25em; text-transform: uppercase;
    color: var(--accent); margin-bottom: 20px; display: flex; align-items: center; gap: 10px;
  }
  .header-eyebrow::before { content: ''; display: inline-block; width: 28px; height: 2px; background: var(--accent); }
  h1 { font-family: 'Bebas Neue', sans-serif; font-size: clamp(64px, 10vw, 140px); line-height: 0.9; letter-spacing: 0.02em; margin-bottom: 24px; }
  h1 span { color: var(--accent); }
  .header-sub { font-size: 15px; font-weight: 300; color: var(--muted); max-width: 500px; line-height: 1.6; }
  .header-count { position: absolute; right: 48px; top: 80px; font-family: 'Bebas Neue', sans-serif; font-size: 120px; color: rgba(255,255,255,0.03); line-height: 1; pointer-events: none; user-select: none; }

  /* FILTER */
  .filter-section {
    padding: 22px 48px; border-bottom: 1px solid var(--border);
    display: flex; flex-direction: column; gap: 12px;
    position: sticky; top: 0; z-index: 100;
    background: rgba(10,10,10,0.94); backdrop-filter: blur(16px);
  }
  .filter-row { display: flex; align-items: center; gap: 12px; flex-wrap: wrap; }
  .filter-label { font-size: 10px; letter-spacing: 0.22em; text-transform: uppercase; color: var(--muted); font-weight: 500; white-space: nowrap; min-width: 56px; }
  .filter-pills { display: flex; gap: 6px; flex-wrap: wrap; }
  .pill {
    padding: 6px 13px; border-radius: 100px; font-size: 12px; font-weight: 400;
    cursor: pointer; transition: all 0.18s ease; border: 1px solid var(--border);
    background: transparent; color: var(--muted); white-space: nowrap; letter-spacing: 0.02em;
  }
  .pill:hover { border-color: rgba(245,242,238,0.3); color: var(--white); }
  /* type pills active */
  #typePills .pill.active { background: var(--accent); border-color: var(--accent); color: #fff; }
  /* focus pills active - each gets its own colour */
  [data-focus="women"].active      { background: #b84470; border-color: #b84470; color: #fff; }
  [data-focus="nonbinary"].active  { background: #4a7ec4; border-color: #4a7ec4; color: #fff; }
  [data-focus="queer"].active      { background: #8c44b8; border-color: #8c44b8; color: #fff; }
  [data-focus="trans"].active      { background: #2d9abf; border-color: #2d9abf; color: #fff; }
  [data-focus="lgbtq"].active      { background: #6b3fb4; border-color: #6b3fb4; color: #fff; }
  [data-focus="entrylevel"].active  { background: #2d9a6c; border-color: #2d9a6c; color: #fff; }
  [data-focus="midlevel"].active    { background: #2d6e9a; border-color: #2d6e9a; color: #fff; }
  [data-focus="execlevel"].active   { background: #5a2d9a; border-color: #5a2d9a; color: #fff; }
  [data-focus="student"].active     { background: #9a6e2d; border-color: #9a6e2d; color: #fff; }
  [data-focus="parenting"].active   { background: #b48b2d; border-color: #b48b2d; color: #fff; }
  [data-focus="bipoc"].active       { background: #9a3d2d; border-color: #9a3d2d; color: #fff; }
  [data-focus="disability"].active  { background: #3d7a5a; border-color: #3d7a5a; color: #fff; }
  /* role pills active */
  [data-role="mentor"].active  { background: #c47a1a; border-color: #c47a1a; color: #fff; }
  [data-role="mentee"].active  { background: #1a8fc4; border-color: #1a8fc4; color: #fff; }
  [data-role="both"].active    { background: #3a7a3a; border-color: #3a7a3a; color: #fff; }

  .search-wrap { margin-left: auto; position: relative; }
  .search-wrap svg { position: absolute; left: 13px; top: 50%; transform: translateY(-50%); width: 14px; height: 14px; stroke: var(--muted); }
  #search {
    background: rgba(255,255,255,0.04); border: 1px solid var(--border); border-radius: 100px;
    padding: 7px 16px 7px 34px; color: var(--white); font-family: 'DM Sans', sans-serif;
    font-size: 13px; width: 210px; outline: none; transition: border-color 0.2s;
  }
  #search::placeholder { color: var(--muted); }
  #search:focus { border-color: rgba(245,242,238,0.3); }

  /* RESULTS */
  .results-bar { padding: 16px 48px; }
  .results-count { font-size: 12px; color: var(--muted); }
  .results-count strong { color: var(--white); font-weight: 500; }

  /* GRID */
  .grid { padding: 8px 48px 80px; display: grid; grid-template-columns: repeat(auto-fill, minmax(300px, 1fr)); gap: 1px; background: var(--border); }

  /* CARD */
  .card {
    background: var(--black); padding: 28px;
    display: flex; flex-direction: column; gap: 10px;
    transition: background 0.2s; position: relative; overflow: hidden;
    animation: fadeUp 0.4s ease both;
  }
  .card::before {
    content: ''; position: absolute; inset: 0;
    background: radial-gradient(ellipse 80% 60% at 0% 100%, rgba(232,71,28,0.06) 0%, transparent 60%);
    opacity: 0; transition: opacity 0.3s; pointer-events: none;
  }
  .card:hover { background: #111; }
  .card:hover::before { opacity: 1; }

  .card-type { display: inline-flex; align-items: center; font-size: 10px; letter-spacing: 0.18em; text-transform: uppercase; font-weight: 500; padding: 3px 9px; border-radius: 4px; width: fit-content; }
  .type-community { background: rgba(232,71,28,0.12);  color: #e8471c; }
  .type-advocacy  { background: rgba(247,183,49,0.12);  color: #f7b731; }
  .type-safety    { background: rgba(100,220,180,0.12); color: #64dcb4; }
  .type-audio     { background: rgba(160,120,255,0.12); color: #a078ff; }
  .type-live      { background: rgba(255,120,160,0.12); color: #ff78a0; }
  .type-wellness  { background: rgba(80,200,240,0.12);  color: #50c8f0; }
  .type-education { background: rgba(200,240,80,0.12);  color: #b8d440; }
  .type-resource   { background: rgba(200,200,200,0.1);  color: #aaa; }
  .type-mentorship { background: rgba(255,165,50,0.12);  color: #ffa530; }
  .type-profdev    { background: rgba(100,180,255,0.12); color: #64b4ff; }
  .type-mentalhealth { background: rgba(180,120,220,0.12); color: #c080e8; }

  .card-name { font-family: 'Bebas Neue', sans-serif; font-size: 24px; letter-spacing: 0.04em; color: var(--white); line-height: 1; }
  .card-desc { font-size: 13px; font-weight: 300; color: var(--muted); line-height: 1.65; flex: 1; }

  /* FOCUS TAGS ON CARD */
  .card-tags { display: flex; flex-wrap: wrap; gap: 5px; }
  .ftag { font-size: 10px; letter-spacing: 0.1em; text-transform: uppercase; padding: 2px 7px; border-radius: 3px; }
  .ftag-women      { background: rgba(184,68,112,0.12); color: #e080a8; border: 1px solid rgba(184,68,112,0.22); }
  .ftag-nonbinary  { background: rgba(74,126,196,0.12); color: #80a8e0; border: 1px solid rgba(74,126,196,0.22); }
  .ftag-queer      { background: rgba(140,68,184,0.12); color: #c080e0; border: 1px solid rgba(140,68,184,0.22); }
  .ftag-trans      { background: rgba(45,154,191,0.12); color: #70cce8; border: 1px solid rgba(45,154,191,0.22); }
  .ftag-lgbtq      { background: rgba(107,63,180,0.12); color: #aa80e0; border: 1px solid rgba(107,63,180,0.22); }
  .ftag-entrylevel  { background: rgba(45,154,108,0.12); color: #70ddaa; border: 1px solid rgba(45,154,108,0.22); }
  .ftag-midlevel    { background: rgba(45,110,154,0.12); color: #70a8d8; border: 1px solid rgba(45,110,154,0.22); }
  .ftag-execlevel   { background: rgba(90,45,154,0.12);  color: #a870d8; border: 1px solid rgba(90,45,154,0.22); }
  .ftag-student     { background: rgba(154,110,45,0.12); color: #d8a870; border: 1px solid rgba(154,110,45,0.22); }
  .ftag-parenting   { background: rgba(180,139,45,0.12); color: #e0c070; border: 1px solid rgba(180,139,45,0.22); }
  .ftag-bipoc       { background: rgba(154,61,45,0.12);  color: #d88070; border: 1px solid rgba(154,61,45,0.22); }
  .ftag-disability  { background: rgba(61,122,90,0.12);  color: #70c4a0; border: 1px solid rgba(61,122,90,0.22); }

  /* ROLE TAGS */
  .role-tags { display: flex; flex-wrap: wrap; gap: 5px; }
  .rtag { font-size: 10px; letter-spacing: 0.1em; text-transform: uppercase; padding: 2px 7px; border-radius: 3px; display: inline-flex; align-items: center; gap: 4px; }
  .rtag::before { content: ''; width: 5px; height: 5px; border-radius: 50%; display: inline-block; flex-shrink: 0; }
  .rtag-mentor { background: rgba(196,122,26,0.12); color: #e09040; border: 1px solid rgba(196,122,26,0.22); }
  .rtag-mentor::before { background: #e09040; }
  .rtag-mentee { background: rgba(26,143,196,0.12); color: #50b8e8; border: 1px solid rgba(26,143,196,0.22); }
  .rtag-mentee::before { background: #50b8e8; }
  .rtag-both   { background: rgba(58,122,58,0.12);  color: #70c870; border: 1px solid rgba(58,122,58,0.22); }
  .rtag-both::before { background: #70c870; }

  .card-footer { display: flex; align-items: center; justify-content: space-between; padding-top: 14px; border-top: 1px solid var(--border); margin-top: 4px; }
  .card-note { font-size: 11px; color: var(--accent2); font-style: italic; font-weight: 300; }
  .card-link { display: inline-flex; align-items: center; gap: 5px; font-size: 12px; color: var(--white); text-decoration: none; opacity: 0.45; transition: opacity 0.2s; }
  .card-link:hover { opacity: 1; }
  .card-link svg { width: 11px; height: 11px; stroke: currentColor; }

  .empty { grid-column: 1/-1; padding: 80px; text-align: center; color: var(--muted); }
  .empty-icon { font-size: 48px; margin-bottom: 16px; }
  .empty p { font-size: 15px; font-weight: 300; }

  @keyframes fadeUp { from { opacity: 0; transform: translateY(16px); } to { opacity: 1; transform: translateY(0); } }

  footer { border-top: 1px solid var(--border); padding: 28px 48px; display: flex; align-items: center; justify-content: space-between; color: var(--muted); font-size: 12px; letter-spacing: 0.05em; }

  @media (max-width: 640px) {
    header, .filter-section, .results-bar, .grid, footer { padding-left: 20px; padding-right: 20px; }
    .grid { grid-template-columns: 1fr; }
    .search-wrap { margin-left: 0; width: 100%; }
    #search { width: 100%; }
    .header-count { display: none; }
  }
</style>
</head>
<body>

<header>
  <div class="header-eyebrow">There's no such thing as an Industry Plant 🌱</div>
  <h1>MUSIC<br><span>INDUSTRY</span><br>RESOURCES</h1>
  <p class="header-sub">A curated directory of organizations, communities, collectives, and general resources for everyone.</p>
  <div class="header-count" id="headerCount">83</div>
</header>

<div class="filter-section">
  <div class="filter-row">
    <span class="filter-label">Category</span>
    <div class="filter-pills" id="typePills">
      <button class="pill active" data-type="all">All</button>
      <button class="pill" data-type="community">Community</button>
      <button class="pill" data-type="advocacy">Advocacy</button>
      <button class="pill" data-type="safety">Safety</button>
      <button class="pill" data-type="audio">Audio & Production</button>
      <button class="pill" data-type="live">Live & Events</button>
      <button class="pill" data-type="wellness">Wellness</button>
      <button class="pill" data-type="education">Education</button>
      <button class="pill" data-type="resource">Tools & Resources</button>
      <button class="pill" data-type="mentorship">Mentorship</button>
      <button class="pill" data-type="profdev">Professional Dev</button>
      <button class="pill" data-type="mentalhealth">Mental Health</button>
    </div>
  </div>
  <div class="filter-row">
    <span class="filter-label">Focus</span>
    <div class="filter-pills" id="focusPills">
      <button class="pill active" data-focus="all">All</button>
      <button class="pill" data-focus="women">Women</button>
      <button class="pill" data-focus="nonbinary">Non-Binary</button>
      <button class="pill" data-focus="queer">Queer</button>
      <button class="pill" data-focus="trans">Trans</button>
      <button class="pill" data-focus="lgbtq">LGBTQ+</button>
      <button class="pill" data-focus="bipoc">BIPOC</button>
      <button class="pill" data-focus="disability">Disability</button>
      <button class="pill" data-focus="student">Student</button>
      <button class="pill" data-focus="entrylevel">Entry Level</button>
      <button class="pill" data-focus="midlevel">Mid Level</button>
      <button class="pill" data-focus="execlevel">Exec Level</button>
      <button class="pill" data-focus="parenting">Parenting</button>
    </div>
    <div class="search-wrap">
      <svg viewBox="0 0 24 24" fill="none" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
        <circle cx="11" cy="11" r="8"/><line x1="21" y1="21" x2="16.65" y2="16.65"/>
      </svg>
      <input type="text" id="search" placeholder="Search organizations…">
    </div>
  </div>
  <div class="filter-row">
    <span class="filter-label">Role</span>
    <div class="filter-pills" id="rolePills">
      <button class="pill active" data-role="all">All</button>
      <button class="pill" data-role="mentor">Open to Mentors</button>
      <button class="pill" data-role="mentee">Open to Mentees</button>
      <button class="pill" data-role="both">Both</button>
    </div>
  </div>
</div>

<div class="results-bar">
  <div class="results-count" id="resultsCount"><strong>83</strong> organizations</div>
</div>

<div class="grid" id="grid"></div>

<footer>
  <span>There's no such thing as an Industry Plant 🌱</span>
  <span>See a mistake? Something to add? Want to tell us something? <a href="mailto:md@marissadevito.com" style="color:var(--accent);text-decoration:none;">Drop us a note</a></span>
</footer>

<script>
const typeLabels = {
  community:"Community", advocacy:"Advocacy", safety:"Safety",
  audio:"Audio & Production", live:"Live & Events", wellness:"Wellness",
  education:"Education", resource:"Tools & Resources", mentorship:"Mentorship",
  profdev:"Professional Dev", mentalhealth:"Mental Health"
};
const focusLabels = {
  women:"Women", nonbinary:"Non-Binary", queer:"Queer",
  trans:"Trans", lgbtq:"LGBTQ+", bipoc:"BIPOC", disability:"Disability",
  student:"Student", entrylevel:"Entry Level", midlevel:"Mid Level",
  execlevel:"Exec Level", parenting:"Parenting"
};
const roleLabels = {
  mentor:"Open to Mentors", mentee:"Open to Mentees", both:"Open to Both"
};

const resources = [
  { name:"She Said So", url:"https://www.shesaid.so", desc:"A global community of women, gender nonconforming people and allies in the music industry.", type:"community", note:"", focus:["women","nonbinary","queer","lgbtq","midlevel","execlevel"] },
  { name:"Amplify Her Voice", url:"https://www.amplifyhervoice.org/", desc:"Championing gender equality in the music industry and advancing women's careers through events, programs, and community.", type:"advocacy", note:"", focus:["women"] },
  { name:"We Make Noise", url:"", desc:"Harnessing the power of music and technology to advance global gender equity, equipping communities with tools that cultivate limitless potential.", type:"community", note:"FKA Beatz by Girlz", focus:["women","nonbinary"] },
  { name:"Calling All Crows", url:"https://www.callingallcrows.org/", desc:"Connecting music fans to feminist movements for justice and equality.", type:"advocacy", note:"", focus:["women","queer","lgbtq"] },
  { name:"Color of Music Collective", url:"https://www.colorofmusiccollective.com/mission", desc:"Amplifying the voices of people of color and LGBTQ+ individuals working in the music industry.", type:"community", note:"", focus:["lgbtq","queer","trans","bipoc"] },
  { name:"Femme House", url:"https://www.thisisfemmehouse.com/", desc:"Creating a more equitable industry for femme and gender expansive music producers and DJs.", type:"community", note:"", focus:["women","nonbinary","queer","lgbtq"] },
  { name:"Gender Amplified", url:"https://www.genderamplified.org/", desc:"A 501c3 non-profit empowering women and gender-expansive music producers by inspiring the next generation of audio professionals.", type:"audio", note:"", focus:["women","nonbinary","entrylevel"] },
  { name:"Girls Against", url:"https://www.girlsagainst.co.uk/", desc:"Fighting against sexual assault at live music events.", type:"safety", note:"", focus:["women"] },
  { name:"Girls Behind the Rock Show", url:"https://www.instagram.com/girlsbtrs/", desc:"501(c)(3) Non-Profit helping advance women & marginalized genders in the music industry through education & hands-on opportunities.", type:"education", note:"", focus:["women","nonbinary","entrylevel"] },
  { name:"Girls Who Listen", url:"https://www.girlswholisten.org/", desc:"Supporting future female creatives and executives within the music industry.", type:"community", note:"", focus:["women","entrylevel"] },
  { name:"Noise For Now", url:"https://noisefornow.org/", desc:"Enabling artists and entertainers to connect with and support grassroots organizations working in Reproductive Justice, including abortion access.", type:"advocacy", note:"", focus:["women","queer","lgbtq"] },
  { name:"Safetour", url:"https://www.safetour.org/", desc:"Making the music tour community safe, equitable and inclusive.", type:"safety", note:"", focus:["women","nonbinary","lgbtq"] },
  { name:"She Is The Music", url:"https://sheisthemusic.org/", desc:"Advancing equality, inclusivity and opportunity for women in music.", type:"advocacy", note:"", focus:["women"] },
  { name:"We Are Moving the Needle", url:"https://www.wearemovingtheneedle.org/", desc:"Creating measurable change for women in the recording industry.", type:"advocacy", note:"", focus:["women"] },
  { name:"Women in CTRL", url:"https://womeninctrl.com/", desc:"A non-profit music development organisation advancing gender equality by developing, supporting and championing music creators from under-represented groups.", type:"community", note:"", focus:["women","nonbinary"] },
  { name:"Women in Music", url:"https://www.womeninmusic.org/", desc:"Established in 1985, advancing equality, visibility and opportunities for women in the musical arts through education, support, empowerment and recognition.", type:"advocacy", note:"", focus:["women","entrylevel","midlevel","execlevel"] },
  { name:"Women's Audio Mission", url:"https://womensaudiomission.org/", desc:"Changing the face of sound by providing hands-on training, work experience, and job placement to women, girls, and gender-expansive individuals in creative technology.", type:"audio", note:"", focus:["women","nonbinary","entrylevel"] },
  { name:"Book More Women", url:"https://www.bookmorewomen.com/", desc:"Visualizing and addressing the pervasive gender imbalance at music festivals, tracking progress towards better representation on future lineups.", type:"advocacy", note:"", focus:["women"] },
  { name:"Diversify the Stage", url:"https://www.diversifythestage.org/", desc:"A 501(c)3 providing greater access to careers in live music, events, and touring for historically marginalized and underrepresented communities.", type:"live", note:"", focus:["women","nonbinary","lgbtq","bipoc","entrylevel"] },
  { name:"EqualizeHer", url:"https://www.equalizeher.org/", desc:"An initiative to achieve equal representation of women across all aspects of the music industry — from recording studios to stages to board rooms.", type:"advocacy", note:"", focus:["women"] },
  { name:"Femme It Forward", url:"https://www.femmeitforward.com/", desc:"A female-led music and entertainment company celebrating, educating, and empowering women through concerts, tours, festivals, comedy shows, and more.", type:"live", note:"", focus:["women"] },
  { name:"Gritty in Pink", url:"https://www.grittyinpink.co/", desc:"A community of diverse female creators working in the music industry, providing connection, access and opportunities through an inclusive network.", type:"community", note:"", focus:["women","queer","lgbtq"] },
  { name:"Key Change", url:"https://www.keychangeus.com/", desc:"Bringing underrepresented genders in the music industry to the main stage.", type:"advocacy", note:"", focus:["women","nonbinary","trans"] },
  { name:"Live Nation Women", url:"https://livenationwomenfund.livenation.com/", desc:"A global, early-stage fund improving gender equality by investing in female-founded live music businesses and female entrepreneurs across the live music space.", type:"live", note:"", focus:["women"] },
  { name:"Live Out L!ve Foundation", url:"https://www.liveoutlive.com/lol-foundation", desc:"A 501C3 organization amplifying commitment to open doors and set the stage for the next generation of diverse talent.", type:"live", note:"", focus:["women","lgbtq","entrylevel"] },
  { name:"Music Production for Women", url:"https://musicproductionforwomen.com/front-page", desc:"Encouraging and empowering more women in music production and technology through education, community support, and visible role models.", type:"audio", note:"", focus:["women","entrylevel"] },
  { name:"The Photo Ladies", url:"https://www.thephotoladies.com/local-music-project", desc:"A collective of women and non-binary photographers bound by their love of music, supporting and representing one another in the world.", type:"community", note:"", focus:["women","nonbinary"] },
  { name:"Safe Gigs for Women", url:"https://www.instagram.com/safegigs4women/", desc:"Working with venues, promoters, artists and gig-goers to fight sexual assault and harassment at live music events.", type:"safety", note:"", focus:["women","lgbtq"] },
  { name:"SoundGirls", url:"https://soundgirls.org/", desc:"Empowering the next generation of women in audio.", type:"audio", note:"", focus:["women","entrylevel"] },
  { name:"The Wavelength Collective", url:"https://www.instagram.com/thewavelengthcollective/", desc:"A space dedicated to highlighting women who thrive behind the scenes of the music industry.", type:"community", note:"", focus:["women"] },
  { name:"Women That Rock", url:"https://www.womenthatrock.co/", desc:"Supporting the best up-and-coming women in music through daily artist features, articles and events. Queer & GNC inclusive.", type:"community", note:"", focus:["women","queer","nonbinary","lgbtq"] },
  { name:"Grammy U", url:"https://www.recordingacademy.com/membership/grammy-u", desc:"Recording Academy program for college students pursuing careers in the music industry.", type:"education", note:"", focus:["student","entrylevel"] },
  { name:"The Digilogue", url:"https://www.thedigilogue.com/about", desc:"A diverse music and tech community of creators and industry professionals curating conversations around industry education, career resources, and artist discovery.", type:"education", note:"Not female-specific", focus:["entrylevel"] },
  { name:"Girl Be Heard", url:"https://girlbeheard.org/", desc:"Building leaders, change-makers and activists through amplifying the voices of girls and young women via socially conscious theater-making and performance.", type:"advocacy", note:"", focus:["women","entrylevel"] },
  { name:"Female Composer Safety League", url:"https://www.femalecomposersafetyleague.org/", desc:"Providing visibility, safety, advancement, and empowerment of women with a trauma-informed space for victims of sexual abuse in the music composing industry.", type:"safety", note:"", focus:["women"] },
  { name:"Alliance for Women Film Composers", url:"https://theawfc.com/", desc:"A community of composers and colleagues supporting and celebrating women composers through advocacy and education across film, TV, video games and multimedia.", type:"audio", note:"", focus:["women"] },
  { name:"Hire Survivors Hollywood", url:"https://hiresurvivorshollywood.org/", desc:"Working to end career retaliation against survivors of sexual violence in the entertainment industry.", type:"safety", note:"", focus:["women","lgbtq"] },
  { name:"Future of Music Coalition", url:"https://www.futureofmusic.org/about", desc:"A D.C.-based nonprofit supporting a musical ecosystem where artists flourish and are compensated fairly and transparently for their work.", type:"advocacy", note:"", focus:[] },
  { name:"Symphonic Women Empowered", url:"https://symphonic.com/women-empowered/", desc:"A mentorship program empowering women in the music industry through guidance and professional development.", type:"profdev", note:"", focus:["women","entrylevel","midlevel"] },
  { name:"Salary Transparency Sheet", url:"https://docs.google.com/spreadsheets/d/1D9i2TA1Zs9AW1HNdcr_O53XPhuza2gqj7B0xtaoccqg/", desc:"A community salary survey advancing pay transparency in the music industry.", type:"resource", note:"", focus:[] },
  { name:"Mamas in Music", url:"https://mamasinmusic.org/", desc:"A non-profit supporting mothers working in the music industry — building community, hosting song camps and events, and creating a village for mamas navigating a career in music.", type:"community", note:"", focus:["women","parenting"] },
  { name:"Moms in Music", url:"https://www.momsinmusic.org/", desc:"A community and membership organization for moms working in the music industry, offering events, programs, and peer support for navigating parenthood and a music career simultaneously.", type:"community", note:"", focus:["women","parenting"] },
  { name:"Family Alliance in Music (FAM)", url:"https://www.familyallianceinmusic.org/", desc:"An organization dedicated to supporting music industry professionals who are also parents and caregivers, providing resources, community, and advocacy for family-friendly workplaces in music.", type:"advocacy", note:"", focus:["parenting"] },
  { name:"BAK Pitch Perfect", url:"https://bakpitchperfect.org/", desc:"A business community for women entrepreneurs in the music industry — part of the B.A.K. Play.Ground ecosystem — connecting members through shared work opportunities, music business education, and industry dialogue.", type:"community", note:"", focus:["women","entrylevel"] },
  { name:"B.A.K. Play.Ground", url:"https://www.bigasskids.com/playground", desc:"A membership platform connecting artists, creatives, and music professionals through vetted hiring opportunities, music business education, and community. Offers tiers for both artists and industry professionals.", type:"resource", note:"", focus:["entrylevel"] },
  { name:"Lone Wolves Club", url:"https://lonewolvesclub.co/", desc:"A 501(c)(3) nonprofit community for music, tech, and entertainment professionals — born from disruption, built on connection. Turns isolation into collaboration by fostering skill-building and opportunity across disciplines.", type:"community", note:"", focus:[] },

  // ── WELLNESS & MENTAL HEALTH ──────────────────────────────────────────────
  { name:"MusiCares", url:"https://www.musicares.org/", desc:"The Recording Academy's safety net for the music community — providing mental health, addiction recovery, health services, and emergency financial assistance to musicians, songwriters, engineers, producers, live crew, and anyone whose livelihood depends on music.", type:"mentalhealth", note:"", focus:[] },
  { name:"Music Health Alliance", url:"https://musichealthalliance.com/", desc:"Protecting, directing, and connecting music professionals with healthcare — offering free services including insurance navigation, medical bill assistance, and healthcare access for musicians, industry workers, and their families.", type:"mentalhealth", note:"", focus:[] },
  { name:"SIMS Foundation", url:"https://simsfoundation.org/", desc:"Founded in 1995, providing mental health and substance use recovery services to musicians, music industry professionals, and their families through accessible managed care, education, and community partnerships.", type:"mentalhealth", note:"Austin-based", focus:[] },
  { name:"Porter's Call", url:"https://porterscall.com/", desc:"Offering free, confidential counseling, support, and encouragement to recording artists and their families — a safe refuge for signed and independent touring artists to deal with the unique issues they face at no charge.", type:"mentalhealth", note:"", focus:[] },
  { name:"SoundCheck Wellness", url:"https://soundcheckwellness.com/", desc:"A nonprofit providing financial assistance to musicians and tour support crew for health insurance premiums, mental health counseling, dental and vision care, and substance abuse treatment — before reaching the point of crisis.", type:"mentalhealth", note:"", focus:[] },
  { name:"Sweet Relief Musicians Fund", url:"https://www.sweetrelief.org/", desc:"Healing musicians and music industry workers in need by providing vital financial assistance to career musicians facing illness, disability, or age-related problems.", type:"mentalhealth", note:"", focus:["disability"] },
  { name:"Musicians Foundation", url:"https://www.musiciansfoundation.org/", desc:"Since 1914, providing direct financial aid and assistance to professional musicians and their families in cases of need, illness, or hardship.", type:"mentalhealth", note:"", focus:[] },
  { name:"Music Industry Therapist Collective", url:"https://www.musicindustrytherapist.com/", desc:"A collective of psychotherapists and counselors — all with real music industry backgrounds — offering high-quality therapy, seminars, and workshops tailored specifically to the mental health needs of music professionals.", type:"mentalhealth", note:"", focus:[] },
  { name:"Backline", url:"https://backline.care/", desc:"Mental health and wellness resources for the music industry.", type:"mentalhealth", note:"", focus:[] },
  { name:"Touring Professionals Alliance", url:"https://www.touringprofessionals.com/", desc:"A 501(c)(3) nonprofit connecting touring music professionals and their families with mental health, wellness, and industry resources tailored to the unique demands of life on the road.", type:"mentalhealth", note:"", focus:[] },

  // ── PROFESSIONAL ORGS & ADVOCACY ─────────────────────────────────────────
  { name:"RAMPD", url:"https://rampd.org/", desc:"Recording Artists and Music Professionals with Disabilities — a UN-recognized platform equipping the music and live entertainment industries with disability-inclusive tools, trainings, and a global directory of peer-vetted creators and professionals with disabilities and neurodivergence.", type:"community", note:"", focus:["lgbtq","disability"] },
  { name:"Nashville Songwriters Association International (NSAI)", url:"https://nashvillesongwriters.com/", desc:"The world's largest not-for-profit songwriters trade association, with 5,000+ members across the US and beyond. Dedicated to protecting the rights of and serving aspiring and professional songwriters in all genres.", type:"advocacy", note:"", focus:[] },
  { name:"Audio Engineering Society (AES)", url:"https://www.aes.org/", desc:"The only professional society devoted exclusively to audio technology, uniting audio engineers, creative artists, scientists, and students worldwide since 1948 by promoting advances in audio and disseminating new knowledge and research.", type:"community", note:"", focus:[] },
  { name:"Society of Professional Audio Recording Services (SPARS)", url:"https://www.spars.com/", desc:"A nonprofit association representing professionals in the US recording industry — studios, engineers, and audio professionals — offering networking, education, and industry advocacy.", type:"community", note:"", focus:[] },
  { name:"Music Business Association", url:"https://musicbiz.org/", desc:"Representing the full music business ecosystem — labels, streaming services, publishers, distributors, tech companies and more — through the annual Music Biz conference, educational resources, webinars, and the #NEXTGEN_NOW program for emerging professionals.", type:"profdev", note:"", focus:["entrylevel","midlevel"] },
  { name:"Association of Music Producers (AMP)", url:"https://www.ampnow.com/", desc:"Founded in 1998 to educate members and the wider advertising, production, and media communities on all facets of music production — from creation to final use — through events, resources, and advocacy.", type:"community", note:"", focus:[] },
  { name:"Future of Music Coalition", url:"https://www.futureofmusic.org/about", desc:"A D.C.-based nonprofit supporting a musical ecosystem where artists flourish and are compensated fairly and transparently for their work.", type:"advocacy", note:"", focus:[] },
  { name:"Volunteer Lawyers for the Arts", url:"https://vlany.org/", desc:"Since 1969, pioneering arts-related legal aid and educational programs about legal and business issues affecting artists and arts organizations — connecting creatives with pro bono legal services.", type:"resource", note:"", focus:[] },
  { name:"New Music USA", url:"https://newmusicusa.org/", desc:"Committed to the vitality of the new music community — supporting composers, performers, presenters, producers, and fans through grants, resources, and a platform for discovery and connection.", type:"community", note:"", focus:[] },
  { name:"A2IM (American Association of Independent Music)", url:"https://a2im.org/", desc:"A 501(c)(6) trade organization representing 700+ independent US music labels — advocating for independent artists and labels in the marketplace, media, and on Capitol Hill.", type:"advocacy", note:"", focus:[] },
  { name:"Touring Professionals Alliance", url:"https://www.touringprofessionals.com/", desc:"A 501(c)(3) nonprofit connecting touring music professionals and their families with mental health, wellness, and industry resources tailored to the unique demands of life on the road.", type:"wellness", note:"", focus:[] },

  // ── EDUCATION & CAREER DEVELOPMENT ───────────────────────────────────────
  { name:"SOLID (Supporters of Live Independent Diversity)", url:"https://www.solidmusic.org/", desc:"Improving the future of the music industry by strengthening professional relationships and educating a diverse group of future executives while serving the community.", type:"profdev", note:"", focus:["entrylevel","midlevel"] },
  { name:"Young Entertainment Professionals", url:"https://yepnetwork.org/", desc:"Creating a platform for the entertainment industry to thrive in a supportive and creative environment for the betterment of its members through networking events, showcases, mentorship, and educational development.", type:"profdev", note:"", focus:["entrylevel","midlevel"] },
  { name:"Production Music Association (PMA)", url:"https://pmamusic.com/", desc:"Representing production music publishers and composers — providing education on industry trends, digital demo feedback, professional development, and advocacy for performance royalty collection across digital platforms.", type:"community", note:"", focus:[] },
  { name:"No Creeps!", url:"https://www.sharpedgesrecords.com/nocreeps", desc:"A growing movement and coalition of music professionals dedicated to industry-wide safety, mental health, and inclusivity — hosting events, providing resources, sparking crucial conversations, and showcasing artists passionate about making the music industry safer for everyone. Founded by Sharp Edges Records.", type:"safety", note:"", focus:["women","lgbtq"] },

  // ── MENTORSHIP PROGRAMS ─────────────────────────────────────────────────
  { name:"Grammy U Mentorship Program", url:"https://www.recordingacademy.com/membership/grammy-u", desc:"Annual 6-month one-on-one program pairing college students with Recording Academy voting members across six tracks: Producing & Engineering, Performance, Songwriting & Composition, Content Creation & Marketing, Music Business, and Entertainment Law.", type:"mentorship", note:"Presented by Amazon Music", focus:["student","entrylevel"], role:"both", tracks:["Artists & Performers","Songwriters","Producers & Engineers","Music Business","Marketing","Entertainment Law"], who:"College students (mentees); Recording Academy voting/professional members (mentors)" },
  { name:"Women in Music Mentorship Program", url:"https://www.womeninmusic.org/mentorship", desc:"Structured one-on-one terms rotating across industry focus areas — Artists & Songwriters, Producers & Engineers, Managers, Agents, Publishers and more. Pairs women of all career levels based on where they are right now.", type:"mentorship", note:"WIM membership required", focus:["women","entrylevel","midlevel","execlevel"], role:"both", tracks:["Artists & Performers","Songwriters","Producers & Engineers","Managers & Agents","Publishers"], who:"Women & allies at any career stage (both roles); WIM members" },
  { name:"SoundGirls Online Mentoring", url:"https://soundgirls.org/soundgirls-online-mentoring/", desc:"Ongoing group mentoring program pairing SoundGirls members with professional audio engineers across recording, live sound, post-production, and audio manufacturing for virtual sessions.", type:"mentorship", note:"SoundGirls membership required", focus:["women","entrylevel"], role:"both", tracks:["Producers & Engineers","Live Sound","Post-Production"], who:"Women & gender-expansive audio professionals (mentees); working audio professionals (mentors)" },
  { name:"She Is The Music Mentorship Program", url:"https://sheisthemusic.org/", desc:"SITM's mentorship program empowers the next generation of women in music by connecting young women with industry professionals actively working in touring, producing, songwriting, and more.", type:"mentorship", note:"", focus:["women","entrylevel"], role:"mentee", tracks:["Artists & Performers","Songwriters","Producers & Engineers","Touring"], who:"Young women pursuing music careers (mentees)" },
  { name:"Symphonic Women Empowered+", url:"https://symphonic.com/women-empowered/", desc:"Global mentorship initiative connecting women across the music industry with established professionals at companies like Amazon Music, Atlantic Records, Spotify, and more. Open to apply as mentor or mentee.", type:"mentorship", note:"", focus:["women"], role:"both", tracks:["Music Business","Artists & Performers","Marketing"], who:"Women in music at any career stage; open to both mentors and mentees globally" },
  { name:"MINT Talent Group Women's Mentorship", url:"https://www.minttalentgroup.com/mentorship", desc:"Virtual mentorship program creating a safe space for women and nonbinary leaders in live music, designed to empower future leaders through open dialogue, guidance, and education around live touring topics.", type:"mentorship", note:"Ages 18+", focus:["women","nonbinary","lgbtq"], role:"mentee", tracks:["Live Sound","Touring","Music Business"], who:"Women & nonbinary people pursuing live touring careers (mentees)" },
  { name:"VOX Program — NIVF", url:"https://www.nivf.org/vox", desc:"Venue Operations eXperience: paid 8-week internships plus 3-month mentorship at independent venues for POC, women, LGBTQ+, and people with disabilities. Tracks in digital marketing and front-of-house/production. Also recruiting mentors.", type:"mentorship", note:"National Independent Venue Foundation", focus:["women","lgbtq","entrylevel"], role:"both", tracks:["Live Sound","Music Business","Marketing"], who:"POC, women, LGBTQ+, and people with disabilities (mentees); experienced venue pros (mentors)" },
  { name:"Queer|Art|Mentorship", url:"https://www.queer-art.org/mentorship", desc:"Year-long creative and professional development program pairing early-career LGBTQ+ artists with established mentors across Film, Literature, Performance, and Visual Art. Now expanded nationally across the US.", type:"mentorship", note:"15th year running", focus:["lgbtq","queer","trans","nonbinary"], role:"both", tracks:["Artists & Performers"], who:"Early-career LGBTQ+ artists (fellows/mentees); established LGBTQ+ artists (mentors). US-based, not currently enrolled in school" },
  { name:"Latin Grammy Cultural Foundation Mentorship", url:"https://www.latingrammyculturalfoundation.org/en/what-we-do/mentorship", desc:"The 'Leading Ladies of Entertainment Connect TogetHER' program, in partnership with She Is The Music, pairs young women seeking careers in music and entertainment with senior Latin music industry executives for one-on-one virtual mentoring.", type:"mentorship", note:"In partnership with SITM", focus:["women"], role:"mentee", tracks:["Artists & Performers","Music Business","Songwriters"], who:"Young women pursuing music and entertainment careers (mentees)" },
  { name:"Maestra Music Mentorship", url:"https://maestramusic.org/mentorship/", desc:"A 6-month partnering program connecting early-career mentees (21+) interested in making music for theatre with professional women and nonbinary people currently working in the field.", type:"mentorship", note:"Applications open annually", focus:["women","nonbinary"], role:"both", tracks:["Songwriters","Composers"], who:"Early-career (21+) aspiring theatre composers/musicians (mentees); professional women & nonbinary theatre music creators (mentors)" },
  { name:"Key Change Mentorship", url:"https://www.keychangeus.com/", desc:"Key Change connects underrepresented genders in music with mentors to support career development, festival bookings, and visibility. Focused on bringing more diverse voices to main stages.", type:"mentorship", note:"", focus:["women","nonbinary","trans"], role:"both", tracks:["Artists & Performers","Music Business"], who:"Women, nonbinary, and trans music professionals (both roles)" },
  { name:"Gender Amplified Mentorship", url:"https://www.genderamplified.org/", desc:"Mentorship and professional development for women and gender-expansive music producers, connecting emerging audio professionals with established mentors in the production and engineering space.", type:"mentorship", note:"", focus:["women","nonbinary","entrylevel"], role:"both", tracks:["Producers & Engineers"], who:"Women & gender-expansive emerging producers (mentees); established producers (mentors)" }
];

let activeType  = "all";
let activeFocus = "all";
let activeRole  = "all";
let searchQuery = "";

function buildCards() {
  const grid = document.getElementById("grid");
  grid.innerHTML = "";
  const q = searchQuery.toLowerCase();
  const filtered = resources.filter(r => {
    const matchType  = activeType  === "all" || r.type === activeType;
    const matchFocus = activeFocus === "all" || (r.focus && r.focus.includes(activeFocus));
    const matchRole  = activeRole  === "all" || !r.role || r.role === activeRole || r.role === "both";
    const matchSearch = !q || r.name.toLowerCase().includes(q) || r.desc.toLowerCase().includes(q) || (r.who && r.who.toLowerCase().includes(q));
    return matchType && matchFocus && matchRole && matchSearch;
  });

  document.getElementById("resultsCount").innerHTML =
    `<strong>${filtered.length}</strong> organization${filtered.length !== 1 ? "s" : ""}`;
  document.getElementById("headerCount").textContent = filtered.length;

  if (filtered.length === 0) {
    grid.innerHTML = `<div class="empty"><div class="empty-icon">🎵</div><p>No results found. Try a different filter or search term.</p></div>`;
    return;
  }

  filtered.forEach((r, i) => {
    const card = document.createElement("div");
    card.className = "card";
    card.style.animationDelay = `${i * 25}ms`;
    const tagsHTML = (r.focus || []).map(f => `<span class="ftag ftag-${f}">${focusLabels[f]}</span>`).join("");
    const roleHTML = r.role ? `<span class="rtag rtag-${r.role}">${roleLabels[r.role]}</span>` : "";
    const tracksHTML = r.tracks ? r.tracks.map(t => `<span style="font-size:10px;color:var(--muted);background:rgba(255,255,255,0.04);padding:2px 7px;border-radius:3px;letter-spacing:0.05em;">${t}</span>`).join("") : "";
    const whoHTML = r.who ? `<p style="font-size:11px;color:var(--muted);font-style:italic;line-height:1.5;"><span style="color:rgba(245,242,238,0.4);font-style:normal;letter-spacing:0.06em;font-size:9px;text-transform:uppercase;">Who: </span>${r.who}</p>` : "";
    card.innerHTML = `
      <div style="display:flex;gap:6px;flex-wrap:wrap;align-items:center;">
        <span class="card-type type-${r.type}">${typeLabels[r.type]}</span>
        ${roleHTML}
      </div>
      <div class="card-name">${r.name}</div>
      <p class="card-desc">${r.desc}</p>
      ${tracksHTML ? `<div class="card-tags" style="gap:4px;">${tracksHTML}</div>` : ""}
      ${whoHTML}
      ${tagsHTML ? `<div class="card-tags">${tagsHTML}</div>` : ""}
      <div class="card-footer">
        <span class="card-note">${r.note || ""}</span>
        ${r.url ? `<a class="card-link" href="${r.url}" target="_blank" rel="noopener">Visit <svg viewBox="0 0 24 24" fill="none" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"/><polyline points="15 3 21 3 21 9"/><line x1="10" y1="14" x2="21" y2="3"/></svg></a>` : ""}
      </div>`;
    grid.appendChild(card);
  });
}

document.getElementById("rolePills").addEventListener("click", e => {
  const btn = e.target.closest("[data-role]");
  if (!btn) return;
  document.querySelectorAll("#rolePills .pill").forEach(p => p.classList.remove("active"));
  btn.classList.add("active");
  activeRole = btn.dataset.role;
  buildCards();
});

document.getElementById("typePills").addEventListener("click", e => {
  const btn = e.target.closest("[data-type]");
  if (!btn) return;
  document.querySelectorAll("#typePills .pill").forEach(p => p.classList.remove("active"));
  btn.classList.add("active");
  activeType = btn.dataset.type;
  buildCards();
});

document.getElementById("focusPills").addEventListener("click", e => {
  const btn = e.target.closest("[data-focus]");
  if (!btn) return;
  document.querySelectorAll("#focusPills .pill").forEach(p => p.classList.remove("active"));
  btn.classList.add("active");
  activeFocus = btn.dataset.focus;
  buildCards();
});

let debounce;
document.getElementById("search").addEventListener("input", e => {
  clearTimeout(debounce);
  debounce = setTimeout(() => { searchQuery = e.target.value; buildCards(); }, 150);
});

buildCards();
</script>
</body>
</html>
