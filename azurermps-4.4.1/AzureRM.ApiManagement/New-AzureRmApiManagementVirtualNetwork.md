---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
ms.openlocfilehash: 42213ddd4a7780b4d69b357c4b801df34aa9aca4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525792"
---
# <span data-ttu-id="11cdd-101">New-AzureRmApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="11cdd-101">New-AzureRmApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="11cdd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11cdd-102">SYNOPSIS</span></span>
<span data-ttu-id="11cdd-103">PsApiManagementVirtualNetwork의 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="11cdd-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11cdd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="11cdd-104">SYNTAX</span></span>

```
New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11cdd-105">설명은</span><span class="sxs-lookup"><span data-stu-id="11cdd-105">DESCRIPTION</span></span>
<span data-ttu-id="11cdd-106">**AzureRmApiManagementVirtualNetwork** Cmdlet은 **PsApiManagementVirtualNetwork** 의 인스턴스를 만드는 도우미 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="11cdd-106">The **New-AzureRmApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="11cdd-107">이 명령은 **Set-AzureRMApiManagementVirtualNetworks** cmdlet과 함께 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="11cdd-107">This command is used with **Set-AzureRMApiManagementVirtualNetworks** cmdlet.</span></span>

## <span data-ttu-id="11cdd-108">예제의</span><span class="sxs-lookup"><span data-stu-id="11cdd-108">EXAMPLES</span></span>

### <span data-ttu-id="11cdd-109">예제 1: 가상 네트워크 만들기</span><span class="sxs-lookup"><span data-stu-id="11cdd-109">Example 1: Create a virtual network</span></span>
```
PS C:\>$VirtualNetworks = @()
PS C:\> $VirtualNetworks += New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubtenName "ContosoNet" -VnetId "089D3F4D-B986-4DFD-9259-9112BA7A1F03"
PS C:\> Set-AzureRmApiManagementVirtualNetworks -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetworks $VirtualNetworks
```

<span data-ttu-id="11cdd-110">이 예제에서는 가상 네트워크를 만든 다음 **AzureRmApiManagementVirtualNetworks** cmdlet을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="11cdd-110">This example creates a virtual network and then calls the **Set-AzureRmApiManagementVirtualNetworks** cmdlet.</span></span>

## <span data-ttu-id="11cdd-111">변수</span><span class="sxs-lookup"><span data-stu-id="11cdd-111">PARAMETERS</span></span>

### <span data-ttu-id="11cdd-112">-위치</span><span class="sxs-lookup"><span data-stu-id="11cdd-112">-Location</span></span>
<span data-ttu-id="11cdd-113">이 cmdlet이 인스턴스를 만드는 가상 네트워크의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11cdd-113">Specifies the location of the virtual network in which this cmdlet creates the instance.</span></span>

<span data-ttu-id="11cdd-114">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="11cdd-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="11cdd-115">대한민국 미국 중부</span><span class="sxs-lookup"><span data-stu-id="11cdd-115">North Central US</span></span>
- <span data-ttu-id="11cdd-116">미국 중부 US</span><span class="sxs-lookup"><span data-stu-id="11cdd-116">South Central US</span></span>
- <span data-ttu-id="11cdd-117">중부 US</span><span class="sxs-lookup"><span data-stu-id="11cdd-117">Central US</span></span>
- <span data-ttu-id="11cdd-118">유럽 서유럽</span><span class="sxs-lookup"><span data-stu-id="11cdd-118">West Europe</span></span>
- <span data-ttu-id="11cdd-119">동유럽</span><span class="sxs-lookup"><span data-stu-id="11cdd-119">North Europe</span></span>
- <span data-ttu-id="11cdd-120">미국 서 부</span><span class="sxs-lookup"><span data-stu-id="11cdd-120">West US</span></span>
- <span data-ttu-id="11cdd-121">미국 동부</span><span class="sxs-lookup"><span data-stu-id="11cdd-121">East US</span></span>
- <span data-ttu-id="11cdd-122">미국 동부 2</span><span class="sxs-lookup"><span data-stu-id="11cdd-122">East US 2</span></span>
- <span data-ttu-id="11cdd-123">일본 동부</span><span class="sxs-lookup"><span data-stu-id="11cdd-123">Japan East</span></span>
- <span data-ttu-id="11cdd-124">일본 서쪽</span><span class="sxs-lookup"><span data-stu-id="11cdd-124">Japan West</span></span>
- <span data-ttu-id="11cdd-125">브라질 남부</span><span class="sxs-lookup"><span data-stu-id="11cdd-125">Brazil South</span></span>
- <span data-ttu-id="11cdd-126">동남 아시아</span><span class="sxs-lookup"><span data-stu-id="11cdd-126">Southeast Asia</span></span>
- <span data-ttu-id="11cdd-127">동아시아</span><span class="sxs-lookup"><span data-stu-id="11cdd-127">East Asia</span></span>
- <span data-ttu-id="11cdd-128">오스트레일리아 동부</span><span class="sxs-lookup"><span data-stu-id="11cdd-128">Australia East</span></span>
- <span data-ttu-id="11cdd-129">오스트레일리아 남동쪽</span><span class="sxs-lookup"><span data-stu-id="11cdd-129">Australia Southeast</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11cdd-130">-SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="11cdd-130">-SubnetResourceId</span></span>
<span data-ttu-id="11cdd-131">가상 네트워크의 서브넷 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11cdd-131">Specifies the subnet resource ID of the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11cdd-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11cdd-132">-DefaultProfile</span></span>
<span data-ttu-id="11cdd-133">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="11cdd-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11cdd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11cdd-134">CommonParameters</span></span>
<span data-ttu-id="11cdd-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="11cdd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11cdd-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11cdd-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11cdd-137">입력</span><span class="sxs-lookup"><span data-stu-id="11cdd-137">INPUTS</span></span>

## <span data-ttu-id="11cdd-138">출력</span><span class="sxs-lookup"><span data-stu-id="11cdd-138">OUTPUTS</span></span>

### <span data-ttu-id="11cdd-139">ApiManagement. PsApiManagementVirtualNetwork/.</span><span class="sxs-lookup"><span data-stu-id="11cdd-139">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="11cdd-140">상속자</span><span class="sxs-lookup"><span data-stu-id="11cdd-140">NOTES</span></span>

## <span data-ttu-id="11cdd-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="11cdd-141">RELATED LINKS</span></span>

