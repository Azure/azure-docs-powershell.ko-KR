---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/set-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
ms.openlocfilehash: e4329c0d3ad4499af1174458ea3e0449672774a5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218185"
---
# <span data-ttu-id="fdc03-101">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="fdc03-101">Set-AzSearchService</span></span>

## <span data-ttu-id="fdc03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdc03-102">SYNOPSIS</span></span>
<span data-ttu-id="fdc03-103">Azure Search 서비스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdc03-103">Update an Azure Search service.</span></span>

## <span data-ttu-id="fdc03-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fdc03-104">SYNTAX</span></span>

### <span data-ttu-id="fdc03-105">ResourceNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="fdc03-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-PartitionCount <Int32>]
 [-ReplicaCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdc03-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdc03-106">InputObjectParameterSet</span></span>
```
Set-AzSearchService [-InputObject] <PSSearchService> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdc03-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdc03-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchService [-ResourceId] <String> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdc03-108">설명은</span><span class="sxs-lookup"><span data-stu-id="fdc03-108">DESCRIPTION</span></span>
<span data-ttu-id="fdc03-109">**Set-AzSearchService** Cmdlet은 Azure Search 서비스를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdc03-109">The **Set-AzSearchService** cmdlet modifies an Azure Search service.</span></span>

## <span data-ttu-id="fdc03-110">예제의</span><span class="sxs-lookup"><span data-stu-id="fdc03-110">EXAMPLES</span></span>

### <span data-ttu-id="fdc03-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="fdc03-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -PartitionCount 2 -ReplicaCount 2


ResourceGroupName : TestAzureSearchPsGroup
Name              : pstestazuresearch01
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/TestAzureSearchPsGroup/providers/Microsoft.Search/searchServices/pstestazuresearch01
Location          : West US
Sku               : Standard
ReplicaCount      : 2
PartitionCount    : 2
HostingMode       : Default
Tags              :
```

<span data-ttu-id="fdc03-112">이 예제에서는 Azure Search 서비스의 파티션 개수 및 복제본 개수를 2로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdc03-112">The example changes partition count and replica count of the Azure Search service to 2.</span></span>

## <span data-ttu-id="fdc03-113">변수</span><span class="sxs-lookup"><span data-stu-id="fdc03-113">PARAMETERS</span></span>

### <span data-ttu-id="fdc03-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdc03-114">-DefaultProfile</span></span>
<span data-ttu-id="fdc03-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fdc03-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdc03-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fdc03-116">-InputObject</span></span>
<span data-ttu-id="fdc03-117">검색 서비스 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="fdc03-117">Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fdc03-118">-이름</span><span class="sxs-lookup"><span data-stu-id="fdc03-118">-Name</span></span>
<span data-ttu-id="fdc03-119">검색 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fdc03-119">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdc03-120">-파티션 수</span><span class="sxs-lookup"><span data-stu-id="fdc03-120">-PartitionCount</span></span>
<span data-ttu-id="fdc03-121">검색 서비스 파티션 수입니다.</span><span class="sxs-lookup"><span data-stu-id="fdc03-121">Search Service partition count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdc03-122">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="fdc03-122">-ReplicaCount</span></span>
<span data-ttu-id="fdc03-123">검색 서비스 복제본 수입니다.</span><span class="sxs-lookup"><span data-stu-id="fdc03-123">Search Service replica count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdc03-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdc03-124">-ResourceGroupName</span></span>
<span data-ttu-id="fdc03-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fdc03-125">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdc03-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fdc03-126">-ResourceId</span></span>
<span data-ttu-id="fdc03-127">검색 서비스 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="fdc03-127">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdc03-128">-확인</span><span class="sxs-lookup"><span data-stu-id="fdc03-128">-Confirm</span></span>
<span data-ttu-id="fdc03-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdc03-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdc03-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdc03-130">-WhatIf</span></span>
<span data-ttu-id="fdc03-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fdc03-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fdc03-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fdc03-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdc03-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdc03-133">CommonParameters</span></span>
<span data-ttu-id="fdc03-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdc03-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdc03-135">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdc03-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdc03-136">입력</span><span class="sxs-lookup"><span data-stu-id="fdc03-136">INPUTS</span></span>

### <span data-ttu-id="fdc03-137">Microsoft. Azure. PSSearchService를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdc03-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="fdc03-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fdc03-138">System.String</span></span>

## <span data-ttu-id="fdc03-139">출력</span><span class="sxs-lookup"><span data-stu-id="fdc03-139">OUTPUTS</span></span>

### <span data-ttu-id="fdc03-140">Microsoft. Azure. PSSearchService를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdc03-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="fdc03-141">상속자</span><span class="sxs-lookup"><span data-stu-id="fdc03-141">NOTES</span></span>

## <span data-ttu-id="fdc03-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fdc03-142">RELATED LINKS</span></span>

[<span data-ttu-id="fdc03-143">새로운 AzSearchService</span><span class="sxs-lookup"><span data-stu-id="fdc03-143">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="fdc03-144">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="fdc03-144">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="fdc03-145">제거-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="fdc03-145">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)