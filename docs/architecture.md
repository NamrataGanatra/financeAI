# Finance AI Technical Architecture

## System Architecture Diagram

```mermaid
graph TB
    subgraph "Frontend Layer"
        UI[User Interface]
        style UI fill:#e1bee7,stroke:#6B46C1
        subgraph "UI Components"
            RC[React Components]
            TC[TailwindCSS Styling]
            SC[Shadcn/UI Components]
            CH[Chart Components]
        end
        style RC fill:#e1bee7,stroke:#6B46C1
        style TC fill:#e1bee7,stroke:#6B46C1
        style SC fill:#e1bee7,stroke:#6B46C1
        style CH fill:#e1bee7,stroke:#6B46C1
    end

    subgraph "Application Layer"
        NJ[Next.js 14]
        style NJ fill:#d1c4e9,stroke:#6B46C1
        subgraph "Core Features"
            TH[Theme System]
            FH[File Handling]
            VZ[Data Visualization]
        end
        style TH fill:#d1c4e9,stroke:#6B46C1
        style FH fill:#d1c4e9,stroke:#6B46C1
        style VZ fill:#d1c4e9,stroke:#6B46C1
    end

    subgraph "API Layer"
        ER[Edge Runtime]
        AR[API Routes]
        style ER fill:#b39ddb,stroke:#6B46C1
        style AR fill:#b39ddb,stroke:#6B46C1
    end

    subgraph "External Services"
        CL[Claude AI]
        style CL fill:#9575cd,stroke:#6B46C1
    end

    UI --> RC
    RC --> TC
    RC --> SC
    RC --> CH
    
    UI --> NJ
    NJ --> TH
    NJ --> FH
    NJ --> VZ
    
    NJ --> ER
    ER --> AR
    AR --> CL

```

## Technology Stack Details

### Frontend
- **Framework**: Next.js 14 (React 18)
- **Styling**: 
  - TailwindCSS
  - Shadcn/UI Components
  - Custom theme system with dark/light mode
- **Data Visualization**: 
  - Recharts library
  - Custom chart components
- **State Management**: React Hooks
- **File Handling**:
  - PDF.js for PDF processing
  - Base64 encoding for images
  - Text file processing

### Backend
- **Runtime**: Edge Runtime
- **API Routes**: Next.js API Routes
- **AI Integration**: Anthropic Claude API
  - Claude 3 Haiku
  - Claude 3.5 Sonnet

### Development Tools
- **Language**: TypeScript
- **Package Manager**: npm
- **Development Environment**:
  - ESLint
  - PostCSS
  - Environment variables

### Key Features
1. **Intelligent Analysis**
   - Financial data processing
   - Natural language understanding
   - Automated chart generation

2. **File Support**
   - CSV data
   - PDF documents
   - Images
   - Text/Code files

3. **Visualization Types**
   - Line Charts
   - Bar Charts
   - Multi-Bar Charts
   - Area Charts
   - Stacked Area Charts
   - Pie Charts

4. **UI/UX**
   - Responsive design
   - Dark/Light theme
   - Interactive chat interface
   - Real-time updates
   - Toast notifications
   - Loading states

## Security Features
- Environment variable protection
- API key security
- Edge runtime isolation
- Client-side file processing
- Secure data transmission 