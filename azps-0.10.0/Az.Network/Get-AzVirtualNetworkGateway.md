---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
ms.openlocfilehash: 490e61142bdbc0bcdd64f18aeeb2fa527e5180b9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875521"
---
# <span data-ttu-id="3ccc6-101">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3ccc6-101">Get-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="3ccc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ccc6-102">SYNOPSIS</span></span>
<span data-ttu-id="3ccc6-103">가상 네트워크 게이트웨이를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3ccc6-103">Gets a Virtual Network Gateway</span></span>

## <span data-ttu-id="3ccc6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3ccc6-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ccc6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3ccc6-105">DESCRIPTION</span></span>
<span data-ttu-id="3ccc6-106">가상 네트워크 게이트웨이는 Azure에서 게이트웨이를 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3ccc6-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="3ccc6-107">**AzVirtualNetworkGateway** Cmdlet은 이름 및 리소스 그룹 이름에 따라 Azure에서 게이트웨이의 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ccc6-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="3ccc6-108">예제의</span><span class="sxs-lookup"><span data-stu-id="3ccc6-108">EXAMPLES</span></span>

### <span data-ttu-id="3ccc6-109">1: 가상 네트워크 게이트웨이 가져오기</span><span class="sxs-lookup"><span data-stu-id="3ccc6-109">1: Get a Virtual Network Gateway</span></span>
```
Get-AzVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="3ccc6-110">리소스 그룹 "Mygateway" 내에서 이름이 "myGateway" 인 가상 네트워크 게이트웨이의 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ccc6-110">Returns the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="3ccc6-111">변수</span><span class="sxs-lookup"><span data-stu-id="3ccc6-111">PARAMETERS</span></span>

### <span data-ttu-id="3ccc6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ccc6-112">-DefaultProfile</span></span>
<span data-ttu-id="3ccc6-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3ccc6-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ccc6-114">-이름</span><span class="sxs-lookup"><span data-stu-id="3ccc6-114">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ccc6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ccc6-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="3ccc6-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ccc6-116">CommonParameters</span></span>
<span data-ttu-id="3ccc6-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ccc6-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ccc6-118">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ccc6-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ccc6-119">입력</span><span class="sxs-lookup"><span data-stu-id="3ccc6-119">INPUTS</span></span>

## <span data-ttu-id="3ccc6-120">출력</span><span class="sxs-lookup"><span data-stu-id="3ccc6-120">OUTPUTS</span></span>

### <span data-ttu-id="3ccc6-121">PSVirtualNetworkGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="3ccc6-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="3ccc6-122">상속자</span><span class="sxs-lookup"><span data-stu-id="3ccc6-122">NOTES</span></span>

## <span data-ttu-id="3ccc6-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3ccc6-123">RELATED LINKS</span></span>

