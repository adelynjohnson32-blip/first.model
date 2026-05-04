# Mortgage Decision Simulator

A powerful, educational web application for comparing two mortgage options using financial theory. Understand the true cost of borrowing through APR vs EAR analysis, amortization schedules, and interactive visualizations.

## 🎯 Features

- **Dual Loan Comparison**: Side-by-side analysis of two mortgage options
- **Financial Accuracy**: Proper calculation of EAR (Effective Annual Rate) accounting for different compounding frequencies
- **Amortization Schedules**: Complete monthly payment breakdown showing principal vs interest
- **Interactive Visualizations**: 
  - Remaining balance over time
  - Payment breakdown charts
  - Side-by-side comparison metrics
- **Financial Education**: Built-in explanations of key concepts (APR, EAR, compounding, amortization, time value of money)
- **Responsive Design**: Works seamlessly on desktop, tablet, and mobile devices
- **Dark Mode Support**: Automatic light/dark theme based on system preferences
- **Accessibility**: WCAG AA compliant with screen reader support

## 📊 Key Metrics

For each loan, the simulator calculates:
- **Monthly Payment**: Fixed amount you pay each month
- **EAR (Effective Annual Rate)**: True cost accounting for compounding
- **Total Interest**: Sum of all interest paid over the loan term
- **Total Amount Paid**: Principal + total interest
- **Amortization Schedule**: Month-by-month breakdown

## 💰 Financial Concepts Explained

### APR vs EAR
**APR (Annual Percentage Rate)** is the advertised rate, but it doesn't account for compounding. Two loans with the same APR can have different actual costs depending on how often interest compounds.

**EAR (Effective Annual Rate)** = (1 + APR/m)^m − 1, where m = compounding periods per year

This is the true cost of borrowing.

### Compounding Frequency
- **Monthly** (12x/year): Most common for mortgages
- **Quarterly** (4x/year)
- **Semiannual** (2x/year)
- **Annual** (1x/year)

More frequent compounding = higher true cost (for same APR)

### Amortized Loans
A fixed-payment loan where monthly payments remain constant but the ratio of principal to interest changes:
- **Early payments**: Mostly interest (large outstanding balance)
- **Later payments**: Mostly principal (balance decreases)

## 🚀 Getting Started

### Online
Simply open `index.html` in any modern web browser.

### Local Development
```bash
# Clone or download the repository
git clone <repository-url>
cd mortgage-simulator

# Open in your browser
open index.html
# or for Linux:
xdg-open index.html
```

### File Structure
```
mortgage-simulator/
├── index.html      # Main HTML file
├── styles.css      # Stylesheet with dark mode support
├── script.js       # JavaScript logic and Chart.js integration
└── README.md       # This file
```

## 🎨 Usage

1. **Enter Loan Details**:
   - Set the loan amount (principal)
   - Set the term in years
   - Enter the APR (annual percentage rate)
   - Select compounding frequency

2. **Compare**:
   - The simulator instantly updates all metrics
   - View which loan is cheaper over the full term
   - See the EAR difference

3. **Visualize**:
   - Switch between three chart views:
     - **Remaining Balance**: How each loan's balance decreases
     - **Payment Breakdown**: Principal vs interest per payment
     - **Side-by-Side**: Quick metric comparison

4. **Learn**:
   - Click any expandable section to learn about finance concepts
   - Understand why EAR matters
   - See how compounding affects your cost

## 🔧 Technical Details

### Technologies Used
- **HTML5**: Semantic markup with accessibility features
- **CSS3**: Modern layout with CSS variables and animations
- **JavaScript (Vanilla)**: No frameworks, pure ES6+
- **Chart.js 4.4**: Professional data visualization

### Browser Support
- Chrome/Edge 90+
- Firefox 88+
- Safari 14+
- Mobile browsers (iOS Safari, Chrome Android)

### Performance
- Instant recalculation (< 50ms for all calculations)
- Lightweight: ~30KB total (uncompressed)
- No external dependencies except Chart.js

## 📐 Financial Formulas

### Monthly Payment Calculation
```
PMT = [r × PV] / [1 − (1 + r)^(−n)]
```
Where:
- PMT = monthly payment
- r = monthly interest rate
- PV = principal (loan amount)
- n = total number of monthly payments

### Effective Annual Rate (EAR)
```
EAR = (1 + APR/m)^m − 1
```
Where:
- APR = annual percentage rate
- m = compounding frequency per year

### Remaining Balance
After payment k:
```
Balance = PV × [(1 + r)^n − (1 + r)^k] / [(1 + r)^n − 1]
```

## 🎓 Educational Value

This simulator teaches:
- How interest compounds and affects loan cost
- The difference between APR and EAR
- How loan terms affect monthly payments and total interest
- Why comparing loans requires looking beyond the advertised APR
- Time value of money principles

## 🔒 Privacy

All calculations are performed locally in your browser. No data is sent to any server. Your loan information is never stored or shared.

## 💡 Tips for Use

1. **Compare carefully**: Always compare EARs, not APRs
2. **Experiment with terms**: See how a 15-year vs 30-year mortgage affects costs
3. **Understand trade-offs**: Shorter terms mean higher payments but less total interest
4. **Check compounding**: Verify the compounding frequency when comparing real loans
5. **Use for education**: Share with others learning about finance

## 🐛 Known Limitations

- Displays up to 40-year loan terms
- Assumes fixed rates (doesn't model ARM loans)
- Doesn't include property taxes, insurance, or HOA fees
- All rates are annual (converts internally to monthly)

## 📝 License

Open source. Feel free to fork, modify, and use for educational purposes.

## 🤝 Contributing

Found a bug? Have a suggestion? Feel free to:
1. Report issues
2. Suggest new features
3. Submit improvements

## 📞 Support

For issues or questions:
- Check the built-in education sections
- Review the financial formulas above
- Verify your loan parameters are realistic

---

**Made with ❤️ for financial literacy**
