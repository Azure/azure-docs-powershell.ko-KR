---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 7F8C2223-5F82-4E4E-8057-44B72F7D5803
online version: ''
schema: 2.0.0
ms.openlocfilehash: a02d80d46696ff635da95c6bc29875f697f65fd4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046313"
---
# <span data-ttu-id="13108-101">Get-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="13108-101">Get-AzureRouteTable</span></span>

## <span data-ttu-id="13108-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13108-102">SYNOPSIS</span></span>
<span data-ttu-id="13108-103">경로 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="13108-103">Gets a route table.</span></span>

## <span data-ttu-id="13108-104">구문과</span><span class="sxs-lookup"><span data-stu-id="13108-104">SYNTAX</span></span>

```
Get-AzureRouteTable [-Name <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="13108-105">설명은</span><span class="sxs-lookup"><span data-stu-id="13108-105">DESCRIPTION</span></span>
<span data-ttu-id="13108-106">**Get-AzureRouteTable** cmdlet은 경로 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="13108-106">The **Get-AzureRouteTable** cmdlet gets a route table.</span></span>
<span data-ttu-id="13108-107">*자세한* 매개 변수를 지정 하 여 경로 테이블의 경로를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="13108-107">Specify the *Detailed* parameter to list the routes in the route table.</span></span>

## <span data-ttu-id="13108-108">예제의</span><span class="sxs-lookup"><span data-stu-id="13108-108">EXAMPLES</span></span>

### <span data-ttu-id="13108-109">예제 1: 경로 테이블에 대 한 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="13108-109">Example 1: Get details of a route table</span></span>
```
PS C:\> Get-AzureRouteTable -Name "ApplianceRouteTable" -Detailed
Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute}                    ApplianceRouteTable           Central US                    Appliance Route Table
```

<span data-ttu-id="13108-110">이 명령은 ApplianceRouteTable 이라는 경로 테이블의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="13108-110">This command gets the details of a route table named ApplianceRouteTable.</span></span>

## <span data-ttu-id="13108-111">변수</span><span class="sxs-lookup"><span data-stu-id="13108-111">PARAMETERS</span></span>

### <span data-ttu-id="13108-112">-세부 정보</span><span class="sxs-lookup"><span data-stu-id="13108-112">-Detailed</span></span>
<span data-ttu-id="13108-113">이 cmdlet에 경로 테이블의 경로가 표시 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="13108-113">Indicates that this cmdlet displays the routes in the route table.</span></span>

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

### <span data-ttu-id="13108-114">-이름</span><span class="sxs-lookup"><span data-stu-id="13108-114">-Name</span></span>
<span data-ttu-id="13108-115">이 cmdlet이 가져오는 경로 테이블의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13108-115">Specifies the name of the route table that this cmdlet gets.</span></span>

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

### <span data-ttu-id="13108-116">-프로필</span><span class="sxs-lookup"><span data-stu-id="13108-116">-Profile</span></span>
<span data-ttu-id="13108-117">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13108-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="13108-118">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="13108-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="13108-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13108-119">CommonParameters</span></span>
<span data-ttu-id="13108-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="13108-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13108-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13108-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13108-122">입력</span><span class="sxs-lookup"><span data-stu-id="13108-122">INPUTS</span></span>

## <span data-ttu-id="13108-123">출력</span><span class="sxs-lookup"><span data-stu-id="13108-123">OUTPUTS</span></span>

## <span data-ttu-id="13108-124">상속자</span><span class="sxs-lookup"><span data-stu-id="13108-124">NOTES</span></span>

## <span data-ttu-id="13108-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="13108-125">RELATED LINKS</span></span>

[<span data-ttu-id="13108-126">새로운 AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="13108-126">New-AzureRouteTable</span></span>](./New-AzureRouteTable.md)

[<span data-ttu-id="13108-127">제거-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="13108-127">Remove-AzureRouteTable</span></span>](./Remove-AzureRouteTable.md)


