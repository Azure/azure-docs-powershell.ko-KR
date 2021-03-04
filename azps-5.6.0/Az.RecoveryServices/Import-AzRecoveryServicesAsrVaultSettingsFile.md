---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/import-azrecoveryservicesasrvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
ms.openlocfilehash: b287e69093ca748d02cd3f630e3b38fb51cdf8f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007675"
---
# <span data-ttu-id="1fe6b-101">Import-AzRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="1fe6b-101">Import-AzRecoveryServicesAsrVaultSettingsFile</span></span>

## <span data-ttu-id="1fe6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fe6b-102">SYNOPSIS</span></span>
<span data-ttu-id="1fe6b-103">지정된 ASR 자격 증명 모음 설정 파일을 가져와 PowerShell 세션에서 후속 ASR 작업에 대한 자격 증명 모음 컨텍스트(PowerShell 세션 컨텍스트)를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1fe6b-103">Imports the specified ASR vault settings file to set the vault context(PowerShell session context) for subsequent ASR operations in the PowerShell session.</span></span> 

## <span data-ttu-id="1fe6b-104">구문</span><span class="sxs-lookup"><span data-stu-id="1fe6b-104">SYNTAX</span></span>

```
Import-AzRecoveryServicesAsrVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fe6b-105">설명</span><span class="sxs-lookup"><span data-stu-id="1fe6b-105">DESCRIPTION</span></span>
<span data-ttu-id="1fe6b-106">**Import-AzRecoveryServicesAsrVaultSettingsFile** cmdlet은 Azure Site Recovery 자격 증명 모음 설정 파일을 가져온다.</span><span class="sxs-lookup"><span data-stu-id="1fe6b-106">The **Import-AzRecoveryServicesAsrVaultSettingsFile** cmdlet imports the Azure Site Recovery vault settings file.</span></span> <span data-ttu-id="1fe6b-107">자격 증명 모음 설정 파일은 현재 세션에서 후속 Azure Site Recovery 작업에 대한 자격 증명 모음 컨텍스트를 설정하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="1fe6b-107">The vault settings file is used to set the vault context for subsequent Azure Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="1fe6b-108">예제</span><span class="sxs-lookup"><span data-stu-id="1fe6b-108">EXAMPLES</span></span>

### <span data-ttu-id="1fe6b-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="1fe6b-109">Example 1</span></span>
```
PS C:\> $VaultSettings = Import-AzRecoveryServicesAsrVaultSettingsFile -Path $FilePath
```

<span data-ttu-id="1fe6b-110">지정된 Recovery Services 자격 증명 모음 설정 파일을 가져오고 가져온 자격 증명 모음의 설정을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="1fe6b-110">Imports the specified Recovery Services vault settings file and returns settings of the imported vault.</span></span>

## <span data-ttu-id="1fe6b-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1fe6b-111">PARAMETERS</span></span>

### <span data-ttu-id="1fe6b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fe6b-112">-DefaultProfile</span></span>
<span data-ttu-id="1fe6b-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1fe6b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="1fe6b-114">-Path</span><span class="sxs-lookup"><span data-stu-id="1fe6b-114">-Path</span></span>
<span data-ttu-id="1fe6b-115">ASR 자격 증명 모음 설정 파일의 폴더 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1fe6b-115">Specifies the folder path of the ASR vault settings file.</span></span>
<span data-ttu-id="1fe6b-116">이 파일은 Recovery Services 자격 증명 모음 포털에서 다운로드하여 로컬로 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1fe6b-116">This file can be downloaded from the Recovery Services vault portal and stored locally.</span></span>

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

### <span data-ttu-id="1fe6b-117">-확인</span><span class="sxs-lookup"><span data-stu-id="1fe6b-117">-Confirm</span></span>
<span data-ttu-id="1fe6b-118">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1fe6b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fe6b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fe6b-119">-WhatIf</span></span>
<span data-ttu-id="1fe6b-120">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="1fe6b-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1fe6b-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1fe6b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fe6b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fe6b-122">CommonParameters</span></span>
<span data-ttu-id="1fe6b-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1fe6b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fe6b-124">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1fe6b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fe6b-125">입력</span><span class="sxs-lookup"><span data-stu-id="1fe6b-125">INPUTS</span></span>

### <span data-ttu-id="1fe6b-126">System.String</span><span class="sxs-lookup"><span data-stu-id="1fe6b-126">System.String</span></span>

## <span data-ttu-id="1fe6b-127">출력</span><span class="sxs-lookup"><span data-stu-id="1fe6b-127">OUTPUTS</span></span>

### <span data-ttu-id="1fe6b-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="1fe6b-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="1fe6b-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1fe6b-129">NOTES</span></span>

## <span data-ttu-id="1fe6b-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1fe6b-130">RELATED LINKS</span></span>

[<span data-ttu-id="1fe6b-131">Get-AzRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="1fe6b-131">Get-AzRecoveryServicesAsrVaultSettingsFile</span></span>](./Get-AzRecoveryServicesAsrVaultSettingsFile.md)
