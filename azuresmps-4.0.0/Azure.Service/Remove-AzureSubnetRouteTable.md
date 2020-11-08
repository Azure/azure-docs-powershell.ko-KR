---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: AA2F2793-03A5-41D9-8021-D18BE98DB044
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9bf26bd23ecc3dcb9e6973baf4c5eecf3d544402
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046456"
---
# <span data-ttu-id="e187a-101">Remove-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="e187a-101">Remove-AzureSubnetRouteTable</span></span>

## <span data-ttu-id="e187a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e187a-102">SYNOPSIS</span></span>
<span data-ttu-id="e187a-103">서브넷에서 경로 테이블 연결을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e187a-103">Removes a route table association from a subnet.</span></span>

## <span data-ttu-id="e187a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e187a-104">SYNTAX</span></span>

```
Remove-AzureSubnetRouteTable -VirtualNetworkName <String> -SubnetName <String> [-Force] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e187a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e187a-105">DESCRIPTION</span></span>
<span data-ttu-id="e187a-106">**Remove-AzureSubnetRouteTable** cmdlet은 서브넷에서 경로 테이블 연결을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e187a-106">The **Remove-AzureSubnetRouteTable** cmdlet removes a route table association from a subnet.</span></span>

## <span data-ttu-id="e187a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e187a-107">EXAMPLES</span></span>

### <span data-ttu-id="e187a-108">예제 1: 경로 테이블과 서브넷 간의 연결 제거</span><span class="sxs-lookup"><span data-stu-id="e187a-108">Example 1: Remove an association between a route table and a subnet</span></span>
```
PS C:\> Remove-AzureSubnetRouteTable -VirtualNetworkName "VNetUSCentral" -SubnetName "ContosoSubnet"
```

<span data-ttu-id="e187a-109">이 명령은 PublicRouteTable 이라는 경로 테이블의 연결을 ContosoSubnet 이라는 서브넷으로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e187a-109">This command removes the association of the route table named PublicRouteTable to the subnet named ContosoSubnet.</span></span>

## <span data-ttu-id="e187a-110">변수</span><span class="sxs-lookup"><span data-stu-id="e187a-110">PARAMETERS</span></span>

### <span data-ttu-id="e187a-111">-Force</span><span class="sxs-lookup"><span data-stu-id="e187a-111">-Force</span></span>
<span data-ttu-id="e187a-112">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e187a-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e187a-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e187a-113">-PassThru</span></span>
<span data-ttu-id="e187a-114">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e187a-114">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="e187a-115">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e187a-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e187a-116">-프로필</span><span class="sxs-lookup"><span data-stu-id="e187a-116">-Profile</span></span>
<span data-ttu-id="e187a-117">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e187a-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="e187a-118">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="e187a-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e187a-119">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="e187a-119">-SubnetName</span></span>
<span data-ttu-id="e187a-120">이 cmdlet이 경로 테이블을 제거 하는 서브넷을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e187a-120">Specifies the subnet for which this cmdlet removes the route table.</span></span>

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

### <span data-ttu-id="e187a-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="e187a-121">-VirtualNetworkName</span></span>
<span data-ttu-id="e187a-122">이 cmdlet이 경로 테이블을 제거 하는 서브넷을 포함 하는 가상 네트워크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e187a-122">Specifies the name of a virtual network that contains the subnet for which this cmdlet removes the route table.</span></span>

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

### <span data-ttu-id="e187a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e187a-123">CommonParameters</span></span>
<span data-ttu-id="e187a-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e187a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e187a-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e187a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e187a-126">입력</span><span class="sxs-lookup"><span data-stu-id="e187a-126">INPUTS</span></span>

## <span data-ttu-id="e187a-127">출력</span><span class="sxs-lookup"><span data-stu-id="e187a-127">OUTPUTS</span></span>

## <span data-ttu-id="e187a-128">상속자</span><span class="sxs-lookup"><span data-stu-id="e187a-128">NOTES</span></span>

## <span data-ttu-id="e187a-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e187a-129">RELATED LINKS</span></span>

[<span data-ttu-id="e187a-130">Get-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="e187a-130">Get-AzureSubnetRouteTable</span></span>](./Get-AzureSubnetRouteTable.md)

[<span data-ttu-id="e187a-131">Set-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="e187a-131">Set-AzureSubnetRouteTable</span></span>](./Set-AzureSubnetRouteTable.md)


