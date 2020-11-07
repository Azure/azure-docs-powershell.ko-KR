---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: F9A652D0-26D9-4F3F-A365-285B05AA7C0B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoverysite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoverySite.md
ms.openlocfilehash: 4a710507321d2f4eb2a605846928f66c5bdb6a4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703976"
---
# <span data-ttu-id="8ff7c-101">Get-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="8ff7c-101">Get-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="8ff7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ff7c-102">SYNOPSIS</span></span>
<span data-ttu-id="8ff7c-103">사이트 복구 자격 증명 모음에서 Hyper-v 사이트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8ff7c-103">Gets the Hyper-V sites from the Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ff7c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8ff7c-104">SYNTAX</span></span>

### <span data-ttu-id="8ff7c-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="8ff7c-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoverySite [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ff7c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="8ff7c-106">ByName</span></span>
```
Get-AzureRmSiteRecoverySite -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ff7c-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="8ff7c-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoverySite -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8ff7c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="8ff7c-108">DESCRIPTION</span></span>
<span data-ttu-id="8ff7c-109">**AzureRmSiteRecoverySite** Cmdlet은 Azure Site Recovery 자격 증명 모음에서 hyper-v 사이트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8ff7c-109">The **Get-AzureRmSiteRecoverySite** cmdlet gets the Hyper-V sites in the Azure Site Recovery vault.</span></span>

## <span data-ttu-id="8ff7c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="8ff7c-110">EXAMPLES</span></span>

## <span data-ttu-id="8ff7c-111">변수</span><span class="sxs-lookup"><span data-stu-id="8ff7c-111">PARAMETERS</span></span>

### <span data-ttu-id="8ff7c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ff7c-112">-DefaultProfile</span></span>
<span data-ttu-id="8ff7c-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8ff7c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ff7c-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="8ff7c-114">-FriendlyName</span></span>
<span data-ttu-id="8ff7c-115">사이트의 친근 한 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ff7c-115">Specifies the friendly name of the site.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ff7c-116">-이름</span><span class="sxs-lookup"><span data-stu-id="8ff7c-116">-Name</span></span>
<span data-ttu-id="8ff7c-117">사이트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ff7c-117">Specifies the name of the site.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ff7c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ff7c-118">CommonParameters</span></span>
<span data-ttu-id="8ff7c-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ff7c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ff7c-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ff7c-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ff7c-121">입력</span><span class="sxs-lookup"><span data-stu-id="8ff7c-121">INPUTS</span></span>

### <span data-ttu-id="8ff7c-122">않아야</span><span class="sxs-lookup"><span data-stu-id="8ff7c-122">None</span></span>
<span data-ttu-id="8ff7c-123">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8ff7c-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8ff7c-124">출력</span><span class="sxs-lookup"><span data-stu-id="8ff7c-124">OUTPUTS</span></span>

### <span data-ttu-id="8ff7c-125">SiteRecovery ' 1 [Microsoft Azure. e r 사이트] 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ff7c-125">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.SiteRecovery.ASRSite]</span></span>

## <span data-ttu-id="8ff7c-126">상속자</span><span class="sxs-lookup"><span data-stu-id="8ff7c-126">NOTES</span></span>

## <span data-ttu-id="8ff7c-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8ff7c-127">RELATED LINKS</span></span>

[<span data-ttu-id="8ff7c-128">새로운 AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="8ff7c-128">New-AzureRmSiteRecoverySite</span></span>](./New-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="8ff7c-129">제거-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="8ff7c-129">Remove-AzureRmSiteRecoverySite</span></span>](./Remove-AzureRmSiteRecoverySite.md)
