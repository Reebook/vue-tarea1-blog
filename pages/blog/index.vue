<template>
    <main>
      <nav class="navbar navbar-expand-lg navbar-light bg-light">
      <div class="container-fluid">
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav me-auto mb-2 mb-lg-0">
            <li class="nav-item">
              <NuxtLink class="nav-link" to="/">
                Inicio
              </NuxtLink>
            </li>
            <li class="nav-item">
              <NuxtLink class="nav-link" to="/blog">
                Blog
              </NuxtLink>
            </li>
          </ul>
        </div>
      </div>
    </nav>
    <div class="container">
      <div class="row">
        <h1>Lista de entradas</h1>
        <ul>
          <li>
            <NuxtLink class="nav-link" to="/blog/que_es_una_funcion_azure">
              ¿Qué es una función en Azure?
              </NuxtLink>
          </li>
          <li>
            <NuxtLink class="nav-link" to="/blog/casos_de_uso">
              Casos de uso
              </NuxtLink>
          </li>
          <li>
            <NuxtLink class="nav-link" to="/blog/que_no_hacer_con_funciones">
              ¿Qué no se debe hacer en Azure Functions?
              </NuxtLink>
          </li>
          <li>
            <NuxtLink class="nav-link" to="/blog/que_ofrece_nube_azure">
              ¿Qué ofrece la nube de Azure?
              </NuxtLink>
          </li>
            
        </ul>
        
      </div>
    </div>
      
    </main>
  </template>