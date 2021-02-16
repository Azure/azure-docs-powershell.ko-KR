---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/import-azrecoveryservicesasrvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
ms.openlocfilehash: f71f7e37e4864de10c5387d63c101cd66ed9fd34
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398498"
---
# <span data-ttu-id="b1185-101">Import-AzRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="b1185-101">Import-AzRecoveryServicesAsrVaultSettingsFile</span></span>

## <span data-ttu-id="b1185-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1185-102">SYNOPSIS</span></span>
<span data-ttu-id="b1185-103">지정된 ASR 자격 증명 모음 설정 파일을 가져와서 PowerShell 세션에서 후속 ASR 작업에 대한 자격 증명 모음 컨텍스트(PowerShell 세션 컨텍스트)를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b1185-103">Imports the specified ASR vault settings file to set the vault context(PowerShell session context) for subsequent ASR operations in the PowerShell session.</span></span> 

## <span data-ttu-id="b1185-104">구문</span><span class="sxs-lookup"><span data-stu-id="b1185-104">SYNTAX</span></span>

```
Import-AzRecoveryServicesAsrVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1185-105">설명</span><span class="sxs-lookup"><span data-stu-id="b1185-105">DESCRIPTION</span></span>
<span data-ttu-id="b1185-106">**Import-AzRecoveryServicesAsrVaultSettingsFile** cmdlet은 Azure Site Recovery 자격 증명 모음 설정 파일을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1185-106">The **Import-AzRecoveryServicesAsrVaultSettingsFile** cmdlet imports the Azure Site Recovery vault settings file.</span></span> <span data-ttu-id="b1185-107">자격 증명 모음 설정 파일은 현재 세션에서 후속 Azure Site Recovery 작업에 대한 자격 증명 모음 컨텍스트를 설정하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1185-107">The vault settings file is used to set the vault context for subsequent Azure Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="b1185-108">예제</span><span class="sxs-lookup"><span data-stu-id="b1185-108">EXAMPLES</span></span>

### <span data-ttu-id="b1185-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="b1185-109">Example 1</span></span>
```
PS C:\> $VaultSettings = Import-AzRecoveryServicesAsrVaultSettingsFile -Path $FilePath
```

<span data-ttu-id="b1185-110">지정된 Recovery Services 자격 증명 모음 설정 파일을 가져오고 가져온 자격 증명 모음의 설정을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="b1185-110">Imports the specified Recovery Services vault settings file and returns settings of the imported vault.</span></span>

## <span data-ttu-id="b1185-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1185-111">PARAMETERS</span></span>

### <span data-ttu-id="b1185-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1185-112">-DefaultProfile</span></span>
<span data-ttu-id="b1185-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b1185-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="b1185-114">-Path</span><span class="sxs-lookup"><span data-stu-id="b1185-114">-Path</span></span>
<span data-ttu-id="b1185-115">ASR 자격 증명 모음 설정 파일의 폴더 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b1185-115">Specifies the folder path of the ASR vault settings file.</span></span>
<span data-ttu-id="b1185-116">이 파일은 Recovery Services 자격 증명 모음 포털에서 다운로드하여 로컬로 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1185-116">This file can be downloaded from the Recovery Services vault portal and stored locally.</span></span>

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

### <span data-ttu-id="b1185-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b1185-117">-Confirm</span></span>
<span data-ttu-id="b1185-118">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1185-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1185-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1185-119">-WhatIf</span></span>
<span data-ttu-id="b1185-120">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b1185-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b1185-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b1185-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1185-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1185-122">CommonParameters</span></span>
<span data-ttu-id="b1185-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b1185-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1185-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b1185-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1185-125">입력</span><span class="sxs-lookup"><span data-stu-id="b1185-125">INPUTS</span></span>

### <span data-ttu-id="b1185-126">System.String</span><span class="sxs-lookup"><span data-stu-id="b1185-126">System.String</span></span>

## <span data-ttu-id="b1185-127">출력</span><span class="sxs-lookup"><span data-stu-id="b1185-127">OUTPUTS</span></span>

### <span data-ttu-id="b1185-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="b1185-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="b1185-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b1185-129">NOTES</span></span>

## <span data-ttu-id="b1185-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b1185-130">RELATED LINKS</span></span>
