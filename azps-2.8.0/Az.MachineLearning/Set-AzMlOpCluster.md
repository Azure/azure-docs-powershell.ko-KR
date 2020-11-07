---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/set-azmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Set-AzMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Set-AzMlOpCluster.md
ms.openlocfilehash: 833b3456cd39e4589ceaf37e0c86fd654c250ddc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689419"
---
# <span data-ttu-id="976a5-101">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="976a5-101">Set-AzMlOpCluster</span></span>

## <span data-ttu-id="976a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="976a5-102">SYNOPSIS</span></span>
<span data-ttu-id="976a5-103">Operationalization 클러스터의 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="976a5-103">Sets the properties of an operationalization cluster.</span></span>

## <span data-ttu-id="976a5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="976a5-104">SYNTAX</span></span>

### <span data-ttu-id="976a5-105">SetByIndividualParameters (기본값)</span><span class="sxs-lookup"><span data-stu-id="976a5-105">SetByIndividualParameters (Default)</span></span>
```
Set-AzMlOpCluster -ResourceGroupName <String> -Name <String> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="976a5-106">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="976a5-106">SetByInputObject</span></span>
```
Set-AzMlOpCluster -InputObject <PSOperationalizationCluster> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="976a5-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="976a5-107">SetByResourceId</span></span>
```
Set-AzMlOpCluster -ResourceId <String> [-AgentCount <Int32>] [-SslStatus <String>] [-SslCertificate <String>]
 [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="976a5-108">설명은</span><span class="sxs-lookup"><span data-stu-id="976a5-108">DESCRIPTION</span></span>
<span data-ttu-id="976a5-109">Operationalization 클러스터의 모든 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="976a5-109">Sets all the properties of an operationalization cluster.</span></span> <span data-ttu-id="976a5-110">클러스터 개체를 사용할 때 모든 속성이 설정 되므로 완전히 유효한 입력 개체를 전달 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="976a5-110">Since it sets all the properties when using a cluster object a fully valid input object must be passed.</span></span> <span data-ttu-id="976a5-111">읽기 전용 속성은 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="976a5-111">Read-only properties will be ignored.</span></span> <span data-ttu-id="976a5-112">매개 변수 집합에 표시 되는 것 처럼 일부 속성만 현재 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="976a5-112">Only some properties are currently updatable, as shown in the parameter sets.</span></span>

## <span data-ttu-id="976a5-113">예제의</span><span class="sxs-lookup"><span data-stu-id="976a5-113">EXAMPLES</span></span>

### <span data-ttu-id="976a5-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="976a5-114">Example 1</span></span>
<span data-ttu-id="976a5-115">개별 매개 변수를 사용 하 여 클러스터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="976a5-115">Update a cluster using individual parameters.</span></span>

```
PS C:\> Set-AzMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster -AgentCount 5
```

### <span data-ttu-id="976a5-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="976a5-116">Example 2</span></span>
<span data-ttu-id="976a5-117">입력 개체를 사용 하 여 클러스터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="976a5-117">Update a cluster using an input object.</span></span>

```
PS C:\> $cluster = Get-AzMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster
PS C:\> $cluster.ContainerService.AgentCount = 5
PS C:\> Set-AzMlOpCluster -InputObject $cluster
```

## <span data-ttu-id="976a5-118">변수</span><span class="sxs-lookup"><span data-stu-id="976a5-118">PARAMETERS</span></span>

### <span data-ttu-id="976a5-119">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="976a5-119">-AgentCount</span></span>
<span data-ttu-id="976a5-120">ACS 클러스터의 에이전트 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="976a5-120">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="976a5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="976a5-121">-DefaultProfile</span></span>
<span data-ttu-id="976a5-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="976a5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="976a5-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="976a5-123">-InputObject</span></span>
<span data-ttu-id="976a5-124">Operationalization 클러스터 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="976a5-124">The operationalization cluster properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: SetByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="976a5-125">-이름</span><span class="sxs-lookup"><span data-stu-id="976a5-125">-Name</span></span>
<span data-ttu-id="976a5-126">Operationalization 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="976a5-126">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="976a5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="976a5-127">-ResourceGroupName</span></span>
<span data-ttu-id="976a5-128">Operationalization 클러스터에 대 한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="976a5-128">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="976a5-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="976a5-129">-ResourceId</span></span>
<span data-ttu-id="976a5-130">Operationalization 클러스터에 대 한 Azure 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="976a5-130">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="976a5-131">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="976a5-131">-SslCertificate</span></span>
<span data-ttu-id="976a5-132">PEM 형식의 SSL 인증서 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="976a5-132">The SSL certificate data in PEM format.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="976a5-133">-SslCName</span><span class="sxs-lookup"><span data-stu-id="976a5-133">-SslCName</span></span>
<span data-ttu-id="976a5-134">SSL 인증서에 대 한 CName</span><span class="sxs-lookup"><span data-stu-id="976a5-134">The CName for the SSL certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="976a5-135">-SslKey</span><span class="sxs-lookup"><span data-stu-id="976a5-135">-SslKey</span></span>
<span data-ttu-id="976a5-136">PEM 형식의 SSL 키 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="976a5-136">The SSL key data in PEM format.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="976a5-137">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="976a5-137">-SslStatus</span></span>
<span data-ttu-id="976a5-138">SSL 상태</span><span class="sxs-lookup"><span data-stu-id="976a5-138">SSL status.</span></span>
<span data-ttu-id="976a5-139">가능한 값은 ' 사용 ' 및 ' 사용 안 함 '입니다.</span><span class="sxs-lookup"><span data-stu-id="976a5-139">Possible values are 'Enabled' and 'Disabled'.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="976a5-140">-확인</span><span class="sxs-lookup"><span data-stu-id="976a5-140">-Confirm</span></span>
<span data-ttu-id="976a5-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="976a5-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="976a5-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="976a5-142">-WhatIf</span></span>
<span data-ttu-id="976a5-143">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="976a5-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="976a5-144">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="976a5-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="976a5-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="976a5-145">CommonParameters</span></span>
<span data-ttu-id="976a5-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="976a5-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="976a5-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="976a5-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="976a5-148">입력</span><span class="sxs-lookup"><span data-stu-id="976a5-148">INPUTS</span></span>

### <span data-ttu-id="976a5-149">MachineLearningCompute. PSOperationalizationCluster/.</span><span class="sxs-lookup"><span data-stu-id="976a5-149">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="976a5-150">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="976a5-150">System.String</span></span>

### <span data-ttu-id="976a5-151">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e])</span><span class="sxs-lookup"><span data-stu-id="976a5-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="976a5-152">출력</span><span class="sxs-lookup"><span data-stu-id="976a5-152">OUTPUTS</span></span>

### <span data-ttu-id="976a5-153">MachineLearningCompute. PSOperationalizationCluster/.</span><span class="sxs-lookup"><span data-stu-id="976a5-153">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="976a5-154">상속자</span><span class="sxs-lookup"><span data-stu-id="976a5-154">NOTES</span></span>

## <span data-ttu-id="976a5-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="976a5-155">RELATED LINKS</span></span>
