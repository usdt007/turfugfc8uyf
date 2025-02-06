<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Open Tabs for Direct Link</title>
</head>
<body>
  <!-- আপনার ডিরেক্ট লিংক -->
  <a href="#" onclick="openDirectLinkTabs()">Click Here</a>

  <script>
    function openDirectLinkTabs() {
      // আপনার ডিরেক্ট লিংক
      const mainLink = "https://mowcoordinateegypt.com/h99fyprj80?key=c525c0286ab99008d5d9f28d67520932";
      
      // ৪টি নতুন ট্যাব লিংক
      const tabs = [];

      // ৪টি ট্যাব ওপেন করুন
      for (let i = 0; i < 4; i++) {
        let newTab = window.open(mainLink, "_blank");
        tabs.push(newTab);
      }

      // ৫ সেকেন্ড পর ট্যাবগুলো বন্ধ হয়ে যাবে
      setTimeout(() => {
        tabs.forEach(tab => {
          if (tab && !tab.closed) {
            tab.close();  // ট্যাব বন্ধ করে দেওয়া হবে
          }
        });
      }, 5000);  // ৫ সেকেন্ড পর বন্ধ হয়ে যাবে
    }
  </script>
</body>
</html>
