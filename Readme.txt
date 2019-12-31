________________________________________________________________ 

FILENAME: CrystalVCL9.exe

Phone: (604) 669-8379
Fax:   (604) 681-7163

Answers by Email: 
http://support.crystaldecisions.com


For more information, visit us on the Web:

Crystal Reports
http://www.crystaldecisions.com/products/crystalreports

Product Information
http://www.crystaldecisions.com/products

Developer Zone
http://www.crystaldecisions.com/products/dev_zone

Technical Support
http://support.crystaldecisions.com

Training & Consulting
http://www.crystaldecisions.com/services/

Crystal Decisions homepage
http://www.crystaldecisions.com

--------------------------
(c) 2003 Crystal Decisions Inc.
________________________________________________________________ 

PRODUCT VERSION

This Component is for use with version 9.2 of Crystal Reports, 
version 6 of Borland C++ Builder, and version 7 of Borland Delphi.

________________________________________________________________ 

DESCRIPTION

This is an update to the Delphi VCL Components (TCrpe and 
TCrpeDS) for Crystal Reports 9.
________________________________________________________________ 

INSTALLATION

Installation of the components are done manually.  Please 
carefully follow the instructions below:

Unzip the files to the desired directory (due to the large
number of files included with the Crystal VCL components, we
recommend a separate directory for this purpose).

Delphi Installation

1. Open Delphi 7, and choose File|Close All to close any open 
projects. 

2. Go to the Tools menu and choose "Environment Options".  In
the Environment Options dialog, choose the "Library" tab, and 
edit the Library Path to include the Crystal VCL Delphi directory. 
IMPORTANT: If there are any other paths in the Library path 
that point to older Crystal VCL components, these must either
be removed, or the older component files must be removed, 
otherwise the installation of the new components will fail.

3. Choose "File|Open" and load the "dcl7cr9.dpk" file (or 
"vcl7cr9.dpk" if you are compiling the components for runtime 
only and will not be compiling them into your application)
from the Delphi sub-folder.  

4. When the DPK file is loaded, you should see a dialog with
some buttons at the top.  Press the "Compile" button.  When 
compilation is finished, press the "Install" button (if you
are compiling the vcl7cr9.dpk, do not press "Install" as it
cannot be installed as a visual component).  If you get an 
error saying that the component cannot be installed because
it contains units which are already in use by another 
component please check step 2 again (most likely there are
older Crystal VCL source files found in one of the Library
Paths).

You should get a message that TCrpe/TCrpeDS are now registered 
(again, this does not apply to "vcl7cr9.dpk"), and the component
icons should appear on the "Data Access" tab of the Component
Palette.

C++ Builder Installation

1. Open C++ Builder 6, and choose File|Close All to close any open 
projects. 

2. Go to the Tools menu and choose "Environment Options".  In
the Environment Options dialog, choose the "Library" tab, and 
edit the Library Path to include the Crystal VCL Delphi directory. 
The Delphi directory is required because the VCL is implemented
by the Delphi source code located in that directory.
IMPORTANT: If there are any other paths in the Library path 
that point to older Crystal VCL components, these must either
be removed, or the older component files must be removed, 
otherwise the installation of the new components will fail.

3. Choose "File|Open" and load the "cr9cvcl.bpk" file from 
the Builder sub-folder.

4. When the BPK file is loaded, you should see the Package dialog.  
Press the "Compile" button.  When compilation is finished, 
press the "Install" button.  

If you get an error saying that the component cannot be installed because
it contains units which are already in use by another 
component please check step 2 again (most likely there are
older Crystal VCL source files found in one of the Library
Paths).

You should get a message that TCrpe/TCrpeDS are now registered, 
and the component icons should appear on the "Data Access" 
tab of the Component Palette.


________________________________________________________________ 

RELEASE NOTES

1. This VCL is only intended to work with Crystal Reports 9.2.2.
If you are unsure of the version you have installed, please open
Crystal Reports Designer and go to the Help | About dialog.
Where the Product Version is listed, please make sure that the numbers
begin with 9.2.2.  If not, please contact customer service at
+1.604.681.3435 to request a new CD.

A number of fixes have been made to CRPE in support of the VCL.
To ensure the correction functioning of the VCL, you should
get the latest patches from the Crystal Decisions support
Web site, found here:
http://support.crystaldecisions.com/communityCS/FilesAndUpdates/cr90mainwin_en.zip.asp


2. This VCL is only intended to be used within Borland Delphi 7 
and Borland C++ Builder 6.


3. This version of the Crystal VCL is an update to the
Crystal Reports 8.5 VCL, to make it compatible with 
Crystal Reports 9.2.2.  The Crystal Reports Print Engine
does not expose the new Crystal Reports 9 features,
and so the Crystal VCL is also unable to expose these 
new features.  Any reports designed in Crystal Reports 9
can be used with the Crystal VCL, but features that have
been added since Crystal Reports 8.5 cannot be changed
at runtime using the VCL.

Some of the version 9 features that cannot be controlled/modified from
the VCL include:
- Custom Functions
- Repository
- Templates
- Report Parts
- Gauge charts
- Gantt charts
- SQL Commands


4. This VCL is supported by Crystal Decisions (please see
http://support.crystaldecisions.com/).  However, Crystal Decisions does
not intend to escalate any known issues through the Support Escalation
 Process to be fixed in the patches.  Any issues will be addressed in
the next release of Crystal Reports.


5. The following Export Formats have been removed in
Crystal Reports 9:
- LotusWK1
- LotusWKS
- LotusWK3
- DIF
- Crystal Reports 7


6. ISSUE: TextObjects.item.Format.Paragraph.LineSpacingType:
Textobject disappears from report from preview window on
assignment to the property.

RESOULUTION: Value assigned to this property must be in inches
and not in points as specified in help (UCrpe32.hlp). So when the
number 10 is assigned to this property, it makes textbox blank
(too large). The correct value would be 0.1388.

7. The CDO database driver is not installed by default in Crystal Reports 9.x.
If a project uses TCrpeDS, the CDO database component may 
need to be installed.  To do this go to the Add/Remove Programs control
panel, choose Crystal Reports and press the Change button to activate
the Crystal Reports installer.  

8. The TCrpeDS object, TCrDataSource, now implements COM reference 
counting.  If existing projects make use of this component, they should
use COM reference counting to manage the object's lifetime.  I.e., use
AddRef once created and Release when no longer needed.  The TCrDataSource
object will Free itself once the last reference is removed.

9.  Obsolete Items Removed
- Bytes and Tag removed from Tables class
- TCrStoredProcParamType removed
- StoredProcParams and TCrpeStoredProcParamsItem classes
- TCrReportFormat
- CrpePath property
- TCrpeGraphData and TCrpeGraphOptions classes
- ColumnHeadings and TabularFormat removed from TCrpeExportExcel
- Changes to TCrpeExportPDF / TCrpeExportRTF:
    UseOlderDll property was removed
- mdmCustom and PE_MAP_DM_CUSTOMRANGES removed from 
MapStyle.DistributionMethod

10. New Items Added
- TCrExportDestination changed:
    TCrExportDestination = (toFile, toEmailViaMapi, toEmailViaVIM,
      toMSExchange, toLotusNotes, toApplication);
- TCrExportType changed
    TCrExportType = (AdobeAcrobatPDF, CrystalReportRPT, HTML32,
      HTML40, MSExcel, MSWord, ODBCTable, Records, ReportDefinition,
      RichText, SeparatedValues, TabSeparatedText, TextFormat, XML1);
- TCrGroupType changed:
    TCrGroupType = (gtOther, gtDate, gtBoolean, gtTime , gtDateTime);
- TCrGraphNumberFormat changed:
    TCrGraphNumberFormat = (gnfNoDecimal, gnfOneDecimal, gnfTwoDecimal,
      gnfUnknownType, gnfCurrencyTwoDecimal, gnfPercentNoDecimal,
      gnfPercentOneDecimal, gnfPercentTwoDecimal,gnfOther);
- Save as function changed:    
    function  SaveAs (filePath: string): Boolean;
- UserName and Password properties added to TCrpeExportEmail class
- Prompt property added to TCrpeExportODBC
- TCrExportExcelType changed:
    TCrExportExcelType = (ExcelStandard, ExcelDataOnly);
- The following properties were added to TCrpeExportExcel:
    CreatePageBreaks      : Boolean;
    ConvertDatesToStrings : Boolean;
    UsePageRange          : Boolean;
    FirstPage             : DWord;
    LastPage              : DWord;
    ExportHeaderFooter    : Boolean;
    ChopPageHeader        : Boolean;
- The following properties were added to TCrpeExportHTML:
    UsePageRange  : Boolean;
    FirstPage     : DWord;
    LastPage      : DWord;
- TCrpeExportWord class  was added.  These are the properties:
    Prompt       : Boolean;
    UsePageRange : Boolean;
    FirstPage    : Word;
    LastPage     : Word;
- TCrpeExportText class added.
    These five properties were moved from TCrpeExportOptions to TCrpeExportText:
      UseRptNumberFmt : Boolean;
      UseRptDateFmt   : Boolean;
      StringDelimiter : Char;  
      FieldSeparator  : string;
      LinesPerPage    : Word;
    Note these changes:
      CharSepDelimiter was renamed to StringDelimiter
      CharSepSeparator was renamed to FieldSeparator
    These two new properties are in the TCrpeExportText class:
      CharPerInch     : Word;
      RecordsType     : TCrRecordsType;
- New type for TCrpeExportText:
    TCrRecordsType = (ColumnsWithSpaces, ColumnsNoSpaces);
- Prompt property added to TCrpeExportXML
- The following changes were made to TCrpeReportOptions:
    Removed:
      TranslateDOSStrings
      TranslateDOSMemos
    Added:
      UseDummyData                     : Boolean;
      ConvertOtherNullsToDefault       : Boolean;
      VerifyStoredProcOnRefresh        : Boolean;
      RetainImageColourDepth           : Boolean;
- GlobalOptions updated with two new properties:
    DisableThumbnailUpdates          : Boolean;
    VerifyWhenDatabaseDriverUpgraded : Boolean;
- Updated all VCL code that accessed Group types to include 
gtDateTime and PE_GC_TYPEDATETIME
- Fixed Graphs dialog for new Data Points type: gdpShowLabelValue (GraphOptionInfo).
- Fixed Graphs dialog for new NumberFormat types: gnfUnknownType, 
gnfOther (GraphOptionInfo).
- Added IsLinked property to TCrpeParamFields

11. Changes Made
- Global variables in CRDynamic were eliminated and code was made multi-thread safe
- IgnoreKnownProblems (was IgnoreCRPEBugs) moved from published to public (not visible 
on Object Inspector)
- Fixed SearchButtonEvent, Hyperlink Event, OnDrillGroupEvent, OnDrillDetailEvent, 
OnShowGroupEvent, MouseClickEvent
- Updated SectionFormat dialog as the color panels were not 
drawing correctly when XP styles were used in the application.  
Used a ColorBox component instead.

________________________________________________________________ 
 
Last updated on July 16, 2003.
________________________________________________________________ 

