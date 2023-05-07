<template>
    <div class="card shadow p-3 mb-5 bg-body-tertiary rounded mh-300px">
      <div class="row">
        <div class="col-1">
          <img
            width="30"
            class="rounded"
            src="https://picsum.photos/200"
            alt=""
          />
        </div>
        <div class="col-8 d-flex align-items-center">
          <input
            type="text"
            placeholder="Type message"
            class="meso h-100 w-100 border-0 outline-0"
          />
        </div>
        <div class="col-3">
          <div class="d-flex align-items-center justify-content-evenly">
            <img
              width="20"
              src="https://img.icons8.com/external-outline-stroke-bomsymbols-/91/null/external-attach-general-office-outline-outline-stroke-bomsymbols-.png"
            />
            <img
              width="20"
              src="https://img.icons8.com/small/16/null/image.png"
            />
            <img
              width="20"
              src="https://img.icons8.com/ios-filled/50/null/ringer-volume.png"
            />
            <span> &#128512; </span>
          </div>
        </div>
      </div>
      <hr />
      <div class="row">
        <div class="col-3">
          <section class="d-flex align-items-center justify-content-evenly">
            <img
              width="20"
              src="https://img.icons8.com/wired/64/null/phone.png"
            />
            <span class="text-primary">Join</span>
          </section>
        </div>
        <div class="col-3">
          <section class="d-flex align-items-center justify-content-evenly">
            <img
              width="20"
              src="https://img.icons8.com/ios-filled/50/null/camcorder-pro.png"
            />
            <span class="text-primary">Record</span>
          </section>
        </div>
        <div class="col-3">
          <section class="d-flex align-items-center justify-content-evenly">
            <img
              width="20"
              src="https://img.icons8.com/material-outlined/24/null/video.png"
            />
            <span class="text-primary">Join</span>
          </section>
        </div>
      </div>
    </div>
  </template>
  
  <style scoped>
  .meso {
    outline: none;
  }
  .meso:focus {
    outline: 1px solid steelblue;
  }
  </style>
  