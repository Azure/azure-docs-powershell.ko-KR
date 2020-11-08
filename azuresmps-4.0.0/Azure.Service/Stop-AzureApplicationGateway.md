---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 17BA2ED5-E347-45C0-AF20-CDD288469514
online version: ''
schema: 2.0.0
ms.openlocfilehash: a07afcadb2207f2e4377601abfa6094bc3293328
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046408"
---
# <span data-ttu-id="e47d3-101">Stop-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e47d3-101">Stop-AzureApplicationGateway</span></span>

## <span data-ttu-id="e47d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e47d3-102">SYNOPSIS</span></span>
<span data-ttu-id="e47d3-103">응용 프로그램 게이트웨이를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="e47d3-103">Stops an application gateway.</span></span>

## <span data-ttu-id="e47d3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e47d3-104">SYNTAX</span></span>

```
Stop-AzureApplicationGateway -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e47d3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e47d3-105">DESCRIPTION</span></span>
<span data-ttu-id="e47d3-106">**Stop-AzureApplicationGateway** cmdlet은 응용 프로그램 게이트웨이를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="e47d3-106">The **Stop-AzureApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="e47d3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e47d3-107">EXAMPLES</span></span>

### <span data-ttu-id="e47d3-108">예제 1: 응용 프로그램 게이트웨이 중지</span><span class="sxs-lookup"><span data-stu-id="e47d3-108">Example 1: Stop an application gateway</span></span>
```
PS C:\> Stop-AzureApplicationGateway -Name "ApplicationGateway06"
```

<span data-ttu-id="e47d3-109">이 명령은 ApplicationGateway06 이라는 응용 프로그램 게이트웨이를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="e47d3-109">This command stops the application gateway named ApplicationGateway06.</span></span>

## <span data-ttu-id="e47d3-110">변수</span><span class="sxs-lookup"><span data-stu-id="e47d3-110">PARAMETERS</span></span>

### <span data-ttu-id="e47d3-111">-이름</span><span class="sxs-lookup"><span data-stu-id="e47d3-111">-Name</span></span>
<span data-ttu-id="e47d3-112">이 cmdlet이 중지 하는 응용 프로그램 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e47d3-112">Specifies the name of the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="e47d3-113">-프로필</span><span class="sxs-lookup"><span data-stu-id="e47d3-113">-Profile</span></span>
<span data-ttu-id="e47d3-114">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e47d3-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e47d3-115">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="e47d3-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e47d3-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e47d3-116">CommonParameters</span></span>
<span data-ttu-id="e47d3-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e47d3-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e47d3-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e47d3-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e47d3-119">입력</span><span class="sxs-lookup"><span data-stu-id="e47d3-119">INPUTS</span></span>

### <span data-ttu-id="e47d3-120">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e47d3-120">System.String</span></span>

## <span data-ttu-id="e47d3-121">출력</span><span class="sxs-lookup"><span data-stu-id="e47d3-121">OUTPUTS</span></span>

### <span data-ttu-id="e47d3-122">WindowsAzure의. i a m a 관리 응답</span><span class="sxs-lookup"><span data-stu-id="e47d3-122">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="e47d3-123">상속자</span><span class="sxs-lookup"><span data-stu-id="e47d3-123">NOTES</span></span>

## <span data-ttu-id="e47d3-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e47d3-124">RELATED LINKS</span></span>

[<span data-ttu-id="e47d3-125">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e47d3-125">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="e47d3-126">새 AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e47d3-126">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="e47d3-127">-AzureApplicationGateway 제거</span><span class="sxs-lookup"><span data-stu-id="e47d3-127">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="e47d3-128">시작-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e47d3-128">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="e47d3-129">업데이트-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e47d3-129">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)
