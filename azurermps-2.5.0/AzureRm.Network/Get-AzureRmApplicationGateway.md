---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 77CDEE77-FD5D-4C2D-B027-FF1F6FF6618E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: 2b6373944f8b7bbc741557629fad7c9f717e979e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882998"
---
# <span data-ttu-id="f56e1-101">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f56e1-101">Get-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="f56e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f56e1-102">SYNOPSIS</span></span>
<span data-ttu-id="f56e1-103">응용 프로그램 게이트웨이를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f56e1-103">Gets an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f56e1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f56e1-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGateway [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f56e1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f56e1-105">DESCRIPTION</span></span>
<span data-ttu-id="f56e1-106">**Get-AzureRmApplicationGateway** cmdlet은 응용 프로그램 게이트웨이를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f56e1-106">The **Get-AzureRmApplicationGateway** cmdlet gets an application gateway.</span></span>

## <span data-ttu-id="f56e1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f56e1-107">EXAMPLES</span></span>

### <span data-ttu-id="f56e1-108">예제 1: 지정 된 응용 프로그램 게이트웨이 가져오기</span><span class="sxs-lookup"><span data-stu-id="f56e1-108">Example 1: Get a specified application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f56e1-109">이 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져오고이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f56e1-109">This command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

### <span data-ttu-id="f56e1-110">예제 2: 리소스 그룹의 응용 프로그램 게이트웨이 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="f56e1-110">Example 2: Get a list of application gateways in a resource group</span></span>
```
PS C:\>$AppGwList = Get-AzureRmApplicationGateway -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f56e1-111">이 명령은 ResourceGroup01 이라는 리소스 그룹에 있는 모든 응용 프로그램 게이트웨이의 목록을 가져와이를 $AppGwList 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f56e1-111">This command gets a list of all the application gateways in the resource group named ResourceGroup01 and stores it in the $AppGwList variable.</span></span>

### <span data-ttu-id="f56e1-112">예제 3: 구독에서 응용 프로그램 게이트웨이 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="f56e1-112">Example 3: Get a list of application gateways in a subscription</span></span>
```
PS C:\>$AppGwList = Get-AzureRmApplicationGateway
```

<span data-ttu-id="f56e1-113">이 명령은 구독의 모든 응용 프로그램 게이트웨이 목록을 가져와 $AppGwList 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f56e1-113">This command gets a list of all the application gateways in the subscription and stores it in the $AppGwList variable.</span></span>

## <span data-ttu-id="f56e1-114">변수</span><span class="sxs-lookup"><span data-stu-id="f56e1-114">PARAMETERS</span></span>

### <span data-ttu-id="f56e1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f56e1-115">-DefaultProfile</span></span>
<span data-ttu-id="f56e1-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f56e1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f56e1-117">-이름</span><span class="sxs-lookup"><span data-stu-id="f56e1-117">-Name</span></span>
<span data-ttu-id="f56e1-118">이 cmdlet이 가져오는 응용 프로그램 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f56e1-118">Specifies the name of the application gateway that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f56e1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f56e1-119">-ResourceGroupName</span></span>
<span data-ttu-id="f56e1-120">응용 프로그램 게이트웨이를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f56e1-120">Specifies the name of the resource group that contains the application gateway.</span></span>

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

### <span data-ttu-id="f56e1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f56e1-121">CommonParameters</span></span>
<span data-ttu-id="f56e1-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f56e1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f56e1-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f56e1-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f56e1-124">입력</span><span class="sxs-lookup"><span data-stu-id="f56e1-124">INPUTS</span></span>

### <span data-ttu-id="f56e1-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f56e1-125">System.String</span></span>

## <span data-ttu-id="f56e1-126">출력</span><span class="sxs-lookup"><span data-stu-id="f56e1-126">OUTPUTS</span></span>

### <span data-ttu-id="f56e1-127">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f56e1-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f56e1-128">상속자</span><span class="sxs-lookup"><span data-stu-id="f56e1-128">NOTES</span></span>

## <span data-ttu-id="f56e1-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f56e1-129">RELATED LINKS</span></span>

[<span data-ttu-id="f56e1-130">중지-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f56e1-130">Stop-AzureRmApplicationGateway</span></span>](./Stop-AzureRmApplicationGateway.md)


