# Azaii
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ajay Kumar Yasalapu - Personal Profile</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.6.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Product+Sans:wght@400;500&display=swap');
        
        body {
            font-family: 'Product Sans', system-ui, sans-serif;
        }
        
        .google-logo span:nth-child(1) { color: #4285f4; }
        .google-logo span:nth-child(2) { color: #ea4335; }
        .google-logo span:nth-child(3) { color: #fbbc05; }
        .google-logo span:nth-child(4) { color: #4285f4; }
        .google-logo span:nth-child(5) { color: #34a853; }
        .google-logo span:nth-child(6) { color: #ea4335; }
        
        .search-box {
            box-shadow: 0 1px 6px rgba(32, 33, 36, 0.28);
            transition: box-shadow 0.2s;
        }
        .search-box:hover {
            box-shadow: 0 4px 12px rgba(32, 33, 36, 0.3);
        }
        
        .profile-img {
            border: 4px solid #fff;
            box-shadow: 0 4px 20px rgba(0,0,0,0.15);
            transition: transform 0.3s;
        }
        .profile-img:hover {
            transform: scale(1.05);
        }
    </style>
</head>
<body class="bg-white text-[#202124] min-h-screen">

    <!-- Top Navigation -->
    <nav class="flex justify-end items-center gap-6 px-6 py-4 text-sm">
        <a href="#" class="hover:underline">Gmail</a>
        <a href="#" class="hover:underline">Images</a>
        <div class="w-10 h-10 bg-gray-100 hover:bg-gray-200 rounded-full flex items-center justify-center cursor-pointer">
            <i class="fa-solid fa-grid text-xl"></i>
        </div>
        <div class="w-9 h-9 bg-blue-600 text-white rounded-full flex items-center justify-center font-medium cursor-pointer">AK</div>
    </nav>

    <!-- Main Content -->
    <div class="max-w-2xl mx-auto pt-24 px-4 text-center">
        
        <!-- Google-style Logo -->
        <div class="flex justify-center mb-8">
            <h1 class="google-logo text-8xl font-normal tracking-tighter">
                <span>A</span><span>J</span><span>A</span><span>Y</span>
            </h1>
        </div>

        <!-- Your Latest Photo -->
        <div class="flex justify-center mb-6">
            <img src="/home/workdir/attachments/1000012007" 
                 alt="Ajay Kumar Yasalapu"
                 class="profile-img w-52 h-52 object-cover rounded-full">
        </div>

        <h2 class="text-3xl font-medium mb-1">Ajay Kumar Yasalapu</h2>
        <p class="text-gray-600 mb-10">Born • 03 December 2007 • 18 Years</p>

        <!-- Information Card -->
        <div class="search-box bg-white border border-gray-300 rounded-3xl py-6 px-8 max-w-xl mx-auto mb-10">
            <div class="flex items-center gap-4 mb-6 border-b pb-5">
                <i class="fa-solid fa-user text-[#4285f4] text-3xl"></i>
                <div class="text-left">
                    <p class="font-medium text-lg">Full Name</p>
                    <p class="text-xl">AJAY KUMAR YASALAPU</p>
                </div>
            </div>

            <div class="grid grid-cols-2 gap-8 text-left">
                <div>
                    <p class="text-sm text-gray-500 mb-2">Education</p>
                    <p class="font-medium">Bhargavi Vidya Mandir School</p>
                    <p class="text-sm text-gray-600">Nursery to 10th Class</p>
                    <p class="font-medium mt-4">Sri Chaitanya Junior College</p>
                </div>
                
                <div>
                    <p class="text-sm text-gray-500 mb-2">Connect</p>
                    <a href="https://instagram.com/_azaiiiii" target="_blank" 
                       class="flex items-center gap-3 hover:text-pink-600 transition-colors mb-3">
                        <i class="fa-brands fa-instagram text-2xl"></i>
                        <span class="font-medium">@_azaiiiii</span>
                    </a>
                    <div class="flex items-center gap-3">
                        <i class="fa-solid fa-gamepad text-2xl text-green-600"></i>
                        <span class="font-medium">DARINGPANTHER</span>
                    </div>
                </div>
            </div>
        </div>

        <!-- Google Style Buttons -->
        <div class="flex justify-center gap-4">
            <button onclick="alert('✅ Identity Verified Successfully!')" 
                    class="px-8 py-3 bg-[#f8f9fa] hover:bg-gray-200 rounded-md text-sm font-medium border border-gray-300">
                Verify Profile
            </button>
            <button onclick="window.scrollTo({top: document.body.scrollHeight, behavior: 'smooth'})" 
                    class="px-8 py-3 bg-[#f8f9fa] hover:bg-gray-200 rounded-md text-sm font-medium border border-gray-300">
                View More
            </button>
        </div>
    </div>

    <!-- Footer -->
    <footer class="fixed bottom-0 w-full bg-[#f2f2f2] py-4 text-sm text-gray-600 border-t">
        <div class="max-w-5xl mx-auto px-8 flex flex-col md:flex-row justify-between items-center gap-4 text-center">
            <div>Personal Digital Identity • 2026</div>
            <div class="flex gap-6">
                <a href="https://instagram.com/_azaiiiii" target="_blank" class="hover:underline">Instagram</a>
                <a href="#" class="hover:underline">BGMI</a>
            </div>
        </div>
    </footer>

    <script>
        // Hover effect on image
        const img = document.querySelector('.profile-img');
        img.addEventListener('mousemove', (e) => {
            const rect = img.getBoundingClientRect();
            const x = (e.clientX - rect.left) / rect.width - 0.5;
            const y = (e.clientY - rect.top) / rect.height - 0.5;
            img.style.transform = `perspective(800px) rotateX(\( {y * -8}deg) rotateY( \){x * 12}deg) scale(1.05)`;
        });
        img.addEventListener('mouseleave', () => {
            img.style.transform = 'scale(1)';
        });
    </script>
</body>
</html>
