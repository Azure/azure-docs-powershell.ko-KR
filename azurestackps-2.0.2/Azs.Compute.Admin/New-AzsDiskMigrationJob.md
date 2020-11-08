---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/new-azsdiskmigrationjob
schema: 2.0.0
ms.openlocfilehash: c3fd190fb033a685bcb0d5087c544298681e47c5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046730"
---
# <span data-ttu-id="73757-101">New-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="73757-101">New-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="73757-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73757-102">SYNOPSIS</span></span>


## <span data-ttu-id="73757-103">구문과</span><span class="sxs-lookup"><span data-stu-id="73757-103">SYNTAX</span></span>

### <span data-ttu-id="73757-104">볼륨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="73757-104">Volume (Default)</span></span>
```
New-AzsDiskMigrationJob -Name <String> -TargetScaleUnit <String> -TargetVolumeLabel <String> -Disks <IDisk[]>
 [-Location <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="73757-105">공유</span><span class="sxs-lookup"><span data-stu-id="73757-105">Share</span></span>
```
New-AzsDiskMigrationJob -Name <String> -TargetShare <String> -Disks <IDisk[]> [-Location <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="73757-106">설명은</span><span class="sxs-lookup"><span data-stu-id="73757-106">DESCRIPTION</span></span>


## <span data-ttu-id="73757-107">예제의</span><span class="sxs-lookup"><span data-stu-id="73757-107">EXAMPLES</span></span>

### <span data-ttu-id="73757-108">예제 1:</span><span class="sxs-lookup"><span data-stu-id="73757-108">Example 1:</span></span>
```powershell
PS C:\> $disks = Get-AzsDisk
PS C:\> New-AzsDiskMigrationJob -Name TestJob1 -TargetScaleUnit s-cluster -TargetVolumeLabel ObjStore_2 -Disks $disks

CreationTime : 2/26/2020 10:56:32 AM
EndTime      : 
Id           : /subscriptions/627fecef-520e-4c18-94e0-8f0665ba86a7/providers/Microsoft.Compute.Admin/locations/redmond/diskmigrationjobs/TestJob1
Location     : redmond
MigrationId  : TestJob1
Name         : redmond/TestJob1
StartTime    : 
Status       : Pending
Subtask      : {53ee3665-00e4-4c69-a067-524058905ead, d551734f-0370-4851-9704-c7cec80b34c5}
TargetShare  : \\SU1FileServer.s31r1801.masd.stbtest.microsoft.com\SU1_ObjStore_2
Type         : Microsoft.Compute.Admin/locations/diskmigrationjobs
```

<span data-ttu-id="73757-109">디스크 마이그레이션 작업을 만들어 디스크를 대상 크기 조정 단위 및 볼륨으로 마이그레이션합니다.</span><span class="sxs-lookup"><span data-stu-id="73757-109">Create a disk migration job to migrate disks to the target scale unit and volume.</span></span>

### <span data-ttu-id="73757-110">예제 2:</span><span class="sxs-lookup"><span data-stu-id="73757-110">Example 2:</span></span> 
```powershell
PS C:\> PS C:\> $disks = Get-AzsDisk
PS C:\> New-AzsDiskMigrationJob -Name TestJob2 -TargetShare \\SU1FileServer.s31r1801.masd.stbtest.microsoft.com\SU1_ObjStore_3 -Disks $disks
WARNING: TargetShare parameter will be deprecated in a future release, please use Volume instead.

CreationTime : 2/26/2020 11:02:48 AM
EndTime      : 
Id           : /subscriptions/627fecef-520e-4c18-94e0-8f0665ba86a7/providers/Microsoft.Compute.Admin/locations/redmond/diskmigrati
               onjobs/TestJob2
Location     : redmond
MigrationId  : TestJob2
Name         : redmond/TestJob2
StartTime    : 
Status       : Pending
Subtask      : {0cfd8d29-1ca4-42db-a490-9198814abc50, 89c9b15e-47c6-4321-a390-611fc190cfad}
TargetShare  : \\SU1FileServer.s31r1801.masd.stbtest.microsoft.com\SU1_ObjStore_3
Type         : Microsoft.Compute.Admin/locations/diskmigrationjobs-AzsDiskMigrationJob -Name TestJob1 -TargetScaleUnit s-cluster -TargetVolumeLabel ObjStore_2 -Disks $disks

```

<span data-ttu-id="73757-111">디스크 마이그레이션 작업을 만들어 디스크를 대상 공유로 마이그레이션합니다.</span><span class="sxs-lookup"><span data-stu-id="73757-111">Create a disk migration job to migrate disks to the target share.</span></span>

## <span data-ttu-id="73757-112">변수</span><span class="sxs-lookup"><span data-stu-id="73757-112">PARAMETERS</span></span>

### <span data-ttu-id="73757-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73757-113">-DefaultProfile</span></span>


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

### <span data-ttu-id="73757-114">-디스크</span><span class="sxs-lookup"><span data-stu-id="73757-114">-Disks</span></span>
<span data-ttu-id="73757-115">생성 하려면 디스크 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="73757-115">To construct, see NOTES section for DISKS properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDisk[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="73757-116">-위치</span><span class="sxs-lookup"><span data-stu-id="73757-116">-Location</span></span>


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

### <span data-ttu-id="73757-117">-이름</span><span class="sxs-lookup"><span data-stu-id="73757-117">-Name</span></span>


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

### <span data-ttu-id="73757-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="73757-118">-SubscriptionId</span></span>


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

### <span data-ttu-id="73757-119">-TargetScaleUnit</span><span class="sxs-lookup"><span data-stu-id="73757-119">-TargetScaleUnit</span></span>


```yaml
Type: System.String
Parameter Sets: Volume
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="73757-120">-TargetShare</span><span class="sxs-lookup"><span data-stu-id="73757-120">-TargetShare</span></span>


```yaml
Type: System.String
Parameter Sets: Share
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="73757-121">-TargetVolumeLabel</span><span class="sxs-lookup"><span data-stu-id="73757-121">-TargetVolumeLabel</span></span>


```yaml
Type: System.String
Parameter Sets: Volume
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="73757-122">-확인</span><span class="sxs-lookup"><span data-stu-id="73757-122">-Confirm</span></span>
<span data-ttu-id="73757-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="73757-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73757-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73757-124">-WhatIf</span></span>
<span data-ttu-id="73757-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="73757-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73757-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="73757-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73757-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73757-127">CommonParameters</span></span>
<span data-ttu-id="73757-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="73757-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73757-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="73757-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73757-130">입력</span><span class="sxs-lookup"><span data-stu-id="73757-130">INPUTS</span></span>

### <span data-ttu-id="73757-131">Api20180730Preview. t a t t a t a t a t a t 디스크 []</span><span class="sxs-lookup"><span data-stu-id="73757-131">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDisk[]</span></span>

## <span data-ttu-id="73757-132">출력</span><span class="sxs-lookup"><span data-stu-id="73757-132">OUTPUTS</span></span>

### <span data-ttu-id="73757-133">Api20180730Preview. IDiskMigrationJob에 대 한. t t t</span><span class="sxs-lookup"><span data-stu-id="73757-133">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDiskMigrationJob</span></span>



### <span data-ttu-id="73757-134">Start-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="73757-134">Start-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="73757-135">상속자</span><span class="sxs-lookup"><span data-stu-id="73757-135">NOTES</span></span>

<span data-ttu-id="73757-136">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="73757-136">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="73757-137">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="73757-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="73757-138">디스크 <IDisk [] >:</span><span class="sxs-lookup"><span data-stu-id="73757-138">DISKS <IDisk[]>:</span></span> 
  - <span data-ttu-id="73757-139">`[Location <String>]`: 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="73757-139">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="73757-140">`[DiskId <String>]`: 디스크 id입니다.</span><span class="sxs-lookup"><span data-stu-id="73757-140">`[DiskId <String>]`: The disk id.</span></span>
  - <span data-ttu-id="73757-141">`[SharePath <String>]`: 디스크 공유 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="73757-141">`[SharePath <String>]`: The disk share path.</span></span>
  - <span data-ttu-id="73757-142">`[Status <DiskState?>]`: 디스크 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="73757-142">`[Status <DiskState?>]`: The disk status.</span></span>

## <span data-ttu-id="73757-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="73757-143">RELATED LINKS</span></span>

