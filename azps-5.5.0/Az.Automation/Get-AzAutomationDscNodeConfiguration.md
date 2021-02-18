---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 89C931AE-DA81-47A7-80E4-159C36497DA0
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: 1114d0a78518c33126f28fb4b409a881a52a4ae7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201177"
---
# <span data-ttu-id="f05f4-101">Get-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="f05f4-101">Get-AzAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="f05f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f05f4-102">SYNOPSIS</span></span>
<span data-ttu-id="f05f4-103">Automation에서 DSC 노드 구성에 대한 메타데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f05f4-103">Gets metadata for DSC node configurations in Automation.</span></span>

## <span data-ttu-id="f05f4-104">구문</span><span class="sxs-lookup"><span data-stu-id="f05f4-104">SYNTAX</span></span>

### <span data-ttu-id="f05f4-105">ByAll(기본값)</span><span class="sxs-lookup"><span data-stu-id="f05f4-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfiguration [-RollupStatus <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f05f4-106">ByNodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f05f4-106">ByNodeConfigurationName</span></span>
```
Get-AzAutomationDscNodeConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f05f4-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f05f4-107">ByConfigurationName</span></span>
```
Get-AzAutomationDscNodeConfiguration -ConfigurationName <String> [-RollupStatus <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f05f4-108">설명</span><span class="sxs-lookup"><span data-stu-id="f05f4-108">DESCRIPTION</span></span>
<span data-ttu-id="f05f4-109">**Get-AzAutomationDscNodeConfiguration** cmdlet은 Azure Automation에서 APS DSC(필요한 상태 구성) 노드 구성에 대한 메타데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f05f4-109">The **Get-AzAutomationDscNodeConfiguration** cmdlet gets metadata for APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="f05f4-110">Automation은 DSC 노드 구성을 MOF(관리 개체 형식) 구성 문서로 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="f05f4-110">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="f05f4-111">예제</span><span class="sxs-lookup"><span data-stu-id="f05f4-111">EXAMPLES</span></span>

### <span data-ttu-id="f05f4-112">예제 1: 모든 DSC 노드 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f05f4-112">Example 1: Get all DSC node configurations</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="f05f4-113">이 명령은 Contoso17이라는 Automation 계정의 모든 DSC 노드 구성에 대한 메타데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f05f4-113">This command gets metadata for all DSC node configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="f05f4-114">예제 2: DSC 구성에 대한 모든 DSC 노드 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f05f4-114">Example 2: Get all DSC node configurations for a DSC configuration</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="f05f4-115">이 명령은 ContosoConfiguration이라는 DSC 구성이 생성한 Contoso17 Automation 계정의 모든 DSC 노드 구성에 대한 메타데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f05f4-115">This command gets metadata for all DSC node configurations in the Automation account named Contoso17 that the DSC configuration named ContosoConfiguration generated.</span></span>

### <span data-ttu-id="f05f4-116">예제 3: 이름으로 DSC 노드 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f05f4-116">Example 3: Get a DSC node configuration by name</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration.webserver"
```

<span data-ttu-id="f05f4-117">이 명령은 Contoso17이라는 Automation 계정에서 ContosoConfiguration.webserver라는 이름으로 DSC 노드 구성에 대한 메타데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f05f4-117">This command gets metadata for a DSC node configuration with the name ContosoConfiguration.webserver in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="f05f4-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f05f4-118">PARAMETERS</span></span>

### <span data-ttu-id="f05f4-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f05f4-119">-AutomationAccountName</span></span>
<span data-ttu-id="f05f4-120">이 cmdlet에서 메타데이터를 얻을 DSC 노드 구성을 포함하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f05f4-120">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="f05f4-121">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f05f4-121">-ConfigurationName</span></span>
<span data-ttu-id="f05f4-122">이 cmdlet이 노드 구성 메타데이터를 얻을 DSC 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f05f4-122">Specifies the name of DSC configuration for which this cmdlet gets node configuration metadata.</span></span>

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

### <span data-ttu-id="f05f4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f05f4-123">-DefaultProfile</span></span>
<span data-ttu-id="f05f4-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f05f4-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f05f4-125">-Name</span><span class="sxs-lookup"><span data-stu-id="f05f4-125">-Name</span></span>
<span data-ttu-id="f05f4-126">이 cmdlet이 메타데이터를 얻을 DSC 노드 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f05f4-126">Specifies the name of the DSC node configuration for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="f05f4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f05f4-127">-ResourceGroupName</span></span>
<span data-ttu-id="f05f4-128">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f05f4-128">Specifies the name of a resource group.</span></span>
<span data-ttu-id="f05f4-129">이 cmdlet은 이 매개 변수가 지정하는 리소스 그룹의 DSC 노드 구성에 대한 메타데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f05f4-129">This cmdlet gets metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f05f4-130">-RollupStatus</span><span class="sxs-lookup"><span data-stu-id="f05f4-130">-RollupStatus</span></span>
<span data-ttu-id="f05f4-131">이 cmdlet에서 얻을 DSC 노드 구성의 롤업 상태를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f05f4-131">Specifies the rollup status of DSC node configurations that this cmdlet gets.</span></span>
<span data-ttu-id="f05f4-132">유효한 값은</span><span class="sxs-lookup"><span data-stu-id="f05f4-132">Valid values are:</span></span> 
- <span data-ttu-id="f05f4-133">Bad</span><span class="sxs-lookup"><span data-stu-id="f05f4-133">Bad</span></span> 
- <span data-ttu-id="f05f4-134">좋음</span><span class="sxs-lookup"><span data-stu-id="f05f4-134">Good</span></span>

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

### <span data-ttu-id="f05f4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f05f4-135">CommonParameters</span></span>
<span data-ttu-id="f05f4-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f05f4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f05f4-137">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f05f4-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f05f4-138">입력</span><span class="sxs-lookup"><span data-stu-id="f05f4-138">INPUTS</span></span>

### <span data-ttu-id="f05f4-139">System.String</span><span class="sxs-lookup"><span data-stu-id="f05f4-139">System.String</span></span>

## <span data-ttu-id="f05f4-140">출력</span><span class="sxs-lookup"><span data-stu-id="f05f4-140">OUTPUTS</span></span>

### <span data-ttu-id="f05f4-141">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span><span class="sxs-lookup"><span data-stu-id="f05f4-141">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="f05f4-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f05f4-142">NOTES</span></span>

## <span data-ttu-id="f05f4-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f05f4-143">RELATED LINKS</span></span>

[<span data-ttu-id="f05f4-144">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="f05f4-144">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)


