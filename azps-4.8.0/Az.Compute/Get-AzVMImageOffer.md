---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimageoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
ms.openlocfilehash: bd434bae36bc48d5c06bee1ed5fa77673ac426ec
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056533"
---
# <span data-ttu-id="b2e4f-101">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="b2e4f-101">Get-AzVMImageOffer</span></span>

## <span data-ttu-id="b2e4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2e4f-102">SYNOPSIS</span></span>
<span data-ttu-id="b2e4f-103">VMImage 제공 형식을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b2e4f-103">Gets VMImage offer types.</span></span>

## <span data-ttu-id="b2e4f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b2e4f-104">SYNTAX</span></span>

```
Get-AzVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b2e4f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b2e4f-105">DESCRIPTION</span></span>
<span data-ttu-id="b2e4f-106">**AzVMImageOffer** Cmdlet은 VMImage 제안 형식을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b2e4f-106">The **Get-AzVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="b2e4f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b2e4f-107">EXAMPLES</span></span>

### <span data-ttu-id="b2e4f-108">예제 1: 게시자에 대 한 제안 형식 가져오기</span><span class="sxs-lookup"><span data-stu-id="b2e4f-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="b2e4f-109">이 명령은 중앙 US 지역에서 지정 된 게시자에 대 한 제공 유형을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b2e4f-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="b2e4f-110">변수</span><span class="sxs-lookup"><span data-stu-id="b2e4f-110">PARAMETERS</span></span>

### <span data-ttu-id="b2e4f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2e4f-111">-DefaultProfile</span></span>
<span data-ttu-id="b2e4f-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b2e4f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2e4f-113">-위치</span><span class="sxs-lookup"><span data-stu-id="b2e4f-113">-Location</span></span>
<span data-ttu-id="b2e4f-114">VMImage의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2e4f-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="b2e4f-115">-최신 Ername</span><span class="sxs-lookup"><span data-stu-id="b2e4f-115">-PublisherName</span></span>
<span data-ttu-id="b2e4f-116">VMImage의 게시자 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2e4f-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="b2e4f-117">게시자를 얻으려면 Get-AzVMImagePublisher cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2e4f-117">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="b2e4f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2e4f-118">CommonParameters</span></span>
<span data-ttu-id="b2e4f-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2e4f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2e4f-120">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b2e4f-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2e4f-121">입력</span><span class="sxs-lookup"><span data-stu-id="b2e4f-121">INPUTS</span></span>

### <span data-ttu-id="b2e4f-122">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b2e4f-122">System.String</span></span>

## <span data-ttu-id="b2e4f-123">출력</span><span class="sxs-lookup"><span data-stu-id="b2e4f-123">OUTPUTS</span></span>

### <span data-ttu-id="b2e4f-124">Microsoft. \*. m a g m.</span><span class="sxs-lookup"><span data-stu-id="b2e4f-124">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span></span>

## <span data-ttu-id="b2e4f-125">상속자</span><span class="sxs-lookup"><span data-stu-id="b2e4f-125">NOTES</span></span>

## <span data-ttu-id="b2e4f-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b2e4f-126">RELATED LINKS</span></span>

[<span data-ttu-id="b2e4f-127">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="b2e4f-127">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="b2e4f-128">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="b2e4f-128">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="b2e4f-129">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="b2e4f-129">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="b2e4f-130">저장-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="b2e4f-130">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


