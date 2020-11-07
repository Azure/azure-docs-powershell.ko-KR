---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BBD37C4B-BB6F-4560-BDEE-F0440EC1938A
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscConfiguration.md
ms.openlocfilehash: b400efe3224a4fa4b014b9ac93786cd130d4ce6e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697860"
---
# <span data-ttu-id="08341-101">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="08341-101">Get-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="08341-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08341-102">SYNOPSIS</span></span>
<span data-ttu-id="08341-103">자동화에서 DSC 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="08341-103">Gets DSC configurations from Automation.</span></span>

## <span data-ttu-id="08341-104">구문과</span><span class="sxs-lookup"><span data-stu-id="08341-104">SYNTAX</span></span>

### <span data-ttu-id="08341-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="08341-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08341-106">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="08341-106">ByConfigurationName</span></span>
```
Get-AzAutomationDscConfiguration [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08341-107">설명은</span><span class="sxs-lookup"><span data-stu-id="08341-107">DESCRIPTION</span></span>
<span data-ttu-id="08341-108">**AzAutomationDscConfiguration** Cmdlet은 Azure AUTOMATION에서 Ap (원하는 상태 구성) 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="08341-108">The **Get-AzAutomationDscConfiguration** cmdlet gets APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="08341-109">예제의</span><span class="sxs-lookup"><span data-stu-id="08341-109">EXAMPLES</span></span>

### <span data-ttu-id="08341-110">예제 1: 모든 DSC 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="08341-110">Example 1: Get all DSC configurations</span></span>
```
PS C:\>Get-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="08341-111">이 명령은 Contoso17 이라는 자동화 계정의 모든 DSC 구성에 대 한 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="08341-111">This command gets metadata for all DSC configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="08341-112">예제 2: 이름별로 DSC 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="08341-112">Example 2: Get a DSC configuration by name</span></span>
```
PS C:\>Get-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration"
```

<span data-ttu-id="08341-113">이 명령은 Contoso17 이라는 자동화 계정에서 MyConfiguration 이라는 DSC 구성에 대 한 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="08341-113">This command gets metadata for a DSC configuration named MyConfiguration in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="08341-114">변수</span><span class="sxs-lookup"><span data-stu-id="08341-114">PARAMETERS</span></span>

### <span data-ttu-id="08341-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="08341-115">-AutomationAccountName</span></span>
<span data-ttu-id="08341-116">이 cmdlet이 가져오는 DSC 구성을 포함 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="08341-116">Specifies the name of the Automation account that contains DSC configurations that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08341-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08341-117">-DefaultProfile</span></span>
<span data-ttu-id="08341-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="08341-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08341-119">-이름</span><span class="sxs-lookup"><span data-stu-id="08341-119">-Name</span></span>
<span data-ttu-id="08341-120">이 cmdlet이 가져오는 DSC 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="08341-120">Specifies the name of the DSC configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
Aliases: ConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08341-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08341-121">-ResourceGroupName</span></span>
<span data-ttu-id="08341-122">이 cmdlet에서 DSC 구성을 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="08341-122">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08341-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08341-123">CommonParameters</span></span>
<span data-ttu-id="08341-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="08341-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08341-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08341-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08341-126">입력</span><span class="sxs-lookup"><span data-stu-id="08341-126">INPUTS</span></span>

### <span data-ttu-id="08341-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="08341-127">System.String</span></span>

## <span data-ttu-id="08341-128">출력</span><span class="sxs-lookup"><span data-stu-id="08341-128">OUTPUTS</span></span>

### <span data-ttu-id="08341-129">DscConfiguration를 통해 서.</span><span class="sxs-lookup"><span data-stu-id="08341-129">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="08341-130">상속자</span><span class="sxs-lookup"><span data-stu-id="08341-130">NOTES</span></span>

## <span data-ttu-id="08341-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="08341-131">RELATED LINKS</span></span>

[<span data-ttu-id="08341-132">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="08341-132">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="08341-133">가져오기-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="08341-133">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


