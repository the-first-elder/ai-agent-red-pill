# The RedPill AI Agent Template

The RedPill AI Agent template is a **MINIMAL** template designed to help you build an AI Agent that can be hosted on Phala Network's decentralized hosting protocol.

## Getting Started

### Prepare

1. **Install dependencies**

   ```bash
   npm install
   ```

### Testing Locally

1. **Create a `.env` file** and add your RedPill API Key:

   ```bash
   cp .env.example .env
   ```

2. **Get an OpenAI API Key from RedPill**

   - Visit the [RedPill Dashboard](https://red-pill.ai/dashboard) to claim your OpenAI API Key.
   - Swap some ETH for wGPT at [Uniswap](https://app.uniswap.org/explore/tokens/base/0x74F62Bc1961028C22b8080961c6534f4eDD49D6C).

   Video guide: [Watch here](https://youtu.be/ZoJwbLNhbWE).

3. **In the `.env` file**, replace `YOUR_OPENAI_KEY` with your API Key:

   ```bash
   OPENAI_API_KEY="YOUR_OPENAI_KEY"
   ```

### Build your Agent

```bash
npm run build
```

### Test your Agent locally

```bash
npm run test
```

### Expected Test Results

After running the tests, you should see the expected output confirming that your AI Agent is working correctly.

```bash
INPUT: {"method":"GET","path":"/ipfs/QmVHbLYhhYA5z6yKpQr4JWr3D54EhbSsh7e7BFAAyrkkMf","queries":{"chatQuery":["Who are you?"],"openAiModel":["gpt-4o"]},"secret":{"openaiApiKey":"YOUR_OPENAI_KEY"},"headers":{}}

GET RESULT: {
  status: 200,
  body: '\n' +
    '    <!DOCTYPE html>\n' +
    '    <html lang="en">\n' +
    '        <head>\n' +
    '            <meta charset="utf-8" />\n' +
    '            <title>AI Agent Contract Demo UI</title>\n' +
    '        </head>\n' +
    '        <body>\n' +
    '            <div align="center">\n' +
    '                <p>"OpenAI AI Agent Contract hosted on <a href="https://github.com/Phala-Network/ai-agent-template-openai">Phala Network</a>, an AI Coprocessor for hosting AI Agents."</p>\n' +
    '                <img src="https://i.imgur.com/8B3igON.png" width="600" alt="AI Agent Contract" />\n' +
    '                <p>I’m an AI language model developed by OpenAI, here to help answer your questions and provide information on a wide range of topics. How can I assist you today?</p>\n' +
    '            </div>\n' +
    '        </body>\n' +
    '    </html>',
  headers: {
    'Content-Type': 'text/html; charset=UTF-8',
    'Access-Control-Allow-Origin': '*'
  }
}
INPUT: {"method":"POST","path":"/ipfs/QmVHbLYhhYA5z6yKpQr4JWr3D54EhbSsh7e7BFAAyrkkMf","queries":{"chatQuery":["When did humans land on the moon?"],"openAiModel":["gpt-4o"]},"secret":{"openaiApiKey":"YOUR_OPENAI_KEY"},"headers":{},"body":{}}
POST RESULT: {
  status: 200,
  body: '\n' +
    '    <!DOCTYPE html>\n' +
    '    <html lang="en">\n' +
    '        <head>\n' +
    '            <meta charset="utf-8" />\n' +
    '            <title>AI Agent Contract Demo UI</title>\n' +
    '        </head>\n' +
    '        <body>\n' +
    '            <div align="center">\n' +
    '                <p>"OpenAI AI Agent Contract hosted on <a href="https://github.com/Phala-Network/ai-agent-template-openai">Phala Network</a>, an AI Coprocessor for hosting AI Agents."</p>\n' +
    '                <img src="https://i.imgur.com/8B3igON.png" width="600" alt="AI Agent Contract" />\n' +
    `                <p>Humans first landed on the moon on July 20, 1969, during NASA's Apollo 11 mission. The astronauts who made this historic journey were Neil Armstrong, who became the first person to walk on the moon, and Edwin "Buzz" Aldrin, who followed shortly after. Michael Collins, the third member of the Apollo 11 crew, remained in lunar orbit aboard the Command Module. Armstrong's famous words as he stepped onto the lunar surface were, "That's one small step for man, one giant leap for mankind."</p>\n` +
    '            </div>\n' +
    '        </body>\n' +
    '    </html>',
  headers: {
    'Content-Type': 'text/html; charset=UTF-8',
    'Access-Control-Allow-Origin': '*'
  }
}

To test in the SideVM playground go to https://phat.phala.network/contracts/view/0xf0a398600f02ea9b47a86c59aed61387e450e2a99cb8b921cd1d46f734e45409

Connect you polkadot.js account and select 'run_js' with the parameters:
- engine: SidevmQuickJSWithPolyfill
- js_code: Source code text of dist/index.ts
- args: {"method":"GET","path":"/ipfs/QmVHbLYhhYA5z6yKpQr4JWr3D54EhbSsh7e7BFAAyrkkMf","queries":{"chatQuery":["Who are you?"],"openAiModel":["gpt-4o"]},"secret":{"openaiApiKey":"YOUR_OPENAI_KEY"},"headers":{}}
Watch video here for to see the visual steps of testing in Sidevm playground: https://www.youtube.com/watch?v=fNqNeLfFFME

Make sure to replace queries and secret with your values compatible with your AI Agent Contract.
```
