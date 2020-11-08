---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0983e05a36de72148571ccbbc7f1454343ad393a
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046634"
---
# <span data-ttu-id="a51b5-101">Remove-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="a51b5-101">Remove-AzsStorageQuota</span></span>

## <span data-ttu-id="a51b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a51b5-102">SYNOPSIS</span></span>
<span data-ttu-id="a51b5-103">기존 할당량 삭제</span><span class="sxs-lookup"><span data-stu-id="a51b5-103">Delete an existing quota</span></span>

## <span data-ttu-id="a51b5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a51b5-104">SYNTAX</span></span>

### <span data-ttu-id="a51b5-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="a51b5-105">Delete (Default)</span></span>
```
Remove-AzsStorageQuota -Name <String> [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a51b5-106">리소스</span><span class="sxs-lookup"><span data-stu-id="a51b5-106">ResourceId</span></span>
```
Remove-AzsStorageQuota -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a51b5-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a51b5-107">DESCRIPTION</span></span>
<span data-ttu-id="a51b5-108">기존 할당량 삭제</span><span class="sxs-lookup"><span data-stu-id="a51b5-108">Delete an existing quota</span></span>

## <span data-ttu-id="a51b5-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a51b5-109">EXAMPLES</span></span>

### <span data-ttu-id="a51b5-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="a51b5-110">EXAMPLE 1</span></span>
```
Remove-AzsStorageQuota -Name 'TestDeleteStorageQuota'
```

<span data-ttu-id="a51b5-111">이름으로 저장소 할당량을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a51b5-111">Remove a storage quota by name.</span></span>

### <span data-ttu-id="a51b5-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="a51b5-112">EXAMPLE 2</span></span>
```
Get-AzsStorageQuota -Name 'testquota' | Remove-AzsStorageQuota
```

<span data-ttu-id="a51b5-113">파이프에 따라 저장소 할당량을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a51b5-113">Remove a storage quota by piping.</span></span>

## <span data-ttu-id="a51b5-114">변수</span><span class="sxs-lookup"><span data-stu-id="a51b5-114">PARAMETERS</span></span>

### <span data-ttu-id="a51b5-115">-이름</span><span class="sxs-lookup"><span data-stu-id="a51b5-115">-Name</span></span>
<span data-ttu-id="a51b5-116">저장소 할당량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a51b5-116">The name of the storage quota.</span></span>

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

### <span data-ttu-id="a51b5-117">-위치</span><span class="sxs-lookup"><span data-stu-id="a51b5-117">-Location</span></span>
<span data-ttu-id="a51b5-118">리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="a51b5-118">Resource location.</span></span>

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

### <span data-ttu-id="a51b5-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a51b5-119">-ResourceId</span></span>
<span data-ttu-id="a51b5-120">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="a51b5-120">The resource id.</span></span>

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

### <span data-ttu-id="a51b5-121">-Force</span><span class="sxs-lookup"><span data-stu-id="a51b5-121">-Force</span></span>
<span data-ttu-id="a51b5-122">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a51b5-122">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="a51b5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a51b5-123">-WhatIf</span></span>
<span data-ttu-id="a51b5-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a51b5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a51b5-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a51b5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a51b5-126">-확인</span><span class="sxs-lookup"><span data-stu-id="a51b5-126">-Confirm</span></span>
<span data-ttu-id="a51b5-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a51b5-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a51b5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a51b5-128">CommonParameters</span></span>
<span data-ttu-id="a51b5-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a51b5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a51b5-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a51b5-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a51b5-131">입력</span><span class="sxs-lookup"><span data-stu-id="a51b5-131">INPUTS</span></span>

## <span data-ttu-id="a51b5-132">출력</span><span class="sxs-lookup"><span data-stu-id="a51b5-132">OUTPUTS</span></span>

## <span data-ttu-id="a51b5-133">상속자</span><span class="sxs-lookup"><span data-stu-id="a51b5-133">NOTES</span></span>

## <span data-ttu-id="a51b5-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a51b5-134">RELATED LINKS</span></span>
