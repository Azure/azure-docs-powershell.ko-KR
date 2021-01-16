---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/new-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/New-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/New-AzConnectedKubernetes.md
ms.openlocfilehash: 5ee758c305a960f6a06fb72290996bbec8037ed7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337089"
---
# <span data-ttu-id="f9b35-101">New-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="f9b35-101">New-AzConnectedKubernetes</span></span>

## <span data-ttu-id="f9b35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9b35-102">SYNOPSIS</span></span>
<span data-ttu-id="f9b35-103">새 K8s 클러스터를 등록하여 클러스터에서 추적된 리소스를 만드는 API ARM</span><span class="sxs-lookup"><span data-stu-id="f9b35-103">API to register a new K8s cluster and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="f9b35-104">구문</span><span class="sxs-lookup"><span data-stu-id="f9b35-104">SYNTAX</span></span>

```
New-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> -Location <String>
 [-SubscriptionId <String>] [-KubeConfig <String>] [-KubeContext <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f9b35-105">설명</span><span class="sxs-lookup"><span data-stu-id="f9b35-105">DESCRIPTION</span></span>
<span data-ttu-id="f9b35-106">새 K8s 클러스터를 등록하여 클러스터에서 추적된 리소스를 만드는 API ARM</span><span class="sxs-lookup"><span data-stu-id="f9b35-106">API to register a new K8s cluster and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="f9b35-107">예제</span><span class="sxs-lookup"><span data-stu-id="f9b35-107">EXAMPLES</span></span>

### <span data-ttu-id="f9b35-108">예제 1: 연결된 kubernetes 만들기</span><span class="sxs-lookup"><span data-stu-id="f9b35-108">Example 1: Create a connected kubernetes</span></span>
```powershell
PS C:\> New-AzConnectedKubernetes -ClusterName ps-connaks-t01 -ResourceGroupName connected-aks -Location 
Location Name         Type
-------- ----         ----
eastus   ps-connaks-t01 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="f9b35-109">이 명령은 연결된 kubernetes를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f9b35-109">This command creates a connected kubernetes.</span></span>

### <span data-ttu-id="f9b35-110">예제 1: kubeConfig 및 kubeContext 매개 변수를 사용하여 연결된 kubernetes 만들기</span><span class="sxs-lookup"><span data-stu-id="f9b35-110">Example 1: Create a connected kubernetes with parameters kubeConfig and kubeContext</span></span>
```powershell
PS C:\> New-AzConnectedKubernetes -ClusterName ps-connaks-t02 -ResourceGroupName connected-aks -Location eastus -KubeConfig $HOME\.kube\config -KubeContext portal-aks-t01

Location Name         Type
-------- ----         ----
eastus   ps-connaks-t02 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="f9b35-111">이 명령은 kubeConfig 및 kubeContext 매개 변수를 사용하여 연결된 kubernetes를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f9b35-111">This command creates a connected kubernetes with parameters kubeConfig and kubeContext.</span></span>

## <span data-ttu-id="f9b35-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9b35-112">PARAMETERS</span></span>

### <span data-ttu-id="f9b35-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f9b35-113">-ClusterName</span></span>
<span data-ttu-id="f9b35-114">get이 호출되는 Kubernetes 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9b35-114">The name of the Kubernetes cluster on which get is called.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9b35-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9b35-115">-DefaultProfile</span></span>
<span data-ttu-id="f9b35-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f9b35-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9b35-117">-KubeConfig</span><span class="sxs-lookup"><span data-stu-id="f9b35-117">-KubeConfig</span></span>
<span data-ttu-id="f9b35-118">kube 구성 파일의 경로</span><span class="sxs-lookup"><span data-stu-id="f9b35-118">Path to the kube config file</span></span>

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

### <span data-ttu-id="f9b35-119">-KubeContext</span><span class="sxs-lookup"><span data-stu-id="f9b35-119">-KubeContext</span></span>
<span data-ttu-id="f9b35-120">현재 컴퓨터의 Kubconfig 컨텍스트</span><span class="sxs-lookup"><span data-stu-id="f9b35-120">Kubconfig context from current machine</span></span>

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

### <span data-ttu-id="f9b35-121">-Location</span><span class="sxs-lookup"><span data-stu-id="f9b35-121">-Location</span></span>
<span data-ttu-id="f9b35-122">클러스터의 위치</span><span class="sxs-lookup"><span data-stu-id="f9b35-122">Location of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9b35-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9b35-123">-ResourceGroupName</span></span>
<span data-ttu-id="f9b35-124">kubernetes 클러스터가 등록된 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9b35-124">The name of the resource group to which the kubernetes cluster is registered.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9b35-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f9b35-125">-SubscriptionId</span></span>
<span data-ttu-id="f9b35-126">kubernetes 클러스터가 등록된 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f9b35-126">The ID of the subscription to which the kubernetes cluster is registered.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9b35-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f9b35-127">-Confirm</span></span>
<span data-ttu-id="f9b35-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9b35-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9b35-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9b35-129">-WhatIf</span></span>
<span data-ttu-id="f9b35-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f9b35-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9b35-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f9b35-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9b35-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9b35-132">CommonParameters</span></span>
<span data-ttu-id="f9b35-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f9b35-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9b35-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f9b35-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9b35-135">입력</span><span class="sxs-lookup"><span data-stu-id="f9b35-135">INPUTS</span></span>

## <span data-ttu-id="f9b35-136">출력</span><span class="sxs-lookup"><span data-stu-id="f9b35-136">OUTPUTS</span></span>

### <span data-ttu-id="f9b35-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="f9b35-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span></span>

## <span data-ttu-id="f9b35-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f9b35-138">NOTES</span></span>

<span data-ttu-id="f9b35-139">별칭</span><span class="sxs-lookup"><span data-stu-id="f9b35-139">ALIASES</span></span>

## <span data-ttu-id="f9b35-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f9b35-140">RELATED LINKS</span></span>
