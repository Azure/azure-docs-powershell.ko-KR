---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimageoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMImageOffer.md
ms.openlocfilehash: 66c0355af202c5900fddc60c81e92f2851ddc1ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530997"
---
# <span data-ttu-id="27951-101">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="27951-101">Get-AzureRmVMImageOffer</span></span>

## <span data-ttu-id="27951-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27951-102">SYNOPSIS</span></span>
<span data-ttu-id="27951-103">VMImage 제공 형식을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="27951-103">Gets VMImage offer types.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27951-104">구문과</span><span class="sxs-lookup"><span data-stu-id="27951-104">SYNTAX</span></span>

```
Get-AzureRmVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="27951-105">설명은</span><span class="sxs-lookup"><span data-stu-id="27951-105">DESCRIPTION</span></span>
<span data-ttu-id="27951-106">**AzureRmVMImageOffer** Cmdlet은 VMImage 제안 형식을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="27951-106">The **Get-AzureRmVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="27951-107">예제의</span><span class="sxs-lookup"><span data-stu-id="27951-107">EXAMPLES</span></span>

### <span data-ttu-id="27951-108">예제 1: 게시자에 대 한 제안 형식 가져오기</span><span class="sxs-lookup"><span data-stu-id="27951-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzureRmVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="27951-109">이 명령은 중앙 US 지역에서 지정 된 게시자에 대 한 제공 유형을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="27951-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="27951-110">변수</span><span class="sxs-lookup"><span data-stu-id="27951-110">PARAMETERS</span></span>

### <span data-ttu-id="27951-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27951-111">-DefaultProfile</span></span>
<span data-ttu-id="27951-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="27951-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27951-113">-위치</span><span class="sxs-lookup"><span data-stu-id="27951-113">-Location</span></span>
<span data-ttu-id="27951-114">VMImage의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="27951-114">Specifies the location of the VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27951-115">-최신 Ername</span><span class="sxs-lookup"><span data-stu-id="27951-115">-PublisherName</span></span>
<span data-ttu-id="27951-116">VMImage의 게시자 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="27951-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="27951-117">게시자를 얻으려면 Get-AzureRmVMImagePublisher cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="27951-117">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27951-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27951-118">CommonParameters</span></span>
<span data-ttu-id="27951-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="27951-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27951-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27951-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27951-121">입력</span><span class="sxs-lookup"><span data-stu-id="27951-121">INPUTS</span></span>

### <span data-ttu-id="27951-122">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="27951-122">System.String</span></span>

## <span data-ttu-id="27951-123">출력</span><span class="sxs-lookup"><span data-stu-id="27951-123">OUTPUTS</span></span>

### <span data-ttu-id="27951-124">Microsoft. \*. m a g m.</span><span class="sxs-lookup"><span data-stu-id="27951-124">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span></span>

## <span data-ttu-id="27951-125">상속자</span><span class="sxs-lookup"><span data-stu-id="27951-125">NOTES</span></span>

## <span data-ttu-id="27951-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="27951-126">RELATED LINKS</span></span>

[<span data-ttu-id="27951-127">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="27951-127">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="27951-128">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="27951-128">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="27951-129">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="27951-129">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="27951-130">저장-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="27951-130">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)

