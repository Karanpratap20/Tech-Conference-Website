<script>
    import { onMount } from "svelte";

    let days = "00", hours = "00", minutes = "00", seconds = "00";

    const deadline = new Date(2025, 2, 7, 23, 59, 59).getTime();

    function updateCountdown() {
        const now = new Date().getTime();
        const distance = deadline - now;

        if (distance < 0) {
            days = hours = minutes = seconds = "00";
            return;
        }

        days = String(Math.floor(distance / (1000 * 60 * 60 * 24))).padStart(2, "0");
        hours = String(Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60))).padStart(2, "0");
        minutes = String(Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60))).padStart(2, "0");
        seconds = String(Math.floor((distance % (1000 * 60)) / 1000)).padStart(2, "0");
    }

    onMount(() => {
        updateCountdown();
        const interval = setInterval(updateCountdown, 1000);
        return () => clearInterval(interval);
    });
</script>

<style>
    .countdown-container {
        text-align: center;
        max-width: 350px;
        margin: 5px;
    }

    .countdown-timer {
        display: flex;
        justify-content: center;
        gap: 10px;
        margin-bottom: 10px;
    }

    .countdown-item {
        background: #eef2ff;
        border-radius: 50%;
        width: 70px;
        height: 70px;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        font-weight: bold;
        font-size: 18px;
        color: #333;
        box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    }

    .countdown-label {
        font-size: 12px;
        color: #666;
    }

    .buy-button {
        background: linear-gradient(to right, #a78bfa, #7c3aed);
        color: white;
        border: none;
        padding: 12px 24px;
        font-size: 18px;
        font-weight: bold;
        border-radius: 8px;
        cursor: pointer;
        margin-top: 15px;
        transition: 0.3s;
    }

    .buy-button:hover {
        background: #7c3aed;
    }
</style>

<div class="countdown-container">
    <div class="countdown-timer">
        <div class="countdown-item">
            <span>{days}</span>
            <span class="countdown-label">Days</span>
        </div>
        <div class="countdown-item">
            <span>{hours}</span>
            <span class="countdown-label">Hours</span>
        </div>
        <div class="countdown-item">
            <span>{minutes}</span>
            <span class="countdown-label">Minutes</span>
        </div>
        <div class="countdown-item">
            <span>{seconds}</span>
            <span class="countdown-label">Seconds</span>
        </div>
    </div>
    <button class="buy-button">Get your slot now</button>
</div>
