# stylePanel.css
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@400;600&display=swap');

body {
margin: 0;
background: #1a1a1a;
height: 100vh;
display: flex;
flex-direction: column;
justify-content: center;
align-items: center;
color: #fff;
overflow: hidden;
font-family: 'Open Sans', sans-serif;
}

#particles-js {
position: absolute;
width: 100%;
height: 100%;
top: 0;
left: 0;
z-index: -1;
}

.header {
text-align: center;
margin: 20px 0;
z-index: 1;
}

.header h1 {
font-size: 2.5rem;
background: linear-gradient(90deg, #ff7eb3, #65b2ff);
-webkit-background-clip: text;
color: transparent;
text-transform: uppercase;
letter-spacing: 5px;
text-shadow: 0 0 15px rgba(255, 255, 255, 0.8);
transition: 0.3s ease-in-out;
}

.header h1:hover {
letter-spacing: 8px;
text-shadow: 0 0 30px rgba(255, 255, 255, 1);
}

.header h2 {
font-size: 1.5rem;
color: #ccc;
margin: 5px 0;
letter-spacing: 2px;
}

.container {
background: rgba(20, 20, 20, 0.8);
padding: 25px 20px;
border-radius: 15px;
box-shadow: 0 0 40px rgba(0, 0, 0, 0.8);
width: 400px;
z-index: 1;
}


.toggle-item {
display: flex;
justify-content: space-between;
align-items: center;
padding: 15px;
margin: 10px 0;
border-radius: 15px;
box-shadow: 0 0 15px rgba(255, 255, 255, 0.1);
width: 100%;
box-sizing: border-box;
background-color: #333;
}

.toggle-item:hover {
}

.toggle-item span {
font-size: 1.1em;
display: flex;
align-items: center;
}

.toggle-item img {
width: 24px;
margin-right: 10px;
}

.toggle-switch {
position: relative;
width: 50px;
height: 28px;
flex-shrink: 0;
margin-left: 10px;
}

.toggle-switch input {
opacity: 0;
position: absolute;
width: 100%;
height: 100%;
cursor: pointer;
}

.slider {
position: absolute;
top: 0;
left: 0;
right: 0;
bottom: 0;
background: linear-gradient(90deg, #2196F3, #e91e63);
transition: .4s;
border-radius: 20px;
}

.slider:before {
content: "";
position: absolute;
background-color: white;
border-radius: 50%;
transition: transform 0.3s;
height: 14px;
width: 14px;
left: 3px;
bottom: 3px;
}

input:checked + .slider {
background: linear-gradient(90deg, #e91e63, #2196F3);
}

input:checked + .slider:before {
transform: translateX(20px);
}

.button-container {
position: absolute;
bottom: 30px;
left: 50%;
transform: translateX(-50%);
z-index: 1;
text-align: center;
margin-top: 30px;
}

.button-container button {
background: linear-gradient(90deg, #ff7eb3, #65b2ff);
border: none;
padding: 12px 40px;
font-size: 1.2em;
font-weight: 600;
color: #fff;
border-radius: 50px;
cursor: pointer;
box-shadow: 0 0 20px rgba(255, 255, 255, 0.3);
transition: all 0.3s ease;
}

.button-container button:hover {
transform: scale(1.1);
box-shadow: 0 0 30px rgba(255, 255, 255, 0.5);
}

.copyright {
margin-top: 20px;
font-size: 0.9em;
color: #aaa;
}

@media (max-width: 768px) {
.container { width: 80%; }
.toggle-item { margin-bottom: 10px; }
.button-container { margin-top: 15px; }
}

.loader {
border: 6px solid #f3f3f3;
border-top: 6px solid #3498db;
border-radius: 50%;
width: 30px;
height: 30px;
animation: spin 1s linear infinite;
display: none;
position: absolute;
top: 50%;
left: 50%;
transform: translate(-50%, -50%);
}

@keyframes spin {
0% { transform: rotate(0deg); }
100% { transform: rotate(360deg); }
}

.modalUpdate {
display: flex;
justify-content: center;
align-items: center;
position: fixed;
z-index: 1000;
left: 0;
top: 0;
width: 100%;
height: 100%;
background-color: rgba(0, 0, 0, 0.7);
}

.modalUpdate .modal-content {
background: linear-gradient(135deg, #121212, #1f1f1f);
border-radius: 25px;
padding: 30px;
box-shadow: 0 8px 30px rgba(0, 0, 0, 0.5);
width: 85%;
max-width: 450px;
text-align: center;
animation: fadeIn 0.3s ease;
}

.modalUpdate .modal-content h2 {
margin: 0 0 20px;
color: #007bff
}

.modalUpdate .modal-content p {
margin: 0 0 25px;
line-height: 1.7;
}

.modalUpdate button {
background: linear-gradient(90deg, #e91e63, #65b2ff);
color: white;
border: none;
border-radius: 50px;
padding: 15px 40px;
font-size: 18px;
cursor: pointer;
transition: background-color 0.3s ease;
}

.modalUpdate button:hover {
background-color: #e91e63;
}

@keyframes fadeIn {
from { opacity: 0; }
to { opacity: 1; }
}

@keyframes fadeOut {
from { opacity: 1; }
to { opacity: 0; }
}
#splashScreen {
position: fixed;
top: 0;
left: 0;
width: 100%;
height: 100%;
background-color: #000;
display: flex;
justify-content: center;
align-items: center;
z-index: 1000;
opacity: 1;
visibility: visible;
animation: splashFadeOut 1.5s ease-out 1.5s forwards;
}

#splashScreen img {
max-width: 80%;
max-height: 80%;
transform: scale(1);
animation: splashZoom 1.5s ease-out forwards;
}

@keyframes splashFadeOut {
to {
opacity: 0;
visibility: hidden;
}
}

@keyframes splashZoom {
from {
transform: scale(1);
}
to {
transform: scale(1.2);
}
    }
