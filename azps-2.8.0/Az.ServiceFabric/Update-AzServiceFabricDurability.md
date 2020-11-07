---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
ms.openlocfilehash: 283ca228ba44d2ec87cd926d23e0217eb67434eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871494"
---
# <span data-ttu-id="67aa3-101">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="67aa3-101">Update-AzServiceFabricDurability</span></span>

## <span data-ttu-id="67aa3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67aa3-102">SYNOPSIS</span></span>
<span data-ttu-id="67aa3-103">클러스터의 노드 형식에 대 한 내구성 계층 또는 VmSku를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="67aa3-103">Update the durability tier or VmSku of a node type in the cluster.</span></span>

## <span data-ttu-id="67aa3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="67aa3-104">SYNTAX</span></span>

```
Update-AzServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67aa3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="67aa3-105">DESCRIPTION</span></span>
<span data-ttu-id="67aa3-106">**업데이트-AzServiceFabricDurability** 를 사용 하 여 클러스터의 영속성 또는 SKU를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="67aa3-106">Use **Update-AzServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="67aa3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="67aa3-107">EXAMPLES</span></span>

### <span data-ttu-id="67aa3-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="67aa3-108">Example 1</span></span>
```
PS c:> Update-AzServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="67aa3-109">이 명령은 NodeType ' nt1 '의 영속성 계층을 은색으로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="67aa3-109">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="67aa3-110">변수</span><span class="sxs-lookup"><span data-stu-id="67aa3-110">PARAMETERS</span></span>

### <span data-ttu-id="67aa3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67aa3-111">-DefaultProfile</span></span>
<span data-ttu-id="67aa3-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="67aa3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67aa3-113">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="67aa3-113">-DurabilityLevel</span></span>
<span data-ttu-id="67aa3-114">내구성 수준을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67aa3-114">Specify durability level.</span></span>

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

### <span data-ttu-id="67aa3-115">-이름</span><span class="sxs-lookup"><span data-stu-id="67aa3-115">-Name</span></span>
<span data-ttu-id="67aa3-116">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67aa3-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="67aa3-117">-NodeType</span><span class="sxs-lookup"><span data-stu-id="67aa3-117">-NodeType</span></span>
<span data-ttu-id="67aa3-118">서비스 패브릭 노드 형식 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67aa3-118">Specify Service Fabric node type name.</span></span>

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

### <span data-ttu-id="67aa3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67aa3-119">-ResourceGroupName</span></span>
<span data-ttu-id="67aa3-120">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67aa3-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="67aa3-121">-Sku</span><span class="sxs-lookup"><span data-stu-id="67aa3-121">-Sku</span></span>
<span data-ttu-id="67aa3-122">노드 형식의 SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67aa3-122">Specify the SKU of the node type.</span></span>

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

### <span data-ttu-id="67aa3-123">-확인</span><span class="sxs-lookup"><span data-stu-id="67aa3-123">-Confirm</span></span>
<span data-ttu-id="67aa3-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="67aa3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67aa3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67aa3-125">-WhatIf</span></span>
<span data-ttu-id="67aa3-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="67aa3-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="67aa3-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="67aa3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67aa3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67aa3-128">CommonParameters</span></span>
<span data-ttu-id="67aa3-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="67aa3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67aa3-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67aa3-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67aa3-131">입력</span><span class="sxs-lookup"><span data-stu-id="67aa3-131">INPUTS</span></span>

### <span data-ttu-id="67aa3-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="67aa3-132">System.String</span></span>

### <span data-ttu-id="67aa3-133">ServiceFabric. DurabilityLevel/.</span><span class="sxs-lookup"><span data-stu-id="67aa3-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="67aa3-134">출력</span><span class="sxs-lookup"><span data-stu-id="67aa3-134">OUTPUTS</span></span>

### <span data-ttu-id="67aa3-135">ServiceFabric 클러스터의 모든.</span><span class="sxs-lookup"><span data-stu-id="67aa3-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="67aa3-136">상속자</span><span class="sxs-lookup"><span data-stu-id="67aa3-136">NOTES</span></span>

## <span data-ttu-id="67aa3-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="67aa3-137">RELATED LINKS</span></span>
