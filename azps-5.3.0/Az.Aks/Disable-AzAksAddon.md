---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/disable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddon.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddon.md
ms.openlocfilehash: 0fca409546822ef596897adbbf755a1a4ae43e38
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494540"
---
# <span data-ttu-id="521ea-101">Disable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="521ea-101">Disable-AzAksAddOn</span></span>

## <span data-ttu-id="521ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="521ea-102">SYNOPSIS</span></span>
<span data-ttu-id="521ea-103">aks에 대한 추가 기능을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="521ea-103">Disable the addons for aks.</span></span>

## <span data-ttu-id="521ea-104">구문</span><span class="sxs-lookup"><span data-stu-id="521ea-104">SYNTAX</span></span>

### <span data-ttu-id="521ea-105">defaultParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="521ea-105">defaultParameterSet (Default)</span></span>
```
Disable-AzAksAddOn [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="521ea-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="521ea-106">InputObjectParameterSet</span></span>
```
Disable-AzAksAddOn -ClusterObject <PSKubernetesCluster> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="521ea-107">설명</span><span class="sxs-lookup"><span data-stu-id="521ea-107">DESCRIPTION</span></span>
<span data-ttu-id="521ea-108">aks에 대한 추가 기능을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="521ea-108">Disable the addons for aks.</span></span>

## <span data-ttu-id="521ea-109">예제</span><span class="sxs-lookup"><span data-stu-id="521ea-109">EXAMPLES</span></span>

### <span data-ttu-id="521ea-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="521ea-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Disable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard
```

<span data-ttu-id="521ea-111">추가 `HttpApplicationRouting` 기능, `Monitoring` , `AzurePolicy` `VirtualNode` `KubeDashboard` aks를 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="521ea-111">Disable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="521ea-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="521ea-112">PARAMETERS</span></span>

### <span data-ttu-id="521ea-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="521ea-113">-ClusterName</span></span>
<span data-ttu-id="521ea-114">Kubernetes 관리되는 클러스터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="521ea-114">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="521ea-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="521ea-115">-ClusterObject</span></span>
<span data-ttu-id="521ea-116">일반적으로 파이프라인을 통해 전달되는 PSKubernetesCluster 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="521ea-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="521ea-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="521ea-117">-DefaultProfile</span></span>
<span data-ttu-id="521ea-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="521ea-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="521ea-119">-Name</span><span class="sxs-lookup"><span data-stu-id="521ea-119">-Name</span></span>
<span data-ttu-id="521ea-120">Kubernetes 관리되는 클러스터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="521ea-120">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="521ea-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="521ea-121">-ResourceGroupName</span></span>
<span data-ttu-id="521ea-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="521ea-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="521ea-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="521ea-123">-Confirm</span></span>
<span data-ttu-id="521ea-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="521ea-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="521ea-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="521ea-125">-WhatIf</span></span>
<span data-ttu-id="521ea-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="521ea-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="521ea-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="521ea-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="521ea-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="521ea-128">CommonParameters</span></span>
<span data-ttu-id="521ea-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="521ea-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="521ea-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="521ea-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="521ea-131">입력</span><span class="sxs-lookup"><span data-stu-id="521ea-131">INPUTS</span></span>

### <span data-ttu-id="521ea-132">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="521ea-132">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="521ea-133">System.String</span><span class="sxs-lookup"><span data-stu-id="521ea-133">System.String</span></span>

## <span data-ttu-id="521ea-134">출력</span><span class="sxs-lookup"><span data-stu-id="521ea-134">OUTPUTS</span></span>

### <span data-ttu-id="521ea-135">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="521ea-135">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="521ea-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="521ea-136">NOTES</span></span>

## <span data-ttu-id="521ea-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="521ea-137">RELATED LINKS</span></span>
