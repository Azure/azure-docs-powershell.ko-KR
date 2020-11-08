---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 5C8A79D1-32D4-4B30-AAC8-C6EF3B68017E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c2f695022e3a03d90443ad9ac2eb36ef8cb22ce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046135"
---
# <span data-ttu-id="fc1d3-101">Remove-AzureRoute</span><span class="sxs-lookup"><span data-stu-id="fc1d3-101">Remove-AzureRoute</span></span>

## <span data-ttu-id="fc1d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc1d3-102">SYNOPSIS</span></span>
<span data-ttu-id="fc1d3-103">경로 테이블에서 경로를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1d3-103">Removes a route from a route table.</span></span>

## <span data-ttu-id="fc1d3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fc1d3-104">SYNTAX</span></span>

```
Remove-AzureRoute -RouteName <String> [-Force] -RouteTable <IRouteTable> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="fc1d3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fc1d3-105">DESCRIPTION</span></span>
<span data-ttu-id="fc1d3-106">**AzureRoute** cmdlet은 경로 테이블에서 경로를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1d3-106">The **Remove-AzureRoute** cmdlet removes a route from a route table.</span></span>

## <span data-ttu-id="fc1d3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="fc1d3-107">EXAMPLES</span></span>

### <span data-ttu-id="fc1d3-108">예제 1: 경로 제거</span><span class="sxs-lookup"><span data-stu-id="fc1d3-108">Example 1: Remove a route</span></span>
```
PS C:\> Get-AzureRouteTable -Name "ApplianceRouteTable" | Remove-AzureRoute -RouteName "InternetRoute"
Confirm
Are you sure you want to remove the Route "InternetRoute" from Route Table "ApplianceRouteTable"?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute}                    AppRT                         Central US                    Appliance Route Table
```

<span data-ttu-id="fc1d3-109">이 명령은 ApplianceRouteTable 이라는 경로 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fc1d3-109">This command gets a route table named ApplianceRouteTable.</span></span>
<span data-ttu-id="fc1d3-110">명령이 현재 cmdlet에 경로 테이블을 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1d3-110">The command passes that route table to the current cmdlet.</span></span>
<span data-ttu-id="fc1d3-111">현재 cmdlet은 InternetRoute 라는 경로를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1d3-111">The current cmdlet removes a route named InternetRoute.</span></span>

## <span data-ttu-id="fc1d3-112">변수</span><span class="sxs-lookup"><span data-stu-id="fc1d3-112">PARAMETERS</span></span>

### <span data-ttu-id="fc1d3-113">-Force</span><span class="sxs-lookup"><span data-stu-id="fc1d3-113">-Force</span></span>
<span data-ttu-id="fc1d3-114">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1d3-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fc1d3-115">-프로필</span><span class="sxs-lookup"><span data-stu-id="fc1d3-115">-Profile</span></span>
<span data-ttu-id="fc1d3-116">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1d3-116">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="fc1d3-117">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1d3-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fc1d3-118">-RouteName</span><span class="sxs-lookup"><span data-stu-id="fc1d3-118">-RouteName</span></span>
<span data-ttu-id="fc1d3-119">이 cmdlet이 제거 하는 새 경로의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1d3-119">Specifies a name for the new route that this cmdlet removes.</span></span>

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

### <span data-ttu-id="fc1d3-120">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="fc1d3-120">-RouteTable</span></span>
<span data-ttu-id="fc1d3-121">이 cmdlet이 경로를 제거할 경로 테이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1d3-121">Specifies the route table from which this cmdlet removes a route.</span></span>

```yaml
Type: IRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc1d3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc1d3-122">CommonParameters</span></span>
<span data-ttu-id="fc1d3-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1d3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc1d3-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc1d3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc1d3-125">입력</span><span class="sxs-lookup"><span data-stu-id="fc1d3-125">INPUTS</span></span>

## <span data-ttu-id="fc1d3-126">출력</span><span class="sxs-lookup"><span data-stu-id="fc1d3-126">OUTPUTS</span></span>

## <span data-ttu-id="fc1d3-127">상속자</span><span class="sxs-lookup"><span data-stu-id="fc1d3-127">NOTES</span></span>

## <span data-ttu-id="fc1d3-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fc1d3-128">RELATED LINKS</span></span>

[<span data-ttu-id="fc1d3-129">Set-AzureRoute</span><span class="sxs-lookup"><span data-stu-id="fc1d3-129">Set-AzureRoute</span></span>](./Set-AzureRoute.md)


