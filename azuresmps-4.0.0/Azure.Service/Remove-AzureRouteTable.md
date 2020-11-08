---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 58329D8A-CB54-46FB-84A7-C31F00C13827
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6333430682de7693b6b87f9d037dea66725bfed8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046132"
---
# <span data-ttu-id="85ba5-101">Remove-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="85ba5-101">Remove-AzureRouteTable</span></span>

## <span data-ttu-id="85ba5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85ba5-102">SYNOPSIS</span></span>
<span data-ttu-id="85ba5-103">경로 테이블을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="85ba5-103">Removes a route table.</span></span>

## <span data-ttu-id="85ba5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="85ba5-104">SYNTAX</span></span>

```
Remove-AzureRouteTable -Name <String> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="85ba5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="85ba5-105">DESCRIPTION</span></span>
<span data-ttu-id="85ba5-106">**AzureRouteTable** cmdlet은 구독에서 경로 테이블을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="85ba5-106">The **Remove-AzureRouteTable** cmdlet removes a route table from your subscription.</span></span>
<span data-ttu-id="85ba5-107">경로 테이블이 서브넷에 연결 된 경우에는 테이블을 제거할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="85ba5-107">If a route table is associated to a subnet, you cannot remove the table.</span></span>

## <span data-ttu-id="85ba5-108">예제의</span><span class="sxs-lookup"><span data-stu-id="85ba5-108">EXAMPLES</span></span>

### <span data-ttu-id="85ba5-109">예제 1: 경로 테이블 제거</span><span class="sxs-lookup"><span data-stu-id="85ba5-109">Example 1: Remove a route table</span></span>
```
PS C:\> Remove-AzureRouteTable -Name "PublicRouteTable"
```

<span data-ttu-id="85ba5-110">이 명령은 PublicRouteTable 이라는 경로 테이블을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="85ba5-110">This command removes the route table named PublicRouteTable.</span></span>

## <span data-ttu-id="85ba5-111">변수</span><span class="sxs-lookup"><span data-stu-id="85ba5-111">PARAMETERS</span></span>

### <span data-ttu-id="85ba5-112">-Force</span><span class="sxs-lookup"><span data-stu-id="85ba5-112">-Force</span></span>
<span data-ttu-id="85ba5-113">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="85ba5-113">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85ba5-114">-이름</span><span class="sxs-lookup"><span data-stu-id="85ba5-114">-Name</span></span>
<span data-ttu-id="85ba5-115">이 cmdlet이 제거 하는 경로 테이블의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="85ba5-115">Specifies the name of the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="85ba5-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85ba5-116">-PassThru</span></span>
<span data-ttu-id="85ba5-117">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="85ba5-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="85ba5-118">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="85ba5-118">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85ba5-119">-프로필</span><span class="sxs-lookup"><span data-stu-id="85ba5-119">-Profile</span></span>
<span data-ttu-id="85ba5-120">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="85ba5-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="85ba5-121">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="85ba5-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="85ba5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85ba5-122">CommonParameters</span></span>
<span data-ttu-id="85ba5-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="85ba5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85ba5-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85ba5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85ba5-125">입력</span><span class="sxs-lookup"><span data-stu-id="85ba5-125">INPUTS</span></span>

## <span data-ttu-id="85ba5-126">출력</span><span class="sxs-lookup"><span data-stu-id="85ba5-126">OUTPUTS</span></span>

## <span data-ttu-id="85ba5-127">상속자</span><span class="sxs-lookup"><span data-stu-id="85ba5-127">NOTES</span></span>

## <span data-ttu-id="85ba5-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="85ba5-128">RELATED LINKS</span></span>

[<span data-ttu-id="85ba5-129">Get-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="85ba5-129">Get-AzureRouteTable</span></span>](./Get-AzureRouteTable.md)

[<span data-ttu-id="85ba5-130">새로운 AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="85ba5-130">New-AzureRouteTable</span></span>](./New-AzureRouteTable.md)
