---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmextensionimagetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMExtensionImageType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMExtensionImageType.md
ms.openlocfilehash: c4af2c651438659508e231bf2710e88de19830cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531001"
---
# <span data-ttu-id="acf22-101">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="acf22-101">Get-AzureRmVMExtensionImageType</span></span>

## <span data-ttu-id="acf22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acf22-102">SYNOPSIS</span></span>
<span data-ttu-id="acf22-103">Azure 확장의 형식을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="acf22-103">Gets the type of an Azure extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="acf22-104">구문과</span><span class="sxs-lookup"><span data-stu-id="acf22-104">SYNTAX</span></span>

```
Get-AzureRmVMExtensionImageType -Location <String> -PublisherName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acf22-105">설명은</span><span class="sxs-lookup"><span data-stu-id="acf22-105">DESCRIPTION</span></span>
<span data-ttu-id="acf22-106">**AzureRmVMExtensionImageType** Cmdlet은 Azure 확장의 형식을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="acf22-106">The **Get-AzureRmVMExtensionImageType** cmdlet gets the type of an Azure extension.</span></span>

## <span data-ttu-id="acf22-107">예제의</span><span class="sxs-lookup"><span data-stu-id="acf22-107">EXAMPLES</span></span>

### <span data-ttu-id="acf22-108">예제 1: 확장 이미지 형식 가져오기</span><span class="sxs-lookup"><span data-stu-id="acf22-108">Example 1: Get an extension image type</span></span>
```
PS C:\> Get-AzureRmVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="acf22-109">이 명령은 지정 된 게시자 및 위치에 대 한 확장 이미지 형식을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="acf22-109">This command gets the extension image type for the specified publisher and location.</span></span>

## <span data-ttu-id="acf22-110">변수</span><span class="sxs-lookup"><span data-stu-id="acf22-110">PARAMETERS</span></span>

### <span data-ttu-id="acf22-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acf22-111">-DefaultProfile</span></span>
<span data-ttu-id="acf22-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="acf22-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="acf22-113">-위치</span><span class="sxs-lookup"><span data-stu-id="acf22-113">-Location</span></span>
<span data-ttu-id="acf22-114">확장의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="acf22-114">Specifies the location of an extension.</span></span>
<span data-ttu-id="acf22-115">이 cmdlet은이 매개 변수에서 지정 하는 위치에서 확장에 대 한 형식을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="acf22-115">This cmdlet gets the type for an extension at the location that this parameter specifies.</span></span>

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

### <span data-ttu-id="acf22-116">-최신 Ername</span><span class="sxs-lookup"><span data-stu-id="acf22-116">-PublisherName</span></span>
<span data-ttu-id="acf22-117">확장명의 게시자 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="acf22-117">Specifies the name of a publisher of an extension.</span></span>
<span data-ttu-id="acf22-118">확장 게시자를 가져오려면 Get-AzureRmVMImagePublisher cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="acf22-118">To obtain an extension publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>
<span data-ttu-id="acf22-119">이 cmdlet은이 매개 변수에서 지정 하는 게시자에서 확장에 대 한 형식을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="acf22-119">This cmdlet gets the type for an extension from the publisher that this parameter specifies.</span></span>

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

### <span data-ttu-id="acf22-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acf22-120">CommonParameters</span></span>
<span data-ttu-id="acf22-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="acf22-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acf22-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acf22-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acf22-123">입력</span><span class="sxs-lookup"><span data-stu-id="acf22-123">INPUTS</span></span>

### <span data-ttu-id="acf22-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="acf22-124">System.String</span></span>

## <span data-ttu-id="acf22-125">출력</span><span class="sxs-lookup"><span data-stu-id="acf22-125">OUTPUTS</span></span>

### <span data-ttu-id="acf22-126">Microsoft. a. PSVirtualMachineExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="acf22-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageType</span></span>

## <span data-ttu-id="acf22-127">상속자</span><span class="sxs-lookup"><span data-stu-id="acf22-127">NOTES</span></span>

## <span data-ttu-id="acf22-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="acf22-128">RELATED LINKS</span></span>

[<span data-ttu-id="acf22-129">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="acf22-129">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="acf22-130">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="acf22-130">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)


