---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BBD37C4B-BB6F-4560-BDEE-F0440EC1938A
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscConfiguration.md
ms.openlocfilehash: 82c853f6f18f12c1e7005a859a5df924d3555b79
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993001"
---
# <span data-ttu-id="d312b-101">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="d312b-101">Get-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="d312b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d312b-102">SYNOPSIS</span></span>
<span data-ttu-id="d312b-103">Automation에서 DSC 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d312b-103">Gets DSC configurations from Automation.</span></span>

## <span data-ttu-id="d312b-104">구문</span><span class="sxs-lookup"><span data-stu-id="d312b-104">SYNTAX</span></span>

### <span data-ttu-id="d312b-105">ByAll(기본값)</span><span class="sxs-lookup"><span data-stu-id="d312b-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d312b-106">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="d312b-106">ByConfigurationName</span></span>
```
Get-AzAutomationDscConfiguration [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d312b-107">설명</span><span class="sxs-lookup"><span data-stu-id="d312b-107">DESCRIPTION</span></span>
<span data-ttu-id="d312b-108">**Get-AzAutomationDscConfiguration** cmdlet은 Azure Automation에서 DSC(원하는 상태 구성) 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d312b-108">The **Get-AzAutomationDscConfiguration** cmdlet gets APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="d312b-109">예제</span><span class="sxs-lookup"><span data-stu-id="d312b-109">EXAMPLES</span></span>

### <span data-ttu-id="d312b-110">예제 1: 모든 DSC 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d312b-110">Example 1: Get all DSC configurations</span></span>
```
PS C:\>Get-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="d312b-111">이 명령은 Contoso17이라는 Automation 계정의 모든 DSC 구성에 대한 메타데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d312b-111">This command gets metadata for all DSC configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="d312b-112">예제 2: 이름에 따라 DSC 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d312b-112">Example 2: Get a DSC configuration by name</span></span>
```
PS C:\>Get-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration"
```

<span data-ttu-id="d312b-113">이 명령은 Contoso17이라는 Automation 계정에서 MyConfiguration이라는 DSC 구성에 대한 메타데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d312b-113">This command gets metadata for a DSC configuration named MyConfiguration in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="d312b-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d312b-114">PARAMETERS</span></span>

### <span data-ttu-id="d312b-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d312b-115">-AutomationAccountName</span></span>
<span data-ttu-id="d312b-116">이 cmdlet에서 얻을 DSC 구성을 포함하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d312b-116">Specifies the name of the Automation account that contains DSC configurations that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d312b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d312b-117">-DefaultProfile</span></span>
<span data-ttu-id="d312b-118">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d312b-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d312b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d312b-119">-Name</span></span>
<span data-ttu-id="d312b-120">이 cmdlet에서 얻을 DSC 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d312b-120">Specifies the name of the DSC configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d312b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d312b-121">-ResourceGroupName</span></span>
<span data-ttu-id="d312b-122">이 cmdlet에서 DSC 구성을 얻을 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d312b-122">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="d312b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d312b-123">CommonParameters</span></span>
<span data-ttu-id="d312b-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d312b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d312b-125">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d312b-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d312b-126">입력</span><span class="sxs-lookup"><span data-stu-id="d312b-126">INPUTS</span></span>

### <span data-ttu-id="d312b-127">System.String</span><span class="sxs-lookup"><span data-stu-id="d312b-127">System.String</span></span>

## <span data-ttu-id="d312b-128">출력</span><span class="sxs-lookup"><span data-stu-id="d312b-128">OUTPUTS</span></span>

### <span data-ttu-id="d312b-129">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="d312b-129">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="d312b-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d312b-130">NOTES</span></span>

## <span data-ttu-id="d312b-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d312b-131">RELATED LINKS</span></span>

[<span data-ttu-id="d312b-132">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="d312b-132">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="d312b-133">Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="d312b-133">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


