let userScore = 0;
let compScore = 0;
const rock = document.querySelector(".rock");
const paper = document.querySelector(".paper");
const scissor = document.querySelector(".scissor");
const text = document.querySelector(".text-display");
const uScore = document.querySelector(".user-score");
const cScore = document.querySelector(".comp-score");
const score_div = document.querySelector(".score");
let w = 16;
let s = 1;
var div;

function getComp() {
  const move = ["r", "p", "s"];
  var val = Math.floor(Math.random() * 3);
  return move[val];
}

rock.addEventListener("click", () => onClick("r"));
paper.addEventListener("click", () => onClick("p"));
scissor.addEventListener("click", () => onClick("s"));

function onClick(userChoice) {
  var compChoice = getComp();
  var test = userChoice + compChoice;
  var res = "";
  if (div != undefined) {
    div.style.border = `#dedede solid 0.4em`;
  }
  if (userChoice === "r") {
    div = document.querySelector(".rock");
  } else if (userChoice === "p") {
    div = document.querySelector(".paper");
  } else if (userChoice === "s") {
    div = document.querySelector(".scissor");
  }

  if (userScore.toString().length > compScore.toString().length) {
    s = userScore.toString().length;
  } else {
    s = compScore.toString().length;
  }
  switch (test) {
    case "rs":
    case "sp":
    case "pr":
      res = "w";
      userScore++;
      break;
    case "rp":
    case "ps":
    case "sr":
      res = "l";
      compScore++;
      break;
    default:
      res = "d";
      break;
  }
  if (userScore.toString().length > s || compScore.toString().length > s) {
    w += 8;
    score_div.style.width = `${w}em`;
  }
  var view = "";
  switch (res) {
    case "w":
      view = "Hey, You won to the Computer,🔥🔥🔥";
      uScore.innerHTML = `<span>${userScore}</span>`;
      div.style.border = `green 0.4em solid`;
      break;
    case "l":
      view = "Aww, You losed,💩💩💩";
      cScore.innerHTML = `<span>${compScore}</span>`;
      div.style.border = `red 0.4em solid`;
      break;
    default:
      view = "Ohh, Its a Draw,😎😎😎";
      div.style.border = `grey 0.4em solid`;
      break;
  }

  text.innerHTML = `<span>${view}</span>`;
}
