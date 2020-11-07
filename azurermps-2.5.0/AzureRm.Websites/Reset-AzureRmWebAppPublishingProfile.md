---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/reset-azurermwebapppublishingprofile
schema: 2.0.0
ms.openlocfilehash: f082241be9e31b11782fcbbf5570a7f3c3947012
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880282"
---
# <span data-ttu-id="e6d3f-101">Reset-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="e6d3f-101">Reset-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="e6d3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6d3f-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6d3f-103">구문과</span><span class="sxs-lookup"><span data-stu-id="e6d3f-103">SYNTAX</span></span>

### <span data-ttu-id="e6d3f-104">S1</span><span class="sxs-lookup"><span data-stu-id="e6d3f-104">S1</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6d3f-105">구성원과</span><span class="sxs-lookup"><span data-stu-id="e6d3f-105">S2</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e6d3f-106">설명은</span><span class="sxs-lookup"><span data-stu-id="e6d3f-106">DESCRIPTION</span></span>
<span data-ttu-id="e6d3f-107">**AzureRmWebAppPublishingProfile** cmdlet은 지정 된 웹 앱에 대 한 게시 프로필을 재설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6d3f-107">The **Reset-AzureRmWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="e6d3f-108">예제의</span><span class="sxs-lookup"><span data-stu-id="e6d3f-108">EXAMPLES</span></span>

### <span data-ttu-id="e6d3f-109">raid-1</span><span class="sxs-lookup"><span data-stu-id="e6d3f-109">1:</span></span>
```
PS C:\> Reset-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="e6d3f-110">이 명령은 리소스 그룹 ContosoWebApp에 연결 된 웹 앱에 대 한 게시 프로필을 다시 설정 합니다. 웹-WestUS.</span><span class="sxs-lookup"><span data-stu-id="e6d3f-110">This command resets the publishing profile for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="e6d3f-111">변수</span><span class="sxs-lookup"><span data-stu-id="e6d3f-111">PARAMETERS</span></span>

### <span data-ttu-id="e6d3f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6d3f-112">-DefaultProfile</span></span>
<span data-ttu-id="e6d3f-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e6d3f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6d3f-114">-이름</span><span class="sxs-lookup"><span data-stu-id="e6d3f-114">-Name</span></span>
<span data-ttu-id="e6d3f-115">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="e6d3f-115">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6d3f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6d3f-116">-ResourceGroupName</span></span>
<span data-ttu-id="e6d3f-117">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="e6d3f-117">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6d3f-118">-Web app</span><span class="sxs-lookup"><span data-stu-id="e6d3f-118">-WebApp</span></span>
<span data-ttu-id="e6d3f-119">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="e6d3f-119">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6d3f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6d3f-120">CommonParameters</span></span>
<span data-ttu-id="e6d3f-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6d3f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6d3f-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6d3f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6d3f-123">입력</span><span class="sxs-lookup"><span data-stu-id="e6d3f-123">INPUTS</span></span>

### <span data-ttu-id="e6d3f-124">Site</span><span class="sxs-lookup"><span data-stu-id="e6d3f-124">Site</span></span>
<span data-ttu-id="e6d3f-125">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6d3f-125">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="e6d3f-126">출력</span><span class="sxs-lookup"><span data-stu-id="e6d3f-126">OUTPUTS</span></span>

## <span data-ttu-id="e6d3f-127">상속자</span><span class="sxs-lookup"><span data-stu-id="e6d3f-127">NOTES</span></span>

## <span data-ttu-id="e6d3f-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e6d3f-128">RELATED LINKS</span></span>

