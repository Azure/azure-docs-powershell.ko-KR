---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseFirewallRule.md
ms.openlocfilehash: b4579d01ed6dd5a7d742cbb82afb424151579772
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360893"
---
# <span data-ttu-id="79803-101">New-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="79803-101">New-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="79803-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79803-102">SYNOPSIS</span></span>
<span data-ttu-id="79803-103">Synapse 분석 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="79803-103">Creates a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="79803-104">구문</span><span class="sxs-lookup"><span data-stu-id="79803-104">SYNTAX</span></span>

### <span data-ttu-id="79803-105">CreateByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="79803-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -StartIpAddress <String> -EndIpAddress <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79803-106">CreateByNameAllowAllIpParameterSet</span><span class="sxs-lookup"><span data-stu-id="79803-106">CreateByNameAllowAllIpParameterSet</span></span>
```
New-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> [-AllowAllAzureIP] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79803-107">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="79803-107">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> -Name <String> -StartIpAddress <String>
 -EndIpAddress <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="79803-108">CreateByParentObjectAllowAllIpParameterSet</span><span class="sxs-lookup"><span data-stu-id="79803-108">CreateByParentObjectAllowAllIpParameterSet</span></span>
```
New-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> [-AllowAllAzureIP] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79803-109">설명</span><span class="sxs-lookup"><span data-stu-id="79803-109">DESCRIPTION</span></span>
<span data-ttu-id="79803-110">**New-AzSynapseFirewallRule** cmdlet은 Azure Synapse Analytics 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="79803-110">The **New-AzSynapseFirewallRule** cmdlet creates an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="79803-111">예제</span><span class="sxs-lookup"><span data-stu-id="79803-111">EXAMPLES</span></span>

### <span data-ttu-id="79803-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="79803-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseFirewallRule -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAddress "255.255.255.255"
```

<span data-ttu-id="79803-113">이 명령은 ContosoFirewallRule이라는 이름의 작업 영역 ContosoWorkspace 아래에 ContosoFirewallRule이라는 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="79803-113">This command creates firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="79803-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="79803-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseFirewallRule -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAddress "255.255.255.255"
```

<span data-ttu-id="79803-115">이 명령은 파이프라인을 통해 작업 영역 아래에 ContosoFirewallRule이라는 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="79803-115">This command creates firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

### <span data-ttu-id="79803-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="79803-116">Example 3</span></span>
```powershell
PS C:\> New-AzSynapseFirewallRule -WorkspaceName ContosoWorkspace -AllowAllAzureIP
```

<span data-ttu-id="79803-117">이 명령은 작업 영역의 모든 Azure IP를 허용하는 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="79803-117">This command creates firewall rule that allow all azure ips under a workspace.</span></span>

## <span data-ttu-id="79803-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79803-118">PARAMETERS</span></span>

### <span data-ttu-id="79803-119">-AllowAllAzureIP</span><span class="sxs-lookup"><span data-stu-id="79803-119">-AllowAllAzureIP</span></span>
<span data-ttu-id="79803-120">모든 Azure IP가 액세스를 허용하는 특수 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="79803-120">Creates a special firewall rule that permits all Azure IPs to have access.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateByNameAllowAllIpParameterSet, CreateByParentObjectAllowAllIpParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79803-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79803-121">-AsJob</span></span>
<span data-ttu-id="79803-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="79803-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="79803-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79803-123">-DefaultProfile</span></span>
<span data-ttu-id="79803-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="79803-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79803-125">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="79803-125">-EndIpAddress</span></span>
<span data-ttu-id="79803-126">방화벽 규칙의 끝 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="79803-126">The end IP address of the firewall rule.</span></span>
<span data-ttu-id="79803-127">IPv4 형식이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="79803-127">Must be IPv4 format.</span></span>
<span data-ttu-id="79803-128">startIpAddress보다 크거나 같아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="79803-128">Must be greater than or equal to startIpAddress.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79803-129">-Name</span><span class="sxs-lookup"><span data-stu-id="79803-129">-Name</span></span>
<span data-ttu-id="79803-130">작업 영역의 firerwall 규칙 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="79803-130">The firerwall rule name for the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79803-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79803-131">-ResourceGroupName</span></span>
<span data-ttu-id="79803-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="79803-132">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByNameAllowAllIpParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79803-133">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="79803-133">-StartIpAddress</span></span>
<span data-ttu-id="79803-134">방화벽 규칙의 시작 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="79803-134">The start IP address of the firewall rule.</span></span>
<span data-ttu-id="79803-135">IPv4 형식이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="79803-135">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79803-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="79803-136">-WorkspaceName</span></span>
<span data-ttu-id="79803-137">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="79803-137">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByNameAllowAllIpParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79803-138">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="79803-138">-WorkspaceObject</span></span>
<span data-ttu-id="79803-139">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="79803-139">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateByParentObjectParameterSet, CreateByParentObjectAllowAllIpParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79803-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79803-140">-Confirm</span></span>
<span data-ttu-id="79803-141">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="79803-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79803-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79803-142">-WhatIf</span></span>
<span data-ttu-id="79803-143">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="79803-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79803-144">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="79803-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79803-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79803-145">CommonParameters</span></span>
<span data-ttu-id="79803-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="79803-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79803-147">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="79803-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79803-148">입력</span><span class="sxs-lookup"><span data-stu-id="79803-148">INPUTS</span></span>

### <span data-ttu-id="79803-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="79803-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="79803-150">출력</span><span class="sxs-lookup"><span data-stu-id="79803-150">OUTPUTS</span></span>

### <span data-ttu-id="79803-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="79803-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="79803-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="79803-152">NOTES</span></span>

## <span data-ttu-id="79803-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="79803-153">RELATED LINKS</span></span>
