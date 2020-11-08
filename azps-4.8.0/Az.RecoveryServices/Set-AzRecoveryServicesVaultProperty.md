---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: 4b34bdf2357b389081297df8f49745127953985b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214013"
---
# <span data-ttu-id="39897-101">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="39897-101">Set-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="39897-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39897-102">SYNOPSIS</span></span>
<span data-ttu-id="39897-103">저장실의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="39897-103">Updates properties of a Vault.</span></span>

## <span data-ttu-id="39897-104">구문과</span><span class="sxs-lookup"><span data-stu-id="39897-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultProperty -SoftDeleteFeatureState <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39897-105">설명은</span><span class="sxs-lookup"><span data-stu-id="39897-105">DESCRIPTION</span></span>
<span data-ttu-id="39897-106">**AzRecoveryServicesVaultProperty** Cmdlet은 Recovery services 자격 증명 모음의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="39897-106">The **Set-AzRecoveryServicesVaultProperty** cmdlet updates properties of a Recovery services vault.</span></span>
<span data-ttu-id="39897-107">이 cmdlet은 현재 설정 작업 후에 업데이트 된 자격 증명 모음 속성을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="39897-107">This cmdlet returns the updated vault properties after the current set operation.</span></span>
<span data-ttu-id="39897-108">소프트 삭제와 같은 저장실의이 cmdlet 속성을 사용 하면 언제 든 지 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="39897-108">Using this cmdlet properties of vault such as soft-delete can be enabled at any point of time.</span></span>
<span data-ttu-id="39897-109">자격 증명 모음의 **소프트 Deletefeaturestate** 속성은 자격 증명 모음에 등록 된 컨테이너가 없는 경우에만 사용 하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="39897-109">**SoftDeleteFeatureState** property of a vault can be disabled only if there are no registered containers in the vault.</span></span>

## <span data-ttu-id="39897-110">예제의</span><span class="sxs-lookup"><span data-stu-id="39897-110">EXAMPLES</span></span>

### <span data-ttu-id="39897-111">예제 1: 저장실의 소프트 Deletefeaturestate 업데이트</span><span class="sxs-lookup"><span data-stu-id="39897-111">Example 1: Update SoftDeleteFeatureState of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -Name "MyVaultName"
PS C:\> $props = Set-AzRecoveryServicesVaultProperty -VaultId $vault.Id -SoftDeleteFeatureState Enable
```

<span data-ttu-id="39897-112">첫 번째 명령은 자격 증명 모음 개체를 가져온 다음 $vault 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="39897-112">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="39897-113">두 번째 명령은 저장실의 소프트 Deletefeaturestate 속성을 "사용" 상태로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="39897-113">The second command Updates the SoftDeleteFeatureState property of the vault to "Enabled" state.</span></span>

## <span data-ttu-id="39897-114">변수</span><span class="sxs-lookup"><span data-stu-id="39897-114">PARAMETERS</span></span>

### <span data-ttu-id="39897-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39897-115">-DefaultProfile</span></span>
<span data-ttu-id="39897-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="39897-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39897-117">-소프트 Deletefeaturestate</span><span class="sxs-lookup"><span data-stu-id="39897-117">-SoftDeleteFeatureState</span></span>
<span data-ttu-id="39897-118">복구 서비스 자격 증명 모음의 소프트 Deletefeaturestate입니다.</span><span class="sxs-lookup"><span data-stu-id="39897-118">SoftDeleteFeatureState of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="39897-119">-VaultId</span><span class="sxs-lookup"><span data-stu-id="39897-119">-VaultId</span></span>
<span data-ttu-id="39897-120">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="39897-120">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="39897-121">-확인</span><span class="sxs-lookup"><span data-stu-id="39897-121">-Confirm</span></span>
<span data-ttu-id="39897-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="39897-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39897-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39897-123">-WhatIf</span></span>
<span data-ttu-id="39897-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="39897-124">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="39897-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39897-125">CommonParameters</span></span>
<span data-ttu-id="39897-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="39897-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39897-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="39897-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39897-128">입력</span><span class="sxs-lookup"><span data-stu-id="39897-128">INPUTS</span></span>

### <span data-ttu-id="39897-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="39897-129">System.String</span></span>

### <span data-ttu-id="39897-130">VaultSoftDeleteFeatureState에서. i. i m/.</span><span class="sxs-lookup"><span data-stu-id="39897-130">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span></span>

## <span data-ttu-id="39897-131">출력</span><span class="sxs-lookup"><span data-stu-id="39897-131">OUTPUTS</span></span>

### <span data-ttu-id="39897-132">BackupResourceVaultConfigResource/. m m/.</span><span class="sxs-lookup"><span data-stu-id="39897-132">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="39897-133">상속자</span><span class="sxs-lookup"><span data-stu-id="39897-133">NOTES</span></span>

## <span data-ttu-id="39897-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="39897-134">RELATED LINKS</span></span>

[<span data-ttu-id="39897-135">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="39897-135">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="39897-136">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="39897-136">Get-AzRecoveryServicesVaultProperty</span></span>](./Get-AzRecoveryServicesVaultProperty.md)


