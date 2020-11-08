---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverylogchain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
ms.openlocfilehash: 8a0fbc09f9c46bea6ac09d75911ac83b68f0e296
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044733"
---
# <span data-ttu-id="e078a-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span><span class="sxs-lookup"><span data-stu-id="e078a-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span></span>

## <span data-ttu-id="e078a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e078a-102">SYNOPSIS</span></span>
<span data-ttu-id="e078a-103">이 명령은 지정 된 백업 항목의 끊어지지 않은 로그 체인 시작점과 끝점을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="e078a-103">This command lists the start and end points of the unbroken log chain of the given backup item.</span></span> <span data-ttu-id="e078a-104">이 기능을 사용 하 여 사용자가 DB를 복원 하려는 시점 시간 (유효 여부)을 결정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e078a-104">Use it to determine whether the point-in-time, to which the user wants the DB to be restored, is valid or not.</span></span>

## <span data-ttu-id="e078a-105">구문과</span><span class="sxs-lookup"><span data-stu-id="e078a-105">SYNTAX</span></span>

### <span data-ttu-id="e078a-106">NoFilterParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="e078a-106">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e078a-107">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="e078a-107">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e078a-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e078a-108">DESCRIPTION</span></span>
<span data-ttu-id="e078a-109">**AzRecoveryServicesBackupRecoveryLogChain** cmdlet은 백업 된 Azure 백업 항목에 대 한 시간 범위 복구 지점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e078a-109">The **Get-AzRecoveryServicesBackupRecoveryLogChain** cmdlet gets the time range recovery points in time for a backed up Azure Backup item.</span></span>
<span data-ttu-id="e078a-110">항목을 백업한 후에는 **AzRecoveryServicesBackupRecoveryLogChain** 개체에 복구 시간 범위가 하나 이상 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e078a-110">After an item has been backed up, an **AzRecoveryServicesBackupRecoveryLogChain** object has one or more recovery time ranges.</span></span>

## <span data-ttu-id="e078a-111">예제의</span><span class="sxs-lookup"><span data-stu-id="e078a-111">EXAMPLES</span></span>

### <span data-ttu-id="e078a-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="e078a-112">Example 1</span></span>
```
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureWorkload -Status Registered
PS C:\> $RP = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType MSSQL | Get-AzRecoveryServicesBackupRecoveryLogChain -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="e078a-113">첫 번째 명령은 7 일 전 날짜를 가져온 다음 $StartDate 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e078a-113">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="e078a-114">두 번째 명령은 오늘 날짜를 가져온 다음 $EndDate 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e078a-114">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="e078a-115">세 번째 명령은 AzureWorkload 부하 백업 컨테이너를 가져와 $Containers 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e078a-115">The third command gets AzureWorkload backup containers, and stores them in the $Containers variable.</span></span>
<span data-ttu-id="e078a-116">네 번째 명령은 백업 항목을 가져온 다음 $BackupItem 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e078a-116">The fourth command gets the backup item, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="e078a-117">마지막 명령은 $BackupItem의 항목에 대 한 복구 시점 시간 범위의 배열을 가져온 다음 $RP 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e078a-117">The last command gets an array of recovery point time ranges for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="e078a-118">변수</span><span class="sxs-lookup"><span data-stu-id="e078a-118">PARAMETERS</span></span>

### <span data-ttu-id="e078a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e078a-119">-DefaultProfile</span></span>
<span data-ttu-id="e078a-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e078a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e078a-121">-EndDate</span><span class="sxs-lookup"><span data-stu-id="e078a-121">-EndDate</span></span>
<span data-ttu-id="e078a-122">복구 지점을 가져오지 않아도 되는 시간 범위 종료 시간</span><span class="sxs-lookup"><span data-stu-id="e078a-122">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="e078a-123">-항목</span><span class="sxs-lookup"><span data-stu-id="e078a-123">-Item</span></span>
<span data-ttu-id="e078a-124">복구 지점을 가져오지 않아도 되는 보호 된 항목 개체</span><span class="sxs-lookup"><span data-stu-id="e078a-124">Protected Item object for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="e078a-125">-시작 날짜</span><span class="sxs-lookup"><span data-stu-id="e078a-125">-StartDate</span></span>
<span data-ttu-id="e078a-126">복구 지점을 가져오지 않아도 되는 시작 시간 범위</span><span class="sxs-lookup"><span data-stu-id="e078a-126">Start time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="e078a-127">-VaultId</span><span class="sxs-lookup"><span data-stu-id="e078a-127">-VaultId</span></span>
<span data-ttu-id="e078a-128">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e078a-128">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="e078a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e078a-129">CommonParameters</span></span>
<span data-ttu-id="e078a-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e078a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e078a-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e078a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e078a-132">입력</span><span class="sxs-lookup"><span data-stu-id="e078a-132">INPUTS</span></span>

### <span data-ttu-id="e078a-133">Microsoft Azure.. i g i..</span><span class="sxs-lookup"><span data-stu-id="e078a-133">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="e078a-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e078a-134">System.String</span></span>

## <span data-ttu-id="e078a-135">출력</span><span class="sxs-lookup"><span data-stu-id="e078a-135">OUTPUTS</span></span>

### <span data-ttu-id="e078a-136">RecoveryPointBase에서. i. i m/.</span><span class="sxs-lookup"><span data-stu-id="e078a-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="e078a-137">상속자</span><span class="sxs-lookup"><span data-stu-id="e078a-137">NOTES</span></span>

## <span data-ttu-id="e078a-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e078a-138">RELATED LINKS</span></span>
