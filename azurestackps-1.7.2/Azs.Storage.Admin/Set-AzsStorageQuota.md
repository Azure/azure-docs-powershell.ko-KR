---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2eec56d9fc157da994521a5b258cd28132344c52
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874199"
---
# <span data-ttu-id="c33ff-101">Set-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="c33ff-101">Set-AzsStorageQuota</span></span>

## <span data-ttu-id="c33ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c33ff-102">SYNOPSIS</span></span>
<span data-ttu-id="c33ff-103">기존 저장소 할당량을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c33ff-103">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="c33ff-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c33ff-104">SYNTAX</span></span>

### <span data-ttu-id="c33ff-105">업데이트 (기본값)</span><span class="sxs-lookup"><span data-stu-id="c33ff-105">Update (Default)</span></span>
```
Set-AzsStorageQuota -Name <String> [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>]
 [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c33ff-106">리소스</span><span class="sxs-lookup"><span data-stu-id="c33ff-106">ResourceId</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -ResourceId <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c33ff-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="c33ff-107">InputObject</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -InputObject <StorageQuota>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c33ff-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c33ff-108">DESCRIPTION</span></span>
<span data-ttu-id="c33ff-109">기존 저장소 할당량을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c33ff-109">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="c33ff-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c33ff-110">EXAMPLES</span></span>

### <span data-ttu-id="c33ff-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c33ff-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsStorageQuota -Name 'TestUpdateStorageQuota' -CapacityInGb 123 -NumberOfStorageAccounts 10
```

<span data-ttu-id="c33ff-112">기존 저장소 할당량을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c33ff-112">Update an existing storage quota.</span></span>

## <span data-ttu-id="c33ff-113">변수</span><span class="sxs-lookup"><span data-stu-id="c33ff-113">PARAMETERS</span></span>

### <span data-ttu-id="c33ff-114">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="c33ff-114">-CapacityInGb</span></span>
<span data-ttu-id="c33ff-115">Maxium 용량 (GB).</span><span class="sxs-lookup"><span data-stu-id="c33ff-115">Maxium capacity (GB).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c33ff-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c33ff-116">-InputObject</span></span>
<span data-ttu-id="c33ff-117">Posbbily가 AzsStorageQuota에서 반환 된 저장소 할당량을 수정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="c33ff-117">Posbbily modified storage quota returned by Get-AzsStorageQuota.</span></span>

```yaml
Type: StorageQuota
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c33ff-118">-위치</span><span class="sxs-lookup"><span data-stu-id="c33ff-118">-Location</span></span>
<span data-ttu-id="c33ff-119">리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="c33ff-119">Resource location.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c33ff-120">-이름</span><span class="sxs-lookup"><span data-stu-id="c33ff-120">-Name</span></span>
<span data-ttu-id="c33ff-121">저장소 할당량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c33ff-121">The name of the storage quota.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c33ff-122">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="c33ff-122">-NumberOfStorageAccounts</span></span>
<span data-ttu-id="c33ff-123">총 저장소 계정 수입니다.</span><span class="sxs-lookup"><span data-stu-id="c33ff-123">Total number of storage accounts.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c33ff-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c33ff-124">-ResourceId</span></span>
<span data-ttu-id="c33ff-125">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="c33ff-125">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c33ff-126">-확인</span><span class="sxs-lookup"><span data-stu-id="c33ff-126">-Confirm</span></span>
<span data-ttu-id="c33ff-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c33ff-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c33ff-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c33ff-128">-WhatIf</span></span>
<span data-ttu-id="c33ff-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c33ff-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c33ff-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c33ff-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c33ff-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c33ff-131">CommonParameters</span></span>
<span data-ttu-id="c33ff-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c33ff-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c33ff-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c33ff-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c33ff-134">입력</span><span class="sxs-lookup"><span data-stu-id="c33ff-134">INPUTS</span></span>

## <span data-ttu-id="c33ff-135">출력</span><span class="sxs-lookup"><span data-stu-id="c33ff-135">OUTPUTS</span></span>

### <span data-ttu-id="c33ff-136">StorageQuota. 관리자. m a 관리</span><span class="sxs-lookup"><span data-stu-id="c33ff-136">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="c33ff-137">상속자</span><span class="sxs-lookup"><span data-stu-id="c33ff-137">NOTES</span></span>

## <span data-ttu-id="c33ff-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c33ff-138">RELATED LINKS</span></span>

