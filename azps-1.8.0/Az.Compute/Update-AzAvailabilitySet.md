---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
ms.openlocfilehash: 4051cbb697625f527afdf2e189953c4d6e776214
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868842"
---
# <span data-ttu-id="7d688-101">Update-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="7d688-101">Update-AzAvailabilitySet</span></span>

## <span data-ttu-id="7d688-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d688-102">SYNOPSIS</span></span>
<span data-ttu-id="7d688-103">가용성 집합을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d688-103">Updates an availability set.</span></span>

## <span data-ttu-id="7d688-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7d688-104">SYNTAX</span></span>

### <span data-ttu-id="7d688-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d688-105">SkuParameterSet</span></span>
```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d688-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="7d688-106">ManagedParamterSet</span></span>
```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d688-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7d688-107">DESCRIPTION</span></span>
<span data-ttu-id="7d688-108">**업데이트 AzAvailabilitySet** cmdlet은 가용성 집합을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d688-108">The **Update-AzAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="7d688-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7d688-109">EXAMPLES</span></span>

### <span data-ttu-id="7d688-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="7d688-110">Example 1</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzAvailabilitySet -Managed;
```

<span data-ttu-id="7d688-111">이 명령은 ' ResourceGroup01 ' 라는 리소스 그룹에서 ' AvSet01 ' 이라는 가용성 집합을 관리 되는 가용성 집합에 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d688-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="7d688-112">변수</span><span class="sxs-lookup"><span data-stu-id="7d688-112">PARAMETERS</span></span>

### <span data-ttu-id="7d688-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7d688-113">-AsJob</span></span>
<span data-ttu-id="7d688-114">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d688-114">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d688-115">-AvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="7d688-115">-AvailabilitySet</span></span>
<span data-ttu-id="7d688-116">업데이트할 가용성 집합 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d688-116">Specifies the availability set object to be updated.</span></span>

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

### <span data-ttu-id="7d688-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d688-117">-DefaultProfile</span></span>
<span data-ttu-id="7d688-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7d688-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d688-119">관리</span><span class="sxs-lookup"><span data-stu-id="7d688-119">-Managed</span></span>
<span data-ttu-id="7d688-120">관리 되는 가용성 집합</span><span class="sxs-lookup"><span data-stu-id="7d688-120">Managed Availability Set</span></span>

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

### <span data-ttu-id="7d688-121">-Sku</span><span class="sxs-lookup"><span data-stu-id="7d688-121">-Sku</span></span>
<span data-ttu-id="7d688-122">Sku 이름</span><span class="sxs-lookup"><span data-stu-id="7d688-122">The Name of Sku</span></span>

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

### <span data-ttu-id="7d688-123">태그</span><span class="sxs-lookup"><span data-stu-id="7d688-123">-Tag</span></span>
<span data-ttu-id="7d688-124">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="7d688-124">Key-value pairs in the form of a hash table.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d688-125">-확인</span><span class="sxs-lookup"><span data-stu-id="7d688-125">-Confirm</span></span>
<span data-ttu-id="7d688-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d688-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d688-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d688-127">-WhatIf</span></span>
<span data-ttu-id="7d688-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7d688-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7d688-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7d688-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d688-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d688-130">CommonParameters</span></span>
<span data-ttu-id="7d688-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d688-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d688-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d688-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d688-133">입력</span><span class="sxs-lookup"><span data-stu-id="7d688-133">INPUTS</span></span>

### <span data-ttu-id="7d688-134">PSAvailabilitySet를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d688-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="7d688-135">출력</span><span class="sxs-lookup"><span data-stu-id="7d688-135">OUTPUTS</span></span>

### <span data-ttu-id="7d688-136">PSAvailabilitySet를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d688-136">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="7d688-137">상속자</span><span class="sxs-lookup"><span data-stu-id="7d688-137">NOTES</span></span>

## <span data-ttu-id="7d688-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7d688-138">RELATED LINKS</span></span>
