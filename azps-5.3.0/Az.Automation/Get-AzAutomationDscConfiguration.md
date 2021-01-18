---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BBD37C4B-BB6F-4560-BDEE-F0440EC1938A
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscConfiguration.md
ms.openlocfilehash: 0616cb9f2a379e93a01b450ab8a66da95ca9add1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494346"
---
# <span data-ttu-id="08d90-101">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="08d90-101">Get-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="08d90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08d90-102">SYNOPSIS</span></span>
<span data-ttu-id="08d90-103">Automation에서 DSC 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="08d90-103">Gets DSC configurations from Automation.</span></span>

## <span data-ttu-id="08d90-104">구문</span><span class="sxs-lookup"><span data-stu-id="08d90-104">SYNTAX</span></span>

### <span data-ttu-id="08d90-105">ByAll(기본값)</span><span class="sxs-lookup"><span data-stu-id="08d90-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08d90-106">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="08d90-106">ByConfigurationName</span></span>
```
Get-AzAutomationDscConfiguration [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08d90-107">설명</span><span class="sxs-lookup"><span data-stu-id="08d90-107">DESCRIPTION</span></span>
<span data-ttu-id="08d90-108">**Get-AzAutomationDscConfiguration** cmdlet은 Azure Automation에서 APS DSC(Desired State Configuration) 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="08d90-108">The **Get-AzAutomationDscConfiguration** cmdlet gets APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="08d90-109">예제</span><span class="sxs-lookup"><span data-stu-id="08d90-109">EXAMPLES</span></span>

### <span data-ttu-id="08d90-110">예제 1: 모든 DSC 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="08d90-110">Example 1: Get all DSC configurations</span></span>
```
PS C:\>Get-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="08d90-111">이 명령은 Contoso17이라는 Automation 계정의 모든 DSC 구성에 대한 메타데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="08d90-111">This command gets metadata for all DSC configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="08d90-112">예제 2: 이름으로 DSC 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="08d90-112">Example 2: Get a DSC configuration by name</span></span>
```
PS C:\>Get-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration"
```

<span data-ttu-id="08d90-113">이 명령은 Contoso17이라는 Automation 계정에서 MyConfiguration이라는 DSC 구성에 대한 메타데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="08d90-113">This command gets metadata for a DSC configuration named MyConfiguration in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="08d90-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="08d90-114">PARAMETERS</span></span>

### <span data-ttu-id="08d90-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="08d90-115">-AutomationAccountName</span></span>
<span data-ttu-id="08d90-116">이 cmdlet에서 얻을 DSC 구성을 포함하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="08d90-116">Specifies the name of the Automation account that contains DSC configurations that this cmdlet gets.</span></span>

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

### <span data-ttu-id="08d90-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08d90-117">-DefaultProfile</span></span>
<span data-ttu-id="08d90-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="08d90-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="08d90-119">-Name</span><span class="sxs-lookup"><span data-stu-id="08d90-119">-Name</span></span>
<span data-ttu-id="08d90-120">이 cmdlet에서 얻을 DSC 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="08d90-120">Specifies the name of the DSC configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="08d90-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08d90-121">-ResourceGroupName</span></span>
<span data-ttu-id="08d90-122">이 cmdlet이 DSC 구성을 얻을 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="08d90-122">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="08d90-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08d90-123">CommonParameters</span></span>
<span data-ttu-id="08d90-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="08d90-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08d90-125">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="08d90-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08d90-126">입력</span><span class="sxs-lookup"><span data-stu-id="08d90-126">INPUTS</span></span>

### <span data-ttu-id="08d90-127">System.String</span><span class="sxs-lookup"><span data-stu-id="08d90-127">System.String</span></span>

## <span data-ttu-id="08d90-128">출력</span><span class="sxs-lookup"><span data-stu-id="08d90-128">OUTPUTS</span></span>

### <span data-ttu-id="08d90-129">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="08d90-129">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="08d90-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="08d90-130">NOTES</span></span>

## <span data-ttu-id="08d90-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="08d90-131">RELATED LINKS</span></span>

[<span data-ttu-id="08d90-132">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="08d90-132">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="08d90-133">Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="08d90-133">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


