---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverylogchain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
ms.openlocfilehash: ba82e1ddf8385f74b271feb9119280d48fc1b859
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351374"
---
# <span data-ttu-id="2b6bb-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span><span class="sxs-lookup"><span data-stu-id="2b6bb-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span></span>

## <span data-ttu-id="2b6bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b6bb-102">SYNOPSIS</span></span>
<span data-ttu-id="2b6bb-103">이 명령은 주어진 백업 항목의 끊어지지 않은 로그 체인의 시작점과 끝점을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="2b6bb-103">This command lists the start and end points of the unbroken log chain of the given backup item.</span></span> <span data-ttu-id="2b6bb-104">이를 사용하여 사용자가 DB를 복원하려는 특정 시점이 유효한지 여부를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b6bb-104">Use it to determine whether the point-in-time, to which the user wants the DB to be restored, is valid or not.</span></span>

## <span data-ttu-id="2b6bb-105">구문</span><span class="sxs-lookup"><span data-stu-id="2b6bb-105">SYNTAX</span></span>

### <span data-ttu-id="2b6bb-106">NoFilterParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="2b6bb-106">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b6bb-107">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="2b6bb-107">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b6bb-108">설명</span><span class="sxs-lookup"><span data-stu-id="2b6bb-108">DESCRIPTION</span></span>
<span data-ttu-id="2b6bb-109">**Get-AzRecoveryServicesBackupRecoveryLogChain** cmdlet은 백업된 Azure Backup 항목에 대한 시간 범위 복구 지점을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2b6bb-109">The **Get-AzRecoveryServicesBackupRecoveryLogChain** cmdlet gets the time range recovery points in time for a backed up Azure Backup item.</span></span>
<span data-ttu-id="2b6bb-110">항목이 백업된 후 **AzRecoveryServicesBackupRecoveryLogChain** 개체에는 하나 이상의 복구 시간 범위가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b6bb-110">After an item has been backed up, an **AzRecoveryServicesBackupRecoveryLogChain** object has one or more recovery time ranges.</span></span>

## <span data-ttu-id="2b6bb-111">예제</span><span class="sxs-lookup"><span data-stu-id="2b6bb-111">EXAMPLES</span></span>

### <span data-ttu-id="2b6bb-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="2b6bb-112">Example 1</span></span>
```powershell
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureWorkload -Status Registered
PS C:\> $RP = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType MSSQL | Get-AzRecoveryServicesBackupRecoveryLogChain -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="2b6bb-113">첫 번째 명령은 7일 전에 날짜를 인용한 다음 $StartDate 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="2b6bb-113">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="2b6bb-114">두 번째 명령은 오늘 날짜를 인용한 다음, $EndDate 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="2b6bb-114">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="2b6bb-115">세 번째 명령은 AzureWorkload 백업 컨테이너를 사용하여 컨테이너를 $Container 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="2b6bb-115">The third command gets AzureWorkload backup containers, and stores them in the $Container variable.</span></span>
<span data-ttu-id="2b6bb-116">네 번째 명령은 백업 항목을 인출한 다음 파이프된 cmdlet에서 백업 항목 개체로 공유합니다.</span><span class="sxs-lookup"><span data-stu-id="2b6bb-116">The fourth command gets the backup item, and then shares it across the piped cmdlet as backup item object.</span></span>
<span data-ttu-id="2b6bb-117">마지막 명령은 $BackupItem 항목에 대한 복구 지점 시간 범위의 배열을 $RP 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="2b6bb-117">The last command gets an array of recovery point time ranges for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

### <span data-ttu-id="2b6bb-118">예제 2</span><span class="sxs-lookup"><span data-stu-id="2b6bb-118">Example 2</span></span>

<span data-ttu-id="2b6bb-119">이 명령은 주어진 백업 항목의 끊어지지 않은 로그 체인의 시작점과 끝점을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="2b6bb-119">This command lists the start and end points of the unbroken log chain of the given backup item.</span></span> <span data-ttu-id="2b6bb-120">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="2b6bb-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupRecoveryLogChain -Item $Item -VaultId $vault.ID
```

## <span data-ttu-id="2b6bb-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2b6bb-121">PARAMETERS</span></span>

### <span data-ttu-id="2b6bb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b6bb-122">-DefaultProfile</span></span>
<span data-ttu-id="2b6bb-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2b6bb-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b6bb-124">-EndDate</span><span class="sxs-lookup"><span data-stu-id="2b6bb-124">-EndDate</span></span>
<span data-ttu-id="2b6bb-125">복구 지점을 페치해야 하는 시간 범위의 종료 시간</span><span class="sxs-lookup"><span data-stu-id="2b6bb-125">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="2b6bb-126">-Item</span><span class="sxs-lookup"><span data-stu-id="2b6bb-126">-Item</span></span>
<span data-ttu-id="2b6bb-127">복구 지점을 페치해야 하는 보호된 항목 개체</span><span class="sxs-lookup"><span data-stu-id="2b6bb-127">Protected Item object for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="2b6bb-128">-StartDate</span><span class="sxs-lookup"><span data-stu-id="2b6bb-128">-StartDate</span></span>
<span data-ttu-id="2b6bb-129">복구 지점을 페치해야 하는 시간 범위의 시작 시간</span><span class="sxs-lookup"><span data-stu-id="2b6bb-129">Start time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="2b6bb-130">-VaultId</span><span class="sxs-lookup"><span data-stu-id="2b6bb-130">-VaultId</span></span>
<span data-ttu-id="2b6bb-131">ARM 자격 증명 모음의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2b6bb-131">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="2b6bb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b6bb-132">CommonParameters</span></span>
<span data-ttu-id="2b6bb-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2b6bb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b6bb-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2b6bb-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b6bb-135">입력</span><span class="sxs-lookup"><span data-stu-id="2b6bb-135">INPUTS</span></span>

### <span data-ttu-id="2b6bb-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="2b6bb-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="2b6bb-137">System.String</span><span class="sxs-lookup"><span data-stu-id="2b6bb-137">System.String</span></span>

## <span data-ttu-id="2b6bb-138">출력</span><span class="sxs-lookup"><span data-stu-id="2b6bb-138">OUTPUTS</span></span>

### <span data-ttu-id="2b6bb-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="2b6bb-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="2b6bb-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2b6bb-140">NOTES</span></span>

## <span data-ttu-id="2b6bb-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2b6bb-141">RELATED LINKS</span></span>
