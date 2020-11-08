---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: a9bd1eead98a7afb06e1f5b480f8a65fc5079bd4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043521"
---
# <span data-ttu-id="a34c8-101">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="a34c8-101">Set-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="a34c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a34c8-102">SYNOPSIS</span></span>
<span data-ttu-id="a34c8-103">저장실의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a34c8-103">Updates properties of a Vault.</span></span>

## <span data-ttu-id="a34c8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a34c8-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultProperty -SoftDeleteFeatureState <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a34c8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a34c8-105">DESCRIPTION</span></span>
<span data-ttu-id="a34c8-106">**AzRecoveryServicesVaultProperty** Cmdlet은 Recovery services 자격 증명 모음의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a34c8-106">The **Set-AzRecoveryServicesVaultProperty** cmdlet updates properties of a Recovery services vault.</span></span>
<span data-ttu-id="a34c8-107">**Set-AzRecoveryServicesVaultProperty** cmdlet을 사용 하 여 자격 증명 모음의 현재 속성을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a34c8-107">You can use **Set-AzRecoveryServicesVaultProperty** cmdlet to get the current properties of a vault.</span></span>
<span data-ttu-id="a34c8-108">이 cmdlet을 사용 하 여 볼트의 **소프트 Deletefeaturestate** 속성을 언제 든 지 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a34c8-108">Using this cmdlet **SoftDeleteFeatureState** property of a vault can be enabled at any point of time.</span></span>
<span data-ttu-id="a34c8-109">자격 증명 모음의 **소프트 Deletefeaturestate** 속성은 자격 증명 모음에 등록 된 컨테이너가 없는 경우에만 사용 하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a34c8-109">**SoftDeleteFeatureState** property of a vault can be disabled only if there are no registered containers in the vault.</span></span>
<span data-ttu-id="a34c8-110">현재 cmdlet을 사용 하기 전에 Set-AzRecoveryServicesVaultContext cmdlet을 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a34c8-110">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="a34c8-111">예제의</span><span class="sxs-lookup"><span data-stu-id="a34c8-111">EXAMPLES</span></span>

### <span data-ttu-id="a34c8-112">예제 1: 저장실의 소프트 Deletefeaturestate 업데이트</span><span class="sxs-lookup"><span data-stu-id="a34c8-112">Example 1: Update SoftDeleteFeatureState of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -Name "MyVaultName"
PS C:\> $props = Set-AzRecoveryServicesVaultProperty -VaultId $vault.Id -SoftDeleteFeatureState Enable
```

<span data-ttu-id="a34c8-113">첫 번째 명령은 자격 증명 모음 개체를 가져온 다음 $vault 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a34c8-113">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="a34c8-114">두 번째 명령은 저장실의 소프트 Deletefeaturestate 속성을 "사용" 상태로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a34c8-114">The second command Updates the SoftDeleteFeatureState property of the vault to "Enabled" state.</span></span>

## <span data-ttu-id="a34c8-115">변수</span><span class="sxs-lookup"><span data-stu-id="a34c8-115">PARAMETERS</span></span>

### <span data-ttu-id="a34c8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a34c8-116">-DefaultProfile</span></span>
<span data-ttu-id="a34c8-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a34c8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a34c8-118">-소프트 Deletefeaturestate</span><span class="sxs-lookup"><span data-stu-id="a34c8-118">-SoftDeleteFeatureState</span></span>
<span data-ttu-id="a34c8-119">복구 서비스 자격 증명 모음의 소프트 Deletefeaturestate입니다.</span><span class="sxs-lookup"><span data-stu-id="a34c8-119">SoftDeleteFeatureState of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="a34c8-120">-VaultId</span><span class="sxs-lookup"><span data-stu-id="a34c8-120">-VaultId</span></span>
<span data-ttu-id="a34c8-121">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a34c8-121">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="a34c8-122">-확인</span><span class="sxs-lookup"><span data-stu-id="a34c8-122">-Confirm</span></span>
<span data-ttu-id="a34c8-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a34c8-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a34c8-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a34c8-124">-WhatIf</span></span>
<span data-ttu-id="a34c8-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a34c8-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a34c8-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a34c8-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a34c8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a34c8-127">CommonParameters</span></span>
<span data-ttu-id="a34c8-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a34c8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a34c8-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a34c8-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a34c8-130">입력</span><span class="sxs-lookup"><span data-stu-id="a34c8-130">INPUTS</span></span>

### <span data-ttu-id="a34c8-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a34c8-131">System.String</span></span>

### <span data-ttu-id="a34c8-132">VaultSoftDeleteFeatureState에서. i. i m/.</span><span class="sxs-lookup"><span data-stu-id="a34c8-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span></span>

## <span data-ttu-id="a34c8-133">출력</span><span class="sxs-lookup"><span data-stu-id="a34c8-133">OUTPUTS</span></span>

### <span data-ttu-id="a34c8-134">BackupResourceVaultConfigResource/. m m/.</span><span class="sxs-lookup"><span data-stu-id="a34c8-134">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="a34c8-135">상속자</span><span class="sxs-lookup"><span data-stu-id="a34c8-135">NOTES</span></span>

## <span data-ttu-id="a34c8-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a34c8-136">RELATED LINKS</span></span>

[<span data-ttu-id="a34c8-137">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="a34c8-137">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="a34c8-138">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="a34c8-138">Get-AzRecoveryServicesVaultProperty</span></span>](./Get-AzRecoveryServicesVaultProperty.md)


