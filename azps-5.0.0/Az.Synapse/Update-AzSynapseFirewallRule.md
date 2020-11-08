---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseFirewallRule.md
ms.openlocfilehash: 9188a1cc8dde39db4d755fb2059f3633fc85ead8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215143"
---
# <span data-ttu-id="1746f-101">Update-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1746f-101">Update-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="1746f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1746f-102">SYNOPSIS</span></span>
<span data-ttu-id="1746f-103">Synapse Analytics 방화벽 규칙을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1746f-103">Updates a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="1746f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1746f-104">SYNTAX</span></span>

### <span data-ttu-id="1746f-105">UpdateByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="1746f-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-StartIpAddress <String>] [-EndIpAddress <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1746f-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1746f-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-StartIpAddress <String>]
 [-EndIpAddress <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1746f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1746f-107">DESCRIPTION</span></span>
<span data-ttu-id="1746f-108">**AzSynapseFirewallRule** Cmdlet은 Azure Synapse Analytics 방화벽 규칙을 modifys 합니다.</span><span class="sxs-lookup"><span data-stu-id="1746f-108">The **Update-AzSynapseFirewallRule** cmdlet modifys an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="1746f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="1746f-109">EXAMPLES</span></span>

### <span data-ttu-id="1746f-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="1746f-110">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAssdress "255.255.255.255"
```

<span data-ttu-id="1746f-111">이 명령은 이름 ContosoFirewallRule를 사용 하 여 작업 영역 ContosoWorkspace에서 ContosoFirewallRule 이라는 방화벽 규칙을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1746f-111">This command updates firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="1746f-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="1746f-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseFirewallRule -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAssdress "255.255.255.255"
```

<span data-ttu-id="1746f-113">이 명령은 파이프라인을 통해 작업 영역 아래에 ContosoFirewallRule 이라는 방화벽 규칙을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1746f-113">This command updates firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

## <span data-ttu-id="1746f-114">변수</span><span class="sxs-lookup"><span data-stu-id="1746f-114">PARAMETERS</span></span>

### <span data-ttu-id="1746f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1746f-115">-AsJob</span></span>
<span data-ttu-id="1746f-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="1746f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1746f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1746f-117">-DefaultProfile</span></span>
<span data-ttu-id="1746f-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1746f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1746f-119">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="1746f-119">-EndIpAddress</span></span>
<span data-ttu-id="1746f-120">방화벽 규칙의 끝 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="1746f-120">The end IP address of the firewall rule.</span></span>
<span data-ttu-id="1746f-121">IPv4 형식 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1746f-121">Must be IPv4 format.</span></span>
<span data-ttu-id="1746f-122">StartIpAddress 보다 크거나 같아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1746f-122">Must be greater than or equal to startIpAddress.</span></span>

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

### <span data-ttu-id="1746f-123">-이름</span><span class="sxs-lookup"><span data-stu-id="1746f-123">-Name</span></span>
<span data-ttu-id="1746f-124">작업 영역에 대 한 firerwall 규칙 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1746f-124">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="1746f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1746f-125">-ResourceGroupName</span></span>
<span data-ttu-id="1746f-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1746f-126">Resource group name.</span></span>

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

### <span data-ttu-id="1746f-127">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="1746f-127">-StartIpAddress</span></span>
<span data-ttu-id="1746f-128">방화벽 규칙의 시작 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="1746f-128">The start IP address of the firewall rule.</span></span>
<span data-ttu-id="1746f-129">IPv4 형식 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1746f-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="1746f-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1746f-130">-WorkspaceName</span></span>
<span data-ttu-id="1746f-131">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1746f-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="1746f-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="1746f-132">-WorkspaceObject</span></span>
<span data-ttu-id="1746f-133">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="1746f-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="1746f-134">-확인</span><span class="sxs-lookup"><span data-stu-id="1746f-134">-Confirm</span></span>
<span data-ttu-id="1746f-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1746f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1746f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1746f-136">-WhatIf</span></span>
<span data-ttu-id="1746f-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1746f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1746f-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1746f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1746f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1746f-139">CommonParameters</span></span>
<span data-ttu-id="1746f-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1746f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1746f-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1746f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1746f-142">입력</span><span class="sxs-lookup"><span data-stu-id="1746f-142">INPUTS</span></span>

### <span data-ttu-id="1746f-143">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="1746f-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="1746f-144">출력</span><span class="sxs-lookup"><span data-stu-id="1746f-144">OUTPUTS</span></span>

### <span data-ttu-id="1746f-145">Synapse. PSSynapseIpFirewallRule/.</span><span class="sxs-lookup"><span data-stu-id="1746f-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="1746f-146">상속자</span><span class="sxs-lookup"><span data-stu-id="1746f-146">NOTES</span></span>

## <span data-ttu-id="1746f-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1746f-147">RELATED LINKS</span></span>
