---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5bf583c30d2faff1055debf366a84a0739789467
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046804"
---
# <span data-ttu-id="f819a-101">Start-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="f819a-101">Start-AzsBackup</span></span>

## <span data-ttu-id="f819a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f819a-102">SYNOPSIS</span></span>
<span data-ttu-id="f819a-103">특정 위치를 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="f819a-103">Back up a specific location.</span></span>

## <span data-ttu-id="f819a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f819a-104">SYNTAX</span></span>

### <span data-ttu-id="f819a-105">CreateBackup (기본값)</span><span class="sxs-lookup"><span data-stu-id="f819a-105">CreateBackup (Default)</span></span>
```
Start-AzsBackup [-ResourceGroupName <String>] [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f819a-106">CreateBackup_FromResourceId</span><span class="sxs-lookup"><span data-stu-id="f819a-106">CreateBackup_FromResourceId</span></span>
```
Start-AzsBackup -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f819a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f819a-107">DESCRIPTION</span></span>
<span data-ttu-id="f819a-108">특정 위치를 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="f819a-108">Back up a specific location.</span></span>

## <span data-ttu-id="f819a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f819a-109">EXAMPLES</span></span>

### <span data-ttu-id="f819a-110">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f819a-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsBackup
```

<span data-ttu-id="f819a-111">Azure 스택 백업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="f819a-111">Start an Azure Stack backup.</span></span>

## <span data-ttu-id="f819a-112">변수</span><span class="sxs-lookup"><span data-stu-id="f819a-112">PARAMETERS</span></span>

### <span data-ttu-id="f819a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f819a-113">-AsJob</span></span>
<span data-ttu-id="f819a-114">비동기를 작업으로 실행 하 고 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f819a-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="f819a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f819a-115">-Force</span></span>
<span data-ttu-id="f819a-116">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f819a-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="f819a-117">-위치</span><span class="sxs-lookup"><span data-stu-id="f819a-117">-Location</span></span>
<span data-ttu-id="f819a-118">백업 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f819a-118">Name of the backup location.</span></span>

```yaml
Type: String
Parameter Sets: CreateBackup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f819a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f819a-119">-ResourceGroupName</span></span>
<span data-ttu-id="f819a-120">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f819a-120">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: CreateBackup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f819a-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f819a-121">-ResourceId</span></span>
<span data-ttu-id="f819a-122">{{ResourceId: 채우기 설명}}</span><span class="sxs-lookup"><span data-stu-id="f819a-122">{{Fill ResourceId Description}}</span></span>

```yaml
Type: String
Parameter Sets: CreateBackup_FromResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f819a-123">-확인</span><span class="sxs-lookup"><span data-stu-id="f819a-123">-Confirm</span></span>
<span data-ttu-id="f819a-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f819a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f819a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f819a-125">-WhatIf</span></span>
<span data-ttu-id="f819a-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f819a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f819a-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f819a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f819a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f819a-128">CommonParameters</span></span>
<span data-ttu-id="f819a-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f819a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f819a-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f819a-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f819a-131">입력</span><span class="sxs-lookup"><span data-stu-id="f819a-131">INPUTS</span></span>

## <span data-ttu-id="f819a-132">출력</span><span class="sxs-lookup"><span data-stu-id="f819a-132">OUTPUTS</span></span>

### <span data-ttu-id="f819a-133">LongRunningOperationStatus. 관리자. m a. 관리</span><span class="sxs-lookup"><span data-stu-id="f819a-133">Microsoft.AzureStack.Management.Backup.Admin.Models.LongRunningOperationStatus</span></span>

## <span data-ttu-id="f819a-134">상속자</span><span class="sxs-lookup"><span data-stu-id="f819a-134">NOTES</span></span>

## <span data-ttu-id="f819a-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f819a-135">RELATED LINKS</span></span>

