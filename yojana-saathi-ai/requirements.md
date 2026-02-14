# YojanaSaathi AI - Requirements Document

## 1. Introduction

YojanaSaathi AI is a citizen-first intelligent platform designed to bridge the gap between Indian citizens and government welfare schemes. Acting as "Google Maps for Government Schemes" or "ChatGPT for Public Services", the platform leverages artificial intelligence, natural language processing, and optical character recognition to simplify scheme discovery, eligibility assessment, and application processes.

The platform aims to democratize access to government benefits by providing personalized recommendations, multilingual support, and end-to-end application guidance, particularly targeting underserved rural populations and digitally disadvantaged citizens.

## 2. Problem Statement

### 2.1 India Context

India operates over 1,000+ central and state government schemes across sectors including agriculture, education, healthcare, employment, and social welfare. Despite significant government investment, scheme utilization remains critically low due to:

- **Awareness Gap**: Citizens, especially in rural areas, are unaware of schemes they qualify for
- **Information Fragmentation**: Scheme details scattered across multiple government portals and departments
- **Complex Eligibility Criteria**: Difficult-to-understand requirements and documentation needs
- **Language Barriers**: Most information available only in English or Hindi, excluding regional language speakers
- **Digital Divide**: Limited digital literacy and internet access in rural communities
- **Application Complexity**: Cumbersome multi-step processes with unclear documentation requirements
- **Lack of Personalization**: No centralized system to match citizen profiles with relevant schemes
- **Fraud and Duplication**: Multiple applications and fraudulent claims drain resources

### 2.2 Rural Challenges

Rural citizens face additional barriers:
- Limited access to government offices and information centers
- Low literacy rates making document comprehension difficult
- Lack of awareness about required documents
- No guidance on application tracking and follow-up
- Dependency on middlemen who exploit information asymmetry

## 3. Objectives

### 3.1 Primary Objectives

- **O-01**: Provide AI-powered personalized scheme recommendations based on citizen profile data
- **O-02**: Enable multilingual access through NLP chatbot and voice assistant capabilities
- **O-03**: Simplify document submission through OCR-based automatic data extraction
- **O-04**: Generate smart, personalized document checklists for each scheme application
- **O-05**: Detect and prevent fraudulent and duplicate applications
- **O-06**: Provide end-to-end application guidance and real-time tracking

### 3.2 Secondary Objectives

- **O-07**: Increase scheme awareness and utilization rates, particularly in rural areas
- **O-08**: Reduce application processing time and administrative burden
- **O-09**: Create a unified platform aggregating central and state government schemes
- **O-10**: Build trust in government services through transparency and ease of use

## 4. Scope of the System

### 4.1 In Scope

- AI-based scheme recommendation engine using citizen profile matching
- Multilingual NLP chatbot for scheme queries and guidance
- Voice assistant with speech-to-text and text-to-speech capabilities
- OCR engine for extracting data from Aadhaar cards, land records, bank passbooks, and income certificates
- Smart document checklist generation based on scheme requirements
- Fraud detection system identifying duplicate applications and anomalies
- Application tracking dashboard with status updates
- User profile management with secure data storage
- Integration with government scheme databases (simulated for hackathon)
- Mobile-responsive web interface

### 4.2 Out of Scope

- Direct integration with live government payment systems
- Physical document verification and biometric authentication
- Actual scheme disbursement and fund transfer
- Government official backend portal (focus on citizen-facing features)
- Blockchain-based verification (future enhancement)
- Complete offline mobile application (web-first approach)

## 5. Functional Requirements

### 5.1 User Registration and Profile Management

**FR-01**: The system shall allow users to register using mobile number with OTP verification

**FR-02**: The system shall collect and store user profile data including:
- Personal details (name, age, gender, marital status)
- Location (state, district, village/city, pin code)
- Category (General, SC, ST, OBC, EWS)
- Occupation and income details
- Family composition and dependent information
- Education qualification
- Land ownership and agricultural details (if applicable)
- Disability status (if applicable)

**FR-03**: The system shall allow users to update their profile information at any time

**FR-04**: The system shall support profile creation in multiple Indian languages

### 5.2 AI-Based Scheme Recommendation

**FR-05**: The system shall analyze user profile data and recommend relevant government schemes with eligibility match percentage

**FR-06**: The system shall rank recommendations based on:
- Eligibility match score
- Benefit amount/value
- Application deadline proximity
- Scheme popularity and success rate

**FR-07**: The system shall display scheme details including:
- Scheme name and description
- Eligibility criteria
- Benefits and coverage
- Application deadline
- Required documents
- Application process overview

**FR-08**: The system shall allow users to filter schemes by category (agriculture, education, health, employment, housing, social welfare)

**FR-09**: The system shall provide "Why recommended?" explanations showing which profile attributes matched eligibility criteria

### 5.3 NLP Chatbot and Voice Assistant

**FR-10**: The system shall provide an AI chatbot capable of answering queries about:
- Scheme details and eligibility
- Application process and documentation
- Application status
- General guidance

**FR-11**: The system shall support chatbot interactions in at least 5 Indian languages (Hindi, English, Tamil, Telugu, Bengali)

**FR-12**: The system shall provide voice input capability using speech-to-text conversion

**FR-13**: The system shall provide voice output capability using text-to-speech conversion in multiple languages

**FR-14**: The system shall maintain conversation context and history for personalized responses

**FR-15**: The system shall handle common queries using intent recognition and entity extraction

### 5.4 OCR-Based Document Extraction

**FR-16**: The system shall extract data from Aadhaar cards including:
- Name
- Aadhaar number
- Date of birth
- Gender
- Address

**FR-17**: The system shall extract data from bank passbooks including:
- Account holder name
- Account number
- IFSC code
- Bank name and branch

**FR-18**: The system shall extract data from land records including:
- Owner name
- Survey/plot number
- Land area
- Location details

**FR-19**: The system shall extract data from income certificates including:
- Name
- Annual income
- Issuing authority
- Certificate number

**FR-20**: The system shall auto-populate user profile fields with extracted OCR data

**FR-21**: The system shall allow users to review and correct OCR-extracted data before submission

**FR-22**: The system shall support image uploads in JPG, PNG, and PDF formats

### 5.5 Smart Document Checklist Generation

**FR-23**: The system shall generate a personalized document checklist for each scheme based on:
- Scheme requirements
- User profile data
- User category and demographics

**FR-24**: The system shall indicate which documents the user has already uploaded

**FR-25**: The system shall provide document templates and sample formats where applicable

**FR-26**: The system shall allow users to upload documents against checklist items

**FR-27**: The system shall validate document completeness before allowing application submission

### 5.6 Fraud and Duplicate Detection

**FR-28**: The system shall detect duplicate applications by the same user for the same scheme

**FR-29**: The system shall flag suspicious patterns including:
- Multiple applications from same device/IP within short timeframe
- Identical or highly similar document uploads across different users
- Profile data inconsistencies

**FR-30**: The system shall use AI-based anomaly detection to identify potentially fraudulent applications

**FR-31**: The system shall maintain an audit log of all application submissions and modifications

**FR-32**: The system shall prevent submission of duplicate applications with appropriate user warnings

### 5.7 Application Guidance and Tracking

**FR-33**: The system shall provide step-by-step application guidance for each scheme

**FR-34**: The system shall allow users to save application progress and resume later

**FR-35**: The system shall generate application summary for user review before final submission

**FR-36**: The system shall provide application tracking dashboard showing:
- Application ID and submission date
- Current status (submitted, under review, approved, rejected)
- Expected timeline
- Next steps or actions required

**FR-37**: The system shall send notifications for application status updates via SMS/email

**FR-38**: The system shall allow users to view application history and past submissions

### 5.8 Search and Discovery

**FR-39**: The system shall provide keyword-based scheme search functionality

**FR-40**: The system shall support advanced filters including:
- Scheme category
- Benefit type
- Eligibility criteria
- Application deadline
- State/central government

**FR-41**: The system shall display trending and popular schemes on the homepage

**FR-42**: The system shall provide scheme comparison feature for similar schemes

## 6. Non-Functional Requirements

### 6.1 Performance

**NFR-01**: The system shall load the homepage within 3 seconds on 3G network connection

**NFR-02**: The system shall return scheme recommendations within 5 seconds of profile submission

**NFR-03**: The system shall process OCR extraction within 10 seconds per document

**NFR-04**: The system shall respond to chatbot queries within 2 seconds

**NFR-05**: The system shall support at least 1,000 concurrent users during hackathon demonstration

### 6.2 Scalability

**NFR-06**: The system architecture shall be designed to scale horizontally to support 100,000+ users

**NFR-07**: The system shall handle peak loads during scheme announcement periods

**NFR-08**: The database shall be optimized for fast read operations on scheme data

### 6.3 Security

**NFR-09**: The system shall encrypt all user personal data at rest and in transit using industry-standard encryption (AES-256)

**NFR-10**: The system shall implement secure authentication using OTP-based verification

**NFR-11**: The system shall comply with data privacy regulations and not share user data with third parties

**NFR-12**: The system shall implement role-based access control for different user types

**NFR-13**: The system shall sanitize all user inputs to prevent SQL injection and XSS attacks

**NFR-14**: The system shall implement rate limiting to prevent API abuse

**NFR-15**: The system shall securely store uploaded documents with access controls

### 6.4 Usability

**NFR-16**: The system shall provide an intuitive user interface requiring minimal training

**NFR-17**: The system shall be accessible on mobile devices with responsive design

**NFR-18**: The system shall support users with low digital literacy through voice and visual guidance

**NFR-19**: The system shall provide help documentation and FAQs in multiple languages

**NFR-20**: The system shall follow accessibility guidelines (WCAG 2.1 Level AA) for users with disabilities

**NFR-21**: The system shall use simple language and avoid technical jargon in user-facing content

### 6.5 Reliability and Availability

**NFR-22**: The system shall maintain 99% uptime during hackathon demonstration period

**NFR-23**: The system shall implement error handling with user-friendly error messages

**NFR-24**: The system shall provide graceful degradation if external services (OCR, NLP) are unavailable

**NFR-25**: The system shall implement automatic backup of user data daily

### 6.6 Maintainability

**NFR-26**: The system code shall be modular and follow clean code principles

**NFR-27**: The system shall include comprehensive API documentation

**NFR-28**: The system shall implement logging for debugging and monitoring

**NFR-29**: The system shall use version control for all code and configuration

### 6.7 Compatibility

**NFR-30**: The system shall be compatible with modern web browsers (Chrome, Firefox, Safari, Edge)

**NFR-31**: The system shall work on Android and iOS mobile browsers

**NFR-32**: The system shall support screen sizes from 320px (mobile) to 1920px (desktop)

## 7. User Personas

### 7.1 Persona 1: Ramesh - Small Farmer

**Demographics**:
- Age: 45 years
- Location: Rural village in Maharashtra
- Education: 8th grade
- Language: Marathi (primary), limited Hindi
- Digital literacy: Low (uses basic smartphone features)

**Profile**:
- Owns 2 acres of agricultural land
- Annual income: ₹80,000
- Family: Wife and 2 children
- Category: OBC

**Goals**:
- Find agricultural subsidies and crop insurance schemes
- Get financial assistance for farm equipment
- Access schemes for children's education

**Pain Points**:
- Unaware of available schemes
- Difficulty reading English/Hindi documents
- Cannot travel frequently to government offices
- Needs help with documentation

**How YojanaSaathi Helps**:
- Voice assistant in Marathi for easy interaction
- OCR to extract data from land records and Aadhaar
- Personalized recommendations for agriculture schemes
- Step-by-step application guidance

### 7.2 Persona 2: Priya - College Student

**Demographics**:
- Age: 20 years
- Location: Tier-2 city in Tamil Nadu
- Education: Undergraduate student
- Language: Tamil (primary), English
- Digital literacy: High

**Profile**:
- From middle-class family
- Annual family income: ₹3,50,000
- Category: General
- Pursuing engineering degree

**Goals**:
- Find scholarship opportunities
- Access skill development programs
- Get information about education loans and grants

**Pain Points**:
- Overwhelmed by number of schemes
- Unsure about eligibility criteria
- Misses application deadlines
- Complicated application processes

**How YojanaSaathi Helps**:
- AI recommendations filtered for education schemes
- Deadline reminders and tracking
- Document checklist to ensure complete applications
- Chatbot for quick queries

### 7.3 Persona 3: Lakshmi - Elderly Widow

**Demographics**:
- Age: 68 years
- Location: Semi-urban area in Karnataka
- Education: Illiterate
- Language: Kannada only
- Digital literacy: None (relies on family members)

**Profile**:
- Widow, living with son's family
- No independent income
- Category: SC
- Has disability certificate (partial vision loss)

**Goals**:
- Access widow pension schemes
- Get healthcare benefits
- Find disability assistance programs

**Pain Points**:
- Cannot read or write
- Completely dependent on others for information
- Afraid of complex processes
- Limited mobility to visit offices

**How YojanaSaathi Helps**:
- Voice assistant for complete hands-free interaction
- Family members can help with initial setup
- Simple visual interface with large fonts
- Automatic eligibility detection based on profile

### 7.4 Persona 4: Meena - Self-Help Group Member

**Demographics**:
- Age: 32 years
- Location: Rural Rajasthan
- Education: 10th grade
- Language: Hindi (primary), basic English
- Digital literacy: Medium

**Profile**:
- Member of women's self-help group
- Runs small tailoring business
- Annual income: ₹1,20,000
- Category: OBC
- Married with 3 children

**Goals**:
- Find microfinance and business loan schemes
- Access women entrepreneurship programs
- Get skill training opportunities
- Find schemes for children's welfare

**Pain Points**:
- Limited time due to work and family responsibilities
- Needs schemes for both business and family
- Confused about which schemes to apply for first
- Worried about loan eligibility

**How YojanaSaathi Helps**:
- Consolidated view of business and family schemes
- Priority recommendations based on benefit value
- Document checklist reduces back-and-forth
- Application tracking saves time

### 7.5 Persona 5: Arjun - Unemployed Youth

**Demographics**:
- Age: 24 years
- Location: Small town in Uttar Pradesh
- Education: Graduate (B.Com)
- Language: Hindi (primary), English
- Digital literacy: High

**Profile**:
- Unemployed for 6 months after graduation
- Annual family income: ₹2,00,000
- Category: General
- Looking for job opportunities and skill training

**Goals**:
- Find employment generation schemes
- Access skill development and training programs
- Get information about startup schemes
- Find financial assistance for job search

**Pain Points**:
- Frustrated with job search
- Unaware of government employment schemes
- Needs guidance on skill development
- Limited financial resources for training

**How YojanaSaathi Helps**:
- Employment-focused scheme recommendations
- Information about skill training programs
- Application guidance for self-employment schemes
- Chatbot for career guidance queries

## 8. Assumptions and Constraints

### 8.1 Assumptions

**A-01**: Users have access to a smartphone or computer with internet connectivity

**A-02**: Users can provide basic identity documents (Aadhaar, mobile number) for registration

**A-03**: Government scheme data is available in structured format (simulated database for hackathon)

**A-04**: OCR accuracy will be 85% + for standard document formats

**A-05**: Users consent to data collection and storage for scheme recommendation purposes

**A-06**: Third-party APIs (NLP, OCR, speech services) are available and functional

**A-07**: The system will initially focus on central government schemes and 2-3 major states

**A-08**: Users understand that the platform provides guidance but final approval rests with government authorities

### 8.2 Constraints

**C-01**: Hackathon timeline limits full integration with live government databases

**C-02**: Budget constraints limit use of premium AI/ML services (will use open-source alternatives where possible)

**C-03**: Cannot implement actual payment or disbursement functionality

**C-04**: Limited to web-based platform (no native mobile apps in initial version)

**C-05**: Multilingual support limited to 5 major Indian languages initially

**C-06**: OCR limited to 4 document types (Aadhaar, bank passbook, land record, income certificate)

**C-07**: Fraud detection will use rule-based and basic ML models (not advanced deep learning)

**C-08**: Real-time government API integration not feasible (will simulate with mock data)

**C-09**: Team size and expertise limit scope of AI model sophistication

**C-10**: Demo environment will support limited concurrent users (1,000 max)

---

**Document Version**: 1.0  
**Last Updated**: February 14, 2026  
**Status**: Draft for Review
