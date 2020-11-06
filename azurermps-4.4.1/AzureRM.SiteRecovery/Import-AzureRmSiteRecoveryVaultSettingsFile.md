---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 070DA86E-9EA4-4777-9D53-64B58B4401B8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Import-AzureRmSiteRecoveryVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Import-AzureRmSiteRecoveryVaultSettingsFile.md
ms.openlocfilehash: 42863e0dbf6982ced1f77f916c97ed4fc19d6979
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536168"
---
# <span data-ttu-id="4bd21-101">Import-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="4bd21-101">Import-AzureRmSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="4bd21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bd21-102">SYNOPSIS</span></span>
<span data-ttu-id="4bd21-103">사이트 복구 자격 증명 모음 설정 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4bd21-103">Imports a Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4bd21-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4bd21-104">SYNTAX</span></span>

```
Import-AzureRmSiteRecoveryVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4bd21-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4bd21-105">DESCRIPTION</span></span>
<span data-ttu-id="4bd21-106">**AzureRmSiteRecoveryVaultSettingsFile** Cmdlet은 Azure Site recovery 자격 증명 모음 설정 파일을 가져와 현재 세션의 후속 사이트 복구 작업에 대 한 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bd21-106">The **Import-AzureRmSiteRecoveryVaultSettingsFile** cmdlet imports an Azure Site Recovery vault settings file to set the vault context for subsequent Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="4bd21-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4bd21-107">EXAMPLES</span></span>

## <span data-ttu-id="4bd21-108">변수</span><span class="sxs-lookup"><span data-stu-id="4bd21-108">PARAMETERS</span></span>

### <span data-ttu-id="4bd21-109">-Path</span><span class="sxs-lookup"><span data-stu-id="4bd21-109">-Path</span></span>
<span data-ttu-id="4bd21-110">사이트 복구 자격 증명 모음 설정 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bd21-110">Specifies the path of the Site Recovery vault settings file.</span></span>
<span data-ttu-id="4bd21-111">이 파일은 사이트 복구 자격 증명 모음 포털에서 다운로드 하 여 로컬에 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4bd21-111">This file can be downloaded from the Site Recovery vault portal and stored locally.</span></span>

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

### <span data-ttu-id="4bd21-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bd21-112">-DefaultProfile</span></span>
<span data-ttu-id="4bd21-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4bd21-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4bd21-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bd21-114">CommonParameters</span></span>
<span data-ttu-id="4bd21-115">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bd21-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bd21-116">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bd21-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bd21-117">입력</span><span class="sxs-lookup"><span data-stu-id="4bd21-117">INPUTS</span></span>

## <span data-ttu-id="4bd21-118">출력</span><span class="sxs-lookup"><span data-stu-id="4bd21-118">OUTPUTS</span></span>

### <span data-ttu-id="4bd21-119">SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="4bd21-119">Microsoft.Azure.Commands.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="4bd21-120">상속자</span><span class="sxs-lookup"><span data-stu-id="4bd21-120">NOTES</span></span>

## <span data-ttu-id="4bd21-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4bd21-121">RELATED LINKS</span></span>

[<span data-ttu-id="4bd21-122">Get-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="4bd21-122">Get-AzureRmSiteRecoveryVaultSettingsFile</span></span>](./Get-AzureRmSiteRecoveryVaultSettingsFile.md)
