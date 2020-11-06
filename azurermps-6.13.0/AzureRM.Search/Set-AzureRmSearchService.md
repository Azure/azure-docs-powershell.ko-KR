---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/set-azurermsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Set-AzureRmSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Set-AzureRmSearchService.md
ms.openlocfilehash: c938dd611d9f6d731c07d5aee76cb390838f4679
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529392"
---
# <span data-ttu-id="abebf-101">Set-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="abebf-101">Set-AzureRmSearchService</span></span>

## <span data-ttu-id="abebf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abebf-102">SYNOPSIS</span></span>
<span data-ttu-id="abebf-103">Azure Search 서비스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="abebf-103">Update an Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abebf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="abebf-104">SYNTAX</span></span>

### <span data-ttu-id="abebf-105">ResourceNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="abebf-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzureRmSearchService [-ResourceGroupName] <String> [-Name] <String> [-PartitionCount <Int32>]
 [-ReplicaCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abebf-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="abebf-106">InputObjectParameterSet</span></span>
```
Set-AzureRmSearchService [-InputObject] <PSSearchService> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abebf-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="abebf-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmSearchService [-ResourceId] <String> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abebf-108">설명은</span><span class="sxs-lookup"><span data-stu-id="abebf-108">DESCRIPTION</span></span>
<span data-ttu-id="abebf-109">**Set-AzureRmSearchService** Cmdlet은 Azure Search 서비스를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="abebf-109">The **Set-AzureRmSearchService** cmdlet modifies an Azure Search service.</span></span>

## <span data-ttu-id="abebf-110">예제의</span><span class="sxs-lookup"><span data-stu-id="abebf-110">EXAMPLES</span></span>

### <span data-ttu-id="abebf-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="abebf-111">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -PartitionCount 2 -ReplicaCount 2


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

<span data-ttu-id="abebf-112">이 예제에서는 Azure Search 서비스의 파티션 개수 및 복제본 개수를 2로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="abebf-112">The example changes partition count and replica count of the Azure Search service to 2.</span></span>

## <span data-ttu-id="abebf-113">변수</span><span class="sxs-lookup"><span data-stu-id="abebf-113">PARAMETERS</span></span>

### <span data-ttu-id="abebf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abebf-114">-DefaultProfile</span></span>
<span data-ttu-id="abebf-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="abebf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abebf-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="abebf-116">-InputObject</span></span>
<span data-ttu-id="abebf-117">검색 서비스 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="abebf-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="abebf-118">-이름</span><span class="sxs-lookup"><span data-stu-id="abebf-118">-Name</span></span>
<span data-ttu-id="abebf-119">검색 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="abebf-119">Search Service name.</span></span>

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

### <span data-ttu-id="abebf-120">-파티션 수</span><span class="sxs-lookup"><span data-stu-id="abebf-120">-PartitionCount</span></span>
<span data-ttu-id="abebf-121">검색 서비스 파티션 수입니다.</span><span class="sxs-lookup"><span data-stu-id="abebf-121">Search Service partition count.</span></span>

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

### <span data-ttu-id="abebf-122">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="abebf-122">-ReplicaCount</span></span>
<span data-ttu-id="abebf-123">검색 서비스 복제본 수입니다.</span><span class="sxs-lookup"><span data-stu-id="abebf-123">Search Service replica count.</span></span>

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

### <span data-ttu-id="abebf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abebf-124">-ResourceGroupName</span></span>
<span data-ttu-id="abebf-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="abebf-125">Resource Group name.</span></span>

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

### <span data-ttu-id="abebf-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="abebf-126">-ResourceId</span></span>
<span data-ttu-id="abebf-127">검색 서비스 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="abebf-127">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="abebf-128">-확인</span><span class="sxs-lookup"><span data-stu-id="abebf-128">-Confirm</span></span>
<span data-ttu-id="abebf-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="abebf-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abebf-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abebf-130">-WhatIf</span></span>
<span data-ttu-id="abebf-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="abebf-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="abebf-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="abebf-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abebf-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abebf-133">CommonParameters</span></span>
<span data-ttu-id="abebf-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="abebf-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abebf-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abebf-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abebf-136">입력</span><span class="sxs-lookup"><span data-stu-id="abebf-136">INPUTS</span></span>

### <span data-ttu-id="abebf-137">Microsoft. Azure. PSSearchService를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="abebf-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="abebf-138">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="abebf-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="abebf-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="abebf-139">System.String</span></span>

## <span data-ttu-id="abebf-140">출력</span><span class="sxs-lookup"><span data-stu-id="abebf-140">OUTPUTS</span></span>

### <span data-ttu-id="abebf-141">Microsoft. Azure. PSSearchService를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="abebf-141">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="abebf-142">상속자</span><span class="sxs-lookup"><span data-stu-id="abebf-142">NOTES</span></span>

## <span data-ttu-id="abebf-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="abebf-143">RELATED LINKS</span></span>

[<span data-ttu-id="abebf-144">새로운 AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="abebf-144">New-AzureRmSearchService</span></span>](./New-AzureRmSearchService.md)

[<span data-ttu-id="abebf-145">Get-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="abebf-145">Get-AzureRmSearchService</span></span>](./Get-AzureRmSearchService.md)

[<span data-ttu-id="abebf-146">제거-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="abebf-146">Remove-AzureRmSearchService</span></span>](./Remove-AzureRmSearchService.md)
