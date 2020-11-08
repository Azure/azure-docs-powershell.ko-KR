---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/enable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddon.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddon.md
ms.openlocfilehash: de4453129ee626ac7eeeaa20fa14c1068011c001
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217898"
---
# <span data-ttu-id="60518-101">Enable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="60518-101">Enable-AzAksAddOn</span></span>

## <span data-ttu-id="60518-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60518-102">SYNOPSIS</span></span>
<span data-ttu-id="60518-103">Aks에 addons을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60518-103">Enable the addons for aks.</span></span>

## <span data-ttu-id="60518-104">구문과</span><span class="sxs-lookup"><span data-stu-id="60518-104">SYNTAX</span></span>

### <span data-ttu-id="60518-105">defaultParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="60518-105">defaultParameterSet (Default)</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] [-ResourceGroupName] <String>
 [-ClusterName] <String> [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="60518-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="60518-106">InputObjectParameterSet</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] -ClusterObject <PSKubernetesCluster>
 [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60518-107">설명은</span><span class="sxs-lookup"><span data-stu-id="60518-107">DESCRIPTION</span></span>
<span data-ttu-id="60518-108">Aks에 addons을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60518-108">Enable the addons for aks.</span></span>

## <span data-ttu-id="60518-109">예제의</span><span class="sxs-lookup"><span data-stu-id="60518-109">EXAMPLES</span></span>

### <span data-ttu-id="60518-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="60518-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Enable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard -WorkspaceResourceId xxxxx/xxxx -SubnetName subnet
```

<span data-ttu-id="60518-111">Addons,,, 및 aks를 사용 하도록 설정 `HttpApplicationRouting` `Monitoring` `AzurePolicy` `VirtualNode` `KubeDashboard` 합니다.</span><span class="sxs-lookup"><span data-stu-id="60518-111">Enable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="60518-112">변수</span><span class="sxs-lookup"><span data-stu-id="60518-112">PARAMETERS</span></span>

### <span data-ttu-id="60518-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="60518-113">-ClusterName</span></span>
<span data-ttu-id="60518-114">Kubernetes 관리 되는 클러스터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="60518-114">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="60518-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="60518-115">-ClusterObject</span></span>
<span data-ttu-id="60518-116">일반적으로 파이프라인을 통해 전달 되는 P고 U칭찬 Netescluster 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="60518-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="60518-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60518-117">-DefaultProfile</span></span>
<span data-ttu-id="60518-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="60518-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60518-119">-이름</span><span class="sxs-lookup"><span data-stu-id="60518-119">-Name</span></span>
<span data-ttu-id="60518-120">Kubernetes 관리 되는 클러스터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="60518-120">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="60518-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60518-121">-ResourceGroupName</span></span>
<span data-ttu-id="60518-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="60518-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="60518-123">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="60518-123">-SubnetName</span></span>
<span data-ttu-id="60518-124">VirtualNode의 서브넷 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="60518-124">Subnet name of VirtualNode.</span></span>

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

### <span data-ttu-id="60518-125">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="60518-125">-WorkspaceResourceId</span></span>
<span data-ttu-id="60518-126">모니터링 작업 영역의 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="60518-126">Resource Id of the workspace of Monitoring.</span></span>

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

### <span data-ttu-id="60518-127">-확인</span><span class="sxs-lookup"><span data-stu-id="60518-127">-Confirm</span></span>
<span data-ttu-id="60518-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="60518-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60518-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60518-129">-WhatIf</span></span>
<span data-ttu-id="60518-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="60518-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60518-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="60518-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60518-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60518-132">CommonParameters</span></span>
<span data-ttu-id="60518-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="60518-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60518-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="60518-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60518-135">입력</span><span class="sxs-lookup"><span data-stu-id="60518-135">INPUTS</span></span>

### <span data-ttu-id="60518-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="60518-136">System.String</span></span>

### <span data-ttu-id="60518-137">Aks. p U Netescluster</span><span class="sxs-lookup"><span data-stu-id="60518-137">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="60518-138">출력</span><span class="sxs-lookup"><span data-stu-id="60518-138">OUTPUTS</span></span>

### <span data-ttu-id="60518-139">Aks. p U<c13> Netescluster</span><span class="sxs-lookup"><span data-stu-id="60518-139">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="60518-140">상속자</span><span class="sxs-lookup"><span data-stu-id="60518-140">NOTES</span></span>

## <span data-ttu-id="60518-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="60518-141">RELATED LINKS</span></span>
