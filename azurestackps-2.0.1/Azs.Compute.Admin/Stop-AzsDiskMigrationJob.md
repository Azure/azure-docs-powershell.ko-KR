---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/stop-azsdiskmigrationjob
schema: 2.0.0
ms.openlocfilehash: bb5c78d6c0ae29d415e02d3e78e79f963bc3315c
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94045357"
---
# <span data-ttu-id="e48cc-101">Stop-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="e48cc-101">Stop-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="e48cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e48cc-102">SYNOPSIS</span></span>
<span data-ttu-id="e48cc-103">디스크 마이그레이션 작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="e48cc-103">Cancel a disk migration job.</span></span>

## <span data-ttu-id="e48cc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e48cc-104">SYNTAX</span></span>

```
Stop-AzsDiskMigrationJob -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e48cc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e48cc-105">DESCRIPTION</span></span>
<span data-ttu-id="e48cc-106">디스크 마이그레이션 작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="e48cc-106">Cancel a disk migration job.</span></span>

## <span data-ttu-id="e48cc-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e48cc-107">EXAMPLES</span></span>

### <span data-ttu-id="e48cc-108">예제 1:</span><span class="sxs-lookup"><span data-stu-id="e48cc-108">Example 1:</span></span>
```powershell
PS C:\> Stop-AzsDiskMigrationJob -Name TestJob

CreationTime : 2/26/2020 11:06:40 AM
EndTime      : 2/26/2020 11:07:24 AM
Id           : /subscriptions/627fecef-520e-4c18-94e0-8f0665ba86a7/providers/Microsoft.Compute.Admin/locations/redmond/diskmigrati
               onjobs/TestJob
Location     : redmond
MigrationId  : TestJob
Name         : redmond/TestJob
StartTime    : 2/26/2020 11:06:40 AM
Status       : Canceled
Subtask      : {47774498-6bc7-4ce2-98ca-738739ded2fc, b09ac623-f71d-480c-98bc-88fa3f603f2c}
TargetShare  : \\SU1FileServer.s31r1801.masd.stbtest.microsoft.com\SU1_ObjStore_4
Type         : Microsoft.Compute.Admin/locations/diskmigrationjobs
```

<span data-ttu-id="e48cc-109">관리 되는 디스크 마이그레이션 작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="e48cc-109">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="e48cc-110">변수</span><span class="sxs-lookup"><span data-stu-id="e48cc-110">PARAMETERS</span></span>

### <span data-ttu-id="e48cc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e48cc-111">-DefaultProfile</span></span>
<span data-ttu-id="e48cc-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e48cc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e48cc-113">-위치</span><span class="sxs-lookup"><span data-stu-id="e48cc-113">-Location</span></span>
<span data-ttu-id="e48cc-114">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="e48cc-114">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e48cc-115">-이름</span><span class="sxs-lookup"><span data-stu-id="e48cc-115">-Name</span></span>
<span data-ttu-id="e48cc-116">마이그레이션 작업 guid 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e48cc-116">The migration job guid name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MigrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e48cc-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e48cc-117">-SubscriptionId</span></span>
<span data-ttu-id="e48cc-118">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="e48cc-118">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e48cc-119">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e48cc-119">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e48cc-120">-확인</span><span class="sxs-lookup"><span data-stu-id="e48cc-120">-Confirm</span></span>
<span data-ttu-id="e48cc-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e48cc-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e48cc-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e48cc-122">-WhatIf</span></span>
<span data-ttu-id="e48cc-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e48cc-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e48cc-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e48cc-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e48cc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e48cc-125">CommonParameters</span></span>
<span data-ttu-id="e48cc-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e48cc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e48cc-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e48cc-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e48cc-128">입력</span><span class="sxs-lookup"><span data-stu-id="e48cc-128">INPUTS</span></span>

## <span data-ttu-id="e48cc-129">출력</span><span class="sxs-lookup"><span data-stu-id="e48cc-129">OUTPUTS</span></span>

### <span data-ttu-id="e48cc-130">Api20180730Preview. IDiskMigrationJob에 대 한. t t t</span><span class="sxs-lookup"><span data-stu-id="e48cc-130">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDiskMigrationJob</span></span>



## <span data-ttu-id="e48cc-131">상속자</span><span class="sxs-lookup"><span data-stu-id="e48cc-131">NOTES</span></span>

## <span data-ttu-id="e48cc-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e48cc-132">RELATED LINKS</span></span>

