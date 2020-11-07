---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImageSku.md
ms.openlocfilehash: fad6c42c53e475343ad518c89dbb1a918a0f1e68
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93877052"
---
# <span data-ttu-id="70db2-101">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="70db2-101">Get-AzVMImageSku</span></span>

## <span data-ttu-id="70db2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70db2-102">SYNOPSIS</span></span>
<span data-ttu-id="70db2-103">VMImage Sku를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="70db2-103">Gets VMImage SKUs.</span></span>

## <span data-ttu-id="70db2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="70db2-104">SYNTAX</span></span>

```
Get-AzVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70db2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="70db2-105">DESCRIPTION</span></span>
<span data-ttu-id="70db2-106">**Get-AzVMImageSku** Cmdlet은 VMImage sku를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="70db2-106">The **Get-AzVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="70db2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="70db2-107">EXAMPLES</span></span>

### <span data-ttu-id="70db2-108">예제 1: VMImage Sku 가져오기</span><span class="sxs-lookup"><span data-stu-id="70db2-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="70db2-109">이 명령은 지정 된 게시자 및 제안에 대 한 Sku를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="70db2-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="70db2-110">변수</span><span class="sxs-lookup"><span data-stu-id="70db2-110">PARAMETERS</span></span>

### <span data-ttu-id="70db2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70db2-111">-DefaultProfile</span></span>
<span data-ttu-id="70db2-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="70db2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70db2-113">-위치</span><span class="sxs-lookup"><span data-stu-id="70db2-113">-Location</span></span>
<span data-ttu-id="70db2-114">VMImage의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70db2-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="70db2-115">-제공</span><span class="sxs-lookup"><span data-stu-id="70db2-115">-Offer</span></span>
<span data-ttu-id="70db2-116">VMImage 제안 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70db2-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="70db2-117">-최신 Ername</span><span class="sxs-lookup"><span data-stu-id="70db2-117">-PublisherName</span></span>
<span data-ttu-id="70db2-118">VMImage의 게시자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70db2-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="70db2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70db2-119">CommonParameters</span></span>
<span data-ttu-id="70db2-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="70db2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70db2-121">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70db2-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70db2-122">입력</span><span class="sxs-lookup"><span data-stu-id="70db2-122">INPUTS</span></span>

### <span data-ttu-id="70db2-123">않아야</span><span class="sxs-lookup"><span data-stu-id="70db2-123">None</span></span>
<span data-ttu-id="70db2-124">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="70db2-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="70db2-125">출력</span><span class="sxs-lookup"><span data-stu-id="70db2-125">OUTPUTS</span></span>

### <span data-ttu-id="70db2-126">PSVirtualMachineImageSku를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="70db2-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="70db2-127">상속자</span><span class="sxs-lookup"><span data-stu-id="70db2-127">NOTES</span></span>

## <span data-ttu-id="70db2-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="70db2-128">RELATED LINKS</span></span>

[<span data-ttu-id="70db2-129">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="70db2-129">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="70db2-130">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="70db2-130">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="70db2-131">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="70db2-131">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="70db2-132">저장-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="70db2-132">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


