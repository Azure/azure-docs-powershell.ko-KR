---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: 9a5d0f0607692217cf4016a1261f23b725d07e68
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699692"
---
# <span data-ttu-id="23513-101">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="23513-101">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>

## <span data-ttu-id="23513-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23513-102">SYNOPSIS</span></span>
<span data-ttu-id="23513-103">백업 항목에 대 한 복구 지점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="23513-103">Gets the recovery points for a backed up item.</span></span>

## <span data-ttu-id="23513-104">구문과</span><span class="sxs-lookup"><span data-stu-id="23513-104">SYNTAX</span></span>

### <span data-ttu-id="23513-105">NoFilterParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="23513-105">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23513-106">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="23513-106">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>] [-Item] <ItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23513-107">RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="23513-107">RecoveryPointId</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="23513-108">설명은</span><span class="sxs-lookup"><span data-stu-id="23513-108">DESCRIPTION</span></span>
<span data-ttu-id="23513-109">**AzRecoveryServicesBackupRecoveryPoint** cmdlet은 백업 된 Azure 백업 항목에 대 한 복구 지점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="23513-109">The **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="23513-110">항목을 백업한 후 **AzureRmRecoveryServicesBackupRecoveryPoint** 개체에는 하나 이상의 복구 지점이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="23513-110">After an item has been backed up, an **AzureRmRecoveryServicesBackupRecoveryPoint** object has one or more recovery points.</span></span>
<span data-ttu-id="23513-111">현재 cmdlet을 사용 하기 전에 Set-AzRecoveryServicesVaultContext cmdlet을 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23513-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="23513-112">예제의</span><span class="sxs-lookup"><span data-stu-id="23513-112">EXAMPLES</span></span>

### <span data-ttu-id="23513-113">예제 1: 항목에 대 한 지난 주의 복구 지점 가져오기</span><span class="sxs-lookup"><span data-stu-id="23513-113">Example 1: Get recovery points from the last week for an item</span></span>
```
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM 
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="23513-114">첫 번째 명령은 7 일 전 날짜를 가져온 다음 $StartDate 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="23513-114">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="23513-115">두 번째 명령은 오늘 날짜를 가져온 다음 $EndDate 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="23513-115">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="23513-116">세 번째 명령은 Add-azurevm 백업 컨테이너를 가져와 $Containers 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="23513-116">The third command gets AzureVM backup containers, and stores them in the $Containers variable.</span></span>
<span data-ttu-id="23513-117">네 번째 명령은 V2VM 이라는 백업 항목을 가져온 다음이를 $BackupItem 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="23513-117">The fourth command gets the backup item named V2VM, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="23513-118">마지막 명령은 $BackupItem의 항목에 대 한 복구 지점 배열을 가져온 다음 $RP 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="23513-118">The last command gets an array of recovery points for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="23513-119">변수</span><span class="sxs-lookup"><span data-stu-id="23513-119">PARAMETERS</span></span>

### <span data-ttu-id="23513-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23513-120">-DefaultProfile</span></span>
<span data-ttu-id="23513-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="23513-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23513-122">-EndDate</span><span class="sxs-lookup"><span data-stu-id="23513-122">-EndDate</span></span>
<span data-ttu-id="23513-123">날짜 범위의 끝을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23513-123">Specifies the end of the date range.</span></span>

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

### <span data-ttu-id="23513-124">-항목</span><span class="sxs-lookup"><span data-stu-id="23513-124">-Item</span></span>
<span data-ttu-id="23513-125">이 cmdlet이 복구 지점을 가져오는 항목을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23513-125">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="23513-126">**AzureRmRecoveryServicesBackupItem** 개체를 가져오려면 Get-AzRecoveryServicesBackupItem cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="23513-126">To obtain an **AzureRmRecoveryServicesBackupItem** object, use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="23513-127">-KeyFileDownloadLocation</span><span class="sxs-lookup"><span data-stu-id="23513-127">-KeyFileDownloadLocation</span></span>
<span data-ttu-id="23513-128">암호화 된 가상 컴퓨터에 대 한 KeyVault 키를 복원 하기 위해 입력 파일을 다운로드할 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23513-128">Specifies the location to download the input file to restore the KeyVault key for an encrypted virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RecoveryPointId
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23513-129">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="23513-129">-RecoveryPointId</span></span>
<span data-ttu-id="23513-130">복구 지점의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23513-130">Specifies the recovery point ID.</span></span>

```yaml
Type: System.String
Parameter Sets: RecoveryPointId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23513-131">-시작 날짜</span><span class="sxs-lookup"><span data-stu-id="23513-131">-StartDate</span></span>
<span data-ttu-id="23513-132">날짜 범위의 시작을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23513-132">Specifies the start of the date range.</span></span>

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

### <span data-ttu-id="23513-133">-VaultId</span><span class="sxs-lookup"><span data-stu-id="23513-133">-VaultId</span></span>
<span data-ttu-id="23513-134">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="23513-134">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="23513-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23513-135">CommonParameters</span></span>
<span data-ttu-id="23513-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="23513-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23513-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23513-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23513-138">입력</span><span class="sxs-lookup"><span data-stu-id="23513-138">INPUTS</span></span>

### <span data-ttu-id="23513-139">Microsoft Azure.. i g i..</span><span class="sxs-lookup"><span data-stu-id="23513-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="23513-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="23513-140">System.String</span></span>

## <span data-ttu-id="23513-141">출력</span><span class="sxs-lookup"><span data-stu-id="23513-141">OUTPUTS</span></span>

### <span data-ttu-id="23513-142">RecoveryPointBase에서. i. i m/.</span><span class="sxs-lookup"><span data-stu-id="23513-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="23513-143">상속자</span><span class="sxs-lookup"><span data-stu-id="23513-143">NOTES</span></span>

## <span data-ttu-id="23513-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="23513-144">RELATED LINKS</span></span>

[<span data-ttu-id="23513-145">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="23513-145">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="23513-146">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="23513-146">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

