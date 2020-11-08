---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 0AED21E8-A638-4019-9B23-447472E56C7A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 202066cfc2649b0f56810123e211bbeb5d69720f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045670"
---
# <span data-ttu-id="251ca-101">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="251ca-101">Get-AzureApplicationGateway</span></span>

## <span data-ttu-id="251ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="251ca-102">SYNOPSIS</span></span>
<span data-ttu-id="251ca-103">응용 프로그램 게이트웨이를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="251ca-103">Gets an Application Gateway.</span></span>

## <span data-ttu-id="251ca-104">구문과</span><span class="sxs-lookup"><span data-stu-id="251ca-104">SYNTAX</span></span>

```
Get-AzureApplicationGateway [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="251ca-105">설명은</span><span class="sxs-lookup"><span data-stu-id="251ca-105">DESCRIPTION</span></span>
<span data-ttu-id="251ca-106">**Get-AzureApplicationGateway** cmdlet은 기존 Azure Application gateway를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="251ca-106">The **Get-AzureApplicationGateway** cmdlet gets an existing Azure Application Gateway.</span></span>

## <span data-ttu-id="251ca-107">예제의</span><span class="sxs-lookup"><span data-stu-id="251ca-107">EXAMPLES</span></span>

### <span data-ttu-id="251ca-108">예제 1: 응용 프로그램 게이트웨이 가져오기</span><span class="sxs-lookup"><span data-stu-id="251ca-108">Example 1: Get an Application Gateway</span></span>
```
PS C:\> Get-AzureApplicationGateway -Name "ApplicationGateway06"
```

<span data-ttu-id="251ca-109">이 명령은 ApplicationGateway06 이라는 응용 프로그램 게이트웨이를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="251ca-109">This command gets the Application Gateway named ApplicationGateway06.</span></span>

### <span data-ttu-id="251ca-110">예제 2: 모든 응용 프로그램 게이트웨이 가져오기</span><span class="sxs-lookup"><span data-stu-id="251ca-110">Example 2: Get all Application Gateways</span></span>
```
PS C:\> Get-AzureApplicationGateway
```

<span data-ttu-id="251ca-111">이 명령은 구독 하는 모든 응용 프로그램 게이트웨이를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="251ca-111">This command gets all the Application Gateways under your subscription.</span></span>

## <span data-ttu-id="251ca-112">변수</span><span class="sxs-lookup"><span data-stu-id="251ca-112">PARAMETERS</span></span>

### <span data-ttu-id="251ca-113">-이름</span><span class="sxs-lookup"><span data-stu-id="251ca-113">-Name</span></span>
<span data-ttu-id="251ca-114">이 cmdlet이 가져오는 응용 프로그램 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="251ca-114">Specifies the name of the Application Gateway that this cmdlet gets.</span></span>

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

### <span data-ttu-id="251ca-115">-프로필</span><span class="sxs-lookup"><span data-stu-id="251ca-115">-Profile</span></span>
<span data-ttu-id="251ca-116">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="251ca-116">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="251ca-117">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="251ca-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="251ca-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="251ca-118">CommonParameters</span></span>
<span data-ttu-id="251ca-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="251ca-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="251ca-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="251ca-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="251ca-121">입력</span><span class="sxs-lookup"><span data-stu-id="251ca-121">INPUTS</span></span>

### <span data-ttu-id="251ca-122">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="251ca-122">System.String</span></span>

## <span data-ttu-id="251ca-123">출력</span><span class="sxs-lookup"><span data-stu-id="251ca-123">OUTPUTS</span></span>

### <span data-ttu-id="251ca-124">Microsoft. 네트워킹과. i m m. i m a m a i m a m a i m a i<. i m a i m a i m a i m/ApplicationGateway object></span><span class="sxs-lookup"><span data-stu-id="251ca-124">Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGateway, IEnumerable<Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGateway></span></span>

## <span data-ttu-id="251ca-125">상속자</span><span class="sxs-lookup"><span data-stu-id="251ca-125">NOTES</span></span>

## <span data-ttu-id="251ca-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="251ca-126">RELATED LINKS</span></span>

[<span data-ttu-id="251ca-127">새 AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="251ca-127">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="251ca-128">-AzureApplicationGateway 제거</span><span class="sxs-lookup"><span data-stu-id="251ca-128">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="251ca-129">시작-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="251ca-129">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="251ca-130">Stop-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="251ca-130">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)

[<span data-ttu-id="251ca-131">업데이트-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="251ca-131">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)


