---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/reset-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
ms.openlocfilehash: 81eaa3b287a14cdc9aa71150c2f0b3724aeb4f4b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874118"
---
# <span data-ttu-id="ef5bc-101">Reset-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="ef5bc-101">Reset-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="ef5bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef5bc-102">SYNOPSIS</span></span>

## <span data-ttu-id="ef5bc-103">구문과</span><span class="sxs-lookup"><span data-stu-id="ef5bc-103">SYNTAX</span></span>

### <span data-ttu-id="ef5bc-104">S1</span><span class="sxs-lookup"><span data-stu-id="ef5bc-104">S1</span></span>
```
Reset-AzWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef5bc-105">구성원과</span><span class="sxs-lookup"><span data-stu-id="ef5bc-105">S2</span></span>
```
Reset-AzWebAppPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ef5bc-106">설명은</span><span class="sxs-lookup"><span data-stu-id="ef5bc-106">DESCRIPTION</span></span>
<span data-ttu-id="ef5bc-107">**AzWebAppPublishingProfile** cmdlet은 지정 된 웹 앱에 대 한 게시 프로필을 재설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef5bc-107">The **Reset-AzWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="ef5bc-108">예제의</span><span class="sxs-lookup"><span data-stu-id="ef5bc-108">EXAMPLES</span></span>

### <span data-ttu-id="ef5bc-109">raid-1</span><span class="sxs-lookup"><span data-stu-id="ef5bc-109">1:</span></span>
```
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="ef5bc-110">이 명령은 리소스 그룹 ContosoWebApp에 연결 된 웹 앱에 대 한 게시 프로필을 다시 설정 합니다. 웹-WestUS.</span><span class="sxs-lookup"><span data-stu-id="ef5bc-110">This command resets the publishing profile for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="ef5bc-111">변수</span><span class="sxs-lookup"><span data-stu-id="ef5bc-111">PARAMETERS</span></span>

### <span data-ttu-id="ef5bc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef5bc-112">-DefaultProfile</span></span>
<span data-ttu-id="ef5bc-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ef5bc-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef5bc-114">-이름</span><span class="sxs-lookup"><span data-stu-id="ef5bc-114">-Name</span></span>
<span data-ttu-id="ef5bc-115">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="ef5bc-115">WebApp Name</span></span>

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

### <span data-ttu-id="ef5bc-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef5bc-116">-ResourceGroupName</span></span>
<span data-ttu-id="ef5bc-117">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="ef5bc-117">Resource Group Name</span></span>

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

### <span data-ttu-id="ef5bc-118">-Web app</span><span class="sxs-lookup"><span data-stu-id="ef5bc-118">-WebApp</span></span>
<span data-ttu-id="ef5bc-119">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="ef5bc-119">WebApp Object</span></span>

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

### <span data-ttu-id="ef5bc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef5bc-120">CommonParameters</span></span>
<span data-ttu-id="ef5bc-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef5bc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef5bc-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef5bc-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef5bc-123">입력</span><span class="sxs-lookup"><span data-stu-id="ef5bc-123">INPUTS</span></span>

### <span data-ttu-id="ef5bc-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ef5bc-124">System.String</span></span>

### <span data-ttu-id="ef5bc-125">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="ef5bc-125">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ef5bc-126">출력</span><span class="sxs-lookup"><span data-stu-id="ef5bc-126">OUTPUTS</span></span>

### <span data-ttu-id="ef5bc-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ef5bc-127">System.String</span></span>

## <span data-ttu-id="ef5bc-128">상속자</span><span class="sxs-lookup"><span data-stu-id="ef5bc-128">NOTES</span></span>

## <span data-ttu-id="ef5bc-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ef5bc-129">RELATED LINKS</span></span>
