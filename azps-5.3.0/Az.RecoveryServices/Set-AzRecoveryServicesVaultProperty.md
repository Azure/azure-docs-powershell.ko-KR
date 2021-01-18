---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: e6bd0284d9ce5b5cb6973fce6aae5e16a4c06883
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492480"
---
# <span data-ttu-id="ceba2-101">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="ceba2-101">Set-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="ceba2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ceba2-102">SYNOPSIS</span></span>
<span data-ttu-id="ceba2-103">자격 증명 모음의 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ceba2-103">Updates properties of a Vault.</span></span>

## <span data-ttu-id="ceba2-104">구문</span><span class="sxs-lookup"><span data-stu-id="ceba2-104">SYNTAX</span></span>

### <span data-ttu-id="ceba2-105">AzureRSVaultSoftDelteParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ceba2-105">AzureRSVaultSoftDelteParameterSet (Default)</span></span>
```
Set-AzRecoveryServicesVaultProperty -SoftDeleteFeatureState <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ceba2-106">AzureRSVaultCMKParameterSet</span><span class="sxs-lookup"><span data-stu-id="ceba2-106">AzureRSVaultCMKParameterSet</span></span>
```
Set-AzRecoveryServicesVaultProperty -EncryptionKeyId <string> -KeyVaultSubscriptionId <string> [-InfrastructureEncryption] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ceba2-107">설명</span><span class="sxs-lookup"><span data-stu-id="ceba2-107">DESCRIPTION</span></span>
<span data-ttu-id="ceba2-108">**Set-AzRecoveryServicesVaultProperty** cmdlet은 Recovery Services 자격 증명 모음의 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ceba2-108">The **Set-AzRecoveryServicesVaultProperty** cmdlet updates properties of a Recovery services vault.</span></span> <span data-ttu-id="ceba2-109">이 cmdlet은 두 개의 다른 매개 변수 집합이 있는 자격 증명 모음에 대해 소프트 삭제를 활성화/비활성화하거나 CMK 암호화를 설정하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ceba2-109">This cmdlet can be used to enable/disable soft delete or set CMK encryption for a vault with two different parameter sets.</span></span> 
<span data-ttu-id="ceba2-110">자격 증명 모음에 등록된 컨테이너가 없는 경우 자격 증명 모음의 **SoftDeleteFeatureState** 속성을 사용하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ceba2-110">**SoftDeleteFeatureState** property of a vault can be disabled only if there are no registered containers in the vault.</span></span> <span data-ttu-id="ceba2-111">InfrastructurEncryption은 사용자가 CMK 자격 증명 모음을 처음 업데이트할 때만 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ceba2-111">InfrastructurEncryption can only be set the first time a user updates the CMK vault.</span></span>

## <span data-ttu-id="ceba2-112">예제</span><span class="sxs-lookup"><span data-stu-id="ceba2-112">EXAMPLES</span></span>

### <span data-ttu-id="ceba2-113">예제 1: 자격 증명 모음의 SoftDeleteFeatureState 업데이트</span><span class="sxs-lookup"><span data-stu-id="ceba2-113">Example 1: Update SoftDeleteFeatureState of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName"
PS C:\> $props = Set-AzRecoveryServicesVaultProperty -VaultId $vault.Id -SoftDeleteFeatureState Enable
```

<span data-ttu-id="ceba2-114">첫 번째 명령은 자격 증명 모음 개체를 인용한 다음, 자격 증명 모음 $vault 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="ceba2-114">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="ceba2-115">두 번째 명령은 자격 증명 모음의 SoftDeleteFeatureState 속성을 "Enabled" 상태로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ceba2-115">The second command Updates the SoftDeleteFeatureState property of the vault to "Enabled" state.</span></span>

### <span data-ttu-id="ceba2-116">예제 2: 자격 증명 모음의 CMK 암호화 업데이트</span><span class="sxs-lookup"><span data-stu-id="ceba2-116">Example 2: Update CMK encryption of a vault</span></span>

```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName"
PS C:\> $keyVault = Get-AzKeyVault -VaultName "keyVaultName" -ResourceGroupName "RGName" 
PS C:\> $key = Get-AzKeyVaultKey -VaultName "keyVaultName" -Name "keyName" 
PS C:\> Set-AzRecoveryServicesVaultProperty -EncryptionKeyId $key.ID -KeyVaultSubscriptionId "f870818k-5h28-4t48-8961-37458592348r" -InfrastructureEncryption -VaultId $vault.ID
```

<span data-ttu-id="ceba2-117">첫 번째 cmdlet은 암호화 속성을 업데이트하는 RSVault를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ceba2-117">First cmdlet gets the RSVault to update encryption properties.</span></span> <span data-ttu-id="ceba2-118">두 번째 cmdlet은 Azure Key Vault를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ceba2-118">Second cmdlet gets the azure key vault.</span></span> <span data-ttu-id="ceba2-119">세 번째 cmdlet은 키 자격 증명 모음에서 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ceba2-119">Third cmdlet get the key from the key vault.</span></span>
<span data-ttu-id="ceba2-120">네 번째 cmdlet은 RSVault 내에서 고객 관리 암호화 키를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ceba2-120">Fourth cmdlet updates the customer managed encryption key within the RSVault.</span></span> <span data-ttu-id="ceba2-121">-InfrastructureEncryption param을 사용하여 처음으로 업데이트할 때 인프라 암호화를 사용하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ceba2-121">Use -InfrastructureEncryption param to enable infrastructure encryption for the first time update.</span></span> 

## <span data-ttu-id="ceba2-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ceba2-122">PARAMETERS</span></span>

### <span data-ttu-id="ceba2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceba2-123">-DefaultProfile</span></span>
<span data-ttu-id="ceba2-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ceba2-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ceba2-125">-SoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="ceba2-125">-SoftDeleteFeatureState</span></span>
<span data-ttu-id="ceba2-126">Recovery Services 자격 증명 모음의 SoftDeleteFeatureState입니다.</span><span class="sxs-lookup"><span data-stu-id="ceba2-126">SoftDeleteFeatureState of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enable, Disable

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceba2-127">-EncryptionKeyId</span><span class="sxs-lookup"><span data-stu-id="ceba2-127">-EncryptionKeyId</span></span>
<span data-ttu-id="ceba2-128">CMK에 사용할 암호화 키의 KeyId입니다.</span><span class="sxs-lookup"><span data-stu-id="ceba2-128">KeyId of the encryption key to be used for CMK.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: KeyID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceba2-129">-KeyVaultSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ceba2-129">-KeyVaultSubscriptionId</span></span>
<span data-ttu-id="ceba2-130">Key Vault의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ceba2-130">Subscription Id of the Key Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SubscriptionID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceba2-131">-InfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="ceba2-131">-InfrastructureEncryption</span></span>
<span data-ttu-id="ceba2-132">이 자격 증명 모음에서 인프라 암호화를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="ceba2-132">Enables infrastructure encryption on this vault.</span></span> <span data-ttu-id="ceba2-133">암호화를 구성할 때 인프라 암호화를 사용하도록 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceba2-133">Infrastructure encryption must be enabled when configuring encryption.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceba2-134">-VaultId</span><span class="sxs-lookup"><span data-stu-id="ceba2-134">-VaultId</span></span>
<span data-ttu-id="ceba2-135">ARM 자격 증명 모음의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ceba2-135">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="ceba2-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ceba2-136">-Confirm</span></span>
<span data-ttu-id="ceba2-137">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ceba2-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ceba2-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ceba2-138">-WhatIf</span></span>
<span data-ttu-id="ceba2-139">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ceba2-139">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="ceba2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceba2-140">CommonParameters</span></span>
<span data-ttu-id="ceba2-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ceba2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceba2-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ceba2-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceba2-143">입력</span><span class="sxs-lookup"><span data-stu-id="ceba2-143">INPUTS</span></span>

### <span data-ttu-id="ceba2-144">System.String</span><span class="sxs-lookup"><span data-stu-id="ceba2-144">System.String</span></span>

### <span data-ttu-id="ceba2-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="ceba2-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span></span>

## <span data-ttu-id="ceba2-146">출력</span><span class="sxs-lookup"><span data-stu-id="ceba2-146">OUTPUTS</span></span>

### <span data-ttu-id="ceba2-147">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="ceba2-147">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="ceba2-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ceba2-148">NOTES</span></span>

## <span data-ttu-id="ceba2-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ceba2-149">RELATED LINKS</span></span>

[<span data-ttu-id="ceba2-150">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ceba2-150">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="ceba2-151">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="ceba2-151">Get-AzRecoveryServicesVaultProperty</span></span>](./Get-AzRecoveryServicesVaultProperty.md)
