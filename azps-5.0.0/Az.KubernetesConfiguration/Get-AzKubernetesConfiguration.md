---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/get-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
ms.openlocfilehash: 3fd93e42b8f38659f61fcbeb0f49040409f635a8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94219036"
---
# <span data-ttu-id="b4a2c-101">Get-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4a2c-101">Get-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="b4a2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4a2c-102">SYNOPSIS</span></span>
<span data-ttu-id="b4a2c-103">소스 제어 구성에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b4a2c-103">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="b4a2c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b4a2c-104">SYNTAX</span></span>

### <span data-ttu-id="b4a2c-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="b4a2c-105">List (Default)</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b4a2c-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="b4a2c-106">Get</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b4a2c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b4a2c-107">GetViaIdentity</span></span>
```
Get-AzKubernetesConfiguration -InputObject <IKubernetesConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b4a2c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b4a2c-108">DESCRIPTION</span></span>
<span data-ttu-id="b4a2c-109">소스 제어 구성에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b4a2c-109">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="b4a2c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b4a2c-110">EXAMPLES</span></span>

### <span data-ttu-id="b4a2c-111">예제 1: kubernetes 클러스터의 모든 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="b4a2c-111">Example 1: Get all configurations of kubernetes cluster</span></span>
```powershell
PS C:\> Get-AzKubernetesConfiguration -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t02 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters

Name        Type
----        ----
conf-test01 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="b4a2c-112">이 명령은 kubernetes cluster의 모든 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b4a2c-112">This command gets all configurations of kubernetes cluster.</span></span>

### <span data-ttu-id="b4a2c-113">예제 2: 이름으로 kubernetes 클러스터의 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="b4a2c-113">Example 2: Get a configuration of kubernetes cluster by name</span></span>
```powershell
PS C:\> Get-AzKubernetesConfiguration -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t02 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters -Name conf-t02

Name     Type
----     ----
conf-t02 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="b4a2c-114">이 명령은 이름으로 kubernetes 클러스터의 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b4a2c-114">This command gets a configuration of kubernetes cluster by name.</span></span>

### <span data-ttu-id="b4a2c-115">예제 3: kubernetes 클러스터의 구성 가져오기 개체</span><span class="sxs-lookup"><span data-stu-id="b4a2c-115">Example 3: Get a configuration of kubernetes cluster by object</span></span>
```powershell
PS C:\> $kubConf = New-AzKubernetesConfiguration -Name conf-test02 -ClusterName connaks-dkc29c -ResourceGroupName connaks-rg-w9vlnp -RepositoryUrl http://github.com/xxxx
PS C:\> Get-AzKubernetesConfiguration -InputObject $kubConf

Name     Type
----     ----
conf-t02 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="b4a2c-116">이 명령은 kubernetes 클러스터의 구성을 개체 별로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b4a2c-116">This command gets a configuration of kubernetes cluster by object.</span></span>

### <span data-ttu-id="b4a2c-117">예제 4: 파이프라인을 기준으로 kubernetes 클러스터의 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="b4a2c-117">Example 4: Get a configuration of kubernetes cluster by pipeline</span></span>
```powershell
PS C:\> @{Id='/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/connaks-rg-w9vlnp/providers/Microsoft.Kubernetes/connectedClusters/connaks-d983yc/providers/Microsoft.KubernetesConfiguration/sourceControlConfigurations/conf-test01'} | Get-AzKubernetesConfiguration

Name        Type
----        ----
conf-test01 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="b4a2c-118">이 명령은 kubernetes 클러스터의 구성을 파이프라인 별로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b4a2c-118">This command gets a configuration of kubernetes cluster by pipeline.</span></span>

## <span data-ttu-id="b4a2c-119">변수</span><span class="sxs-lookup"><span data-stu-id="b4a2c-119">PARAMETERS</span></span>

### <span data-ttu-id="b4a2c-120">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b4a2c-120">-ClusterName</span></span>
<span data-ttu-id="b4a2c-121">Kubernetes 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b4a2c-121">The name of the kubernetes cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a2c-122">-ClusterRp</span><span class="sxs-lookup"><span data-stu-id="b4a2c-122">-ClusterRp</span></span>
<span data-ttu-id="b4a2c-123">Kubernetes 클러스터 RP-ContainerService (AKS 클러스터의 경우) 또는 Kubernetes (OnPrem K8S 클러스터의 경우).</span><span class="sxs-lookup"><span data-stu-id="b4a2c-123">The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a2c-124">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="b4a2c-124">-ClusterType</span></span>
<span data-ttu-id="b4a2c-125">Kubernetes 클러스터 리소스 이름 (AKS 클러스터의 경우) 또는 connectedClusters (OnPrem K8S 클러스터의 경우).</span><span class="sxs-lookup"><span data-stu-id="b4a2c-125">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a2c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4a2c-126">-DefaultProfile</span></span>
<span data-ttu-id="b4a2c-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b4a2c-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4a2c-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4a2c-128">-InputObject</span></span>
<span data-ttu-id="b4a2c-129">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b4a2c-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4a2c-130">-이름</span><span class="sxs-lookup"><span data-stu-id="b4a2c-130">-Name</span></span>
<span data-ttu-id="b4a2c-131">소스 제어 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b4a2c-131">Name of the Source Control Configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SourceControlConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a2c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4a2c-132">-ResourceGroupName</span></span>
<span data-ttu-id="b4a2c-133">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b4a2c-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a2c-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b4a2c-134">-SubscriptionId</span></span>
<span data-ttu-id="b4a2c-135">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b4a2c-135">The Azure subscription ID.</span></span>
<span data-ttu-id="b4a2c-136">GUID 형식 문자열입니다 (예: 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="b4a2c-136">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a2c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4a2c-137">CommonParameters</span></span>
<span data-ttu-id="b4a2c-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4a2c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4a2c-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b4a2c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4a2c-140">입력</span><span class="sxs-lookup"><span data-stu-id="b4a2c-140">INPUTS</span></span>

### <span data-ttu-id="b4a2c-141">KubernetesConfiguration. IKubernetesConfigurationIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="b4a2c-141">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span></span>

## <span data-ttu-id="b4a2c-142">출력</span><span class="sxs-lookup"><span data-stu-id="b4a2c-142">OUTPUTS</span></span>

### <span data-ttu-id="b4a2c-143">KubernetesConfiguration. Api20191101Preview. ISourceControlConfiguration에 대 한</span><span class="sxs-lookup"><span data-stu-id="b4a2c-143">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20191101Preview.ISourceControlConfiguration</span></span>

## <span data-ttu-id="b4a2c-144">상속자</span><span class="sxs-lookup"><span data-stu-id="b4a2c-144">NOTES</span></span>

<span data-ttu-id="b4a2c-145">별칭과</span><span class="sxs-lookup"><span data-stu-id="b4a2c-145">ALIASES</span></span>

<span data-ttu-id="b4a2c-146">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="b4a2c-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b4a2c-147">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4a2c-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b4a2c-148">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="b4a2c-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b4a2c-149">INPUTOBJECT <IKubernetesConfigurationIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b4a2c-149">INPUTOBJECT <IKubernetesConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b4a2c-150">`[ClusterName <String>]`: Kubernetes 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b4a2c-150">`[ClusterName <String>]`: The name of the kubernetes cluster.</span></span>
  - <span data-ttu-id="b4a2c-151">`[ClusterResourceName <String>]`: Kubernetes 클러스터 리소스 이름 (AKS 클러스터의 경우) 또는 connectedClusters (OnPrem K8S cluster의 경우)입니다.</span><span class="sxs-lookup"><span data-stu-id="b4a2c-151">`[ClusterResourceName <String>]`: The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="b4a2c-152">`[ClusterRp <String>]`: Kubernetes 클러스터 RP-ContainerService (AKS 클러스터의 경우) 또는 Microsoft. Kubernetes (OnPrem K8S cluster의 경우).</span><span class="sxs-lookup"><span data-stu-id="b4a2c-152">`[ClusterRp <String>]`: The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="b4a2c-153">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="b4a2c-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b4a2c-154">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b4a2c-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="b4a2c-155">`[SourceControlConfigurationName <String>]`: 소스 제어 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b4a2c-155">`[SourceControlConfigurationName <String>]`: Name of the Source Control Configuration.</span></span>
  - <span data-ttu-id="b4a2c-156">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b4a2c-156">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="b4a2c-157">GUID 형식 문자열입니다 (예: 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="b4a2c-157">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="b4a2c-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b4a2c-158">RELATED LINKS</span></span>

