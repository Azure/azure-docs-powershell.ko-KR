---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: 676ba76cb4412e03c684be4d166e8707c5652b26
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217922"
---
# <span data-ttu-id="0c0b1-101">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="0c0b1-101">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>

## <span data-ttu-id="0c0b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c0b1-102">SYNOPSIS</span></span>

<span data-ttu-id="0c0b1-103">백업 항목에 대 한 복구 지점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0c0b1-103">Gets the recovery points for a backed up item.</span></span>

## <span data-ttu-id="0c0b1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0c0b1-104">SYNTAX</span></span>

### <span data-ttu-id="0c0b1-105">NoFilterParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="0c0b1-105">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c0b1-106">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="0c0b1-106">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>] [-Item] <ItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c0b1-107">RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="0c0b1-107">RecoveryPointId</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0c0b1-108">설명은</span><span class="sxs-lookup"><span data-stu-id="0c0b1-108">DESCRIPTION</span></span>

<span data-ttu-id="0c0b1-109">**AzRecoveryServicesBackupRecoveryPoint** cmdlet은 백업 된 Azure 백업 항목에 대 한 복구 지점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0c0b1-109">The **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="0c0b1-110">항목을 백업한 후 **AzureRmRecoveryServicesBackupRecoveryPoint** 개체에는 하나 이상의 복구 지점이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0c0b1-110">After an item has been backed up, an **AzureRmRecoveryServicesBackupRecoveryPoint** object has one or more recovery points.</span></span>
<span data-ttu-id="0c0b1-111">-VaultId 매개 변수를 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c0b1-111">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="0c0b1-112">예제의</span><span class="sxs-lookup"><span data-stu-id="0c0b1-112">EXAMPLES</span></span>

### <span data-ttu-id="0c0b1-113">예제 1: 항목에 대 한 지난 주의 복구 지점 가져오기</span><span class="sxs-lookup"><span data-stu-id="0c0b1-113">Example 1: Get recovery points from the last week for an item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime() -VaultId $vault.ID
```

<span data-ttu-id="0c0b1-114">첫 번째 명령은 vaultName에 따라 자격 증명 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0c0b1-114">The first command gets vault object based on vaultName.</span></span> <span data-ttu-id="0c0b1-115">두 번째 명령은 7 일 전 날짜를 가져온 다음 $StartDate 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c0b1-115">The second command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="0c0b1-116">세 번째 명령은 오늘 날짜를 가져온 다음 $EndDate 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c0b1-116">The third command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="0c0b1-117">네 번째 명령은 Add-azurevm 백업 컨테이너를 가져와 $Container 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c0b1-117">The fourth command gets AzureVM backup containers, and stores them in the $Container variable.</span></span> <span data-ttu-id="0c0b1-118">다섯 번째 명령은 workloadType, vaultId를 기반으로 하는 백업 항목을 가져온 다음이를 $BackupItem 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c0b1-118">The fifth command gets the backup item based on workloadType, vaultId and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="0c0b1-119">마지막 명령은 $BackupItem의 항목에 대 한 복구 지점 배열을 가져온 다음 $RP 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c0b1-119">The last command gets an array of recovery points for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="0c0b1-120">변수</span><span class="sxs-lookup"><span data-stu-id="0c0b1-120">PARAMETERS</span></span>

### <span data-ttu-id="0c0b1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c0b1-121">-DefaultProfile</span></span>

<span data-ttu-id="0c0b1-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0c0b1-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c0b1-123">-EndDate</span><span class="sxs-lookup"><span data-stu-id="0c0b1-123">-EndDate</span></span>

<span data-ttu-id="0c0b1-124">날짜 범위의 끝을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c0b1-124">Specifies the end of the date range.</span></span>

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

### <span data-ttu-id="0c0b1-125">-항목</span><span class="sxs-lookup"><span data-stu-id="0c0b1-125">-Item</span></span>

<span data-ttu-id="0c0b1-126">이 cmdlet이 복구 지점을 가져오는 항목을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c0b1-126">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="0c0b1-127">**AzureRmRecoveryServicesBackupItem** 개체를 얻으려면 **Get-AzRecoveryServicesBackupItem** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c0b1-127">To obtain an **AzureRmRecoveryServicesBackupItem** object, use the **Get-AzRecoveryServicesBackupItem** cmdlet.</span></span>

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

### <span data-ttu-id="0c0b1-128">-KeyFileDownloadLocation</span><span class="sxs-lookup"><span data-stu-id="0c0b1-128">-KeyFileDownloadLocation</span></span>

<span data-ttu-id="0c0b1-129">암호화 된 가상 컴퓨터에 대 한 KeyVault 키를 복원 하기 위해 입력 파일을 다운로드할 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c0b1-129">Specifies the location to download the input file to restore the KeyVault key for an encrypted virtual machine.</span></span>

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

### <span data-ttu-id="0c0b1-130">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="0c0b1-130">-RecoveryPointId</span></span>

<span data-ttu-id="0c0b1-131">복구 지점의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c0b1-131">Specifies the recovery point ID.</span></span>

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

### <span data-ttu-id="0c0b1-132">-시작 날짜</span><span class="sxs-lookup"><span data-stu-id="0c0b1-132">-StartDate</span></span>

<span data-ttu-id="0c0b1-133">날짜 범위의 시작을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c0b1-133">Specifies the start of the date range.</span></span>

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

### <span data-ttu-id="0c0b1-134">-VaultId</span><span class="sxs-lookup"><span data-stu-id="0c0b1-134">-VaultId</span></span>

<span data-ttu-id="0c0b1-135">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0c0b1-135">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="0c0b1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c0b1-136">CommonParameters</span></span>
<span data-ttu-id="0c0b1-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c0b1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c0b1-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0c0b1-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c0b1-139">입력</span><span class="sxs-lookup"><span data-stu-id="0c0b1-139">INPUTS</span></span>

### <span data-ttu-id="0c0b1-140">Microsoft Azure.. i g i..</span><span class="sxs-lookup"><span data-stu-id="0c0b1-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="0c0b1-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0c0b1-141">System.String</span></span>

## <span data-ttu-id="0c0b1-142">출력</span><span class="sxs-lookup"><span data-stu-id="0c0b1-142">OUTPUTS</span></span>

### <span data-ttu-id="0c0b1-143">RecoveryPointBase에서. i. i m/.</span><span class="sxs-lookup"><span data-stu-id="0c0b1-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="0c0b1-144">상속자</span><span class="sxs-lookup"><span data-stu-id="0c0b1-144">NOTES</span></span>

## <span data-ttu-id="0c0b1-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0c0b1-145">RELATED LINKS</span></span>

[<span data-ttu-id="0c0b1-146">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="0c0b1-146">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="0c0b1-147">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="0c0b1-147">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)
