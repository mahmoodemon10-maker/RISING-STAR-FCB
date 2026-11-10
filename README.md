# RISING STAR FCB – সেটআপ

1. console.firebase.google.com → নতুন Project → Web app (</>) যোগ করুন → config কপি করে index.html-এর `firebaseConfig`-এ বসান।
2. Authentication → Sign-in method → **Google** ও **Phone** চালু করুন। Settings → Authorized domains-এ আপনার সাইটের ডোমেইন আছে কিনা দেখুন।
3. Firestore Database তৈরি করুন, তারপর Rules ট্যাবে firestore.rules-এর লেখা পেস্ট করে Publish করুন।
4. প্রথমবার নিজে লগইন করুন। Authentication → Users থেকে আপনার UID কপি করুন।
   Firestore → collection `roles` → Document ID = আপনার UID → field `role` (string) = `admin`।
   ম্যানেজারের জন্য একইভাবে `role` = `manager`।
5. GitHub-এ এই ফোল্ডার আপলোড করুন। হোস্ট করতে: `npm i -g firebase-tools && firebase login && firebase init hosting && firebase deploy`
   (বা GitHub Pages ব্যবহার করুন; তখন Authorized domains-এ সেই ডোমেইন যোগ করুন।)
6. খেলোয়াড়ের ইমেইল/ফোন অ্যাডমিন প্যানেলে যেভাবে দিয়েছেন, সেই ইমেইল/ফোনে লগইন করলেই "আমার কার্ড"-এ নিজের কার্ড দেখা যাবে।
