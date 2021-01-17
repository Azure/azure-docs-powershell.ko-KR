---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: 4b34bdf2357b389081297df8f49745127953985b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371281"
---
# <span data-ttu-id="ccd41-101">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="ccd41-101">Set-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="ccd41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccd41-102">SYNOPSIS</span></span>
<span data-ttu-id="ccd41-103">자격 증명 모음의 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd41-103">Updates properties of a Vault.</span></span>

## <span data-ttu-id="ccd41-104">구문</span><span class="sxs-lookup"><span data-stu-id="ccd41-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultProperty -SoftDeleteFeatureState <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccd41-105">설명</span><span class="sxs-lookup"><span data-stu-id="ccd41-105">DESCRIPTION</span></span>
<span data-ttu-id="ccd41-106">**Set-AzRecoveryServicesVaultProperty** cmdlet은 Recovery Services 자격 증명 모음의 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd41-106">The **Set-AzRecoveryServicesVaultProperty** cmdlet updates properties of a Recovery services vault.</span></span>
<span data-ttu-id="ccd41-107">이 cmdlet은 현재 설정 작업 후에 업데이트된 자격 증명 모음 속성을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd41-107">This cmdlet returns the updated vault properties after the current set operation.</span></span>
<span data-ttu-id="ccd41-108">소프트 삭제와 같은 자격 증명 모음의 이 cmdlet 속성을 사용하면 어느 시점에서든 사용하도록 설정될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ccd41-108">Using this cmdlet properties of vault such as soft-delete can be enabled at any point of time.</span></span>
<span data-ttu-id="ccd41-109">자격 증명 모음에 등록된 컨테이너가 없는 경우 자격 증명 모음의 **SoftDeleteFeatureState** 속성을 사용하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ccd41-109">**SoftDeleteFeatureState** property of a vault can be disabled only if there are no registered containers in the vault.</span></span>

## <span data-ttu-id="ccd41-110">예제</span><span class="sxs-lookup"><span data-stu-id="ccd41-110">EXAMPLES</span></span>

### <span data-ttu-id="ccd41-111">예제 1: 자격 증명 모음의 SoftDeleteFeatureState 업데이트</span><span class="sxs-lookup"><span data-stu-id="ccd41-111">Example 1: Update SoftDeleteFeatureState of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -Name "MyVaultName"
PS C:\> $props = Set-AzRecoveryServicesVaultProperty -VaultId $vault.Id -SoftDeleteFeatureState Enable
```

<span data-ttu-id="ccd41-112">첫 번째 명령은 자격 증명 모음 개체를 인용한 다음, 자격 증명 모음 $vault 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd41-112">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="ccd41-113">두 번째 명령은 자격 증명 모음의 SoftDeleteFeatureState 속성을 "Enabled" 상태로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd41-113">The second command Updates the SoftDeleteFeatureState property of the vault to "Enabled" state.</span></span>

## <span data-ttu-id="ccd41-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ccd41-114">PARAMETERS</span></span>

### <span data-ttu-id="ccd41-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccd41-115">-DefaultProfile</span></span>
<span data-ttu-id="ccd41-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ccd41-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ccd41-117">-SoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="ccd41-117">-SoftDeleteFeatureState</span></span>
<span data-ttu-id="ccd41-118">Recovery Services 자격 증명 모음의 SoftDeleteFeatureState입니다.</span><span class="sxs-lookup"><span data-stu-id="ccd41-118">SoftDeleteFeatureState of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="ccd41-119">-VaultId</span><span class="sxs-lookup"><span data-stu-id="ccd41-119">-VaultId</span></span>
<span data-ttu-id="ccd41-120">ARM 자격 증명 모음의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ccd41-120">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="ccd41-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ccd41-121">-Confirm</span></span>
<span data-ttu-id="ccd41-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ccd41-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccd41-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccd41-123">-WhatIf</span></span>
<span data-ttu-id="ccd41-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ccd41-124">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="ccd41-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccd41-125">CommonParameters</span></span>
<span data-ttu-id="ccd41-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd41-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccd41-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ccd41-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccd41-128">입력</span><span class="sxs-lookup"><span data-stu-id="ccd41-128">INPUTS</span></span>

### <span data-ttu-id="ccd41-129">System.String</span><span class="sxs-lookup"><span data-stu-id="ccd41-129">System.String</span></span>

### <span data-ttu-id="ccd41-130">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="ccd41-130">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span></span>

## <span data-ttu-id="ccd41-131">출력</span><span class="sxs-lookup"><span data-stu-id="ccd41-131">OUTPUTS</span></span>

### <span data-ttu-id="ccd41-132">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="ccd41-132">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="ccd41-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ccd41-133">NOTES</span></span>

## <span data-ttu-id="ccd41-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ccd41-134">RELATED LINKS</span></span>

[<span data-ttu-id="ccd41-135">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ccd41-135">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="ccd41-136">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="ccd41-136">Get-AzRecoveryServicesVaultProperty</span></span>](./Get-AzRecoveryServicesVaultProperty.md)


