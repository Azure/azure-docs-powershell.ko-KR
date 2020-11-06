---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 85b62b8ffbdcdcefff5bbb5c984a19ef0b7cb644
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93524160"
---
# <span data-ttu-id="3a15d-101">Remove-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="3a15d-101">Remove-AzsStorageQuota</span></span>

## <span data-ttu-id="3a15d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a15d-102">SYNOPSIS</span></span>
<span data-ttu-id="3a15d-103">기존 할당량 삭제</span><span class="sxs-lookup"><span data-stu-id="3a15d-103">Delete an existing quota</span></span>

## <span data-ttu-id="3a15d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3a15d-104">SYNTAX</span></span>

### <span data-ttu-id="3a15d-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="3a15d-105">Delete (Default)</span></span>
```
Remove-AzsStorageQuota -Name <String> [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a15d-106">리소스</span><span class="sxs-lookup"><span data-stu-id="3a15d-106">ResourceId</span></span>
```
Remove-AzsStorageQuota -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a15d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3a15d-107">DESCRIPTION</span></span>
<span data-ttu-id="3a15d-108">기존 할당량 삭제</span><span class="sxs-lookup"><span data-stu-id="3a15d-108">Delete an existing quota</span></span>

## <span data-ttu-id="3a15d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="3a15d-109">EXAMPLES</span></span>

### <span data-ttu-id="3a15d-110">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3a15d-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsStorageQuota -Name 'TestDeleteStorageQuota'
```

<span data-ttu-id="3a15d-111">이름으로 저장소 할당량을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a15d-111">Remove a storage quota by name.</span></span>

### <span data-ttu-id="3a15d-112">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="3a15d-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageQuota -Name 'testquota' | Remove-AzsStorageQuota
```

<span data-ttu-id="3a15d-113">파이프에 따라 저장소 할당량을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a15d-113">Remove a storage quota by piping.</span></span>

## <span data-ttu-id="3a15d-114">변수</span><span class="sxs-lookup"><span data-stu-id="3a15d-114">PARAMETERS</span></span>

### <span data-ttu-id="3a15d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3a15d-115">-Force</span></span>
<span data-ttu-id="3a15d-116">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3a15d-116">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a15d-117">-위치</span><span class="sxs-lookup"><span data-stu-id="3a15d-117">-Location</span></span>
<span data-ttu-id="3a15d-118">리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="3a15d-118">Resource location.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a15d-119">-이름</span><span class="sxs-lookup"><span data-stu-id="3a15d-119">-Name</span></span>
<span data-ttu-id="3a15d-120">저장소 할당량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3a15d-120">The name of the storage quota.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a15d-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3a15d-121">-ResourceId</span></span>
<span data-ttu-id="3a15d-122">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="3a15d-122">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a15d-123">-확인</span><span class="sxs-lookup"><span data-stu-id="3a15d-123">-Confirm</span></span>
<span data-ttu-id="3a15d-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a15d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a15d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a15d-125">-WhatIf</span></span>
<span data-ttu-id="3a15d-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3a15d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a15d-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3a15d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a15d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a15d-128">CommonParameters</span></span>
<span data-ttu-id="3a15d-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a15d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a15d-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a15d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a15d-131">입력</span><span class="sxs-lookup"><span data-stu-id="3a15d-131">INPUTS</span></span>

## <span data-ttu-id="3a15d-132">출력</span><span class="sxs-lookup"><span data-stu-id="3a15d-132">OUTPUTS</span></span>

## <span data-ttu-id="3a15d-133">상속자</span><span class="sxs-lookup"><span data-stu-id="3a15d-133">NOTES</span></span>

## <span data-ttu-id="3a15d-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3a15d-134">RELATED LINKS</span></span>

