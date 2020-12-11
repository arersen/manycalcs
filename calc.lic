unit CalculatorUnit;

interface

uses
  Windows, Messages, SysUtils, Classes, Graphics, Controls, Forms, Dialogs,
  StdCtrls, ExtCtrls;

type
  TCalculatorForm = class(TForm)
    Addition: TButton;
    Subtraction: TButton;
    Multiplication: TButton;
    Division: TButton;
    One: TButton;
    Two: TButton;
    Three: TButton;
    Four: TButton;
    Five: TButton;
    Six: TButton;
    Seven: TButton;
    Eight: TButton;
    Nine: TButton;
    Zero: TButton;
    Decimal: TButton;
    Enter: TButton;
    Equals: TLabel;
    ClearValue: TButton;
    Panel1: TPanel;
    Negative: TButton;
    Reset: TButton;
    NumberEdit: TEdit;
    procedure NumberButtonClick (Sender: TOject);
    procedure NegativeClick(Sender: TObject);
    procedure AdditionClick(Sender: TObject);
    procedure SubtractionClick(Sender: TObject);
    procedure MultiplicationClick(Sender: TObject);
    procedure DivisionClick(Sender: TObject);
    procedure EnterClick(Sender: TObject);
    procedure ClearValueClick(Sender: TObject);
    procedure ResetClick(Sender: TObject);

  private
    { Private declarations }
  public
    { Public declarations }
  end;

var
  CalculatorForm: TCalculatorForm;

implementation

{$R *.DFM}

//'The variables listed below have a "global scope."

var
   FNumber : real;
   Math : string;

//The following procedure gives the number buttons their ability to add a
//numerical value to the first number's text box.

procedure TCalculatorForm.NumberButtonClick (Sender: TObject);
begin
  NumberEdit.Text := NumberEdit.Text + (Sender as TButton).Caption;
end;

//The following procedure controls the negative/positive button.  The string in
//the edit box is converted into a real number, multiplied by -1, and then
//converted back into a string to be placed back into the edit box.

procedure TCalculatorForm.NegativeClick(Sender: TObject);
var
     OriginalNumber: real;
     TextNumber: string;
begin
     OriginalNumber := -(StrToFloat(NumberEdit.Text));
     TextNumber := FormatFloat('0.##########', OriginalNumber);
     NumberEdit.Text := TextNumber
end;

//The following procedures give the mathematical function buttons their ability
//to instigate a specific math function.  When a function button is pressed,
//the string variable "Math" is assigned a specific term.  The procedures also
//turn the first string found in the edit box into a floating variable and
//clears the edit box so another value can be entered.

procedure TCalculatorForm.AdditionClick(Sender: TObject);
begin
     Math := 'Add';
     FNumber := StrToFloat(NumberEdit.Text);
     NumberEdit.Clear;
end;

procedure TCalculatorForm.SubtractionClick(Sender: TObject);
begin
     Math := 'Subtract';
     FNumber := StrToFloat(NumberEdit.Text);
     NumberEdit.Clear;
end;

procedure TCalculatorForm.MultiplicationClick(Sender: TObject);
begin
    Math := 'Multiply';
     FNumber := StrToFloat(NumberEdit.Text);
     NumberEdit.Clear;
end;

procedure TCalculatorForm.DivisionClick(Sender: TObject);
begin
    Math := 'Divide';
    FNumber := StrToFloat(NumberEdit.Text);
    NumberEdit.Clear;
end;

//The following procedure gives the enter button its ability to interpret all
//previous procedures and calculate the correct answer.  The overall procedure
//turns the second number (formatted as a string) entered into the edit box into
//a floating variable.  The procedure then breaks into if statements.
//These if statements corespond with the string value the variable "Math" was
//given in above procedures.  The if statements contain code to give the real
//variable "Answer" which is formatted to be placed in the label designated for
//answers.

procedure TCalculatorForm.EnterClick(Sender: TObject);
var
   Answer, SNumber : real;
   Text : string;

begin
    SNumber := StrToFloat(NumberEdit.Text);

  begin
    if Math = 'Add' then
      Answer := FNumber + SNumber;
      Text := FormatFloat('0.#####', Answer);
      Equals.Caption := '= ' + Text;
      NumberEdit.Clear;
  end;

  begin
    if Math = 'Subtract' then
      Answer := FNumber - SNumber;
      Text := FormatFloat('0.#####', Answer);
      Equals.Caption := '= ' + Text;
      NumberEdit.Clear;
  end;

  begin
    if Math = 'Multiply' then
      Answer := FNumber * SNumber;
      Text := FormatFloat('0.#####', Answer);
      Equals.Caption := '= ' + Text;
      NumberEdit.Clear;
  end;

  begin
    if Math = 'Divide' then
      Answer := FNumber / SNumber;
      Text := FormatFloat('0.#####', Answer);
      Equals.Caption := '= ' + Text;
      NumberEdit.Clear;

  end;

end;

//This is the procedure for the clear value button.  This button will only clear
//a value entered onto the edit box; it will not clear selected functions.

procedure TCalculatorForm.ClearValueClick(Sender: TObject);
  begin
    NumberEdit.Clear;
  end;

//This is a procedure to reset the calculator.

procedure TCalculatorForm.ResetClick(Sender: TObject);
  begin
    Equals.Caption := ;
    NumberEdit.Clear;
    FNumber := 0;
    SNumber := 0;
    Math := 'Default';
  end;

end.
