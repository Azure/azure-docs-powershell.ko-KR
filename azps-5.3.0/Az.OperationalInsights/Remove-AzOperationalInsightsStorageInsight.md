---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 92261663-CF50-4EBD-85D2-C2E254F39B41
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: ac9e061fea8c6d7737eb268feec225dff0b0924d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496312"
---
# <span data-ttu-id="df153-101">Remove-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="df153-101">Remove-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="df153-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df153-102">SYNOPSIS</span></span>
<span data-ttu-id="df153-103">Storage 인사이트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="df153-103">Removes a Storage Insight.</span></span>

## <span data-ttu-id="df153-104">구문</span><span class="sxs-lookup"><span data-stu-id="df153-104">SYNTAX</span></span>

### <span data-ttu-id="df153-105">ByWorkspaceName(기본값)</span><span class="sxs-lookup"><span data-stu-id="df153-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df153-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="df153-106">ByWorkspaceObject</span></span>
```
Remove-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df153-107">설명</span><span class="sxs-lookup"><span data-stu-id="df153-107">DESCRIPTION</span></span>
<span data-ttu-id="df153-108">**Remove-AzOperationalInsightsStorageInsight** cmdlet은 작업 영역의 Storage Insight를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="df153-108">The **Remove-AzOperationalInsightsStorageInsight** cmdlet deletes a Storage Insight from a workspace.</span></span>

## <span data-ttu-id="df153-109">예제</span><span class="sxs-lookup"><span data-stu-id="df153-109">EXAMPLES</span></span>

### <span data-ttu-id="df153-110">예제 1: 이름으로 Storage 인사이트 제거</span><span class="sxs-lookup"><span data-stu-id="df153-110">Example 1: Remove a Storage Insight by name</span></span>
```
PS C:\>Remove-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight"
```

<span data-ttu-id="df153-111">이 명령은 지정된 리소스 그룹의 MyWorkspace라는 작업 영역에서 MyStorageInsight라는 Storage Insight를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="df153-111">This command removes the Storage Insight named MyStorageInsight from the workspace named MyWorkspace in the specified resource group.</span></span>
<span data-ttu-id="df153-112">이 명령은 Force 매개 변수를 지정하지 않습니다. *따라서* Storage Insight를 제거하기 전에 확인하라는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="df153-112">The command does not specify the *Force* parameter, so it prompts you for confirmation before removing the Storage Insight.</span></span>

### <span data-ttu-id="df153-113">예제 2: 확인 없이 Storage 인사이트 제거</span><span class="sxs-lookup"><span data-stu-id="df153-113">Example 2: Remove a Storage Insight without confirmation</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Remove-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Force
```

<span data-ttu-id="df153-114">첫 번째 명령은 Get-AzOperationalInsightsWorkspace cmdlet을 사용하여 MyWorkspace라는 작업 영역이 있는 다음, $Workspace 변수에 저장합니다. 두 번째 명령은 확인 메시지를 표시하지 않고 $Workspace MyStorageInsight라는 저장소 인사이트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="df153-114">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.The second command removes the storage insight named MyStorageInsight from $Workspace without prompting you for confirmation.</span></span>

## <span data-ttu-id="df153-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df153-115">PARAMETERS</span></span>

### <span data-ttu-id="df153-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df153-116">-DefaultProfile</span></span>
<span data-ttu-id="df153-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="df153-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df153-118">-Force</span><span class="sxs-lookup"><span data-stu-id="df153-118">-Force</span></span>
<span data-ttu-id="df153-119">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="df153-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="df153-120">-Name</span><span class="sxs-lookup"><span data-stu-id="df153-120">-Name</span></span>
<span data-ttu-id="df153-121">Storage 인사이트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="df153-121">Specifies the name of the Storage Insight.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df153-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df153-122">-ResourceGroupName</span></span>
<span data-ttu-id="df153-123">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="df153-123">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df153-124">-Workspace</span><span class="sxs-lookup"><span data-stu-id="df153-124">-Workspace</span></span>
<span data-ttu-id="df153-125">Storage 인사이트를 포함하는 작업 공간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="df153-125">Specifies the workspace that contains the Storage Insight.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df153-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="df153-126">-WorkspaceName</span></span>
<span data-ttu-id="df153-127">Storage Insight를 포함하는 작업 영역의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="df153-127">Specifies the name of the workspace that contains the Storage Insight.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df153-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df153-128">-Confirm</span></span>
<span data-ttu-id="df153-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="df153-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df153-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df153-130">-WhatIf</span></span>
<span data-ttu-id="df153-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="df153-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df153-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="df153-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df153-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df153-133">CommonParameters</span></span>
<span data-ttu-id="df153-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="df153-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df153-135">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="df153-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df153-136">입력</span><span class="sxs-lookup"><span data-stu-id="df153-136">INPUTS</span></span>

### <span data-ttu-id="df153-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="df153-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="df153-138">System.String</span><span class="sxs-lookup"><span data-stu-id="df153-138">System.String</span></span>

## <span data-ttu-id="df153-139">출력</span><span class="sxs-lookup"><span data-stu-id="df153-139">OUTPUTS</span></span>

### <span data-ttu-id="df153-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="df153-140">System.Void</span></span>

## <span data-ttu-id="df153-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="df153-141">NOTES</span></span>

## <span data-ttu-id="df153-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="df153-142">RELATED LINKS</span></span>

[<span data-ttu-id="df153-143">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="df153-143">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="df153-144">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="df153-144">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


