---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/new-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
ms.openlocfilehash: 70ff3c636f6c88ac89e53a5c2b1acb209aad274a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492862"
---
# <span data-ttu-id="91cac-101">New-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="91cac-101">New-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="91cac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91cac-102">SYNOPSIS</span></span>
<span data-ttu-id="91cac-103">새 Kubernetes 소스 제어 구성을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91cac-103">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="91cac-104">구문</span><span class="sxs-lookup"><span data-stu-id="91cac-104">SYNTAX</span></span>

```
New-AzKubernetesConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 -RepositoryUrl <String> [-ClusterType <String>] [-SubscriptionId <String>] [-ClusterScoped]
 [-EnableHelmOperator] [-HelmOperatorChartValues <String>] [-HelmOperatorChartVersion <String>]
 [-OperatorInstanceName <String>] [-OperatorNamespace <String>] [-OperatorParameters <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="91cac-105">설명</span><span class="sxs-lookup"><span data-stu-id="91cac-105">DESCRIPTION</span></span>
<span data-ttu-id="91cac-106">새 Kubernetes 소스 제어 구성을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91cac-106">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="91cac-107">예제</span><span class="sxs-lookup"><span data-stu-id="91cac-107">EXAMPLES</span></span>

### <span data-ttu-id="91cac-108">예제 1: kubernetes 클러스터에 대한 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="91cac-108">Example 1: Create a configuation for kubernetes cluster</span></span>
```powershell
PS C:\> New-AzKubernetesConfiguration -Name conf-test01 -ClusterName connaks-d983yc -ResourceGroupName connaks-rg-w9vlnp -RepositoryUrl http://github.com/xxxx

Name        Type
----        ----
conf-test01 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="91cac-109">이 명령은 kubernetes 클러스터에 대한 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91cac-109">This command creates a configuation for kubernetes cluster.</span></span>

## <span data-ttu-id="91cac-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91cac-110">PARAMETERS</span></span>

### <span data-ttu-id="91cac-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="91cac-111">-ClusterName</span></span>
<span data-ttu-id="91cac-112">kubernetes 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91cac-112">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="91cac-113">-ClusterScoped</span><span class="sxs-lookup"><span data-stu-id="91cac-113">-ClusterScoped</span></span>
<span data-ttu-id="91cac-114">전달된 경우 구성 범위를 클러스터로 설정(기본값: nameSpace)합니다.</span><span class="sxs-lookup"><span data-stu-id="91cac-114">If passed set the scope of the Configuration to Cluster (default is nameSpace).</span></span>

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

### <span data-ttu-id="91cac-115">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="91cac-115">-ClusterType</span></span>
<span data-ttu-id="91cac-116">Kubernetes 클러스터 리소스 이름 - managedClusters(AKS 클러스터용) 또는 connectedClusters(OnPrem K8S 클러스터의 경우)</span><span class="sxs-lookup"><span data-stu-id="91cac-116">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="91cac-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91cac-117">-DefaultProfile</span></span>
<span data-ttu-id="91cac-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="91cac-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91cac-119">-EnableHelmOperator</span><span class="sxs-lookup"><span data-stu-id="91cac-119">-EnableHelmOperator</span></span>
<span data-ttu-id="91cac-120">이 git 구성에 Helm 연산자를 사용하도록 설정하는 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="91cac-120">Option to enable Helm Operator for this git configuration.</span></span>

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

### <span data-ttu-id="91cac-121">-HelmOperatorChartValues</span><span class="sxs-lookup"><span data-stu-id="91cac-121">-HelmOperatorChartValues</span></span>
<span data-ttu-id="91cac-122">연산자 Helm 차트에 대한 값을 능가합니다.</span><span class="sxs-lookup"><span data-stu-id="91cac-122">Values override for the operator Helm chart.</span></span>

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

### <span data-ttu-id="91cac-123">-HelmOperatorChartVersion</span><span class="sxs-lookup"><span data-stu-id="91cac-123">-HelmOperatorChartVersion</span></span>
<span data-ttu-id="91cac-124">연산자 Helm 차트의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="91cac-124">Version of the operator Helm chart.</span></span>

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

### <span data-ttu-id="91cac-125">-Name</span><span class="sxs-lookup"><span data-stu-id="91cac-125">-Name</span></span>
<span data-ttu-id="91cac-126">소스 제어 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91cac-126">Name of the Source Control Configuration.</span></span>

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

### <span data-ttu-id="91cac-127">-OperatorInstanceName</span><span class="sxs-lookup"><span data-stu-id="91cac-127">-OperatorInstanceName</span></span>
<span data-ttu-id="91cac-128">연산자의 인스턴스 이름 - 특정 구성을 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="91cac-128">Instance name of the operator - identifying the specific configuration.</span></span>

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

### <span data-ttu-id="91cac-129">-OperatorNamespace</span><span class="sxs-lookup"><span data-stu-id="91cac-129">-OperatorNamespace</span></span>
<span data-ttu-id="91cac-130">이 연산자가 설치된 네임스페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="91cac-130">The namespace to which this operator is installed to.</span></span>
<span data-ttu-id="91cac-131">최대 253자 소문자 영속 문자, 하이픈 및 기간만 해당.</span><span class="sxs-lookup"><span data-stu-id="91cac-131">Maximum of 253 lower case alphanumeric characters, hyphen and period only.</span></span>

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

### <span data-ttu-id="91cac-132">-OperatorParameters</span><span class="sxs-lookup"><span data-stu-id="91cac-132">-OperatorParameters</span></span>
<span data-ttu-id="91cac-133">문자열 형식의 연산자 인스턴스에 대한 모든 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="91cac-133">Any Parameters for the Operator instance in string format.</span></span>

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

### <span data-ttu-id="91cac-134">-RepositoryUrl</span><span class="sxs-lookup"><span data-stu-id="91cac-134">-RepositoryUrl</span></span>
<span data-ttu-id="91cac-135">SourceControl 리포지토리의 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="91cac-135">Url of the SourceControl Repository.</span></span>

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

### <span data-ttu-id="91cac-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91cac-136">-ResourceGroupName</span></span>
<span data-ttu-id="91cac-137">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91cac-137">The name of the resource group.</span></span>

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

### <span data-ttu-id="91cac-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="91cac-138">-SubscriptionId</span></span>
<span data-ttu-id="91cac-139">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="91cac-139">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="91cac-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="91cac-140">-Confirm</span></span>
<span data-ttu-id="91cac-141">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="91cac-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91cac-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91cac-142">-WhatIf</span></span>
<span data-ttu-id="91cac-143">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="91cac-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91cac-144">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="91cac-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91cac-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91cac-145">CommonParameters</span></span>
<span data-ttu-id="91cac-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="91cac-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91cac-147">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="91cac-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91cac-148">입력</span><span class="sxs-lookup"><span data-stu-id="91cac-148">INPUTS</span></span>

## <span data-ttu-id="91cac-149">출력</span><span class="sxs-lookup"><span data-stu-id="91cac-149">OUTPUTS</span></span>

### <span data-ttu-id="91cac-150">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20191101Preview.ISourceControlConfiguration</span><span class="sxs-lookup"><span data-stu-id="91cac-150">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20191101Preview.ISourceControlConfiguration</span></span>

## <span data-ttu-id="91cac-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="91cac-151">NOTES</span></span>

<span data-ttu-id="91cac-152">별칭</span><span class="sxs-lookup"><span data-stu-id="91cac-152">ALIASES</span></span>

## <span data-ttu-id="91cac-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="91cac-153">RELATED LINKS</span></span>

