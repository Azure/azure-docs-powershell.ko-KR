---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 358d3da36996c9b020db3a805889b7098b9c36ec
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214702"
---
# <span data-ttu-id="37dab-101">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="37dab-101">Get-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="37dab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37dab-102">SYNOPSIS</span></span>

<span data-ttu-id="37dab-103">백업의 컨테이너에서 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="37dab-103">Gets the items from a container in Backup.</span></span>

## <span data-ttu-id="37dab-104">구문과</span><span class="sxs-lookup"><span data-stu-id="37dab-104">SYNTAX</span></span>

### <span data-ttu-id="37dab-105">Get항목 Forcontainer (기본값)</span><span class="sxs-lookup"><span data-stu-id="37dab-105">GetItemsForContainer (Default)</span></span>
```
Get-AzRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37dab-106">Get항목 Forvault</span><span class="sxs-lookup"><span data-stu-id="37dab-106">GetItemsForVault</span></span>
```
Get-AzRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37dab-107">Get항목 Forpolicy</span><span class="sxs-lookup"><span data-stu-id="37dab-107">GetItemsForPolicy</span></span>
```
Get-AzRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37dab-108">설명은</span><span class="sxs-lookup"><span data-stu-id="37dab-108">DESCRIPTION</span></span>

<span data-ttu-id="37dab-109">**AzRecoveryServicesBackupItem** cmdlet은 컨테이너의 보호 된 항목 목록과 항목의 보호 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="37dab-109">The **Get-AzRecoveryServicesBackupItem** cmdlet gets the list of protected items in a container and the protection status of the items.</span></span>
<span data-ttu-id="37dab-110">Azure Recovery Services 자격 증명 모음에 등록 된 컨테이너에는 보호할 수 있는 항목이 하나 이상 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37dab-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="37dab-111">Azure 가상 컴퓨터의 경우 가상 컴퓨터 컨테이너에 백업 항목이 하나만 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37dab-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="37dab-112">-VaultId 매개 변수를 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37dab-112">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="37dab-113">예제의</span><span class="sxs-lookup"><span data-stu-id="37dab-113">EXAMPLES</span></span>

### <span data-ttu-id="37dab-114">예제 1: 백업 컨테이너에서 항목 가져오기</span><span class="sxs-lookup"><span data-stu-id="37dab-114">Example 1: Get an item from a Backup container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM -VaultId $vault.ID
```

<span data-ttu-id="37dab-115">첫 번째 명령은 Add-azurevm 형식의 컨테이너를 가져온 다음 $Container 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="37dab-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="37dab-116">두 번째 명령은 $Container에서 V2VM 이라는 이름의 백업 항목을 가져온 다음 $BackupItem 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="37dab-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

### <span data-ttu-id="37dab-117">예제 2: FriendlyName에서 Azure 파일 공유 항목 가져오기</span><span class="sxs-lookup"><span data-stu-id="37dab-117">Example 2: Get an Azure File Share Item from FriendlyName</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureStorage -Status Registered -Name "StorageAccount1" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureFiles -VaultId $vault.ID -FriendlyName "FileShareName"
```

<span data-ttu-id="37dab-118">첫 번째 명령은 AzureStorage 형식의 컨테이너를 가져온 다음 $Container 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="37dab-118">The first command gets the container of type AzureStorage, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="37dab-119">두 번째 명령은 friendlyname 매개 변수에서 전달 된 값과 일치 하는 항목을 가져온 다음 $BackupItem 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="37dab-119">The second command gets the Backup item whose friendlyName matches the value passed in FriendlyName Parameter, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="37dab-120">FriendlyName 매개 변수를 사용 하면 둘 이상의 Azure 파일 공유가 반환 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37dab-120">Using FriendlyName parameter can result in returning more than one Azure File Share.</span></span> <span data-ttu-id="37dab-121">이러한 경우-Name 매개 변수에 대 한 값을 $BackupItem 결과 집합에 반환 되는 Name 속성으로 전달 하 여 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="37dab-121">In such cases, execute the cmdlet by passing value for -Name parameter as the Name property returned in the result set of $BackupItem.</span></span>

## <span data-ttu-id="37dab-122">변수</span><span class="sxs-lookup"><span data-stu-id="37dab-122">PARAMETERS</span></span>

### <span data-ttu-id="37dab-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="37dab-123">-BackupManagementType</span></span>

<span data-ttu-id="37dab-124">보호 되는 리소스의 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="37dab-124">The class of resources being protected.</span></span> <span data-ttu-id="37dab-125">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="37dab-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="37dab-126">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="37dab-126">AzureVM</span></span>
- <span data-ttu-id="37dab-127">MAB</span><span class="sxs-lookup"><span data-stu-id="37dab-127">MAB</span></span>
- <span data-ttu-id="37dab-128">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="37dab-128">AzureStorage</span></span>
- <span data-ttu-id="37dab-129">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="37dab-129">AzureWorkload</span></span>

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

### <span data-ttu-id="37dab-130">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="37dab-130">-Container</span></span>

<span data-ttu-id="37dab-131">이 cmdlet에서 백업 항목을 가져오는 컨테이너 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37dab-131">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="37dab-132">**AzureRmRecoveryServicesBackupContainer** 을 얻으려면 **AzRecoveryServicesBackupContainer** cmdlet을 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="37dab-132">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the **Get-AzRecoveryServicesBackupContainer** cmdlet.</span></span>

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

### <span data-ttu-id="37dab-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37dab-133">-DefaultProfile</span></span>

<span data-ttu-id="37dab-134">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="37dab-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37dab-135">-DeleteState</span><span class="sxs-lookup"><span data-stu-id="37dab-135">-DeleteState</span></span>
<span data-ttu-id="37dab-136">항목의 deletestate를 지정 합니다 .이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="37dab-136">Specifies the deletestate of the item The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="37dab-137">ToBeDeleted</span><span class="sxs-lookup"><span data-stu-id="37dab-137">ToBeDeleted</span></span>
- <span data-ttu-id="37dab-138">NotDeleted</span><span class="sxs-lookup"><span data-stu-id="37dab-138">NotDeleted</span></span>

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

### <span data-ttu-id="37dab-139">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="37dab-139">-FriendlyName</span></span>
<span data-ttu-id="37dab-140">백업 항목의 FriendlyName</span><span class="sxs-lookup"><span data-stu-id="37dab-140">FriendlyName of the backed up item</span></span>

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

### <span data-ttu-id="37dab-141">-이름</span><span class="sxs-lookup"><span data-stu-id="37dab-141">-Name</span></span>

<span data-ttu-id="37dab-142">백업 항목의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37dab-142">Specifies the name of backup item.</span></span> <span data-ttu-id="37dab-143">파일 공유의 경우 보호 된 파일 공유의 고유 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37dab-143">For file share, specify the unique ID of protected file share.</span></span>

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

### <span data-ttu-id="37dab-144">-정책</span><span class="sxs-lookup"><span data-stu-id="37dab-144">-Policy</span></span>

<span data-ttu-id="37dab-145">보호 정책 개체.</span><span class="sxs-lookup"><span data-stu-id="37dab-145">Protection policy object.</span></span>

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

### <span data-ttu-id="37dab-146">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="37dab-146">-ProtectionState</span></span>

<span data-ttu-id="37dab-147">보호 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37dab-147">Specifies the state of protection.</span></span>
<span data-ttu-id="37dab-148">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="37dab-148">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="37dab-149">IRPending.</span><span class="sxs-lookup"><span data-stu-id="37dab-149">IRPending.</span></span>
<span data-ttu-id="37dab-150">초기 동기화가 시작 되지 않고 아직 복구 지점이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="37dab-150">Initial synchronization has not started and there is no recovery point yet.</span></span>
- <span data-ttu-id="37dab-151">됨.</span><span class="sxs-lookup"><span data-stu-id="37dab-151">Protected.</span></span>
<span data-ttu-id="37dab-152">보호가 진행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="37dab-152">Protection is ongoing.</span></span>
- <span data-ttu-id="37dab-153">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="37dab-153">ProtectionError.</span></span>
<span data-ttu-id="37dab-154">보호 오류가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37dab-154">There is a protection error.</span></span>
- <span data-ttu-id="37dab-155">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="37dab-155">ProtectionStopped.</span></span>
<span data-ttu-id="37dab-156">보호를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="37dab-156">Protection is disabled.</span></span>

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

### <span data-ttu-id="37dab-157">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="37dab-157">-ProtectionStatus</span></span>

<span data-ttu-id="37dab-158">컨테이너에 있는 항목의 전체 보호 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37dab-158">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="37dab-159">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="37dab-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="37dab-160">손상</span><span class="sxs-lookup"><span data-stu-id="37dab-160">Healthy</span></span>
- <span data-ttu-id="37dab-161">상태임</span><span class="sxs-lookup"><span data-stu-id="37dab-161">Unhealthy</span></span>

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

### <span data-ttu-id="37dab-162">-VaultId</span><span class="sxs-lookup"><span data-stu-id="37dab-162">-VaultId</span></span>

<span data-ttu-id="37dab-163">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="37dab-163">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="37dab-164">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="37dab-164">-WorkloadType</span></span>

<span data-ttu-id="37dab-165">리소스의 작업 부하 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="37dab-165">Workload type of the resource.</span></span> <span data-ttu-id="37dab-166">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="37dab-166">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="37dab-167">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="37dab-167">AzureVM</span></span>
- <span data-ttu-id="37dab-168">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="37dab-168">AzureFiles</span></span>
- <span data-ttu-id="37dab-169">원인은</span><span class="sxs-lookup"><span data-stu-id="37dab-169">MSSQL</span></span>

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

### <span data-ttu-id="37dab-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37dab-170">CommonParameters</span></span>
<span data-ttu-id="37dab-171">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="37dab-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37dab-172">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="37dab-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37dab-173">입력</span><span class="sxs-lookup"><span data-stu-id="37dab-173">INPUTS</span></span>

### <span data-ttu-id="37dab-174">ContainerBase에서. i. i m/.</span><span class="sxs-lookup"><span data-stu-id="37dab-174">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="37dab-175">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="37dab-175">System.String</span></span>

## <span data-ttu-id="37dab-176">출력</span><span class="sxs-lookup"><span data-stu-id="37dab-176">OUTPUTS</span></span>

### <span data-ttu-id="37dab-177">Microsoft Azure.. i g i..</span><span class="sxs-lookup"><span data-stu-id="37dab-177">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="37dab-178">상속자</span><span class="sxs-lookup"><span data-stu-id="37dab-178">NOTES</span></span>

## <span data-ttu-id="37dab-179">관련 링크</span><span class="sxs-lookup"><span data-stu-id="37dab-179">RELATED LINKS</span></span>

[<span data-ttu-id="37dab-180">백업-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="37dab-180">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="37dab-181">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="37dab-181">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="37dab-182">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="37dab-182">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="37dab-183">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="37dab-183">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
