---
date: 2026-08-19
title: Bird's Nest Troubleshooting – Symptom Selector
linkTitle: Bird's Nest Diagnosis
description: Learn how to diagnose and fix bird's nest problems on embroidery machines.
author: Kimi Embroidery Repair Tech Station
---

<style>
  /* force Hugo to treat this as raw HTML */
  .symptom-card {
    cursor: pointer;
    transition: transform 0.2s, box-shadow 0.2s;
    border: 2px solid #dee2e6;
    border-radius: 12px;
    overflow: hidden;
    background: #ffffff;
    box-shadow: 0 2px 8px rgba(0,0,0,0.08);
    margin-bottom: 20px;
    height: 100%;
  }
  .symptom-card:hover {
    transform: translateY(-3px);
    border-color: #0d6efd;
    box-shadow: 0 6px 20px rgba(13,110,253,0.15);
  }
  .symptom-image-box {
    width: 100%;
    height: 280px;
    display: flex;
    align-items: center;
    justify-content: center;
    background: #f8f9fa;
    overflow: hidden;
  }
  .symptom-image-box img {
    width: 100%;
    height: 100%;
    object-fit: contain;
    padding: 12px;
    box-sizing: border-box;
    display: block;
  }
  .symptom-label {
    min-height: 60px;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 12px;
    text-align: center;
    font-weight: 600;
    font-size: 1.05rem;
    background: #ffffff;
    border-top: 1px solid #eee;
  }
  .top-banner {
    background: #fff3cd;
    border-left: 5px solid #ffc107;
    padding: 16px 20px;
    border-radius: 8px;
    margin-bottom: 24px;
    font-weight: 500;
    color: #856404;
  }
  .top-banner strong { color: #d39e00; }
  .detail-content {
    display: none;
    margin-top: 24px;
    padding: 24px 20px 20px 20px;
    border: 1px solid #dee2e6;
    border-radius: 12px;
    background: #fcfcfd;
  }
  .detail-content.active { display: block; }
  .sub-item {
    border: 1px solid #e9ecef;
    border-radius: 8px;
    margin-bottom: 12px;
    overflow: hidden;
  }
  .sub-header {
    background: #f1f3f5;
    padding: 12px 18px;
    cursor: pointer;
    font-weight: 600;
    display: flex;
    justify-content: space-between;
    align-items: center;
    user-select: none;
  }
  .sub-header:hover { background: #e9ecef; }
  .sub-header .arrow {
    transition: transform 0.3s;
    font-size: 0.8rem;
    color: #6c757d;
  }
  .sub-header.active .arrow { transform: rotate(180deg); }
  .sub-body {
    display: none;
    padding: 16px 18px 18px 18px;
    background: #ffffff;
  }
  .sub-body.open { display: block; }
  .sub-body h5 {
    color: #0d6efd;
    font-size: 0.95rem;
    margin-bottom: 12px;
    border-bottom: 1px solid #e9ecef;
    padding-bottom: 8px;
  }
  .step-img-wrapper { margin-bottom: 12px; text-align: center; }
  .step-img {
    width: 100%;
    height: 140px;
    object-fit: contain;
    display: block;
    background: #ffffff;
    border-radius: 6px;
    border: 1px solid #e9ecef;
    padding: 4px;
    box-sizing: border-box;
  }
  .step-text {
    text-align: center;
    font-weight: 500;
    font-size: 0.85rem;
    color: #212529;
    padding: 4px 2px 0 2px;
  }
  .step-number {
    display: inline-block;
    background: #0d6efd;
    color: #fff;
    border-radius: 50%;
    width: 22px;
    height: 22px;
    line-height: 22px;
    font-size: 0.7rem;
    font-weight: 700;
    text-align: center;
    margin-right: 4px;
  }
  .verification-box {
    margin-top: 18px;
    padding: 12px 16px;
    background: #e7f3ff;
    border-radius: 8px;
    border-left: 4px solid #0d6efd;
  }
  .click-hint { color: #6c757d; font-size: 0.95rem; margin-bottom: 18px; }
  .section-divider { margin: 32px 0 20px 0; border-top: 2px dashed #dee2e6; }
  @media (max-width: 768px) {
    .symptom-image-box { height: 180px; }
    .step-img { height: 110px; }
    .symptom-label { font-size: 0.95rem; padding: 10px; min-height: 50px; }
    .detail-content { padding: 16px 12px 12px 12px; }
    .sub-header { font-size: 0.9rem; padding: 10px 14px; }
    .sub-body { padding: 12px 14px 14px 14px; }
  }
  @media (max-width: 576px) {
    .symptom-image-box { height: 150px; }
    .step-img { height: 90px; }
  }
</style>

<!-- TOP BANNER -->
<div class="top-banner">
  <strong>⚠️ A bird's nest does not always mean a machine problem.</strong>
  Improper cap installation, hooping, stabilizer selection, or digitizing can also cause thread nesting.
</div>

<h2>Select Your Embroidery Scenario</h2>
<p class="click-hint">👇 Click the image below to see the step‑by‑step guide.</p>

<!-- CARDS（已移除 onclick，绑定交由下方脚本处理） -->
<div class="row g-4">
  <div class="col-md-6">
    <div class="symptom-card" data-target="A">
      <div class="symptom-image-box">
        <img src="phenomenon-clothing.jpg" alt="Clothing bird's nest">
      </div>
      <div class="symptom-label">👕 Clothing — Bird's Nest</div>
    </div>
  </div>
  <div class="col-md-6">
    <div class="symptom-card" data-target="B">
      <div class="symptom-image-box">
        <img src="phenomenon-cap.jpg" alt="Cap bird's nest">
      </div>
      <div class="symptom-label">🧢 Caps — Bird's Nest</div>
    </div>
  </div>
</div>

<!-- DETAIL A: CLOTHING -->
<div id="detailA" class="detail-content">
  <h4>🧵 Clothing — Troubleshooting</h4>
  <p><strong>Applies to:</strong> T‑shirts, shirts, sweatshirts, denim, and other garments.</p>
  <div class="sub-item">
    <div class="sub-header" data-sub="A1">
      <span>⚙️ Machine Setup</span><span class="arrow">▾</span>
    </div>
    <div id="subA1" class="sub-body">
      <h5>Threading, Tension &amp; Needle</h5>
      <div class="row">
        <div class="col-6 col-md-4">
          <div class="step-img-wrapper"><img src="clothing-m1.jpg" class="step-img" alt="Threading"></div>
          <p class="step-text"><span class="step-number">1</span>Verify threading path</p>
        </div>
        <div class="col-6 col-md-4">
          <div class="step-img-wrapper"><img src="clothing-m2.jpg" class="step-img" alt="Top tension"></div>
          <p class="step-text"><span class="step-number">2</span>Check top tension</p>
        </div>
        <div class="col-6 col-md-4">
          <div class="step-img-wrapper"><img src="clothing-m3.jpg" class="step-img" alt="Bobbin tension"></div>
          <p class="step-text"><span class="step-number">3</span>Check bobbin tension</p>
        </div>
        <div class="col-6 col-md-4">
          <div class="step-img-wrapper"><img src="clothing-m4.png" class="step-img" alt="Needle"></div>
          <p class="step-text"><span class="step-number">4</span>Needle direction &amp; insertion</p>
        </div>
        <div class="col-6 col-md-4">
          <div class="step-img-wrapper"><img src="clothing-m5.jpg" class="step-img" alt="Replace needle"></div>
          <p class="step-text"><span class="step-number">5</span>Replace if bent/damaged</p>
        </div>
      </div>
    </div>
  </div>


  <div class="sub-item">
    <div class="sub-header" data-sub="A2">
      <span>📦 Material Setup</span><span class="arrow">▾</span>
    </div>
    <div id="subA2" class="sub-body">
      <h5>Hooping &amp; Stabilizer</h5>
      <div class="row">
        <div class="col-6 col-md-4">
          <div class="step-img-wrapper"><img src="clothing-h1.jpg" class="step-img" alt="Hooping"></div>
          <p class="step-text"><span class="step-number">1</span>Hoop taut — no wrinkles</p>
        </div>
        <div class="col-6 col-md-4">
          <div class="step-img-wrapper"><img src="clothing-h2.jpg" class="step-img" alt="Stabilizer"></div>
          <p class="step-text"><span class="step-number">2</span>Correct stabilizer type</p>
        </div>
        <div class="col-6 col-md-4">
          <div class="step-img-wrapper"><img src="clothing-h3.jpg" class="step-img" alt="Stabilizer coverage"></div>
          <p class="step-text"><span class="step-number">3</span>Stabilizer covers full hoop</p>
        </div>
        <div class="col-6 col-md-4">
          <div class="step-img-wrapper"><img src="clothing-h4.png" class="step-img" alt="Needle plate"></div>
          <p class="step-text"><span class="step-number">4</span>Needle plate — no burrs/lint</p>
        </div>
      </div>
    </div>
  </div>

  <div class="sub-item">
    <div class="sub-header" data-sub="A3">
      <span>💻 Digitizing</span><span class="arrow">▾</span>
    </div>
    <div id="subA3" class="sub-body">
      <h5>Design‑related causes</h5>
      <div class="row">
        <div class="col-6 col-md-4">
          <div class="step-img-wrapper"><img src="clothing-d1.png" class="step-img" alt="Density(Replace it with the standard tension test design.)"></div>
          <p class="step-text"><span class="step-number">1</span>Density(Replace it with the standard tension test design.)</p>
        </div>
        <div class="col-6 col-md-4">
          <div class="step-img-wrapper"><img src="clothing-d2.png" class="step-img" alt="Underlay"></div>
          <p class="step-text"><span class="step-number">2</span>Incorrect underlay</p>
        </div>
        <div class="col-6 col-md-4">
          <div class="step-img-wrapper"><img src="clothing-d3.png" class="step-img" alt="Scale the design up or down to the correct size."></div>
          <p class="step-text"><span class="step-number">3</span>Scale the design up or down to the correct size.</p>
        </div>
       </div>
    </div>
  </div>
  <div class="sub-item">
    <div class="sub-header" data-sub="A4">
      <span>🔧 Hardware &amp; Timing</span><span class="arrow">▾</span>
    </div>
    <div id="subA4" class="sub-body">
      <h5>Bobbin Case, Rotary Hook &amp; Timing</h5>
      <div class="row">
        <div class="col-6 col-md-4">
          <div class="step-img-wrapper"><img src="clothing-hw1.jpg" class="step-img" alt="Bobbin case"></div>
          <p class="step-text"><span class="step-number">1</span>Inspect bobbin case</p>
        </div>
        <div class="col-6 col-md-4">
          <div class="step-img-wrapper"><img src="clothing-hw2.jpg" class="step-img" alt="Rotary hook"></div>
          <p class="step-text"><span class="step-number">2</span>Clean rotary hook area</p>
        </div>
        <div class="col-6 col-md-4">
          <div class="step-img-wrapper"><img src="clothing-hw3.jpg" class="step-img" alt="Timing"></div>
          <p class="step-text"><span class="step-number">3</span>Timing at 202° — last resort</p>
        </div>          
      </div>
    </div>
  </div>


  <div class="verification-box">
    <strong>✅ Verification:</strong> Run a test on the same fabric. If the bird's nest disappears, the issue is resolved.
  </div>
</div>

<!-- DETAIL B: CAPS -->
<div id="detailB" class="detail-content">
  <h4>🧢 Caps — Troubleshooting</h4>
  <p><strong>Applies to:</strong> Baseball caps, bucket hats, military caps, and other structured headwear.</p>

  <div class="sub-item">
    <div class="sub-header" data-sub="B1" style="border-left:4px solid #ffc107;">
      <span>🧢 ⭐ Cap Installation</span><span class="arrow">▾</span>
    </div>
    <div id="subB1" class="sub-body">
      <h5>#1 cause — secure the cap properly</h5>
      <div class="row">
        <div class="col-6 col-md-4">
          <div class="step-img-wrapper"><img src="cap-i1.jpg" class="step-img" alt="Cap on driver"></div>
          <p class="step-text"><span class="step-number">1</span>Seated on cap driver</p>
        </div>
        <div class="col-6 col-md-4">
          <div class="step-img-wrapper"><img src="cap-i2.jpg" class="step-img" alt="Cap frame"></div>
          <p class="step-text"><span class="step-number">2</span>Frame installed securely</p>
        </div>
        <div class="col-6 col-md-4">
          <div class="step-img-wrapper"><img src="cap-i3.jpg" class="step-img" alt="Centering"></div>
          <p class="step-text"><span class="step-number">3</span>Cap centered under needle</p>
        </div>
        <div class="col-6 col-md-4">
          <div class="step-img-wrapper"><img src="cap-i4.jpg" class="step-img" alt="Clamping"></div>
          <p class="step-text"><span class="step-number">4</span>Firmly clamped — no movement</p>
        </div>
        <div class="col-6 col-md-4">
          <div class="step-img-wrapper"><img src="cap-i5.jpg" class="step-img" alt="Brim"></div>
          <p class="step-text"><span class="step-number">5</span>Brim positioned correctly</p>
        </div>
      </div>
    </div>
  </div>
  <div class="sub-item">
    <div class="sub-header" data-sub="B2">
      <span>⚙️ Machine Setup</span><span class="arrow">▾</span>
    </div>
    <div id="subB2" class="sub-body">
      <h5>Threading, Tension &amp; Needle</h5>
      <div class="row">
        <div class="col-6 col-md-4">
          <div class="step-img-wrapper"><img src="cap-m1.jpg" class="step-img" alt="Threading"></div>
          <p class="step-text"><span class="step-number">1</span>Verify threading path</p>
        </div>
        <div class="col-6 col-md-4">
          <div class="step-img-wrapper"><img src="cap-m2.jpg" class="step-img" alt="Top tension"></div>
          <p class="step-text"><span class="step-number">2</span>Top tension — slightly tighter</p>
        </div>
        <div class="col-6 col-md-4">
          <div class="step-img-wrapper"><img src="cap-m3.jpg" class="step-img" alt="Bobbin tension"></div>
          <p class="step-text"><span class="step-number">3</span>Bobbin — slightly looser</p>
        </div>
        <div class="col-6 col-md-4">
          <div class="step-img-wrapper"><img src="cap-m4.png" class="step-img" alt="Needle"></div>
          <p class="step-text"><span class="step-number">4</span>Correct needle size</p>
        </div>
      </div>
    </div>
  </div>

  <div class="sub-item">
    <div class="sub-header" data-sub="B3">
      <span>💻 Digitizing</span><span class="arrow">▾</span>
    </div>
    <div id="subB3" class="sub-body">
      <h5>Design‑related causes for caps</h5>
      <div class="row">
        <div class="col-6 col-md-4">
          <div class="step-img-wrapper"><img src="cap-d1.jpg" class="step-img" alt="Density"></div>
          <p class="step-text"><span class="step-number">1</span>Density too high</p>
        </div>
        <div class="col-6 col-md-4">
          <div class="step-img-wrapper"><img src="cap-d2.png" class="step-img" alt="Underlay"></div>
          <p class="step-text"><span class="step-number">2</span>Incorrect underlay</p>
        </div>
        <div class="col-6 col-md-4">
          <div class="step-img-wrapper"><img src="cap-d3.png" class="step-img" alt="Design size"></div>
          <p class="step-text"><span class="step-number">3</span>Hat embroidery should stitch from the center outward to both sides.</p>
        </div>
      </div>
    </div>
  </div>

  <div class="sub-item">
    <div class="sub-header" data-sub="B4">
      <span>🔧 Hardware &amp; Timing</span><span class="arrow">▾</span>
    </div>
    <div id="subB4" class="sub-body">
      <h5>Bobbin Case, Rotary Hook &amp; Timing</h5>
      <div class="row">
        <div class="col-6 col-md-4">
          <div class="step-img-wrapper"><img src="cap-hw1.jpg" class="step-img" alt="Bobbin case"></div>
          <p class="step-text"><span class="step-number">1</span>Inspect bobbin case</p>
        </div>
        <div class="col-6 col-md-4">
          <div class="step-img-wrapper"><img src="cap-hw2.jpg" class="step-img" alt="Rotary hook"></div>
          <p class="step-text"><span class="step-number">2</span>Clean rotary hook area</p>
        </div>
        <div class="col-6 col-md-4">
          <div class="step-img-wrapper"><img src="cap-hw3.jpg" class="step-img" alt="Timing"></div>
          <p class="step-text"><span class="step-number">3</span>Timing at 202° — last resort</p>
        </div>       
      </div>
    </div>
  </div>


  <div class="verification-box">
    <strong>✅ Verification:</strong> Run a test on the same cap. If the bird's nest disappears, the issue is resolved.
  </div>
</div>

<!-- JAVASCRIPT：统一事件绑定，不依赖任何内联 onclick -->
<script>
  (function() {
    // 卡片展开功能
    function toggleDetail(id) {
      var all = document.querySelectorAll('.detail-content');
      all.forEach(function(el) { el.classList.remove('active'); });
      var target = document.getElementById('detail' + id);
      if (target) {
        target.classList.add('active');
        document.querySelectorAll('.sub-body').forEach(function(el) { el.classList.remove('open'); });
        document.querySelectorAll('.sub-header').forEach(function(el) { el.classList.remove('active'); });
        setTimeout(function() { target.scrollIntoView({ behavior: 'smooth', block: 'start' }); }, 150);
      }
    }

    // 子项折叠功能
    function toggleSub(id) {
      var body = document.getElementById('sub' + id);
      var header = body ? body.previousElementSibling : null;
      if (body && header) {
        body.classList.toggle('open');
        header.classList.toggle('active');
      }
    }
    
    // 页面加载完成后绑定事件
    document.addEventListener('DOMContentLoaded', function() {
      // 绑定卡片点击
      var cards = document.querySelectorAll('.symptom-card');
      cards.forEach(function(card) {
        card.addEventListener('click', function(e) {
          var targetId = this.getAttribute('data-target');
          if (targetId) {
            toggleDetail(targetId);
          }
        });
      });
    
      // 绑定子项点击
      var subHeaders = document.querySelectorAll('.sub-header');
      subHeaders.forEach(function(header) {
        header.addEventListener('click', function(e) {
          var subId = this.getAttribute('data-sub');
          if (subId) {
            toggleSub(subId);
          }
        });
      });
    });
  })();
</script>

<hr class="section-divider">

<h2>Quick Summary</h2>
<div class="row">
  <div class="col-md-6">
    <h5>👕 Clothing — Check Order</h5>
    <ol>
      <li>Machine Setup (threading, tension, needle)</li>
      <li>Material Setup (hooping, stabilizer)</li>
      <li>Digitizing (density, underlay, pull comp)</li>
      <li>Hardware (bobbin case, hook, timing)</li>
    </ol>
  </div>
  <div class="col-md-6">
    <h5>🧢 Caps — Check Order</h5>
    <ol>
      <li><strong>Cap Installation (most critical!)</strong></li>
      <li>Machine Setup (threading, tension, needle)</li>
      <li>Digitizing (density, underlay, stitch direction)</li>
      <li>Hardware (bobbin case, hook, timing)</li>
    </ol>
  </div>
</div>