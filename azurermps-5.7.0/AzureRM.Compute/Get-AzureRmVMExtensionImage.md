---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImage.md
ms.openlocfilehash: bae8fb04e71700d1572b8742f8cccbb2ebe8e331
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526972"
---
# <span data-ttu-id="ca892-101">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="ca892-101">Get-AzureRmVMExtensionImage</span></span>

## <span data-ttu-id="ca892-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca892-102">SYNOPSIS</span></span>
<span data-ttu-id="ca892-103">Azure 확장에 대 한 모든 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ca892-103">Gets all versions for an Azure extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca892-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ca892-104">SYNTAX</span></span>

```
Get-AzureRmVMExtensionImage -Location <String> -PublisherName <String> -Type <String>
 [-FilterExpression <String>] [-Version <String>] [<CommonParameters>]
```

## <span data-ttu-id="ca892-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ca892-105">DESCRIPTION</span></span>
<span data-ttu-id="ca892-106">**AzureRmVMExtensionImage** Cmdlet은 Azure 확장에 대 한 모든 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ca892-106">The **Get-AzureRmVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="ca892-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ca892-107">EXAMPLES</span></span>

### <span data-ttu-id="ca892-108">예제 1: 확장 이미지 버전 가져오기</span><span class="sxs-lookup"><span data-stu-id="ca892-108">Example 1: Get the versions of an extension image</span></span>
```
PS C:\> Get-AzureRmVMExtensionImage -Location "Central US" -PublisherName "Fabrikam" -Type "FabrikamEndpointProtection"
```

<span data-ttu-id="ca892-109">이 명령은 지정 된 위치, 게시자 및 형식에 대 한 확장 이미지의 모든 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ca892-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

## <span data-ttu-id="ca892-110">변수</span><span class="sxs-lookup"><span data-stu-id="ca892-110">PARAMETERS</span></span>

### <span data-ttu-id="ca892-111">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="ca892-111">-FilterExpression</span></span>
<span data-ttu-id="ca892-112">필터 식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca892-112">Specifies a filter expression.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca892-113">-위치</span><span class="sxs-lookup"><span data-stu-id="ca892-113">-Location</span></span>
<span data-ttu-id="ca892-114">확장의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca892-114">Specifies the location of an extension.</span></span>

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

### <span data-ttu-id="ca892-115">-최신 Ername</span><span class="sxs-lookup"><span data-stu-id="ca892-115">-PublisherName</span></span>
<span data-ttu-id="ca892-116">확장 게시자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca892-116">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="ca892-117">확장 게시자를 가져오려면 Get-AzureRmVMImagePublisher cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca892-117">To obtain an extension publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="ca892-118">-Type</span><span class="sxs-lookup"><span data-stu-id="ca892-118">-Type</span></span>
<span data-ttu-id="ca892-119">확장 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca892-119">Specifies the type of the extension.</span></span>
<span data-ttu-id="ca892-120">확장 형식을 가져오려면 Get-AzureRmVMExtensionImageType cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca892-120">To obtain an extension type, use the Get-AzureRmVMExtensionImageType cmdlet.</span></span>

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

### <span data-ttu-id="ca892-121">-버전</span><span class="sxs-lookup"><span data-stu-id="ca892-121">-Version</span></span>
<span data-ttu-id="ca892-122">이 cmdlet이 가져오는 확장의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca892-122">Specifies the version of the extension that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca892-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca892-123">CommonParameters</span></span>
<span data-ttu-id="ca892-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca892-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca892-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca892-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca892-126">입력</span><span class="sxs-lookup"><span data-stu-id="ca892-126">INPUTS</span></span>

### <span data-ttu-id="ca892-127">않아야</span><span class="sxs-lookup"><span data-stu-id="ca892-127">None</span></span>
<span data-ttu-id="ca892-128">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ca892-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ca892-129">출력</span><span class="sxs-lookup"><span data-stu-id="ca892-129">OUTPUTS</span></span>

## <span data-ttu-id="ca892-130">상속자</span><span class="sxs-lookup"><span data-stu-id="ca892-130">NOTES</span></span>

## <span data-ttu-id="ca892-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ca892-131">RELATED LINKS</span></span>

[<span data-ttu-id="ca892-132">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="ca892-132">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="ca892-133">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="ca892-133">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="ca892-134">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="ca892-134">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)


