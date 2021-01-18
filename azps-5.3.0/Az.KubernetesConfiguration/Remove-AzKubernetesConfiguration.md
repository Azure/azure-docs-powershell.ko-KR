---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/remove-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Remove-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Remove-AzKubernetesConfiguration.md
ms.openlocfilehash: 2a9547b88129a199f97bbcff9281348f9d2c4659
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492856"
---
# <span data-ttu-id="1aa77-101">Remove-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="1aa77-101">Remove-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="1aa77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1aa77-102">SYNOPSIS</span></span>
<span data-ttu-id="1aa77-103">이렇게 하면 원본 제어 구성을 설정하는 데 사용되는 YAML 파일이 삭제되어 원본 리포지터에서 향후 동기화가 중지됩니다.</span><span class="sxs-lookup"><span data-stu-id="1aa77-103">This will delete the YAML file used to set up the Source control configuration, thus stopping future sync from the source repo.</span></span>

## <span data-ttu-id="1aa77-104">구문</span><span class="sxs-lookup"><span data-stu-id="1aa77-104">SYNTAX</span></span>

### <span data-ttu-id="1aa77-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="1aa77-105">Delete (Default)</span></span>
```
Remove-AzKubernetesConfiguration -ClusterName <String> -ClusterType <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1aa77-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1aa77-106">DeleteViaIdentity</span></span>
```
Remove-AzKubernetesConfiguration -InputObject <IKubernetesConfigurationIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1aa77-107">설명</span><span class="sxs-lookup"><span data-stu-id="1aa77-107">DESCRIPTION</span></span>
<span data-ttu-id="1aa77-108">이렇게 하면 원본 제어 구성을 설정하는 데 사용되는 YAML 파일이 삭제되어 원본 리포지터에서 향후 동기화가 중지됩니다.</span><span class="sxs-lookup"><span data-stu-id="1aa77-108">This will delete the YAML file used to set up the Source control configuration, thus stopping future sync from the source repo.</span></span>

## <span data-ttu-id="1aa77-109">예제</span><span class="sxs-lookup"><span data-stu-id="1aa77-109">EXAMPLES</span></span>

### <span data-ttu-id="1aa77-110">예제 1: 이름으로 kubernetes 클러스터의 구성 제거</span><span class="sxs-lookup"><span data-stu-id="1aa77-110">Example 1: Remove a configuation of kubernetes cluster by name</span></span>
```powershell
PS C:\> Remove-AzKubernetesConfiguration -ClusterName connaks-d983yc -ClusterType ConnectedClusters -ResourceGroupName connaks-rg-w9vlnp -Name conf-test01

```

<span data-ttu-id="1aa77-111">이 명령은 kubernetes 클러스터의 구성을 이름으로 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1aa77-111">This command removes a configuation of kubernetes cluster by name.</span></span>

### <span data-ttu-id="1aa77-112">예제 2: 개체로 kubernetes 클러스터의 구성 제거</span><span class="sxs-lookup"><span data-stu-id="1aa77-112">Example 2: Remove a configuation of kubernetes cluster by object</span></span>
```powershell
PS C:\> $kubConf = Get-AzKubernetesConfiguration -ClusterName connaks-dkc29c -ClusterType ConnectedClusters -ResourceGroupName connaks-rg-w9vlnp -Name conf-test02 -ClusterRp Microsoft.Kubernetes
PS C:\> Remove-AzKubernetesConfiguration -InputObject $kubConf

```

<span data-ttu-id="1aa77-113">이 명령은 개체에 따라 kubernetes 클러스터의 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1aa77-113">This command removes a configuation of kubernetes cluster by object.</span></span>

## <span data-ttu-id="1aa77-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1aa77-114">PARAMETERS</span></span>

### <span data-ttu-id="1aa77-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1aa77-115">-AsJob</span></span>
<span data-ttu-id="1aa77-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="1aa77-116">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aa77-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1aa77-117">-ClusterName</span></span>
<span data-ttu-id="1aa77-118">kubernetes 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1aa77-118">The name of the kubernetes cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aa77-119">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="1aa77-119">-ClusterType</span></span>
<span data-ttu-id="1aa77-120">Kubernetes 클러스터 리소스 이름 - managedClusters(AKS 클러스터용) 또는 connectedClusters(OnPrem K8S 클러스터의 경우)</span><span class="sxs-lookup"><span data-stu-id="1aa77-120">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aa77-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1aa77-121">-DefaultProfile</span></span>
<span data-ttu-id="1aa77-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1aa77-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1aa77-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1aa77-123">-InputObject</span></span>
<span data-ttu-id="1aa77-124">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="1aa77-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1aa77-125">-Name</span><span class="sxs-lookup"><span data-stu-id="1aa77-125">-Name</span></span>
<span data-ttu-id="1aa77-126">소스 제어 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1aa77-126">Name of the Source Control Configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SourceControlConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aa77-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1aa77-127">-NoWait</span></span>
<span data-ttu-id="1aa77-128">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="1aa77-128">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aa77-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1aa77-129">-PassThru</span></span>
<span data-ttu-id="1aa77-130">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="1aa77-130">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aa77-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1aa77-131">-ResourceGroupName</span></span>
<span data-ttu-id="1aa77-132">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1aa77-132">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aa77-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1aa77-133">-SubscriptionId</span></span>
<span data-ttu-id="1aa77-134">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1aa77-134">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aa77-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1aa77-135">-Confirm</span></span>
<span data-ttu-id="1aa77-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1aa77-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1aa77-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1aa77-137">-WhatIf</span></span>
<span data-ttu-id="1aa77-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1aa77-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1aa77-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1aa77-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1aa77-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1aa77-140">CommonParameters</span></span>
<span data-ttu-id="1aa77-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1aa77-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1aa77-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1aa77-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1aa77-143">입력</span><span class="sxs-lookup"><span data-stu-id="1aa77-143">INPUTS</span></span>

### <span data-ttu-id="1aa77-144">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="1aa77-144">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span></span>

## <span data-ttu-id="1aa77-145">출력</span><span class="sxs-lookup"><span data-stu-id="1aa77-145">OUTPUTS</span></span>

### <span data-ttu-id="1aa77-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1aa77-146">System.Boolean</span></span>

## <span data-ttu-id="1aa77-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1aa77-147">NOTES</span></span>

<span data-ttu-id="1aa77-148">별칭</span><span class="sxs-lookup"><span data-stu-id="1aa77-148">ALIASES</span></span>

<span data-ttu-id="1aa77-149">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="1aa77-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1aa77-150">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="1aa77-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1aa77-151">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1aa77-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1aa77-152">INPUTOBJECT: <IKubernetesConfigurationIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1aa77-152">INPUTOBJECT <IKubernetesConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1aa77-153">`[ClusterName <String>]`: kubernetes 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1aa77-153">`[ClusterName <String>]`: The name of the kubernetes cluster.</span></span>
  - <span data-ttu-id="1aa77-154">`[ClusterResourceName <String>]`: Kubernetes 클러스터 리소스 이름 - managedClusters(AKS 클러스터용) 또는 connectedClusters(OnPrem K8S 클러스터의 경우)</span><span class="sxs-lookup"><span data-stu-id="1aa77-154">`[ClusterResourceName <String>]`: The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="1aa77-155">`[ClusterRp <String>]`: Kubernetes 클러스터 RP - Microsoft.ContainerService(AKS 클러스터용) 또는 Microsoft.Kubernetes(OnPrem K8S 클러스터의 경우)</span><span class="sxs-lookup"><span data-stu-id="1aa77-155">`[ClusterRp <String>]`: The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="1aa77-156">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="1aa77-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1aa77-157">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1aa77-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="1aa77-158">`[SourceControlConfigurationName <String>]`: 소스 제어 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1aa77-158">`[SourceControlConfigurationName <String>]`: Name of the Source Control Configuration.</span></span>
  - <span data-ttu-id="1aa77-159">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1aa77-159">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="1aa77-160">GUID 형식 문자열입니다(예: 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="1aa77-160">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="1aa77-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1aa77-161">RELATED LINKS</span></span>

