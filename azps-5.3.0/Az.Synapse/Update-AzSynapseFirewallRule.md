---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseFirewallRule.md
ms.openlocfilehash: 9188a1cc8dde39db4d755fb2059f3633fc85ead8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494628"
---
# <span data-ttu-id="445e9-101">Update-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="445e9-101">Update-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="445e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="445e9-102">SYNOPSIS</span></span>
<span data-ttu-id="445e9-103">Synapse 분석 방화벽 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="445e9-103">Updates a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="445e9-104">구문</span><span class="sxs-lookup"><span data-stu-id="445e9-104">SYNTAX</span></span>

### <span data-ttu-id="445e9-105">UpdateByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="445e9-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-StartIpAddress <String>] [-EndIpAddress <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="445e9-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="445e9-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-StartIpAddress <String>]
 [-EndIpAddress <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="445e9-107">설명</span><span class="sxs-lookup"><span data-stu-id="445e9-107">DESCRIPTION</span></span>
<span data-ttu-id="445e9-108">**Update-AzSynapseFirewallRule** cmdlet은 Azure Synapse Analytics 방화벽 규칙을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="445e9-108">The **Update-AzSynapseFirewallRule** cmdlet modifys an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="445e9-109">예제</span><span class="sxs-lookup"><span data-stu-id="445e9-109">EXAMPLES</span></span>

### <span data-ttu-id="445e9-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="445e9-110">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAssdress "255.255.255.255"
```

<span data-ttu-id="445e9-111">이 명령은 작업 영역 ContosoWorkspace에서 ContosoFirewallRule이라는 방화벽 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="445e9-111">This command updates firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="445e9-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="445e9-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseFirewallRule -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAssdress "255.255.255.255"
```

<span data-ttu-id="445e9-113">이 명령은 파이프라인을 통해 작업 영역 아래에 ContosoFirewallRule이라는 방화벽 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="445e9-113">This command updates firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

## <span data-ttu-id="445e9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="445e9-114">PARAMETERS</span></span>

### <span data-ttu-id="445e9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="445e9-115">-AsJob</span></span>
<span data-ttu-id="445e9-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="445e9-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="445e9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="445e9-117">-DefaultProfile</span></span>
<span data-ttu-id="445e9-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="445e9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="445e9-119">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="445e9-119">-EndIpAddress</span></span>
<span data-ttu-id="445e9-120">방화벽 규칙의 끝 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="445e9-120">The end IP address of the firewall rule.</span></span>
<span data-ttu-id="445e9-121">IPv4 형식이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="445e9-121">Must be IPv4 format.</span></span>
<span data-ttu-id="445e9-122">startIpAddress보다 크거나 같아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="445e9-122">Must be greater than or equal to startIpAddress.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="445e9-123">-Name</span><span class="sxs-lookup"><span data-stu-id="445e9-123">-Name</span></span>
<span data-ttu-id="445e9-124">작업 영역의 firerwall 규칙 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="445e9-124">The firerwall rule name for the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="445e9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="445e9-125">-ResourceGroupName</span></span>
<span data-ttu-id="445e9-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="445e9-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="445e9-127">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="445e9-127">-StartIpAddress</span></span>
<span data-ttu-id="445e9-128">방화벽 규칙의 시작 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="445e9-128">The start IP address of the firewall rule.</span></span>
<span data-ttu-id="445e9-129">IPv4 형식이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="445e9-129">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="445e9-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="445e9-130">-WorkspaceName</span></span>
<span data-ttu-id="445e9-131">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="445e9-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="445e9-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="445e9-132">-WorkspaceObject</span></span>
<span data-ttu-id="445e9-133">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="445e9-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="445e9-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="445e9-134">-Confirm</span></span>
<span data-ttu-id="445e9-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="445e9-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="445e9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="445e9-136">-WhatIf</span></span>
<span data-ttu-id="445e9-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="445e9-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="445e9-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="445e9-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="445e9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="445e9-139">CommonParameters</span></span>
<span data-ttu-id="445e9-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="445e9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="445e9-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="445e9-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="445e9-142">입력</span><span class="sxs-lookup"><span data-stu-id="445e9-142">INPUTS</span></span>

### <span data-ttu-id="445e9-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="445e9-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="445e9-144">출력</span><span class="sxs-lookup"><span data-stu-id="445e9-144">OUTPUTS</span></span>

### <span data-ttu-id="445e9-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="445e9-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="445e9-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="445e9-146">NOTES</span></span>

## <span data-ttu-id="445e9-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="445e9-147">RELATED LINKS</span></span>
