---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
ms.openlocfilehash: c7b33e3f2afd013b6fd54f6d425c0aa1d0d08bd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537364"
---
# <span data-ttu-id="5458b-101">Update-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="5458b-101">Update-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="5458b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5458b-102">SYNOPSIS</span></span>
<span data-ttu-id="5458b-103">가용성 집합을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5458b-103">Updates an availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5458b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5458b-104">SYNTAX</span></span>

### <span data-ttu-id="5458b-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="5458b-105">SkuParameterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5458b-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="5458b-106">ManagedParamterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5458b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="5458b-107">DESCRIPTION</span></span>
<span data-ttu-id="5458b-108">**업데이트 AzureRmAvailabilitySet** cmdlet은 가용성 집합을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5458b-108">The **Update-AzureRmAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="5458b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="5458b-109">EXAMPLES</span></span>

### <span data-ttu-id="5458b-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="5458b-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzureRmAvailabilitySet -Managed;
```

<span data-ttu-id="5458b-111">이 명령은 ' ResourceGroup01 ' 라는 리소스 그룹에서 ' AvSet01 ' 이라는 가용성 집합을 관리 되는 가용성 집합에 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5458b-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="5458b-112">변수</span><span class="sxs-lookup"><span data-stu-id="5458b-112">PARAMETERS</span></span>

### <span data-ttu-id="5458b-113">-AvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="5458b-113">-AvailabilitySet</span></span>
<span data-ttu-id="5458b-114">업데이트할 가용성 집합 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5458b-114">Specifies the availability set object to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5458b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5458b-115">-DefaultProfile</span></span>
<span data-ttu-id="5458b-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5458b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5458b-117">관리</span><span class="sxs-lookup"><span data-stu-id="5458b-117">-Managed</span></span>
<span data-ttu-id="5458b-118">관리 되는 가용성 집합</span><span class="sxs-lookup"><span data-stu-id="5458b-118">Managed Availability Set</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedParamterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5458b-119">-Sku</span><span class="sxs-lookup"><span data-stu-id="5458b-119">-Sku</span></span>
<span data-ttu-id="5458b-120">Sku 이름</span><span class="sxs-lookup"><span data-stu-id="5458b-120">The Name of Sku</span></span>

```yaml
Type: System.String
Parameter Sets: SkuParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5458b-121">-확인</span><span class="sxs-lookup"><span data-stu-id="5458b-121">-Confirm</span></span>
<span data-ttu-id="5458b-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5458b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5458b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5458b-123">-WhatIf</span></span>
<span data-ttu-id="5458b-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5458b-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5458b-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5458b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5458b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5458b-126">CommonParameters</span></span>
<span data-ttu-id="5458b-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5458b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5458b-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5458b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5458b-129">입력</span><span class="sxs-lookup"><span data-stu-id="5458b-129">INPUTS</span></span>

### <span data-ttu-id="5458b-130">PSAvailabilitySet를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="5458b-130">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="5458b-131">출력</span><span class="sxs-lookup"><span data-stu-id="5458b-131">OUTPUTS</span></span>

### <span data-ttu-id="5458b-132">PSAvailabilitySet를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="5458b-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="5458b-133">상속자</span><span class="sxs-lookup"><span data-stu-id="5458b-133">NOTES</span></span>

## <span data-ttu-id="5458b-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5458b-134">RELATED LINKS</span></span>

