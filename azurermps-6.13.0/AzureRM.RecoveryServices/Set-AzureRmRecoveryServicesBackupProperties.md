---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: C635D723-0F03-4EF8-9435-24DBE0859899
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/set-azurermrecoveryservicesbackupproperties
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesBackupProperties.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesBackupProperties.md
ms.openlocfilehash: 7fa55bd306a1cbe04ddf3af63a66682a0fa17f1f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526100"
---
# <span data-ttu-id="2a755-101">Set-AzureRmRecoveryServicesBackupProperties</span><span class="sxs-lookup"><span data-stu-id="2a755-101">Set-AzureRmRecoveryServicesBackupProperties</span></span>

## <span data-ttu-id="2a755-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a755-102">SYNOPSIS</span></span>
<span data-ttu-id="2a755-103">백업 관리에 대 한 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a755-103">Sets the properties for backup management.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a755-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2a755-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesBackupProperties -Vault <ARSVault>
 [-BackupStorageRedundancy <AzureRmRecoveryServicesBackupStorageRedundancyType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a755-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2a755-105">DESCRIPTION</span></span>
<span data-ttu-id="2a755-106">**AzureRmRecoveryServicesBackupProperties** Cmdlet은 복구 서비스 자격 증명 모음에 대 한 백업 저장소 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a755-106">The **Set-AzureRmRecoveryServicesBackupProperties** cmdlet sets backup storage properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="2a755-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2a755-107">EXAMPLES</span></span>

### <span data-ttu-id="2a755-108">예제 1: 자격 증명 모음에 대 한 GeoRedundant 저장소 설정</span><span class="sxs-lookup"><span data-stu-id="2a755-108">Example 1: Set GeoRedundant storage for a vault</span></span>
```
PS C:\> $Vault01 = Get-AzureRmRecoveryServicesVault -Name "TestVault"
PS C:\> Set-AzureRmRecoveryServicesBackupProperties -Vault $Vault01 -BackupStorageRedundancy GeoRedundant
```

<span data-ttu-id="2a755-109">첫 번째 명령은 TestVault 이라는 자격 증명 모음을 가져온 다음이를 $Vault 01 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a755-109">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="2a755-110">두 번째 명령은 $Vault 01에 대 한 백업 저장소 중복성을 GeoRedundant으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a755-110">The second command sets the backup storage redundancy for $Vault01 to GeoRedundant.</span></span>

## <span data-ttu-id="2a755-111">변수</span><span class="sxs-lookup"><span data-stu-id="2a755-111">PARAMETERS</span></span>

### <span data-ttu-id="2a755-112">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="2a755-112">-BackupStorageRedundancy</span></span>
<span data-ttu-id="2a755-113">백업 저장소 중복성 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a755-113">Specifies the backup storage redundancy type.</span></span>

```yaml
Type: AzureRmRecoveryServicesBackupStorageRedundancyType
Parameter Sets: (All)
Aliases:
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a755-114">-저장실</span><span class="sxs-lookup"><span data-stu-id="2a755-114">-Vault</span></span>
<span data-ttu-id="2a755-115">자격 증명 모음의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a755-115">Specifies the name of the vault.</span></span>
<span data-ttu-id="2a755-116">자격 증명 모음이 **AzureRmRecoveryServicesVault** 개체 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a755-116">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a755-117">-확인</span><span class="sxs-lookup"><span data-stu-id="2a755-117">-Confirm</span></span>
<span data-ttu-id="2a755-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a755-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a755-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a755-119">-WhatIf</span></span>
<span data-ttu-id="2a755-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2a755-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2a755-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2a755-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a755-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a755-122">-DefaultProfile</span></span>
<span data-ttu-id="2a755-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2a755-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a755-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a755-124">CommonParameters</span></span>
<span data-ttu-id="2a755-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a755-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a755-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a755-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a755-127">입력</span><span class="sxs-lookup"><span data-stu-id="2a755-127">INPUTS</span></span>

### <span data-ttu-id="2a755-128">ARSVault를 통한 명령</span><span class="sxs-lookup"><span data-stu-id="2a755-128">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>
<span data-ttu-id="2a755-129">매개 변수: 자격 증명 모음 (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2a755-129">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="2a755-130">출력</span><span class="sxs-lookup"><span data-stu-id="2a755-130">OUTPUTS</span></span>

### <span data-ttu-id="2a755-131">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="2a755-131">System.Void</span></span>

## <span data-ttu-id="2a755-132">상속자</span><span class="sxs-lookup"><span data-stu-id="2a755-132">NOTES</span></span>

## <span data-ttu-id="2a755-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2a755-133">RELATED LINKS</span></span>

[<span data-ttu-id="2a755-134">Get-AzureRmRecoveryServicesBackupProperties</span><span class="sxs-lookup"><span data-stu-id="2a755-134">Get-AzureRmRecoveryServicesBackupProperties</span></span>](./Get-AzureRmRecoveryServicesBackupProperties.md)

[<span data-ttu-id="2a755-135">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="2a755-135">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)


