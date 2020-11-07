---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 143f368b73aac490242e42f21ed76ee76ab012dc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701812"
---
# <span data-ttu-id="0f89c-101">New-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="0f89c-101">New-AzsStorageQuota</span></span>

## <span data-ttu-id="0f89c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f89c-102">SYNOPSIS</span></span>
<span data-ttu-id="0f89c-103">새 저장소 할당량을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0f89c-103">Create a new storage quota.</span></span>

## <span data-ttu-id="0f89c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0f89c-104">SYNTAX</span></span>

```
New-AzsStorageQuota [-Name] <String> [[-CapacityInGb] <Int32>] [[-NumberOfStorageAccounts] <Int32>]
 [[-Location] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f89c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0f89c-105">DESCRIPTION</span></span>
<span data-ttu-id="0f89c-106">새 저장소 할당량을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0f89c-106">Create a new storage quota.</span></span>

## <span data-ttu-id="0f89c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0f89c-107">EXAMPLES</span></span>

### <span data-ttu-id="0f89c-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0f89c-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsStorageQuota -CapacityInGb 1000 -NumberOfStorageAccounts 100 -Name 'TestCreateStorageQuota'
```

<span data-ttu-id="0f89c-109">지정 된 값을 사용 하 여 새 저장소 할당량을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0f89c-109">Create a new storage quota with specified values.</span></span>

## <span data-ttu-id="0f89c-110">변수</span><span class="sxs-lookup"><span data-stu-id="0f89c-110">PARAMETERS</span></span>

### <span data-ttu-id="0f89c-111">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="0f89c-111">-CapacityInGb</span></span>
<span data-ttu-id="0f89c-112">Maxium 용량 (GB).</span><span class="sxs-lookup"><span data-stu-id="0f89c-112">Maxium capacity (GB).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: 500
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f89c-113">-위치</span><span class="sxs-lookup"><span data-stu-id="0f89c-113">-Location</span></span>
<span data-ttu-id="0f89c-114">리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="0f89c-114">Resource location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f89c-115">-이름</span><span class="sxs-lookup"><span data-stu-id="0f89c-115">-Name</span></span>
<span data-ttu-id="0f89c-116">저장소 할당량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0f89c-116">The name of the storage quota.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f89c-117">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="0f89c-117">-NumberOfStorageAccounts</span></span>
<span data-ttu-id="0f89c-118">총 저장소 계정 수입니다.</span><span class="sxs-lookup"><span data-stu-id="0f89c-118">Total number of storage accounts.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: 20
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f89c-119">-확인</span><span class="sxs-lookup"><span data-stu-id="0f89c-119">-Confirm</span></span>
<span data-ttu-id="0f89c-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f89c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f89c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f89c-121">-WhatIf</span></span>
<span data-ttu-id="0f89c-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0f89c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f89c-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0f89c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f89c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f89c-124">CommonParameters</span></span>
<span data-ttu-id="0f89c-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f89c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f89c-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f89c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f89c-127">입력</span><span class="sxs-lookup"><span data-stu-id="0f89c-127">INPUTS</span></span>

## <span data-ttu-id="0f89c-128">출력</span><span class="sxs-lookup"><span data-stu-id="0f89c-128">OUTPUTS</span></span>

### <span data-ttu-id="0f89c-129">StorageQuota. 관리자. m a 관리</span><span class="sxs-lookup"><span data-stu-id="0f89c-129">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="0f89c-130">상속자</span><span class="sxs-lookup"><span data-stu-id="0f89c-130">NOTES</span></span>

## <span data-ttu-id="0f89c-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0f89c-131">RELATED LINKS</span></span>

