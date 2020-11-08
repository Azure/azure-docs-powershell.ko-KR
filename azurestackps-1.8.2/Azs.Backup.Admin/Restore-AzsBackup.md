---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 573a47b3684020817130e1d41c764abef717de0a
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046805"
---
# <span data-ttu-id="20117-101">Restore-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="20117-101">Restore-AzsBackup</span></span>

## <span data-ttu-id="20117-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20117-102">SYNOPSIS</span></span>
<span data-ttu-id="20117-103">백업을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="20117-103">Restore a backup.</span></span>

## <span data-ttu-id="20117-104">구문과</span><span class="sxs-lookup"><span data-stu-id="20117-104">SYNTAX</span></span>

### <span data-ttu-id="20117-105">Backups_Restore (기본값)</span><span class="sxs-lookup"><span data-stu-id="20117-105">Backups_Restore (Default)</span></span>
```
Restore-AzsBackup [-ResourceGroupName <String>] -Name <String> [-Location <String>] [-AsJob] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20117-106">리소스</span><span class="sxs-lookup"><span data-stu-id="20117-106">ResourceId</span></span>
```
Restore-AzsBackup -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20117-107">설명은</span><span class="sxs-lookup"><span data-stu-id="20117-107">DESCRIPTION</span></span>
<span data-ttu-id="20117-108">백업을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="20117-108">Restore a backup.</span></span>

## <span data-ttu-id="20117-109">예제의</span><span class="sxs-lookup"><span data-stu-id="20117-109">EXAMPLES</span></span>

### <span data-ttu-id="20117-110">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="20117-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Restore-AzsBackup -Backup 4e90bd2f-c7ab-47a3-a3c7-908cddd1ad0e
```

<span data-ttu-id="20117-111">Azure 스택 백업에서 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="20117-111">Restore from an Azure Stack backup.</span></span>

## <span data-ttu-id="20117-112">변수</span><span class="sxs-lookup"><span data-stu-id="20117-112">PARAMETERS</span></span>

### <span data-ttu-id="20117-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="20117-113">-AsJob</span></span>
<span data-ttu-id="20117-114">비동기를 작업으로 실행 하 고 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="20117-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="20117-115">-Force</span><span class="sxs-lookup"><span data-stu-id="20117-115">-Force</span></span>
<span data-ttu-id="20117-116">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="20117-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="20117-117">-위치</span><span class="sxs-lookup"><span data-stu-id="20117-117">-Location</span></span>
<span data-ttu-id="20117-118">백업할 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="20117-118">Name of location to backup.</span></span>

```yaml
Type: String
Parameter Sets: Backups_Restore
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20117-119">-이름</span><span class="sxs-lookup"><span data-stu-id="20117-119">-Name</span></span>
<span data-ttu-id="20117-120">백업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="20117-120">Name of the backup.</span></span>

```yaml
Type: String
Parameter Sets: Backups_Restore
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20117-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20117-121">-ResourceGroupName</span></span>
<span data-ttu-id="20117-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="20117-122">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: Backups_Restore
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20117-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="20117-123">-ResourceId</span></span>
<span data-ttu-id="20117-124">{{ResourceId: 채우기 설명}}</span><span class="sxs-lookup"><span data-stu-id="20117-124">{{Fill ResourceId Description}}</span></span>

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

### <span data-ttu-id="20117-125">-확인</span><span class="sxs-lookup"><span data-stu-id="20117-125">-Confirm</span></span>
<span data-ttu-id="20117-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="20117-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20117-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20117-127">-WhatIf</span></span>
<span data-ttu-id="20117-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="20117-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20117-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="20117-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20117-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20117-130">CommonParameters</span></span>
<span data-ttu-id="20117-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="20117-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20117-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20117-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20117-133">입력</span><span class="sxs-lookup"><span data-stu-id="20117-133">INPUTS</span></span>

## <span data-ttu-id="20117-134">출력</span><span class="sxs-lookup"><span data-stu-id="20117-134">OUTPUTS</span></span>

## <span data-ttu-id="20117-135">상속자</span><span class="sxs-lookup"><span data-stu-id="20117-135">NOTES</span></span>

## <span data-ttu-id="20117-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="20117-136">RELATED LINKS</span></span>

