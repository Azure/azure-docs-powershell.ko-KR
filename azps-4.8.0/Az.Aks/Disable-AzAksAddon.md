---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/disable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddon.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddon.md
ms.openlocfilehash: 0fca409546822ef596897adbbf755a1a4ae43e38
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048031"
---
# <span data-ttu-id="25f7c-101">Disable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="25f7c-101">Disable-AzAksAddOn</span></span>

## <span data-ttu-id="25f7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25f7c-102">SYNOPSIS</span></span>
<span data-ttu-id="25f7c-103">Aks에 대해 addons를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25f7c-103">Disable the addons for aks.</span></span>

## <span data-ttu-id="25f7c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="25f7c-104">SYNTAX</span></span>

### <span data-ttu-id="25f7c-105">defaultParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="25f7c-105">defaultParameterSet (Default)</span></span>
```
Disable-AzAksAddOn [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25f7c-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="25f7c-106">InputObjectParameterSet</span></span>
```
Disable-AzAksAddOn -ClusterObject <PSKubernetesCluster> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25f7c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="25f7c-107">DESCRIPTION</span></span>
<span data-ttu-id="25f7c-108">Aks에 대해 addons를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25f7c-108">Disable the addons for aks.</span></span>

## <span data-ttu-id="25f7c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="25f7c-109">EXAMPLES</span></span>

### <span data-ttu-id="25f7c-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="25f7c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Disable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard
```

<span data-ttu-id="25f7c-111">Addons,,, aks을 사용 하지 않도록 설정 `HttpApplicationRouting` `Monitoring` `AzurePolicy` `VirtualNode` `KubeDashboard` 합니다.</span><span class="sxs-lookup"><span data-stu-id="25f7c-111">Disable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="25f7c-112">변수</span><span class="sxs-lookup"><span data-stu-id="25f7c-112">PARAMETERS</span></span>

### <span data-ttu-id="25f7c-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="25f7c-113">-ClusterName</span></span>
<span data-ttu-id="25f7c-114">Kubernetes 관리 되는 클러스터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="25f7c-114">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="25f7c-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="25f7c-115">-ClusterObject</span></span>
<span data-ttu-id="25f7c-116">일반적으로 파이프라인을 통해 전달 되는 P고 U칭찬 Netescluster 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="25f7c-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="25f7c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25f7c-117">-DefaultProfile</span></span>
<span data-ttu-id="25f7c-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="25f7c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25f7c-119">-이름</span><span class="sxs-lookup"><span data-stu-id="25f7c-119">-Name</span></span>
<span data-ttu-id="25f7c-120">Kubernetes 관리 되는 클러스터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="25f7c-120">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="25f7c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25f7c-121">-ResourceGroupName</span></span>
<span data-ttu-id="25f7c-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="25f7c-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="25f7c-123">-확인</span><span class="sxs-lookup"><span data-stu-id="25f7c-123">-Confirm</span></span>
<span data-ttu-id="25f7c-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="25f7c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25f7c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25f7c-125">-WhatIf</span></span>
<span data-ttu-id="25f7c-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="25f7c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25f7c-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="25f7c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25f7c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25f7c-128">CommonParameters</span></span>
<span data-ttu-id="25f7c-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="25f7c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25f7c-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="25f7c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25f7c-131">입력</span><span class="sxs-lookup"><span data-stu-id="25f7c-131">INPUTS</span></span>

### <span data-ttu-id="25f7c-132">Aks. p U Netescluster</span><span class="sxs-lookup"><span data-stu-id="25f7c-132">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="25f7c-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="25f7c-133">System.String</span></span>

## <span data-ttu-id="25f7c-134">출력</span><span class="sxs-lookup"><span data-stu-id="25f7c-134">OUTPUTS</span></span>

### <span data-ttu-id="25f7c-135">Aks. p U Netescluster</span><span class="sxs-lookup"><span data-stu-id="25f7c-135">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="25f7c-136">상속자</span><span class="sxs-lookup"><span data-stu-id="25f7c-136">NOTES</span></span>

## <span data-ttu-id="25f7c-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="25f7c-137">RELATED LINKS</span></span>
