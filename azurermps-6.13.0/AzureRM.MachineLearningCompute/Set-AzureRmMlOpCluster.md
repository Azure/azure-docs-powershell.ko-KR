---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/set-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Set-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Set-AzureRmMlOpCluster.md
ms.openlocfilehash: cbe72d14eac4864b784f31c4a800db09fc38b042
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530235"
---
# <span data-ttu-id="617a8-101">Set-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="617a8-101">Set-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="617a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="617a8-102">SYNOPSIS</span></span>
<span data-ttu-id="617a8-103">Operationalization 클러스터의 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="617a8-103">Sets the properties of an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="617a8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="617a8-104">SYNTAX</span></span>

### <span data-ttu-id="617a8-105">SetByIndividualParameters (기본값)</span><span class="sxs-lookup"><span data-stu-id="617a8-105">SetByIndividualParameters (Default)</span></span>
```
Set-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="617a8-106">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="617a8-106">SetByInputObject</span></span>
```
Set-AzureRmMlOpCluster -InputObject <PSOperationalizationCluster> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="617a8-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="617a8-107">SetByResourceId</span></span>
```
Set-AzureRmMlOpCluster -ResourceId <String> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="617a8-108">설명은</span><span class="sxs-lookup"><span data-stu-id="617a8-108">DESCRIPTION</span></span>
<span data-ttu-id="617a8-109">Operationalization 클러스터의 모든 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="617a8-109">Sets all the properties of an operationalization cluster.</span></span> <span data-ttu-id="617a8-110">클러스터 개체를 사용할 때 모든 속성이 설정 되므로 완전히 유효한 입력 개체를 전달 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="617a8-110">Since it sets all the properties when using a cluster object a fully valid input object must be passed.</span></span> <span data-ttu-id="617a8-111">읽기 전용 속성은 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="617a8-111">Read-only properties will be ignored.</span></span> <span data-ttu-id="617a8-112">매개 변수 집합에 표시 되는 것 처럼 일부 속성만 현재 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="617a8-112">Only some properties are currently updatable, as shown in the parameter sets.</span></span>

## <span data-ttu-id="617a8-113">예제의</span><span class="sxs-lookup"><span data-stu-id="617a8-113">EXAMPLES</span></span>

### <span data-ttu-id="617a8-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="617a8-114">Example 1</span></span>
<span data-ttu-id="617a8-115">개별 매개 변수를 사용 하 여 클러스터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="617a8-115">Update a cluster using individual parameters.</span></span>

```
PS C:\> Set-AzureRmMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster -AgentCount 5
```

### <span data-ttu-id="617a8-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="617a8-116">Example 2</span></span>
<span data-ttu-id="617a8-117">입력 개체를 사용 하 여 클러스터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="617a8-117">Update a cluster using an input object.</span></span>

```
PS C:\> $cluster = Get-AzureRmMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster
PS C:\> $cluster.ContainerService.AgentCount = 5
PS C:\> Set-AzureRmMlOpCluster -InputObject $cluster
```

## <span data-ttu-id="617a8-118">변수</span><span class="sxs-lookup"><span data-stu-id="617a8-118">PARAMETERS</span></span>

### <span data-ttu-id="617a8-119">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="617a8-119">-AgentCount</span></span>
<span data-ttu-id="617a8-120">ACS 클러스터의 에이전트 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="617a8-120">The number of agent nodes in the ACS cluster.</span></span>

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

### <span data-ttu-id="617a8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="617a8-121">-DefaultProfile</span></span>
<span data-ttu-id="617a8-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="617a8-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="617a8-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="617a8-123">-InputObject</span></span>
<span data-ttu-id="617a8-124">Operationalization 클러스터 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="617a8-124">The operationalization cluster properties.</span></span>

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

### <span data-ttu-id="617a8-125">-이름</span><span class="sxs-lookup"><span data-stu-id="617a8-125">-Name</span></span>
<span data-ttu-id="617a8-126">Operationalization 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="617a8-126">The name of the operationalization cluster.</span></span>

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

### <span data-ttu-id="617a8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="617a8-127">-ResourceGroupName</span></span>
<span data-ttu-id="617a8-128">Operationalization 클러스터에 대 한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="617a8-128">The name of the resource group for the operationalization cluster.</span></span>

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

### <span data-ttu-id="617a8-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="617a8-129">-ResourceId</span></span>
<span data-ttu-id="617a8-130">Operationalization 클러스터에 대 한 Azure 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="617a8-130">The Azure resource id for the operationalization cluster.</span></span>

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

### <span data-ttu-id="617a8-131">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="617a8-131">-SslCertificate</span></span>
<span data-ttu-id="617a8-132">PEM 형식의 SSL 인증서 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="617a8-132">The SSL certificate data in PEM format.</span></span>

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

### <span data-ttu-id="617a8-133">-SslCName</span><span class="sxs-lookup"><span data-stu-id="617a8-133">-SslCName</span></span>
<span data-ttu-id="617a8-134">SSL 인증서에 대 한 CName</span><span class="sxs-lookup"><span data-stu-id="617a8-134">The CName for the SSL certificate.</span></span>

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

### <span data-ttu-id="617a8-135">-SslKey</span><span class="sxs-lookup"><span data-stu-id="617a8-135">-SslKey</span></span>
<span data-ttu-id="617a8-136">PEM 형식의 SSL 키 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="617a8-136">The SSL key data in PEM format.</span></span>

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

### <span data-ttu-id="617a8-137">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="617a8-137">-SslStatus</span></span>
<span data-ttu-id="617a8-138">SSL 상태</span><span class="sxs-lookup"><span data-stu-id="617a8-138">SSL status.</span></span>
<span data-ttu-id="617a8-139">가능한 값은 ' 사용 ' 및 ' 사용 안 함 '입니다.</span><span class="sxs-lookup"><span data-stu-id="617a8-139">Possible values are 'Enabled' and 'Disabled'.</span></span>

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

### <span data-ttu-id="617a8-140">-확인</span><span class="sxs-lookup"><span data-stu-id="617a8-140">-Confirm</span></span>
<span data-ttu-id="617a8-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="617a8-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="617a8-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="617a8-142">-WhatIf</span></span>
<span data-ttu-id="617a8-143">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="617a8-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="617a8-144">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="617a8-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="617a8-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="617a8-145">CommonParameters</span></span>
<span data-ttu-id="617a8-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="617a8-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="617a8-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="617a8-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="617a8-148">입력</span><span class="sxs-lookup"><span data-stu-id="617a8-148">INPUTS</span></span>

### <span data-ttu-id="617a8-149">MachineLearningCompute. PSOperationalizationCluster/.</span><span class="sxs-lookup"><span data-stu-id="617a8-149">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
<span data-ttu-id="617a8-150">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="617a8-150">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="617a8-151">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="617a8-151">System.String</span></span>

### <span data-ttu-id="617a8-152">시스템 Null 허용 ' 1 [[b77a5c561934e089, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="617a8-152">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="617a8-153">출력</span><span class="sxs-lookup"><span data-stu-id="617a8-153">OUTPUTS</span></span>

### <span data-ttu-id="617a8-154">MachineLearningCompute. PSOperationalizationCluster/.</span><span class="sxs-lookup"><span data-stu-id="617a8-154">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="617a8-155">상속자</span><span class="sxs-lookup"><span data-stu-id="617a8-155">NOTES</span></span>

## <span data-ttu-id="617a8-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="617a8-156">RELATED LINKS</span></span>
