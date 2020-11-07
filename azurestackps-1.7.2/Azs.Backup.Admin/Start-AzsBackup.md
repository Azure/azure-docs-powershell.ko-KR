---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 460d24e091a702cfee32b8c5b7d9c3a8016e73b3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874541"
---
# <span data-ttu-id="f0a2c-101">Start-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="f0a2c-101">Start-AzsBackup</span></span>

## <span data-ttu-id="f0a2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0a2c-102">SYNOPSIS</span></span>
<span data-ttu-id="f0a2c-103">특정 위치를 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0a2c-103">Back up a specific location.</span></span>

## <span data-ttu-id="f0a2c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f0a2c-104">SYNTAX</span></span>

### <span data-ttu-id="f0a2c-105">CreateBackup (기본값)</span><span class="sxs-lookup"><span data-stu-id="f0a2c-105">CreateBackup (Default)</span></span>
```
Start-AzsBackup [-ResourceGroupName <String>] [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f0a2c-106">CreateBackup_FromResourceId</span><span class="sxs-lookup"><span data-stu-id="f0a2c-106">CreateBackup_FromResourceId</span></span>
```
Start-AzsBackup -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0a2c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f0a2c-107">DESCRIPTION</span></span>
<span data-ttu-id="f0a2c-108">특정 위치를 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0a2c-108">Back up a specific location.</span></span>

## <span data-ttu-id="f0a2c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f0a2c-109">EXAMPLES</span></span>

### <span data-ttu-id="f0a2c-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="f0a2c-110">EXAMPLE 1</span></span>
```
Start-AzsBackup
```

<span data-ttu-id="f0a2c-111">Azure 스택 백업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0a2c-111">Start an Azure Stack backup.</span></span>

## <span data-ttu-id="f0a2c-112">변수</span><span class="sxs-lookup"><span data-stu-id="f0a2c-112">PARAMETERS</span></span>

### <span data-ttu-id="f0a2c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f0a2c-113">-AsJob</span></span>
<span data-ttu-id="f0a2c-114">비동기를 작업으로 실행 하 고 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0a2c-114">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0a2c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f0a2c-115">-Force</span></span>
<span data-ttu-id="f0a2c-116">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f0a2c-116">Don't ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0a2c-117">-위치</span><span class="sxs-lookup"><span data-stu-id="f0a2c-117">-Location</span></span>
<span data-ttu-id="f0a2c-118">백업 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f0a2c-118">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0a2c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0a2c-119">-ResourceGroupName</span></span>
<span data-ttu-id="f0a2c-120">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f0a2c-120">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0a2c-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0a2c-121">-ResourceId</span></span>
<span data-ttu-id="f0a2c-122">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="f0a2c-122">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBackup_FromResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0a2c-123">-확인</span><span class="sxs-lookup"><span data-stu-id="f0a2c-123">-Confirm</span></span>
<span data-ttu-id="f0a2c-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0a2c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0a2c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0a2c-125">-WhatIf</span></span>
<span data-ttu-id="f0a2c-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f0a2c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0a2c-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f0a2c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0a2c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0a2c-128">CommonParameters</span></span>
<span data-ttu-id="f0a2c-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0a2c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0a2c-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0a2c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0a2c-131">입력</span><span class="sxs-lookup"><span data-stu-id="f0a2c-131">INPUTS</span></span>

## <span data-ttu-id="f0a2c-132">출력</span><span class="sxs-lookup"><span data-stu-id="f0a2c-132">OUTPUTS</span></span>

### <span data-ttu-id="f0a2c-133">LongRunningOperationStatus. 관리자. m a. 관리</span><span class="sxs-lookup"><span data-stu-id="f0a2c-133">Microsoft.AzureStack.Management.Backup.Admin.Models.LongRunningOperationStatus</span></span>

## <span data-ttu-id="f0a2c-134">상속자</span><span class="sxs-lookup"><span data-stu-id="f0a2c-134">NOTES</span></span>

## <span data-ttu-id="f0a2c-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f0a2c-135">RELATED LINKS</span></span>
