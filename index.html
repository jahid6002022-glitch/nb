<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>Mess Marketing Tracker</title>
<style>
  body { font-family: Arial, sans-serif; background: #f4f6f9; margin: 0; padding: 0; }
  header { background: #2c3e50; color: #fff; padding: 14px; text-align: center; }
  .container { width: 92%; margin: 18px auto; }
  .card { background:#fff; padding:18px; margin:18px auto; border-radius:8px; max-width:420px; box-shadow:0 2px 6px rgba(0,0,0,0.12); }
  .hidden { display:none; }
  input, select, button { width:100%; padding:10px; margin:8px 0; border-radius:6px; border:1px solid #ccc; box-sizing:border-box; }
  button { background:#2980b9; color:#fff; border:none; cursor:pointer; }
  button:hover { background:#1f6391; }
  .link { color:#2980b9; cursor:pointer; display:block; margin-top:8px; text-align:center; }
  .small { width:auto; display:inline-block; padding:6px 10px; font-size:13px; border-radius:6px; }
  table { width:100%; border-collapse:collapse; margin-top:10px; background:#fff; box-shadow:0 1px 4px rgba(0,0,0,0.06); }
  th, td { border:1px solid #e6e6e6; padding:8px; text-align:center; font-size:14px; }
  th { background:#34495e; color:#fff; }
  .total-box { margin: 14px 0; padding: 12px; background: #27ae60; color: #fff; font-size:16px; border-radius:6px; text-align:center; }
  .floating-btn {
    position: fixed; bottom: 20px; right: 20px; background: #2980b9; color: #fff; border: none;
    padding: 14px; border-radius: 50%; font-size: 22px; cursor: pointer; box-shadow: 0 6px 18px rgba(0,0,0,0.25);
    z-index: 9999;
  }
  .form-popup {
    display:none; position:fixed; bottom:86px; right:20px; z-index:9998;
    background:#fff; padding:14px; border-radius:8px; width:92%; max-width:420px; box-shadow:0 6px 20px rgba(0,0,0,0.18);
  }
  .item-row { display:flex; gap:8px; align-items:center; margin-bottom:8px; }
  .item-row input[type="text"]{ flex:1; }
  .item-row input[type="number"]{ width:110px; }
  .muted { color:#666; font-size:13px; }
</style>
</head>
<body>
<header><h2>Mess Marketing Tracker</h2></header>

<!-- LOGIN -->
<section id="loginPage" class="card">
  <h3>Login</h3>
  <div style="display:flex;gap:12px;margin-bottom:8px;">
    <label><input name="loginType" type="radio" value="user" checked> User</label>
    <label><input name="loginType" type="radio" value="admin"> Admin</label>
  </div>
  <input id="loginUser" placeholder="Mobile No (User) or admin">
  <input id="loginPass" type="password" placeholder="Password">
  <button onclick="login()">Login</button>
  <div style="display:flex;gap:8px;margin-top:8px;">
    <a class="link" onclick="showPage('signupPage')">Sign up</a>
    <a class="link" style="margin-left:auto;" onclick="showPage('forgotPage')">Forgot password?</a>
  </div>
</section>

<!-- SIGNUP -->
<section id="signupPage" class="card hidden">
  <h3>Sign up</h3>
  <input id="signupName" placeholder="Full Name">
  <input id="signupUser" placeholder="Mobile No (10 digits)">
  <label class="muted">Date of Birth</label>
  <input id="signupDob" type="date">
  <input id="signupPass" type="password" placeholder="Password">
  <button onclick="signup()">Create account</button>
  <a class="link" onclick="showPage('loginPage')">Have account? Login</a>
</section>

<!-- FORGOT -->
<section id="forgotPage" class="card hidden">
  <h3>Recover password</h3>
  <input id="forgotUser" placeholder="Mobile No">
  <label class="muted">Date of Birth</label>
  <input id="forgotDob" type="date">
  <button onclick="recoverPassword()">Show password</button>
  <a class="link" onclick="showPage('loginPage')">Back to login</a>
</section>

<!-- ADMIN -->
<section id="adminPage" class="container hidden">
  <div style="display:flex;
  justify-content:space-between;
  align-items:center;">
    <h3>Admin — User management</h3>
    <div><button onclick="logout()">Logout</button></div>
  </div>

  <table id="approvalTable">
    <thead><tr><th>Name</th><th>Mobile</th><th>DOB</th><th>Status</th><th>Action</th></tr></thead>
    <tbody><tr><td colspan="5">No users</td></tr></tbody>
  </table>
</section>

<!-- HOME -->
<section id="homePage" class="container hidden">
  <div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:8px;">
    <div>
      <label for="monthSelect"><b>Select month</b></label>
      <select id="monthSelect" onchange="renderData()"></select>
    </div>
    <div><button onclick="logout()">Logout</button></div>
  </div>

  <div class="total-box" id="totalSpending">Total Spending: ₹0</div>

  <h4>Marketing Records</h4>
  <table id="recordsTable">
    <thead>
        <tr>
            <th>Date</th>
            <th>Marketer</th>
            <th>Total (₹)</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td colspan="3">No data available</td>
        </tr>
    </tbody>
  </table>

  <h4>Marketer Contributions</h4>
  <table id="contributionsTable">
    <thead>
        <tr>
            <th>Marketer</th>
            <th>Total (₹)</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td colspan="2">No data available</td>
        </tr>
    </tbody>
  </table>

  <div style="margin-top:12px;">
    <h4>Print marketing list</h4>
    <input id="printDate" type="date">
    <button style="margin-top:8px" onclick="printList()">Print list for date</button>
  </div>
</section>

<!-- Floating add button -->
<button id="addBtn" class="floating-btn hidden" onclick="toggleForm()">➕</button>

<!-- Contribution popup -->
<div id="formPopup" class="form-popup">
  <h3>Add Contribution</h3>
  <label class="muted">Date</label>
  <input id="dateInput" type="date">
  <p class="muted">Marketer: <strong id="marketerLabel"></strong></p>
  <div id="itemsContainer"></div>
  <div style="display:flex;gap:8px;margin-top:8px;">
    <button onclick="addItem()" style="flex:1">➕ Add item</button>
    <button onclick="saveContribution()" style="flex:1">Save</button>
  </div>
  <div style="margin-top:8px;text-align:right;">
    <button onclick="toggleForm()" style="background:#aaa">Cancel</button>
  </div>
</div>

<script>
let currentUser=null, currentName=null;

/* USERS */
function getUsers(){ return JSON.parse(localStorage.getItem('users')||'[]'); }
function setUsers(u){ localStorage.setItem('users',JSON.stringify(u)); }

/* GLOBAL CONTRIBUTIONS (shared) */
function getAllRecords(){ return JSON.parse(localStorage.getItem('marketingData')||'[]'); }
function setAllRecords(arr){ localStorage.setItem('marketingData',JSON.stringify(arr)); }

/* PAGE NAV */
function showPage(id){
  ['loginPage','signupPage','forgotPage','homePage','adminPage'].forEach(p=>document.getElementById(p).classList.add('hidden'));
  document.getElementById(id).classList.remove('hidden');
  document.getElementById('addBtn').classList.toggle('hidden',id!=='homePage'||!currentUser||currentUser==='admin');
  if(id==='adminPage') renderApprovals();
  if(id==='homePage') renderData();
}

/* SIGNUP/LOGIN/FORGOT */
function signup(){
  const name=document.getElementById('signupName').value.trim();
  const userid=document.getElementById('signupUser').value.trim();
  const dob=document.getElementById('signupDob').value;
  const pass=document.getElementById('signupPass').value;
  if(!name||!userid||!dob||!pass){alert('Fill all fields');return;}
  if(!/^[0-9]{10}$/.test(userid)){alert('Enter 10-digit mobile');return;}
  let users=getUsers();
  if(users.find(u=>u.userid===userid)){alert('User exists');return;}
  users.push({userid,name,dob,password:pass,approved:false});
  setUsers(users);
  alert('Signup done. Wait for admin approval.');
  showPage('loginPage');
}
function login(){
  const type=document.querySelector('input[name="loginType"]:checked').value;
  const u=document.getElementById('loginUser').value.trim();
  const p=document.getElementById('loginPass').value;
  if(type==='admin'){
    if(u==='admin1'&&p==='admin@123'){currentUser='admin';currentName='Admin';showPage('adminPage');return;}
    alert('Invalid admin');return;
  }
  let users=getUsers();
  let user=users.find(x=>x.userid===u&&x.password===p);
  if(!user){alert('Invalid credentials');return;}
  if(!user.approved){alert('Awaiting approval');return;}
  currentUser=user.userid;currentName=user.name;
  showPage('homePage');
}
function recoverPassword(){
  const u=document.getElementById('forgotUser').value.trim();
  const dob=document.getElementById('forgotDob').value;
  let users=getUsers();
  let user=users.find(x=>x.userid===u&&x.dob===dob);
  if(!user){alert('No match');return;}
  alert('Password: '+user.password);
}

/* ADMIN */
function renderApprovals(){
  let users=getUsers().filter(u=>u.userid!=='admin');
  const tb=document.querySelector('#approvalTable tbody');
  tb.innerHTML=users.length?'':'<tr><td colspan=5>No users</td></tr>';
  users.forEach(u=>{
    let status=u.approved?'Approved':'Pending';
    let act='';
    if(!u.approved) act+=`<button onclick="approveUser('${u.userid}')">Approve</button> `;
    act+=`<button onclick="deleteUser('${u.userid}')">Delete</button>`;
    tb.innerHTML+=`<tr><td>${u.name}</td><td>${u.userid}</td><td>${u.dob}</td><td>${status}</td><td>${act}</td></tr>`;
  });
}
function approveUser(id){let u=getUsers();let x=u.find(v=>v.userid===id);if(x){x.approved=true;setUsers(u);}renderApprovals();}
function deleteUser(id){let u=getUsers().filter(v=>v.userid!==id);setUsers(u);renderApprovals();}

/* CONTRIBUTIONS */
function getMonthFromDate(d){return d.slice(0,7);}
function populateMonthSelector(records){
  const sel=document.getElementById('monthSelect');
  const months=[...new Set(records.map(r=>getMonthFromDate(r.date)))];
  const now=new Date();const cur=`${now.getFullYear()}-${String(now.getMonth()+1).padStart(2,'0')}`;
  if(!months.includes(cur)) months.push(cur);
  const prev=sel.value; sel.innerHTML='';
  months.sort().reverse().forEach(m=>{let o=document.createElement('option');o.value=m;o.textContent=m;sel.appendChild(o);});
  sel.value=(prev&&months.includes(prev))?prev:cur;
}
function renderData(){
  const records=getAllRecords();
  populateMonthSelector(records);
  const m=document.getElementById('monthSelect').value;
  const monthRecs=records.filter(r=>getMonthFromDate(r.date)===m);
  const total=monthRecs.reduce((s,e)=>s+e.items.reduce((a,i)=>a+Number(i.price),0),0);
  document.getElementById('totalSpending').textContent=`Total Spending (${m}): ₹${total}`;
  const recTb=document.querySelector('#recordsTable tbody');recTb.innerHTML=monthRecs.length?'':'<tr><td colspan=3>No data</td></tr>';
  monthRecs.forEach(e=>{recTb.innerHTML+=`<tr><td>${e.date}</td><td>${e.marketer}</td><td>₹${e.items.reduce((a,i)=>a+i.price,0)}</td></tr>`;});
  const contrib={};monthRecs.forEach(e=>{let t=e.items.reduce((a,i)=>a+i.price,0);contrib[e.marketer]=(contrib[e.marketer]||0)+t;});
  const cTb=document.querySelector('#contributionsTable tbody');cTb.innerHTML=Object.keys(contrib).length?'':'<tr><td colspan=2>No data</td></tr>';
  for(let k in contrib){cTb.innerHTML+=`<tr><td>${k}</td><td>₹${contrib[k]}</td></tr>`;}
}
function toggleForm(){
  if(!currentUser||currentUser==='admin'){alert('Only users');return;}
  const f=document.getElementById('formPopup');
  if(f.style.display==='block'){f.style.display='none';return;}
  f.style.display='block';document.getElementById('itemsContainer').innerHTML='';addItem();
  const t=new Date().toISOString().split('T')[0];document.getElementById('dateInput').max=t;document.getElementById('dateInput').value=t;
  document.getElementById('marketerLabel').textContent=currentName;
}
function addItem(){
  const c=document.getElementById('itemsContainer');
  const d=document.createElement('div');d.className='item-row';
  d.innerHTML=`<input class="itemName" placeholder="Item"><input type="number" class="itemPrice" placeholder="Price"><button onclick="this.parentElement.remove()">✖</button>`;
  c.appendChild(d);
}
function saveContribution(){
  const date=document.getElementById('dateInput').value;if(!date){alert('Pick date');return;}
  const names=[...document.querySelectorAll('.itemName')].map(i=>i.value.trim());
  const prices=[...document.querySelectorAll('.itemPrice')].map(i=>parseFloat(i.value));
  if(names.length===0||names.some(n=>!n)||prices.some(p=>!Number.isFinite(p)||p<=0)){alert('Invalid');return;}
  let recs=getAllRecords();const items=names.map((n,i)=>({name:n,price:prices[i]}));
  recs.push({date,marketer:currentName,userid:currentUser,items});setAllRecords(recs);
  alert('Saved');document.getElementById('formPopup').style.display='none';renderData();
}
function printList(){
  const d=document.getElementById('printDate').value;if(!d){alert('Pick date');return;}
  const recs=getAllRecords().filter(r=>r.date===d);if(!recs.length){alert('No data');return;}
  let c='';recs.forEach(e=>{let t=e.items.reduce((a,i)=>a+i.price,0);c+=`<div style="margin:20px;font-family:Arial"><h3>Marketing List - ${e.marketer}</h3><p>Date: ${e.date}</p><hr><ol>${e.items.map(i=>`<li>${i.name} ... ₹${i.price}</li>`).join('')}</ol><hr><b>Total: ₹${t}</b></div>`;});
  const w=window.open('','_blank');w.document.write(c);w.print();
}

/* LOGOUT */
function logout(){currentUser=null;currentName=null;showPage('loginPage');}
</script>
</body>
</html>
