<svg
  fill="none"
  viewBox="0 0 800 400"
  width="800"
  height="400"
  xmlns="http://www.w3.org/2000/svg"
>
  <foreignObject width="100%" height="100%">
    <div xmlns="http://www.w3.org/1999/xhtml">
      <style>
        .duck {
          display: flex;
          flex-direction: column;
          position: relative;
        }
        .duck__wrapper {
          display: grid;
          place-content: center;
        }
        
        .duck__head {
          align-self: flex-end;
          width: 6rem;
          height: 4rem;
          border-radius: 8rem 8rem 0 0;
          background-color: #ffed02;
          position: relative;
          transform: translateY(1px);
          z-index: 1;
        }
        .duck__head::after,
        .duck__head::before {
          content: "";
          position: absolute;
          border-radius: 1rem;
          background-color: #ffed02;
          width: 0.4rem;
          height: 2rem;
          top: 0;
        }
        .duck__head::after {
          left: 44%;
          transform: translate(-50%, -50%) rotate(-30deg);
        }
        .duck__head::before {
          left: 45%;
          transform: translate(-50%, -50%) rotate(10deg);
        }
        .duck__white {
          position: absolute;
          top: 0.8rem;
          left: 0.8rem;
          width: 0.6rem;
          height: 1.3rem;
          transform: rotate(40deg);
          border-radius: 50%;
          border-left: 0.2rem solid #fff;
        }
        .duck__eye {
          position: absolute;
          bottom: 0.2rem;
          right: 1rem;
          width: 0.8rem;
          height: 0.8rem;
          border-radius: 50%;
          background-color: #000;
          animation: eye-animation 1s infinite linear;
        }
        .duck__eye--shadow {
          position: absolute;
          bottom: -0.5rem;
          right: 2rem;
          width: 0.8rem;
          height: 0.8rem;
          border-radius: 50%;
          background-color: #fcaa1d;
          z-index: 1;
        }
        .duck__mouth {
          position: absolute;
          right: 0;
          top: 40%;
          width: 1rem;
          height: 1.2rem;
          transform: translate(90%, -50%);
          clip-path: polygon(0 0, 100% 40%, 100% 60%, 0% 100%);
          border-radius: 0 1rem 1rem 0;
          background-color: #f57a00;
        }
        .duck__body {
          width: 9.5rem;
          height: 5rem;
          border-radius: 1rem 0 16rem 16rem;
          background-color: #ffed02;
          position: relative;
          overflow: hidden;
        }
        .duck__body::after {
          content: "";
          position: absolute;
          width: 105%;
          height: 200%;
          left: 50%;
          top: -95%;
          transform: translate(-50%, 0.02rem) rotate(-6deg);
          border-radius: 50%;
          border-bottom: 1rem solid #fcaa1d;
        }
        .duck__wing {
          position: absolute;
          left: 0.6rem;
          top: 55%;
          width: 4rem;
          height: 2.4rem;
          border-radius: 1rem 1rem 4rem 4rem;
          background-color: #fece00;
          transform: translate(0, -50%);
          transform-origin: right;
          animation: wing-animation 1s linear infinite;
          z-index: 1;
        }
        .duck__foot {
          position: absolute;
          width: 0.6rem;
          height: 2rem;
          background-color: #f57a00;
          z-index: -1;
        }
        .duck__foot::after {
          content: "";
          position: absolute;
          width: 2rem;
          height: 0.6rem;
          bottom: 0rem;
          left: -0.5rem;
          background-color: #f57a00;
          border-radius: 1rem;
        }
        .duck__foot--1,
        .duck__foot--2 {
          left: 40%;
          bottom: 0;
          transform: translate(-50%, 80%);
        }
        .duck__foot--1 {
          animation: foot-ans 1s linear infinite;
        }
        .duck__foot--2 {
          animation: foot-ans 2s 1s linear infinite;
        }

        .surface {
          position: absolute;
          bottom: -1.9rem;
          left: 55%;
          transform: translateX(-50%);
          background-color: steelblue;
          width: 8rem;
          height: 0.5rem;
          border-radius: 1rem;
          animation: surface-animation 1s linear infinite;
        }

        @keyframes surface-animation {
          0%,
          100% {
            transform: translateX(-50%) scaleX(0.9);
          }
          50% {
            transform: translateX(-50%) scaleX(1);
          }
        }
        @keyframes foot-ans {
          0% {
            transform: translate(-50%, 80%) rotate(0deg);
          }
          10% {
            transform: translate(-150%, 80%) rotate(10deg);
          }
          20% {
            transform: translate(-150%, 10%) rotate(10deg);
          }
          40% {
            transform: translate(400%, 10%) rotate(-20deg);
          }
          60% {
            transform: translate(600%, 60%) rotate(-20deg);
          }
          70% {
            transform: translate(500%, 60%) rotate(0deg);
          }
        }
        .duck__inner {
          animation: bird-up-down 1s linear infinite;
        }

        @keyframes bird-up-down {
          0%,
          100% {
            transform: translateY(0.4rem);
          }
          50% {
            transform: translateY(0rem);
          }
        }
        @keyframes wing-animation {
          0%,
          100% {
            transform: translate(0, -50%) rotate(16deg);
          }
          50% {
            transform: translate(0, -50%) rotate(-2deg);
          }
        }
        @keyframes eye-animation {
          0%,
          20% {
            transform: scaleY(1);
          }
          10% {
            transform: scaleY(0);
          }
        }
        .cloud {
          position: absolute;
          top: 10vh;
          left: 0;
          width: 5rem;
          height: 3rem;
          border-radius: 6rem 6rem 0 1rem;
          background-color: white;
          transform: translateX(110vw);
          animation: cloud-animation-1 10s linear infinite;
        }
        .cloud--2,
        .cloud--4 {
          top: 20vh;
          transform: translateX(120vw) scale(0.8);
          animation: cloud-animation-2 10s 2.5s linear infinite;
        }
        .cloud--3 {
          animation-delay: 5s;
        }
        .cloud--4 {
          animation-delay: 7.5s;
        }
        .cloud::after {
          content: "";
          position: absolute;
          width: 6rem;
          height: 3.5rem;
          bottom: 0;
          border-radius: 6rem 10rem 1rem 0;
          transform: translateX(3rem);
          background-color: #fff;
        }
        .cloud::before {
          content: "";
          position: absolute;
          width: 4rem;
          height: 3rem;
          bottom: 2rem;
          border-radius: 10rem 10rem 0 0;
          transform: translateX(2rem);
          background-color: #fff;
        }

        @keyframes cloud-animation-1 {
          0% {
            transform: translate(110vw);
          }
          100% {
            transform: translateX(-50vw);
          }
        }
        @keyframes cloud-animation-2 {
          0% {
            transform: translateX(110vw) scale(0.8);
          }
          100% {
            transform: translateX(-50vw) scale(0.8);
          }
        }
      </style>

      <h1 style="color:white;">Hi, im STOJANOVICLJUBINKO</h1>
      <div class="cloud cloud--1"></div>
                    <div class="cloud cloud--2"></div>
                    <div class="cloud cloud--3"></div>
                    <div class="cloud cloud--4"></div>
                    <div class="duck__wrapper" style="margin-left:50px; margin-top:250px;">
                        <div class="duck">
                            <div class="duck duck__inner">
                                <div class="duck__mouth"></div>
                                <div class="duck__head">
                                    <div class="duck__eye"></div>
                                    <div class="duck__eye--shadow"></div>
                                    <div class="duck__white"></div>
                                </div>
                                <div class="duck__body"></div>
                                <div class="duck__wing"></div>
                            </div>
                            <div class="duck__foot duck__foot--1" style="z-index: 1;"></div>
                            <div class="duck__foot duck__foot--2" style="z-index: 1;"></div>
                            <div class="surface"></div>
                        </div>
                        </div>
  </foreignObject>
</svg>

