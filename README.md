- 👋 Hi, I’m @Navin-vidyarthi
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
Navin-vidyarthi/Navin-vidyarthi is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
CopilotKit
Docs
GitHub
Discord

Search documentation…

Sign up to Copilot Cloud
Getting Started
What is CopilotKit?
Quickstart: Chatbot
CoAgents (Early Access)
Introduction to CoAgents
Getting Started
Advanced Usage
Features
Demo: Perplexity Clone
Tutorial: Todo List Copilot
Overview
Step 1: Checkout the repo
Step 2: Setup CopilotKit
Step 3: Copilot Readable State
Step 4: Copilot Actions
Next Steps
Tutorial: Textarea Autocomplete
Overview
Step 1: Checkout the repo
Step 2: Setup CopilotKit
Step 3: Copilot Textarea
Step 4: Copilot Readable State
Next Steps

Concepts
Generative UI
Self Hosting
LLM Providers
Agents (LangChain)
Customize Look & Feel

Reference

Components
All Chat Components
<CopilotChat />
<CopilotPopup />
Install Dependencies
Usage
Properties
<CopilotSidebar />
Others
<CopilotKit />
<CopilotTextarea />

Hooks

Classes
Contributing
Code Contributions
How To Contribute
Advanced: Package Linking
Documentation Contributions
Extras
Anonymous Telemetry
Reference
Components
<CopilotPopup />
<CopilotPopup />


A chatbot popup component for the CopilotKit framework. The component allows for a high degree of customization through various props and custom CSS.

See CopilotSidebar for a sidebar version of this component.

Install Dependencies
This component is part of the @copilotkit/react-ui package.

npm install @copilotkit/react-core @copilotkit/react-ui


Usage
import { CopilotPopup } from "@copilotkit/react-ui";
 
<CopilotPopup
  labels={{
    title: "Your Assistant",
    initial: "Hi! 👋 How can I assist you today?",
  }}
/>


Look & Feel
By default, CopilotKit components do not have any styles. You can import CopilotKit’s stylesheet at the root of your project:

...
export function YourRootComponent() {
  return (
    <CopilotKit>
      ...
    </CopilotKit>
  );
}


For more information about how to customize the styles, check out the Customize Look & Feel guide.

Properties
instructions
string
Custom instructions to be added to the system message. Use this property to provide additional context or guidance to the language model, influencing its responses. These instructions can include specific directions, preferences, or criteria that the model should consider when generating its output, thereby tailoring the conversation more precisely to the user’s needs or the application’s requirements.

onInProgress
(inProgress: boolean) => void
A callback that gets called when the in progress state changes.

onSubmitMessage
(message: string) => void | Promise<void>
A callback that gets called when a new message it submitted.

icons
CopilotChatIcons
Icons can be used to set custom icons for the chat window.

labels
CopilotChatLabels
Labels can be used to set custom labels for the chat window.

makeSystemMessage
SystemMessageFunction
A function that takes in context string and instructions and returns the system message to include in the chat request. Use this to completely override the system message, when providing instructions is not enough.

showResponseButton
boolean
Default: "true"
Whether to show the response button.

Messages
React.ComponentType<MessagesProps>
A custom Messages component to use instead of the default.

Input
React.ComponentType<InputProps>
A custom Input component to use instead of the default.

ResponseButton
React.ComponentType<ResponseButtonProps>
A custom ResponseButton component to use instead of the default.

className
string
A class name to apply to the root element.

children
React.ReactNode
Children to render.

defaultOpen
boolean
Default: "false"
Whether the chat window should be open by default.

clickOutsideToClose
boolean
Default: "true"
If the chat window should close when the user clicks outside of it.

hitEscapeToClose
boolean
Default: "true"
If the chat window should close when the user hits the Escape key.

shortcut
string
Default: "'/'"
The shortcut key to open the chat window. Uses Command-[shortcut] on a Mac and Ctrl-[shortcut] on Windows.

onSetOpen
(open: boolean) => void
A callback that gets called when the chat window opens or closes.

Window
React.ComponentType<WindowProps>
A custom Window component to use instead of the default.

Button
React.ComponentTy


pe<ButtonProps>
A custom Button component to use instead of the default.

Header
React.ComponentType<HeaderProps>
A custom Header component to use instead of the default.

<CopilotChat />
<CopilotSidebar />
