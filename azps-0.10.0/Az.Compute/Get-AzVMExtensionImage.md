---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextensionimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMExtensionImage.md
ms.openlocfilehash: 1864b4c2dcbd4b3d9934ffb15c54fae18082c920
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93877059"
---
# <span data-ttu-id="f5584-101">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="f5584-101">Get-AzVMExtensionImage</span></span>

## <span data-ttu-id="f5584-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5584-102">SYNOPSIS</span></span>
<span data-ttu-id="f5584-103">Azure 확장에 대 한 모든 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f5584-103">Gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="f5584-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f5584-104">SYNTAX</span></span>

```
Get-AzVMExtensionImage -Location <String> -PublisherName <String> -Type <String>
 [-FilterExpression <String>] [-Version <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f5584-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f5584-105">DESCRIPTION</span></span>
<span data-ttu-id="f5584-106">**AzVMExtensionImage** Cmdlet은 Azure 확장에 대 한 모든 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f5584-106">The **Get-AzVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="f5584-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f5584-107">EXAMPLES</span></span>

### <span data-ttu-id="f5584-108">예제 1: 확장 이미지 버전 가져오기</span><span class="sxs-lookup"><span data-stu-id="f5584-108">Example 1: Get the versions of an extension image</span></span>
```
PS C:\> Get-AzVMExtensionImage -Location "Central US" -PublisherName "Fabrikam" -Type "FabrikamEndpointProtection"
```

<span data-ttu-id="f5584-109">이 명령은 지정 된 위치, 게시자 및 형식에 대 한 확장 이미지의 모든 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f5584-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

## <span data-ttu-id="f5584-110">변수</span><span class="sxs-lookup"><span data-stu-id="f5584-110">PARAMETERS</span></span>

### <span data-ttu-id="f5584-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5584-111">-DefaultProfile</span></span>
<span data-ttu-id="f5584-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f5584-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5584-113">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="f5584-113">-FilterExpression</span></span>
<span data-ttu-id="f5584-114">필터 식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5584-114">Specifies a filter expression.</span></span>

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

### <span data-ttu-id="f5584-115">-위치</span><span class="sxs-lookup"><span data-stu-id="f5584-115">-Location</span></span>
<span data-ttu-id="f5584-116">확장의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5584-116">Specifies the location of an extension.</span></span>

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

### <span data-ttu-id="f5584-117">-최신 Ername</span><span class="sxs-lookup"><span data-stu-id="f5584-117">-PublisherName</span></span>
<span data-ttu-id="f5584-118">확장 게시자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5584-118">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="f5584-119">확장 게시자를 가져오려면 Get-AzVMImagePublisher cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5584-119">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="f5584-120">-Type</span><span class="sxs-lookup"><span data-stu-id="f5584-120">-Type</span></span>
<span data-ttu-id="f5584-121">확장 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5584-121">Specifies the type of the extension.</span></span>
<span data-ttu-id="f5584-122">확장 형식을 가져오려면 Get-AzVMExtensionImageType cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5584-122">To obtain an extension type, use the Get-AzVMExtensionImageType cmdlet.</span></span>

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

### <span data-ttu-id="f5584-123">-버전</span><span class="sxs-lookup"><span data-stu-id="f5584-123">-Version</span></span>
<span data-ttu-id="f5584-124">이 cmdlet이 가져오는 확장의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5584-124">Specifies the version of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f5584-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5584-125">CommonParameters</span></span>
<span data-ttu-id="f5584-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5584-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5584-127">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5584-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5584-128">입력</span><span class="sxs-lookup"><span data-stu-id="f5584-128">INPUTS</span></span>

### <span data-ttu-id="f5584-129">않아야</span><span class="sxs-lookup"><span data-stu-id="f5584-129">None</span></span>
<span data-ttu-id="f5584-130">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f5584-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f5584-131">출력</span><span class="sxs-lookup"><span data-stu-id="f5584-131">OUTPUTS</span></span>

### <span data-ttu-id="f5584-132">Microsoft Azure. PSVirtualMachineExtensionImage</span><span class="sxs-lookup"><span data-stu-id="f5584-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImage</span></span>

### <span data-ttu-id="f5584-133">Microsoft. PSVirtualMachineExtensionImageDetails</span><span class="sxs-lookup"><span data-stu-id="f5584-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageDetails</span></span>

## <span data-ttu-id="f5584-134">상속자</span><span class="sxs-lookup"><span data-stu-id="f5584-134">NOTES</span></span>

## <span data-ttu-id="f5584-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f5584-135">RELATED LINKS</span></span>

[<span data-ttu-id="f5584-136">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="f5584-136">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="f5584-137">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="f5584-137">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="f5584-138">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="f5584-138">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)


