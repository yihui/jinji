---
title: 无题
author: 金吉
date: '2021-08-18'
slug: ''
categories:
  - '2021'
tags: []
---


<script>
(function() {
  var m = document.querySelector('.main');
  if (!document.createTreeWalker) {
    m.style.display = 'none'; return;
  }
  function textNodes(el) {
    var n, a = [], walk = document.createTreeWalker(el,
NodeFilter.SHOW_TEXT, null, false);
    while(n = walk.nextNode()) a.push(n);
    return a;
  }
  function manipulate(str) {
    var res = [], n;
    for (var i = 0; i < str.length; i++) {
      n = str.charCodeAt(i) - 1;
      if (n < 0) n = 65535;
      res.push(String.fromCharCode(n));
    }
    return res.join('');
  }
  textNodes(m).forEach(function(el) {
    el.textContent = manipulate(el.textContent);
  });
})();
</script>


