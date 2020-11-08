---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: AEFC9094-144F-4E29-AC5A-DBFDA175A920
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8e56496c1fdf04b5227121f5ac39193938a2214e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045542"
---
# <span data-ttu-id="f63d6-101">Get-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="f63d6-101">Get-AzureSubnetRouteTable</span></span>

## <span data-ttu-id="f63d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f63d6-102">SYNOPSIS</span></span>
<span data-ttu-id="f63d6-103">서브넷에 대 한 경로 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f63d6-103">Gets a route table for a subnet.</span></span>

## <span data-ttu-id="f63d6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f63d6-104">SYNTAX</span></span>

```
Get-AzureSubnetRouteTable -VirtualNetworkName <String> -SubnetName <String> [-Detailed]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f63d6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f63d6-105">DESCRIPTION</span></span>
<span data-ttu-id="f63d6-106">**Get-AzureSubnetRouteTable** cmdlet은 서브넷과 연결 된 경로 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f63d6-106">The **Get-AzureSubnetRouteTable** cmdlet gets the route table that is associated with a subnet.</span></span>

## <span data-ttu-id="f63d6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f63d6-107">EXAMPLES</span></span>

### <span data-ttu-id="f63d6-108">예제 1: 서브넷에 대 한 경로 표시</span><span class="sxs-lookup"><span data-stu-id="f63d6-108">Example 1: Display routes for a subnet</span></span>
```
PS C:\> Get-AzureSubnetRouteTable -VirtualNetworkName "VNetUSCentral" -SubnetName "ContosoSubnet" -Detailed
Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{internetroute}               PublicRT                      Central US                    Sample RT in Central US
```

<span data-ttu-id="f63d6-109">이 명령은 ContosoSubnet 이라는 서브넷과 연결 된 경로 테이블 이름에 경로를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f63d6-109">This command displays the routes in the route table name that is associated with subnet named ContosoSubnet.</span></span>

## <span data-ttu-id="f63d6-110">변수</span><span class="sxs-lookup"><span data-stu-id="f63d6-110">PARAMETERS</span></span>

### <span data-ttu-id="f63d6-111">-세부 정보</span><span class="sxs-lookup"><span data-stu-id="f63d6-111">-Detailed</span></span>
<span data-ttu-id="f63d6-112">이 cmdlet에 서브넷과 연결 된 경로 테이블의 경로가 표시 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f63d6-112">Indicates that this cmdlet displays the routes in the route table that is associated with the subnet.</span></span>

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

### <span data-ttu-id="f63d6-113">-프로필</span><span class="sxs-lookup"><span data-stu-id="f63d6-113">-Profile</span></span>
<span data-ttu-id="f63d6-114">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f63d6-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="f63d6-115">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="f63d6-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f63d6-116">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="f63d6-116">-SubnetName</span></span>
<span data-ttu-id="f63d6-117">이 cmdlet이 경로 테이블을 가져오는 서브넷을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f63d6-117">Specifies the subnet for which this cmdlet gets the route table.</span></span>

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

### <span data-ttu-id="f63d6-118">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="f63d6-118">-VirtualNetworkName</span></span>
<span data-ttu-id="f63d6-119">이 cmdlet이 경로 테이블을 가져오는 서브넷을 포함 하는 가상 네트워크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f63d6-119">Specifies the name of a virtual network that contains the subnet for which this cmdlet gets the route table.</span></span>

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

### <span data-ttu-id="f63d6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f63d6-120">CommonParameters</span></span>
<span data-ttu-id="f63d6-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f63d6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f63d6-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f63d6-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f63d6-123">입력</span><span class="sxs-lookup"><span data-stu-id="f63d6-123">INPUTS</span></span>

## <span data-ttu-id="f63d6-124">출력</span><span class="sxs-lookup"><span data-stu-id="f63d6-124">OUTPUTS</span></span>

## <span data-ttu-id="f63d6-125">상속자</span><span class="sxs-lookup"><span data-stu-id="f63d6-125">NOTES</span></span>

## <span data-ttu-id="f63d6-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f63d6-126">RELATED LINKS</span></span>

[<span data-ttu-id="f63d6-127">제거-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="f63d6-127">Remove-AzureSubnetRouteTable</span></span>](./Remove-AzureSubnetRouteTable.md)

[<span data-ttu-id="f63d6-128">Set-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="f63d6-128">Set-AzureSubnetRouteTable</span></span>](./Set-AzureSubnetRouteTable.md)


