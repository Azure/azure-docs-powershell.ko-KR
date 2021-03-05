---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 89C931AE-DA81-47A7-80E4-159C36497DA0
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: b139ed5b67bbc36bad45ab2528ed74299d40c1b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969712"
---
# <span data-ttu-id="af04a-101">Get-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="af04a-101">Get-AzAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="af04a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af04a-102">SYNOPSIS</span></span>
<span data-ttu-id="af04a-103">Automation에서 DSC 노드 구성에 대한 메타데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="af04a-103">Gets metadata for DSC node configurations in Automation.</span></span>

## <span data-ttu-id="af04a-104">구문</span><span class="sxs-lookup"><span data-stu-id="af04a-104">SYNTAX</span></span>

### <span data-ttu-id="af04a-105">ByAll(기본값)</span><span class="sxs-lookup"><span data-stu-id="af04a-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfiguration [-RollupStatus <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af04a-106">ByNodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="af04a-106">ByNodeConfigurationName</span></span>
```
Get-AzAutomationDscNodeConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af04a-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="af04a-107">ByConfigurationName</span></span>
```
Get-AzAutomationDscNodeConfiguration -ConfigurationName <String> [-RollupStatus <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="af04a-108">설명</span><span class="sxs-lookup"><span data-stu-id="af04a-108">DESCRIPTION</span></span>
<span data-ttu-id="af04a-109">**Get-AzAutomationDscNodeConfiguration** cmdlet은 Azure Automation의 APS 원하는 상태 구성(DSC) 노드 구성에 대한 메타데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="af04a-109">The **Get-AzAutomationDscNodeConfiguration** cmdlet gets metadata for APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="af04a-110">Automation은 DSC 노드 구성을 MOF(관리 개체 형식) 구성 문서로 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="af04a-110">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="af04a-111">예제</span><span class="sxs-lookup"><span data-stu-id="af04a-111">EXAMPLES</span></span>

### <span data-ttu-id="af04a-112">예제 1: 모든 DSC 노드 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="af04a-112">Example 1: Get all DSC node configurations</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="af04a-113">이 명령은 Contoso17이라는 Automation 계정의 모든 DSC 노드 구성에 대한 메타데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="af04a-113">This command gets metadata for all DSC node configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="af04a-114">예제 2: DSC 구성에 대한 모든 DSC 노드 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="af04a-114">Example 2: Get all DSC node configurations for a DSC configuration</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="af04a-115">이 명령은 ContosoConfiguration이라는 DSC 구성이 생성된 Contoso17이라는 Automation 계정의 모든 DSC 노드 구성에 대한 메타데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="af04a-115">This command gets metadata for all DSC node configurations in the Automation account named Contoso17 that the DSC configuration named ContosoConfiguration generated.</span></span>

### <span data-ttu-id="af04a-116">예제 3: 이름에 따라 DSC 노드 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="af04a-116">Example 3: Get a DSC node configuration by name</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration.webserver"
```

<span data-ttu-id="af04a-117">이 명령은 Contoso17이라는 Automation 계정에서 ContosoConfiguration.webserver라는 이름으로 DSC 노드 구성에 대한 메타데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="af04a-117">This command gets metadata for a DSC node configuration with the name ContosoConfiguration.webserver in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="af04a-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="af04a-118">PARAMETERS</span></span>

### <span data-ttu-id="af04a-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="af04a-119">-AutomationAccountName</span></span>
<span data-ttu-id="af04a-120">이 cmdlet에서 메타데이터를 얻을 수 있는 DSC 노드 구성을 포함하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="af04a-120">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="af04a-121">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="af04a-121">-ConfigurationName</span></span>
<span data-ttu-id="af04a-122">이 cmdlet에서 노드 구성 메타데이터를 얻을 DSC 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="af04a-122">Specifies the name of DSC configuration for which this cmdlet gets node configuration metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af04a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af04a-123">-DefaultProfile</span></span>
<span data-ttu-id="af04a-124">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="af04a-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af04a-125">-Name</span><span class="sxs-lookup"><span data-stu-id="af04a-125">-Name</span></span>
<span data-ttu-id="af04a-126">이 cmdlet에서 메타데이터를 얻을 DSC 노드 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="af04a-126">Specifies the name of the DSC node configuration for which this cmdlet gets metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeConfigurationName
Aliases: NodeConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af04a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af04a-127">-ResourceGroupName</span></span>
<span data-ttu-id="af04a-128">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="af04a-128">Specifies the name of a resource group.</span></span>
<span data-ttu-id="af04a-129">이 cmdlet은 이 매개 변수가 지정하는 리소스 그룹의 DSC 노드 구성에 대한 메타데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="af04a-129">This cmdlet gets metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="af04a-130">-RollupStatus</span><span class="sxs-lookup"><span data-stu-id="af04a-130">-RollupStatus</span></span>
<span data-ttu-id="af04a-131">이 cmdlet이 얻을 DSC 노드 구성의 롤업 상태를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="af04a-131">Specifies the rollup status of DSC node configurations that this cmdlet gets.</span></span>
<span data-ttu-id="af04a-132">유효한 값은:</span><span class="sxs-lookup"><span data-stu-id="af04a-132">Valid values are:</span></span> 
- <span data-ttu-id="af04a-133">잘못된</span><span class="sxs-lookup"><span data-stu-id="af04a-133">Bad</span></span> 
- <span data-ttu-id="af04a-134">좋음</span><span class="sxs-lookup"><span data-stu-id="af04a-134">Good</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, ByConfigurationName
Aliases:
Accepted values: Good, Bad

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af04a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af04a-135">CommonParameters</span></span>
<span data-ttu-id="af04a-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="af04a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af04a-137">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="af04a-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af04a-138">입력</span><span class="sxs-lookup"><span data-stu-id="af04a-138">INPUTS</span></span>

### <span data-ttu-id="af04a-139">System.String</span><span class="sxs-lookup"><span data-stu-id="af04a-139">System.String</span></span>

## <span data-ttu-id="af04a-140">출력</span><span class="sxs-lookup"><span data-stu-id="af04a-140">OUTPUTS</span></span>

### <span data-ttu-id="af04a-141">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span><span class="sxs-lookup"><span data-stu-id="af04a-141">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="af04a-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="af04a-142">NOTES</span></span>

## <span data-ttu-id="af04a-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="af04a-143">RELATED LINKS</span></span>

[<span data-ttu-id="af04a-144">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="af04a-144">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)


