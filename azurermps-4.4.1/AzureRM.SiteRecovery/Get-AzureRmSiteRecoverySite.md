---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: F9A652D0-26D9-4F3F-A365-285B05AA7C0B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoverySite.md
ms.openlocfilehash: e41b491611ebc5dda1da56ac26827c5fa547dd4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529112"
---
# <span data-ttu-id="123b2-101">Get-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="123b2-101">Get-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="123b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="123b2-102">SYNOPSIS</span></span>
<span data-ttu-id="123b2-103">사이트 복구 자격 증명 모음에서 Hyper-v 사이트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="123b2-103">Gets the Hyper-V sites from the Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="123b2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="123b2-104">SYNTAX</span></span>

### <span data-ttu-id="123b2-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="123b2-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoverySite [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="123b2-106">ByName</span><span class="sxs-lookup"><span data-stu-id="123b2-106">ByName</span></span>
```
Get-AzureRmSiteRecoverySite -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="123b2-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="123b2-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoverySite -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="123b2-108">설명은</span><span class="sxs-lookup"><span data-stu-id="123b2-108">DESCRIPTION</span></span>
<span data-ttu-id="123b2-109">**AzureRmSiteRecoverySite** Cmdlet은 Azure Site Recovery 자격 증명 모음에서 hyper-v 사이트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="123b2-109">The **Get-AzureRmSiteRecoverySite** cmdlet gets the Hyper-V sites in the Azure Site Recovery vault.</span></span>

## <span data-ttu-id="123b2-110">예제의</span><span class="sxs-lookup"><span data-stu-id="123b2-110">EXAMPLES</span></span>

## <span data-ttu-id="123b2-111">변수</span><span class="sxs-lookup"><span data-stu-id="123b2-111">PARAMETERS</span></span>

### <span data-ttu-id="123b2-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="123b2-112">-FriendlyName</span></span>
<span data-ttu-id="123b2-113">사이트의 친근 한 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="123b2-113">Specifies the friendly name of the site.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="123b2-114">-이름</span><span class="sxs-lookup"><span data-stu-id="123b2-114">-Name</span></span>
<span data-ttu-id="123b2-115">사이트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="123b2-115">Specifies the name of the site.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="123b2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="123b2-116">-DefaultProfile</span></span>
<span data-ttu-id="123b2-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="123b2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="123b2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="123b2-118">CommonParameters</span></span>
<span data-ttu-id="123b2-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="123b2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="123b2-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="123b2-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="123b2-121">입력</span><span class="sxs-lookup"><span data-stu-id="123b2-121">INPUTS</span></span>

## <span data-ttu-id="123b2-122">출력</span><span class="sxs-lookup"><span data-stu-id="123b2-122">OUTPUTS</span></span>

### <span data-ttu-id="123b2-123">SiteRecovery ' 1 [Microsoft Azure. e r 사이트] 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="123b2-123">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.SiteRecovery.ASRSite]</span></span>

## <span data-ttu-id="123b2-124">상속자</span><span class="sxs-lookup"><span data-stu-id="123b2-124">NOTES</span></span>

## <span data-ttu-id="123b2-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="123b2-125">RELATED LINKS</span></span>

[<span data-ttu-id="123b2-126">새로운 AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="123b2-126">New-AzureRmSiteRecoverySite</span></span>](./New-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="123b2-127">제거-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="123b2-127">Remove-AzureRmSiteRecoverySite</span></span>](./Remove-AzureRmSiteRecoverySite.md)
