---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 7E40C4A2-8B9A-47E8-82AB-19208247349C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 893e03f8e59b3cd01e7d96ca2d04119ee6fb4c66
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045812"
---
# <span data-ttu-id="922d7-101">Set-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="922d7-101">Set-AzureSubnetRouteTable</span></span>

## <span data-ttu-id="922d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="922d7-102">SYNOPSIS</span></span>
<span data-ttu-id="922d7-103">라우팅 테이블을 서브넷에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="922d7-103">Associates a route table to a subnet.</span></span>

## <span data-ttu-id="922d7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="922d7-104">SYNTAX</span></span>

```
Set-AzureSubnetRouteTable -VirtualNetworkName <String> -SubnetName <String> -RouteTableName <String>
 [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="922d7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="922d7-105">DESCRIPTION</span></span>
<span data-ttu-id="922d7-106">**Set-AzureSubnetRouteTable** cmdlet은 경로 테이블을 서브넷에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="922d7-106">The **Set-AzureSubnetRouteTable** cmdlet associates a route table to a subnet.</span></span>

## <span data-ttu-id="922d7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="922d7-107">EXAMPLES</span></span>

### <span data-ttu-id="922d7-108">예제 1: 서브넷에 경로 테이블 연결</span><span class="sxs-lookup"><span data-stu-id="922d7-108">Example 1: Associate a route table to a subnet</span></span>
```
PS C:\> Set-AzureSubnetRouteTable -VirtualNetworkName "VNetUSCentral" -SubnetName "ContosoSubnet" -RouteTableName "PublicRouteTable"
```

<span data-ttu-id="922d7-109">이 명령은 PublicRouteTable 이라는 경로 테이블을 ContosoSubnet 이라는 서브넷에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="922d7-109">This command associates the route table named PublicRouteTable to the subnet named ContosoSubnet.</span></span>

## <span data-ttu-id="922d7-110">변수</span><span class="sxs-lookup"><span data-stu-id="922d7-110">PARAMETERS</span></span>

### <span data-ttu-id="922d7-111">-PassThru</span><span class="sxs-lookup"><span data-stu-id="922d7-111">-PassThru</span></span>
<span data-ttu-id="922d7-112">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="922d7-112">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="922d7-113">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="922d7-113">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="922d7-114">-프로필</span><span class="sxs-lookup"><span data-stu-id="922d7-114">-Profile</span></span>
<span data-ttu-id="922d7-115">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="922d7-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="922d7-116">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="922d7-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="922d7-117">-RouteTableName</span><span class="sxs-lookup"><span data-stu-id="922d7-117">-RouteTableName</span></span>
<span data-ttu-id="922d7-118">이 cmdlet가 서브넷과 연결 하는 경로 테이블의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="922d7-118">Specifies the name of the route table that this cmdlet associates with a subnet.</span></span>

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

### <span data-ttu-id="922d7-119">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="922d7-119">-SubnetName</span></span>
<span data-ttu-id="922d7-120">이 cmdlet이 경로 테이블을 연결 하는 서브넷을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="922d7-120">Specifies the subnet to which this cmdlet associates the route table.</span></span>

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

### <span data-ttu-id="922d7-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="922d7-121">-VirtualNetworkName</span></span>
<span data-ttu-id="922d7-122">이 cmdlet이 경로 테이블을 연결 하는 서브넷을 포함 하는 가상 네트워크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="922d7-122">Specifies the name of a virtual network that contains the subnet to which this cmdlet associates the route table.</span></span>

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

### <span data-ttu-id="922d7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="922d7-123">CommonParameters</span></span>
<span data-ttu-id="922d7-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="922d7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="922d7-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="922d7-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="922d7-126">입력</span><span class="sxs-lookup"><span data-stu-id="922d7-126">INPUTS</span></span>

## <span data-ttu-id="922d7-127">출력</span><span class="sxs-lookup"><span data-stu-id="922d7-127">OUTPUTS</span></span>

## <span data-ttu-id="922d7-128">상속자</span><span class="sxs-lookup"><span data-stu-id="922d7-128">NOTES</span></span>

## <span data-ttu-id="922d7-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="922d7-129">RELATED LINKS</span></span>

[<span data-ttu-id="922d7-130">Get-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="922d7-130">Get-AzureSubnetRouteTable</span></span>](./Get-AzureSubnetRouteTable.md)

[<span data-ttu-id="922d7-131">제거-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="922d7-131">Remove-AzureSubnetRouteTable</span></span>](./Remove-AzureSubnetRouteTable.md)
