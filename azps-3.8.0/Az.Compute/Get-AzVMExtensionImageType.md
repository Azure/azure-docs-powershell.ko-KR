---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextensionimagetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
ms.openlocfilehash: eb2c92b0efcbcd5333c600fe481e21752a96be9e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042886"
---
# <span data-ttu-id="96c04-101">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="96c04-101">Get-AzVMExtensionImageType</span></span>

## <span data-ttu-id="96c04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96c04-102">SYNOPSIS</span></span>
<span data-ttu-id="96c04-103">Azure 확장의 형식을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="96c04-103">Gets the type of an Azure extension.</span></span>

## <span data-ttu-id="96c04-104">구문과</span><span class="sxs-lookup"><span data-stu-id="96c04-104">SYNTAX</span></span>

```
Get-AzVMExtensionImageType -Location <String> -PublisherName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96c04-105">설명은</span><span class="sxs-lookup"><span data-stu-id="96c04-105">DESCRIPTION</span></span>
<span data-ttu-id="96c04-106">**AzVMExtensionImageType** Cmdlet은 Azure 확장의 형식을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="96c04-106">The **Get-AzVMExtensionImageType** cmdlet gets the type of an Azure extension.</span></span>

## <span data-ttu-id="96c04-107">예제의</span><span class="sxs-lookup"><span data-stu-id="96c04-107">EXAMPLES</span></span>

### <span data-ttu-id="96c04-108">예제 1: 확장 이미지 형식 가져오기</span><span class="sxs-lookup"><span data-stu-id="96c04-108">Example 1: Get an extension image type</span></span>
```
PS C:\> Get-AzVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="96c04-109">이 명령은 지정 된 게시자 및 위치에 대 한 확장 이미지 형식을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="96c04-109">This command gets the extension image type for the specified publisher and location.</span></span>

## <span data-ttu-id="96c04-110">변수</span><span class="sxs-lookup"><span data-stu-id="96c04-110">PARAMETERS</span></span>

### <span data-ttu-id="96c04-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96c04-111">-DefaultProfile</span></span>
<span data-ttu-id="96c04-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="96c04-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96c04-113">-위치</span><span class="sxs-lookup"><span data-stu-id="96c04-113">-Location</span></span>
<span data-ttu-id="96c04-114">확장의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="96c04-114">Specifies the location of an extension.</span></span>
<span data-ttu-id="96c04-115">이 cmdlet은이 매개 변수에서 지정 하는 위치에서 확장에 대 한 형식을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="96c04-115">This cmdlet gets the type for an extension at the location that this parameter specifies.</span></span>

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

### <span data-ttu-id="96c04-116">-최신 Ername</span><span class="sxs-lookup"><span data-stu-id="96c04-116">-PublisherName</span></span>
<span data-ttu-id="96c04-117">확장명의 게시자 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="96c04-117">Specifies the name of a publisher of an extension.</span></span>
<span data-ttu-id="96c04-118">확장 게시자를 가져오려면 Get-AzVMImagePublisher cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="96c04-118">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>
<span data-ttu-id="96c04-119">이 cmdlet은이 매개 변수에서 지정 하는 게시자에서 확장에 대 한 형식을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="96c04-119">This cmdlet gets the type for an extension from the publisher that this parameter specifies.</span></span>

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

### <span data-ttu-id="96c04-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96c04-120">CommonParameters</span></span>
<span data-ttu-id="96c04-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="96c04-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96c04-122">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="96c04-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96c04-123">입력</span><span class="sxs-lookup"><span data-stu-id="96c04-123">INPUTS</span></span>

### <span data-ttu-id="96c04-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="96c04-124">System.String</span></span>

## <span data-ttu-id="96c04-125">출력</span><span class="sxs-lookup"><span data-stu-id="96c04-125">OUTPUTS</span></span>

### <span data-ttu-id="96c04-126">Microsoft. a. PSVirtualMachineExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="96c04-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageType</span></span>

## <span data-ttu-id="96c04-127">상속자</span><span class="sxs-lookup"><span data-stu-id="96c04-127">NOTES</span></span>

## <span data-ttu-id="96c04-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="96c04-128">RELATED LINKS</span></span>

[<span data-ttu-id="96c04-129">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="96c04-129">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="96c04-130">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="96c04-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)


