# ptDocGenerator
My goal is to automate repetitive documentation in a clinician friendly way. The focus is physical therapy right now and automating my documentation. 

What the project does?
  This project generates repetitive phrases used in physical therapy documentation. It has a Skilled Nursing Focus as of right now. 

Why the project is useful?
  It allows you to generate a short objective sentence you can copy and paste to your clinics EMR. 

How users can get started with the project?
  Open the project via GitHub, click the parameters you want from the prompts. 
  
Where users can get help with your project?

  mitchelldramsey@gmail.com

Who maintains and contributes to the project?

Mitchell Ramsey PTA

<!DOCTYPE html>
<html lang="en">
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PT Documentation Generator</title>
    <style>
        body { font-family: Arial, sans-serif; margin: 20px; }
        label, select, input { display: block; margin: 10px 0; }
        textarea { width: 100%; height: 100px; margin-top: 10px; }
    </style>

    <!-- <style>
        body { 
    font-family: Arial, sans-serif; 
    margin: 20px; 
    max-width: 600px;
}

textarea {
    width: 100%; 
    height: 100px; 
    margin-top: 10px;
}

button {
    background-color: #007bff;
    color: white;
    padding: 10px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}

button:hover {
    background-color: #0056b3;
}



    </style> -->
</head>
<body>
    
    <h2>Physical Therapy Documentation Generator</h2>

    <p>Welcome to my documentation generator. I wish to provide concise, consistently formatted notes to save clinicians time.</p>
    <p>To that end I will use common abbreviations, formulaic strucutre. Ex: <b>Transfer x AD x Assist + VC: Cue 1, Cue 2, etc.</b></p>
    <p>Lets face it documentation sucks. After a day of treatment, who wants to write an essay.</p>
    <p>Join me in making documentation short, predictable and repeatable. Try it out!</p>
    <h1>Instructions</h1>
    <ol>
        <li>Select Training and measures</li>
        <li>Click Generate Button at bottom of section</li>
        <li>Copy and Paste to your note</li>
    </ol>

    <form id="docForm">
        <h3>Therapeutic Activity</h3>
        <label for="transfer">Transfer Training:</label>
        <select id="transfer">
            <option value=""></option>
            <option value="STS">STS = Sit to Stand</option>
            <option value="SPT">SPT = Stand Pivot Transfer</option>
            <option value="SB transfer">SB = Slide Board</option>
            <option value="Supine to Sit">Supine to Sit</option>
            <option value="Squat Pivot">Squat Pivot</option>
            <option value="Bed to Chair">Bed to Chair</option>
        </select>

        <label for="assistiveDevice">Assistive Device:</label>
        <select id="assistiveDevice">
            <option value=""></option>
            <option value="no AD">no AD</option>
            <option value="2WW">2WW = 2 Wheeled Walker</option>
            <option value="4WW">4WW = 4 Wheeled Walker</option>
            <option value="RW PLATFM attatchment">RW PLATFM = Walker Platform Attatchment</option>
            <option value="HW">HW = Hemi Walker</option>
            <option value="SPC">SPC = Single Point Cane</option>
            <option value="SBQC">SBQC = Short Based Quad Cane</option>
            <option value="WBQC">WBQC = Wide Based Quad Cane</option>
            <option value="Crutches">Crutches</option>
            <option value="SR">SR = Side Rail</option>
            <option value="BHR">BHR = Bilateral Hand Rails</option>
            <option value="RHR">RHR = Right Hand Rail</option>
            <option value="LHR">LHR = Left Hand Rail</option>
            <option value="hoyer lift">hoyer lift</option>
            <option value="stand lift">stand lift</option>
            <option value="standing frame">standing frame</option>
            <option value="using SB">using SB</option>
        </select>

        <label for="assist">Assist Level</label>
        <select id="assist">
            <option value=""></option>
            <option value="(I)">I = Independent</option>
            <option value="MI">MI = Modified Independent</option>
            <option value="S/U">S/U = Set Up</option>
            <option value="SUP">SUP = Supervised</option>
            <option value="SBA-SUP">SBA-SUP</option>
            <option value="SBA">SBA = Stand By Assist</option>
            <option value="CGA-SBA">CGA-SBA</option>
            <option value="CGA">CGA = Contact Guard Assist</option>
            <option value="Min-CGA">Min-CGA</option>
            <option value="Min A">Min A</option>
            <option value="Mod-Min A">Min-CGA</option>
            <option value="Mod A">Mod A</option>
            <option value="Max-Mod A">Min-CGA</option>
            <option value="Max A">Max A</option>
            <option value="Max A x 2 persons">Max A x 2 persons</option>
            <option value="(TD+)">TD+ = Total Dependent Patient Assisting</option>
            <option value="TD">TD = Total Dependent</option>
        </select>

        <label for="reps">Transfer Reps:</label>
        <input type="reps" id="reps" placeholder="Enter Transfer Reps">

        <label for="cues">Cue Type?</label>
        <select id="cues">
            <option value=""></option>
            <option value="cues from therapist">no cues from therapist</option>
            <option value="VC">VC</option>
            <option value="VC / TC">VC / TC</option>
            <option value="TC">TC</option>
            <option value="HHA">HHA = Hand Held Assist</option>
            <option value="Visual Demo">Visual Demo</option>
            <option value="mirroring therapist">mirroring therapist</option>
        </select>

        <label for="percentCue">% Cues Given?</label>
        <select id="percentCue">
            <option value=""></option>
            <option value="0%">0%</option>
            <option value="25%">25%</option>
            <option value="50%">50%</option>
            <option value="75%">75%</option>
            <option value="100%">100%</option>
        </select>

        <label for="specificCue">Specific Cue?</label>
        <select id="specificCue">
            <option value=" "></option>
            <option value="no cues given">no cues</option>
            <option value="sit to stand sequence">sit to stand sequence</option>
            <option value="safe hand and foot placement">safe hand and foot placement</option>
            <option value="nose over toes">nose over toes</option>
            <option value="weight shifting">weight shifting</option>
            <option value="transfer technique">transfer technique</option>
        </select>

        <button type="button" onclick="generateDocumentation('transfer')">Generate Transfer</button>

        <button type="button" onclick="copyToClipboard('transferOutput')">Copy Transfer Text</button>

        <h4>Transfer Documentation</h4>
        <textarea id="transferOutput" readonly></textarea>

        <!-- Works! -->
        <h3>Gait Training</h3>
        
        <label for="ambDistance">Ambulation Distance (ft):</label>
        <input type="number" id="ambDistance" placeholder="Enter distance">

        <label for="ambReps">Ambulation Bouts:</label>
        <input type="number" id="ambReps" placeholder="Enter Bouts">

        <label for="ambAD">Assistive Device:</label>
        <select id="ambAD">
            <option value="no AD">no AD</option>
            <option value="2WW">2WW</option>
            <option value="4WW">4WW</option>
            <option value="RW PLATFM">RW PLATFM</option>
            <option value="HW">HW</option>
            <option value="SPC">SPC</option>
            <option value="SBQC">SBQC</option>
            <option value="WBQC">WBQC</option>
            <option value="Crutches">Crutches</option>
        </select>

        <label for="ambAssist">Assist Level</label>
        <select id="ambAssist">
            <option value="I">I = Independent</option>
            <option value="MI">MI = Modified Independent</option>
            <option value="S/U">S/U = Set Up</option>
            <option value="SUP">SUP = Supervised</option>
            <option value="SBA-SUP">SBA-SUP</option>
            <option value="SBA">SBA = Stand By Assist</option>
            <option value="CGA-SBA">CGA-SBA</option>
            <option value="CGA">CGA = Contact Guard Assist</option>
            <option value="Min-CGA">Min-CGA</option>
            <option value="Min A">Min A</option>
            <option value="Mod-Min A">Min-CGA</option>
            <option value="Mod A">Mod A</option>
            <option value="Max-Mod A">Min-CGA</option>
            <option value="Max A">Max A</option>
            <option value="Max A x 2 persons">Max A x 2 persons</option>
            <option value="(TD+)">TD+ = Total Dependent Patient Assisting</option>
            <option value="TD">TD = Total Dependent</option>
        </select>

        <label for="ambCuePercent">% Cues Given?</label>
        <select id="ambCuePercent">
            <option value=""></option>
            <option value="25%">25%</option>
            <option value="50%">50%</option>
            <option value="75%">75%</option>
            <option value="100%">100%</option>
        </select>

        <label for="ambCueType">Cue Type?</label>
        <select id="ambCueType">
            <option value=""></option>
            <option value="VC">VC</option>
            <option value="TC">TC</option>
            <option value="HHA">HHA</option>
            <option value="Visual Demo">Visual Demo</option>
            <option value="mirroring therapist">mirroring therapist</option>
            <option value="feedback using mirror">using mirror</option>
        </select>

        <label for="ambSpecificCue">Specific Cue?</label>
        <select id="ambSpecificCue">
            <option value=" "></option>
            <option value="normalized Gt pattern">normalized Gt pattern</option>
            <option value="step length c height">step length c height</option>
            <option value="upright posture">upright posture</option>
            <option value="glute and core activation">glute and core activation</option>
            <option value="proper BOS">BOS = Base of Support</option>
            <option value="proper COG">COG = Center of Gravity</option>
            <option value="scanning environment">scanning environment</option>
            <option value="2 pt gait">2 point gait</option>
            <option value="3 pt gait">3 point gait</option>
            <option value="4 pt gait">4 point gait</option>
        </select>

        <button type="button" onclick="generateDocumentation('ambulation')">Generate Ambulation</button>

        <button type="button" onclick="copyToClipboard('ambulationOutput')">Copy Ambulation Text</button>

        <h4>Ambulation Documentation</h4>
        <textarea id="ambulationOutput" readonly></textarea>

        <h4>Stairs</h4>

        <label for="strReps">Stairs Climbed:</label>
        <input type="number" id="strReps" placeholder="Enter Steps climbed">

        <label for="strHeight">Stair Height?</label>
        <select id="strHeight">
            <option value="2">2</option>
            <option value="4">4</option>
            <option value="6">6</option>
            <option value="8">8</option>
            <option value="varying height">varied</option>
        </select>

        <label for="strAD">strAD:</label>
        <select id="strAD">
            <option value="BHR">BHR</option>
            <option value="RHR">RHR</option>
            <option value="LHR">LHR</option>
            <option value="no AD">no AD</option>
            <option value="2WW">2WW</option>
            <option value="4WW">4WW</option>
            <option value="RW PLATFM">RW PLATFM</option>
            <option value="HW">HW</option>
            <option value="SPC">SPC</option>
            <option value="SBQC">SBQC</option>
            <option value="WBQC">WBQC</option>
            <option value="Crutches">Crutches</option>
            <option value="SR">SR</option>
        </select>

        <label for="strAssist">Assist Level</label>
        <select id="strAssist">
            <option value="I">I = Independent</option>
            <option value="MI">MI = Modified Independent</option>
            <option value="S/U">S/U = Set Up</option>
            <option value="SUP">SUP = Supervised</option>
            <option value="SBA-SUP">SBA-SUP</option>
            <option value="SBA">SBA = Stand By Assist</option>
            <option value="CGA-SBA">CGA-SBA</option>
            <option value="CGA">CGA = Contact Guard Assist</option>
            <option value="Min-CGA">Min-CGA</option>
            <option value="Min A">Min A</option>
            <option value="Mod-Min A">Min-CGA</option>
            <option value="Mod A">Mod A</option>
            <option value="Max-Mod A">Min-CGA</option>
            <option value="Max A">Max A</option>
            <option value="Max A x 2 persons">Max A x 2 persons</option>
            <option value="(TD+)">TD+ = Total Dependent Patient Assisting</option>
            <option value="TD">TD = Total Dependent</option>
        </select>

        <label for="strCuePercent">% Cues Given?</label>
        <select id="strCuePercent">
            <option value=""></option>
            <option value="25%">25%</option>
            <option value="50%">50%</option>
            <option value="75%">75%</option>
            <option value="100%">100%</option>
        </select>

        <label for="strCueType">Cue Type?</label>
        <select id="strCueType">
            <option value=""></option>
            <option value="VC">VC</option>
            <option value="TC">TC</option>
            <option value="HHA">HHA</option>
            <option value="Visual Demo">Visual Demo</option>
            <option value="mirroring therapist">mirroring therapist</option>
        </select>

        <label for="strSpecificCue">Specific Cue?</label>
        <select id="strSpecificCue">
            <option value=" "></option>
            <option value="step-to pattern">step too pattern</option>
            <option value="reciprocal pattern">reciprocal pattern</option>
            <option value="good up bad down">good up bad down</option>
            <option value="eccentric control">eccentric control</option>
        </select>

         <!-- <button type="button" onclick="strText()">Generate Stairs</button> -->
         <button type="button" onclick="generateDocumentation('stairs')">Generate Stairs</button>

         <button type="button" onclick="copyToClipboard('stairOutput')">Copy Stairs Text</button>
 
     <textarea id="stairOutput" readonly></textarea>
        

     <!-- Exercise -->

     <h4>Therapeutic Exercise</h4>

     <p>For best results</p>
     <ol>
        <li>Use the word "sets" after entering number of sets. Ex: "2 sets"</li>
        <li>Use the word "reps" after entering number of rets. Ex: "2 reps"</li>
        <li>Use the unit of time" after entering amount of time. Ex: "2 min"</li>
     </ol>

        <label for="exSelection">Exercise Performed?</label>
        <select id="exSelection">
            <option value=""></option>
            <option value="Ankle PF">Ankle PF</option>
            <option value="Ankle DF">Ankle DF</option>
            <option value="Ankle ER">Ankle ER</option>
            <option value="Ankle IR">Ankle IR</option>
            <option value="Knee Extension">Knee Extension</option>
            <option value="Knee Flexion">Knee Flexion</option>
            <option value="Hip Flexion">Hip Flexion</option>
            <option value="Hip Extension">Hip Extension</option>
            <option value="Hip Abduction">Hip Abduction</option>
            <option value="Hip Adduction">Hip Adduction</option>
            <option value="Glute Squeeze">Glute Squeeze</option>
            <option value="LE Ergometer">BLE Ergometer</option>
            <option value="UE Ergometer">UE Ergometer</option>
            <option value="Trunk Flexion">Trunk Flexion</option>
            <option value="Trunk Extension">Trunk Extension</option>
            <option value="Trunk Lateral Flexion">Trunk Lateral Flexion</option>
            <option value="Trunk Rotation">Trunk Rotation</option>
            <option value="Shoulder Flexion">Shoulder Flexion</option>
            <option value="Shoulder Extension">Shoulder Extension</option>
            <option value="Shoulder Abduction">Shoulder Abduction</option>
            <option value="Shoulder ER">Shoulder ER</option>
            <option value="Shoulder IR">Shoulder IR</option>
            <option value="Elbow Flexion">Elbow Flexion</option>
            <option value="Elbow Extension">Elbow Extension</option>
            <option value="Wrist Flexion">Wrist Flexion</option>
            <option value="Wrist Extension">Wrist Extension</option>
            <option value="Wrist Radial Deviation">Wrist Radial Deviation</option>
            <option value="Wrist Ulnar Deviation">Wrist Ulnar Deviation</option>
        </select>

        <label for="exPosition">Exercise Position?</label>
        <select id="exPosition">
            <option value=""></option>
            <option value="in supine">supine</option>
            <option value="in side lying">side lying</option>
            <option value="in hook lying">hook lying</option>
            <option value="in prone">prone</option>
            <option value="in short sit">short sit</option>
            <option value="in long sit">long sit</option>
            <option value="in standing">standing</option>
            <option value="in quadraped">quadraped</option>
            <option value="on NuStep">NuStep</option>
            <option value="shoulder 90 elbow 90">shoulder 90 elbow 90</option>

        </select>

        <label for="exAssist">Exercise Performance Level</label>
        <select id="exAssist">
            <option value=""></option>
            <option value="PROM">PROM</option>
            <option value="AAROM">AAROM</option>
            <option value="AROM">AROM</option>
        </select>

        <label for="exResistance">Exercise Resistance</label>
        <select id="exResistance">
            <option value=""></option>
            <option value="2# AW">2 lb AW = Ankle Weight</option>
            <option value="3# AW">3# AW</option>
            <option value="4# AW">4# AW</option>
            <option value="5# AW">5# AW</option>
            <option value="6# AW">6# AW</option>
            <option value="7# AW">7# AW</option>
            <option value="8# AW">8# AW</option>
            <option value="9# AW">9# AW</option>
            <option value="10# AW">10# AW</option>
            <option value="Yellow TB">YTB = Yellow Theraband</option>
            <option value="Red TB">Red TB</option>
            <option value="Blue TB">Blue TB</option>
            <option value="Black TB">Black TB</option>
            <option value="Ergometer L1">Ergometer L1</option>
            <option value="Ergometer L2">Ergometer L2</option>
            <option value="Ergometer L3">Ergometer L3</option>
            <option value="Ergometer L4">Ergometer L4</option>
            <option value="Ergometer L5">Ergometer L5</option>
            <option value="Ergometer L6">Ergometer L6</option>
            <option value="Ergometer L7">Ergometer L7</option>
            <option value="Ergometer L8">Ergometer L8</option>
            <option value="Ergometer L9">Ergometer L9</option>
            <option value="Ergometer L10">Ergometer L10</option>
        </select>

        <label for="exSets">Exercise Sets:</label>
        <input type="exSets" id="exSets" placeholder="Enter Number of Sets">

        <label for="exReps">Exercise Reps:</label>
        <input type="exReps" id="exReps" placeholder="Enter Number of Reps">

        <label for="exTime">Exercise Time:</label>
        <input type="exTime" id="exTime" placeholder="Enter Time">

        <label for="exCueType">Cue Type?</label>
        <select id="exCueType">
            <option value=""></option>
            <option value="VC">VC</option>
            <option value="TC">TC</option>
            <option value="HHA">HHA</option>
            <option value="Visual Demo">Visual Demo</option>
            <option value="mirroring therapist">mirroring therapist</option>
        </select>

        <label for="exSpecificCue"> Exercise Specific Cue?</label>
        <select id="exSpecificCue">
            <option value=" "></option>
            <option value="tempo and technique">tempo and technique</option>
            <option value="eliminate subsitutions">eliminate subsitutions</option>
            <option value="proper muscle engagement">proper muscle engagement</option>
        </select>

         <!-- <button type="button" onclick="strText()">Generate Stairs</button> -->
         <button type="button" onclick="generateDocumentation('exercise')">Generate Exercise</button>

         <button type="button" onclick="copyToClipboard('exerciseOutput')">Copy Exercise Text</button>
 
     <textarea id="exerciseOutput" readonly></textarea>

     <h3>Group</h3>
        
     <label for="grpType">Group Type:</label>
     <select id="grpType">
         <option value=""></option>
         <option value="Therapeutic Exercise">Therapeutic Exercise</option>
         <option value="Therapeutic Activity">Therapeutic Activity</option>
         <option value="Gait">Gait</option>
         <option value="Education">Education</option>
         <option value="Balance">Balance</option>
         <option value="Wheelchair Mobility">Wheelchair Mobility</option>
         <option value="Transfer">Transfer</option>
         <option value="Safety Awareness">Safety Awareness</option>
     </select>
     
        <label for="grpNum">Participants in group:</label>
        <input type="grpNum" id="grpNum" placeholder="Enter number of participants">

        <label for="grpParameter">Goal of Group:</label>
     <select id="grpParameter">
         <option value=""></option>
         <option value="transfer technique">transfer</option>
         <option value="gait technique">gait</option>
         <option value="AD technique">assistive device</option>
         <option value="safety awareness">safety awareness</option>
         <option value="balance during mobility">balance</option>
         <option value="wheelchair Mobility">Wheelchair Mobility</option>
         <option value="transfer">Transfer</option>
         <option value="safety Awareness">Safety Awareness</option>
         <option value="social involvement">Social Involvement</option>
         <option value="strength c ROM">strength c ROM</option>
         <option value="functional activity tolerance">functional activity tolerance</option>

     </select>


        <label for="grpParticipation">Level of participation?</label>
        <select id="grpParticipation">
            <option value="poor">Poor</option>
            <option value="fair">Fair</option>
            <option value="good">Good</option>
            <option value="excellent">Excellent</option>
        </select>

        <button type="button" onclick="generateDocumentation('group')">Generate Group</button>

        <button type="button" onclick="copyToClipboard('groupOutput')">Copy Group Text</button>

        <h4>Group Documentation</h4>
        <textarea id="groupOutput" readonly></textarea>

    </form>
    
    <script>

        function generateDocumentation(type) {
    let fields = {
        transfer: ['transfer', 'assistiveDevice', 'assist', 'reps', 'percentCue', 'cues', 'specificCue'],
        ambulation: ['ambDistance', 'ambReps', 'ambAD', 'ambAssist', 'ambCuePercent', 'ambCueType', 'ambSpecificCue'],
        stairs: ['strReps', 'strHeight', 'strAD', 'strAssist', 'strCuePercent', 'strCueType', 'strSpecificCue'],
        exercise: ['exSelection', 'exPosition', 'exAssist', 'exResistance', 'exSets', 'exReps', 'exTime', 'exCueType', 'exSpecificCue'],
        group: ['grpType', 'grpNum', 'grpParameter', 'grpParticipation'],
    };

    let outputIds = {
        transfer: 'transferOutput',
        ambulation: 'ambulationOutput',
        stairs: 'stairOutput',
        exercise: 'exerciseOutput',
        group: 'groupOutput',
    };

    let values = fields[type].map(id => document.getElementById(id).value);
    
    let templates = {
        transfer: `Pt performed ${values[0]} ${values[1]} ${values[2]} ${values[3]} reps + ${values[4]} ${values[5]}: ${values[6]}.`,
        ambulation: `Pt performed ${values[0]}'x${values[1]} bouts ${values[2]} ${values[3]} + ${values[4]} ${values[5]}: ${values[6]}.`,
        stairs: `Pt performed ${values[0]} steps at ${values[1]}" height ${values[2]} ${values[3]} + ${values[4]} ${values[5]}: ${values[6]}.`,
        exercise: `Pt performed ${values[0]} ${values[1]} ${values[2]} ${values[3]} ${values[4]} x ${values[5]} ${values[6]}: ${values[7]} for ${values[8]}`,
        group: `Pt participated in ${values[0]} group with ${values[1]} participants, to improve ${values[2]}. Pt demo's ${values[3]} participation in this session.`,
    };

    document.getElementById(outputIds[type]).value = templates[type];
}


function copyToClipboard(elementId) {
    let textArea = document.getElementById(elementId);
    textArea.select();
    document.execCommand('copy');
    alert('Copied to clipboard!');
}

    </script>
</body>
</html>
