---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
ms.openlocfilehash: 7e460c866912387b05a55b6fd228c65ef9b68348
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525255"
---
# <span data-ttu-id="bf847-101">Update-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="bf847-101">Update-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="bf847-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf847-102">SYNOPSIS</span></span>
<span data-ttu-id="bf847-103">가용성 집합을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf847-103">Updates an availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf847-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bf847-104">SYNTAX</span></span>

### <span data-ttu-id="bf847-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf847-105">SkuParameterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bf847-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="bf847-106">ManagedParamterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bf847-107">설명은</span><span class="sxs-lookup"><span data-stu-id="bf847-107">DESCRIPTION</span></span>
<span data-ttu-id="bf847-108">**업데이트 AzureRmAvailabilitySet** cmdlet은 가용성 집합을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf847-108">The **Update-AzureRmAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="bf847-109">예제의</span><span class="sxs-lookup"><span data-stu-id="bf847-109">EXAMPLES</span></span>

### <span data-ttu-id="bf847-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="bf847-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzureRmAvailabilitySet -Managed;
```

<span data-ttu-id="bf847-111">이 명령은 ' ResourceGroup01 ' 라는 리소스 그룹에서 ' AvSet01 ' 이라는 가용성 집합을 관리 되는 가용성 집합에 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf847-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="bf847-112">변수</span><span class="sxs-lookup"><span data-stu-id="bf847-112">PARAMETERS</span></span>

### <span data-ttu-id="bf847-113">-AvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="bf847-113">-AvailabilitySet</span></span>
<span data-ttu-id="bf847-114">업데이트할 가용성 집합 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf847-114">Specifies the availability set object to be updated.</span></span>

```yaml
Type: PSAvailabilitySet
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf847-115">관리</span><span class="sxs-lookup"><span data-stu-id="bf847-115">-Managed</span></span>
<span data-ttu-id="bf847-116">관리 되는 가용성 집합</span><span class="sxs-lookup"><span data-stu-id="bf847-116">Managed Availability Set</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ManagedParamterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf847-117">-Sku</span><span class="sxs-lookup"><span data-stu-id="bf847-117">-Sku</span></span>
<span data-ttu-id="bf847-118">Sku 이름</span><span class="sxs-lookup"><span data-stu-id="bf847-118">The Name of Sku</span></span>

```yaml
Type: String
Parameter Sets: SkuParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf847-119">-확인</span><span class="sxs-lookup"><span data-stu-id="bf847-119">-Confirm</span></span>
<span data-ttu-id="bf847-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf847-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf847-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf847-121">-WhatIf</span></span>
<span data-ttu-id="bf847-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bf847-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bf847-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bf847-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf847-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf847-124">CommonParameters</span></span>
<span data-ttu-id="bf847-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf847-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf847-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf847-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf847-127">입력</span><span class="sxs-lookup"><span data-stu-id="bf847-127">INPUTS</span></span>

### <span data-ttu-id="bf847-128">PSAvailabilitySet를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf847-128">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="bf847-129">출력</span><span class="sxs-lookup"><span data-stu-id="bf847-129">OUTPUTS</span></span>

### <span data-ttu-id="bf847-130">PSAvailabilitySet를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf847-130">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="bf847-131">상속자</span><span class="sxs-lookup"><span data-stu-id="bf847-131">NOTES</span></span>

## <span data-ttu-id="bf847-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bf847-132">RELATED LINKS</span></span>

