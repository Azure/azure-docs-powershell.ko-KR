---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C635D723-0F03-4EF8-9435-24DBE0859899
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: 6912f54810baeeab795e5f2efca4a51ecafe1c93
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699607"
---
# <span data-ttu-id="35714-101">Set-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="35714-101">Set-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="35714-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35714-102">SYNOPSIS</span></span>
<span data-ttu-id="35714-103">백업 관리에 대 한 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35714-103">Sets the properties for backup management.</span></span>

## <span data-ttu-id="35714-104">구문과</span><span class="sxs-lookup"><span data-stu-id="35714-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesBackupProperty -Vault <ARSVault>
 [-BackupStorageRedundancy <AzureRmRecoveryServicesBackupStorageRedundancyType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35714-105">설명은</span><span class="sxs-lookup"><span data-stu-id="35714-105">DESCRIPTION</span></span>
<span data-ttu-id="35714-106">**AzRecoveryServicesBackupProperty** Cmdlet은 복구 서비스 자격 증명 모음에 대 한 백업 저장소 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35714-106">The **Set-AzRecoveryServicesBackupProperty** cmdlet sets backup storage properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="35714-107">예제의</span><span class="sxs-lookup"><span data-stu-id="35714-107">EXAMPLES</span></span>

### <span data-ttu-id="35714-108">예제 1: 자격 증명 모음에 대 한 GeoRedundant 저장소 설정</span><span class="sxs-lookup"><span data-stu-id="35714-108">Example 1: Set GeoRedundant storage for a vault</span></span>
```
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> Set-AzRecoveryServicesBackupProperty -Vault $Vault01 -BackupStorageRedundancy GeoRedundant
```

<span data-ttu-id="35714-109">첫 번째 명령은 TestVault 이라는 자격 증명 모음을 가져온 다음이를 $Vault 01 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="35714-109">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="35714-110">두 번째 명령은 $Vault 01에 대 한 백업 저장소 중복성을 GeoRedundant으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35714-110">The second command sets the backup storage redundancy for $Vault01 to GeoRedundant.</span></span>

## <span data-ttu-id="35714-111">변수</span><span class="sxs-lookup"><span data-stu-id="35714-111">PARAMETERS</span></span>

### <span data-ttu-id="35714-112">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="35714-112">-BackupStorageRedundancy</span></span>
<span data-ttu-id="35714-113">백업 저장소 중복성 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35714-113">Specifies the backup storage redundancy type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.AzureRmRecoveryServicesBackupStorageRedundancyType]
Parameter Sets: (All)
Aliases:
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35714-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35714-114">-DefaultProfile</span></span>
<span data-ttu-id="35714-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="35714-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35714-116">-저장실</span><span class="sxs-lookup"><span data-stu-id="35714-116">-Vault</span></span>
<span data-ttu-id="35714-117">자격 증명 모음의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35714-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="35714-118">자격 증명 모음이 **AzureRmRecoveryServicesVault** 개체 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="35714-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="35714-119">-확인</span><span class="sxs-lookup"><span data-stu-id="35714-119">-Confirm</span></span>
<span data-ttu-id="35714-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="35714-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35714-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35714-121">-WhatIf</span></span>
<span data-ttu-id="35714-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="35714-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="35714-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="35714-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35714-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35714-124">CommonParameters</span></span>
<span data-ttu-id="35714-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="35714-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35714-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35714-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35714-127">입력</span><span class="sxs-lookup"><span data-stu-id="35714-127">INPUTS</span></span>

### <span data-ttu-id="35714-128">ARSVault를 통한 명령</span><span class="sxs-lookup"><span data-stu-id="35714-128">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="35714-129">출력</span><span class="sxs-lookup"><span data-stu-id="35714-129">OUTPUTS</span></span>

### <span data-ttu-id="35714-130">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="35714-130">System.Void</span></span>

## <span data-ttu-id="35714-131">상속자</span><span class="sxs-lookup"><span data-stu-id="35714-131">NOTES</span></span>

## <span data-ttu-id="35714-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="35714-132">RELATED LINKS</span></span>

[<span data-ttu-id="35714-133">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="35714-133">Get-AzRecoveryServicesBackupProperty</span></span>](./Get-AzRecoveryServicesBackupProperty.md)

[<span data-ttu-id="35714-134">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="35714-134">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

