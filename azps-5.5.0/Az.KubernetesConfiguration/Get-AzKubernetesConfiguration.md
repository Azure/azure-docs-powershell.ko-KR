---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/get-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
ms.openlocfilehash: daa058d1f3cc13e073d8533403341dad3db7c319
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185348"
---
# <span data-ttu-id="51b6e-101">Get-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="51b6e-101">Get-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="51b6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51b6e-102">SYNOPSIS</span></span>
<span data-ttu-id="51b6e-103">소스 제어 구성에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="51b6e-103">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="51b6e-104">구문</span><span class="sxs-lookup"><span data-stu-id="51b6e-104">SYNTAX</span></span>

### <span data-ttu-id="51b6e-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="51b6e-105">List (Default)</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="51b6e-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="51b6e-106">Get</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="51b6e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="51b6e-107">GetViaIdentity</span></span>
```
Get-AzKubernetesConfiguration -InputObject <IKubernetesConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="51b6e-108">설명</span><span class="sxs-lookup"><span data-stu-id="51b6e-108">DESCRIPTION</span></span>
<span data-ttu-id="51b6e-109">소스 제어 구성에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="51b6e-109">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="51b6e-110">예제</span><span class="sxs-lookup"><span data-stu-id="51b6e-110">EXAMPLES</span></span>

### <span data-ttu-id="51b6e-111">예제 1: kubernetes 클러스터의 모든 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="51b6e-111">Example 1: Get all configurations of kubernetes cluster</span></span>
```powershell
PS C:\> Get-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:29:33 AM                                             12/21/2020 5:29:33 AM                                                          Microsoft.KubernetesConfiguration/so…
k8sconfig-t01 12/21/2020 5:26:17 AM                                             12/21/2020 5:27:45 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="51b6e-112">이 명령은 kubernetes 클러스터의 모든 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="51b6e-112">This command gets all configurations of kubernetes cluster.</span></span>

### <span data-ttu-id="51b6e-113">예제 2: 이름으로 kubernetes 클러스터의 구성을 구합니다.</span><span class="sxs-lookup"><span data-stu-id="51b6e-113">Example 2: Get a configuration of kubernetes cluster by name</span></span>
```powershell
PS C:\>  Get-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters -Name  k8sconfig-t02

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:29:33 AM                                             12/21/2020 5:29:33 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="51b6e-114">이 명령은 이름으로 kubernetes 클러스터의 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="51b6e-114">This command gets a configuration of kubernetes cluster by name.</span></span>

### <span data-ttu-id="51b6e-115">예제 3: 개체에 따라 kubernetes 클러스터의 구성을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="51b6e-115">Example 3: Get a configuration of kubernetes cluster by object</span></span>
```powershell
PS C:\> $kubConf = New-AzKubernetesConfiguration -Name k8sconfig-t02 -ClusterName connaks-dkc29c -ResourceGroupName connaks-rg-w9vlnp -RepositoryUrl http://github.com/xxxx
PS C:\> Get-AzKubernetesConfiguration -InputObject $kubConf

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:29:33 AM                                             12/21/2020 5:29:33 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="51b6e-116">이 명령은 개체에 따라 kubernetes 클러스터의 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="51b6e-116">This command gets a configuration of kubernetes cluster by object.</span></span>

### <span data-ttu-id="51b6e-117">예제 4: 파이프라인에 의해 kubernetes 클러스터 구성을 얻게</span><span class="sxs-lookup"><span data-stu-id="51b6e-117">Example 4: Get a configuration of kubernetes cluster by pipeline</span></span>
```powershell
PS C:\> @{Id='/subscriptions/xxxxx-xxxxxxx-xxxxx-xxxxxx/resourceGroups/connaks-rg-w9vlnp/providers/Microsoft.Kubernetes/connectedClusters/connaks-d983yc/providers/Microsoft.KubernetesConfiguration/sourceControlConfigurations/k8sconfig-t02'} | Get-AzKubernetesConfiguration

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:29:33 AM                                             12/21/2020 5:29:33 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="51b6e-118">이 명령은 파이프라인에 의해 kubernetes 클러스터의 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="51b6e-118">This command gets a configuration of kubernetes cluster by pipeline.</span></span>

## <span data-ttu-id="51b6e-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="51b6e-119">PARAMETERS</span></span>

### <span data-ttu-id="51b6e-120">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="51b6e-120">-ClusterName</span></span>
<span data-ttu-id="51b6e-121">kubernetes 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="51b6e-121">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="51b6e-122">-ClusterRp</span><span class="sxs-lookup"><span data-stu-id="51b6e-122">-ClusterRp</span></span>
<span data-ttu-id="51b6e-123">Kubernetes 클러스터 RP - Microsoft.ContainerService(AKS 클러스터용) 또는 Microsoft.Kubernetes(OnPrem K8S 클러스터의 경우)</span><span class="sxs-lookup"><span data-stu-id="51b6e-123">The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="51b6e-124">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="51b6e-124">-ClusterType</span></span>
<span data-ttu-id="51b6e-125">Kubernetes 클러스터 리소스 이름 - managedClusters(AKS 클러스터의 경우) 또는 connectedClusters(OnPrem K8S 클러스터의 경우)</span><span class="sxs-lookup"><span data-stu-id="51b6e-125">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="51b6e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51b6e-126">-DefaultProfile</span></span>
<span data-ttu-id="51b6e-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="51b6e-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51b6e-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51b6e-128">-InputObject</span></span>
<span data-ttu-id="51b6e-129">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="51b6e-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="51b6e-130">-Name</span><span class="sxs-lookup"><span data-stu-id="51b6e-130">-Name</span></span>
<span data-ttu-id="51b6e-131">소스 제어 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="51b6e-131">Name of the Source Control Configuration.</span></span>

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

### <span data-ttu-id="51b6e-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51b6e-132">-ResourceGroupName</span></span>
<span data-ttu-id="51b6e-133">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="51b6e-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="51b6e-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="51b6e-134">-SubscriptionId</span></span>
<span data-ttu-id="51b6e-135">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="51b6e-135">The Azure subscription ID.</span></span>
<span data-ttu-id="51b6e-136">GUID 형식 문자열입니다(예: 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="51b6e-136">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="51b6e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51b6e-137">CommonParameters</span></span>
<span data-ttu-id="51b6e-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="51b6e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51b6e-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="51b6e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51b6e-140">입력</span><span class="sxs-lookup"><span data-stu-id="51b6e-140">INPUTS</span></span>

### <span data-ttu-id="51b6e-141">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="51b6e-141">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span></span>

## <span data-ttu-id="51b6e-142">출력</span><span class="sxs-lookup"><span data-stu-id="51b6e-142">OUTPUTS</span></span>

### <span data-ttu-id="51b6e-143">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20201001Preview.ISourceControlConfiguration</span><span class="sxs-lookup"><span data-stu-id="51b6e-143">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20201001Preview.ISourceControlConfiguration</span></span>

## <span data-ttu-id="51b6e-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="51b6e-144">NOTES</span></span>

<span data-ttu-id="51b6e-145">별칭</span><span class="sxs-lookup"><span data-stu-id="51b6e-145">ALIASES</span></span>

<span data-ttu-id="51b6e-146">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="51b6e-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="51b6e-147">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="51b6e-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="51b6e-148">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="51b6e-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="51b6e-149">INPUTOBJECT: <IKubernetesConfigurationIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="51b6e-149">INPUTOBJECT <IKubernetesConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="51b6e-150">`[ClusterName <String>]`: kubernetes 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="51b6e-150">`[ClusterName <String>]`: The name of the kubernetes cluster.</span></span>
  - <span data-ttu-id="51b6e-151">`[ClusterResourceName <String>]`: Kubernetes 클러스터 리소스 이름 - managedClusters(AKS 클러스터용) 또는 connectedClusters(OnPrem K8S 클러스터의 경우)</span><span class="sxs-lookup"><span data-stu-id="51b6e-151">`[ClusterResourceName <String>]`: The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="51b6e-152">`[ClusterRp <String>]`: Kubernetes 클러스터 RP - Microsoft.ContainerService(AKS 클러스터용) 또는 Microsoft.Kubernetes(OnPrem K8S 클러스터의 경우)</span><span class="sxs-lookup"><span data-stu-id="51b6e-152">`[ClusterRp <String>]`: The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="51b6e-153">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="51b6e-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="51b6e-154">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="51b6e-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="51b6e-155">`[SourceControlConfigurationName <String>]`: 소스 제어 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="51b6e-155">`[SourceControlConfigurationName <String>]`: Name of the Source Control Configuration.</span></span>
  - <span data-ttu-id="51b6e-156">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="51b6e-156">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="51b6e-157">GUID 형식 문자열입니다(예: 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="51b6e-157">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="51b6e-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="51b6e-158">RELATED LINKS</span></span>

