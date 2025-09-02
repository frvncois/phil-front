<template>
    <section>
        <div class="projects is-wrap">
            <div class="projects is-title">
                <div class="title is-line"><h2>No fluff. Just results.</h2></div>
            </div>
            <div class="projects is-filters">
                <ul>
                    <li><button class="is-active">All</button></li>
                    <li><button>Features</button></li>
                    <li><button>Retails</button></li>
                    <li><button>Food</button></li>
                    <li><button>Services</button></li>
                    <li><button>Tech</button></li>
                    <li><button>Social Impact</button></li>
                </ul>
            </div>
            <div class="projects is-list">
                <ul>
                    <li>
                        <div class="is-cover">
                            <img src="@/assets/01.png" />
                            <h2>Project Title</h2>
                        </div>
                        <div class="is-details">
                            <h3>Lorem ipsum</h3>
                            <div class="is-tags">
                                <span><img src="@/assets/tags-top.svg"/>Web</span>
                                <span><img src="@/assets/tags-top.svg"/>Mobile</span>
                                <span><img src="@/assets/tags-top.svg"/>AI</span>
                            </div>
                        </div>
                    </li>
                    <li>
                        <div class="is-cover">
                            <img src="@/assets/02.png" />
                            <h2>Project Title</h2>
                        </div>
                        <div class="is-details">
                            <h3>Project Two</h3>
                            <div class="is-tags">
                                <span><img src="@/assets/tags-top.svg"/>Web</span>
                                <span><img src="@/assets/tags-top.svg"/>Mobile</span>
                                <span><img src="@/assets/tags-top.svg"/>AI</span>
                            </div>
                        </div>
                    </li>
                    <li>
                        <div class="is-cover">
                            <img src="@/assets/03.png" />
                            <h2>Project Title</h2>
                        </div>
                        <div class="is-details">
                            <h3>Project Three</h3>
                            <div class="is-tags">
                                <span><img src="@/assets/tags-top.svg"/>Web</span>
                                <span><img src="@/assets/tags-top.svg"/>Mobile</span>
                                <span><img src="@/assets/tags-top.svg"/>AI</span>
                            </div>
                        </div>
                    </li>
                    <li>
                        <div class="is-cover">
                            <img src="@/assets/04.png" />
                            <h2>Project Title</h2>
                        </div>
                        <div class="is-details">
                            <h3>Project Four</h3>
                            <div class="is-tags">
                                <span><img src="@/assets/tags-top.svg"/>Web</span>
                                <span><img src="@/assets/tags-top.svg"/>Mobile</span>
                                <span><img src="@/assets/tags-top.svg"/>AI</span>
                            </div>
                        </div>
                    </li>
                    <li>
                        <div class="is-cover">
                            <img src="@/assets/01.png" />
                            <h2>Project Title</h2>
                        </div>
                        <div class="is-details">
                            <h3>Project Five</h3>
                            <div class="is-tags">
                                <span><img src="@/assets/tags-top.svg"/>Web</span>
                                <span><img src="@/assets/tags-top.svg"/>Mobile</span>
                                <span><img src="@/assets/tags-top.svg"/>AI</span>
                            </div>
                        </div>
                    </li>
                    <li>
                        <div class="is-cover">
                            <img src="@/assets/02.png" />
                            <h2>Project Title</h2>
                        </div>
                        <div class="is-details">
                            <h3>Project Six</h3>
                            <div class="is-tags">
                                <span><img src="@/assets/tags-top.svg"/>Web</span>
                                <span><img src="@/assets/tags-top.svg"/>Mobile</span>
                                <span><img src="@/assets/tags-top.svg"/>AI</span>
                            </div>
                        </div>
                    </li>
                </ul>
            </div>
            <div class="projects is-cta">All work</div>
        </div>
    </section>
</template>

<style scoped>
/* First item - spans 3 rows */
.is-list li:nth-child(1) {
  grid-row: span 3;
}

/* Second item - spans 2 rows */
.is-list li:nth-child(2) {
  grid-row: span 2;
}

/* Third item - spans 1 row */
.is-list li:nth-child(3) {
  grid-row: span 3;
}

/* Fourth item - spans 2 rows */
.is-list li:nth-child(4) {
  grid-row: span 3;
}

/* Fifth item - spans 1 row */
.is-list li:nth-child(5) {
  grid-row: span 4;
}

/* Sixth item - spans 3 rows */
.is-list li:nth-child(6) {
  grid-row: span 3;
}
</style>