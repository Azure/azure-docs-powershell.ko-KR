---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/set-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Set-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Set-AzureRmMlOpCluster.md
ms.openlocfilehash: 142dd983b00b578f47e2c1f2eebcbd0686614430
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711419"
---
# <span data-ttu-id="b4740-101">Set-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="b4740-101">Set-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="b4740-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4740-102">SYNOPSIS</span></span>
<span data-ttu-id="b4740-103">Operationalization 클러스터의 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4740-103">Sets the properties of an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4740-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b4740-104">SYNTAX</span></span>

### <span data-ttu-id="b4740-105">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="b4740-105">SetByInputObject</span></span>
```
Set-AzureRmMlOpCluster -InputObject <PSOperationalizationCluster> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="b4740-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b4740-106">SetByResourceId</span></span>
```
Set-AzureRmMlOpCluster -ResourceId <String> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="b4740-107">SetByIndividualParameters</span><span class="sxs-lookup"><span data-stu-id="b4740-107">SetByIndividualParameters</span></span>
```
Set-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="b4740-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b4740-108">DESCRIPTION</span></span>
<span data-ttu-id="b4740-109">Operationalization 클러스터의 모든 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4740-109">Sets all the properties of an operationalization cluster.</span></span> <span data-ttu-id="b4740-110">클러스터 개체를 사용할 때 모든 속성이 설정 되므로 완전히 유효한 입력 개체를 전달 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4740-110">Since it sets all the properties when using a cluster object a fully valid input object must be passed.</span></span> <span data-ttu-id="b4740-111">읽기 전용 속성은 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b4740-111">Read-only properties will be ignored.</span></span> <span data-ttu-id="b4740-112">매개 변수 집합에 표시 되는 것 처럼 일부 속성만 현재 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b4740-112">Only some properties are currently updatable, as shown in the parameter sets.</span></span>

## <span data-ttu-id="b4740-113">예제의</span><span class="sxs-lookup"><span data-stu-id="b4740-113">EXAMPLES</span></span>

### <span data-ttu-id="b4740-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="b4740-114">Example 1</span></span>
<span data-ttu-id="b4740-115">개별 매개 변수를 사용 하 여 클러스터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4740-115">Update a cluster using individual parameters.</span></span>
```
PS C:\> Set-AzureRmMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster -AgentCount 5
```

### <span data-ttu-id="b4740-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="b4740-116">Example 2</span></span>
<span data-ttu-id="b4740-117">입력 개체를 사용 하 여 클러스터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4740-117">Update a cluster using an input object.</span></span>
```
PS C:\> $cluster = Get-AzureRmMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster
PS C:\> $cluster.ContainerService.AgentCount = 5
PS C:\> Set-AzureRmMlOpCluster -InputObject $cluster
```

## <span data-ttu-id="b4740-118">변수</span><span class="sxs-lookup"><span data-stu-id="b4740-118">PARAMETERS</span></span>

### <span data-ttu-id="b4740-119">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="b4740-119">-AgentCount</span></span>
<span data-ttu-id="b4740-120">ACS 클러스터의 에이전트 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="b4740-120">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByInputObject, SetByResourceId, SetByIndividualParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4740-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4740-121">-DefaultProfile</span></span>
<span data-ttu-id="b4740-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b4740-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4740-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4740-123">-InputObject</span></span>
<span data-ttu-id="b4740-124">Operationalization 클러스터 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="b4740-124">The operationalization cluster properties.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: SetByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4740-125">-이름</span><span class="sxs-lookup"><span data-stu-id="b4740-125">-Name</span></span>
<span data-ttu-id="b4740-126">Operationalization 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b4740-126">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: SetByIndividualParameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4740-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4740-127">-ResourceGroupName</span></span>
<span data-ttu-id="b4740-128">Operationalization 클러스터에 대 한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b4740-128">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: SetByIndividualParameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4740-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4740-129">-ResourceId</span></span>
<span data-ttu-id="b4740-130">Operationalization 클러스터에 대 한 Azure 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="b4740-130">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4740-131">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="b4740-131">-SslCertificate</span></span>
<span data-ttu-id="b4740-132">PEM 형식의 SSL 인증서 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="b4740-132">The SSL certificate data in PEM format.</span></span>

```yaml
Type: String
Parameter Sets: SetByInputObject, SetByResourceId, SetByIndividualParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4740-133">-SslCName</span><span class="sxs-lookup"><span data-stu-id="b4740-133">-SslCName</span></span>
<span data-ttu-id="b4740-134">SSL 인증서에 대 한 CName</span><span class="sxs-lookup"><span data-stu-id="b4740-134">The CName for the SSL certificate.</span></span>

```yaml
Type: String
Parameter Sets: SetByInputObject, SetByResourceId, SetByIndividualParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4740-135">-SslKey</span><span class="sxs-lookup"><span data-stu-id="b4740-135">-SslKey</span></span>
<span data-ttu-id="b4740-136">PEM 형식의 SSL 키 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="b4740-136">The SSL key data in PEM format.</span></span>

```yaml
Type: String
Parameter Sets: SetByInputObject, SetByResourceId, SetByIndividualParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4740-137">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="b4740-137">-SslStatus</span></span>
<span data-ttu-id="b4740-138">SSL 상태</span><span class="sxs-lookup"><span data-stu-id="b4740-138">SSL status.</span></span>
<span data-ttu-id="b4740-139">가능한 값은 ' 사용 ' 및 ' 사용 안 함 '입니다.</span><span class="sxs-lookup"><span data-stu-id="b4740-139">Possible values are 'Enabled' and 'Disabled'.</span></span>

```yaml
Type: String
Parameter Sets: SetByInputObject, SetByResourceId, SetByIndividualParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4740-140">-확인</span><span class="sxs-lookup"><span data-stu-id="b4740-140">-Confirm</span></span>
<span data-ttu-id="b4740-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4740-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4740-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4740-142">-WhatIf</span></span>
<span data-ttu-id="b4740-143">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b4740-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4740-144">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b4740-144">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="b4740-145">입력</span><span class="sxs-lookup"><span data-stu-id="b4740-145">INPUTS</span></span>

### <span data-ttu-id="b4740-146">MachineLearningCompute. PSOperationalizationCluster/.</span><span class="sxs-lookup"><span data-stu-id="b4740-146">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
### <span data-ttu-id="b4740-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b4740-147">System.String</span></span>
### <span data-ttu-id="b4740-148">시스템 Null 허용 ' 1 [[b77a5c561934e089, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="b4740-148">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>


## <span data-ttu-id="b4740-149">출력</span><span class="sxs-lookup"><span data-stu-id="b4740-149">OUTPUTS</span></span>

### <span data-ttu-id="b4740-150">MachineLearningCompute. PSOperationalizationCluster/.</span><span class="sxs-lookup"><span data-stu-id="b4740-150">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>


## <span data-ttu-id="b4740-151">상속자</span><span class="sxs-lookup"><span data-stu-id="b4740-151">NOTES</span></span>

## <span data-ttu-id="b4740-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b4740-152">RELATED LINKS</span></span>

