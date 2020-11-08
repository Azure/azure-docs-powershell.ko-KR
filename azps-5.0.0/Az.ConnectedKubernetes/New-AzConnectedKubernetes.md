---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/new-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/New-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/New-AzConnectedKubernetes.md
ms.openlocfilehash: 5ee758c305a960f6a06fb72290996bbec8037ed7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216752"
---
# <span data-ttu-id="c0465-101">New-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="c0465-101">New-AzConnectedKubernetes</span></span>

## <span data-ttu-id="c0465-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0465-102">SYNOPSIS</span></span>
<span data-ttu-id="c0465-103">새 K8s 클러스터를 등록 하 여 ARM에서 추적 된 리소스를 만드는 API</span><span class="sxs-lookup"><span data-stu-id="c0465-103">API to register a new K8s cluster and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="c0465-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c0465-104">SYNTAX</span></span>

```
New-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> -Location <String>
 [-SubscriptionId <String>] [-KubeConfig <String>] [-KubeContext <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c0465-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c0465-105">DESCRIPTION</span></span>
<span data-ttu-id="c0465-106">새 K8s 클러스터를 등록 하 여 ARM에서 추적 된 리소스를 만드는 API</span><span class="sxs-lookup"><span data-stu-id="c0465-106">API to register a new K8s cluster and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="c0465-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c0465-107">EXAMPLES</span></span>

### <span data-ttu-id="c0465-108">예제 1: 연결 된 kubernetes 만들기</span><span class="sxs-lookup"><span data-stu-id="c0465-108">Example 1: Create a connected kubernetes</span></span>
```powershell
PS C:\> New-AzConnectedKubernetes -ClusterName ps-connaks-t01 -ResourceGroupName connected-aks -Location 
Location Name         Type
-------- ----         ----
eastus   ps-connaks-t01 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="c0465-109">이 명령은 연결 된 kubernetes를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c0465-109">This command creates a connected kubernetes.</span></span>

### <span data-ttu-id="c0465-110">예제 1: 매개 변수 kubeConfig 및 kubeContext를 사용 하 여 연결 된 kubernetes 만들기</span><span class="sxs-lookup"><span data-stu-id="c0465-110">Example 1: Create a connected kubernetes with parameters kubeConfig and kubeContext</span></span>
```powershell
PS C:\> New-AzConnectedKubernetes -ClusterName ps-connaks-t02 -ResourceGroupName connected-aks -Location eastus -KubeConfig $HOME\.kube\config -KubeContext portal-aks-t01

Location Name         Type
-------- ----         ----
eastus   ps-connaks-t02 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="c0465-111">이 명령은 kubeConfig 및 kubeContext 매개 변수를 사용 하 여 연결 된 kubernetes를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c0465-111">This command creates a connected kubernetes with parameters kubeConfig and kubeContext.</span></span>

## <span data-ttu-id="c0465-112">변수</span><span class="sxs-lookup"><span data-stu-id="c0465-112">PARAMETERS</span></span>

### <span data-ttu-id="c0465-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c0465-113">-ClusterName</span></span>
<span data-ttu-id="c0465-114">Get이 호출 되는 Kubernetes 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c0465-114">The name of the Kubernetes cluster on which get is called.</span></span>

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

### <span data-ttu-id="c0465-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0465-115">-DefaultProfile</span></span>
<span data-ttu-id="c0465-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c0465-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0465-117">-KubeConfig</span><span class="sxs-lookup"><span data-stu-id="c0465-117">-KubeConfig</span></span>
<span data-ttu-id="c0465-118">Kube config 파일 경로</span><span class="sxs-lookup"><span data-stu-id="c0465-118">Path to the kube config file</span></span>

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

### <span data-ttu-id="c0465-119">-KubeContext</span><span class="sxs-lookup"><span data-stu-id="c0465-119">-KubeContext</span></span>
<span data-ttu-id="c0465-120">현재 컴퓨터의 kubconfig 컨텍스트</span><span class="sxs-lookup"><span data-stu-id="c0465-120">Kubconfig context from current machine</span></span>

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

### <span data-ttu-id="c0465-121">-위치</span><span class="sxs-lookup"><span data-stu-id="c0465-121">-Location</span></span>
<span data-ttu-id="c0465-122">클러스터 위치</span><span class="sxs-lookup"><span data-stu-id="c0465-122">Location of the cluster</span></span>

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

### <span data-ttu-id="c0465-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0465-123">-ResourceGroupName</span></span>
<span data-ttu-id="c0465-124">Kubernetes 클러스터가 등록 된 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c0465-124">The name of the resource group to which the kubernetes cluster is registered.</span></span>

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

### <span data-ttu-id="c0465-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c0465-125">-SubscriptionId</span></span>
<span data-ttu-id="c0465-126">Kubernetes 클러스터가 등록 된 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c0465-126">The ID of the subscription to which the kubernetes cluster is registered.</span></span>

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

### <span data-ttu-id="c0465-127">-확인</span><span class="sxs-lookup"><span data-stu-id="c0465-127">-Confirm</span></span>
<span data-ttu-id="c0465-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0465-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0465-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0465-129">-WhatIf</span></span>
<span data-ttu-id="c0465-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c0465-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0465-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c0465-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0465-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0465-132">CommonParameters</span></span>
<span data-ttu-id="c0465-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0465-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0465-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c0465-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0465-135">입력</span><span class="sxs-lookup"><span data-stu-id="c0465-135">INPUTS</span></span>

## <span data-ttu-id="c0465-136">출력</span><span class="sxs-lookup"><span data-stu-id="c0465-136">OUTPUTS</span></span>

### <span data-ttu-id="c0465-137">ConnectedKubernetes. Api202001Preview. IConnectedCluster에 대 한</span><span class="sxs-lookup"><span data-stu-id="c0465-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span></span>

## <span data-ttu-id="c0465-138">상속자</span><span class="sxs-lookup"><span data-stu-id="c0465-138">NOTES</span></span>

<span data-ttu-id="c0465-139">별칭과</span><span class="sxs-lookup"><span data-stu-id="c0465-139">ALIASES</span></span>

## <span data-ttu-id="c0465-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c0465-140">RELATED LINKS</span></span>

