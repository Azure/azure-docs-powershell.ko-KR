---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4cc08220a92dce5a49544cf958db79d7243b9ebb
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93875180"
---
# <span data-ttu-id="b1a89-101">New-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="b1a89-101">New-AzsStorageQuota</span></span>

## <span data-ttu-id="b1a89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1a89-102">SYNOPSIS</span></span>
<span data-ttu-id="b1a89-103">새 저장소 할당량을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b1a89-103">Create a new storage quota.</span></span>

## <span data-ttu-id="b1a89-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b1a89-104">SYNTAX</span></span>

```
New-AzsStorageQuota [-Name] <String> [[-CapacityInGb] <Int32>] [[-NumberOfStorageAccounts] <Int32>]
 [[-Location] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1a89-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b1a89-105">DESCRIPTION</span></span>
<span data-ttu-id="b1a89-106">새 저장소 할당량을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b1a89-106">Create a new storage quota.</span></span>

## <span data-ttu-id="b1a89-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b1a89-107">EXAMPLES</span></span>

### <span data-ttu-id="b1a89-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b1a89-108">EXAMPLE 1</span></span>
```
New-AzsStorageQuota -CapacityInGb 1000 -NumberOfStorageAccounts 100 -Name 'TestCreateStorageQuota'
```

<span data-ttu-id="b1a89-109">지정 된 값을 사용 하 여 새 저장소 할당량을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b1a89-109">Create a new storage quota with specified values.</span></span>

## <span data-ttu-id="b1a89-110">변수</span><span class="sxs-lookup"><span data-stu-id="b1a89-110">PARAMETERS</span></span>

### <span data-ttu-id="b1a89-111">-이름</span><span class="sxs-lookup"><span data-stu-id="b1a89-111">-Name</span></span>
<span data-ttu-id="b1a89-112">저장소 할당량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1a89-112">The name of the storage quota.</span></span>

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

### <span data-ttu-id="b1a89-113">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="b1a89-113">-CapacityInGb</span></span>
<span data-ttu-id="b1a89-114">Maxium 용량 (GB).</span><span class="sxs-lookup"><span data-stu-id="b1a89-114">Maxium capacity (GB).</span></span>

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

### <span data-ttu-id="b1a89-115">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="b1a89-115">-NumberOfStorageAccounts</span></span>
<span data-ttu-id="b1a89-116">총 저장소 계정 수입니다.</span><span class="sxs-lookup"><span data-stu-id="b1a89-116">Total number of storage accounts.</span></span>

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

### <span data-ttu-id="b1a89-117">-위치</span><span class="sxs-lookup"><span data-stu-id="b1a89-117">-Location</span></span>
<span data-ttu-id="b1a89-118">리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="b1a89-118">Resource location.</span></span>

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

### <span data-ttu-id="b1a89-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1a89-119">-WhatIf</span></span>
<span data-ttu-id="b1a89-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b1a89-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1a89-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b1a89-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1a89-122">-확인</span><span class="sxs-lookup"><span data-stu-id="b1a89-122">-Confirm</span></span>
<span data-ttu-id="b1a89-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1a89-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1a89-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1a89-124">CommonParameters</span></span>
<span data-ttu-id="b1a89-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1a89-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1a89-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1a89-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1a89-127">입력</span><span class="sxs-lookup"><span data-stu-id="b1a89-127">INPUTS</span></span>

## <span data-ttu-id="b1a89-128">출력</span><span class="sxs-lookup"><span data-stu-id="b1a89-128">OUTPUTS</span></span>

### <span data-ttu-id="b1a89-129">StorageQuota. 관리자. m a 관리</span><span class="sxs-lookup"><span data-stu-id="b1a89-129">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="b1a89-130">상속자</span><span class="sxs-lookup"><span data-stu-id="b1a89-130">NOTES</span></span>

## <span data-ttu-id="b1a89-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b1a89-131">RELATED LINKS</span></span>
