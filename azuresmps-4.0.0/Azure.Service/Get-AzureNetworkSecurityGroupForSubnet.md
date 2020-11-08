---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 4D75240C-F2B5-4273-848C-107308DD6837
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d56de5b27565f7bfdd90198ad45e2766da521f4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045638"
---
# <span data-ttu-id="cbd4b-101">Get-AzureNetworkSecurityGroupForSubnet</span><span class="sxs-lookup"><span data-stu-id="cbd4b-101">Get-AzureNetworkSecurityGroupForSubnet</span></span>

## <span data-ttu-id="cbd4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbd4b-102">SYNOPSIS</span></span>
<span data-ttu-id="cbd4b-103">서브넷에 대 한 네트워크 보안 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cbd4b-103">Gets the network security group for a subnet.</span></span>

## <span data-ttu-id="cbd4b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cbd4b-104">SYNTAX</span></span>

```
Get-AzureNetworkSecurityGroupForSubnet -VirtualNetworkName <String> -SubnetName <String> [-Detailed]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="cbd4b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cbd4b-105">DESCRIPTION</span></span>
<span data-ttu-id="cbd4b-106">**AzureNetworkSecurityGroupForSubnet** cmdlet은 서브넷에 연결 된 네트워크 보안 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cbd4b-106">The **Get-AzureNetworkSecurityGroupForSubnet** cmdlet gets the network security group that is associated to a subnet.</span></span>

## <span data-ttu-id="cbd4b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cbd4b-107">EXAMPLES</span></span>

## <span data-ttu-id="cbd4b-108">변수</span><span class="sxs-lookup"><span data-stu-id="cbd4b-108">PARAMETERS</span></span>

### <span data-ttu-id="cbd4b-109">-세부 정보</span><span class="sxs-lookup"><span data-stu-id="cbd4b-109">-Detailed</span></span>
<span data-ttu-id="cbd4b-110">이 cmdlet에 네트워크 보안 규칙이 표시 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="cbd4b-110">Indicates that this cmdlet displays the network security rules.</span></span>

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

### <span data-ttu-id="cbd4b-111">-프로필</span><span class="sxs-lookup"><span data-stu-id="cbd4b-111">-Profile</span></span>
<span data-ttu-id="cbd4b-112">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbd4b-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cbd4b-113">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="cbd4b-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cbd4b-114">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="cbd4b-114">-SubnetName</span></span>
<span data-ttu-id="cbd4b-115">이 cmdlet이 네트워크 보안 그룹을 가져오는 서브넷의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbd4b-115">Specifies the name of a subnet for which this cmdlet gets a network security group.</span></span>

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

### <span data-ttu-id="cbd4b-116">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="cbd4b-116">-VirtualNetworkName</span></span>
<span data-ttu-id="cbd4b-117">가상 네트워크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbd4b-117">Specifies the name of a virtual network.</span></span>
<span data-ttu-id="cbd4b-118">이 cmdlet은이 매개 변수에서 지정 하는 가상 네트워크의 서브넷에 대 한 네트워크 보안 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cbd4b-118">This cmdlet gets a network security group for a subnet in the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="cbd4b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbd4b-119">CommonParameters</span></span>
<span data-ttu-id="cbd4b-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbd4b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbd4b-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbd4b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbd4b-122">입력</span><span class="sxs-lookup"><span data-stu-id="cbd4b-122">INPUTS</span></span>

## <span data-ttu-id="cbd4b-123">출력</span><span class="sxs-lookup"><span data-stu-id="cbd4b-123">OUTPUTS</span></span>

## <span data-ttu-id="cbd4b-124">상속자</span><span class="sxs-lookup"><span data-stu-id="cbd4b-124">NOTES</span></span>

## <span data-ttu-id="cbd4b-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cbd4b-125">RELATED LINKS</span></span>

[<span data-ttu-id="cbd4b-126">제거-AzureNetworkSecurityGroupFromSubnet</span><span class="sxs-lookup"><span data-stu-id="cbd4b-126">Remove-AzureNetworkSecurityGroupFromSubnet</span></span>](./Remove-AzureNetworkSecurityGroupFromSubnet.md)

[<span data-ttu-id="cbd4b-127">Set-AzureNetworkSecurityGroupToSubnet</span><span class="sxs-lookup"><span data-stu-id="cbd4b-127">Set-AzureNetworkSecurityGroupToSubnet</span></span>](./Set-AzureNetworkSecurityGroupToSubnet.md)
