---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/disable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddOn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddOn.md
ms.openlocfilehash: 5d0cc543d5ec893ecb1f83b8fd62f25bcb32f5b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966971"
---
# <span data-ttu-id="732f9-101">Disable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="732f9-101">Disable-AzAksAddOn</span></span>

## <span data-ttu-id="732f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="732f9-102">SYNOPSIS</span></span>
<span data-ttu-id="732f9-103">aks에 대한 추가 기능을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="732f9-103">Disable the addons for aks.</span></span>

## <span data-ttu-id="732f9-104">구문</span><span class="sxs-lookup"><span data-stu-id="732f9-104">SYNTAX</span></span>

### <span data-ttu-id="732f9-105">defaultParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="732f9-105">defaultParameterSet (Default)</span></span>
```
Disable-AzAksAddOn [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="732f9-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="732f9-106">InputObjectParameterSet</span></span>
```
Disable-AzAksAddOn -ClusterObject <PSKubernetesCluster> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="732f9-107">설명</span><span class="sxs-lookup"><span data-stu-id="732f9-107">DESCRIPTION</span></span>
<span data-ttu-id="732f9-108">aks에 대한 추가 기능을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="732f9-108">Disable the addons for aks.</span></span>

## <span data-ttu-id="732f9-109">예제</span><span class="sxs-lookup"><span data-stu-id="732f9-109">EXAMPLES</span></span>

### <span data-ttu-id="732f9-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="732f9-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Disable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard
```

<span data-ttu-id="732f9-111">aks에 대한 추가 기능 `HttpApplicationRouting` `Monitoring` , , 및 `AzurePolicy` `VirtualNode` `KubeDashboard` 를 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="732f9-111">Disable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="732f9-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="732f9-112">PARAMETERS</span></span>

### <span data-ttu-id="732f9-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="732f9-113">-ClusterName</span></span>
<span data-ttu-id="732f9-114">Kubernetes 관리되는 클러스터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="732f9-114">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="732f9-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="732f9-115">-ClusterObject</span></span>
<span data-ttu-id="732f9-116">일반적으로 파이프라인을 통해 전달되는 PSKubernetesCluster 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="732f9-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="732f9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="732f9-117">-DefaultProfile</span></span>
<span data-ttu-id="732f9-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="732f9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="732f9-119">-Name</span><span class="sxs-lookup"><span data-stu-id="732f9-119">-Name</span></span>
<span data-ttu-id="732f9-120">Kubernetes 관리되는 클러스터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="732f9-120">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="732f9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="732f9-121">-ResourceGroupName</span></span>
<span data-ttu-id="732f9-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="732f9-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="732f9-123">-확인</span><span class="sxs-lookup"><span data-stu-id="732f9-123">-Confirm</span></span>
<span data-ttu-id="732f9-124">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="732f9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="732f9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="732f9-125">-WhatIf</span></span>
<span data-ttu-id="732f9-126">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="732f9-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="732f9-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="732f9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="732f9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="732f9-128">CommonParameters</span></span>
<span data-ttu-id="732f9-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="732f9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="732f9-130">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="732f9-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="732f9-131">입력</span><span class="sxs-lookup"><span data-stu-id="732f9-131">INPUTS</span></span>

### <span data-ttu-id="732f9-132">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="732f9-132">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="732f9-133">System.String</span><span class="sxs-lookup"><span data-stu-id="732f9-133">System.String</span></span>

## <span data-ttu-id="732f9-134">출력</span><span class="sxs-lookup"><span data-stu-id="732f9-134">OUTPUTS</span></span>

### <span data-ttu-id="732f9-135">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="732f9-135">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="732f9-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="732f9-136">NOTES</span></span>

## <span data-ttu-id="732f9-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="732f9-137">RELATED LINKS</span></span>
