<!-- eslint-disable no-lonely-if -->
<!-- eslint-disable eqeqeq -->
<!-- eslint-disable no-tabs -->
<template>
  <div id="main">
    <h1>TIC TAC TOE</h1>
    <p id="ins">
      Game starts by just Tap on box<br><br>First Player starts as
      <b>Player X </b>And Second Player as
      <b>Player 0</b>
    </p>
    <br><br>
    <div class="ui">
      <div class="row">
        <input
          id="b1"
          type="text"
          class="cell"
          onclick="myfunc_3(); myfunc();"
          readonly
        >
        <input
          id="b2"
          type="text"
          class="cell"
          onclick="myfunc_4(); myfunc();"
          readonly
        >
        <input
          id="b3"
          type="text"
          class="cell"
          onclick="myfunc_5(); myfunc();"
          readonly
        >
      </div>
      <div class="row">
        <input
          id="b4"
          type="text"
          class="cell"
          onclick="myfunc_6(); myfunc();"
          readonly
        >
        <input
          id="b5"
          type="text"
          class="cell"
          onclick="myfunc_7(); myfunc();"
          readonly
        >
        <input
          id="b6"
          type="text"
          class="cell"
          onclick="myfunc_8(); myfunc();"
          readonly
        >
      </div>
      <div class="row">
        <input
          id="b7"
          type="text"
          class="cell"
          onclick="myfunc_9(); myfunc();"
          readonly
        >
        <input
          id="b8"
          type="text"
          class="cell"
          onclick="myfunc_10();myfunc();"
          readonly
        >
        <input
          id="b9"
          type="text"
          class="cell"
          onclick="myfunc_11();myfunc();"
          readonly
        >
      </div>
    </div>
    <br><br><br>

    <button id="but" onclick="myfunc_2()">
      RESET
    </button>
    <br><br>
    <p id="print" />
  </div>
</template>
<script>
export default {
  data () {
    return {
      flag: 1
    }
  },
  methods: {
    myfunc () {
      // Setting DOM to all boxes or input field

      const b1 = document.getElementById('b1').value
      const b2 = document.getElementById('b2').value
      const b3 = document.getElementById('b3').value
      const b4 = document.getElementById('b4').value
      const b5 = document.getElementById('b5').value
      const b6 = document.getElementById('b6').value
      const b7 = document.getElementById('b7').value
      const b8 = document.getElementById('b8').value
      const b9 = document.getElementById('b9').value

      const b1btn = document.getElementById('b1')
      const b2btn = document.getElementById('b2')
      const b3btn = document.getElementById('b3')
      const b4btn = document.getElementById('b4')
      const b5btn = document.getElementById('b5')
      const b6btn = document.getElementById('b6')
      const b7btn = document.getElementById('b7')
      const b8btn = document.getElementById('b8')
      const b9btn = document.getElementById('b9')

      // Checking if Player X won or not and after
      // that disabled all the other fields
      if ((b1 === 'x' || b1 === 'X') && (b2 === 'x' ||
      b2 === 'X') && (b3 === 'x' || b3 === 'X')) {
        document.getElementById('print')
          .innerHTML = 'Player X won'
        b4btn.disabled = true
        b5btn.disabled = true
        b6btn.disabled = true
        b7btn.disabled = true
        b8btn.disabled = true
        b9btn.disabled = true

        b1btn.style.color = 'red'
        b2btn.style.color = 'red'
        b3btn.style.color = 'red'
      } else if ((b1 === 'x' || b1 === 'X') && (b4 === 'x' ||
      b4 === 'X') && (b7 === 'x' || b7 === 'X')) {
        document.getElementById('print')
          .innerHTML = 'Player X won'
        b2btn.disabled = true
        b3btn.disabled = true
        b5btn.disabled = true
        b6btn.disabled = true
        b8btn.disabled = true
        b9btn.disabled = true

        b1btn.style.color = 'red'
        b4btn.style.color = 'red'
        b7btn.style.color = 'red'
      } else if ((b7 === 'x' || b7 === 'X') && (b8 === 'x' ||
      b8 === 'X') && (b9 === 'x' || b9 === 'X')) {
        document.getElementById('print')
          .innerHTML = 'Player X won'

        b1btn.disabled = true
        b2btn.disabled = true
        b3btn.disabled = true
        b4btn.disabled = true
        b5btn.disabled = true
        b6btn.disabled = true

        b7btn.style.color = 'red'
        b8btn.style.color = 'red'
        b9btn.style.color = 'red'
      } else if ((b3 === 'x' || b3 === 'X') && (b6 === 'x' ||
      b6 === 'X') && (b9 === 'x' || b9 === 'X')) {
        document.getElementById('print')
          .innerHTML = 'Player X won'

        b1btn.disabled = true
        b2btn.disabled = true
        b4btn.disabled = true
        b5btn.disabled = true
        b7btn.disabled = true
        b8btn.disabled = true

        b3btn.style.color = 'red'
        b6btn.style.color = 'red'
        b9btn.style.color = 'red'
      } else if ((b1 === 'x' || b1 === 'X') && (b5 === 'x' ||
      b5 === 'X') && (b9 === 'x' || b9 === 'X')) {
        document.getElementById('print')
          .innerHTML = 'Player X won'
        b2btn.disabled = true
        b3btn.disabled = true
        b4btn.disabled = true
        b6btn.disabled = true
        b7btn.disabled = true
        b8btn.disabled = true

        b1btn.style.color = 'red'
        b5btn.style.color = 'red'
        b9btn.style.color = 'red'
      } else if ((b3 === 'x' || b3 === 'X') && (b5 === 'x' ||
      b5 === 'X') && (b7 === 'x' || b7 === 'X')) {
        document.getElementById('print')
          .innerHTML = 'Player X won'
        b1btn.disabled = true
        b2btn.disabled = true
        b4btn.disabled = true
        b6btn.disabled = true
        b8btn.disabled = true
        b9btn.disabled = true

        b3btn.style.color = 'red'
        b5btn.style.color = 'red'
        b7btn.style.color = 'red'
      } else if ((b2 === 'x' || b2 === 'X') && (b5 === 'x' ||
      b5 === 'X') && (b8 === 'x' || b8 === 'X')) {
        document.getElementById('print')
          .innerHTML = 'Player X won'
        b1btn.disabled = true
        b2btn.disabled = true
        b4btn.disabled = true
        b6btn.disabled = true
        b7btn.disabled = true
        b9btn.disabled = true

        b2btn.style.color = 'red'
        b5btn.style.color = 'red'
        b8btn.style.color = 'red'
      } else if ((b4 === 'x' || b4 === 'X') && (b5 === 'x' ||
      b5 === 'X') && (b6 === 'x' || b6 === 'X')) {
        document.getElementById('print')
          .innerHTML = 'Player X won'
        b1btn.disabled = true
        b2btn.disabled = true
        b3btn.disabled = true
        b7btn.disabled = true
        b8btn.disabled = true
        b9btn.disabled = true

        b4btn.style.color = 'red'
        b5btn.style.color = 'red'
        b6btn.style.color = 'red'
      // eslint-disable-next-line brace-style
      }

      // Checking of Player X finish
      // Checking for Player 0 starts, Is player 0 won or
      // not and after that disabled all the other fields
      else if ((b1 === '0' || b1 === '0') && (b2 === '0' ||
      b2 === '0') && (b3 === '0' || b3 === '0')) {
        document.getElementById('print')
          .innerHTML = 'Player 0 won'
        b4btn.disabled = true
        b5btn.disabled = true
        b6btn.disabled = true
        b7btn.disabled = true
        b8btn.disabled = true
        b9btn.disabled = true

        b1btn.style.color = 'red'
        b2btn.style.color = 'red'
        b3btn.style.color = 'red'
      } else if ((b1 === '0' || b1 === '0') && (b4 === '0' ||
      b4 === '0') && (b7 === '0' || b7 === '0')) {
        document.getElementById('print')
          .innerHTML = 'Player 0 won'
        b2btn.disabled = true
        b3btn.disabled = true
        b5btn.disabled = true
        b6btn.disabled = true
        b8btn.disabled = true
        b9btn.disabled = true

        b1btn.style.color = 'red'
        b4btn.style.color = 'red'
        b7btn.style.color = 'red'
      } else if ((b7 === '0' || b7 === '0') && (b8 === '0' ||
      b8 === '0') && (b9 === '0' || b9 === '0')) {
        document.getElementById('print')
          .innerHTML = 'Player 0 won'
        b1btn.disabled = true
        b2btn.disabled = true
        b3btn.disabled = true
        b4btn.disabled = true
        b5btn.disabled = true
        b6btn.disabled = true

        b7btn.style.color = 'red'
        b8btn.style.color = 'red'
        b9btn.style.color = 'red'
      } else if ((b3 === '0' || b3 === '0') && (b6 === '0' ||
      b6 === '0') && (b9 === '0' || b9 === '0')) {
        document.getElementById('print')
          .innerHTML = 'Player 0 won'
        b1btn.disabled = true
        b2btn.disabled = true
        b4btn.disabled = true
        b5btn.disabled = true
        b7btn.disabled = true
        b8btn.disabled = true
        b3btn.style.color = 'red'
        b6btn.style.color = 'red'
        b9btn.style.color = 'red'
      } else if ((b1 === '0' || b1 === '0') && (b5 === '0' ||
      b5 === '0') && (b9 === '0' || b9 === '0')) {
        document.getElementById('print')
          .innerHTML = 'Player 0 won'
        b2btn.disabled = true
        b3btn.disabled = true
        b4btn.disabled = true
        b6btn.disabled = true
        b7btn.disabled = true
        b8btn.disabled = true

        b1btn.style.color = 'red'
        b5btn.style.color = 'red'
        b9btn.style.color = 'red'
      } else if ((b3 === '0' || b3 === '0') && (b5 === '0' ||
      b5 === '0') && (b7 === '0' || b7 === '0')) {
        document.getElementById('print')
          .innerHTML = 'Player 0 won'
        b1btn.disabled = true
        b2btn.disabled = true
        b4btn.disabled = true
        b6btn.disabled = true
        b8btn.disabled = true
        b9btn.disabled = true

        b3btn.style.color = 'red'
        b5btn.style.color = 'red'
        b7btn.style.color = 'red'
      } else if ((b2 === '0' || b2 === '0') && (b5 === '0' ||
      b5 === '0') && (b8 === '0' || b8 === '0')) {
        document.getElementById('print')
          .innerHTML = 'Player 0 won'
        b1btn.disabled = true
        b3btn.disabled = true
        b4btn.disabled = true
        b6btn.disabled = true
        b7btn.disabled = true
        b9btn.disabled = true

        b2btn.style.color = 'red'
        b5btn.style.color = 'red'
        b8btn.style.color = 'red'
      } else if ((b4 === '0' || b4 === '0') && (b5 === '0' ||
      b5 === '0') && (b6 === '0' || b6 === '0')) {
        document.getElementById('print')
          .innerHTML = 'Player 0 won'
        b1btn.disabled = true
        b2btn.disabled = true
        b3btn.disabled = true
        b7btn.disabled = true
        b8btn.disabled = true
        b9btn.disabled = true

        b4btn.style.color = 'red'
        b5btn.style.color = 'red'
        b6btn.style.color = 'red'
      // eslint-disable-next-line brace-style
      }

      // Checking of Player 0 finish
      // Here, Checking about Tie
      else if ((b1 === 'X' || b1 === '0') && (b2 === 'X' ||
      b2 === '0') && (b3 === 'X' || b3 === '0') &&
      (b4 === 'X' || b4 === '0') && (b5 === 'X' ||
          b5 === '0') && (b6 === 'X' || b6 === '0') &&
      (b7 === 'X' || b7 === '0') && (b8 === 'X' ||
          b8 === '0') && (b9 === 'X' || b9 === '0')) {
        document.getElementById('print')
          .innerHTML = 'Match Tie'
      } else {
        // Here, Printing Result
        // eslint-disable-next-line no-lonely-if
        if (this.flag === 1) {
          document.getElementById('print')
            .innerHTML = 'Player X Turn'
        } else {
          document.getElementById('print')
            .innerHTML = 'Player 0 Turn'
        }
      }
    },

    // to reset game
    // myfunc_2 () {
    //   location.reload()
    //   b1 = b2 = b3 = b4 = b5 = b6 = b7 = b8 = b9 = ''
    // },

    // Here onwards,  check turn of the player
    // and put accordingly value X or 0

    myfunc_3 () {
      if (this.flag === 1) {
        document.getElementById('b1').value = 'X'
        document.getElementById('b1').disabled = true
        this.flag = 0
      } else {
        document.getElementById('b1').value = '0'
        document.getElementById('b1').disabled = true
        this.flag = 1
      }
    },

    myfunc_4 () {
      if (this.flag === 1) {
        document.getElementById('b2').value = 'X'
        document.getElementById('b2').disabled = true
        this.flag = 0
      } else {
        document.getElementById('b2').value = '0'
        document.getElementById('b2').disabled = true
        this.flag = 1
      }
    },

    myfunc_5 () {
      if (this.flag === 1) {
        document.getElementById('b3').value = 'X'
        document.getElementById('b3').disabled = true
        this.flag = 0
      } else {
        document.getElementById('b3').value = '0'
        document.getElementById('b3').disabled = true
        this.flag = 1
      }
    },

    myfunc_6 () {
      if (this.flag === 1) {
        document.getElementById('b4').value = 'X'
        document.getElementById('b4').disabled = true
        this.flag = 0
      } else {
        document.getElementById('b4').value = '0'
        document.getElementById('b4').disabled = true
        this.flag = 1
      }
    },

    myfunc_7 () {
      if (this.flag === 1) {
        document.getElementById('b5').value = 'X'
        document.getElementById('b5').disabled = true
        this.flag = 0
      } else {
        document.getElementById('b5').value = '0'
        document.getElementById('b5').disabled = true
        this.flag = 1
      }
    },

    myfunc_8 () {
      if (this.flag === 1) {
        document.getElementById('b6').value = 'X'
        document.getElementById('b6').disabled = true
        this.flag = 0
      } else {
        document.getElementById('b6').value = '0'
        document.getElementById('b6').disabled = true
        this.flag = 1
      }
    },

    myfunc_9 () {
      if (this.flag === 1) {
        document.getElementById('b7').value = 'X'
        document.getElementById('b7').disabled = true
        this.flag = 0
      } else {
        document.getElementById('b7').value = '0'
        document.getElementById('b7').disabled = true
        this.flag = 1
      }
    },

    myfunc_10 () {
      if (this.flag === 1) {
        document.getElementById('b8').value = 'X'
        document.getElementById('b8').disabled = true
        this.flag = 0
      } else {
        document.getElementById('b8').value = '0'
        document.getElementById('b8').disabled = true
        this.flag = 1
      }
    },

    myfunc_11 () {
      if (this.flag === 1) {
        document.getElementById('b9').value = 'X'
        document.getElementById('b9').disabled = true
        this.flag = 0
      } else {
        document.getElementById('b9').value = '0'
        document.getElementById('b9').disabled = true
        this.flag = 1
      }
    }
  }
}
</script>
<style>
h1 {
  color: orangered;
  margin-bottom: -5px;
}
p {
  margin-bottom: -10px;
}
.ui {
  display: flex;
  flex-direction: column;
  align-items: center;
}
.row {
  display: flex;
}
.cell {
  border: none;
  width: 80px;
  height: 80px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 24px;
  text-align: center;
  cursor: pointer;
}
.cell:active {
  outline: none;
}
/* 3*3 Grid */
#b1 {
  border-bottom: 1px solid gray;
  border-right: 1px solid gray;
}

#b2 {
  border-bottom: 1px solid gray;
  border-right: 1px solid gray;
  border-left: 1px solid gray;
}

#b3 {
  border-bottom: 1px solid gray;
  border-left: 1px solid gray;
}

#b4 {
  border-top: 1px solid gray;
  border-bottom: 1px solid gray;
  border-right: 1px solid gray;
}

#b5 {
  border: 1px solid gray;
}

#b6 {
  border-top: 1px solid gray;
  border-bottom: 1px solid gray;
  border-left: 1px solid gray;
}

#b7 {
  border-top: 1px solid gray;
  border-right: 1px solid gray;
}

#b8 {
  border-top: 1px solid gray;
  border-right: 1px solid gray;
  border-left: 1px solid gray;
}

#b9 {
  border-top: 1px solid gray;
  border-left: 1px solid gray;
}
/* Reset Button */
#but {
  box-sizing: border-box;
  width: 95px;
  height: 40px;
  border: 1px solid dodgerblue;
  margin-left: auto;
  border-radius: 8px;
  font-family: Verdana, Geneva, Tahoma, sans-serif;

  background-color: whitesmoke;
  color: dodgerblue;
  font-size: 20px;
  cursor: pointer;
}

/* Player turn space */
#print {
  font-family: Verdana, Geneva, Tahoma, sans-serif;
  color: dodgerblue;
  font-size: 20px;
}

/* Main Container */
#main {
  text-align: center;
}

/* Game Instruction Text */
#ins {
  font-family: Verdana, Geneva, Tahoma, sans-serif;
  color: dodgerblue;
}
</style>
