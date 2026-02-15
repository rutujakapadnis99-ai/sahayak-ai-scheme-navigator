# Requirements Document: Sahayak – AI Powered Scheme Navigator for Bharat

## Introduction

Sahayak is an AI-powered conversational assistant designed to bridge the accessibility gap between government welfare schemes and eligible citizens in Bharat.

Despite the availability of thousands of welfare programs, millions of rural and semi-urban citizens remain unaware of benefits due to complex portals, language barriers, lack of personalization, and low digital literacy.

Sahayak simplifies scheme discovery by providing personalized eligibility matching, multilingual explanations, and guided application assistance through an intuitive conversational interface.

The system focuses on accessibility, clarity, and scalability, ensuring that welfare benefits effectively reach intended beneficiaries.

## Scope of MVP (Hackathon Phase)

The Minimum Viable Product (MVP) of Sahayak will include:

- User profile-based eligibility evaluation
- Personalized scheme recommendations
- Simplified scheme explanations
- Document checklist generation
- Step-by-step application guidance
- Multilingual text interface

The MVP will NOT include:

- Direct government portal API integration
- Aadhaar authentication
- Automatic form submission

The system will be designed for AWS-based deployment and scalable cloud architecture.

## Glossary

- **Sahayak_System**: The complete AI-powered scheme navigation application
- **User**: A citizen seeking information about government welfare schemes
- **Scheme**: A government welfare program offering benefits to eligible citizens
- **Eligibility_Evaluator**: Component that determines which schemes a user qualifies for
- **Profile**: User demographic and socioeconomic information used for eligibility assessment
- **Recommendation_Engine**: Component that generates personalized scheme suggestions
- **Document_Checklist**: List of required documents for scheme application
- **Application_Guide**: Step-by-step instructions for applying to a scheme
- **Scheme_Database**: Repository of government scheme information
- **Language_Processor**: Component handling multilingual text support

## Requirements

### Requirement 1: User Profile Collection

**User Story:** As a user, I want to provide my personal information, so that the system can determine which schemes I am eligible for.

#### Acceptance Criteria

1. WHEN a user accesses the system, THE Sahayak_System SHALL prompt for profile information including age, income, occupation, and state
2. WHEN a user enters profile data, THE Sahayak_System SHALL validate required fields
3. WHEN invalid data is provided, THE Sahayak_System SHALL display a clear error message
4. THE Sahayak_System SHALL store user profile data securely for the session duration
5. WHEN profile entry is complete, THE Sahayak_System SHALL confirm information before proceeding
6. THE system SHALL allow users to modify profile information before eligibility evaluation.

### Requirement 2: Eligibility Evaluation

**User Story:** As a user, I want the system to automatically determine which schemes I qualify for, so that I do not have to manually check each scheme.

#### Acceptance Criteria

1. WHEN profile is complete, THE Eligibility_Evaluator SHALL assess eligibility against all schemes in the Scheme_Database
2. THE Eligibility_Evaluator SHALL apply scheme-specific criteria including age, income, occupation, and geographic restrictions
3. WHEN a user meets criteria, THE scheme SHALL be marked eligible
4. WHEN a user partially meets criteria, THE scheme SHALL be marked potentially eligible
5. THE Eligibility_Evaluator SHALL complete evaluation within 3 seconds for a dataset of up to 500 schemes

### Requirement 3: Personalized Scheme Recommendations

**User Story:** As a user, I want to see schemes ranked by relevance, so that I can focus on the most beneficial options.

#### Acceptance Criteria

1. THE Recommendation_Engine SHALL generate ranked eligible schemes
2. THE ranking SHALL consider benefit amount, ease of application, and profile match
3. THE system SHALL display scheme name, short description, and estimated benefit
4. THE system SHALL display at least top 5 schemes
5. IF no schemes match, THE system SHALL provide clear explanation

### Requirement 4: Scheme Information Presentation

**User Story:** As a user with low digital literacy, I want scheme information explained in simple language, so that I can understand clearly.

#### Acceptance Criteria

1. THE scheme details SHALL be displayed in simplified language
2. THE information SHALL include eligibility, benefits, documents, and process overview
3. THE system SHALL avoid technical jargon
4. THE benefits SHALL be shown with clear examples and currency values
5. THE content SHALL use clear formatting and short paragraphs

### Requirement 5: Document Checklist Generation

**User Story:** As a user, I want to know exactly which documents I need, so that I can prepare before applying.

#### Acceptance Criteria

1. THE system SHALL generate personalized document checklist
2. THE checklist SHALL include only relevant documents
3. THE document names SHALL appear in selected language
4. THE user SHALL mark documents as collected or pending
5. WHEN all documents collected, THE guidance SHALL activate

### Requirement 6: Application Guidance

**User Story:** As a user unfamiliar with online systems, I want step-by-step guidance, so that I can apply confidently.

#### Acceptance Criteria

1. THE Application_Guide SHALL provide sequential steps
2. THE steps SHALL include instructions and common mistakes
3. THE complex steps SHALL be broken into simple actions
4. THE external portal URLs SHALL be provided where needed
5. THE user SHALL track completion progress

### Requirement 7: Multilingual Support

**User Story:** As a regional language user, I want to use the system in my preferred language.

#### Acceptance Criteria

1. THE language selection SHALL appear at first access
2. THE system SHALL support Hindi, English, Tamil, Telugu, and Bengali
3. ALL content SHALL update based on selected language
4. THE language change SHALL apply instantly
5. THE terminology SHALL remain consistent across languages

### Requirement 8: Low-Bandwidth Optimization

**User Story:** As a rural user, I want the system to work on slow internet connections.

#### Acceptance Criteria

1. THE interface SHALL load within 5 seconds on 2G speeds
2. THE essential content SHALL load first
3. THE assets SHALL be compressed
4. THE viewed content SHALL be cached for temporary offline viewing
5. THE loading indicators SHALL be displayed

### Requirement 9: Data Security and Privacy

**User Story:** As a user providing personal information, I want my data to remain secure.

#### Acceptance Criteria

1. THE data SHALL be encrypted in transit using TLS 1.3
2. THE data SHALL be encrypted at rest using AES-256
3. THE session data SHALL be deleted within 24 hours
4. THE data SHALL not be shared without consent
5. THE system SHALL comply with Indian data protection regulations

### Requirement 10: System Availability and Scalability

**User Story:** As an administrator, I want the system to handle high traffic reliably.

#### Acceptance Criteria

1. THE system SHALL maintain minimum 99.5% uptime
2. THE system SHALL scale to 10,000 concurrent users
3. THE failover SHALL occur within 30 seconds
4. THE errors SHALL be logged and monitored
5. THE deployment SHALL use AWS managed services

### Requirement 11: Scheme Database Management

**User Story:** As an administrator, I want to update scheme data easily.

#### Acceptance Criteria

1. THE database SHALL store eligibility, benefits, documents, and URLs
2. THE updates SHALL occur without downtime
3. THE changes SHALL be versioned
4. THE new schemes SHALL reflect within 1 hour
5. THE database SHALL support efficient eligibility querying

### Requirement 12: Conversational Interface

**User Story:** As a user, I want to interact conversationally rather than using complex forms.

#### Acceptance Criteria

1. THE system SHALL respond conversationally to user queries
2. THE system SHALL understand common questions about eligibility and documents
3. THE clarifying questions SHALL be asked if data is incomplete
4. THE conversation context SHALL be maintained
5. THE minor typos SHALL be interpreted correctly

### Requirement 13: Accessibility and Usability

**User Story:** As a first-time digital user, I want the system to be simple and easy to use.

#### Acceptance Criteria

1. THE language SHALL be suitable for Grade 6 readability
2. THE scheme recommendations SHALL be reachable within 3 steps
3. THE UI SHALL follow accessibility best practices
4. THE interface SHALL use high contrast and readable fonts
5. THE user testing SHALL confirm usability for low digital literacy users
