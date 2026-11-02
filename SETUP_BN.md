# GitHub Profile Setup — mrmshafi

এই প্যাকেজে রেফারেন্সের burgundy/cream design, animated personalized banner, typing text, skill icons, দুই কলামের repository showcase, live statistics, 3D contribution widget ও snake workflow আছে। নিজের তথ্য ও repository সংখ্যা আলাদা হওয়ায় এটি রেফারেন্সের ব্যক্তিগত তথ্যসহ pixel-exact copy নয়।

## যেভাবে বসাবেন

1. ZIP extract করুন।
2. https://github.com/mrmshafi/mrmshafi খুলুন।
3. README.md-এর বর্তমান লেখা এই প্যাকেজের README.md দিয়ে replace করুন।
4. Add file → Upload files দিয়ে assets folder আপলোড করুন। Folder-এর ভেতরের files নয়, assets folder-সহ আপলোড করবেন। README ও assets একই repository root-এ থাকবে।
5. Add file → Create new file চাপুন। Filename লিখুন `.github/workflows/profile-snake.yml`। প্যাকেজের একই ফাইলের সব লেখা paste করে Commit changes করুন। এই পদ্ধতিতে hidden .github folder বাদ পড়ার সমস্যা থাকবে না।
6. Actions tab-এ Profile Snake workflow খুলুন। প্রয়োজন হলে Actions enable করুন। Run workflow → main → Run workflow চাপুন।
7. Workflow সফল হলে assets/github-snake.svg আসল contribution animation দিয়ে replace হবে। এরপর প্রতিদিন আনুমানিক সকাল ৬টায় বাংলাদেশ সময় স্বয়ংক্রিয়ভাবে আপডেট হবে। GitHub schedule দেরি করতে পারে।
8. Profile খুলে দেখুন: https://github.com/mrmshafi

Snake workflow-এর জন্য আলাদা personal access token লাগবে না। এটি built-in GITHUB_TOKEN ব্যবহার করে এবং শুধু generated SVG commit করে। Repository rules সরাসরি bot push আটকালেই workflow fail করতে পারে; আগে Actions run-এর error দেখুন।

## আপনার তথ্য অনুযায়ী পরিবর্তন

- পরিচিতি ও skill list: README.md
- নামের banner: assets/mamun-motion-header.svg
- Project covers: assets/*repository-name*.svg
- প্রকৃত project screenshots পেলে cover image-গুলোর জায়গায় সেগুলো বসাতে পারবেন। এখনকার cover-গুলো artwork, screenshot নয়।
- telemedicine-app repository বর্তমানে খালি, তাই সেটিকে completed app বলা হয়নি।
- ব্যক্তিগত LinkedIn, email, চাকরি, university বা awards নিশ্চিত করা হয়নি বলে যোগ করা হয়নি।
- GitHub-এর বাম পাশের profile photo, bio এবং pinned repositories README দিয়ে বদলায় না; Edit profile / Customize your pins থেকে বদলাতে হবে।
- External stats widgets provider বন্ধ বা rate-limited হলে ছবি নাও দেখা যেতে পারে।

## যাচাই

SVG XML, local image paths, workflow YAML ও ZIP contents যাচাই করা হয়েছে। GitHub-এ upload, remote rendering এবং scheduled workflow execution এখনও করা হয়নি।
