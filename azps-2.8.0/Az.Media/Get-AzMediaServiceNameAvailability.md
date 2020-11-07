---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 23C6C9D3-A745-46C8-AB2C-B874223FBFFF
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservicenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
ms.openlocfilehash: 8c62bf114feee8f9b87e2b7ca35b4c67b423ed66
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689366"
---
# <span data-ttu-id="15443-101">Get-AzMediaServiceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="15443-101">Get-AzMediaServiceNameAvailability</span></span>

## <span data-ttu-id="15443-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15443-102">SYNOPSIS</span></span>
<span data-ttu-id="15443-103">미디어 서비스 이름을 사용할 수 있는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="15443-103">Checks whether a media service name is available.</span></span>
<span data-ttu-id="15443-104">미디어 서비스 이름은 전역적으로 고유 합니다.</span><span class="sxs-lookup"><span data-stu-id="15443-104">Media service names are globally unique.</span></span>

## <span data-ttu-id="15443-105">구문과</span><span class="sxs-lookup"><span data-stu-id="15443-105">SYNTAX</span></span>

```
Get-AzMediaServiceNameAvailability [-DefaultProfile <IAzureContextContainer>] [-AccountName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="15443-106">설명은</span><span class="sxs-lookup"><span data-stu-id="15443-106">DESCRIPTION</span></span>
<span data-ttu-id="15443-107">**AzMediaServiceNameAvailability** cmdlet은 미디어 서비스 이름을 사용할 수 있는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="15443-107">The **Get-AzMediaServiceNameAvailability** cmdlet checks whether a media service name is available.</span></span>
<span data-ttu-id="15443-108">미디어 서비스 이름은 전역적으로 고유 합니다.</span><span class="sxs-lookup"><span data-stu-id="15443-108">Media service names are globally unique.</span></span>

## <span data-ttu-id="15443-109">예제의</span><span class="sxs-lookup"><span data-stu-id="15443-109">EXAMPLES</span></span>

### <span data-ttu-id="15443-110">예제 1: 미디어 서비스 이름을 사용할 수 있는지 확인</span><span class="sxs-lookup"><span data-stu-id="15443-110">Example 1: Check whether a Media Service name is available</span></span>
```
PS C:\>Get-AzMediaServiceNameAvailability -AccountName "MediaService1"
```

<span data-ttu-id="15443-111">이 명령은 MediaService1 이름을 사용할 수 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="15443-111">This command checks if the name MediaService1 is available.</span></span>

## <span data-ttu-id="15443-112">변수</span><span class="sxs-lookup"><span data-stu-id="15443-112">PARAMETERS</span></span>

### <span data-ttu-id="15443-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="15443-113">-AccountName</span></span>
<span data-ttu-id="15443-114">이 cmdlet이 가져오는 미디어 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="15443-114">Specifies the name of the media service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="15443-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15443-115">-DefaultProfile</span></span>
<span data-ttu-id="15443-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="15443-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="15443-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15443-117">CommonParameters</span></span>
<span data-ttu-id="15443-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="15443-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15443-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15443-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15443-120">입력</span><span class="sxs-lookup"><span data-stu-id="15443-120">INPUTS</span></span>

### <span data-ttu-id="15443-121">않아야</span><span class="sxs-lookup"><span data-stu-id="15443-121">None</span></span>

## <span data-ttu-id="15443-122">출력</span><span class="sxs-lookup"><span data-stu-id="15443-122">OUTPUTS</span></span>

### <span data-ttu-id="15443-123">PSCheckNameAvailabilityOutput (\*).</span><span class="sxs-lookup"><span data-stu-id="15443-123">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="15443-124">상속자</span><span class="sxs-lookup"><span data-stu-id="15443-124">NOTES</span></span>

## <span data-ttu-id="15443-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="15443-125">RELATED LINKS</span></span>

[<span data-ttu-id="15443-126">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="15443-126">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="15443-127">새로운 AzMediaService</span><span class="sxs-lookup"><span data-stu-id="15443-127">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="15443-128">제거-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="15443-128">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="15443-129">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="15443-129">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


