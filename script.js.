
/* =================================
   FUNNGRO WEBSITE
   JavaScript
================================= */

document.addEventListener("DOMContentLoaded", function () {

  // Smooth scrolling for section links
  const sectionLinks = document.querySelectorAll(
    'a[href^="#"], a[href*="#"]'
  );

  sectionLinks.forEach(function (link) {

    link.addEventListener("click", function (event) {

      const url = new URL(link.href);

      if (
        url.pathname === window.location.pathname &&
        url.hash
      ) {
        const target = document.querySelector(url.hash);

        if (target) {
          event.preventDefault();

          target.scrollIntoView({
            behavior: "smooth",
            block: "start"
          });
        }
      }

    });

  });


  // Reveal feature cards when they enter the screen
  const cards = document.querySelectorAll(
    ".feature-card"
  );

  if ("IntersectionObserver" in window) {

    const observer = new IntersectionObserver(
      function (entries, currentObserver) {

        entries.forEach(function (entry) {

          if (entry.isIntersecting) {

            entry.target.classList.add("visible");

            currentObserver.unobserve(entry.target);

          }

        });

      },
      {
        threshold: 0.15
      }
    );

    cards.forEach(function (card) {
      observer.observe(card);
    });

  } else {

    cards.forEach(function (card) {
      card.classList.add("visible");
    });

  }

});
