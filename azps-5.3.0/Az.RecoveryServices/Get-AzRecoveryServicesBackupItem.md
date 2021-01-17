---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 429e0801cc0c003aa1ffdb7080caada8e8d07517
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491703"
---
# <span data-ttu-id="3df50-101">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="3df50-101">Get-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="3df50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3df50-102">SYNOPSIS</span></span>

<span data-ttu-id="3df50-103">Backup의 컨테이너에서 항목을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3df50-103">Gets the items from a container in Backup.</span></span>

## <span data-ttu-id="3df50-104">구문</span><span class="sxs-lookup"><span data-stu-id="3df50-104">SYNTAX</span></span>

### <span data-ttu-id="3df50-105">GetItemsForContainer(기본값)</span><span class="sxs-lookup"><span data-stu-id="3df50-105">GetItemsForContainer (Default)</span></span>
```
Get-AzRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3df50-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="3df50-106">GetItemsForVault</span></span>
```
Get-AzRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3df50-107">GetItemsForPolicy</span><span class="sxs-lookup"><span data-stu-id="3df50-107">GetItemsForPolicy</span></span>
```
Get-AzRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3df50-108">설명</span><span class="sxs-lookup"><span data-stu-id="3df50-108">DESCRIPTION</span></span>

<span data-ttu-id="3df50-109">**Get-AzRecoveryServicesBackupItem** cmdlet은 컨테이너의 보호된 항목 목록과 항목의 보호 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3df50-109">The **Get-AzRecoveryServicesBackupItem** cmdlet gets the list of protected items in a container and the protection status of the items.</span></span>
<span data-ttu-id="3df50-110">Azure Recovery Services 자격 증명 모음에 등록된 컨테이너에는 보호할 수 있는 하나 이상의 항목이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3df50-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="3df50-111">Azure 가상 머신의 경우 가상 머신 컨테이너에 하나의 백업 항목만 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3df50-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="3df50-112">-VaultId 매개 변수를 사용하여 자격 증명 모음 컨텍스트를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="3df50-112">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="3df50-113">예제</span><span class="sxs-lookup"><span data-stu-id="3df50-113">EXAMPLES</span></span>

### <span data-ttu-id="3df50-114">예제 1: Backup 컨테이너에서 항목 얻기</span><span class="sxs-lookup"><span data-stu-id="3df50-114">Example 1: Get an item from a Backup container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -FriendlyName "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM -VaultId $vault.ID
```

<span data-ttu-id="3df50-115">첫 번째 명령은 AzureVM 형식의 컨테이너를 인용한 다음, $Container 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="3df50-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="3df50-116">두 번째 명령은 V2VM이라는 Backup 항목을 $Container V2VM을 $BackupItem 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="3df50-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

### <span data-ttu-id="3df50-117">예제 2: FriendlyName에서 Azure 파일 공유 항목 다운로드</span><span class="sxs-lookup"><span data-stu-id="3df50-117">Example 2: Get an Azure File Share Item from FriendlyName</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureStorage -Status Registered -FriendlyName "StorageAccount1" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureFiles -VaultId $vault.ID -FriendlyName "FileShareName"
```

<span data-ttu-id="3df50-118">첫 번째 명령은 AzureStorage 형식의 컨테이너를 구한 다음, $Container 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="3df50-118">The first command gets the container of type AzureStorage, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="3df50-119">두 번째 명령은 friendlyName이 FriendlyName 매개 변수에 전달된 값과 일치하는 Backup 항목을 $BackupItem 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="3df50-119">The second command gets the Backup item whose friendlyName matches the value passed in FriendlyName Parameter, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="3df50-120">FriendlyName 매개 변수를 사용하면 Azure 파일 공유가 두 개 이상 반환될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3df50-120">Using FriendlyName parameter can result in returning more than one Azure File Share.</span></span> <span data-ttu-id="3df50-121">이러한 경우 -Name 매개 변수에 대한 값을 이름 매개 변수의 결과 집합에 반환된 Name 속성으로 전달하여 cmdlet을 $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="3df50-121">In such cases, execute the cmdlet by passing value for -Name parameter as the Name property returned in the result set of $BackupItem.</span></span>

## <span data-ttu-id="3df50-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3df50-122">PARAMETERS</span></span>

### <span data-ttu-id="3df50-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="3df50-123">-BackupManagementType</span></span>

<span data-ttu-id="3df50-124">보호되는 리소스의 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="3df50-124">The class of resources being protected.</span></span> <span data-ttu-id="3df50-125">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="3df50-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3df50-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="3df50-126">AzureVM</span></span>
- <span data-ttu-id="3df50-127">MAB</span><span class="sxs-lookup"><span data-stu-id="3df50-127">MAB</span></span>
- <span data-ttu-id="3df50-128">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="3df50-128">AzureStorage</span></span>
- <span data-ttu-id="3df50-129">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="3df50-129">AzureWorkload</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: GetItemsForVault
Aliases:
Accepted values: AzureVM, MARS, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3df50-130">-Container</span><span class="sxs-lookup"><span data-stu-id="3df50-130">-Container</span></span>

<span data-ttu-id="3df50-131">이 cmdlet이 백업 항목을 얻을 컨테이너 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3df50-131">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="3df50-132">**AzureRmRecoveryServicesBackupContainer를** 얻습니다. **Get-AzRecoveryServicesBackupContainer** cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="3df50-132">To obtain an **AzureRmRecoveryServicesBackupContainer**, use the **Get-AzRecoveryServicesBackupContainer** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: GetItemsForContainer
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3df50-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3df50-133">-DefaultProfile</span></span>

<span data-ttu-id="3df50-134">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3df50-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3df50-135">-DeleteState</span><span class="sxs-lookup"><span data-stu-id="3df50-135">-DeleteState</span></span>
<span data-ttu-id="3df50-136">항목의 삭제를 지정합니다. 이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="3df50-136">Specifies the deletestate of the item The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3df50-137">ToBeDeleted</span><span class="sxs-lookup"><span data-stu-id="3df50-137">ToBeDeleted</span></span>
- <span data-ttu-id="3df50-138">NotDeleted</span><span class="sxs-lookup"><span data-stu-id="3df50-138">NotDeleted</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemDeleteState
Parameter Sets: (All)
Aliases:
Accepted values: ToBeDeleted, NotDeleted

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3df50-139">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="3df50-139">-FriendlyName</span></span>
<span data-ttu-id="3df50-140">백업된 항목의 FriendlyName</span><span class="sxs-lookup"><span data-stu-id="3df50-140">FriendlyName of the backed up item</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3df50-141">-Name</span><span class="sxs-lookup"><span data-stu-id="3df50-141">-Name</span></span>

<span data-ttu-id="3df50-142">백업 항목의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3df50-142">Specifies the name of backup item.</span></span> <span data-ttu-id="3df50-143">파일 공유의 경우 보호된 파일 공유의 고유 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3df50-143">For file share, specify the unique ID of protected file share.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3df50-144">-Policy</span><span class="sxs-lookup"><span data-stu-id="3df50-144">-Policy</span></span>

<span data-ttu-id="3df50-145">보호 정책 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3df50-145">Protection policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: GetItemsForPolicy
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3df50-146">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="3df50-146">-ProtectionState</span></span>

<span data-ttu-id="3df50-147">보호 상태를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3df50-147">Specifies the state of protection.</span></span>
<span data-ttu-id="3df50-148">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="3df50-148">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3df50-149">IRPending.</span><span class="sxs-lookup"><span data-stu-id="3df50-149">IRPending.</span></span>
<span data-ttu-id="3df50-150">초기 동기화가 시작되지 않았고 아직 복구 지점이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="3df50-150">Initial synchronization has not started and there is no recovery point yet.</span></span>
- <span data-ttu-id="3df50-151">보호됩니다.</span><span class="sxs-lookup"><span data-stu-id="3df50-151">Protected.</span></span>
<span data-ttu-id="3df50-152">보호가 진행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="3df50-152">Protection is ongoing.</span></span>
- <span data-ttu-id="3df50-153">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="3df50-153">ProtectionError.</span></span>
<span data-ttu-id="3df50-154">보호 오류가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3df50-154">There is a protection error.</span></span>
- <span data-ttu-id="3df50-155">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="3df50-155">ProtectionStopped.</span></span>
<span data-ttu-id="3df50-156">보호를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="3df50-156">Protection is disabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemProtectionState
Parameter Sets: (All)
Aliases:
Accepted values: IRPending, ProtectionError, Protected, ProtectionStopped

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3df50-157">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="3df50-157">-ProtectionStatus</span></span>

<span data-ttu-id="3df50-158">컨테이너에 있는 항목의 전체 보호 상태를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3df50-158">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="3df50-159">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="3df50-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3df50-160">정상</span><span class="sxs-lookup"><span data-stu-id="3df50-160">Healthy</span></span>
- <span data-ttu-id="3df50-161">Unhealthy</span><span class="sxs-lookup"><span data-stu-id="3df50-161">Unhealthy</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemProtectionStatus
Parameter Sets: (All)
Aliases:
Accepted values: Healthy, Unhealthy

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3df50-162">-VaultId</span><span class="sxs-lookup"><span data-stu-id="3df50-162">-VaultId</span></span>

<span data-ttu-id="3df50-163">ARM 자격 증명 모음의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3df50-163">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="3df50-164">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="3df50-164">-WorkloadType</span></span>

<span data-ttu-id="3df50-165">리소스의 워크로드 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="3df50-165">Workload type of the resource.</span></span> <span data-ttu-id="3df50-166">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="3df50-166">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3df50-167">AzureVM</span><span class="sxs-lookup"><span data-stu-id="3df50-167">AzureVM</span></span>
- <span data-ttu-id="3df50-168">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="3df50-168">AzureFiles</span></span>
- <span data-ttu-id="3df50-169">MSSQL</span><span class="sxs-lookup"><span data-stu-id="3df50-169">MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: GetItemsForContainer, GetItemsForVault
Aliases:
Accepted values: AzureVM, AzureFiles, MSSQL

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3df50-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3df50-170">CommonParameters</span></span>
<span data-ttu-id="3df50-171">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3df50-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3df50-172">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3df50-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3df50-173">입력</span><span class="sxs-lookup"><span data-stu-id="3df50-173">INPUTS</span></span>

### <span data-ttu-id="3df50-174">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span><span class="sxs-lookup"><span data-stu-id="3df50-174">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="3df50-175">System.String</span><span class="sxs-lookup"><span data-stu-id="3df50-175">System.String</span></span>

## <span data-ttu-id="3df50-176">출력</span><span class="sxs-lookup"><span data-stu-id="3df50-176">OUTPUTS</span></span>

### <span data-ttu-id="3df50-177">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="3df50-177">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="3df50-178">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3df50-178">NOTES</span></span>

## <span data-ttu-id="3df50-179">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3df50-179">RELATED LINKS</span></span>

[<span data-ttu-id="3df50-180">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="3df50-180">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="3df50-181">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="3df50-181">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="3df50-182">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="3df50-182">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="3df50-183">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="3df50-183">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
