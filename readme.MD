# FinTechCo Legacy Retirement Calculator

![](images/myRetirmentCalculatorScreen.png?raw=true) 

## About FinTechCo

FinTechCo is a modern financial services company that seamlessly blends cutting-edge digital payment solutions with traditional banking excellence. As a leader in the fintech space, we operate:

- **Digital Payment Services**: Our platform rivals PayPal and Venmo, offering instant peer-to-peer transfers, merchant services, and seamless mobile wallet integration
- **Traditional Banking Division**: Full-service banking including checking/savings accounts, loans, mortgages, and wealth management services
- **Financial Planning Tools**: Comprehensive suite of calculators and planning resources to help our customers achieve their financial goals

## Legacy Retirement Calculator

This retirement calculator represents FinTechCo's commitment to making financial planning accessible to everyone. Originally developed for our internal financial advisors, we've open-sourced this tool to benefit the broader community. The calculator takes a FIRE (Financially Independent Retire Early) perspective, helping users determine when they can achieve financial independence based on their savings rate and investment returns.

### Key Features
- Comprehensive modeling of income, expenses, savings, and investments over your lifetime
- Tax calculations based on current US tax brackets
- Social Security and pension income projections
- Housing costs including mortgage payoff timelines
- Healthcare and dependent cost modeling
- Inflation adjustments for accurate long-term planning
- Interactive charts showing your financial trajectory

## Demo
* Live Calculator: http://www.abrandao.com/retire

## Getting Started

Clone this repository or download the **index.html** file. The entire calculation engine is self-contained for easy deployment and modification.

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- Basic understanding of HTML/JavaScript for customization (optional)

## Technology Stack

This calculator runs entirely in your browser using:
- **jQuery** - For DOM manipulation and event handling
- **Bootstrap 3** - Responsive design and UI components  
- **Chart.js** - Interactive data visualization

We deliberately chose mature, stable technologies to ensure broad compatibility and ease of maintenance. All dependencies are loaded via CDN for simple deployment.

## Installation

1. Clone the repository:
```bash
git clone https://github.com/KitagawaPowa/retirementCalc-Legacy.git
```

2. Open `index.html` in your web browser

That's it! No build process or server required.

## How It Works

### Calculation Model

The calculator uses a year-by-year projection model:

1. **Income Phase** (Working Years)
   - Salary income with configurable savings rate
   - Investment returns on savings and retirement accounts
   - Additional income sources (rental, business, etc.)

2. **Expense Modeling**
   - Progressive tax calculations
   - Housing costs (mortgage + ongoing expenses)
   - Healthcare, food, utilities, transportation
   - Dependent costs
   - Inflation adjustments

3. **Retirement Phase**
   - Withdrawal rate strategy (default 4% SWR)
   - Social Security benefits
   - Pension income
   - Continued investment returns

### Sample Code

Income calculation during working years:
```javascript
for (i = 1 ; i < years+1; i++) { 
  var ai = {};  // Annual Income object
  ai.age = (+i + +currentAge);
  ai.income_earned = (i <= work_years) ? parseInt($("#income").val()) : 0;
  ai.income_saved = (i <= work_years) ? 
    $("#income").val() * parseFloat($("#income_savings_rate").val()/100) : 0;
  ai.savings_Int = +$("#savings").val() * parseFloat($("#savings_apy").val()/100);
  // ... additional calculations
}
```

## Debugging

Press F12 in your browser to open developer tools. The calculator outputs detailed year-by-year projections to the console for verification and debugging.

## Future Enhancements

Our product team is considering:
- CSV/Excel export functionality
- Cloud save and share capabilities
- Monte Carlo simulations
- International tax support
- Mobile app integration with FinTechCo accounts

## Contributing

We welcome contributions! Please submit issues and pull requests via GitHub. For major changes, please open an issue first to discuss your proposed changes.

## Security

This calculator processes all data locally in your browser. No financial information is transmitted to FinTechCo or any third party.

## Support

For support with the calculator:
- GitHub Issues: Report bugs and request features
- FinTechCo Support: 1-800-FINTECH (for FinTechCo customers)
- Email: retirement-calc@fintechco.com

## License

MIT License

Copyright (c) 2024 FinTechCo Financial Services, Inc.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

## Acknowledgments

- Bootstrap, jQuery, and Chart.js teams for excellent open-source libraries
- The FIRE community for inspiring financial independence
- FinTechCo's Financial Planning Division for domain expertise
- Our customers who provided valuable feedback during beta testing

---

*FinTechCo - Empowering Your Financial Future*