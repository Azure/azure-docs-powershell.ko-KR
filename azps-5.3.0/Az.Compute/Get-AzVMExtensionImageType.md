---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextensionimagetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
ms.openlocfilehash: eb2c92b0efcbcd5333c600fe481e21752a96be9e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493870"
---
# <span data-ttu-id="7398f-101">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="7398f-101">Get-AzVMExtensionImageType</span></span>

## <span data-ttu-id="7398f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7398f-102">SYNOPSIS</span></span>
<span data-ttu-id="7398f-103">Azure 확장의 형식을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7398f-103">Gets the type of an Azure extension.</span></span>

## <span data-ttu-id="7398f-104">구문</span><span class="sxs-lookup"><span data-stu-id="7398f-104">SYNTAX</span></span>

```
Get-AzVMExtensionImageType -Location <String> -PublisherName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7398f-105">설명</span><span class="sxs-lookup"><span data-stu-id="7398f-105">DESCRIPTION</span></span>
<span data-ttu-id="7398f-106">**Get-AzVMExtensionImageType** cmdlet은 Azure 확장의 형식을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7398f-106">The **Get-AzVMExtensionImageType** cmdlet gets the type of an Azure extension.</span></span>

## <span data-ttu-id="7398f-107">예제</span><span class="sxs-lookup"><span data-stu-id="7398f-107">EXAMPLES</span></span>

### <span data-ttu-id="7398f-108">예제 1: 확장 이미지 형식을 얻게</span><span class="sxs-lookup"><span data-stu-id="7398f-108">Example 1: Get an extension image type</span></span>
```
PS C:\> Get-AzVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="7398f-109">이 명령은 지정된 게시자 및 위치에 대한 확장 이미지 형식을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7398f-109">This command gets the extension image type for the specified publisher and location.</span></span>

## <span data-ttu-id="7398f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7398f-110">PARAMETERS</span></span>

### <span data-ttu-id="7398f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7398f-111">-DefaultProfile</span></span>
<span data-ttu-id="7398f-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7398f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7398f-113">-Location</span><span class="sxs-lookup"><span data-stu-id="7398f-113">-Location</span></span>
<span data-ttu-id="7398f-114">확장의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7398f-114">Specifies the location of an extension.</span></span>
<span data-ttu-id="7398f-115">이 cmdlet은 이 매개 변수가 지정하는 위치에서 확장에 대한 형식을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7398f-115">This cmdlet gets the type for an extension at the location that this parameter specifies.</span></span>

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

### <span data-ttu-id="7398f-116">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="7398f-116">-PublisherName</span></span>
<span data-ttu-id="7398f-117">확장의 게시자 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7398f-117">Specifies the name of a publisher of an extension.</span></span>
<span data-ttu-id="7398f-118">확장 게시자를 얻습니다. Get-AzVMImagePublisher cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7398f-118">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>
<span data-ttu-id="7398f-119">이 cmdlet은 이 매개 변수가 지정하는 게시자에서 확장의 형식을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7398f-119">This cmdlet gets the type for an extension from the publisher that this parameter specifies.</span></span>

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

### <span data-ttu-id="7398f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7398f-120">CommonParameters</span></span>
<span data-ttu-id="7398f-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7398f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7398f-122">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7398f-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7398f-123">입력</span><span class="sxs-lookup"><span data-stu-id="7398f-123">INPUTS</span></span>

### <span data-ttu-id="7398f-124">System.String</span><span class="sxs-lookup"><span data-stu-id="7398f-124">System.String</span></span>

## <span data-ttu-id="7398f-125">출력</span><span class="sxs-lookup"><span data-stu-id="7398f-125">OUTPUTS</span></span>

### <span data-ttu-id="7398f-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="7398f-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageType</span></span>

## <span data-ttu-id="7398f-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7398f-127">NOTES</span></span>

## <span data-ttu-id="7398f-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7398f-128">RELATED LINKS</span></span>

[<span data-ttu-id="7398f-129">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="7398f-129">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="7398f-130">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="7398f-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)


