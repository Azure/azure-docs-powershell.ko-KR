---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: 8e102b6542e2e9b262224e73af7b0eb0ed49236a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192972"
---
# <span data-ttu-id="4678a-101">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="4678a-101">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>

## <span data-ttu-id="4678a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4678a-102">SYNOPSIS</span></span>

<span data-ttu-id="4678a-103">백업된 항목에 대한 복구 지점을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4678a-103">Gets the recovery points for a backed up item.</span></span>

## <span data-ttu-id="4678a-104">구문</span><span class="sxs-lookup"><span data-stu-id="4678a-104">SYNTAX</span></span>

### <span data-ttu-id="4678a-105">NoFilterParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="4678a-105">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-UseSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4678a-106">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="4678a-106">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>] [-Item] <ItemBase>
 [-UseSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4678a-107">RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="4678a-107">RecoveryPointId</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-UseSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4678a-108">설명</span><span class="sxs-lookup"><span data-stu-id="4678a-108">DESCRIPTION</span></span>

<span data-ttu-id="4678a-109">**Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet은 백업된 Azure Backup 항목에 대한 복구 지점을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4678a-109">The **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="4678a-110">항목이 백업된 후 **AzureRmRecoveryServicesBackupRecoveryPoint** 개체에는 하나 이상의 복구 지점이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4678a-110">After an item has been backed up, an **AzureRmRecoveryServicesBackupRecoveryPoint** object has one or more recovery points.</span></span>
<span data-ttu-id="4678a-111">-VaultId 매개 변수를 사용하여 자격 증명 모음 컨텍스트를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4678a-111">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="4678a-112">예제</span><span class="sxs-lookup"><span data-stu-id="4678a-112">EXAMPLES</span></span>

### <span data-ttu-id="4678a-113">예제 1: 항목에 대한 지난 주의 복구 지점을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4678a-113">Example 1: Get recovery points from the last week for an item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime() -VaultId $vault.ID
```

<span data-ttu-id="4678a-114">첫 번째 명령은 vaultName에 따라 자격 증명 모음 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4678a-114">The first command gets vault object based on vaultName.</span></span> <span data-ttu-id="4678a-115">두 번째 명령은 7일 전에 날짜를 인용한 다음, $StartDate 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="4678a-115">The second command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="4678a-116">세 번째 명령은 오늘 날짜를 인용한 다음, $EndDate 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="4678a-116">The third command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="4678a-117">네 번째 명령은 AzureVM 백업 컨테이너를 구하고 해당 컨테이너를 $Container 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="4678a-117">The fourth command gets AzureVM backup containers, and stores them in the $Container variable.</span></span> <span data-ttu-id="4678a-118">다섯 번째 명령은 workloadType, vaultId에 따라 백업 항목을 10진수 $BackupItem 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="4678a-118">The fifth command gets the backup item based on workloadType, vaultId and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="4678a-119">마지막 명령은 $BackupItem 항목의 복구 지점 배열을 $RP 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="4678a-119">The last command gets an array of recovery points for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="4678a-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4678a-120">PARAMETERS</span></span>

### <span data-ttu-id="4678a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4678a-121">-DefaultProfile</span></span>

<span data-ttu-id="4678a-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4678a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4678a-123">-EndDate</span><span class="sxs-lookup"><span data-stu-id="4678a-123">-EndDate</span></span>

<span data-ttu-id="4678a-124">날짜 범위의 끝을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4678a-124">Specifies the end of the date range.</span></span>

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

### <span data-ttu-id="4678a-125">-Item</span><span class="sxs-lookup"><span data-stu-id="4678a-125">-Item</span></span>

<span data-ttu-id="4678a-126">이 cmdlet이 복구 지점을 얻을 항목을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4678a-126">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="4678a-127">**AzureRmRecoveryServicesBackupItem** 개체를 얻습니다. **Get-AzRecoveryServicesBackupItem** cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="4678a-127">To obtain an **AzureRmRecoveryServicesBackupItem** object, use the **Get-AzRecoveryServicesBackupItem** cmdlet.</span></span>

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

### <span data-ttu-id="4678a-128">-KeyFileDownloadLocation</span><span class="sxs-lookup"><span data-stu-id="4678a-128">-KeyFileDownloadLocation</span></span>

<span data-ttu-id="4678a-129">암호화된 가상 머신에 대한 KeyVault 키를 복원하기 위해 입력 파일을 다운로드할 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4678a-129">Specifies the location to download the input file to restore the KeyVault key for an encrypted virtual machine.</span></span>

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

### <span data-ttu-id="4678a-130">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="4678a-130">-RecoveryPointId</span></span>

<span data-ttu-id="4678a-131">복구 지점 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4678a-131">Specifies the recovery point ID.</span></span>

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

### <span data-ttu-id="4678a-132">-StartDate</span><span class="sxs-lookup"><span data-stu-id="4678a-132">-StartDate</span></span>

<span data-ttu-id="4678a-133">날짜 범위의 시작을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4678a-133">Specifies the start of the date range.</span></span>

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

### <span data-ttu-id="4678a-134">-VaultId</span><span class="sxs-lookup"><span data-stu-id="4678a-134">-VaultId</span></span>

<span data-ttu-id="4678a-135">ARM 자격 증명 모음의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4678a-135">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="4678a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4678a-136">CommonParameters</span></span>
<span data-ttu-id="4678a-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4678a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4678a-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4678a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4678a-139">입력</span><span class="sxs-lookup"><span data-stu-id="4678a-139">INPUTS</span></span>

### <span data-ttu-id="4678a-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="4678a-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="4678a-141">System.String</span><span class="sxs-lookup"><span data-stu-id="4678a-141">System.String</span></span>

## <span data-ttu-id="4678a-142">출력</span><span class="sxs-lookup"><span data-stu-id="4678a-142">OUTPUTS</span></span>

### <span data-ttu-id="4678a-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="4678a-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="4678a-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4678a-144">NOTES</span></span>

## <span data-ttu-id="4678a-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4678a-145">RELATED LINKS</span></span>

[<span data-ttu-id="4678a-146">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="4678a-146">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="4678a-147">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="4678a-147">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)
