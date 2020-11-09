---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseFirewallRule.md
ms.openlocfilehash: b4579d01ed6dd5a7d742cbb82afb424151579772
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309810"
---
# <span data-ttu-id="17471-101">New-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="17471-101">New-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="17471-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17471-102">SYNOPSIS</span></span>
<span data-ttu-id="17471-103">Synapse Analytics 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="17471-103">Creates a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="17471-104">구문과</span><span class="sxs-lookup"><span data-stu-id="17471-104">SYNTAX</span></span>

### <span data-ttu-id="17471-105">CreateByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="17471-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -StartIpAddress <String> -EndIpAddress <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17471-106">CreateByNameAllowAllIpParameterSet</span><span class="sxs-lookup"><span data-stu-id="17471-106">CreateByNameAllowAllIpParameterSet</span></span>
```
New-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> [-AllowAllAzureIP] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17471-107">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="17471-107">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> -Name <String> -StartIpAddress <String>
 -EndIpAddress <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="17471-108">CreateByParentObjectAllowAllIpParameterSet</span><span class="sxs-lookup"><span data-stu-id="17471-108">CreateByParentObjectAllowAllIpParameterSet</span></span>
```
New-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> [-AllowAllAzureIP] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17471-109">설명은</span><span class="sxs-lookup"><span data-stu-id="17471-109">DESCRIPTION</span></span>
<span data-ttu-id="17471-110">**AzSynapseFirewallRule** Cmdlet은 Azure Synapse Analytics 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="17471-110">The **New-AzSynapseFirewallRule** cmdlet creates an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="17471-111">예제의</span><span class="sxs-lookup"><span data-stu-id="17471-111">EXAMPLES</span></span>

### <span data-ttu-id="17471-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="17471-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseFirewallRule -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAddress "255.255.255.255"
```

<span data-ttu-id="17471-113">이 명령은 이름 ContosoFirewallRule를 사용 하 여 작업 영역 ContosoWorkspace에 ContosoFirewallRule 이라는 이름의 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="17471-113">This command creates firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="17471-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="17471-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseFirewallRule -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAddress "255.255.255.255"
```

<span data-ttu-id="17471-115">이 명령은 파이프라인을 통해 작업 영역 아래에 ContosoFirewallRule 이라는 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="17471-115">This command creates firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

### <span data-ttu-id="17471-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="17471-116">Example 3</span></span>
```powershell
PS C:\> New-AzSynapseFirewallRule -WorkspaceName ContosoWorkspace -AllowAllAzureIP
```

<span data-ttu-id="17471-117">이 명령은 작업 영역에서 모든 azure ip를 허용 하는 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="17471-117">This command creates firewall rule that allow all azure ips under a workspace.</span></span>

## <span data-ttu-id="17471-118">변수</span><span class="sxs-lookup"><span data-stu-id="17471-118">PARAMETERS</span></span>

### <span data-ttu-id="17471-119">-AllowAllAzureIP</span><span class="sxs-lookup"><span data-stu-id="17471-119">-AllowAllAzureIP</span></span>
<span data-ttu-id="17471-120">모든 Azure Ip에 액세스할 수 있도록 허용 하는 특별 한 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="17471-120">Creates a special firewall rule that permits all Azure IPs to have access.</span></span>

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

### <span data-ttu-id="17471-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="17471-121">-AsJob</span></span>
<span data-ttu-id="17471-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="17471-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="17471-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17471-123">-DefaultProfile</span></span>
<span data-ttu-id="17471-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="17471-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17471-125">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="17471-125">-EndIpAddress</span></span>
<span data-ttu-id="17471-126">방화벽 규칙의 끝 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="17471-126">The end IP address of the firewall rule.</span></span>
<span data-ttu-id="17471-127">IPv4 형식 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="17471-127">Must be IPv4 format.</span></span>
<span data-ttu-id="17471-128">StartIpAddress 보다 크거나 같아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="17471-128">Must be greater than or equal to startIpAddress.</span></span>

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

### <span data-ttu-id="17471-129">-이름</span><span class="sxs-lookup"><span data-stu-id="17471-129">-Name</span></span>
<span data-ttu-id="17471-130">작업 영역에 대 한 firerwall 규칙 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="17471-130">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="17471-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17471-131">-ResourceGroupName</span></span>
<span data-ttu-id="17471-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="17471-132">Resource group name.</span></span>

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

### <span data-ttu-id="17471-133">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="17471-133">-StartIpAddress</span></span>
<span data-ttu-id="17471-134">방화벽 규칙의 시작 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="17471-134">The start IP address of the firewall rule.</span></span>
<span data-ttu-id="17471-135">IPv4 형식 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="17471-135">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="17471-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="17471-136">-WorkspaceName</span></span>
<span data-ttu-id="17471-137">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="17471-137">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="17471-138">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="17471-138">-WorkspaceObject</span></span>
<span data-ttu-id="17471-139">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="17471-139">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="17471-140">-확인</span><span class="sxs-lookup"><span data-stu-id="17471-140">-Confirm</span></span>
<span data-ttu-id="17471-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="17471-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17471-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17471-142">-WhatIf</span></span>
<span data-ttu-id="17471-143">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="17471-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17471-144">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="17471-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17471-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17471-145">CommonParameters</span></span>
<span data-ttu-id="17471-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="17471-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17471-147">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="17471-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17471-148">입력</span><span class="sxs-lookup"><span data-stu-id="17471-148">INPUTS</span></span>

### <span data-ttu-id="17471-149">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="17471-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="17471-150">출력</span><span class="sxs-lookup"><span data-stu-id="17471-150">OUTPUTS</span></span>

### <span data-ttu-id="17471-151">Synapse. PSSynapseIpFirewallRule/.</span><span class="sxs-lookup"><span data-stu-id="17471-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="17471-152">상속자</span><span class="sxs-lookup"><span data-stu-id="17471-152">NOTES</span></span>

## <span data-ttu-id="17471-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="17471-153">RELATED LINKS</span></span>
