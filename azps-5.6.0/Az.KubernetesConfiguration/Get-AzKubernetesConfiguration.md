---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/powershell/module/az.kubernetesconfiguration/get-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
ms.openlocfilehash: 8cbf938917f26b1229b5c18d25448da4df3bb5b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976832"
---
# <span data-ttu-id="6a5f8-101">Get-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a5f8-101">Get-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="6a5f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a5f8-102">SYNOPSIS</span></span>
<span data-ttu-id="6a5f8-103">원본 제어 구성에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-103">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="6a5f8-104">구문</span><span class="sxs-lookup"><span data-stu-id="6a5f8-104">SYNTAX</span></span>

### <span data-ttu-id="6a5f8-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="6a5f8-105">List (Default)</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6a5f8-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="6a5f8-106">Get</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6a5f8-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6a5f8-107">GetViaIdentity</span></span>
```
Get-AzKubernetesConfiguration -InputObject <IKubernetesConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="6a5f8-108">설명</span><span class="sxs-lookup"><span data-stu-id="6a5f8-108">DESCRIPTION</span></span>
<span data-ttu-id="6a5f8-109">원본 제어 구성에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-109">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="6a5f8-110">예제</span><span class="sxs-lookup"><span data-stu-id="6a5f8-110">EXAMPLES</span></span>

### <span data-ttu-id="6a5f8-111">예제 1: kubernetes 클러스터의 모든 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-111">Example 1: Get all configurations of kubernetes cluster</span></span>
```powershell
PS C:\> Get-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:29:33 AM                                             12/21/2020 5:29:33 AM                                                          Microsoft.KubernetesConfiguration/so…
k8sconfig-t01 12/21/2020 5:26:17 AM                                             12/21/2020 5:27:45 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="6a5f8-112">이 명령은 kubernetes 클러스터의 모든 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-112">This command gets all configurations of kubernetes cluster.</span></span>

### <span data-ttu-id="6a5f8-113">예제 2: 이름에 따라 kubernetes 클러스터 구성을 구합니다.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-113">Example 2: Get a configuration of kubernetes cluster by name</span></span>
```powershell
PS C:\>  Get-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters -Name  k8sconfig-t02

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:29:33 AM                                             12/21/2020 5:29:33 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="6a5f8-114">이 명령은 이름으로 kubernetes 클러스터의 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-114">This command gets a configuration of kubernetes cluster by name.</span></span>

### <span data-ttu-id="6a5f8-115">예제 3: 개체에 따라 kubernetes 클러스터 구성을 구합니다.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-115">Example 3: Get a configuration of kubernetes cluster by object</span></span>
```powershell
PS C:\> $kubConf = New-AzKubernetesConfiguration -Name k8sconfig-t02 -ClusterName connaks-dkc29c -ResourceGroupName connaks-rg-w9vlnp -RepositoryUrl http://github.com/xxxx
PS C:\> Get-AzKubernetesConfiguration -InputObject $kubConf

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:29:33 AM                                             12/21/2020 5:29:33 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="6a5f8-116">이 명령은 개체에 따라 kubernetes 클러스터의 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-116">This command gets a configuration of kubernetes cluster by object.</span></span>

### <span data-ttu-id="6a5f8-117">예제 4: 파이프라인에 따라 kubernetes 클러스터 구성을 구합니다.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-117">Example 4: Get a configuration of kubernetes cluster by pipeline</span></span>
```powershell
PS C:\> @{Id='/subscriptions/xxxxx-xxxxxxx-xxxxx-xxxxxx/resourceGroups/connaks-rg-w9vlnp/providers/Microsoft.Kubernetes/connectedClusters/connaks-d983yc/providers/Microsoft.KubernetesConfiguration/sourceControlConfigurations/k8sconfig-t02'} | Get-AzKubernetesConfiguration

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:29:33 AM                                             12/21/2020 5:29:33 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="6a5f8-118">이 명령은 파이프라인에 따라 kubernetes 클러스터의 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-118">This command gets a configuration of kubernetes cluster by pipeline.</span></span>

## <span data-ttu-id="6a5f8-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6a5f8-119">PARAMETERS</span></span>

### <span data-ttu-id="6a5f8-120">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="6a5f8-120">-ClusterName</span></span>
<span data-ttu-id="6a5f8-121">kubernetes 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-121">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="6a5f8-122">-ClusterRp</span><span class="sxs-lookup"><span data-stu-id="6a5f8-122">-ClusterRp</span></span>
<span data-ttu-id="6a5f8-123">Kubernetes 클러스터 RP - Microsoft.ContainerService(AKS 클러스터용) 또는 Microsoft.Kubernetes(OnPrem K8S 클러스터용)입니다.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-123">The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="6a5f8-124">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="6a5f8-124">-ClusterType</span></span>
<span data-ttu-id="6a5f8-125">Kubernetes 클러스터 리소스 이름 - 관리되는Clusters(AKS 클러스터용) 또는 연결된Clusters(OnPrem K8S 클러스터의 경우)입니다.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-125">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="6a5f8-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a5f8-126">-DefaultProfile</span></span>
<span data-ttu-id="6a5f8-127">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a5f8-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a5f8-128">-InputObject</span></span>
<span data-ttu-id="6a5f8-129">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6a5f8-130">-Name</span><span class="sxs-lookup"><span data-stu-id="6a5f8-130">-Name</span></span>
<span data-ttu-id="6a5f8-131">원본 제어 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-131">Name of the Source Control Configuration.</span></span>

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

### <span data-ttu-id="6a5f8-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a5f8-132">-ResourceGroupName</span></span>
<span data-ttu-id="6a5f8-133">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="6a5f8-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6a5f8-134">-SubscriptionId</span></span>
<span data-ttu-id="6a5f8-135">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-135">The Azure subscription ID.</span></span>
<span data-ttu-id="6a5f8-136">GUID 형식 문자열입니다(예: 00000000-0000-0000-000000000)입니다.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-136">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="6a5f8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a5f8-137">CommonParameters</span></span>
<span data-ttu-id="6a5f8-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a5f8-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6a5f8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a5f8-140">입력</span><span class="sxs-lookup"><span data-stu-id="6a5f8-140">INPUTS</span></span>

### <span data-ttu-id="6a5f8-141">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="6a5f8-141">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span></span>

## <span data-ttu-id="6a5f8-142">출력</span><span class="sxs-lookup"><span data-stu-id="6a5f8-142">OUTPUTS</span></span>

### <span data-ttu-id="6a5f8-143">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20210301.ISourceControlConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a5f8-143">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20210301.ISourceControlConfiguration</span></span>

## <span data-ttu-id="6a5f8-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6a5f8-144">NOTES</span></span>

<span data-ttu-id="6a5f8-145">별칭</span><span class="sxs-lookup"><span data-stu-id="6a5f8-145">ALIASES</span></span>

<span data-ttu-id="6a5f8-146">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="6a5f8-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6a5f8-147">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6a5f8-148">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6a5f8-149">INPUTOBJECT <IKubernetesConfigurationIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="6a5f8-149">INPUTOBJECT <IKubernetesConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6a5f8-150">`[ClusterName <String>]`: kubernetes 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-150">`[ClusterName <String>]`: The name of the kubernetes cluster.</span></span>
  - <span data-ttu-id="6a5f8-151">`[ClusterResourceName <String>]`: Kubernetes 클러스터 리소스 이름 - 관리되는Clusters(AKS 클러스터용) 또는 연결된Clusters(OnPrem K8S 클러스터의 경우)입니다.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-151">`[ClusterResourceName <String>]`: The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="6a5f8-152">`[ClusterRp <String>]`: Kubernetes 클러스터 RP - Microsoft.ContainerService(AKS 클러스터용) 또는 Microsoft.Kubernetes(OnPrem K8S 클러스터용)입니다.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-152">`[ClusterRp <String>]`: The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="6a5f8-153">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="6a5f8-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6a5f8-154">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="6a5f8-155">`[SourceControlConfigurationName <String>]`: 원본 제어 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-155">`[SourceControlConfigurationName <String>]`: Name of the Source Control Configuration.</span></span>
  - <span data-ttu-id="6a5f8-156">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-156">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="6a5f8-157">GUID 형식 문자열입니다(예: 00000000-0000-0000-000000000)입니다.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-157">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="6a5f8-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6a5f8-158">RELATED LINKS</span></span>

