---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/update-azservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
ms.openlocfilehash: 40ac27339faf2915ccc88c3bbd5f0a39581af743
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955547"
---
# <span data-ttu-id="b831e-101">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="b831e-101">Update-AzServiceFabricDurability</span></span>

## <span data-ttu-id="b831e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b831e-102">SYNOPSIS</span></span>
<span data-ttu-id="b831e-103">클러스터의 노드 형식의 내구성 계층 또는 VmSku를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b831e-103">Update the durability tier or VmSku of a node type in the cluster.</span></span>

## <span data-ttu-id="b831e-104">구문</span><span class="sxs-lookup"><span data-stu-id="b831e-104">SYNTAX</span></span>

```
Update-AzServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b831e-105">설명</span><span class="sxs-lookup"><span data-stu-id="b831e-105">DESCRIPTION</span></span>
<span data-ttu-id="b831e-106">**Update-AzServiceFabricDurability를** 사용하여 클러스터의 내구성 또는 SKU를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b831e-106">Use **Update-AzServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="b831e-107">예제</span><span class="sxs-lookup"><span data-stu-id="b831e-107">EXAMPLES</span></span>

### <span data-ttu-id="b831e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b831e-108">Example 1</span></span>
```
PS c:> Update-AzServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="b831e-109">이 명령은 NodeType 'nt1'의 내구성 계층을 실버로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="b831e-109">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="b831e-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b831e-110">PARAMETERS</span></span>

### <span data-ttu-id="b831e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b831e-111">-DefaultProfile</span></span>
<span data-ttu-id="b831e-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b831e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b831e-113">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="b831e-113">-DurabilityLevel</span></span>
<span data-ttu-id="b831e-114">내구성 수준을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b831e-114">Specify durability level.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: Bronze, Silver, Gold

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b831e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b831e-115">-Name</span></span>
<span data-ttu-id="b831e-116">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b831e-116">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b831e-117">-NodeType</span><span class="sxs-lookup"><span data-stu-id="b831e-117">-NodeType</span></span>
<span data-ttu-id="b831e-118">Service Fabric 노드 형식 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b831e-118">Specify Service Fabric node type name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b831e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b831e-119">-ResourceGroupName</span></span>
<span data-ttu-id="b831e-120">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b831e-120">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b831e-121">-Sku</span><span class="sxs-lookup"><span data-stu-id="b831e-121">-Sku</span></span>
<span data-ttu-id="b831e-122">노드 형식의 SKU를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b831e-122">Specify the SKU of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b831e-123">-확인</span><span class="sxs-lookup"><span data-stu-id="b831e-123">-Confirm</span></span>
<span data-ttu-id="b831e-124">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b831e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b831e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b831e-125">-WhatIf</span></span>
<span data-ttu-id="b831e-126">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="b831e-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b831e-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b831e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b831e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b831e-128">CommonParameters</span></span>
<span data-ttu-id="b831e-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b831e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b831e-130">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b831e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b831e-131">입력</span><span class="sxs-lookup"><span data-stu-id="b831e-131">INPUTS</span></span>

### <span data-ttu-id="b831e-132">System.String</span><span class="sxs-lookup"><span data-stu-id="b831e-132">System.String</span></span>

### <span data-ttu-id="b831e-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="b831e-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="b831e-134">출력</span><span class="sxs-lookup"><span data-stu-id="b831e-134">OUTPUTS</span></span>

### <span data-ttu-id="b831e-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="b831e-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="b831e-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b831e-136">NOTES</span></span>

## <span data-ttu-id="b831e-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b831e-137">RELATED LINKS</span></span>
