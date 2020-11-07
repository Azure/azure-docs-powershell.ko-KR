---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: 03da361f8dd68d345782568dc243d4438cad1d77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711252"
---
# <span data-ttu-id="d5383-101">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="d5383-101">Get-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="d5383-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5383-102">SYNOPSIS</span></span>
<span data-ttu-id="d5383-103">백업의 컨테이너에서 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d5383-103">Gets the items from a container in Backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5383-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d5383-104">SYNTAX</span></span>

### <span data-ttu-id="d5383-105">Get항목 Forcontainer (기본값)</span><span class="sxs-lookup"><span data-stu-id="d5383-105">GetItemsForContainer (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5383-106">Get항목 Forvault</span><span class="sxs-lookup"><span data-stu-id="d5383-106">GetItemsForVault</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5383-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d5383-107">DESCRIPTION</span></span>
<span data-ttu-id="d5383-108">**AzureRmRecoveryServicesBackupItem** cmdlet은 컨테이너의 항목 또는 Azure Backup의 값과 항목의 보호 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d5383-108">The **Get-AzureRmRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>

<span data-ttu-id="d5383-109">Azure Recovery Services 자격 증명 모음에 등록 된 컨테이너에는 보호할 수 있는 항목이 하나 이상 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d5383-109">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="d5383-110">Azure 가상 컴퓨터의 경우 가상 컴퓨터 컨테이너에 백업 항목이 하나만 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d5383-110">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>

<span data-ttu-id="d5383-111">현재 cmdlet을 사용 하기 전에 Set-AzureRmRecoveryServicesVaultContext cmdlet을 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5383-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="d5383-112">예제의</span><span class="sxs-lookup"><span data-stu-id="d5383-112">EXAMPLES</span></span>

### <span data-ttu-id="d5383-113">예제 1: 백업 컨테이너에서 항목 가져오기</span><span class="sxs-lookup"><span data-stu-id="d5383-113">Example 1: Get an item from a Backup container</span></span>
```
PS C:\>$Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM
```

<span data-ttu-id="d5383-114">첫 번째 명령은 Add-azurevm 형식의 컨테이너를 가져온 다음 $Container 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5383-114">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="d5383-115">두 번째 명령은 $Container에서 V2VM 이라는 이름의 백업 항목을 가져온 다음 $BackupItem 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5383-115">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

## <span data-ttu-id="d5383-116">변수</span><span class="sxs-lookup"><span data-stu-id="d5383-116">PARAMETERS</span></span>

### <span data-ttu-id="d5383-117">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="d5383-117">-BackupManagementType</span></span>
<span data-ttu-id="d5383-118">백업 관리 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5383-118">Specifies the Backup management type.</span></span>
<span data-ttu-id="d5383-119">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d5383-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d5383-120">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="d5383-120">AzureVM</span></span> 
- <span data-ttu-id="d5383-121">화성</span><span class="sxs-lookup"><span data-stu-id="d5383-121">MARS</span></span> 
- <span data-ttu-id="d5383-122">SCDPM</span><span class="sxs-lookup"><span data-stu-id="d5383-122">SCDPM</span></span> 
- <span data-ttu-id="d5383-123">AzureBackupServer AzureSQL</span><span class="sxs-lookup"><span data-stu-id="d5383-123">AzureBackupServer AzureSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: GetItemsForVault
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5383-124">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="d5383-124">-Container</span></span>
<span data-ttu-id="d5383-125">이 cmdlet에서 백업 항목을 가져오는 컨테이너 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5383-125">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="d5383-126">**AzureRmRecoveryServicesBackupContainer** 을 얻으려면 Get-AzureRmRecoveryServicesBackupContainer cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5383-126">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the Get-AzureRmRecoveryServicesBackupContainer cmdlet.</span></span>

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

### <span data-ttu-id="d5383-127">-이름</span><span class="sxs-lookup"><span data-stu-id="d5383-127">-Name</span></span>
<span data-ttu-id="d5383-128">컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5383-128">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="d5383-129">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="d5383-129">-ProtectionState</span></span>
<span data-ttu-id="d5383-130">보호 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5383-130">Specifies the state of protection.</span></span>
<span data-ttu-id="d5383-131">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d5383-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d5383-132">IRPending.</span><span class="sxs-lookup"><span data-stu-id="d5383-132">IRPending.</span></span>
<span data-ttu-id="d5383-133">초기 동기화가 시작 되지 않고 아직 복구 지점이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d5383-133">Initial synchronization has not started and there is no recovery point yet.</span></span> 
- <span data-ttu-id="d5383-134">됨.</span><span class="sxs-lookup"><span data-stu-id="d5383-134">Protected.</span></span>
<span data-ttu-id="d5383-135">보호가 진행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="d5383-135">Protection is ongoing.</span></span> 
- <span data-ttu-id="d5383-136">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="d5383-136">ProtectionError.</span></span>
<span data-ttu-id="d5383-137">보호 오류가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d5383-137">There is a protection error.</span></span>
- <span data-ttu-id="d5383-138">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="d5383-138">ProtectionStopped.</span></span>
<span data-ttu-id="d5383-139">보호를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d5383-139">Protection is disabled.</span></span>

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

### <span data-ttu-id="d5383-140">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="d5383-140">-ProtectionStatus</span></span>
<span data-ttu-id="d5383-141">컨테이너에 있는 항목의 전체 보호 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5383-141">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="d5383-142">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d5383-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d5383-143">손상</span><span class="sxs-lookup"><span data-stu-id="d5383-143">Healthy</span></span>
- <span data-ttu-id="d5383-144">상태임</span><span class="sxs-lookup"><span data-stu-id="d5383-144">Unhealthy</span></span>

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

### <span data-ttu-id="d5383-145">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="d5383-145">-WorkloadType</span></span>
<span data-ttu-id="d5383-146">작업 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5383-146">Specifies the workload type.</span></span> <span data-ttu-id="d5383-147">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d5383-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d5383-148">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="d5383-148">AzureVM</span></span> 
- <span data-ttu-id="d5383-149">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="d5383-149">AzureSQLDatabase</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5383-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5383-150">-DefaultProfile</span></span>
<span data-ttu-id="d5383-151">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d5383-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5383-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5383-152">CommonParameters</span></span>
<span data-ttu-id="d5383-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5383-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5383-154">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5383-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5383-155">입력</span><span class="sxs-lookup"><span data-stu-id="d5383-155">INPUTS</span></span>

## <span data-ttu-id="d5383-156">출력</span><span class="sxs-lookup"><span data-stu-id="d5383-156">OUTPUTS</span></span>

### <span data-ttu-id="d5383-157">Microsoft Azure.. i g i..</span><span class="sxs-lookup"><span data-stu-id="d5383-157">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="d5383-158">System.webserver. IList ' 1 [Microsoft Azure. e-명령. i n t]</span><span class="sxs-lookup"><span data-stu-id="d5383-158">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase]</span></span>

## <span data-ttu-id="d5383-159">상속자</span><span class="sxs-lookup"><span data-stu-id="d5383-159">NOTES</span></span>

## <span data-ttu-id="d5383-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d5383-160">RELATED LINKS</span></span>

[<span data-ttu-id="d5383-161">백업-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="d5383-161">Backup-AzureRmRecoveryServicesBackupItem</span></span>](./Backup-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="d5383-162">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="d5383-162">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="d5383-163">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="d5383-163">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="d5383-164">Restore-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="d5383-164">Restore-AzureRmRecoveryServicesBackupItem</span></span>](./Restore-AzureRmRecoveryServicesBackupItem.md)


