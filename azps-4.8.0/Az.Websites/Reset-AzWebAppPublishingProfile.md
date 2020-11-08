---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/reset-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
ms.openlocfilehash: 81005ceac6bfa3c258a147f3fbef168e95c302cb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056015"
---
# <span data-ttu-id="4a4a0-101">Reset-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="4a4a0-101">Reset-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="4a4a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a4a0-102">SYNOPSIS</span></span>

## <span data-ttu-id="4a4a0-103">구문과</span><span class="sxs-lookup"><span data-stu-id="4a4a0-103">SYNTAX</span></span>

### <span data-ttu-id="4a4a0-104">S1</span><span class="sxs-lookup"><span data-stu-id="4a4a0-104">S1</span></span>
```
Reset-AzWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a4a0-105">구성원과</span><span class="sxs-lookup"><span data-stu-id="4a4a0-105">S2</span></span>
```
Reset-AzWebAppPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4a4a0-106">설명은</span><span class="sxs-lookup"><span data-stu-id="4a4a0-106">DESCRIPTION</span></span>
<span data-ttu-id="4a4a0-107">**AzWebAppPublishingProfile** cmdlet은 지정 된 웹 앱에 대 한 게시 프로필을 재설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a4a0-107">The **Reset-AzWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="4a4a0-108">예제의</span><span class="sxs-lookup"><span data-stu-id="4a4a0-108">EXAMPLES</span></span>

### <span data-ttu-id="4a4a0-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="4a4a0-109">Example 1</span></span>

<span data-ttu-id="4a4a0-110">다음 예제에서는 리소스 그룹 MyResourceGroup과 연결 된 웹 앱 IpRule의 게시 프로필을 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a4a0-110">The following example resets the publishing profile for the Web App IpRule associated with the resource group MyResourceGroup.</span></span>

```powershell <!-- Aladdin Generated Example --> 
Reset-AzWebAppPublishingProfile -Name IpRule -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="4a4a0-111">변수</span><span class="sxs-lookup"><span data-stu-id="4a4a0-111">PARAMETERS</span></span>

### <span data-ttu-id="4a4a0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a4a0-112">-DefaultProfile</span></span>
<span data-ttu-id="4a4a0-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4a4a0-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a4a0-114">-이름</span><span class="sxs-lookup"><span data-stu-id="4a4a0-114">-Name</span></span>
<span data-ttu-id="4a4a0-115">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="4a4a0-115">WebApp Name</span></span>

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

### <span data-ttu-id="4a4a0-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a4a0-116">-ResourceGroupName</span></span>
<span data-ttu-id="4a4a0-117">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="4a4a0-117">Resource Group Name</span></span>

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

### <span data-ttu-id="4a4a0-118">-Web app</span><span class="sxs-lookup"><span data-stu-id="4a4a0-118">-WebApp</span></span>
<span data-ttu-id="4a4a0-119">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="4a4a0-119">WebApp Object</span></span>

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

### <span data-ttu-id="4a4a0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a4a0-120">CommonParameters</span></span>
<span data-ttu-id="4a4a0-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a4a0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a4a0-122">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a4a0-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a4a0-123">입력</span><span class="sxs-lookup"><span data-stu-id="4a4a0-123">INPUTS</span></span>

### <span data-ttu-id="4a4a0-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4a4a0-124">System.String</span></span>

### <span data-ttu-id="4a4a0-125">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="4a4a0-125">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="4a4a0-126">출력</span><span class="sxs-lookup"><span data-stu-id="4a4a0-126">OUTPUTS</span></span>

### <span data-ttu-id="4a4a0-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4a4a0-127">System.String</span></span>

## <span data-ttu-id="4a4a0-128">상속자</span><span class="sxs-lookup"><span data-stu-id="4a4a0-128">NOTES</span></span>

## <span data-ttu-id="4a4a0-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4a4a0-129">RELATED LINKS</span></span>
