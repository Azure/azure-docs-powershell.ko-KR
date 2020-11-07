---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzAvailabilitySet.md
ms.openlocfilehash: e8bd36cd9c054d155dca034f49be8cd422a244bc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875984"
---
# <span data-ttu-id="e0335-101">Update-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e0335-101">Update-AzAvailabilitySet</span></span>

## <span data-ttu-id="e0335-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0335-102">SYNOPSIS</span></span>
<span data-ttu-id="e0335-103">가용성 집합을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0335-103">Updates an availability set.</span></span>

## <span data-ttu-id="e0335-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e0335-104">SYNTAX</span></span>

### <span data-ttu-id="e0335-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0335-105">SkuParameterSet</span></span>
```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0335-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="e0335-106">ManagedParamterSet</span></span>
```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0335-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e0335-107">DESCRIPTION</span></span>
<span data-ttu-id="e0335-108">**업데이트 AzAvailabilitySet** cmdlet은 가용성 집합을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0335-108">The **Update-AzAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="e0335-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e0335-109">EXAMPLES</span></span>

### <span data-ttu-id="e0335-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="e0335-110">Example 1</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzAvailabilitySet -Managed;
```

<span data-ttu-id="e0335-111">이 명령은 ' ResourceGroup01 ' 라는 리소스 그룹에서 ' AvSet01 ' 이라는 가용성 집합을 관리 되는 가용성 집합에 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0335-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="e0335-112">변수</span><span class="sxs-lookup"><span data-stu-id="e0335-112">PARAMETERS</span></span>

### <span data-ttu-id="e0335-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e0335-113">-AsJob</span></span>
<span data-ttu-id="e0335-114">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0335-114">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0335-115">-AvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e0335-115">-AvailabilitySet</span></span>
<span data-ttu-id="e0335-116">업데이트할 가용성 집합 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0335-116">Specifies the availability set object to be updated.</span></span>

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

### <span data-ttu-id="e0335-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0335-117">-DefaultProfile</span></span>
<span data-ttu-id="e0335-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e0335-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0335-119">관리</span><span class="sxs-lookup"><span data-stu-id="e0335-119">-Managed</span></span>
<span data-ttu-id="e0335-120">관리 되는 가용성 집합</span><span class="sxs-lookup"><span data-stu-id="e0335-120">Managed Availability Set</span></span>

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

### <span data-ttu-id="e0335-121">-Sku</span><span class="sxs-lookup"><span data-stu-id="e0335-121">-Sku</span></span>
<span data-ttu-id="e0335-122">Sku 이름</span><span class="sxs-lookup"><span data-stu-id="e0335-122">The Name of Sku</span></span>

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

### <span data-ttu-id="e0335-123">-확인</span><span class="sxs-lookup"><span data-stu-id="e0335-123">-Confirm</span></span>
<span data-ttu-id="e0335-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0335-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0335-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0335-125">-WhatIf</span></span>
<span data-ttu-id="e0335-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e0335-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0335-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e0335-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0335-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0335-128">CommonParameters</span></span>
<span data-ttu-id="e0335-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0335-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0335-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0335-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0335-131">입력</span><span class="sxs-lookup"><span data-stu-id="e0335-131">INPUTS</span></span>

### <span data-ttu-id="e0335-132">PSAvailabilitySet를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0335-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="e0335-133">출력</span><span class="sxs-lookup"><span data-stu-id="e0335-133">OUTPUTS</span></span>

### <span data-ttu-id="e0335-134">PSAvailabilitySet를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0335-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="e0335-135">상속자</span><span class="sxs-lookup"><span data-stu-id="e0335-135">NOTES</span></span>

## <span data-ttu-id="e0335-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e0335-136">RELATED LINKS</span></span>

