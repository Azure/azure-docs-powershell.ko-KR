---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: C635D723-0F03-4EF8-9435-24DBE0859899
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesBackupProperties.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesBackupProperties.md
ms.openlocfilehash: bb4009edce4e447daacd4cd32835bebc8655dba1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529190"
---
# <span data-ttu-id="2dedb-101">Set-AzureRmRecoveryServicesBackupProperties</span><span class="sxs-lookup"><span data-stu-id="2dedb-101">Set-AzureRmRecoveryServicesBackupProperties</span></span>

## <span data-ttu-id="2dedb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2dedb-102">SYNOPSIS</span></span>
<span data-ttu-id="2dedb-103">백업 관리에 대 한 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2dedb-103">Sets the properties for backup management.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2dedb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2dedb-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesBackupProperties -Vault <ARSVault>
 [-BackupStorageRedundancy <AzureRmRecoveryServicesBackupStorageRedundancyType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2dedb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2dedb-105">DESCRIPTION</span></span>
<span data-ttu-id="2dedb-106">**AzureRmRecoveryServicesBackupProperties** Cmdlet은 복구 서비스 자격 증명 모음에 대 한 백업 저장소 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2dedb-106">The **Set-AzureRmRecoveryServicesBackupProperties** cmdlet sets backup storage properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="2dedb-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2dedb-107">EXAMPLES</span></span>

### <span data-ttu-id="2dedb-108">예제 1: 자격 증명 모음에 대 한 GeoRedundant 저장소 설정</span><span class="sxs-lookup"><span data-stu-id="2dedb-108">Example 1: Set GeoRedundant storage for a vault</span></span>
```
PS C:\> $Vault01 = Get-AzureRmRecoveryServicesVault -Name "TestVault"
PS C:\> Set-AzureRmRecoveryServicesBackupProperties -Vault $Vault01 -BackupStorageRedundancy GeoRedundant
```

<span data-ttu-id="2dedb-109">첫 번째 명령은 TestVault 이라는 자격 증명 모음을 가져온 다음이를 $Vault 01 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2dedb-109">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>

<span data-ttu-id="2dedb-110">두 번째 명령은 $Vault 01에 대 한 백업 저장소 중복성을 GeoRedundant으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2dedb-110">The second command sets the backup storage redundancy for $Vault01 to GeoRedundant.</span></span>

## <span data-ttu-id="2dedb-111">변수</span><span class="sxs-lookup"><span data-stu-id="2dedb-111">PARAMETERS</span></span>

### <span data-ttu-id="2dedb-112">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="2dedb-112">-BackupStorageRedundancy</span></span>
<span data-ttu-id="2dedb-113">백업 저장소 중복성 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2dedb-113">Specifies the backup storage redundancy type.</span></span>

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

### <span data-ttu-id="2dedb-114">-저장실</span><span class="sxs-lookup"><span data-stu-id="2dedb-114">-Vault</span></span>
<span data-ttu-id="2dedb-115">자격 증명 모음의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2dedb-115">Specifies the name of the vault.</span></span>
<span data-ttu-id="2dedb-116">자격 증명 모음이 **AzureRmRecoveryServicesVault** 개체 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2dedb-116">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="2dedb-117">-확인</span><span class="sxs-lookup"><span data-stu-id="2dedb-117">-Confirm</span></span>
<span data-ttu-id="2dedb-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2dedb-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2dedb-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dedb-119">-WhatIf</span></span>
<span data-ttu-id="2dedb-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2dedb-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2dedb-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2dedb-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2dedb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dedb-122">-DefaultProfile</span></span>
<span data-ttu-id="2dedb-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2dedb-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2dedb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dedb-124">CommonParameters</span></span>
<span data-ttu-id="2dedb-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2dedb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dedb-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dedb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dedb-127">입력</span><span class="sxs-lookup"><span data-stu-id="2dedb-127">INPUTS</span></span>

### <span data-ttu-id="2dedb-128">ARSVault</span><span class="sxs-lookup"><span data-stu-id="2dedb-128">ARSVault</span></span>
<span data-ttu-id="2dedb-129">' Vault ' 매개 변수는 파이프라인에서 ' ARSVault ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2dedb-129">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="2dedb-130">출력</span><span class="sxs-lookup"><span data-stu-id="2dedb-130">OUTPUTS</span></span>

## <span data-ttu-id="2dedb-131">상속자</span><span class="sxs-lookup"><span data-stu-id="2dedb-131">NOTES</span></span>

## <span data-ttu-id="2dedb-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2dedb-132">RELATED LINKS</span></span>

[<span data-ttu-id="2dedb-133">Get-AzureRmRecoveryServicesBackupProperties</span><span class="sxs-lookup"><span data-stu-id="2dedb-133">Get-AzureRmRecoveryServicesBackupProperties</span></span>](./Get-AzureRmRecoveryServicesBackupProperties.md)

[<span data-ttu-id="2dedb-134">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="2dedb-134">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)


