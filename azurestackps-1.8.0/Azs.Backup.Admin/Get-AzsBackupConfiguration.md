---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25091f0cb439e0447d19b534d59a0084a5b05c6e
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93874851"
---
# <span data-ttu-id="633d2-101">Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="633d2-101">Get-AzsBackupConfiguration</span></span>

## <span data-ttu-id="633d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="633d2-102">SYNOPSIS</span></span>
<span data-ttu-id="633d2-103">백업 구성 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="633d2-103">Returns the list of backup configurations.</span></span>

## <span data-ttu-id="633d2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="633d2-104">SYNTAX</span></span>

### <span data-ttu-id="633d2-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="633d2-105">List (Default)</span></span>
```
Get-AzsBackupConfiguration [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="633d2-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="633d2-106">Get</span></span>
```
Get-AzsBackupConfiguration [[-Location] <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="633d2-107">리소스</span><span class="sxs-lookup"><span data-stu-id="633d2-107">ResourceId</span></span>
```
Get-AzsBackupConfiguration -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="633d2-108">설명은</span><span class="sxs-lookup"><span data-stu-id="633d2-108">DESCRIPTION</span></span>
<span data-ttu-id="633d2-109">백업 구성 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="633d2-109">Returns the list of backup configurations.</span></span>

## <span data-ttu-id="633d2-110">예제의</span><span class="sxs-lookup"><span data-stu-id="633d2-110">EXAMPLES</span></span>

### <span data-ttu-id="633d2-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="633d2-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsBackupConfiguration
```

<span data-ttu-id="633d2-112">Azure 스택 백업 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="633d2-112">Get Azure Stack backup configuration.</span></span>

## <span data-ttu-id="633d2-113">변수</span><span class="sxs-lookup"><span data-stu-id="633d2-113">PARAMETERS</span></span>

### <span data-ttu-id="633d2-114">-위치</span><span class="sxs-lookup"><span data-stu-id="633d2-114">-Location</span></span>
<span data-ttu-id="633d2-115">백업 위치.</span><span class="sxs-lookup"><span data-stu-id="633d2-115">Backup location.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="633d2-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="633d2-116">-ResourceGroupName</span></span>
<span data-ttu-id="633d2-117">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="633d2-117">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="633d2-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="633d2-118">-ResourceId</span></span>
<span data-ttu-id="633d2-119">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="633d2-119">The resource id.</span></span>

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

### <span data-ttu-id="633d2-120">-생략</span><span class="sxs-lookup"><span data-stu-id="633d2-120">-Skip</span></span>
<span data-ttu-id="633d2-121">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="633d2-121">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="633d2-122">-위쪽</span><span class="sxs-lookup"><span data-stu-id="633d2-122">-Top</span></span>
<span data-ttu-id="633d2-123">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="633d2-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="633d2-124">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="633d2-124">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="633d2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="633d2-125">CommonParameters</span></span>
<span data-ttu-id="633d2-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="633d2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="633d2-127">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="633d2-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="633d2-128">입력</span><span class="sxs-lookup"><span data-stu-id="633d2-128">INPUTS</span></span>

## <span data-ttu-id="633d2-129">출력</span><span class="sxs-lookup"><span data-stu-id="633d2-129">OUTPUTS</span></span>

### <span data-ttu-id="633d2-130">BackupLocation. 관리자. m a. 관리</span><span class="sxs-lookup"><span data-stu-id="633d2-130">Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation</span></span>

## <span data-ttu-id="633d2-131">상속자</span><span class="sxs-lookup"><span data-stu-id="633d2-131">NOTES</span></span>

## <span data-ttu-id="633d2-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="633d2-132">RELATED LINKS</span></span>

