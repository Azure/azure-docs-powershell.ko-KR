---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/new-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
ms.openlocfilehash: 70ff3c636f6c88ac89e53a5c2b1acb209aad274a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226903"
---
# <span data-ttu-id="2828f-101">New-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="2828f-101">New-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="2828f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2828f-102">SYNOPSIS</span></span>
<span data-ttu-id="2828f-103">새 Kubernetes 원본 컨트롤 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2828f-103">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="2828f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2828f-104">SYNTAX</span></span>

```
New-AzKubernetesConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 -RepositoryUrl <String> [-ClusterType <String>] [-SubscriptionId <String>] [-ClusterScoped]
 [-EnableHelmOperator] [-HelmOperatorChartValues <String>] [-HelmOperatorChartVersion <String>]
 [-OperatorInstanceName <String>] [-OperatorNamespace <String>] [-OperatorParameters <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2828f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2828f-105">DESCRIPTION</span></span>
<span data-ttu-id="2828f-106">새 Kubernetes 원본 컨트롤 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2828f-106">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="2828f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2828f-107">EXAMPLES</span></span>

### <span data-ttu-id="2828f-108">예제 1: kubernetes cluster에 대 한 configuation 만들기</span><span class="sxs-lookup"><span data-stu-id="2828f-108">Example 1: Create a configuation for kubernetes cluster</span></span>
```powershell
PS C:\> New-AzKubernetesConfiguration -Name conf-test01 -ClusterName connaks-d983yc -ResourceGroupName connaks-rg-w9vlnp -RepositoryUrl http://github.com/xxxx

Name        Type
----        ----
conf-test01 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="2828f-109">이 명령은 kubernetes cluster에 대 한 configuation를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2828f-109">This command creates a configuation for kubernetes cluster.</span></span>

## <span data-ttu-id="2828f-110">변수</span><span class="sxs-lookup"><span data-stu-id="2828f-110">PARAMETERS</span></span>

### <span data-ttu-id="2828f-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2828f-111">-ClusterName</span></span>
<span data-ttu-id="2828f-112">Kubernetes 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2828f-112">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="2828f-113">-ClusterScoped</span><span class="sxs-lookup"><span data-stu-id="2828f-113">-ClusterScoped</span></span>
<span data-ttu-id="2828f-114">성공으로 구성 범위를 Cluster (기본값은 네임 스페이스)로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2828f-114">If passed set the scope of the Configuration to Cluster (default is nameSpace).</span></span>

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

### <span data-ttu-id="2828f-115">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="2828f-115">-ClusterType</span></span>
<span data-ttu-id="2828f-116">Kubernetes 클러스터 리소스 이름 (AKS 클러스터의 경우) 또는 connectedClusters (OnPrem K8S 클러스터의 경우).</span><span class="sxs-lookup"><span data-stu-id="2828f-116">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="2828f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2828f-117">-DefaultProfile</span></span>
<span data-ttu-id="2828f-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2828f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2828f-119">-Enable<c13> Moperon</span><span class="sxs-lookup"><span data-stu-id="2828f-119">-EnableHelmOperator</span></span>
<span data-ttu-id="2828f-120">이 git 구성에 대해 투구 연산자를 사용 하도록 설정 하는 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="2828f-120">Option to enable Helm Operator for this git configuration.</span></span>

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

### <span data-ttu-id="2828f-121">-이 모 Chart값</span><span class="sxs-lookup"><span data-stu-id="2828f-121">-HelmOperatorChartValues</span></span>
<span data-ttu-id="2828f-122">연산자 투구 차트에 대 한 값 재정의.</span><span class="sxs-lookup"><span data-stu-id="2828f-122">Values override for the operator Helm chart.</span></span>

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

### <span data-ttu-id="2828f-123">-기타 Moper<c13> Chartversion</span><span class="sxs-lookup"><span data-stu-id="2828f-123">-HelmOperatorChartVersion</span></span>
<span data-ttu-id="2828f-124">연산자 투구 차트의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="2828f-124">Version of the operator Helm chart.</span></span>

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

### <span data-ttu-id="2828f-125">-이름</span><span class="sxs-lookup"><span data-stu-id="2828f-125">-Name</span></span>
<span data-ttu-id="2828f-126">소스 제어 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2828f-126">Name of the Source Control Configuration.</span></span>

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

### <span data-ttu-id="2828f-127">-OperatorInstanceName</span><span class="sxs-lookup"><span data-stu-id="2828f-127">-OperatorInstanceName</span></span>
<span data-ttu-id="2828f-128">연산자의 인스턴스 이름-특정 구성을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="2828f-128">Instance name of the operator - identifying the specific configuration.</span></span>

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

### <span data-ttu-id="2828f-129">-OperatorNamespace</span><span class="sxs-lookup"><span data-stu-id="2828f-129">-OperatorNamespace</span></span>
<span data-ttu-id="2828f-130">이 연산자가 설치 되어 있는 네임 스페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="2828f-130">The namespace to which this operator is installed to.</span></span>
<span data-ttu-id="2828f-131">최대 253 소문자 영숫자 문자, 하이픈 및 마침표만에만 해당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2828f-131">Maximum of 253 lower case alphanumeric characters, hyphen and period only.</span></span>

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

### <span data-ttu-id="2828f-132">-OperatorParameters</span><span class="sxs-lookup"><span data-stu-id="2828f-132">-OperatorParameters</span></span>
<span data-ttu-id="2828f-133">문자열 형식의 연산자 인스턴스에 대 한 모든 매개 변수</span><span class="sxs-lookup"><span data-stu-id="2828f-133">Any Parameters for the Operator instance in string format.</span></span>

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

### <span data-ttu-id="2828f-134">-RepositoryUrl</span><span class="sxs-lookup"><span data-stu-id="2828f-134">-RepositoryUrl</span></span>
<span data-ttu-id="2828f-135">SourceControl 리포지토리의 Url입니다.</span><span class="sxs-lookup"><span data-stu-id="2828f-135">Url of the SourceControl Repository.</span></span>

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

### <span data-ttu-id="2828f-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2828f-136">-ResourceGroupName</span></span>
<span data-ttu-id="2828f-137">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2828f-137">The name of the resource group.</span></span>

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

### <span data-ttu-id="2828f-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2828f-138">-SubscriptionId</span></span>
<span data-ttu-id="2828f-139">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2828f-139">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="2828f-140">-확인</span><span class="sxs-lookup"><span data-stu-id="2828f-140">-Confirm</span></span>
<span data-ttu-id="2828f-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2828f-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2828f-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2828f-142">-WhatIf</span></span>
<span data-ttu-id="2828f-143">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2828f-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2828f-144">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2828f-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2828f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2828f-145">CommonParameters</span></span>
<span data-ttu-id="2828f-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2828f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2828f-147">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2828f-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2828f-148">입력</span><span class="sxs-lookup"><span data-stu-id="2828f-148">INPUTS</span></span>

## <span data-ttu-id="2828f-149">출력</span><span class="sxs-lookup"><span data-stu-id="2828f-149">OUTPUTS</span></span>

### <span data-ttu-id="2828f-150">KubernetesConfiguration. Api20191101Preview. ISourceControlConfiguration에 대 한</span><span class="sxs-lookup"><span data-stu-id="2828f-150">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20191101Preview.ISourceControlConfiguration</span></span>

## <span data-ttu-id="2828f-151">상속자</span><span class="sxs-lookup"><span data-stu-id="2828f-151">NOTES</span></span>

<span data-ttu-id="2828f-152">별칭과</span><span class="sxs-lookup"><span data-stu-id="2828f-152">ALIASES</span></span>

## <span data-ttu-id="2828f-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2828f-153">RELATED LINKS</span></span>

