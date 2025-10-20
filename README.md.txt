services:
  - type: web
    name: bot-ofertas-telegram
    env: python
    plan: free
    buildCommand: "pip install -r requirements.txt"
    startCommand: "python bot_ofertas.py"
    envVars:
      - key: TELEGRAM_TOKEN
        sync: false
      - key: TELEGRAM_CHANNEL  
        sync: false
      - key: AMAZON_TAG
        sync: false