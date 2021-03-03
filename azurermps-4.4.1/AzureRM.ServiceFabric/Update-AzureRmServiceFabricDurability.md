---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
ms.openlocfilehash: b056e5328c24270df6a95e33b079e7b907f29fa3
ms.sourcegitcommit: 608289d079b819df2b8d1a2f7935cc500367a312
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/03/2021
ms.locfileid: "101685026"
---
# <span data-ttu-id="8df88-101">Update-AzureRmServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="8df88-101">Update-AzureRmServiceFabricDurability</span></span>

## <span data-ttu-id="8df88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8df88-102">SYNOPSIS</span></span>
<span data-ttu-id="8df88-103">클러스터의 노드 형식의 내구성 계층 또는 VmSku를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8df88-103">Update the durability tier or VmSku of a node type in the cluster.</span></span> <span data-ttu-id="8df88-104">또한 연결된 Virtual Machine Scale Set의 Service Fabric VM 확장의 내구성 계층도 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="8df88-104">It will also update the durability tier in the Service Fabric VM extension on the associated Virtual Machine Scale Set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8df88-105">구문</span><span class="sxs-lookup"><span data-stu-id="8df88-105">SYNTAX</span></span>

```
Update-AzureRmServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8df88-106">설명</span><span class="sxs-lookup"><span data-stu-id="8df88-106">DESCRIPTION</span></span>
<span data-ttu-id="8df88-107">**Update-AzureRmServiceFabricDurability를** 사용하여 클러스터의 내구성 또는 SKU를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8df88-107">Use **Update-AzureRmServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="8df88-108">예제</span><span class="sxs-lookup"><span data-stu-id="8df88-108">EXAMPLES</span></span>

### <span data-ttu-id="8df88-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="8df88-109">Example 1</span></span>
```
PS c:> Update-AzureRmServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="8df88-110">이 명령은 NodeType 'nt1'의 내구성 계층을 실버로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="8df88-110">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="8df88-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8df88-111">PARAMETERS</span></span>

### <span data-ttu-id="8df88-112">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="8df88-112">-DurabilityLevel</span></span>
<span data-ttu-id="8df88-113">내구성 수준을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8df88-113">Specify durability level.</span></span>

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

### <span data-ttu-id="8df88-114">-Name</span><span class="sxs-lookup"><span data-stu-id="8df88-114">-Name</span></span>
<span data-ttu-id="8df88-115">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8df88-115">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="8df88-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="8df88-116">-NodeType</span></span>
<span data-ttu-id="8df88-117">Service Fabric 노드 형식 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8df88-117">Specify Service Fabric node type name.</span></span>

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

### <span data-ttu-id="8df88-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8df88-118">-ResourceGroupName</span></span>
<span data-ttu-id="8df88-119">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8df88-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="8df88-120">-Sku</span><span class="sxs-lookup"><span data-stu-id="8df88-120">-Sku</span></span>
<span data-ttu-id="8df88-121">노드 형식의 SKU를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8df88-121">Specify the SKU of the node type.</span></span>

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

### <span data-ttu-id="8df88-122">-확인</span><span class="sxs-lookup"><span data-stu-id="8df88-122">-Confirm</span></span>
<span data-ttu-id="8df88-123">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8df88-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8df88-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8df88-124">-WhatIf</span></span>
<span data-ttu-id="8df88-125">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="8df88-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8df88-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8df88-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8df88-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8df88-127">-DefaultProfile</span></span>
<span data-ttu-id="8df88-128">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8df88-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8df88-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8df88-129">CommonParameters</span></span>
<span data-ttu-id="8df88-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8df88-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8df88-131">자세한 내용은 about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8df88-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8df88-132">입력</span><span class="sxs-lookup"><span data-stu-id="8df88-132">INPUTS</span></span>

### <span data-ttu-id="8df88-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="8df88-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>
<span data-ttu-id="8df88-134">System.String</span><span class="sxs-lookup"><span data-stu-id="8df88-134">System.String</span></span>

## <span data-ttu-id="8df88-135">출력</span><span class="sxs-lookup"><span data-stu-id="8df88-135">OUTPUTS</span></span>

### <span data-ttu-id="8df88-136">Microsoft.Azure.Commands.ServiceFabric.Models.psCluster</span><span class="sxs-lookup"><span data-stu-id="8df88-136">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="8df88-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8df88-137">NOTES</span></span>

## <span data-ttu-id="8df88-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8df88-138">RELATED LINKS</span></span>

