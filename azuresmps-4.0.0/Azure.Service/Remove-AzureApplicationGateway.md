---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 128AD64D-709A-4B59-B233-4221A9120AE1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4803fd24952066c4dcea72daaf0c999b64ae4c5d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046497"
---
# <span data-ttu-id="69a6f-101">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="69a6f-101">Remove-AzureApplicationGateway</span></span>

## <span data-ttu-id="69a6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69a6f-102">SYNOPSIS</span></span>
<span data-ttu-id="69a6f-103">응용 프로그램 게이트웨이를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="69a6f-103">Removes an application gateway.</span></span>

## <span data-ttu-id="69a6f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="69a6f-104">SYNTAX</span></span>

```
Remove-AzureApplicationGateway -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="69a6f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="69a6f-105">DESCRIPTION</span></span>
<span data-ttu-id="69a6f-106">**제거-AzureApplicationGateway** cmdlet은 응용 프로그램 게이트웨이를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="69a6f-106">The **Remove-AzureApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="69a6f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="69a6f-107">EXAMPLES</span></span>

### <span data-ttu-id="69a6f-108">예제 1: 응용 프로그램 게이트웨이 제거</span><span class="sxs-lookup"><span data-stu-id="69a6f-108">Example 1: Remove an application gateway</span></span>
```
PS C:\> Remove-AzureApplicationGateway -Name "ApplicationGateway06"
```

<span data-ttu-id="69a6f-109">이 명령은 ApplicationGateway06 이라는 응용 프로그램 게이트웨이를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="69a6f-109">This command removes the application gateway named ApplicationGateway06.</span></span>

## <span data-ttu-id="69a6f-110">변수</span><span class="sxs-lookup"><span data-stu-id="69a6f-110">PARAMETERS</span></span>

### <span data-ttu-id="69a6f-111">-이름</span><span class="sxs-lookup"><span data-stu-id="69a6f-111">-Name</span></span>
<span data-ttu-id="69a6f-112">이 cmdlet이 제거 하는 응용 프로그램 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69a6f-112">Specifies the name of the application gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="69a6f-113">-프로필</span><span class="sxs-lookup"><span data-stu-id="69a6f-113">-Profile</span></span>
<span data-ttu-id="69a6f-114">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69a6f-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="69a6f-115">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="69a6f-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="69a6f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69a6f-116">CommonParameters</span></span>
<span data-ttu-id="69a6f-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="69a6f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69a6f-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69a6f-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69a6f-119">입력</span><span class="sxs-lookup"><span data-stu-id="69a6f-119">INPUTS</span></span>

### <span data-ttu-id="69a6f-120">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="69a6f-120">System.String</span></span>

## <span data-ttu-id="69a6f-121">출력</span><span class="sxs-lookup"><span data-stu-id="69a6f-121">OUTPUTS</span></span>

### <span data-ttu-id="69a6f-122">WindowsAzure의. i a m a 관리 응답</span><span class="sxs-lookup"><span data-stu-id="69a6f-122">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="69a6f-123">상속자</span><span class="sxs-lookup"><span data-stu-id="69a6f-123">NOTES</span></span>

## <span data-ttu-id="69a6f-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="69a6f-124">RELATED LINKS</span></span>

[<span data-ttu-id="69a6f-125">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="69a6f-125">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="69a6f-126">새 AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="69a6f-126">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="69a6f-127">시작-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="69a6f-127">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="69a6f-128">Stop-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="69a6f-128">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)

[<span data-ttu-id="69a6f-129">업데이트-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="69a6f-129">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)


