---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/reset-azurermwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppPublishingProfile.md
ms.openlocfilehash: 096b062325ddfa12eba1d8c0fe8d6a154c3e77fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530824"
---
# <span data-ttu-id="808b1-101">Reset-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="808b1-101">Reset-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="808b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="808b1-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="808b1-103">구문과</span><span class="sxs-lookup"><span data-stu-id="808b1-103">SYNTAX</span></span>

### <span data-ttu-id="808b1-104">S1</span><span class="sxs-lookup"><span data-stu-id="808b1-104">S1</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="808b1-105">구성원과</span><span class="sxs-lookup"><span data-stu-id="808b1-105">S2</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="808b1-106">설명은</span><span class="sxs-lookup"><span data-stu-id="808b1-106">DESCRIPTION</span></span>
<span data-ttu-id="808b1-107">**AzureRmWebAppPublishingProfile** cmdlet은 지정 된 웹 앱에 대 한 게시 프로필을 재설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="808b1-107">The **Reset-AzureRmWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="808b1-108">예제의</span><span class="sxs-lookup"><span data-stu-id="808b1-108">EXAMPLES</span></span>

### <span data-ttu-id="808b1-109">raid-1</span><span class="sxs-lookup"><span data-stu-id="808b1-109">1:</span></span>
```
PS C:\> Reset-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="808b1-110">이 명령은 리소스 그룹 ContosoWebApp에 연결 된 웹 앱에 대 한 게시 프로필을 다시 설정 합니다. 웹-WestUS.</span><span class="sxs-lookup"><span data-stu-id="808b1-110">This command resets the publishing profile for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="808b1-111">변수</span><span class="sxs-lookup"><span data-stu-id="808b1-111">PARAMETERS</span></span>

### <span data-ttu-id="808b1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="808b1-112">-DefaultProfile</span></span>
<span data-ttu-id="808b1-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="808b1-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="808b1-114">-이름</span><span class="sxs-lookup"><span data-stu-id="808b1-114">-Name</span></span>
<span data-ttu-id="808b1-115">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="808b1-115">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="808b1-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="808b1-116">-ResourceGroupName</span></span>
<span data-ttu-id="808b1-117">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="808b1-117">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="808b1-118">-Web app</span><span class="sxs-lookup"><span data-stu-id="808b1-118">-WebApp</span></span>
<span data-ttu-id="808b1-119">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="808b1-119">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="808b1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="808b1-120">CommonParameters</span></span>
<span data-ttu-id="808b1-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="808b1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="808b1-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="808b1-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="808b1-123">입력</span><span class="sxs-lookup"><span data-stu-id="808b1-123">INPUTS</span></span>

### <span data-ttu-id="808b1-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="808b1-124">System.String</span></span>

### <span data-ttu-id="808b1-125">Microsoft. Azure. 사이트</span><span class="sxs-lookup"><span data-stu-id="808b1-125">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="808b1-126">매개 변수: Web app (ByValue)</span><span class="sxs-lookup"><span data-stu-id="808b1-126">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="808b1-127">출력</span><span class="sxs-lookup"><span data-stu-id="808b1-127">OUTPUTS</span></span>

### <span data-ttu-id="808b1-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="808b1-128">System.String</span></span>

## <span data-ttu-id="808b1-129">상속자</span><span class="sxs-lookup"><span data-stu-id="808b1-129">NOTES</span></span>

## <span data-ttu-id="808b1-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="808b1-130">RELATED LINKS</span></span>
