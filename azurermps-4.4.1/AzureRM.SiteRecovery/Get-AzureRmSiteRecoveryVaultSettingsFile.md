---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 9595E785-6DBF-433C-83B3-8506A3B49B13
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVaultSettingsFile.md
ms.openlocfilehash: 242dfd46b179d1e7d55613d938eddf5b691da6c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711231"
---
# <span data-ttu-id="afb74-101">Get-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="afb74-101">Get-AzureRmSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="afb74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afb74-102">SYNOPSIS</span></span>
<span data-ttu-id="afb74-103">사이트 복구 자격 증명 모음 설정 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="afb74-103">Gets the Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="afb74-104">구문과</span><span class="sxs-lookup"><span data-stu-id="afb74-104">SYNTAX</span></span>

### <span data-ttu-id="afb74-105">ByParam (기본값)</span><span class="sxs-lookup"><span data-stu-id="afb74-105">ByParam (Default)</span></span>
```
Get-AzureRmSiteRecoveryVaultSettingsFile [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="afb74-106">기본값</span><span class="sxs-lookup"><span data-stu-id="afb74-106">Default</span></span>
```
Get-AzureRmSiteRecoveryVaultSettingsFile -Vault <ASRVault> [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="afb74-107">ForSite</span><span class="sxs-lookup"><span data-stu-id="afb74-107">ForSite</span></span>
```
Get-AzureRmSiteRecoveryVaultSettingsFile -Vault <ASRVault> -SiteIdentifier <String> -SiteFriendlyName <String>
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="afb74-108">설명은</span><span class="sxs-lookup"><span data-stu-id="afb74-108">DESCRIPTION</span></span>
<span data-ttu-id="afb74-109">**AzureRmSiteRecoveryVaultSettingsFile** Cmdlet은 Azure Site Recovery 자격 증명 모음에 대 한 설정 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="afb74-109">The **Get-AzureRmSiteRecoveryVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="afb74-110">예제의</span><span class="sxs-lookup"><span data-stu-id="afb74-110">EXAMPLES</span></span>

## <span data-ttu-id="afb74-111">변수</span><span class="sxs-lookup"><span data-stu-id="afb74-111">PARAMETERS</span></span>

### <span data-ttu-id="afb74-112">-Path</span><span class="sxs-lookup"><span data-stu-id="afb74-112">-Path</span></span>
<span data-ttu-id="afb74-113">사이트 복구 자격 증명 모음 설정 파일에 대 한 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="afb74-113">Specifies the path to the Site Recovery vault settings file.</span></span>
<span data-ttu-id="afb74-114">이 파일을 로컬로 저장 하려면 명령이 완료 되 면 사이트 복구 자격 증명 모음 포털에서 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="afb74-114">To store this file locally, download it from the Site Recovery vault portal once the command completes.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, ForSite
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afb74-115">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="afb74-115">-SiteFriendlyName</span></span>
<span data-ttu-id="afb74-116">사이트가 Hyper-v 사이트인 경우 자격 증명 모음의 사이트 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="afb74-116">Specifies the site friendly name for the vault when the site is a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afb74-117">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="afb74-117">-SiteIdentifier</span></span>
<span data-ttu-id="afb74-118">사이트가 Hyper-v 사이트인 경우 자격 증명 모음의 사이트 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="afb74-118">Specifies the site identifier for the vault when the site is a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afb74-119">-저장실</span><span class="sxs-lookup"><span data-stu-id="afb74-119">-Vault</span></span>
<span data-ttu-id="afb74-120">사이트의 자격 증명 모음 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="afb74-120">Specifies the vault object for the site.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRVault
Parameter Sets: Default, ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="afb74-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afb74-121">-DefaultProfile</span></span>
<span data-ttu-id="afb74-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="afb74-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="afb74-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afb74-123">CommonParameters</span></span>
<span data-ttu-id="afb74-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="afb74-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afb74-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afb74-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afb74-126">입력</span><span class="sxs-lookup"><span data-stu-id="afb74-126">INPUTS</span></span>

### <span data-ttu-id="afb74-127">ASRVault</span><span class="sxs-lookup"><span data-stu-id="afb74-127">ASRVault</span></span>
<span data-ttu-id="afb74-128">' Vault ' 매개 변수는 파이프라인에서 ' ASRVault ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="afb74-128">Parameter 'Vault' accepts value of type 'ASRVault' from the pipeline</span></span>

## <span data-ttu-id="afb74-129">출력</span><span class="sxs-lookup"><span data-stu-id="afb74-129">OUTPUTS</span></span>

### <span data-ttu-id="afb74-130">SiteRecovery. VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="afb74-130">Microsoft.Azure.Commands.SiteRecovery.VaultSettingsFilePath</span></span>

## <span data-ttu-id="afb74-131">상속자</span><span class="sxs-lookup"><span data-stu-id="afb74-131">NOTES</span></span>

## <span data-ttu-id="afb74-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="afb74-132">RELATED LINKS</span></span>

[<span data-ttu-id="afb74-133">가져오기-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="afb74-133">Import-AzureRmSiteRecoveryVaultSettingsFile</span></span>](./Import-AzureRmSiteRecoveryVaultSettingsFile.md)

[<span data-ttu-id="afb74-134">Set-AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="afb74-134">Set-AzureRmSiteRecoveryVaultSettings</span></span>](./Set-AzureRmSiteRecoveryVaultSettings.md)
