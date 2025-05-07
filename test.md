<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
    <title>Mobile Controller</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        .arrow-btn {
            position: relative;
            min-width: 60px;
            min-height: 60px;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.2s;
        }
        
        .forward::after {
            content: '';
            position: absolute;
            top: -15px;
            border: 8px solid transparent;
            border-bottom-color: #3B82F6;
        }

        .backward::after {
            content: '';
            position: absolute;
            bottom: -15px;
            border: 8px solid transparent;
            border-top-color: #3B82F6;
        }

        .left::after {
            content: '';
            position: absolute;
            left: -15px;
            border: 8px solid transparent;
            border-right-color: #3B82F6;
        }

        .right::after {
            content: '';
            position: absolute;
            right: -15px;
            border: 8px solid transparent;
            border-left-color: #3B82F6;
        }
    </style>
</head>
<body class="bg-gray-800 h-screen">
    <div class="container mx-auto px-4 h-full flex items-center justify-center">
        <div class="w-full max-w-md h-[500px] bg-gray-900 rounded-2xl p-6 flex gap-6">
            <!-- Directional Controls -->
            <div class="flex-1 flex items-center justify-center">
                <div class="relative w-48 h-48">
                    <!-- Forward -->
                    <button onclick="moveForward()" 
                            class="arrow-btn forward absolute top-0 left-1/2 -translate-x-1/2 bg-blue-500 hover:bg-blue-600 active:bg-blue-700 rounded-t-lg text-white font-bold text-xl">
                        F
                    </button>
                    
                    <!-- Backward -->
                    <button onclick="moveBackward()" 
                            class="arrow-btn backward absolute bottom-0 left-1/2 -translate-x-1/2 bg-blue-500 hover:bg-blue-600 active:bg-blue-700 rounded-b-lg text-white font-bold text-xl">
                        B
                    </button>
                    
                    <!-- Left -->
                    <button onclick="moveLeft()" 
                            class="arrow-btn left absolute left-0 top-1/2 -translate-y-1/2 bg-blue-500 hover:bg-blue-600 active:bg-blue-700 rounded-l-lg text-white font-bold text-xl">
                        L
                    </button>
                    
                    <!-- Right -->
                    <button onclick="moveRight()" 
                            class="arrow-btn right absolute right-0 top-1/2 -translate-y-1/2 bg-blue-500 hover:bg-blue-600 active:bg-blue-700 rounded-r-lg text-white font-bold text-xl">
                        R
                    </button>
                </div>
            </div>
