---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageOffer.md
ms.openlocfilehash: ccdc7ee8a63c0a633caf162f8549fd1ba737ce8e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536087"
---
# <span data-ttu-id="91eff-101">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="91eff-101">Get-AzureRmVMImageOffer</span></span>

## <span data-ttu-id="91eff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91eff-102">SYNOPSIS</span></span>
<span data-ttu-id="91eff-103">VMImage 제공 형식을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="91eff-103">Gets VMImage offer types.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91eff-104">구문과</span><span class="sxs-lookup"><span data-stu-id="91eff-104">SYNTAX</span></span>

```
Get-AzureRmVMImageOffer -Location <String> -PublisherName <String> [<CommonParameters>]
```

## <span data-ttu-id="91eff-105">설명은</span><span class="sxs-lookup"><span data-stu-id="91eff-105">DESCRIPTION</span></span>
<span data-ttu-id="91eff-106">**AzureRmVMImageOffer** Cmdlet은 VMImage 제안 형식을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="91eff-106">The **Get-AzureRmVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="91eff-107">예제의</span><span class="sxs-lookup"><span data-stu-id="91eff-107">EXAMPLES</span></span>

### <span data-ttu-id="91eff-108">예제 1: 게시자에 대 한 제안 형식 가져오기</span><span class="sxs-lookup"><span data-stu-id="91eff-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzureRmVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="91eff-109">이 명령은 중앙 US 지역에서 지정 된 게시자에 대 한 제공 유형을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="91eff-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="91eff-110">변수</span><span class="sxs-lookup"><span data-stu-id="91eff-110">PARAMETERS</span></span>

### <span data-ttu-id="91eff-111">-위치</span><span class="sxs-lookup"><span data-stu-id="91eff-111">-Location</span></span>
<span data-ttu-id="91eff-112">VMImage의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="91eff-112">Specifies the location of the VMImage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91eff-113">-최신 Ername</span><span class="sxs-lookup"><span data-stu-id="91eff-113">-PublisherName</span></span>
<span data-ttu-id="91eff-114">VMImage의 게시자 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="91eff-114">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="91eff-115">게시자를 얻으려면 Get-AzureRmVMImagePublisher cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="91eff-115">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91eff-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91eff-116">CommonParameters</span></span>
<span data-ttu-id="91eff-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="91eff-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91eff-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91eff-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91eff-119">입력</span><span class="sxs-lookup"><span data-stu-id="91eff-119">INPUTS</span></span>

### <span data-ttu-id="91eff-120">않아야</span><span class="sxs-lookup"><span data-stu-id="91eff-120">None</span></span>
<span data-ttu-id="91eff-121">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="91eff-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="91eff-122">출력</span><span class="sxs-lookup"><span data-stu-id="91eff-122">OUTPUTS</span></span>

## <span data-ttu-id="91eff-123">상속자</span><span class="sxs-lookup"><span data-stu-id="91eff-123">NOTES</span></span>

## <span data-ttu-id="91eff-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="91eff-124">RELATED LINKS</span></span>

[<span data-ttu-id="91eff-125">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="91eff-125">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="91eff-126">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="91eff-126">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="91eff-127">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="91eff-127">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="91eff-128">저장-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="91eff-128">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


