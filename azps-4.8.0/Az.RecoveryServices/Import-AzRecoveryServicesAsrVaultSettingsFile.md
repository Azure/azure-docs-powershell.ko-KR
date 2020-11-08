---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/import-azrecoveryservicesasrvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
ms.openlocfilehash: de3604a4bf1f9c46bf88b2f3cda25982672e9096
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047690"
---
# <span data-ttu-id="015c3-101">Import-AzRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="015c3-101">Import-AzRecoveryServicesAsrVaultSettingsFile</span></span>

## <span data-ttu-id="015c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="015c3-102">SYNOPSIS</span></span>
<span data-ttu-id="015c3-103">지정 된 ASR vault 설정 파일을 가져와 PowerShell 세션의 후속 ASR 작업에 대 한 자격 증명 컨텍스트 (PowerShell 세션 컨텍스트)를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="015c3-103">Imports the specified ASR vault settings file to set the vault context(PowerShell session context) for subsequent ASR operations in the PowerShell session.</span></span> 

## <span data-ttu-id="015c3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="015c3-104">SYNTAX</span></span>

```
Import-AzRecoveryServicesAsrVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="015c3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="015c3-105">DESCRIPTION</span></span>
<span data-ttu-id="015c3-106">**AzRecoveryServicesAsrVaultSettingsFile** Cmdlet은 Azure Site Recovery 자격 증명 모음 설정 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="015c3-106">The **Import-AzRecoveryServicesAsrVaultSettingsFile** cmdlet imports the Azure Site Recovery vault settings file.</span></span> <span data-ttu-id="015c3-107">자격 증명 모음 설정 파일은 현재 세션의 후속 Azure Site Recovery 작업에 대 한 자격 증명 모음 컨텍스트를 설정 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="015c3-107">The vault settings file is used to set the vault context for subsequent Azure Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="015c3-108">예제의</span><span class="sxs-lookup"><span data-stu-id="015c3-108">EXAMPLES</span></span>

### <span data-ttu-id="015c3-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="015c3-109">Example 1</span></span>
```
PS C:\> $VaultSettings = Import-AzRecoveryServicesAsrVaultSettingsFile -Path $FilePath
```

<span data-ttu-id="015c3-110">지정 된 복구 서비스 자격 증명 모음 설정 파일을 가져오고 가져온 자격 증명 모음의 설정을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="015c3-110">Imports the specified Recovery Services vault settings file and returns settings of the imported vault.</span></span>

## <span data-ttu-id="015c3-111">변수</span><span class="sxs-lookup"><span data-stu-id="015c3-111">PARAMETERS</span></span>

### <span data-ttu-id="015c3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="015c3-112">-DefaultProfile</span></span>
<span data-ttu-id="015c3-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="015c3-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="015c3-114">-Path</span><span class="sxs-lookup"><span data-stu-id="015c3-114">-Path</span></span>
<span data-ttu-id="015c3-115">ASR vault 설정 파일의 폴더 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="015c3-115">Specifies the folder path of the ASR vault settings file.</span></span>
<span data-ttu-id="015c3-116">이 파일은 복구 서비스 자격 증명 포털에서 다운로드 하 여 로컬에 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="015c3-116">This file can be downloaded from the Recovery Services vault portal and stored locally.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="015c3-117">-확인</span><span class="sxs-lookup"><span data-stu-id="015c3-117">-Confirm</span></span>
<span data-ttu-id="015c3-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="015c3-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="015c3-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="015c3-119">-WhatIf</span></span>
<span data-ttu-id="015c3-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="015c3-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="015c3-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="015c3-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="015c3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="015c3-122">CommonParameters</span></span>
<span data-ttu-id="015c3-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="015c3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="015c3-124">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="015c3-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="015c3-125">입력</span><span class="sxs-lookup"><span data-stu-id="015c3-125">INPUTS</span></span>

### <span data-ttu-id="015c3-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="015c3-126">System.String</span></span>

## <span data-ttu-id="015c3-127">출력</span><span class="sxs-lookup"><span data-stu-id="015c3-127">OUTPUTS</span></span>

### <span data-ttu-id="015c3-128">SiteRecovery. ASRVaultSettings에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="015c3-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="015c3-129">상속자</span><span class="sxs-lookup"><span data-stu-id="015c3-129">NOTES</span></span>

## <span data-ttu-id="015c3-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="015c3-130">RELATED LINKS</span></span>

[<span data-ttu-id="015c3-131">Get-AzRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="015c3-131">Get-AzRecoveryServicesAsrVaultSettingsFile</span></span>](./Get-AzRecoveryServicesAsrVaultSettingsFile.md)
