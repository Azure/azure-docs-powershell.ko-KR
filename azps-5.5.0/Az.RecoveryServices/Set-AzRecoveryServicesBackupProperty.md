---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C635D723-0F03-4EF8-9435-24DBE0859899
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: 17187a1a5caa2de3f39ad7153ee1313e4ee8e3e3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191300"
---
# <span data-ttu-id="a3968-101">Set-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="a3968-101">Set-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="a3968-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3968-102">SYNOPSIS</span></span>
<span data-ttu-id="a3968-103">백업 관리에 대한 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a3968-103">Sets the properties for backup management.</span></span>

## <span data-ttu-id="a3968-104">구문</span><span class="sxs-lookup"><span data-stu-id="a3968-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesBackupProperty -Vault <ARSVault>  [-BackupStorageRedundancy <AzureRmRecoveryServicesBackupStorageRedundancyType>]
 [-EnableCrossRegionRestore] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3968-105">설명</span><span class="sxs-lookup"><span data-stu-id="a3968-105">DESCRIPTION</span></span>
<span data-ttu-id="a3968-106">**Set-AzRecoveryServicesBackupProperty** cmdlet은 Recovery Services 자격 증명 모음에 대한 백업 저장소 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a3968-106">The **Set-AzRecoveryServicesBackupProperty** cmdlet sets backup storage properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="a3968-107">예제</span><span class="sxs-lookup"><span data-stu-id="a3968-107">EXAMPLES</span></span>

### <span data-ttu-id="a3968-108">예제 1: 자격 증명 모음에 대한 GeoRedundant 저장소 설정</span><span class="sxs-lookup"><span data-stu-id="a3968-108">Example 1: Set GeoRedundant storage for a vault</span></span>
```
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> Set-AzRecoveryServicesBackupProperty -Vault $Vault01 -BackupStorageRedundancy GeoRedundant
```

<span data-ttu-id="a3968-109">첫 번째 명령은 TestVault라는 자격 증명 모음을 인용한 다음 $Vault 01 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="a3968-109">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="a3968-110">두 번째 명령은 $Vault 01에 대한 백업 저장소 중복을 GeoRedundant로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a3968-110">The second command sets the backup storage redundancy for $Vault01 to GeoRedundant.</span></span>

## <span data-ttu-id="a3968-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3968-111">PARAMETERS</span></span>

### <span data-ttu-id="a3968-112">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="a3968-112">-BackupStorageRedundancy</span></span>
<span data-ttu-id="a3968-113">백업 저장소 중복 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a3968-113">Specifies the backup storage redundancy type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.AzureRmRecoveryServicesBackupStorageRedundancyType]
Parameter Sets: (All)
Aliases:
Accepted values: GeoRedundant, ZoneRedundant, LocallyRedundant

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3968-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3968-114">-DefaultProfile</span></span>
<span data-ttu-id="a3968-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a3968-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3968-116">-Vault</span><span class="sxs-lookup"><span data-stu-id="a3968-116">-Vault</span></span>
<span data-ttu-id="a3968-117">자격 증명 모음의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a3968-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="a3968-118">자격 증명 모음은 **AzureRmRecoveryServicesVault 개체가 되어야** 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3968-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3968-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3968-119">-Confirm</span></span>
<span data-ttu-id="a3968-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3968-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3968-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3968-121">-WhatIf</span></span>
<span data-ttu-id="a3968-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a3968-122">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="a3968-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3968-123">CommonParameters</span></span>
<span data-ttu-id="a3968-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a3968-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3968-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a3968-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3968-126">입력</span><span class="sxs-lookup"><span data-stu-id="a3968-126">INPUTS</span></span>

### <span data-ttu-id="a3968-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="a3968-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="a3968-128">출력</span><span class="sxs-lookup"><span data-stu-id="a3968-128">OUTPUTS</span></span>

### <span data-ttu-id="a3968-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="a3968-129">System.Void</span></span>

## <span data-ttu-id="a3968-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a3968-130">NOTES</span></span>

## <span data-ttu-id="a3968-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a3968-131">RELATED LINKS</span></span>

[<span data-ttu-id="a3968-132">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="a3968-132">Get-AzRecoveryServicesBackupProperty</span></span>](./Get-AzRecoveryServicesBackupProperty.md)

[<span data-ttu-id="a3968-133">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="a3968-133">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)


