---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 2dfc4b8fd0491a9f8c2200876609ab0a8cb00cce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872710"
---
# <span data-ttu-id="4aff2-101">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="4aff2-101">Get-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="4aff2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4aff2-102">SYNOPSIS</span></span>

<span data-ttu-id="4aff2-103">백업의 컨테이너에서 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4aff2-103">Gets the items from a container in Backup.</span></span>

## <span data-ttu-id="4aff2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4aff2-104">SYNTAX</span></span>

### <span data-ttu-id="4aff2-105">Get항목 Forcontainer (기본값)</span><span class="sxs-lookup"><span data-stu-id="4aff2-105">GetItemsForContainer (Default)</span></span>

```
Get-AzRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4aff2-106">Get항목 Forvault</span><span class="sxs-lookup"><span data-stu-id="4aff2-106">GetItemsForVault</span></span>

```
Get-AzRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4aff2-107">Get항목 Forpolicy</span><span class="sxs-lookup"><span data-stu-id="4aff2-107">GetItemsForPolicy</span></span>

```
Get-AzRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>] [[-DeleteState] <ItemDeleteState>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4aff2-108">설명은</span><span class="sxs-lookup"><span data-stu-id="4aff2-108">DESCRIPTION</span></span>

<span data-ttu-id="4aff2-109">**AzRecoveryServicesBackupItem** cmdlet은 컨테이너의 항목 또는 Azure Backup의 값과 항목의 보호 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4aff2-109">The **Get-AzRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="4aff2-110">Azure Recovery Services 자격 증명 모음에 등록 된 컨테이너에는 보호할 수 있는 항목이 하나 이상 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4aff2-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="4aff2-111">Azure 가상 컴퓨터의 경우 가상 컴퓨터 컨테이너에 백업 항목이 하나만 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4aff2-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="4aff2-112">-VaultId 매개 변수를 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aff2-112">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="4aff2-113">예제의</span><span class="sxs-lookup"><span data-stu-id="4aff2-113">EXAMPLES</span></span>

### <span data-ttu-id="4aff2-114">예제 1: 백업 컨테이너에서 항목 가져오기</span><span class="sxs-lookup"><span data-stu-id="4aff2-114">Example 1: Get an item from a Backup container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM -VaultId $vault.ID
```

<span data-ttu-id="4aff2-115">첫 번째 명령은 Add-azurevm 형식의 컨테이너를 가져온 다음 $Container 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aff2-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="4aff2-116">두 번째 명령은 $Container에서 V2VM 이라는 이름의 백업 항목을 가져온 다음 $BackupItem 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aff2-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

## <span data-ttu-id="4aff2-117">변수</span><span class="sxs-lookup"><span data-stu-id="4aff2-117">PARAMETERS</span></span>

### <span data-ttu-id="4aff2-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="4aff2-118">-BackupManagementType</span></span>

<span data-ttu-id="4aff2-119">백업 관리 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aff2-119">Specifies the Backup management type.</span></span>
<span data-ttu-id="4aff2-120">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4aff2-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4aff2-121">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="4aff2-121">AzureVM</span></span>
- <span data-ttu-id="4aff2-122">화성</span><span class="sxs-lookup"><span data-stu-id="4aff2-122">MARS</span></span>
- <span data-ttu-id="4aff2-123">SCDPM</span><span class="sxs-lookup"><span data-stu-id="4aff2-123">SCDPM</span></span>
- <span data-ttu-id="4aff2-124">AzureBackupServer</span><span class="sxs-lookup"><span data-stu-id="4aff2-124">AzureBackupServer</span></span>
- <span data-ttu-id="4aff2-125">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="4aff2-125">AzureSQL</span></span>
- <span data-ttu-id="4aff2-126">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="4aff2-126">AzureStorage</span></span>
- <span data-ttu-id="4aff2-127">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="4aff2-127">AzureWorkload</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: GetItemsForVault
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4aff2-128">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="4aff2-128">-Container</span></span>

<span data-ttu-id="4aff2-129">이 cmdlet에서 백업 항목을 가져오는 컨테이너 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aff2-129">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="4aff2-130">**AzureRmRecoveryServicesBackupContainer** 을 얻으려면 **AzRecoveryServicesBackupContainer** cmdlet을 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="4aff2-130">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the **Get-AzRecoveryServicesBackupContainer** cmdlet.</span></span>

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

### <span data-ttu-id="4aff2-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aff2-131">-DefaultProfile</span></span>

<span data-ttu-id="4aff2-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4aff2-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4aff2-133">-DeleteState</span><span class="sxs-lookup"><span data-stu-id="4aff2-133">-DeleteState</span></span>
<span data-ttu-id="4aff2-134">항목의 deletestate를 지정 합니다 .이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4aff2-134">Specifies the deletestate of the item The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4aff2-135">ToBeDeleted</span><span class="sxs-lookup"><span data-stu-id="4aff2-135">ToBeDeleted</span></span>
- <span data-ttu-id="4aff2-136">NotDeleted</span><span class="sxs-lookup"><span data-stu-id="4aff2-136">NotDeleted</span></span>

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

### <span data-ttu-id="4aff2-137">-이름</span><span class="sxs-lookup"><span data-stu-id="4aff2-137">-Name</span></span>

<span data-ttu-id="4aff2-138">컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aff2-138">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="4aff2-139">-정책</span><span class="sxs-lookup"><span data-stu-id="4aff2-139">-Policy</span></span>

<span data-ttu-id="4aff2-140">보호 정책 개체.</span><span class="sxs-lookup"><span data-stu-id="4aff2-140">Protection policy object.</span></span>

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

### <span data-ttu-id="4aff2-141">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="4aff2-141">-ProtectionState</span></span>

<span data-ttu-id="4aff2-142">보호 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aff2-142">Specifies the state of protection.</span></span>
<span data-ttu-id="4aff2-143">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4aff2-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4aff2-144">IRPending.</span><span class="sxs-lookup"><span data-stu-id="4aff2-144">IRPending.</span></span>
<span data-ttu-id="4aff2-145">초기 동기화가 시작 되지 않고 아직 복구 지점이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="4aff2-145">Initial synchronization has not started and there is no recovery point yet.</span></span>
- <span data-ttu-id="4aff2-146">됨.</span><span class="sxs-lookup"><span data-stu-id="4aff2-146">Protected.</span></span>
<span data-ttu-id="4aff2-147">보호가 진행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="4aff2-147">Protection is ongoing.</span></span>
- <span data-ttu-id="4aff2-148">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="4aff2-148">ProtectionError.</span></span>
<span data-ttu-id="4aff2-149">보호 오류가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4aff2-149">There is a protection error.</span></span>
- <span data-ttu-id="4aff2-150">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="4aff2-150">ProtectionStopped.</span></span>
<span data-ttu-id="4aff2-151">보호를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="4aff2-151">Protection is disabled.</span></span>

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

### <span data-ttu-id="4aff2-152">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="4aff2-152">-ProtectionStatus</span></span>

<span data-ttu-id="4aff2-153">컨테이너에 있는 항목의 전체 보호 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aff2-153">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="4aff2-154">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4aff2-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4aff2-155">손상</span><span class="sxs-lookup"><span data-stu-id="4aff2-155">Healthy</span></span>
- <span data-ttu-id="4aff2-156">상태임</span><span class="sxs-lookup"><span data-stu-id="4aff2-156">Unhealthy</span></span>

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

### <span data-ttu-id="4aff2-157">-VaultId</span><span class="sxs-lookup"><span data-stu-id="4aff2-157">-VaultId</span></span>

<span data-ttu-id="4aff2-158">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4aff2-158">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="4aff2-159">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="4aff2-159">-WorkloadType</span></span>

<span data-ttu-id="4aff2-160">작업 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aff2-160">Specifies the workload type.</span></span>
<span data-ttu-id="4aff2-161">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4aff2-161">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4aff2-162">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="4aff2-162">AzureVM</span></span>
- <span data-ttu-id="4aff2-163">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="4aff2-163">AzureSQLDatabase</span></span>
- <span data-ttu-id="4aff2-164">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="4aff2-164">AzureFiles</span></span>
- <span data-ttu-id="4aff2-165">원인은</span><span class="sxs-lookup"><span data-stu-id="4aff2-165">MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: GetItemsForContainer, GetItemsForVault
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4aff2-166">-CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aff2-166">-CommonParameters</span></span>

<span data-ttu-id="4aff2-167">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aff2-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aff2-168">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4aff2-168">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aff2-169">입력</span><span class="sxs-lookup"><span data-stu-id="4aff2-169">INPUTS</span></span>

### <span data-ttu-id="4aff2-170">ContainerBase에서. i. i m/.</span><span class="sxs-lookup"><span data-stu-id="4aff2-170">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="4aff2-171">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4aff2-171">System.String</span></span>

## <span data-ttu-id="4aff2-172">출력</span><span class="sxs-lookup"><span data-stu-id="4aff2-172">OUTPUTS</span></span>

### <span data-ttu-id="4aff2-173">Microsoft Azure.. i g i..</span><span class="sxs-lookup"><span data-stu-id="4aff2-173">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="4aff2-174">상속자</span><span class="sxs-lookup"><span data-stu-id="4aff2-174">NOTES</span></span>

## <span data-ttu-id="4aff2-175">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4aff2-175">RELATED LINKS</span></span>

[<span data-ttu-id="4aff2-176">백업-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="4aff2-176">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="4aff2-177">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="4aff2-177">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="4aff2-178">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="4aff2-178">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="4aff2-179">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="4aff2-179">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
