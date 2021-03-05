---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 23C6C9D3-A745-46C8-AB2C-B874223FBFFF
online version: https://docs.microsoft.com/powershell/module/az.media/get-azmediaservicenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
ms.openlocfilehash: d8928aea539910751c61ad03f5e5a4d67188e371
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960464"
---
# <span data-ttu-id="97851-101">Get-AzMediaServiceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="97851-101">Get-AzMediaServiceNameAvailability</span></span>

## <span data-ttu-id="97851-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97851-102">SYNOPSIS</span></span>
<span data-ttu-id="97851-103">미디어 서비스 이름을 사용할 수 있는지 여부를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="97851-103">Checks whether a media service name is available.</span></span>
<span data-ttu-id="97851-104">미디어 서비스 이름은 전역적으로 고유합니다.</span><span class="sxs-lookup"><span data-stu-id="97851-104">Media service names are globally unique.</span></span>

## <span data-ttu-id="97851-105">구문</span><span class="sxs-lookup"><span data-stu-id="97851-105">SYNTAX</span></span>

```
Get-AzMediaServiceNameAvailability [-DefaultProfile <IAzureContextContainer>] [-AccountName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="97851-106">설명</span><span class="sxs-lookup"><span data-stu-id="97851-106">DESCRIPTION</span></span>
<span data-ttu-id="97851-107">**Get-AzMediaServiceNameAvailability** cmdlet은 미디어 서비스 이름을 사용할 수 있는지 여부를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="97851-107">The **Get-AzMediaServiceNameAvailability** cmdlet checks whether a media service name is available.</span></span>
<span data-ttu-id="97851-108">미디어 서비스 이름은 전역적으로 고유합니다.</span><span class="sxs-lookup"><span data-stu-id="97851-108">Media service names are globally unique.</span></span>

## <span data-ttu-id="97851-109">예제</span><span class="sxs-lookup"><span data-stu-id="97851-109">EXAMPLES</span></span>

### <span data-ttu-id="97851-110">예제 1: Media Service 이름을 사용할 수 있는지 확인</span><span class="sxs-lookup"><span data-stu-id="97851-110">Example 1: Check whether a Media Service name is available</span></span>
```
PS C:\>Get-AzMediaServiceNameAvailability -AccountName "MediaService1"
```

<span data-ttu-id="97851-111">이 명령은 MediaService1 이름을 사용할 수 있는지 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="97851-111">This command checks if the name MediaService1 is available.</span></span>

## <span data-ttu-id="97851-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="97851-112">PARAMETERS</span></span>

### <span data-ttu-id="97851-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="97851-113">-AccountName</span></span>
<span data-ttu-id="97851-114">이 cmdlet이 제공하는 미디어 서비스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="97851-114">Specifies the name of the media service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97851-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97851-115">-DefaultProfile</span></span>
<span data-ttu-id="97851-116">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="97851-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97851-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97851-117">CommonParameters</span></span>
<span data-ttu-id="97851-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="97851-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97851-119">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="97851-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97851-120">입력</span><span class="sxs-lookup"><span data-stu-id="97851-120">INPUTS</span></span>

### <span data-ttu-id="97851-121">없음</span><span class="sxs-lookup"><span data-stu-id="97851-121">None</span></span>

## <span data-ttu-id="97851-122">출력</span><span class="sxs-lookup"><span data-stu-id="97851-122">OUTPUTS</span></span>

### <span data-ttu-id="97851-123">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="97851-123">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="97851-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="97851-124">NOTES</span></span>

## <span data-ttu-id="97851-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="97851-125">RELATED LINKS</span></span>

[<span data-ttu-id="97851-126">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="97851-126">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="97851-127">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="97851-127">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="97851-128">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="97851-128">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="97851-129">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="97851-129">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


