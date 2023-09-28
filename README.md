<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <link rel="shortcut icon" type="image/png" href="classpng.png">
    <meta name="viewport" content="width=device-width ,initial-scale=1.0">
    <link rel="icon" type="img/png" href="logo.png"/>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
    <script src="https://unpkg.com/css-doodle@0.15.3/css-doodle.min.js"></script>
    <title> Au Ah </title>
  </head>
  <body>
    <div>
      <css-doodle grid="5" class="doodle">
        :doodle {
            @grid: 30 / 100vmax;
        }
        background: @pick(#29B6F6, #FDD835, #5E35B1, #FFCCBC, #E8EAF6, #B2DFDB, #1B5E20, #2979FF);
        opacity: @r(0, .7);
        clip-path: circle(@r(10%, 40%));
        animation: test infinite @r(60s, 90s) linear;
        
        @keyframes test {
            0% {
            transform: translate3d(0, 0, 0);
            }
            50% {
            transform: translate3d(@r(-1000%, 1000%), @r(-1000%, 1000%), 0);
            }
            100% {
            transform: translate3d(0, 0, 0);
            }
        }
      </css-doodle>
      <div class="class_links">
        <p id="greet" ></p>
<!--         <p>No Regular Online Classes</p> -->
<!--         <h1>6th SEM</h1> -->
<!--         <table border>
          <tr>
            <td>
              <h3><a class="Active" href="https://us02web.zoom.us/j/86118334524" target="_blank">DA</a></h3>
            </td>
            <td>
              <h3><a class="Active" href="https://meet.google.com/kkt-anem-rih" target="_blank">ML</a></h3>
            </td>
            <td>
              <h3><a class="Active" href="https://meet.google.com/rnu-mxmx-qtv" target="_blank">WNS</a></h3>
            </td>
          </tr>
          <tr>
            <td>
              <h3><a class="Active" href="https://meet.google.com/xdq-vrqr-frx" target="_blank">T&T LAB</a></h3>
            </td>
            <td>
              <h3><a class="Active" href="https://kiit-ac-in.zoom.us/j/6209840220" target="_blank">CD</a></h3>
            </td>
            <td>
              <h3><a class="Active" href="http://meet.google.com/abd-qrvj-rqf" target="_blank">FPM</a></h3>
            </td>
          </tr>
         </table>
         <br/>
         <table border>
          <tr>
            <td>
              <h3>
                CC
              </h3>
            </td>
            <td>
              <h3><a class="Active" href="https://meet.google.com/bod-xwfy-wef" target="_blank">Mon</a></h3>
            </td>
            <td>
              <h3><a class="Active" href="https://meet.google.com/psh-hifq-vup" target="_blank">Tue Theory</a></h3>
            </td>
            <td>
              <h3><a class="Active" href="https://meet.google.com/hsd-yxcj-wfv" target="_blank">Tue Lab</a></h3>
            </td>
            <td>
              <h3><a class="Active" href="https://meet.google.com/uhv-tkqt-zjd" target="_blank">Lab Evaluation</a></h3>
            </td>
            <td>
              <h3><a class="Active" href="https://meet.google.com/pqa-roxo-jii" target="_blank">Thu</a></h3>
            </td>
          </tr>
        </table>
        <br/>
        <table border>
          <tr>
            <td>
              <h3>
                HRC
              </h3>
            </td>
            <td>
              <h3><a class="Active" href="https://sites.google.com/view/h2htechtrackgroup6" target="_blank">Notice Board</a></h3>
            </td>
            <td>
              <h3><a class="Active" href="https://docs.google.com/spreadsheets/d/1hnMRpZCHCQNnY3LrVsQ16peXvjtQvztKCYZmZw9lwpw/edit#gid=0" target="_blank">Reading</a></h3>
            </td>
            <td>
              <h3><a class="Active" href="https://docs.google.com/spreadsheets/d/10-k4LP8rNMYGVyXxJekRbCiaM91LjC7o2m2vNCeET1M/edit#gid=0" target="_blank">Itinerary</a></h3>
            </td>
          </tr>
        </table> -->
      </div>
    </div>
    <script>
      const currDate = new Date();
        const hrs = currDate.getHours();
        var greet;
        if (hrs < 12 && hrs > 3)  greet = 'Good Morning Biru';
        else if (hrs >= 12 && hrs < 18) greet = 'Good Afternoon Biru';
        else if (hrs >= 18 && hrs < 24)  greet = 'Good Evening Biru';
        else greet= 'Welcome'
        document.getElementById('greet').innerHTML = greet + "!";
    </script>
    <style>
    * {
      padding: 0;
      margin: 0.5rem;
    }
    .doodle {
      position: fixed;
      z-index: -1;
      filter: blur(5px);
      -webkit-filter: blur(5px);
      background-color: white;
    }
    #greet {
      text-align: center;
      font-weight: 900;
      font-size: 30px;
      font-family: Georgia, 'Times New Roman', Times, serif;
      color: deeppink;
      background-color: white;
    }
    .class_links {
      text-align: center;
      width: 80%;
      margin: 0 10%;
    }
    .class_links h1 {
      font-size: 32px;
      font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif
    }
    table {
      overflow: scroll;
      background-color: aliceblue;
      width: 100%;
      margin: 0;
    }
    td {
      font-size: 1.2rem;
    }      
    a {
      text-decoration:none;
    }
    a:hover {
      color: blueviolet;
      text-decoration: underline;
    }
    .Active {
      color: green;
    }

    @media (max-width: 900px) {
      .class_links {
        width: 100%;
        margin: 0;
      }
      .class_links h1, #greet {
        font-size: 24px;
      }
      td {
        font-size: 1rem;
      }
    }
    </style>
  </body>
</html>
