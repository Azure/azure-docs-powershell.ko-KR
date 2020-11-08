---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/remove-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Remove-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Remove-AzKubernetesConfiguration.md
ms.openlocfilehash: 2a9547b88129a199f97bbcff9281348f9d2c4659
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211865"
---
# <span data-ttu-id="591ef-101">Remove-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="591ef-101">Remove-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="591ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="591ef-102">SYNOPSIS</span></span>
<span data-ttu-id="591ef-103">이렇게 하면 소스 제어 구성을 설정 하는 데 사용 되는 YAML 파일이 삭제 되므로 이후 원본 리포지토리에서의 동기화가 중지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="591ef-103">This will delete the YAML file used to set up the Source control configuration, thus stopping future sync from the source repo.</span></span>

## <span data-ttu-id="591ef-104">구문과</span><span class="sxs-lookup"><span data-stu-id="591ef-104">SYNTAX</span></span>

### <span data-ttu-id="591ef-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="591ef-105">Delete (Default)</span></span>
```
Remove-AzKubernetesConfiguration -ClusterName <String> -ClusterType <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="591ef-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="591ef-106">DeleteViaIdentity</span></span>
```
Remove-AzKubernetesConfiguration -InputObject <IKubernetesConfigurationIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="591ef-107">설명은</span><span class="sxs-lookup"><span data-stu-id="591ef-107">DESCRIPTION</span></span>
<span data-ttu-id="591ef-108">이렇게 하면 소스 제어 구성을 설정 하는 데 사용 되는 YAML 파일이 삭제 되므로 이후 원본 리포지토리에서의 동기화가 중지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="591ef-108">This will delete the YAML file used to set up the Source control configuration, thus stopping future sync from the source repo.</span></span>

## <span data-ttu-id="591ef-109">예제의</span><span class="sxs-lookup"><span data-stu-id="591ef-109">EXAMPLES</span></span>

### <span data-ttu-id="591ef-110">예제 1: 이름으로 kubernetes 클러스터의 configuation 제거</span><span class="sxs-lookup"><span data-stu-id="591ef-110">Example 1: Remove a configuation of kubernetes cluster by name</span></span>
```powershell
PS C:\> Remove-AzKubernetesConfiguration -ClusterName connaks-d983yc -ClusterType ConnectedClusters -ResourceGroupName connaks-rg-w9vlnp -Name conf-test01

```

<span data-ttu-id="591ef-111">이 명령은 kubernetes 클러스터의 configuation 이름을 이름으로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="591ef-111">This command removes a configuation of kubernetes cluster by name.</span></span>

### <span data-ttu-id="591ef-112">예제 2: kubernetes 클러스터의 configuation를 개체 별로 제거</span><span class="sxs-lookup"><span data-stu-id="591ef-112">Example 2: Remove a configuation of kubernetes cluster by object</span></span>
```powershell
PS C:\> $kubConf = Get-AzKubernetesConfiguration -ClusterName connaks-dkc29c -ClusterType ConnectedClusters -ResourceGroupName connaks-rg-w9vlnp -Name conf-test02 -ClusterRp Microsoft.Kubernetes
PS C:\> Remove-AzKubernetesConfiguration -InputObject $kubConf

```

<span data-ttu-id="591ef-113">이 명령은 kubernetes 클러스터의 configuation를 개체 별로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="591ef-113">This command removes a configuation of kubernetes cluster by object.</span></span>

## <span data-ttu-id="591ef-114">변수</span><span class="sxs-lookup"><span data-stu-id="591ef-114">PARAMETERS</span></span>

### <span data-ttu-id="591ef-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="591ef-115">-AsJob</span></span>
<span data-ttu-id="591ef-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="591ef-116">Run the command as a job</span></span>

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

### <span data-ttu-id="591ef-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="591ef-117">-ClusterName</span></span>
<span data-ttu-id="591ef-118">Kubernetes 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="591ef-118">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="591ef-119">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="591ef-119">-ClusterType</span></span>
<span data-ttu-id="591ef-120">Kubernetes 클러스터 리소스 이름 (AKS 클러스터의 경우) 또는 connectedClusters (OnPrem K8S 클러스터의 경우).</span><span class="sxs-lookup"><span data-stu-id="591ef-120">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="591ef-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="591ef-121">-DefaultProfile</span></span>
<span data-ttu-id="591ef-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="591ef-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="591ef-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="591ef-123">-InputObject</span></span>
<span data-ttu-id="591ef-124">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="591ef-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="591ef-125">-이름</span><span class="sxs-lookup"><span data-stu-id="591ef-125">-Name</span></span>
<span data-ttu-id="591ef-126">소스 제어 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="591ef-126">Name of the Source Control Configuration.</span></span>

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

### <span data-ttu-id="591ef-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="591ef-127">-NoWait</span></span>
<span data-ttu-id="591ef-128">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="591ef-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="591ef-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="591ef-129">-PassThru</span></span>
<span data-ttu-id="591ef-130">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="591ef-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="591ef-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="591ef-131">-ResourceGroupName</span></span>
<span data-ttu-id="591ef-132">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="591ef-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="591ef-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="591ef-133">-SubscriptionId</span></span>
<span data-ttu-id="591ef-134">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="591ef-134">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="591ef-135">-확인</span><span class="sxs-lookup"><span data-stu-id="591ef-135">-Confirm</span></span>
<span data-ttu-id="591ef-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="591ef-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="591ef-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="591ef-137">-WhatIf</span></span>
<span data-ttu-id="591ef-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="591ef-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="591ef-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="591ef-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="591ef-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="591ef-140">CommonParameters</span></span>
<span data-ttu-id="591ef-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="591ef-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="591ef-142">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="591ef-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="591ef-143">입력</span><span class="sxs-lookup"><span data-stu-id="591ef-143">INPUTS</span></span>

### <span data-ttu-id="591ef-144">KubernetesConfiguration. IKubernetesConfigurationIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="591ef-144">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span></span>

## <span data-ttu-id="591ef-145">출력</span><span class="sxs-lookup"><span data-stu-id="591ef-145">OUTPUTS</span></span>

### <span data-ttu-id="591ef-146">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="591ef-146">System.Boolean</span></span>

## <span data-ttu-id="591ef-147">상속자</span><span class="sxs-lookup"><span data-stu-id="591ef-147">NOTES</span></span>

<span data-ttu-id="591ef-148">별칭과</span><span class="sxs-lookup"><span data-stu-id="591ef-148">ALIASES</span></span>

<span data-ttu-id="591ef-149">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="591ef-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="591ef-150">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="591ef-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="591ef-151">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="591ef-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="591ef-152">INPUTOBJECT <IKubernetesConfigurationIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="591ef-152">INPUTOBJECT <IKubernetesConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="591ef-153">`[ClusterName <String>]`: Kubernetes 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="591ef-153">`[ClusterName <String>]`: The name of the kubernetes cluster.</span></span>
  - <span data-ttu-id="591ef-154">`[ClusterResourceName <String>]`: Kubernetes 클러스터 리소스 이름 (AKS 클러스터의 경우) 또는 connectedClusters (OnPrem K8S cluster의 경우)입니다.</span><span class="sxs-lookup"><span data-stu-id="591ef-154">`[ClusterResourceName <String>]`: The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="591ef-155">`[ClusterRp <String>]`: Kubernetes 클러스터 RP-ContainerService (AKS 클러스터의 경우) 또는 Microsoft. Kubernetes (OnPrem K8S cluster의 경우).</span><span class="sxs-lookup"><span data-stu-id="591ef-155">`[ClusterRp <String>]`: The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="591ef-156">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="591ef-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="591ef-157">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="591ef-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="591ef-158">`[SourceControlConfigurationName <String>]`: 소스 제어 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="591ef-158">`[SourceControlConfigurationName <String>]`: Name of the Source Control Configuration.</span></span>
  - <span data-ttu-id="591ef-159">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="591ef-159">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="591ef-160">GUID 형식 문자열입니다 (예: 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="591ef-160">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="591ef-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="591ef-161">RELATED LINKS</span></span>

