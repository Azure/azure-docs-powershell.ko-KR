---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/powershell/module/az.kubernetesconfiguration/new-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
ms.openlocfilehash: 0040ab3bc037527400ea1f3eabf3c887189fc73c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976827"
---
# <span data-ttu-id="804e8-101">New-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="804e8-101">New-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="804e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="804e8-102">SYNOPSIS</span></span>
<span data-ttu-id="804e8-103">새 Kubernetes 원본 제어 구성을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="804e8-103">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="804e8-104">구문</span><span class="sxs-lookup"><span data-stu-id="804e8-104">SYNTAX</span></span>

```
New-AzKubernetesConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 -RepositoryUrl <String> [-ClusterType <String>] [-SubscriptionId <String>] [-ClusterScoped]
 [-EnableHelmOperator] [-HelmOperatorChartValues <String>] [-HelmOperatorChartVersion <String>]
 [-OperatorInstanceName <String>] [-OperatorNamespace <String>] [-OperatorParameters <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="804e8-105">설명</span><span class="sxs-lookup"><span data-stu-id="804e8-105">DESCRIPTION</span></span>
<span data-ttu-id="804e8-106">새 Kubernetes 원본 제어 구성을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="804e8-106">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="804e8-107">예제</span><span class="sxs-lookup"><span data-stu-id="804e8-107">EXAMPLES</span></span>

### <span data-ttu-id="804e8-108">예제 1: kubernetes 클러스터에 대한 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="804e8-108">Example 1: Create a configuration for kubernetes cluster</span></span>
```powershell
PS C:\> New-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -Name k8sconfig-t01 -RepositoryUrl http://github.com/xxxx

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t01 12/21/2020 5:26:17 AM                                             12/21/2020 5:26:17 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="804e8-109">이 명령은 kubernetes 클러스터에 대한 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="804e8-109">This command creates a configuration for kubernetes cluster.</span></span>

### <span data-ttu-id="804e8-110">예제 1: Paramter OperatorNamespace를 지정하여 kubernetes 클러스터에 대한 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="804e8-110">Example 1: Create a configuration for kubernetes cluster with specify paramter OperatorNamespace</span></span>
```powershell
PS C:\> New-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -Name k8sconfig-t02 -RepositoryUrl http://github.com/xxxx -OperatorNamespace namespace-t01

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:26:17 AM                                             12/21/2020 5:26:17 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="804e8-111">이 명령은 kubernetes 클러스터에 대한 새 연산자 네임스페이스에 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="804e8-111">This command creates a configuration in the new operator namespace for kubernetes cluster.</span></span>
<span data-ttu-id="804e8-112">참고로 기존 연산자 네임스페이스에서 구성을 만들 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="804e8-112">Note, Unable to create a configuration in an existing operator namespace.</span></span>

## <span data-ttu-id="804e8-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="804e8-113">PARAMETERS</span></span>

### <span data-ttu-id="804e8-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="804e8-114">-ClusterName</span></span>
<span data-ttu-id="804e8-115">kubernetes 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="804e8-115">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="804e8-116">-ClusterScoped</span><span class="sxs-lookup"><span data-stu-id="804e8-116">-ClusterScoped</span></span>
<span data-ttu-id="804e8-117">전달된 경우 구성에서 클러스터로의 범위를 설정합니다(기본값은 nameSpace입니다).</span><span class="sxs-lookup"><span data-stu-id="804e8-117">If passed set the scope of the Configuration to Cluster (default is nameSpace).</span></span>

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

### <span data-ttu-id="804e8-118">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="804e8-118">-ClusterType</span></span>
<span data-ttu-id="804e8-119">Kubernetes 클러스터 리소스 이름 - 관리되는Clusters(AKS 클러스터용) 또는 연결된Clusters(OnPrem K8S 클러스터의 경우)입니다.</span><span class="sxs-lookup"><span data-stu-id="804e8-119">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="804e8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="804e8-120">-DefaultProfile</span></span>
<span data-ttu-id="804e8-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="804e8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="804e8-122">-EnableHelmOperator</span><span class="sxs-lookup"><span data-stu-id="804e8-122">-EnableHelmOperator</span></span>
<span data-ttu-id="804e8-123">이 git 구성에 대해 Helm 연산자를 사용하도록 설정하는 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="804e8-123">Option to enable Helm Operator for this git configuration.</span></span>

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

### <span data-ttu-id="804e8-124">-HelmOperatorChartValues</span><span class="sxs-lookup"><span data-stu-id="804e8-124">-HelmOperatorChartValues</span></span>
<span data-ttu-id="804e8-125">연산자 Helm 차트에 대한 값이 오버라이드됩니다.</span><span class="sxs-lookup"><span data-stu-id="804e8-125">Values override for the operator Helm chart.</span></span>

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

### <span data-ttu-id="804e8-126">-HelmOperatorChartVersion</span><span class="sxs-lookup"><span data-stu-id="804e8-126">-HelmOperatorChartVersion</span></span>
<span data-ttu-id="804e8-127">연산자 Helm 차트의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="804e8-127">Version of the operator Helm chart.</span></span>

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

### <span data-ttu-id="804e8-128">-Name</span><span class="sxs-lookup"><span data-stu-id="804e8-128">-Name</span></span>
<span data-ttu-id="804e8-129">원본 제어 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="804e8-129">Name of the Source Control Configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceControlConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="804e8-130">-OperatorInstanceName</span><span class="sxs-lookup"><span data-stu-id="804e8-130">-OperatorInstanceName</span></span>
<span data-ttu-id="804e8-131">연산자의 인스턴스 이름 - 특정 구성을 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="804e8-131">Instance name of the operator - identifying the specific configuration.</span></span>

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

### <span data-ttu-id="804e8-132">-OperatorNamespace</span><span class="sxs-lookup"><span data-stu-id="804e8-132">-OperatorNamespace</span></span>
<span data-ttu-id="804e8-133">이 연산자가 설치되는 네임스페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="804e8-133">The namespace to which this operator is installed to.</span></span>
<span data-ttu-id="804e8-134">최대 253개 소문자 영수 문자, 하이픈 및 기간만 해당합니다.</span><span class="sxs-lookup"><span data-stu-id="804e8-134">Maximum of 253 lower case alphanumeric characters, hyphen and period only.</span></span>

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

### <span data-ttu-id="804e8-135">-OperatorParameters</span><span class="sxs-lookup"><span data-stu-id="804e8-135">-OperatorParameters</span></span>
<span data-ttu-id="804e8-136">문자열 형식의 연산자 인스턴스에 대한 모든 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="804e8-136">Any Parameters for the Operator instance in string format.</span></span>

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

### <span data-ttu-id="804e8-137">-리포지토리Url</span><span class="sxs-lookup"><span data-stu-id="804e8-137">-RepositoryUrl</span></span>
<span data-ttu-id="804e8-138">SourceControl 리포지토리의 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="804e8-138">Url of the SourceControl Repository.</span></span>

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

### <span data-ttu-id="804e8-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="804e8-139">-ResourceGroupName</span></span>
<span data-ttu-id="804e8-140">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="804e8-140">The name of the resource group.</span></span>

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

### <span data-ttu-id="804e8-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="804e8-141">-SubscriptionId</span></span>
<span data-ttu-id="804e8-142">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="804e8-142">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="804e8-143">-확인</span><span class="sxs-lookup"><span data-stu-id="804e8-143">-Confirm</span></span>
<span data-ttu-id="804e8-144">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="804e8-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="804e8-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="804e8-145">-WhatIf</span></span>
<span data-ttu-id="804e8-146">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="804e8-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="804e8-147">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="804e8-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="804e8-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="804e8-148">CommonParameters</span></span>
<span data-ttu-id="804e8-149">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="804e8-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="804e8-150">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="804e8-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="804e8-151">입력</span><span class="sxs-lookup"><span data-stu-id="804e8-151">INPUTS</span></span>

## <span data-ttu-id="804e8-152">출력</span><span class="sxs-lookup"><span data-stu-id="804e8-152">OUTPUTS</span></span>

### <span data-ttu-id="804e8-153">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20210301.ISourceControlConfiguration</span><span class="sxs-lookup"><span data-stu-id="804e8-153">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20210301.ISourceControlConfiguration</span></span>

## <span data-ttu-id="804e8-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="804e8-154">NOTES</span></span>

<span data-ttu-id="804e8-155">별칭</span><span class="sxs-lookup"><span data-stu-id="804e8-155">ALIASES</span></span>

## <span data-ttu-id="804e8-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="804e8-156">RELATED LINKS</span></span>

