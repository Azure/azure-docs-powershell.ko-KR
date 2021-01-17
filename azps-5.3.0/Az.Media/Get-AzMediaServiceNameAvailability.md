---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 23C6C9D3-A745-46C8-AB2C-B874223FBFFF
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservicenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
ms.openlocfilehash: d7718ffafd6383e0873e61955cd231ca8b6a409d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380745"
---
# <span data-ttu-id="d0376-101">Get-AzMediaServiceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="d0376-101">Get-AzMediaServiceNameAvailability</span></span>

## <span data-ttu-id="d0376-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0376-102">SYNOPSIS</span></span>
<span data-ttu-id="d0376-103">미디어 서비스 이름을 사용할 수 있는지 여부를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="d0376-103">Checks whether a media service name is available.</span></span>
<span data-ttu-id="d0376-104">미디어 서비스 이름은 전역적으로 고유합니다.</span><span class="sxs-lookup"><span data-stu-id="d0376-104">Media service names are globally unique.</span></span>

## <span data-ttu-id="d0376-105">구문</span><span class="sxs-lookup"><span data-stu-id="d0376-105">SYNTAX</span></span>

```
Get-AzMediaServiceNameAvailability [-DefaultProfile <IAzureContextContainer>] [-AccountName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="d0376-106">설명</span><span class="sxs-lookup"><span data-stu-id="d0376-106">DESCRIPTION</span></span>
<span data-ttu-id="d0376-107">**Get-AzMediaServiceNameAvailability** cmdlet은 미디어 서비스 이름을 사용할 수 있는지 여부를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="d0376-107">The **Get-AzMediaServiceNameAvailability** cmdlet checks whether a media service name is available.</span></span>
<span data-ttu-id="d0376-108">미디어 서비스 이름은 전역적으로 고유합니다.</span><span class="sxs-lookup"><span data-stu-id="d0376-108">Media service names are globally unique.</span></span>

## <span data-ttu-id="d0376-109">예제</span><span class="sxs-lookup"><span data-stu-id="d0376-109">EXAMPLES</span></span>

### <span data-ttu-id="d0376-110">예제 1: Media Service 이름을 사용할 수 있는지 확인</span><span class="sxs-lookup"><span data-stu-id="d0376-110">Example 1: Check whether a Media Service name is available</span></span>
```
PS C:\>Get-AzMediaServiceNameAvailability -AccountName "MediaService1"
```

<span data-ttu-id="d0376-111">이 명령은 MediaService1 이름을 사용할 수 있는지 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="d0376-111">This command checks if the name MediaService1 is available.</span></span>

## <span data-ttu-id="d0376-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0376-112">PARAMETERS</span></span>

### <span data-ttu-id="d0376-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d0376-113">-AccountName</span></span>
<span data-ttu-id="d0376-114">이 cmdlet이 제공하는 미디어 서비스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d0376-114">Specifies the name of the media service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d0376-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0376-115">-DefaultProfile</span></span>
<span data-ttu-id="d0376-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d0376-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d0376-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0376-117">CommonParameters</span></span>
<span data-ttu-id="d0376-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d0376-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0376-119">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d0376-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0376-120">입력</span><span class="sxs-lookup"><span data-stu-id="d0376-120">INPUTS</span></span>

### <span data-ttu-id="d0376-121">없음</span><span class="sxs-lookup"><span data-stu-id="d0376-121">None</span></span>

## <span data-ttu-id="d0376-122">출력</span><span class="sxs-lookup"><span data-stu-id="d0376-122">OUTPUTS</span></span>

### <span data-ttu-id="d0376-123">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="d0376-123">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="d0376-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d0376-124">NOTES</span></span>

## <span data-ttu-id="d0376-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d0376-125">RELATED LINKS</span></span>

[<span data-ttu-id="d0376-126">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="d0376-126">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="d0376-127">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="d0376-127">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="d0376-128">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="d0376-128">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="d0376-129">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="d0376-129">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


