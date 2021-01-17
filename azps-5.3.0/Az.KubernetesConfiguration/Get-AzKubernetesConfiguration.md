---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/get-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
ms.openlocfilehash: 3fd93e42b8f38659f61fcbeb0f49040409f635a8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490232"
---
# <span data-ttu-id="a5ea4-101">Get-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5ea4-101">Get-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="a5ea4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5ea4-102">SYNOPSIS</span></span>
<span data-ttu-id="a5ea4-103">소스 제어 구성에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a5ea4-103">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="a5ea4-104">구문</span><span class="sxs-lookup"><span data-stu-id="a5ea4-104">SYNTAX</span></span>

### <span data-ttu-id="a5ea4-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="a5ea4-105">List (Default)</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a5ea4-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="a5ea4-106">Get</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a5ea4-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a5ea4-107">GetViaIdentity</span></span>
```
Get-AzKubernetesConfiguration -InputObject <IKubernetesConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a5ea4-108">설명</span><span class="sxs-lookup"><span data-stu-id="a5ea4-108">DESCRIPTION</span></span>
<span data-ttu-id="a5ea4-109">소스 제어 구성에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a5ea4-109">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="a5ea4-110">예제</span><span class="sxs-lookup"><span data-stu-id="a5ea4-110">EXAMPLES</span></span>

### <span data-ttu-id="a5ea4-111">예제 1: kubernetes 클러스터의 모든 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a5ea4-111">Example 1: Get all configurations of kubernetes cluster</span></span>
```powershell
PS C:\> Get-AzKubernetesConfiguration -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t02 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters

Name        Type
----        ----
conf-test01 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="a5ea4-112">이 명령은 kubernetes 클러스터의 모든 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a5ea4-112">This command gets all configurations of kubernetes cluster.</span></span>

### <span data-ttu-id="a5ea4-113">예제 2: 이름으로 kubernetes 클러스터의 구성을 구합니다.</span><span class="sxs-lookup"><span data-stu-id="a5ea4-113">Example 2: Get a configuration of kubernetes cluster by name</span></span>
```powershell
PS C:\> Get-AzKubernetesConfiguration -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t02 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters -Name conf-t02

Name     Type
----     ----
conf-t02 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="a5ea4-114">이 명령은 이름으로 kubernetes 클러스터의 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a5ea4-114">This command gets a configuration of kubernetes cluster by name.</span></span>

### <span data-ttu-id="a5ea4-115">예제 3: 개체에 따라 kubernetes 클러스터의 구성을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5ea4-115">Example 3: Get a configuration of kubernetes cluster by object</span></span>
```powershell
PS C:\> $kubConf = New-AzKubernetesConfiguration -Name conf-test02 -ClusterName connaks-dkc29c -ResourceGroupName connaks-rg-w9vlnp -RepositoryUrl http://github.com/xxxx
PS C:\> Get-AzKubernetesConfiguration -InputObject $kubConf

Name     Type
----     ----
conf-t02 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="a5ea4-116">이 명령은 개체에 따라 kubernetes 클러스터의 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a5ea4-116">This command gets a configuration of kubernetes cluster by object.</span></span>

### <span data-ttu-id="a5ea4-117">예제 4: 파이프라인에 의해 kubernetes 클러스터 구성을 얻게</span><span class="sxs-lookup"><span data-stu-id="a5ea4-117">Example 4: Get a configuration of kubernetes cluster by pipeline</span></span>
```powershell
PS C:\> @{Id='/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/connaks-rg-w9vlnp/providers/Microsoft.Kubernetes/connectedClusters/connaks-d983yc/providers/Microsoft.KubernetesConfiguration/sourceControlConfigurations/conf-test01'} | Get-AzKubernetesConfiguration

Name        Type
----        ----
conf-test01 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="a5ea4-118">이 명령은 파이프라인에 의해 kubernetes 클러스터의 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a5ea4-118">This command gets a configuration of kubernetes cluster by pipeline.</span></span>

## <span data-ttu-id="a5ea4-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5ea4-119">PARAMETERS</span></span>

### <span data-ttu-id="a5ea4-120">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a5ea4-120">-ClusterName</span></span>
<span data-ttu-id="a5ea4-121">kubernetes 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5ea4-121">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="a5ea4-122">-ClusterRp</span><span class="sxs-lookup"><span data-stu-id="a5ea4-122">-ClusterRp</span></span>
<span data-ttu-id="a5ea4-123">Kubernetes 클러스터 RP - Microsoft.ContainerService(AKS 클러스터용) 또는 Microsoft.Kubernetes(OnPrem K8S 클러스터의 경우)</span><span class="sxs-lookup"><span data-stu-id="a5ea4-123">The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="a5ea4-124">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="a5ea4-124">-ClusterType</span></span>
<span data-ttu-id="a5ea4-125">Kubernetes 클러스터 리소스 이름 - managedClusters(AKS 클러스터용) 또는 connectedClusters(OnPrem K8S 클러스터의 경우)</span><span class="sxs-lookup"><span data-stu-id="a5ea4-125">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="a5ea4-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5ea4-126">-DefaultProfile</span></span>
<span data-ttu-id="a5ea4-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a5ea4-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5ea4-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5ea4-128">-InputObject</span></span>
<span data-ttu-id="a5ea4-129">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="a5ea4-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a5ea4-130">-Name</span><span class="sxs-lookup"><span data-stu-id="a5ea4-130">-Name</span></span>
<span data-ttu-id="a5ea4-131">소스 제어 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5ea4-131">Name of the Source Control Configuration.</span></span>

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

### <span data-ttu-id="a5ea4-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5ea4-132">-ResourceGroupName</span></span>
<span data-ttu-id="a5ea4-133">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5ea4-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="a5ea4-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a5ea4-134">-SubscriptionId</span></span>
<span data-ttu-id="a5ea4-135">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a5ea4-135">The Azure subscription ID.</span></span>
<span data-ttu-id="a5ea4-136">GUID 형식 문자열입니다(예: 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="a5ea4-136">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="a5ea4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5ea4-137">CommonParameters</span></span>
<span data-ttu-id="a5ea4-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a5ea4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5ea4-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a5ea4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5ea4-140">입력</span><span class="sxs-lookup"><span data-stu-id="a5ea4-140">INPUTS</span></span>

### <span data-ttu-id="a5ea4-141">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="a5ea4-141">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span></span>

## <span data-ttu-id="a5ea4-142">출력</span><span class="sxs-lookup"><span data-stu-id="a5ea4-142">OUTPUTS</span></span>

### <span data-ttu-id="a5ea4-143">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20191101Preview.ISourceControlConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5ea4-143">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20191101Preview.ISourceControlConfiguration</span></span>

## <span data-ttu-id="a5ea4-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a5ea4-144">NOTES</span></span>

<span data-ttu-id="a5ea4-145">별칭</span><span class="sxs-lookup"><span data-stu-id="a5ea4-145">ALIASES</span></span>

<span data-ttu-id="a5ea4-146">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="a5ea4-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a5ea4-147">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="a5ea4-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a5ea4-148">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a5ea4-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a5ea4-149">INPUTOBJECT: <IKubernetesConfigurationIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="a5ea4-149">INPUTOBJECT <IKubernetesConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a5ea4-150">`[ClusterName <String>]`: kubernetes 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5ea4-150">`[ClusterName <String>]`: The name of the kubernetes cluster.</span></span>
  - <span data-ttu-id="a5ea4-151">`[ClusterResourceName <String>]`: Kubernetes 클러스터 리소스 이름 - managedClusters(AKS 클러스터용) 또는 connectedClusters(OnPrem K8S 클러스터의 경우)</span><span class="sxs-lookup"><span data-stu-id="a5ea4-151">`[ClusterResourceName <String>]`: The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="a5ea4-152">`[ClusterRp <String>]`: Kubernetes 클러스터 RP - Microsoft.ContainerService(AKS 클러스터용) 또는 Microsoft.Kubernetes(OnPrem K8S 클러스터의 경우)</span><span class="sxs-lookup"><span data-stu-id="a5ea4-152">`[ClusterRp <String>]`: The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="a5ea4-153">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="a5ea4-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a5ea4-154">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5ea4-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="a5ea4-155">`[SourceControlConfigurationName <String>]`: 소스 제어 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5ea4-155">`[SourceControlConfigurationName <String>]`: Name of the Source Control Configuration.</span></span>
  - <span data-ttu-id="a5ea4-156">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a5ea4-156">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="a5ea4-157">GUID 형식 문자열입니다(예: 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="a5ea4-157">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="a5ea4-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a5ea4-158">RELATED LINKS</span></span>

