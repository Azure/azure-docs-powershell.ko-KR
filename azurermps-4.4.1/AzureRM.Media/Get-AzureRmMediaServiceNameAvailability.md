---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 23C6C9D3-A745-46C8-AB2C-B874223FBFFF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceNameAvailability.md
ms.openlocfilehash: be459183e47982fef8dbd2376ddd5110251bb001
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703701"
---
# <span data-ttu-id="51ada-101">Get-AzureRmMediaServiceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="51ada-101">Get-AzureRmMediaServiceNameAvailability</span></span>

## <span data-ttu-id="51ada-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51ada-102">SYNOPSIS</span></span>
<span data-ttu-id="51ada-103">미디어 서비스 이름을 사용할 수 있는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="51ada-103">Checks whether a media service name is available.</span></span>
<span data-ttu-id="51ada-104">미디어 서비스 이름은 전역적으로 고유 합니다.</span><span class="sxs-lookup"><span data-stu-id="51ada-104">Media service names are globally unique.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51ada-105">구문과</span><span class="sxs-lookup"><span data-stu-id="51ada-105">SYNTAX</span></span>

```
Get-AzureRmMediaServiceNameAvailability [-DefaultProfile <IAzureContextContainer>] [-AccountName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="51ada-106">설명은</span><span class="sxs-lookup"><span data-stu-id="51ada-106">DESCRIPTION</span></span>
<span data-ttu-id="51ada-107">**AzureRmMediaServiceNameAvailability** cmdlet은 미디어 서비스 이름을 사용할 수 있는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="51ada-107">The **Get-AzureRmMediaServiceNameAvailability** cmdlet checks whether a media service name is available.</span></span>
<span data-ttu-id="51ada-108">미디어 서비스 이름은 전역적으로 고유 합니다.</span><span class="sxs-lookup"><span data-stu-id="51ada-108">Media service names are globally unique.</span></span>

## <span data-ttu-id="51ada-109">예제의</span><span class="sxs-lookup"><span data-stu-id="51ada-109">EXAMPLES</span></span>

### <span data-ttu-id="51ada-110">예제 1: 미디어 서비스 이름을 사용할 수 있는지 확인</span><span class="sxs-lookup"><span data-stu-id="51ada-110">Example 1: Check whether a Media Service name is available</span></span>
```
PS C:\>Get-AzureRmMediaServiceNameAvailability -AccountName "MediaService1"
```

<span data-ttu-id="51ada-111">이 명령은 MediaService1 이름을 사용할 수 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="51ada-111">This command checks if the name MediaService1 is available.</span></span>

## <span data-ttu-id="51ada-112">변수</span><span class="sxs-lookup"><span data-stu-id="51ada-112">PARAMETERS</span></span>

### <span data-ttu-id="51ada-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="51ada-113">-AccountName</span></span>
<span data-ttu-id="51ada-114">이 cmdlet이 가져오는 미디어 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51ada-114">Specifies the name of the media service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="51ada-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51ada-115">-DefaultProfile</span></span>
<span data-ttu-id="51ada-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="51ada-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51ada-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51ada-117">CommonParameters</span></span>
<span data-ttu-id="51ada-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="51ada-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51ada-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51ada-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51ada-120">입력</span><span class="sxs-lookup"><span data-stu-id="51ada-120">INPUTS</span></span>

## <span data-ttu-id="51ada-121">출력</span><span class="sxs-lookup"><span data-stu-id="51ada-121">OUTPUTS</span></span>

### <span data-ttu-id="51ada-122">PSCheckNameAvailabilityOutput (\*).</span><span class="sxs-lookup"><span data-stu-id="51ada-122">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="51ada-123">상속자</span><span class="sxs-lookup"><span data-stu-id="51ada-123">NOTES</span></span>

## <span data-ttu-id="51ada-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="51ada-124">RELATED LINKS</span></span>

[<span data-ttu-id="51ada-125">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="51ada-125">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="51ada-126">새로운 AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="51ada-126">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="51ada-127">제거-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="51ada-127">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)

[<span data-ttu-id="51ada-128">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="51ada-128">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


