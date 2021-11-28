<template>
    <div>

  <style>
    .modal {
      transition: opacity 0.25s ease;
    }
    body.modal-active {
      overflow-x: hidden;
      overflow-y: visible !important;
    }
  </style>


<body class="relative   items-center justify-center ">
  
  <a class=" modal-open pl-3 inline-block no-underline hover:text-black" href="#">
                    <svg class="fill-current hover:text-black" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24">
                        <path d="M21,7H7.462L5.91,3.586C5.748,3.229,5.392,3,5,3H2v2h2.356L9.09,15.414C9.252,15.771,9.608,16,10,16h8 c0.4,0,0.762-0.238,0.919-0.606l3-7c0.133-0.309,0.101-0.663-0.084-0.944C21.649,7.169,21.336,7,21,7z M17.341,14h-6.697L8.371,9 h11.112L17.341,14z" />
                        <circle cx="10.5" cy="18.5" r="1.5" />
                        <circle cx="17.5" cy="18.5" r="1.5" />
                    </svg>
                </a>
  
  <!--Modal-->
  <div class=" text-black modal opacity-0 pointer-events-none fixed w-full h-full top-0 left-0 flex items-center justify-center">
    <div class="modal-overlay absolute w-full h-full bg-gray-900 opacity-50"></div>
    
    <div class="modal-container bg-white w-11/12 md:max-w-md mx-auto rounded shadow-lg z-50 overflow-y-auto">
      
      <div class="modal-close absolute top-0 right-0 cursor-pointer flex flex-col items-center mt-4 mr-4 text-white text-sm z-50">
        <svg class="fill-current text-white" xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 18 18">
          <path d="M14.53 4.53l-1.06-1.06L9 7.94 4.53 3.47 3.47 4.53 7.94 9l-4.47 4.47 1.06 1.06L9 10.06l4.47 4.47 1.06-1.06L10.06 9z"></path>
        </svg>
        <span class="text-sm">(salir)</span>
      </div>

      <!-- Add margin if you want to see some of the overlay behind the modal-->
      <div class="modal-content py-4 text-left px-6" style="">
        <!--Title-->
        <div class="flex justify-between items-center pb-3">
          <p class="text-2xl font-bold">carrito de compras</p>
          <div class="modal-close cursor-pointer z-50">
            <svg class="fill-current text-black" xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 18 18">
              <path d="M14.53 4.53l-1.06-1.06L9 7.94 4.53 3.47 3.47 4.53 7.94 9l-4.47 4.47 1.06 1.06L9 10.06l4.47 4.47 1.06-1.06L10.06 9z"></path>
            </svg>
          </div>
        </div>

        <!--Body-->
        <div style="overflow-y:scroll; max-height:70vh">
        <p>Modal content can go here</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
        <p>...</p>
</div>
        <!--Footer-->
        <div class="flex justify-end pt-2">
          <button class="px-4 bg-transparent p-3 rounded-lg text-indigo-500 hover:bg-gray-100 hover:text-indigo-400 mr-2">vaciar</button>
          <button class="modal-close px-4 bg-indigo-500 p-3 rounded-lg text-white hover:bg-indigo-400">cerrar</button>
        </div>
        
      </div>
    </div>
  </div>

  <script>
    var openmodal = document.querySelectorAll('.modal-open')
    for (var i = 0; i < openmodal.length i++) {
      openmodal[i].addEventListener('click', function(event){
    	event.preventDefault()
    	toggleModal()
      })
    }
    
    const overlay = document.querySelector('.modal-overlay')
    overlay.addEventListener('click', toggleModal)
    
    var closemodal = document.querySelectorAll('.modal-close')
    for (var i = 0; i < closemodal.length; i++) {
      closemodal[i].addEventListener('click', toggleModal)
    }
    
    document.onkeydown = function(evt) {
      evt = evt || window.event
      var isEscape = false
      if ("key" in evt) {
    	isEscape = (evt.key === "Escape" || evt.key === "Esc")
      } else {
    	isEscape = (evt.keyCode === 27)
      }
      if (isEscape && document.body.classList.contains('modal-active')) {
    	toggleModal()
      }
    };
    
    
    function toggleModal () {
      const body = document.querySelector('body')
      const modal = document.querySelector('.modal')
      modal.classList.toggle('opacity-0')
      modal.classList.toggle('pointer-events-none')
      body.classList.toggle('modal-active')
    }
    
     
  </script>
</body>
    
    </div>
</template>