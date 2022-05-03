import React from "react";
import AppBar from '@mui/material/AppBar';
import Box from '@mui/material/Box';
import Toolbar from '@mui/material/Toolbar';
import Typography from '@mui/material/Typography';
import './index.css';
import Grid from '@mui/material/Grid';
import { Button, InputGroup, FormControl } from 'react-bootstrap';
import 'bootstrap/dist/css/bootstrap.min.css';
import { FontAwesomeIcon } from '@fortawesome/react-fontawesome';
import { library } from '@fortawesome/fontawesome-svg-core';
import { fas } from '@fortawesome/free-solid-svg-icons';
import { faTwitter, faFontAwesome } from '@fortawesome/free-brands-svg-icons';
import { useState } from 'react';
import { FaBootstrap, FaAngular, FaJsfiddle } from 'react-icons/fa';
library.add(fas, faTwitter, faFontAwesome)



function App() {

  // code to hide dropdown on clicking outside button

  //1
  const [drop, setdrop] = useState({
    open: false
  })

  const tog = () => {
    setdrop({ open: !drop.open });
  }


  //2

  const [dropp, setdropp] = useState({
    open: false
  })

  const tog2 = () => {
    setdropp({ open: !dropp.open });
  }

  //3

  const [droppp, setdroppp] = useState({
    open: false
  })

  const tog3 = () => {
    setdroppp({ open: !droppp.open });
  }

  //4

  const [dropppp, setdropppp] = useState({
    open: false
  })

  const tog4 = () => {
    setdropppp({ open: !dropppp.open });
  }

  // Dropdown list Function

  const myFunction = (id1, id2) => {

    var i;
    var x = document.getElementsByClassName("dropdown-content");
    for (i = 0; i < x.length; i++) {
      x[i].style.display = "none";
    }

    document.getElementById(id1).classList.toggle("show");
    document.getElementById(id2).classList.toggle("fa2");

  }

  // Tab navigation Function

  const openCity = (cityName) => {
    var a = cityName;
    var i;
    var x = document.getElementsByClassName("city");
    for (i = 0; i < x.length; i++) {
      x[i].style.display = "none";
    }
    document.getElementById(a).style.display = "block";
  }

  return (
    <>
      {/* Top Grid */}

      <div className="body">
        <div className="topgrid">
          <span className="new">New!</span><br />
          <Grid container spacing={2}>
            <div className='SB'>
              <Grid >
                <span ><a className="Bs" href="https://startbootstrap.com/"> <img className="bootimg" src="sb.png"></img>  Start Bootstrap </a></span>
              </Grid>
            </div>


            {/* Dropdown Buttons */}

            <div class="navbar" >
              <Grid className='home' >
                <div class="dropdown1">
                  <div class="fa1">
                    <button class="dropbtn1" id='b1' onBlur={() => tog()}
                      onFocus={() => tog()} tabIndex="0" onClick={() => myFunction("myDropdown1", "FaB1")}>&nbsp;&nbsp;&nbsp;&nbsp;Themes  </button>
                    <button class="Fb" id="FaB1" onBlur={() => tog()}
                      onFocus={() => tog()} tabIndex="0" onClick={() => myFunction("myDropdown1", "FaB1")}><FontAwesomeIcon icon="fa-solid fa-angle-right" /></button>
                  </div>
                  <div class="dropdown-content1" id="myDropdown1">
                    {drop.open && (
                      <div>
                        <a className="ddimggr" href=""><FontAwesomeIcon className="dpdimgr" icon="fa-solid fa-paintbrush" /> &nbsp; Browse All Themes</a>
                        <a className="ddimggr" href=""><FontAwesomeIcon className="dpdimgr" icon="fa-solid fa-tags" /> &nbsp;  Pro Bootstrap Themes</a>
                        <span className="dplist"  >Theme Catagories:</span>
                        <a className="ddimggr" href="">Admin Dashboard</a>
                        <a className="ddimggr" href="">Landing Pages</a>
                        <a className="ddimggr" href="">Buisness & Corporate</a>
                        <a className="ddimggr" href="">Portfolio & Resume</a>
                        <a className="ddimggr" href="">Blog</a>
                      </div>
                    )}
                  </div>
                </div>
              </Grid>

              <Grid className='home' >
                <div class="dropdown1">
                  <div class="fa1">
                    <button class="dropbtn2" id='b1' onBlur={() => tog2()}
                      onFocus={() => tog2()} tabIndex="0" onClick={() => myFunction("myDropdown2", "FaB2")}>Templates  </button>
                    <button class="Fb" id="FaB2" onBlur={() => tog2()}
                      onFocus={() => tog2()} tabIndex="0" onClick={() => myFunction("myDropdown2", "FaB2")}  ><FontAwesomeIcon icon="fa-solid fa-angle-right" /></button>
                  </div>
                  <div class="dropdown-content1" id="myDropdown2">
                    {dropp.open && (
                      <div>
                        <a className="ddimggr" href="https://startbootstrap.com/templates"><FontAwesomeIcon className="dpdimgb" icon="fa-solid fa-pen-ruler" /> &nbsp; Browse All Themplates</a>
                        <span className="dplistb">Template Catagories:</span>
                        <a className="ddimggr" href="">Admin & Dashboard</a>
                        <a className="ddimggr" href="">Landing Pages & Headers</a>
                        <a className="ddimggr" href="">General Page Layouts</a>
                        <a className="ddimggr" href="">Navigation Layouts</a>
                        <a className="ddimggr" href="">Ecommerce</a>
                        <a className="ddimggr" href="">Blog</a>
                      </div>
                    )}
                  </div>
                </div>
              </Grid>

              <Grid className='home' >
                <div class="dropdown1">
                  <div class="fa1">
                    <button class="dropbtn3" id='b1' onBlur={() => tog3()}
                      onFocus={() => tog3()} tabIndex="0" onClick={() => myFunction("myDropdown3", "FaB3")}>Bundles  </button>
                    <button class="Fb" id="FaB3" onBlur={() => tog3()}
                      onFocus={() => tog3()} tabIndex="0" onClick={() => myFunction("myDropdown3", "FaB3")}><FontAwesomeIcon icon="fa-solid fa-angle-right" /></button>
                  </div>
                  <div class="dropdown-content1" id="myDropdown3">
                    {droppp.open && (
                      <div>
                        <a className="ddimggr" href="#"><span className="dpboot"> <FaBootstrap /> </span>  &nbsp;  Bootstrap HTML Bundle</a>
                        <a className="ddimggr" href="#"><span className="dpdimgr">< FaAngular /></span> &nbsp; Pro Angular Bundle</a>
                      </div>
                    )}
                  </div>
                </div>
              </Grid>

              {/* Forms Button */}

              <Grid  >
                <div >
                  <a className="Na" href="https://startbootstrap.com/solution/contact-forms">Forms</a>
                </div>
              </Grid>

              <Grid className='home' >
                <div class="dropdown1">
                  <div class="fa1">
                    <button class="dropbtn4" id='b1' onBlur={() => tog4()}
                      onFocus={() => tog4()} tabIndex="0" onClick={() => myFunction("myDropdown4", "FaB4")}>&nbsp;&nbsp;Resources  </button>
                    <button class="Fb" id="FaB4" onBlur={() => tog4()}
                      onFocus={() => tog4()} tabIndex="0" onClick={() => myFunction("myDropdown4", "FaB4")}><FontAwesomeIcon icon="fa-solid fa-angle-right" /></button>
                  </div>
                  <div class="dropdown-content1" id="myDropdown4">
                    {dropppp.open && (
                      <div>
                        <span className="dplist">Resources</span>
                        <a className="ddimggr" href="#"><FontAwesomeIcon className="ddimggrimg" icon="fa-solid fa-code" />  &nbsp; Snippets</a>
                        <a className="ddimggr" href="#"><FontAwesomeIcon className="ddimggrimg" icon="fa-solid fa-circle-question" />  &nbsp; Knowledge Base</a>
                        <a className="ddimggr" href="#"><FontAwesomeIcon className="ddimggrimg" icon="fa-solid fa-list" />  &nbsp; Bootstrap Resources List</a>
                        <a className="ddimggr" href="#"><FontAwesomeIcon className="ddimggrimg" icon="fa-solid fa-book" /> &nbsp; Guides</a>
                        <span className="dplist">Tools & Plugins</span>
                        <a className="ddimggr" href="#"><span className="ddimggrimg">< FaAngular /></span> &nbsp;SB Angular Inspector</a>
                        <a className="ddimggr" href="#"><FontAwesomeIcon className="ddimggrimg" icon="fa-solid fa-wrench" /> &nbsp;SB Form Builder</a>
                      </div>
                    )}
                  </div>
                </div>
              </Grid>
            </div>

            {/* Blog Button */}

            <div className="navbar">
              <Grid className='home2' >
                <div class="dropdown1">
                  <a href="https://startbootstrap.com/blog"><button class="dropbtn1" >
                    Blog  </button></a>
                </div>
              </Grid>
            </div>

            {/* Log In Button */}

            <div className="cart">
              <Grid >
                <a href="https://startbootstrap.com/auth/login"> <Button variant="danger">
                  Log In  </Button> </a>
              </Grid>
            </div>
          </Grid>
        </div>
        <br></br>

        {/* Orange Box */}

        <Box sx={{ flexGrow: 1 }}>
          <AppBar position="static">
            <Toolbar style={{ height: "185px" }} className="color">
              <Typography component="div" sx={{ flexGrow: 1 }} >
                <h5 className="fontstyle1">
                  Bootstrap Responsive Pricing Table Snippet
                </h5>
                <div className="fontstyle2">
                  Pricing Table with Custom Hover Effects and Buttons
                </div>
              </Typography>

              <div className="image1">
                <Box sx={{ flexGrow: 1 }}>
                  <Grid container spacing={12}>
                    <Grid item xs={3}>
                      <a href="https://www.creative-tim.com/?affiliate_id=101249" target='_blank'> <img className="img1" src="box.jpg"></img> </a>
                    </Grid>
                    <Grid className="carbon-text" item xs={9}>
                      <h6 > Premium Bootstrap themes, templates,
                        and UI kit by Creative Tim </h6>
                    </Grid>
                  </Grid>
                </Box>
              </div>
            </Toolbar>
          </AppBar>
        </Box>

        {/* svg */}

        <div class="hero">
          <svg className="svgpoly" viewBox="0 0 100 100" preserveAspectRatio="none">
            <polygon points="0,100 100,0 100,100" />
          </svg>
        </div>
        <br></br>

        {/* Bootstrap span */}

        <span className="Boot">Bootstrap 5.1.0</span>  <br></br>

        {/* Tab Navigation */}

        <div className="topgrid1">
          <div class="dropdown">
            <button class="dropbtn" name="Result" onClick={() => openCity("Result")}>Result</button> &nbsp;
            <button class="dropbtn" name="HTML" onClick={() => openCity("HTML")}>HTML</button>  &nbsp;
            <button class="dropbtn" name="CSS" onClick={() => openCity("CSS")}>CSS</button> &nbsp;
            <button class="dropbtn" name="Javascript" onClick={() => openCity("Javascript")}>Javascript</button> &nbsp;
            <button class="dropbtn" name="Resources" onClick={() => openCity("Resources")}>Resources</button> &nbsp;
            <span className="fiddle"><a href="https://jsfiddle.net/StartBootstrap/rgp3qdye/" target='_blank'><span className="fidimg"><FaJsfiddle /></span></a>  &nbsp;
              <a className="NaF" href='https://jsfiddle.net/StartBootstrap/rgp3qdye/' target='_blank'>Edit in JSFiddle</a></span>
          </div>
        </div>

        {/* Result Tab */}

        <div id="Result" class="city">
          <div>
            <section class="pricing py-5">
              <div class="container">
                <div class="row">
                  {/* <!-- Free Tier --> */}
                  <div class="col-lg-4">
                    <div class="card mb-5 mb-lg-0">
                      <div class="card-body">
                        <h5 class="card-title text-muted text-uppercase text-center">Free</h5>
                        <h6 class="card-price text-center">$0<span class="period">/month</span></h6>
                        <hr></hr>
                        <ul class="fa-ul">
                          <li><span class="fa-li"><FontAwesomeIcon icon="fa-solid fa-check" /></span>Single User</li>
                          <li><span class="fa-li"><FontAwesomeIcon icon="fa-solid fa-check" /></span>5GB Storage</li>
                          <li><span class="fa-li"><FontAwesomeIcon icon="fa-solid fa-check" /></span>Unlimited Public Projects</li>
                          <li><span class="fa-li"><FontAwesomeIcon icon="fa-solid fa-check" /></span>Community Access</li>
                          <li class="text-muted"><span class="fa-li"><FontAwesomeIcon icon="fa-solid fa-xmark" /></span>Unlimited
                            Private Projects</li>
                          <li class="text-muted"><span class="fa-li"><FontAwesomeIcon icon="fa-solid fa-xmark" /></span>Dedicated
                            Phone Support</li>
                          <li class="text-muted"><span class="fa-li"><FontAwesomeIcon icon="fa-solid fa-xmark" /></span>Free Subdomain
                          </li>
                          <li class="text-muted"><span class="fa-li"><FontAwesomeIcon icon="fa-solid fa-xmark" /></span>Monthly Status
                            Reports</li>
                        </ul>
                        <div class="d-grid">
                          <a href="#" class="btn btn-primary text-uppercase">Button</a>
                        </div>
                      </div>
                    </div>
                  </div>
                  {/* <!-- Plus Tier --> */}
                  <div class="col-lg-4">
                    <div class="card mb-5 mb-lg-0">
                      <div class="card-body">
                        <h5 class="card-title text-muted text-uppercase text-center">Plus</h5>
                        <h6 class="card-price text-center">$9<span class="period">/month</span></h6>
                        <hr></hr>
                        <ul class="fa-ul">
                          <li><span class="fa-li"><FontAwesomeIcon icon="fa-solid fa-check" /></span><strong>5 Users</strong></li>
                          <li><span class="fa-li"><FontAwesomeIcon icon="fa-solid fa-check" /></span>50GB Storage</li>
                          <li><span class="fa-li"><FontAwesomeIcon icon="fa-solid fa-check" /></span>Unlimited Public Projects</li>
                          <li><span class="fa-li"><FontAwesomeIcon icon="fa-solid fa-check" /></span>Community Access</li>
                          <li><span class="fa-li"><FontAwesomeIcon icon="fa-solid fa-check" /></span>Unlimited Private Projects</li>
                          <li><span class="fa-li"><FontAwesomeIcon icon="fa-solid fa-check" /></span>Dedicated Phone Support</li>
                          <li><span class="fa-li"><FontAwesomeIcon icon="fa-solid fa-check" /></span>Free Subdomain</li>
                          <li class="text-muted"><span class="fa-li"><FontAwesomeIcon icon="fa-solid fa-xmark" /></span>Monthly Status
                            Reports</li>
                        </ul>
                        <div class="d-grid">
                          <a href="#" class="btn btn-primary text-uppercase">Button</a>
                        </div>
                      </div>
                    </div>
                  </div>
                  {/* <!-- Pro Tier --> */}
                  <div class="col-lg-4">
                    <div class="card">
                      <div class="card-body">
                        <h5 class="card-title text-muted text-uppercase text-center">Pro</h5>
                        <h6 class="card-price text-center">$49<span class="period">/month</span></h6>
                        <hr></hr>
                        <ul class="fa-ul">
                          <li><span class="fa-li"><FontAwesomeIcon icon="fa-solid fa-check" /></span><strong>Unlimited Users</strong>
                          </li>
                          <li><span class="fa-li"><FontAwesomeIcon icon="fa-solid fa-check" /></span>150GB Storage</li>
                          <li><span class="fa-li"><FontAwesomeIcon icon="fa-solid fa-check" /></span>Unlimited Public Projects</li>
                          <li><span class="fa-li"><FontAwesomeIcon icon="fa-solid fa-check" /></span>Community Access</li>
                          <li><span class="fa-li"><FontAwesomeIcon icon="fa-solid fa-check" /></span>Unlimited Private Projects</li>
                          <li><span class="fa-li"><FontAwesomeIcon icon="fa-solid fa-check" /></span>Dedicated Phone Support</li>
                          <li><span class="fa-li"><FontAwesomeIcon icon="fa-solid fa-check" /></span><strong>Unlimited</strong> Free
                            Subdomains</li>
                          <li><span class="fa-li"><FontAwesomeIcon icon="fa-solid fa-check" /></span>Monthly Status Reports</li>
                        </ul>
                        <div class="d-grid">
                          <a href="#" class="btn btn-primary text-uppercase">Button</a>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </section>
          </div>
        </div>

        {/* HTML Tab */}

        <div id="HTML" class="city" style={{ display: "none" }}>
          <div className="topgrid2">
            <pre>
              &lt;section class="pricing py-5"&gt; <br></br>
              &lt;div class="container"&gt; <br></br>
              &lt;div class="row"&gt; <br></br>
              &lt;!-- Free Tier --&gt; <br></br>
              &lt;div class="col-lg-4"&gt; <br></br>
              &lt;div class="card mb-5 mb-lg-0"&gt; <br></br>
              &lt;div class="card-body"&gt; <br></br>
              &lt;h5 class="card-title text-muted text-uppercase text-center"&gt;Free&lt;/h5&gt; <br></br>
              &lt;h6 class="card-price text-center"&gt;$0&lt;span class="period"&gt;/month&lt;/span&gt;&lt;/h6&gt; <br></br>
              &lt;hr&gt; <br></br>
              &lt;ul class="fa-ul"&gt; <br></br>
              &lt;li&gt;&lt;span class="fa-li"&gt;&lt;i class="fas fa-check"&gt;&lt;/i&gt;&lt;/span&gt;Single User&lt;/li&gt; <br></br>
              &lt;li&gt;&lt;span class="fa-li"&gt;&lt;i class="fas fa-check"&gt;&lt;/i&gt;&lt;/span&gt;5GB Storage&lt;/li&gt; <br></br>
              &lt;li&gt;&lt;span class="fa-li"&gt;&lt;i class="fas fa-check"&gt;&lt;/i&gt;&lt;/span&gt;Unlimited Public Projects&lt;/li&gt; <br></br>
              &lt;li&gt;&lt;span class="fa-li"&gt;&lt;i class="fas fa-check"&gt;&lt;/i&gt;&lt;/span&gt;Community Access&lt;/li&gt; <br></br>
              &lt;li class="text-muted"&gt;&lt;span class="fa-li"&gt;&lt;i class="fas fa-times"&gt;&lt;/i&gt;&lt;/span&gt;Unlimited
              Private Projects&lt;/li&gt; <br></br>
              &lt;li class="text-muted"&gt;&lt;span class="fa-li"&gt;&lt;i class="fas fa-times"&gt;&lt;/i&gt;&lt;/span&gt;Dedicated
              Phone Support&lt;/li&gt; <br></br>
              &lt;li class="text-muted"&gt;&lt;span class="fa-li"&gt;&lt;i class="fas fa-times"&gt;&lt;/i&gt;&lt;/span&gt;Free Subdomain
              &lt;/li&gt; <br></br>
              &lt;li class="text-muted"&gt;&lt;span class="fa-li"&gt;&lt;i class="fas fa-times"&gt;&lt;/i&gt;&lt;/span&gt;Monthly Status
              Reports&lt;/li&gt; <br></br>
              &lt;/ul&gt; <br></br>
              &lt;div class="d-grid"&gt; <br></br>
              &lt;a href="#" class="btn btn-primary text-uppercase"&gt;Button&lt;/a&gt; <br></br>
              &lt;/div&gt; <br></br>
              &lt;/div&gt; <br></br>
              &lt;/div&gt; <br></br>
              &lt;/div&gt; <br></br>
              &lt;!-- Plus Tier --&gt; <br></br>
              &lt;div class="col-lg-4"&gt; <br></br>
              &lt;div class="card mb-5 mb-lg-0"&gt; <br></br>
              &lt;div class="card-body"&gt; <br></br>
              &lt;h5 class="card-title text-muted text-uppercase text-center"&gt;Plus&lt;/h5&gt; <br></br>
              &lt;h6 class="card-price text-center"&gt;$9&lt;span class="period"&gt;/month&lt;/span&gt;&lt;/h6&gt; <br></br>
              &lt;hr&gt; <br></br>
              &lt;ul class="fa-ul"&gt; <br></br>
              &lt;li&gt;&lt;span class="fa-li"&gt;&lt;i class="fas fa-check"&gt;&lt;/i&gt;&lt;/span&gt;&lt;strong&gt;5 Users&lt;/strong&gt;&lt;/li&gt; <br></br>
              &lt;li&gt;&lt;span class="fa-li"&gt;&lt;i class="fas fa-check"&gt;&lt;/i&gt;&lt;/span&gt;50GB Storage&lt;/li&gt; <br></br>
              &lt;li&gt;&lt;span class="fa-li"&gt;&lt;i class="fas fa-check"&gt;&lt;/i&gt;&lt;/span&gt;Unlimited Public Projects&lt;/li&gt; <br></br>
              &lt;li&gt;&lt;span class="fa-li"&gt;&lt;i class="fas fa-check"&gt;&lt;/i&gt;&lt;/span&gt;Community Access&lt;/li&gt; <br></br>
              &lt;li&gt;&lt;span class="fa-li"&gt;&lt;i class="fas fa-check"&gt;&lt;/i&gt;&lt;/span&gt;Unlimited Private Projects&lt;/li&gt; <br></br>
              &lt;li&gt;&lt;span class="fa-li"&gt;&lt;i class="fas fa-check"&gt;&lt;/i&gt;&lt;/span&gt;Dedicated Phone Support&lt;/li&gt; <br></br>
              &lt;li&gt;&lt;span class="fa-li"&gt;&lt;i class="fas fa-check"&gt;&lt;/i&gt;&lt;/span&gt;Free Subdomain&lt;/li&gt; <br></br>
              &lt;li class="text-muted"&gt;&lt;span class="fa-li"&gt;&lt;i class="fas fa-times"&gt;&lt;/i&gt;&lt;/span&gt;Monthly Status
              Reports&lt;/li&gt; <br></br>
              &lt;/ul&gt; <br></br>
              &lt;div class="d-grid"&gt; <br></br>
              &lt;a href="#" class="btn btn-primary text-uppercase"&gt;Button&lt;/a&gt; <br></br>
              &lt;/div&gt; <br></br>
              &lt;/div&gt; <br></br>
              &lt;/div&gt; <br></br>
              &lt;/div&gt; <br></br>
              &lt;!-- Pro Tier --&gt; <br></br>
              &lt;div class="col-lg-4"&gt; <br></br>
              &lt;div class="card"&gt; <br></br>
              &lt;div class="card-body"&gt; <br></br>
              &lt;h5 class="card-title text-muted text-uppercase text-center"&gt;Pro&lt;/h5&gt; <br></br>
              &lt;h6 class="card-price text-center"&gt;$49&lt;span class="period"&gt;/month&lt;/span&gt;&lt;/h6&gt; <br></br>
              &lt;hr&gt; <br></br>
              &lt;ul class="fa-ul"&gt; <br></br>
              &lt;li&gt;&lt;span class="fa-li"&gt;&lt;i class="fas fa-check"&gt;&lt;/i&gt;&lt;/span&gt;&lt;strong&gt;Unlimited Users&lt;/strong&gt; <br></br>
              &lt;/li&gt; <br></br>
              &lt;li&gt;&lt;span class="fa-li"&gt;&lt;i class="fas fa-check"&gt;&lt;/i&gt;&lt;/span&gt;150GB Storage&lt;/li&gt; <br></br>
              &lt;li&gt;&lt;span class="fa-li"&gt;&lt;i class="fas fa-check"&gt;&lt;/i&gt;&lt;/span&gt;Unlimited Public Projects&lt;/li&gt; <br></br>
              &lt;li&gt;&lt;span class="fa-li"&gt;&lt;i class="fas fa-check"&gt;&lt;/i&gt;&lt;/span&gt;Community Access&lt;/li&gt; <br></br>
              &lt;li&gt;&lt;span class="fa-li"&gt;&lt;i class="fas fa-check"&gt;&lt;/i&gt;&lt;/span&gt;Unlimited Private Projects&lt;/li&gt; <br></br>
              &lt;li&gt;&lt;span class="fa-li"&gt;&lt;i class="fas fa-check"&gt;&lt;/i&gt;&lt;/span&gt;Dedicated Phone Support&lt;/li&gt; <br></br>
              &lt;li&gt;&lt;span class="fa-li"&gt;&lt;i class="fas fa-check"&gt;&lt;/i&gt;&lt;/span&gt;&lt;strong&gt;Unlimited&lt;/strong&gt; Free
              Subdomains&lt;/li&gt; <br></br>
              &lt;li&gt;&lt;span class="fa-li"&gt;&lt;i class="fas fa-check"&gt;&lt;/i&gt;&lt;/span&gt;Monthly Status Reports&lt;/li&gt; <br></br>
              &lt;/ul&gt; <br></br>
              &lt;div class="d-grid"&gt; <br></br>
              &lt;a href="#" class="btn btn-primary text-uppercase"&gt;Button&lt;/a&gt; <br></br>
              &lt;/div&gt; <br></br>
              &lt;/div&gt; <br></br>
              &lt;/div&gt; <br></br>
              &lt;/div&gt; <br></br>
              &lt;/div&gt; <br></br>
              &lt;/div&gt; <br></br>
              &lt;/section&gt;
            </pre>
          </div>
        </div>

        {/* Css Tab */}

        <div id="CSS" class="city" style={{ display: "none" }}>

          <div className="topgrid2">
            <pre>

              section.pricing &#123;<br></br>
              background: #007bff;<br></br>
              background: linear-gradient(to right, #0062E6, #33AEFF);<br></br>
              &#125; <br></br> <br></br>


              .pricing .card &#123;<br></br>
              border: none;<br></br>
              border-radius: 1rem;<br></br>
              transition: all 0.2s;<br></br>
              box-shadow: 0 0.5rem 1rem 0 rgba(0, 0, 0, 0.1);<br></br>
              &#125; <br></br> <br></br>


              .pricing hr &#123;<br></br>
              margin: 1.5rem 0;<br></br>
              &#125; <br></br> <br></br>


              .pricing .card-title &#123;<br></br>
              margin: 0.5rem 0;<br></br>
              font-size: 0.9rem;<br></br>
              letter-spacing: .1rem;<br></br>
              font-weight: bold;<br></br>
              &#125; <br></br> <br></br>


              .pricing .card-price &#123;<br></br>
              font-size: 3rem;<br></br>
              margin: 0;<br></br>
              &#125; <br></br> <br></br>


              .pricing .card-price .period &#123;<br></br>
              font-size: 0.8rem;<br ></br>
              &#125; <br></br> <br></br>


              .pricing ul li &#123;<br></br>
              margin-bottom: 1rem;<br></br>
              &#125; <br></br><br></br>


              .pricing .text-muted &#123;<br></br>
              opacity: 0.7;<br></br>
              &#125; <br></br><br></br>


              .pricing .btn &#123;<br></br>
              font-size: 80%;<br></br>
              border-radius: 5rem;<br></br>
              letter-spacing: .1rem;<br></br>
              font-weight: bold;<br></br>
              padding: 1rem;<br></br>
              opacity: 0.7;<br></br>
              transition: all 0.2s;<br></br>
              &#125; <br></br><br></br>


/* Hover Effects on Card */<br></br>

              @media (min-width: 992px) &#123;<br></br>
              .pricing .card:hover &#123;<br></br>
              margin-top: -.25rem;<br></br>
              margin-bottom: .25rem;<br></br>
              box-shadow: 0 0.5rem 1rem 0 rgba(0, 0, 0, 0.3);<br></br>
              &#125; <br></br><br></br>


              .pricing .card:hover .btn &#123;<br></br>
              opacity: 1;<br></br>
              &#125;<br></br>
            </pre>
          </div>
        </div>

        {/* Javascript Tab */}

        <div id="Javascript" class="city" style={{ display: "none" }}>
          <div className="topgrid3">
          </div>
        </div>

        {/* Resources Tab */}

        <div id="Resources" class="city" style={{ display: "none" }}>
          <div className="topgrid3">
            <span className='Re'>EXTERNAL RESOURCES LOADED INTO THIS FIDDLE:</span>
            <hr></hr> <br />
            <a className="fida" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css" target="_blank"> all.min.css</a>
            <hr></hr> <br />
            <a className="fida" href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.0/dist/css/bootstrap.min.css" target="_blank">bootstrap.min.css</a>
            <hr></hr> <br />
            <a className="fida" href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.0/dist/js/bootstrap.bundle.min.js" target="_blank">bootstrap.bundle.min.js</a>
            <hr></hr>
          </div>
        </div>
        <br></br>


        {/* Bottom SVG */}

        <div className="bsvg">
          <div class="hero1">
            <svg className="svg1" viewBox="0 0 100 100" preserveAspectRatio="none">
              <polygon points="0,100 100,0 100,100" />
            </svg>
          </div>

          <div className="dbar">
            <Box sx={{ flexGrow: 1 }}>
              <AppBar position="static">
                <Toolbar className="tb2" style={{ height: "300px" }}>
                  <Typography className="abar" sx={{ flexGrow: 1 }} >

                    <h2 className="dcard1">
                      Want more Bootstrap themes, templates, and UI tools?
                    </h2>
                    <div className="dcard2">
                      Subscribe to get updated when new Bootstrap related products arrive!
                    </div> <br></br>

                    {/* Input Button */}

                    <Grid container spacing={0}>
                      <Grid xs={11.5}>
                        <InputGroup className="mb-3">
                          <FormControl
                            placeholder="Email address..."
                            aria-label="Recipient's username"
                            aria-describedby="basic-addon2"
                          />
                          <Button variant="danger" className="DangerBt" id="button-addon2">
                            Subscribe
                          </Button>
                        </InputGroup>
                      </Grid>
                    </Grid>
                    <span className="smalltxt">This site is protected by reCAPTCHA and the Google Privacy Policy and Terms of Service apply.</span>
                  </Typography>
                  <div>

                    {/* Boy Image  */}

                    <Box sx={{ flexGrow: 1 }}>
                      <Grid container spacing={0}>
                        <Grid item xs={12}>
                          <img className="wimg" src="walln.png"></img>
                        </Grid>
                      </Grid>
                    </Box>
                  </div>
                </Toolbar>
              </AppBar>
            </Box> <br></br>
          </div>

          {/* Bottom Content */}

          <div className="bcontent">
            <Grid container spacing={3}>
              <Grid item xs={3}>
                <span className="Bcont1">Start Bootstrap</span> <br></br>
                <span>Free & premium UI tools to help you build better websites</span> <br></br>
                <a href="https://twitter.com/SBootstrap" target='_blank'><img className="fbimg1" src="twitter-brands.png"></img></a> &nbsp;&nbsp;&nbsp;
                <a href="https://github.com/StartBootstrap" target='_blank'><img className="fbimg1" src="github-brands.png"></img></a>&nbsp;&nbsp; &nbsp;
                <a href="https://www.facebook.com/StartBootstrap" target='_blank'><img className="fbimg1" src="facebook-brands.png"></img></a>
              </Grid>
              <Grid item xs={2}>
                <span className="Bcont">PRODUCTS</span> <br></br>
                <div className="Ba">
                  <span className="a"><a>Themes</a></span> <br></br>
                  <span className="a"> <a>Templates</a> </span> <br></br>
                  <span className="a">  <a>Snippets</a> </span> <br></br>
                  <span className="a">  <a>Guides</a> </span>
                </div>
              </Grid>
              <Grid item xs={2.5}>
                <span className="Bcont">RESOURCES</span> <br></br>
                <div className="Ba">
                  <span className="a">  <a>Blog</a> </span> <br></br>
                  <span className="a">   <a>Bootstrap Resources</a> </span> <br></br>
                  <span className="a">  <a>SB Angular Inspector</a> </span> <br></br>
                </div>
              </Grid>
              <Grid item xs={2.5}>
                <span className="Bcont">SUPPORT</span> <br></br>
                <div className="Ba">
                  <span className="a">  <a>Knowledge Base</a> </span> <br></br>
                  <span className="a">  <a>Custom Development</a> </span> <br></br>
                </div>
              </Grid>
              <Grid item xs={2}>
                <span className="Bcont">COMPANY</span> <br></br>
                <div className="Ba">
                  <span className="a">  <a>About Us</a> </span> <br></br>
                  <span className="a">  <a>Privacy Policy</a> </span> <br></br>
                  <span className="a">  <a>Terms and Conditions</a> </span> <br></br>
                  <span className="a">  <a>Licenses</a> </span> <br></br>
                </div>
              </Grid>
            </Grid>
          </div> <br></br>
          <div className="btmborder">
            <div className="btm">
              Copyright © Start Bootstrap LLC 2021 <br></br>
            </div>
            <div className="btm1">
              Website built with SB UI Kit Pro and SB Admin Pro with Illustrations by Stories by Freepik.
            </div>
          </div>
        </div>
      </div>
    </>
  );
}

export default App;
