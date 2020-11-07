---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: c861bbe3b422360f58f36cbe859343f7dcc7ed37
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699713"
---
# <span data-ttu-id="65c09-101">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="65c09-101">Get-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="65c09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65c09-102">SYNOPSIS</span></span>
<span data-ttu-id="65c09-103">백업의 컨테이너에서 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="65c09-103">Gets the items from a container in Backup.</span></span>

## <span data-ttu-id="65c09-104">구문과</span><span class="sxs-lookup"><span data-stu-id="65c09-104">SYNTAX</span></span>

### <span data-ttu-id="65c09-105">Get항목 Forcontainer (기본값)</span><span class="sxs-lookup"><span data-stu-id="65c09-105">GetItemsForContainer (Default)</span></span>
```
Get-AzRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="65c09-106">Get항목 Forvault</span><span class="sxs-lookup"><span data-stu-id="65c09-106">GetItemsForVault</span></span>
```
Get-AzRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="65c09-107">Get항목 Forpolicy</span><span class="sxs-lookup"><span data-stu-id="65c09-107">GetItemsForPolicy</span></span>
```
Get-AzRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65c09-108">설명은</span><span class="sxs-lookup"><span data-stu-id="65c09-108">DESCRIPTION</span></span>
<span data-ttu-id="65c09-109">**AzRecoveryServicesBackupItem** cmdlet은 컨테이너의 항목 또는 Azure Backup의 값과 항목의 보호 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="65c09-109">The **Get-AzRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="65c09-110">Azure Recovery Services 자격 증명 모음에 등록 된 컨테이너에는 보호할 수 있는 항목이 하나 이상 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="65c09-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="65c09-111">Azure 가상 컴퓨터의 경우 가상 컴퓨터 컨테이너에 백업 항목이 하나만 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="65c09-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="65c09-112">현재 cmdlet을 사용 하기 전에 Set-AzRecoveryServicesVaultContext cmdlet을 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65c09-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="65c09-113">예제의</span><span class="sxs-lookup"><span data-stu-id="65c09-113">EXAMPLES</span></span>

### <span data-ttu-id="65c09-114">예제 1: 백업 컨테이너에서 항목 가져오기</span><span class="sxs-lookup"><span data-stu-id="65c09-114">Example 1: Get an item from a Backup container</span></span>
```
PS C:\>$Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM
```

<span data-ttu-id="65c09-115">첫 번째 명령은 Add-azurevm 형식의 컨테이너를 가져온 다음 $Container 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="65c09-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="65c09-116">두 번째 명령은 $Container에서 V2VM 이라는 이름의 백업 항목을 가져온 다음 $BackupItem 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="65c09-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

## <span data-ttu-id="65c09-117">변수</span><span class="sxs-lookup"><span data-stu-id="65c09-117">PARAMETERS</span></span>

### <span data-ttu-id="65c09-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="65c09-118">-BackupManagementType</span></span>
<span data-ttu-id="65c09-119">백업 관리 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65c09-119">Specifies the Backup management type.</span></span>
<span data-ttu-id="65c09-120">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="65c09-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="65c09-121">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="65c09-121">AzureVM</span></span> 
- <span data-ttu-id="65c09-122">화성</span><span class="sxs-lookup"><span data-stu-id="65c09-122">MARS</span></span> 
- <span data-ttu-id="65c09-123">SCDPM</span><span class="sxs-lookup"><span data-stu-id="65c09-123">SCDPM</span></span> 
- <span data-ttu-id="65c09-124">AzureBackupServer</span><span class="sxs-lookup"><span data-stu-id="65c09-124">AzureBackupServer</span></span> 
- <span data-ttu-id="65c09-125">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="65c09-125">AzureSQL</span></span>
- <span data-ttu-id="65c09-126">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="65c09-126">AzureStorage</span></span>

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

### <span data-ttu-id="65c09-127">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="65c09-127">-Container</span></span>
<span data-ttu-id="65c09-128">이 cmdlet에서 백업 항목을 가져오는 컨테이너 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65c09-128">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="65c09-129">**AzureRmRecoveryServicesBackupContainer** 을 얻으려면 Get-AzRecoveryServicesBackupContainer cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="65c09-129">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the Get-AzRecoveryServicesBackupContainer cmdlet.</span></span>

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

### <span data-ttu-id="65c09-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65c09-130">-DefaultProfile</span></span>
<span data-ttu-id="65c09-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="65c09-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65c09-132">-이름</span><span class="sxs-lookup"><span data-stu-id="65c09-132">-Name</span></span>
<span data-ttu-id="65c09-133">컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65c09-133">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="65c09-134">-정책</span><span class="sxs-lookup"><span data-stu-id="65c09-134">-Policy</span></span>
<span data-ttu-id="65c09-135">보호 정책 개체.</span><span class="sxs-lookup"><span data-stu-id="65c09-135">Protection policy object.</span></span>

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

### <span data-ttu-id="65c09-136">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="65c09-136">-ProtectionState</span></span>
<span data-ttu-id="65c09-137">보호 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65c09-137">Specifies the state of protection.</span></span>
<span data-ttu-id="65c09-138">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="65c09-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="65c09-139">IRPending.</span><span class="sxs-lookup"><span data-stu-id="65c09-139">IRPending.</span></span>
<span data-ttu-id="65c09-140">초기 동기화가 시작 되지 않고 아직 복구 지점이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="65c09-140">Initial synchronization has not started and there is no recovery point yet.</span></span> 
- <span data-ttu-id="65c09-141">됨.</span><span class="sxs-lookup"><span data-stu-id="65c09-141">Protected.</span></span>
<span data-ttu-id="65c09-142">보호가 진행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="65c09-142">Protection is ongoing.</span></span> 
- <span data-ttu-id="65c09-143">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="65c09-143">ProtectionError.</span></span>
<span data-ttu-id="65c09-144">보호 오류가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="65c09-144">There is a protection error.</span></span>
- <span data-ttu-id="65c09-145">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="65c09-145">ProtectionStopped.</span></span>
<span data-ttu-id="65c09-146">보호를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="65c09-146">Protection is disabled.</span></span>

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

### <span data-ttu-id="65c09-147">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="65c09-147">-ProtectionStatus</span></span>
<span data-ttu-id="65c09-148">컨테이너에 있는 항목의 전체 보호 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65c09-148">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="65c09-149">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="65c09-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="65c09-150">손상</span><span class="sxs-lookup"><span data-stu-id="65c09-150">Healthy</span></span>
- <span data-ttu-id="65c09-151">상태임</span><span class="sxs-lookup"><span data-stu-id="65c09-151">Unhealthy</span></span>

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

### <span data-ttu-id="65c09-152">-VaultId</span><span class="sxs-lookup"><span data-stu-id="65c09-152">-VaultId</span></span>
<span data-ttu-id="65c09-153">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="65c09-153">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="65c09-154">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="65c09-154">-WorkloadType</span></span>
<span data-ttu-id="65c09-155">작업 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65c09-155">Specifies the workload type.</span></span> <span data-ttu-id="65c09-156">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="65c09-156">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="65c09-157">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="65c09-157">AzureVM</span></span> 
- <span data-ttu-id="65c09-158">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="65c09-158">AzureSQLDatabase</span></span>
- <span data-ttu-id="65c09-159">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="65c09-159">AzureFiles</span></span>

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

### <span data-ttu-id="65c09-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65c09-160">CommonParameters</span></span>
<span data-ttu-id="65c09-161">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="65c09-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65c09-162">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65c09-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65c09-163">입력</span><span class="sxs-lookup"><span data-stu-id="65c09-163">INPUTS</span></span>

### <span data-ttu-id="65c09-164">ContainerBase에서. i. i m/.</span><span class="sxs-lookup"><span data-stu-id="65c09-164">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="65c09-165">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="65c09-165">System.String</span></span>

## <span data-ttu-id="65c09-166">출력</span><span class="sxs-lookup"><span data-stu-id="65c09-166">OUTPUTS</span></span>

### <span data-ttu-id="65c09-167">Microsoft Azure.. i g i..</span><span class="sxs-lookup"><span data-stu-id="65c09-167">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="65c09-168">상속자</span><span class="sxs-lookup"><span data-stu-id="65c09-168">NOTES</span></span>

## <span data-ttu-id="65c09-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="65c09-169">RELATED LINKS</span></span>

[<span data-ttu-id="65c09-170">백업-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="65c09-170">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="65c09-171">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="65c09-171">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="65c09-172">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="65c09-172">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="65c09-173">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="65c09-173">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)


