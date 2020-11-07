---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 77CDEE77-FD5D-4C2D-B027-FF1F6FF6618E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGateway.md
ms.openlocfilehash: 61547a4ee5f60fccc371ca7b2c426ca1a4bbb005
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875649"
---
# <span data-ttu-id="302c6-101">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="302c6-101">Get-AzApplicationGateway</span></span>

## <span data-ttu-id="302c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="302c6-102">SYNOPSIS</span></span>
<span data-ttu-id="302c6-103">응용 프로그램 게이트웨이를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="302c6-103">Gets an application gateway.</span></span>

## <span data-ttu-id="302c6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="302c6-104">SYNTAX</span></span>

```
Get-AzApplicationGateway [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="302c6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="302c6-105">DESCRIPTION</span></span>
<span data-ttu-id="302c6-106">**Get-AzApplicationGateway** cmdlet은 응용 프로그램 게이트웨이를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="302c6-106">The **Get-AzApplicationGateway** cmdlet gets an application gateway.</span></span>

## <span data-ttu-id="302c6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="302c6-107">EXAMPLES</span></span>

### <span data-ttu-id="302c6-108">예제 1: 지정 된 응용 프로그램 게이트웨이 가져오기</span><span class="sxs-lookup"><span data-stu-id="302c6-108">Example 1: Get a specified application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="302c6-109">이 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져오고이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="302c6-109">This command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

### <span data-ttu-id="302c6-110">예제 2: 리소스 그룹의 응용 프로그램 게이트웨이 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="302c6-110">Example 2: Get a list of application gateways in a resource group</span></span>
```
PS C:\>$AppGwList = Get-AzApplicationGateway -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="302c6-111">이 명령은 ResourceGroup01 이라는 리소스 그룹에 있는 모든 응용 프로그램 게이트웨이의 목록을 가져와이를 $AppGwList 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="302c6-111">This command gets a list of all the application gateways in the resource group named ResourceGroup01 and stores it in the $AppGwList variable.</span></span>

### <span data-ttu-id="302c6-112">예제 3: 구독에서 응용 프로그램 게이트웨이 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="302c6-112">Example 3: Get a list of application gateways in a subscription</span></span>
```
PS C:\>$AppGwList = Get-AzApplicationGateway
```

<span data-ttu-id="302c6-113">이 명령은 구독의 모든 응용 프로그램 게이트웨이 목록을 가져와 $AppGwList 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="302c6-113">This command gets a list of all the application gateways in the subscription and stores it in the $AppGwList variable.</span></span>

## <span data-ttu-id="302c6-114">변수</span><span class="sxs-lookup"><span data-stu-id="302c6-114">PARAMETERS</span></span>

### <span data-ttu-id="302c6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="302c6-115">-DefaultProfile</span></span>
<span data-ttu-id="302c6-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="302c6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="302c6-117">-이름</span><span class="sxs-lookup"><span data-stu-id="302c6-117">-Name</span></span>
<span data-ttu-id="302c6-118">이 cmdlet이 가져오는 응용 프로그램 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="302c6-118">Specifies the name of the application gateway that this cmdlet gets.</span></span>

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

### <span data-ttu-id="302c6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="302c6-119">-ResourceGroupName</span></span>
<span data-ttu-id="302c6-120">응용 프로그램 게이트웨이를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="302c6-120">Specifies the name of the resource group that contains the application gateway.</span></span>

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

### <span data-ttu-id="302c6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="302c6-121">CommonParameters</span></span>
<span data-ttu-id="302c6-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="302c6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="302c6-123">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="302c6-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="302c6-124">입력</span><span class="sxs-lookup"><span data-stu-id="302c6-124">INPUTS</span></span>

### <span data-ttu-id="302c6-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="302c6-125">System.String</span></span>

## <span data-ttu-id="302c6-126">출력</span><span class="sxs-lookup"><span data-stu-id="302c6-126">OUTPUTS</span></span>

### <span data-ttu-id="302c6-127">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="302c6-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="302c6-128">상속자</span><span class="sxs-lookup"><span data-stu-id="302c6-128">NOTES</span></span>

## <span data-ttu-id="302c6-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="302c6-129">RELATED LINKS</span></span>

[<span data-ttu-id="302c6-130">중지-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="302c6-130">Stop-AzApplicationGateway</span></span>](./Stop-AzApplicationGateway.md)


