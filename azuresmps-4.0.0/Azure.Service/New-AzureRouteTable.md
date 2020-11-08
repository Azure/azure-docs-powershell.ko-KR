---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: F4BADE88-28A2-42FB-9578-93D65148709E
online version: ''
schema: 2.0.0
ms.openlocfilehash: f73e47ec25d44d3965279066de98585ae2cbaee7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045989"
---
# <span data-ttu-id="a6b87-101">New-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="a6b87-101">New-AzureRouteTable</span></span>

## <span data-ttu-id="a6b87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6b87-102">SYNOPSIS</span></span>
<span data-ttu-id="a6b87-103">경로 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a6b87-103">Creates a route table.</span></span>

## <span data-ttu-id="a6b87-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a6b87-104">SYNTAX</span></span>

```
New-AzureRouteTable -Name <String> -Location <String> [-Label <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="a6b87-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a6b87-105">DESCRIPTION</span></span>
<span data-ttu-id="a6b87-106">**AzureRouteTable** cmdlet은 지정 된 위치에 경로 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a6b87-106">The **New-AzureRouteTable** cmdlet creates a route table in a specified location.</span></span>
<span data-ttu-id="a6b87-107">경로 테이블에 사용자 정의 경로를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6b87-107">You can add user-defined routes to the route table.</span></span>
<span data-ttu-id="a6b87-108">가상 네트워크의 서브넷에 경로 테이블을 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6b87-108">You can associate the route table to a subnet in a virtual network.</span></span>

## <span data-ttu-id="a6b87-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a6b87-109">EXAMPLES</span></span>

## <span data-ttu-id="a6b87-110">변수</span><span class="sxs-lookup"><span data-stu-id="a6b87-110">PARAMETERS</span></span>

### <span data-ttu-id="a6b87-111">-레이블</span><span class="sxs-lookup"><span data-stu-id="a6b87-111">-Label</span></span>
<span data-ttu-id="a6b87-112">새 경로 테이블에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6b87-112">Specifies a description for the new route table.</span></span>

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

### <span data-ttu-id="a6b87-113">-위치</span><span class="sxs-lookup"><span data-stu-id="a6b87-113">-Location</span></span>
<span data-ttu-id="a6b87-114">이 cmdlet에서 경로 테이블을 만드는 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6b87-114">Specifies the location in which this cmdlet creates the route table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6b87-115">-이름</span><span class="sxs-lookup"><span data-stu-id="a6b87-115">-Name</span></span>
<span data-ttu-id="a6b87-116">이 cmdlet이 만드는 경로 테이블의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6b87-116">Specifies a name for the route table that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6b87-117">-프로필</span><span class="sxs-lookup"><span data-stu-id="a6b87-117">-Profile</span></span>
<span data-ttu-id="a6b87-118">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6b87-118">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="a6b87-119">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="a6b87-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a6b87-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6b87-120">CommonParameters</span></span>
<span data-ttu-id="a6b87-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6b87-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6b87-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6b87-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6b87-123">입력</span><span class="sxs-lookup"><span data-stu-id="a6b87-123">INPUTS</span></span>

## <span data-ttu-id="a6b87-124">출력</span><span class="sxs-lookup"><span data-stu-id="a6b87-124">OUTPUTS</span></span>

## <span data-ttu-id="a6b87-125">상속자</span><span class="sxs-lookup"><span data-stu-id="a6b87-125">NOTES</span></span>

## <span data-ttu-id="a6b87-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a6b87-126">RELATED LINKS</span></span>

[<span data-ttu-id="a6b87-127">Get-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="a6b87-127">Get-AzureRouteTable</span></span>](./Get-AzureRouteTable.md)

[<span data-ttu-id="a6b87-128">제거-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="a6b87-128">Remove-AzureRouteTable</span></span>](./Remove-AzureRouteTable.md)


