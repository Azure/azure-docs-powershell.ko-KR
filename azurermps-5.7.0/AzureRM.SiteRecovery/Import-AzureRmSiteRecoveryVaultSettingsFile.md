---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 070DA86E-9EA4-4777-9D53-64B58B4401B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/import-azurermsiterecoveryvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Import-AzureRmSiteRecoveryVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Import-AzureRmSiteRecoveryVaultSettingsFile.md
ms.openlocfilehash: 11233414250377331f75e3e8b69f262a0f3a0537
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534615"
---
# <span data-ttu-id="39c8b-101">Import-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="39c8b-101">Import-AzureRmSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="39c8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39c8b-102">SYNOPSIS</span></span>
<span data-ttu-id="39c8b-103">사이트 복구 자격 증명 모음 설정 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="39c8b-103">Imports a Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39c8b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="39c8b-104">SYNTAX</span></span>

```
Import-AzureRmSiteRecoveryVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="39c8b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="39c8b-105">DESCRIPTION</span></span>
<span data-ttu-id="39c8b-106">**AzureRmSiteRecoveryVaultSettingsFile** Cmdlet은 Azure Site recovery 자격 증명 모음 설정 파일을 가져와 현재 세션의 후속 사이트 복구 작업에 대 한 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39c8b-106">The **Import-AzureRmSiteRecoveryVaultSettingsFile** cmdlet imports an Azure Site Recovery vault settings file to set the vault context for subsequent Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="39c8b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="39c8b-107">EXAMPLES</span></span>

## <span data-ttu-id="39c8b-108">변수</span><span class="sxs-lookup"><span data-stu-id="39c8b-108">PARAMETERS</span></span>

### <span data-ttu-id="39c8b-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39c8b-109">-DefaultProfile</span></span>
<span data-ttu-id="39c8b-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="39c8b-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39c8b-111">-Path</span><span class="sxs-lookup"><span data-stu-id="39c8b-111">-Path</span></span>
<span data-ttu-id="39c8b-112">사이트 복구 자격 증명 모음 설정 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39c8b-112">Specifies the path of the Site Recovery vault settings file.</span></span>
<span data-ttu-id="39c8b-113">이 파일은 사이트 복구 자격 증명 모음 포털에서 다운로드 하 여 로컬에 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="39c8b-113">This file can be downloaded from the Site Recovery vault portal and stored locally.</span></span>

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

### <span data-ttu-id="39c8b-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39c8b-114">CommonParameters</span></span>
<span data-ttu-id="39c8b-115">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="39c8b-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39c8b-116">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39c8b-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39c8b-117">입력</span><span class="sxs-lookup"><span data-stu-id="39c8b-117">INPUTS</span></span>

### <span data-ttu-id="39c8b-118">않아야</span><span class="sxs-lookup"><span data-stu-id="39c8b-118">None</span></span>
<span data-ttu-id="39c8b-119">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="39c8b-119">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="39c8b-120">출력</span><span class="sxs-lookup"><span data-stu-id="39c8b-120">OUTPUTS</span></span>

### <span data-ttu-id="39c8b-121">SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="39c8b-121">Microsoft.Azure.Commands.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="39c8b-122">상속자</span><span class="sxs-lookup"><span data-stu-id="39c8b-122">NOTES</span></span>

## <span data-ttu-id="39c8b-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="39c8b-123">RELATED LINKS</span></span>

[<span data-ttu-id="39c8b-124">Get-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="39c8b-124">Get-AzureRmSiteRecoveryVaultSettingsFile</span></span>](./Get-AzureRmSiteRecoveryVaultSettingsFile.md)
