---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 23C6C9D3-A745-46C8-AB2C-B874223FBFFF
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservicenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
ms.openlocfilehash: d7718ffafd6383e0873e61955cd231ca8b6a409d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207168"
---
# <span data-ttu-id="54b8e-101">Get-AzMediaServiceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="54b8e-101">Get-AzMediaServiceNameAvailability</span></span>

## <span data-ttu-id="54b8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54b8e-102">SYNOPSIS</span></span>
<span data-ttu-id="54b8e-103">미디어 서비스 이름을 사용할 수 있는지 여부를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="54b8e-103">Checks whether a media service name is available.</span></span>
<span data-ttu-id="54b8e-104">미디어 서비스 이름은 전역적으로 고유합니다.</span><span class="sxs-lookup"><span data-stu-id="54b8e-104">Media service names are globally unique.</span></span>

## <span data-ttu-id="54b8e-105">구문</span><span class="sxs-lookup"><span data-stu-id="54b8e-105">SYNTAX</span></span>

```
Get-AzMediaServiceNameAvailability [-DefaultProfile <IAzureContextContainer>] [-AccountName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="54b8e-106">설명</span><span class="sxs-lookup"><span data-stu-id="54b8e-106">DESCRIPTION</span></span>
<span data-ttu-id="54b8e-107">**Get-AzMediaServiceNameAvailability** cmdlet은 미디어 서비스 이름을 사용할 수 있는지 여부를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="54b8e-107">The **Get-AzMediaServiceNameAvailability** cmdlet checks whether a media service name is available.</span></span>
<span data-ttu-id="54b8e-108">미디어 서비스 이름은 전역적으로 고유합니다.</span><span class="sxs-lookup"><span data-stu-id="54b8e-108">Media service names are globally unique.</span></span>

## <span data-ttu-id="54b8e-109">예제</span><span class="sxs-lookup"><span data-stu-id="54b8e-109">EXAMPLES</span></span>

### <span data-ttu-id="54b8e-110">예제 1: Media Service 이름을 사용할 수 있는지 확인</span><span class="sxs-lookup"><span data-stu-id="54b8e-110">Example 1: Check whether a Media Service name is available</span></span>
```
PS C:\>Get-AzMediaServiceNameAvailability -AccountName "MediaService1"
```

<span data-ttu-id="54b8e-111">이 명령은 MediaService1 이름을 사용할 수 있는지 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="54b8e-111">This command checks if the name MediaService1 is available.</span></span>

## <span data-ttu-id="54b8e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54b8e-112">PARAMETERS</span></span>

### <span data-ttu-id="54b8e-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="54b8e-113">-AccountName</span></span>
<span data-ttu-id="54b8e-114">이 cmdlet이 제공하는 미디어 서비스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="54b8e-114">Specifies the name of the media service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="54b8e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54b8e-115">-DefaultProfile</span></span>
<span data-ttu-id="54b8e-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="54b8e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54b8e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54b8e-117">CommonParameters</span></span>
<span data-ttu-id="54b8e-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="54b8e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54b8e-119">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="54b8e-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54b8e-120">입력</span><span class="sxs-lookup"><span data-stu-id="54b8e-120">INPUTS</span></span>

### <span data-ttu-id="54b8e-121">없음</span><span class="sxs-lookup"><span data-stu-id="54b8e-121">None</span></span>

## <span data-ttu-id="54b8e-122">출력</span><span class="sxs-lookup"><span data-stu-id="54b8e-122">OUTPUTS</span></span>

### <span data-ttu-id="54b8e-123">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="54b8e-123">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="54b8e-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="54b8e-124">NOTES</span></span>

## <span data-ttu-id="54b8e-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="54b8e-125">RELATED LINKS</span></span>

[<span data-ttu-id="54b8e-126">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="54b8e-126">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="54b8e-127">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="54b8e-127">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="54b8e-128">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="54b8e-128">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="54b8e-129">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="54b8e-129">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


