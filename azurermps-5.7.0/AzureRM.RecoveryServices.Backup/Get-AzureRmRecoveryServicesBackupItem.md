---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: 9b836a4c4c056699e2c74bcb4d5b373f5bfe170e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526719"
---
# <span data-ttu-id="d4d1d-101">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="d4d1d-101">Get-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="d4d1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4d1d-102">SYNOPSIS</span></span>
<span data-ttu-id="d4d1d-103">백업의 컨테이너에서 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d4d1d-103">Gets the items from a container in Backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4d1d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d4d1d-104">SYNTAX</span></span>

### <span data-ttu-id="d4d1d-105">Get항목 Forcontainer (기본값)</span><span class="sxs-lookup"><span data-stu-id="d4d1d-105">GetItemsForContainer (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4d1d-106">Get항목 Forvault</span><span class="sxs-lookup"><span data-stu-id="d4d1d-106">GetItemsForVault</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4d1d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d4d1d-107">DESCRIPTION</span></span>
<span data-ttu-id="d4d1d-108">**AzureRmRecoveryServicesBackupItem** cmdlet은 컨테이너의 항목 또는 Azure Backup의 값과 항목의 보호 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d4d1d-108">The **Get-AzureRmRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>

<span data-ttu-id="d4d1d-109">Azure Recovery Services 자격 증명 모음에 등록 된 컨테이너에는 보호할 수 있는 항목이 하나 이상 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4d1d-109">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="d4d1d-110">Azure 가상 컴퓨터의 경우 가상 컴퓨터 컨테이너에 백업 항목이 하나만 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4d1d-110">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>

<span data-ttu-id="d4d1d-111">현재 cmdlet을 사용 하기 전에 Set-AzureRmRecoveryServicesVaultContext cmdlet을 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4d1d-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="d4d1d-112">예제의</span><span class="sxs-lookup"><span data-stu-id="d4d1d-112">EXAMPLES</span></span>

### <span data-ttu-id="d4d1d-113">예제 1: 백업 컨테이너에서 항목 가져오기</span><span class="sxs-lookup"><span data-stu-id="d4d1d-113">Example 1: Get an item from a Backup container</span></span>
```
PS C:\>$Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM
```

<span data-ttu-id="d4d1d-114">첫 번째 명령은 Add-azurevm 형식의 컨테이너를 가져온 다음 $Container 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4d1d-114">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="d4d1d-115">두 번째 명령은 $Container에서 V2VM 이라는 이름의 백업 항목을 가져온 다음 $BackupItem 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4d1d-115">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

## <span data-ttu-id="d4d1d-116">변수</span><span class="sxs-lookup"><span data-stu-id="d4d1d-116">PARAMETERS</span></span>

### <span data-ttu-id="d4d1d-117">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="d4d1d-117">-BackupManagementType</span></span>
<span data-ttu-id="d4d1d-118">백업 관리 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4d1d-118">Specifies the Backup management type.</span></span>
<span data-ttu-id="d4d1d-119">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d4d1d-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d4d1d-120">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="d4d1d-120">AzureVM</span></span> 
- <span data-ttu-id="d4d1d-121">화성</span><span class="sxs-lookup"><span data-stu-id="d4d1d-121">MARS</span></span> 
- <span data-ttu-id="d4d1d-122">SCDPM</span><span class="sxs-lookup"><span data-stu-id="d4d1d-122">SCDPM</span></span> 
- <span data-ttu-id="d4d1d-123">AzureBackupServer AzureSQL</span><span class="sxs-lookup"><span data-stu-id="d4d1d-123">AzureBackupServer AzureSQL</span></span>

```yaml
Type: BackupManagementType
Parameter Sets: GetItemsForVault
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4d1d-124">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="d4d1d-124">-Container</span></span>
<span data-ttu-id="d4d1d-125">이 cmdlet에서 백업 항목을 가져오는 컨테이너 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4d1d-125">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="d4d1d-126">**AzureRmRecoveryServicesBackupContainer** 을 얻으려면 Get-AzureRmRecoveryServicesBackupContainer cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4d1d-126">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the Get-AzureRmRecoveryServicesBackupContainer cmdlet.</span></span>

```yaml
Type: ContainerBase
Parameter Sets: GetItemsForContainer
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4d1d-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4d1d-127">-DefaultProfile</span></span>
<span data-ttu-id="d4d1d-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d4d1d-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4d1d-129">-이름</span><span class="sxs-lookup"><span data-stu-id="d4d1d-129">-Name</span></span>
<span data-ttu-id="d4d1d-130">컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4d1d-130">Specifies the name of the container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4d1d-131">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="d4d1d-131">-ProtectionState</span></span>
<span data-ttu-id="d4d1d-132">보호 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4d1d-132">Specifies the state of protection.</span></span>
<span data-ttu-id="d4d1d-133">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d4d1d-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d4d1d-134">IRPending.</span><span class="sxs-lookup"><span data-stu-id="d4d1d-134">IRPending.</span></span>
<span data-ttu-id="d4d1d-135">초기 동기화가 시작 되지 않고 아직 복구 지점이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d4d1d-135">Initial synchronization has not started and there is no recovery point yet.</span></span> 
- <span data-ttu-id="d4d1d-136">됨.</span><span class="sxs-lookup"><span data-stu-id="d4d1d-136">Protected.</span></span>
<span data-ttu-id="d4d1d-137">보호가 진행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="d4d1d-137">Protection is ongoing.</span></span> 
- <span data-ttu-id="d4d1d-138">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="d4d1d-138">ProtectionError.</span></span>
<span data-ttu-id="d4d1d-139">보호 오류가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4d1d-139">There is a protection error.</span></span>
- <span data-ttu-id="d4d1d-140">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="d4d1d-140">ProtectionStopped.</span></span>
<span data-ttu-id="d4d1d-141">보호를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d4d1d-141">Protection is disabled.</span></span>

```yaml
Type: ItemProtectionState
Parameter Sets: (All)
Aliases: 
Accepted values: IRPending, ProtectionError, Protected, ProtectionStopped

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4d1d-142">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="d4d1d-142">-ProtectionStatus</span></span>
<span data-ttu-id="d4d1d-143">컨테이너에 있는 항목의 전체 보호 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4d1d-143">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="d4d1d-144">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d4d1d-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d4d1d-145">손상</span><span class="sxs-lookup"><span data-stu-id="d4d1d-145">Healthy</span></span>
- <span data-ttu-id="d4d1d-146">상태임</span><span class="sxs-lookup"><span data-stu-id="d4d1d-146">Unhealthy</span></span>

```yaml
Type: ItemProtectionStatus
Parameter Sets: (All)
Aliases: 
Accepted values: Healthy, Unhealthy

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4d1d-147">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="d4d1d-147">-WorkloadType</span></span>
<span data-ttu-id="d4d1d-148">작업 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4d1d-148">Specifies the workload type.</span></span> <span data-ttu-id="d4d1d-149">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d4d1d-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d4d1d-150">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="d4d1d-150">AzureVM</span></span> 
- <span data-ttu-id="d4d1d-151">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="d4d1d-151">AzureSQLDatabase</span></span>

```yaml
Type: WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4d1d-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4d1d-152">CommonParameters</span></span>
<span data-ttu-id="d4d1d-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4d1d-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4d1d-154">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4d1d-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4d1d-155">입력</span><span class="sxs-lookup"><span data-stu-id="d4d1d-155">INPUTS</span></span>

### <span data-ttu-id="d4d1d-156">않아야</span><span class="sxs-lookup"><span data-stu-id="d4d1d-156">None</span></span>
<span data-ttu-id="d4d1d-157">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d4d1d-157">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d4d1d-158">출력</span><span class="sxs-lookup"><span data-stu-id="d4d1d-158">OUTPUTS</span></span>

### <span data-ttu-id="d4d1d-159">Microsoft Azure.. i g i..</span><span class="sxs-lookup"><span data-stu-id="d4d1d-159">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="d4d1d-160">System.webserver. IList ' 1 [Microsoft Azure. e-명령. i n t]</span><span class="sxs-lookup"><span data-stu-id="d4d1d-160">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase]</span></span>

## <span data-ttu-id="d4d1d-161">상속자</span><span class="sxs-lookup"><span data-stu-id="d4d1d-161">NOTES</span></span>

## <span data-ttu-id="d4d1d-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d4d1d-162">RELATED LINKS</span></span>

[<span data-ttu-id="d4d1d-163">백업-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="d4d1d-163">Backup-AzureRmRecoveryServicesBackupItem</span></span>](./Backup-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="d4d1d-164">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="d4d1d-164">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="d4d1d-165">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="d4d1d-165">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="d4d1d-166">Restore-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="d4d1d-166">Restore-AzureRmRecoveryServicesBackupItem</span></span>](./Restore-AzureRmRecoveryServicesBackupItem.md)


