---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0C35E679-B991-49A8-890F-C8DAB68A8240
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: d02338c34584a68ece2ad3a90887a765f8142347
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336518"
---
# <span data-ttu-id="eda09-101">Remove-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="eda09-101">Remove-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="eda09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eda09-102">SYNOPSIS</span></span>
<span data-ttu-id="eda09-103">작업 영역이 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="eda09-103">Removes a workspace.</span></span>

## <span data-ttu-id="eda09-104">구문</span><span class="sxs-lookup"><span data-stu-id="eda09-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-ForceDelete] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eda09-105">설명</span><span class="sxs-lookup"><span data-stu-id="eda09-105">DESCRIPTION</span></span>
<span data-ttu-id="eda09-106">**Remove-AzOperationalInsightsWorkspace** cmdlet은 기존 작업 영역이 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="eda09-106">The **Remove-AzOperationalInsightsWorkspace** cmdlet deletes an existing workspace.</span></span>
<span data-ttu-id="eda09-107">이 작업 영역이 생성 시 *CustomerId* 매개 변수를 통해 기존 계정에 연결된 경우 Operational Insights 포털에서 원래 계정이 삭제되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eda09-107">If this workspace was linked to an existing account via the *CustomerId* parameter at creation time the original account is not deleted in the Operational Insights portal.</span></span>

## <span data-ttu-id="eda09-108">예제</span><span class="sxs-lookup"><span data-stu-id="eda09-108">EXAMPLES</span></span>

### <span data-ttu-id="eda09-109">예제 1: 이름으로 작업 영역 제거</span><span class="sxs-lookup"><span data-stu-id="eda09-109">Example 1: Remove a workspace by name</span></span>
```
PS C:\>Remove-AzOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="eda09-110">이 명령은 ContosoResourceGroup이라는 리소스 그룹에서 MyWorkspace라는 작업 영역이 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="eda09-110">This command removes the workspace named MyWorkspace from the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="eda09-111">예제 2: 확인 없이 파이프라인을 사용하여 작업 영역 제거</span><span class="sxs-lookup"><span data-stu-id="eda09-111">Example 2: Remove a workspace by using the pipeline and without confirmation</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace" | Remove-AzOperationalInsightsWorkspace -Force
```

<span data-ttu-id="eda09-112">이 명령은 Get-AzOperationalInsightsWorkspace cmdlet을 사용하여 MyWorkspace라는 작업 영역이 있는 다음 파이프라인 연산자를 사용하여 **Remove-AzOperationalInsightsWorkspace** cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="eda09-112">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes it to the **Remove-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator to remove it.</span></span>
<span data-ttu-id="eda09-113">Force *매개* 변수가 지정되어 있는 경우 작업 영역 제거 전에 명령에 메시지가 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eda09-113">Since the *Force* parameter is specified, the command does not prompt you before removing the workspace.</span></span>

### <span data-ttu-id="eda09-114">예제 3: 강제 삭제 작업 영역(복구할 수 없습니다)</span><span class="sxs-lookup"><span data-stu-id="eda09-114">Example 3: Force delete workspace (cannot be recovered)</span></span>
```
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace -ForceDelete
```

<span data-ttu-id="eda09-115">작업 영역 강제 삭제</span><span class="sxs-lookup"><span data-stu-id="eda09-115">Force delete a workspace.</span></span>

## <span data-ttu-id="eda09-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eda09-116">PARAMETERS</span></span>

### <span data-ttu-id="eda09-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eda09-117">-DefaultProfile</span></span>
<span data-ttu-id="eda09-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="eda09-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eda09-119">-Force</span><span class="sxs-lookup"><span data-stu-id="eda09-119">-Force</span></span>
<span data-ttu-id="eda09-120">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="eda09-120">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eda09-121">-ForceDelete</span><span class="sxs-lookup"><span data-stu-id="eda09-121">-ForceDelete</span></span>
<span data-ttu-id="eda09-122">작업 영역 강제 삭제</span><span class="sxs-lookup"><span data-stu-id="eda09-122">Force delete workspace.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eda09-123">-Name</span><span class="sxs-lookup"><span data-stu-id="eda09-123">-Name</span></span>
<span data-ttu-id="eda09-124">작업 영역의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="eda09-124">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="eda09-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eda09-125">-ResourceGroupName</span></span>
<span data-ttu-id="eda09-126">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="eda09-126">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="eda09-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eda09-127">-Confirm</span></span>
<span data-ttu-id="eda09-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="eda09-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eda09-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eda09-129">-WhatIf</span></span>
<span data-ttu-id="eda09-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="eda09-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eda09-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eda09-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eda09-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eda09-132">CommonParameters</span></span>
<span data-ttu-id="eda09-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="eda09-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eda09-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="eda09-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eda09-135">입력</span><span class="sxs-lookup"><span data-stu-id="eda09-135">INPUTS</span></span>

### <span data-ttu-id="eda09-136">System.String</span><span class="sxs-lookup"><span data-stu-id="eda09-136">System.String</span></span>

## <span data-ttu-id="eda09-137">출력</span><span class="sxs-lookup"><span data-stu-id="eda09-137">OUTPUTS</span></span>

### <span data-ttu-id="eda09-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="eda09-138">System.Void</span></span>

## <span data-ttu-id="eda09-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="eda09-139">NOTES</span></span>

## <span data-ttu-id="eda09-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eda09-140">RELATED LINKS</span></span>

[<span data-ttu-id="eda09-141">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eda09-141">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="eda09-142">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="eda09-142">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


