---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImage.md
ms.openlocfilehash: 7010808e1879566d3b0fc78f82d0e9f82bdd626b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703399"
---
# <span data-ttu-id="53e6d-101">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="53e6d-101">Get-AzureRmVMExtensionImage</span></span>

## <span data-ttu-id="53e6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53e6d-102">SYNOPSIS</span></span>
<span data-ttu-id="53e6d-103">Azure 확장에 대 한 모든 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="53e6d-103">Gets all versions for an Azure extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53e6d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="53e6d-104">SYNTAX</span></span>

```
Get-AzureRmVMExtensionImage -Location <String> -PublisherName <String> -Type <String>
 [-FilterExpression <String>] [-Version <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="53e6d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="53e6d-105">DESCRIPTION</span></span>
<span data-ttu-id="53e6d-106">**AzureRmVMExtensionImage** Cmdlet은 Azure 확장에 대 한 모든 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="53e6d-106">The **Get-AzureRmVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="53e6d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="53e6d-107">EXAMPLES</span></span>

### <span data-ttu-id="53e6d-108">예제 1: 확장 이미지 버전 가져오기</span><span class="sxs-lookup"><span data-stu-id="53e6d-108">Example 1: Get the versions of an extension image</span></span>
```
PS C:\> Get-AzureRmVMExtensionImage -Location "Central US" -PublisherName "Fabrikam" -Type "FabrikamEndpointProtection"
```

<span data-ttu-id="53e6d-109">이 명령은 지정 된 위치, 게시자 및 형식에 대 한 확장 이미지의 모든 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="53e6d-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

## <span data-ttu-id="53e6d-110">변수</span><span class="sxs-lookup"><span data-stu-id="53e6d-110">PARAMETERS</span></span>

### <span data-ttu-id="53e6d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53e6d-111">-DefaultProfile</span></span>
<span data-ttu-id="53e6d-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="53e6d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53e6d-113">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="53e6d-113">-FilterExpression</span></span>
<span data-ttu-id="53e6d-114">필터 식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53e6d-114">Specifies a filter expression.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53e6d-115">-위치</span><span class="sxs-lookup"><span data-stu-id="53e6d-115">-Location</span></span>
<span data-ttu-id="53e6d-116">확장의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53e6d-116">Specifies the location of an extension.</span></span>

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

### <span data-ttu-id="53e6d-117">-최신 Ername</span><span class="sxs-lookup"><span data-stu-id="53e6d-117">-PublisherName</span></span>
<span data-ttu-id="53e6d-118">확장 게시자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53e6d-118">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="53e6d-119">확장 게시자를 가져오려면 Get-AzureRmVMImagePublisher cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="53e6d-119">To obtain an extension publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="53e6d-120">-Type</span><span class="sxs-lookup"><span data-stu-id="53e6d-120">-Type</span></span>
<span data-ttu-id="53e6d-121">확장 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53e6d-121">Specifies the type of the extension.</span></span>
<span data-ttu-id="53e6d-122">확장 형식을 가져오려면 Get-AzureRmVMExtensionImageType cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="53e6d-122">To obtain an extension type, use the Get-AzureRmVMExtensionImageType cmdlet.</span></span>

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

### <span data-ttu-id="53e6d-123">-버전</span><span class="sxs-lookup"><span data-stu-id="53e6d-123">-Version</span></span>
<span data-ttu-id="53e6d-124">이 cmdlet이 가져오는 확장의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53e6d-124">Specifies the version of the extension that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53e6d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53e6d-125">CommonParameters</span></span>
<span data-ttu-id="53e6d-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="53e6d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53e6d-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53e6d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53e6d-128">입력</span><span class="sxs-lookup"><span data-stu-id="53e6d-128">INPUTS</span></span>

## <span data-ttu-id="53e6d-129">출력</span><span class="sxs-lookup"><span data-stu-id="53e6d-129">OUTPUTS</span></span>

## <span data-ttu-id="53e6d-130">상속자</span><span class="sxs-lookup"><span data-stu-id="53e6d-130">NOTES</span></span>

## <span data-ttu-id="53e6d-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="53e6d-131">RELATED LINKS</span></span>

[<span data-ttu-id="53e6d-132">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="53e6d-132">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="53e6d-133">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="53e6d-133">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="53e6d-134">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="53e6d-134">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)


