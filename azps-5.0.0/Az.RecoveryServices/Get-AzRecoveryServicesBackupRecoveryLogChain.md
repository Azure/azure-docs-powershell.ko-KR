---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverylogchain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
ms.openlocfilehash: ba82e1ddf8385f74b271feb9119280d48fc1b859
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216858"
---
# <span data-ttu-id="354c2-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span><span class="sxs-lookup"><span data-stu-id="354c2-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span></span>

## <span data-ttu-id="354c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="354c2-102">SYNOPSIS</span></span>
<span data-ttu-id="354c2-103">이 명령은 지정 된 백업 항목의 끊어지지 않은 로그 체인 시작점과 끝점을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="354c2-103">This command lists the start and end points of the unbroken log chain of the given backup item.</span></span> <span data-ttu-id="354c2-104">이 기능을 사용 하 여 사용자가 DB를 복원 하려는 시점 시간 (유효 여부)을 결정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="354c2-104">Use it to determine whether the point-in-time, to which the user wants the DB to be restored, is valid or not.</span></span>

## <span data-ttu-id="354c2-105">구문과</span><span class="sxs-lookup"><span data-stu-id="354c2-105">SYNTAX</span></span>

### <span data-ttu-id="354c2-106">NoFilterParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="354c2-106">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="354c2-107">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="354c2-107">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="354c2-108">설명은</span><span class="sxs-lookup"><span data-stu-id="354c2-108">DESCRIPTION</span></span>
<span data-ttu-id="354c2-109">**AzRecoveryServicesBackupRecoveryLogChain** cmdlet은 백업 된 Azure 백업 항목에 대 한 시간 범위 복구 지점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="354c2-109">The **Get-AzRecoveryServicesBackupRecoveryLogChain** cmdlet gets the time range recovery points in time for a backed up Azure Backup item.</span></span>
<span data-ttu-id="354c2-110">항목을 백업한 후에는 **AzRecoveryServicesBackupRecoveryLogChain** 개체에 복구 시간 범위가 하나 이상 있습니다.</span><span class="sxs-lookup"><span data-stu-id="354c2-110">After an item has been backed up, an **AzRecoveryServicesBackupRecoveryLogChain** object has one or more recovery time ranges.</span></span>

## <span data-ttu-id="354c2-111">예제의</span><span class="sxs-lookup"><span data-stu-id="354c2-111">EXAMPLES</span></span>

### <span data-ttu-id="354c2-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="354c2-112">Example 1</span></span>
```powershell
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureWorkload -Status Registered
PS C:\> $RP = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType MSSQL | Get-AzRecoveryServicesBackupRecoveryLogChain -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="354c2-113">첫 번째 명령은 7 일 전 날짜를 가져온 다음 $StartDate 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="354c2-113">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="354c2-114">두 번째 명령은 오늘 날짜를 가져온 다음 $EndDate 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="354c2-114">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="354c2-115">세 번째 명령은 AzureWorkload 부하 백업 컨테이너를 가져와 $Container 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="354c2-115">The third command gets AzureWorkload backup containers, and stores them in the $Container variable.</span></span>
<span data-ttu-id="354c2-116">네 번째 명령은 백업 항목을 가져온 다음,이를 파이프 된 cmdlet에서 백업 항목 개체로 공유 합니다.</span><span class="sxs-lookup"><span data-stu-id="354c2-116">The fourth command gets the backup item, and then shares it across the piped cmdlet as backup item object.</span></span>
<span data-ttu-id="354c2-117">마지막 명령은 $BackupItem의 항목에 대 한 복구 시점 시간 범위의 배열을 가져온 다음 $RP 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="354c2-117">The last command gets an array of recovery point time ranges for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

### <span data-ttu-id="354c2-118">예제 2</span><span class="sxs-lookup"><span data-stu-id="354c2-118">Example 2</span></span>

<span data-ttu-id="354c2-119">이 명령은 지정 된 백업 항목의 끊어지지 않은 로그 체인 시작점과 끝점을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="354c2-119">This command lists the start and end points of the unbroken log chain of the given backup item.</span></span> <span data-ttu-id="354c2-120">생성</span><span class="sxs-lookup"><span data-stu-id="354c2-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupRecoveryLogChain -Item $Item -VaultId $vault.ID
```

## <span data-ttu-id="354c2-121">변수</span><span class="sxs-lookup"><span data-stu-id="354c2-121">PARAMETERS</span></span>

### <span data-ttu-id="354c2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="354c2-122">-DefaultProfile</span></span>
<span data-ttu-id="354c2-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="354c2-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="354c2-124">-EndDate</span><span class="sxs-lookup"><span data-stu-id="354c2-124">-EndDate</span></span>
<span data-ttu-id="354c2-125">복구 지점을 가져오지 않아도 되는 시간 범위 종료 시간</span><span class="sxs-lookup"><span data-stu-id="354c2-125">End time of Time range for which recovery point need to be fetched</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="354c2-126">-항목</span><span class="sxs-lookup"><span data-stu-id="354c2-126">-Item</span></span>
<span data-ttu-id="354c2-127">복구 지점을 가져오지 않아도 되는 보호 된 항목 개체</span><span class="sxs-lookup"><span data-stu-id="354c2-127">Protected Item object for which recovery point need to be fetched</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="354c2-128">-시작 날짜</span><span class="sxs-lookup"><span data-stu-id="354c2-128">-StartDate</span></span>
<span data-ttu-id="354c2-129">복구 지점을 가져오지 않아도 되는 시작 시간 범위</span><span class="sxs-lookup"><span data-stu-id="354c2-129">Start time of Time range for which recovery point need to be fetched</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="354c2-130">-VaultId</span><span class="sxs-lookup"><span data-stu-id="354c2-130">-VaultId</span></span>
<span data-ttu-id="354c2-131">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="354c2-131">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="354c2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="354c2-132">CommonParameters</span></span>
<span data-ttu-id="354c2-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="354c2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="354c2-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="354c2-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="354c2-135">입력</span><span class="sxs-lookup"><span data-stu-id="354c2-135">INPUTS</span></span>

### <span data-ttu-id="354c2-136">Microsoft Azure.. i g i..</span><span class="sxs-lookup"><span data-stu-id="354c2-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="354c2-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="354c2-137">System.String</span></span>

## <span data-ttu-id="354c2-138">출력</span><span class="sxs-lookup"><span data-stu-id="354c2-138">OUTPUTS</span></span>

### <span data-ttu-id="354c2-139">RecoveryPointBase에서. i. i m/.</span><span class="sxs-lookup"><span data-stu-id="354c2-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="354c2-140">상속자</span><span class="sxs-lookup"><span data-stu-id="354c2-140">NOTES</span></span>

## <span data-ttu-id="354c2-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="354c2-141">RELATED LINKS</span></span>
