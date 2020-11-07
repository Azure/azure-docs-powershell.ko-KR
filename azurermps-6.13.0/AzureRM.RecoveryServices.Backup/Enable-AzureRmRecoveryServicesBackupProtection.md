---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/enable-azurermrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
ms.openlocfilehash: 357256d1c1a754915cbebc978e5c4ccf4440ccf4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703818"
---
# <span data-ttu-id="894c9-101">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="894c9-101">Enable-AzureRmRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="894c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="894c9-102">SYNOPSIS</span></span>
<span data-ttu-id="894c9-103">지정 된 백업 보호 정책이 있는 항목에 대해 백업을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="894c9-103">Enables backup for an item with a specified Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="894c9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="894c9-104">SYNTAX</span></span>

### <span data-ttu-id="894c9-105">AzureVMComputeEnableProtection (기본값)</span><span class="sxs-lookup"><span data-stu-id="894c9-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String>
 [-ResourceGroupName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="894c9-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="894c9-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String> [-ServiceName] <String>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="894c9-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="894c9-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String>
 -StorageAccountName <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="894c9-108">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="894c9-108">ModifyProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="894c9-109">설명은</span><span class="sxs-lookup"><span data-stu-id="894c9-109">DESCRIPTION</span></span>
<span data-ttu-id="894c9-110">**AzureRmRecoveryServicesBackupProtection** cmdlet은 항목에 대 한 Azure 백업 보호 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="894c9-110">The **Enable-AzureRmRecoveryServicesBackupProtection** cmdlet sets Azure Backup protection policy on an item.</span></span>
<span data-ttu-id="894c9-111">현재 cmdlet을 사용 하기 전에 Set-AzureRmRecoveryServicesVaultContext cmdlet을 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="894c9-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="894c9-112">예제의</span><span class="sxs-lookup"><span data-stu-id="894c9-112">EXAMPLES</span></span>

### <span data-ttu-id="894c9-113">예제 1: 항목에 대해 백업 보호 사용</span><span class="sxs-lookup"><span data-stu-id="894c9-113">Example 1: Enable Backup protection for an item</span></span>
```
PS C:\> $Pol = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> Enable-AzureRmRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1"
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="894c9-114">첫 번째 cmdlet은 기본 정책 개체를 가져온 다음 $Pol 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="894c9-114">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="894c9-115">두 번째 cmdlet은 $Pol의 정책을 사용 하 여 V2VM 이라는 ARM 가상 컴퓨터에 대 한 백업 보호 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="894c9-115">The second cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

## <span data-ttu-id="894c9-116">변수</span><span class="sxs-lookup"><span data-stu-id="894c9-116">PARAMETERS</span></span>

### <span data-ttu-id="894c9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="894c9-117">-DefaultProfile</span></span>
<span data-ttu-id="894c9-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="894c9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="894c9-119">-항목</span><span class="sxs-lookup"><span data-stu-id="894c9-119">-Item</span></span>
<span data-ttu-id="894c9-120">이 cmdlet이 보호할 수 있는 백업 항목을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="894c9-120">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="894c9-121">**AzureRmRecoveryServicesBackupItem** 을 얻으려면 Get-AzureRmRecoveryServicesBackupItem cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="894c9-121">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: ModifyProtection
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="894c9-122">-이름</span><span class="sxs-lookup"><span data-stu-id="894c9-122">-Name</span></span>
<span data-ttu-id="894c9-123">백업 항목의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="894c9-123">Specifies the name of the Backup item.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, AzureFileShareEnableProtection
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="894c9-124">-정책</span><span class="sxs-lookup"><span data-stu-id="894c9-124">-Policy</span></span>
<span data-ttu-id="894c9-125">이 cmdlet이 항목과 연결 하는 보호 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="894c9-125">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="894c9-126">**AzureRmRecoveryServicesBackupProtectionPolicy** 개체를 가져오려면 Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="894c9-126">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="894c9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="894c9-127">-ResourceGroupName</span></span>
<span data-ttu-id="894c9-128">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="894c9-128">Specifies the name of the resource group.</span></span>
<span data-ttu-id="894c9-129">ARM 가상 컴퓨터에 대해서만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="894c9-129">Specify this parameter only for ARM virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMComputeEnableProtection
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="894c9-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="894c9-130">-ServiceName</span></span>
<span data-ttu-id="894c9-131">서비스 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="894c9-131">Specifies the service name.</span></span>
<span data-ttu-id="894c9-132">이 매개 변수는 ASM 가상 머신에만 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="894c9-132">Specify this parameter only for ASM virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMClassicComputeEnableProtection
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="894c9-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="894c9-133">-StorageAccountName</span></span>
<span data-ttu-id="894c9-134">Azure 파일 공유 저장소 계정 이름</span><span class="sxs-lookup"><span data-stu-id="894c9-134">Azure file share storage account name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileShareEnableProtection
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="894c9-135">-VaultId</span><span class="sxs-lookup"><span data-stu-id="894c9-135">-VaultId</span></span>
<span data-ttu-id="894c9-136">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="894c9-136">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="894c9-137">-확인</span><span class="sxs-lookup"><span data-stu-id="894c9-137">-Confirm</span></span>
<span data-ttu-id="894c9-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="894c9-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="894c9-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="894c9-139">-WhatIf</span></span>
<span data-ttu-id="894c9-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="894c9-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="894c9-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="894c9-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="894c9-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="894c9-142">CommonParameters</span></span>
<span data-ttu-id="894c9-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="894c9-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="894c9-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="894c9-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="894c9-145">입력</span><span class="sxs-lookup"><span data-stu-id="894c9-145">INPUTS</span></span>

### <span data-ttu-id="894c9-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="894c9-146">System.String</span></span>
<span data-ttu-id="894c9-147">매개 변수: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="894c9-147">Parameters: VaultId (ByValue)</span></span>

### <span data-ttu-id="894c9-148">Microsoft Azure.. i g i..</span><span class="sxs-lookup"><span data-stu-id="894c9-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="894c9-149">매개 변수: Item (ByValue)</span><span class="sxs-lookup"><span data-stu-id="894c9-149">Parameters: Item (ByValue)</span></span>

## <span data-ttu-id="894c9-150">출력</span><span class="sxs-lookup"><span data-stu-id="894c9-150">OUTPUTS</span></span>

### <span data-ttu-id="894c9-151">Microsoft Azure.. i m.. i a m.</span><span class="sxs-lookup"><span data-stu-id="894c9-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="894c9-152">상속자</span><span class="sxs-lookup"><span data-stu-id="894c9-152">NOTES</span></span>

## <span data-ttu-id="894c9-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="894c9-153">RELATED LINKS</span></span>

[<span data-ttu-id="894c9-154">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="894c9-154">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="894c9-155">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="894c9-155">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)


