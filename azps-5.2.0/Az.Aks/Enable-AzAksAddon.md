---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/enable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddon.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddon.md
ms.openlocfilehash: de4453129ee626ac7eeeaa20fa14c1068011c001
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342489"
---
# <span data-ttu-id="1cec9-101">Enable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="1cec9-101">Enable-AzAksAddOn</span></span>

## <span data-ttu-id="1cec9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cec9-102">SYNOPSIS</span></span>
<span data-ttu-id="1cec9-103">aks에 대한 추가 기능을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1cec9-103">Enable the addons for aks.</span></span>

## <span data-ttu-id="1cec9-104">구문</span><span class="sxs-lookup"><span data-stu-id="1cec9-104">SYNTAX</span></span>

### <span data-ttu-id="1cec9-105">defaultParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="1cec9-105">defaultParameterSet (Default)</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] [-ResourceGroupName] <String>
 [-ClusterName] <String> [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1cec9-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cec9-106">InputObjectParameterSet</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] -ClusterObject <PSKubernetesCluster>
 [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cec9-107">설명</span><span class="sxs-lookup"><span data-stu-id="1cec9-107">DESCRIPTION</span></span>
<span data-ttu-id="1cec9-108">aks에 대한 추가 기능을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1cec9-108">Enable the addons for aks.</span></span>

## <span data-ttu-id="1cec9-109">예제</span><span class="sxs-lookup"><span data-stu-id="1cec9-109">EXAMPLES</span></span>

### <span data-ttu-id="1cec9-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="1cec9-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Enable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard -WorkspaceResourceId xxxxx/xxxx -SubnetName subnet
```

<span data-ttu-id="1cec9-111">추가 `HttpApplicationRouting` 기능, `Monitoring` 및 `AzurePolicy` `VirtualNode` `KubeDashboard` aks를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1cec9-111">Enable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="1cec9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1cec9-112">PARAMETERS</span></span>

### <span data-ttu-id="1cec9-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1cec9-113">-ClusterName</span></span>
<span data-ttu-id="1cec9-114">Kubernetes 관리되는 클러스터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1cec9-114">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cec9-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="1cec9-115">-ClusterObject</span></span>
<span data-ttu-id="1cec9-116">일반적으로 파이프라인을 통해 전달되는 PSKubernetesCluster 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="1cec9-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1cec9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cec9-117">-DefaultProfile</span></span>
<span data-ttu-id="1cec9-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1cec9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cec9-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1cec9-119">-Name</span></span>
<span data-ttu-id="1cec9-120">Kubernetes 관리되는 클러스터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1cec9-120">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cec9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cec9-121">-ResourceGroupName</span></span>
<span data-ttu-id="1cec9-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1cec9-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cec9-123">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="1cec9-123">-SubnetName</span></span>
<span data-ttu-id="1cec9-124">VirtualNode의 서브넷 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1cec9-124">Subnet name of VirtualNode.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cec9-125">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="1cec9-125">-WorkspaceResourceId</span></span>
<span data-ttu-id="1cec9-126">모니터링 작업 영역의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1cec9-126">Resource Id of the workspace of Monitoring.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cec9-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1cec9-127">-Confirm</span></span>
<span data-ttu-id="1cec9-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1cec9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cec9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cec9-129">-WhatIf</span></span>
<span data-ttu-id="1cec9-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1cec9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cec9-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1cec9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cec9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cec9-132">CommonParameters</span></span>
<span data-ttu-id="1cec9-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1cec9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cec9-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1cec9-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cec9-135">입력</span><span class="sxs-lookup"><span data-stu-id="1cec9-135">INPUTS</span></span>

### <span data-ttu-id="1cec9-136">System.String</span><span class="sxs-lookup"><span data-stu-id="1cec9-136">System.String</span></span>

### <span data-ttu-id="1cec9-137">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="1cec9-137">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="1cec9-138">출력</span><span class="sxs-lookup"><span data-stu-id="1cec9-138">OUTPUTS</span></span>

### <span data-ttu-id="1cec9-139">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="1cec9-139">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="1cec9-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1cec9-140">NOTES</span></span>

## <span data-ttu-id="1cec9-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1cec9-141">RELATED LINKS</span></span>
