---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Import-AzureRmRecoveryServicesAsrVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Import-AzureRmRecoveryServicesAsrVaultSettingsFile.md
ms.openlocfilehash: ad22cbe1cb17e69358ef386b478fe929abe415b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702425"
---
# <span data-ttu-id="4fc81-101">Import-AzureRmRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="4fc81-101">Import-AzureRmRecoveryServicesAsrVaultSettingsFile</span></span>

## <span data-ttu-id="4fc81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fc81-102">SYNOPSIS</span></span>
<span data-ttu-id="4fc81-103">지정 된 ASR vault 설정 파일을 가져와 PowerShell 세션의 후속 ASR 작업에 대 한 자격 증명 컨텍스트 (PowerShell 세션 컨텍스트)를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fc81-103">Imports the specified ASR vault settings file to set the vault context(PowerShell session context) for subsequent ASR operations in the PowerShell session.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fc81-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4fc81-104">SYNTAX</span></span>

```
Import-AzureRmRecoveryServicesAsrVaultSettingsFile [-Path] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fc81-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4fc81-105">DESCRIPTION</span></span>
<span data-ttu-id="4fc81-106">**AzureRmRecoveryServicesAsrVaultSettingsFile** Cmdlet은 Azure Site Recovery 자격 증명 모음 설정 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4fc81-106">The **Import-AzureRmRecoveryServicesAsrVaultSettingsFile** cmdlet imports the Azure Site Recovery vault settings file.</span></span> <span data-ttu-id="4fc81-107">자격 증명 모음 설정 파일은 현재 세션의 후속 Azure Site Recovery 작업에 대 한 자격 증명 모음 컨텍스트를 설정 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4fc81-107">The vault settings file is used to set the vault context for subsequent Azure Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="4fc81-108">예제의</span><span class="sxs-lookup"><span data-stu-id="4fc81-108">EXAMPLES</span></span>

### <span data-ttu-id="4fc81-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="4fc81-109">Example 1</span></span>
```
PS C:\> $VaultSettings = Import-AzureRmRecoveryServicesAsrVaultSettingsFile -Path $FilePath
```

<span data-ttu-id="4fc81-110">지정 된 복구 서비스 자격 증명 모음 설정 파일을 가져오고 가져온 자격 증명 모음의 설정을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fc81-110">Imports the specified Recovery Services vault settings file and returns settings of the imported vault.</span></span>

## <span data-ttu-id="4fc81-111">변수</span><span class="sxs-lookup"><span data-stu-id="4fc81-111">PARAMETERS</span></span>

### <span data-ttu-id="4fc81-112">-Path</span><span class="sxs-lookup"><span data-stu-id="4fc81-112">-Path</span></span>
<span data-ttu-id="4fc81-113">ASR vault 설정 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fc81-113">Specifies the path of the ASR vault settings file.</span></span>
<span data-ttu-id="4fc81-114">이 파일은 복구 서비스 자격 증명 포털에서 다운로드 하 여 로컬에 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4fc81-114">This file can be downloaded from the Recovery Services vault portal and stored locally.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fc81-115">-확인</span><span class="sxs-lookup"><span data-stu-id="4fc81-115">-Confirm</span></span>
<span data-ttu-id="4fc81-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fc81-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fc81-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fc81-117">-WhatIf</span></span>
<span data-ttu-id="4fc81-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4fc81-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4fc81-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4fc81-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fc81-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fc81-120">CommonParameters</span></span>
<span data-ttu-id="4fc81-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fc81-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fc81-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fc81-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fc81-123">입력</span><span class="sxs-lookup"><span data-stu-id="4fc81-123">INPUTS</span></span>

### <span data-ttu-id="4fc81-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4fc81-124">System.String</span></span>

## <span data-ttu-id="4fc81-125">출력</span><span class="sxs-lookup"><span data-stu-id="4fc81-125">OUTPUTS</span></span>

### <span data-ttu-id="4fc81-126">SiteRecovery. ASRVaultSettings에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="4fc81-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="4fc81-127">상속자</span><span class="sxs-lookup"><span data-stu-id="4fc81-127">NOTES</span></span>

## <span data-ttu-id="4fc81-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4fc81-128">RELATED LINKS</span></span>

[<span data-ttu-id="4fc81-129">Get-AzureRmRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="4fc81-129">Get-AzureRmRecoveryServicesAsrVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesAsrVaultSettingsFile.md)
