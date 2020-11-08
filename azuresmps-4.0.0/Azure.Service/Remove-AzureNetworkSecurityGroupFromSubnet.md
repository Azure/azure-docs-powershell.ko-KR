---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: BABA5142-541F-40C8-AFF5-20E4283BE147
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a718e2f675b4a5e204610a2d4f1fb1aac4c5478
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046150"
---
# <span data-ttu-id="27fe2-101">Remove-AzureNetworkSecurityGroupFromSubnet</span><span class="sxs-lookup"><span data-stu-id="27fe2-101">Remove-AzureNetworkSecurityGroupFromSubnet</span></span>

## <span data-ttu-id="27fe2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27fe2-102">SYNOPSIS</span></span>
<span data-ttu-id="27fe2-103">Dissociates 서브넷에서 네트워크 보안 그룹을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="27fe2-103">Dissociates a network security group from a subnet.</span></span>

## <span data-ttu-id="27fe2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="27fe2-104">SYNTAX</span></span>

```
Remove-AzureNetworkSecurityGroupFromSubnet -Name <String> -VirtualNetworkName <String> -SubnetName <String>
 [-Force] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="27fe2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="27fe2-105">DESCRIPTION</span></span>
<span data-ttu-id="27fe2-106">**AzureNetworkSecurityGroupFromSubnet** cmdlet은 서브넷에서 Azure 네트워크 보안 그룹을 dissociates 합니다.</span><span class="sxs-lookup"><span data-stu-id="27fe2-106">The **Remove-AzureNetworkSecurityGroupFromSubnet** cmdlet dissociates an Azure network security group from a subnet.</span></span>

## <span data-ttu-id="27fe2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="27fe2-107">EXAMPLES</span></span>

## <span data-ttu-id="27fe2-108">변수</span><span class="sxs-lookup"><span data-stu-id="27fe2-108">PARAMETERS</span></span>

### <span data-ttu-id="27fe2-109">-Force</span><span class="sxs-lookup"><span data-stu-id="27fe2-109">-Force</span></span>
<span data-ttu-id="27fe2-110">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="27fe2-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="27fe2-111">-이름</span><span class="sxs-lookup"><span data-stu-id="27fe2-111">-Name</span></span>
<span data-ttu-id="27fe2-112">이 cmdlet이 서브넷에서 dissociates는 네트워크 보안 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="27fe2-112">Specifies the name of the network security group that this cmdlet dissociates from a subnet.</span></span>

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

### <span data-ttu-id="27fe2-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="27fe2-113">-PassThru</span></span>
<span data-ttu-id="27fe2-114">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="27fe2-114">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="27fe2-115">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="27fe2-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="27fe2-116">-프로필</span><span class="sxs-lookup"><span data-stu-id="27fe2-116">-Profile</span></span>
<span data-ttu-id="27fe2-117">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="27fe2-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="27fe2-118">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="27fe2-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="27fe2-119">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="27fe2-119">-SubnetName</span></span>
<span data-ttu-id="27fe2-120">이 cmdlet이 네트워크 보안 그룹을 dissociates 하는 서브넷의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="27fe2-120">Specifies the name of a subnet from which this cmdlet dissociates a network security group.</span></span>

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

### <span data-ttu-id="27fe2-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="27fe2-121">-VirtualNetworkName</span></span>
<span data-ttu-id="27fe2-122">가상 네트워크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="27fe2-122">Specifies the name of a virtual network.</span></span>
<span data-ttu-id="27fe2-123">이 cmdlet은이 매개 변수에서 지정 하는 가상 네트워크의 서브넷에서 네트워크 보안 그룹의 분리를 끊습니다.</span><span class="sxs-lookup"><span data-stu-id="27fe2-123">This cmdlet disassociates a network security group from a subnet in the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="27fe2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27fe2-124">CommonParameters</span></span>
<span data-ttu-id="27fe2-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="27fe2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27fe2-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27fe2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27fe2-127">입력</span><span class="sxs-lookup"><span data-stu-id="27fe2-127">INPUTS</span></span>

## <span data-ttu-id="27fe2-128">출력</span><span class="sxs-lookup"><span data-stu-id="27fe2-128">OUTPUTS</span></span>

## <span data-ttu-id="27fe2-129">상속자</span><span class="sxs-lookup"><span data-stu-id="27fe2-129">NOTES</span></span>

## <span data-ttu-id="27fe2-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="27fe2-130">RELATED LINKS</span></span>

[<span data-ttu-id="27fe2-131">Get-AzureNetworkSecurityGroupForSubnet</span><span class="sxs-lookup"><span data-stu-id="27fe2-131">Get-AzureNetworkSecurityGroupForSubnet</span></span>](./Get-AzureNetworkSecurityGroupForSubnet.md)

[<span data-ttu-id="27fe2-132">Set-AzureNetworkSecurityGroupToSubnet</span><span class="sxs-lookup"><span data-stu-id="27fe2-132">Set-AzureNetworkSecurityGroupToSubnet</span></span>](./Set-AzureNetworkSecurityGroupToSubnet.md)


