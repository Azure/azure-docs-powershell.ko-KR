---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A14F9105-1422-4073-96CF-E75CFC039E05
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7eaf1af2efe3f93f4e0a44d54e1f07ea52166942
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045829"
---
# <span data-ttu-id="b81ae-101">Set-AzureNetworkSecurityGroupToSubnet</span><span class="sxs-lookup"><span data-stu-id="b81ae-101">Set-AzureNetworkSecurityGroupToSubnet</span></span>

## <span data-ttu-id="b81ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b81ae-102">SYNOPSIS</span></span>
<span data-ttu-id="b81ae-103">네트워크 보안 그룹을 서브넷에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="b81ae-103">Associates a network security group to a subnet.</span></span>

## <span data-ttu-id="b81ae-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b81ae-104">SYNTAX</span></span>

```
Set-AzureNetworkSecurityGroupToSubnet -Name <String> -VirtualNetworkName <String> -SubnetName <String> [-Force]
 [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b81ae-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b81ae-105">DESCRIPTION</span></span>
<span data-ttu-id="b81ae-106">**AzureNetworkSecurityGroupToSubnet** Cmdlet은 Azure 네트워크 보안 그룹을 서브넷에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="b81ae-106">The **Set-AzureNetworkSecurityGroupToSubnet** cmdlet associates an Azure network security group to a subnet.</span></span>

## <span data-ttu-id="b81ae-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b81ae-107">EXAMPLES</span></span>

## <span data-ttu-id="b81ae-108">변수</span><span class="sxs-lookup"><span data-stu-id="b81ae-108">PARAMETERS</span></span>

### <span data-ttu-id="b81ae-109">-Force</span><span class="sxs-lookup"><span data-stu-id="b81ae-109">-Force</span></span>
<span data-ttu-id="b81ae-110">이 cmdlet이 서브넷에서 이전 네트워크 보안 그룹의 제거를 확인 하 라는 메시지를 표시 하지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b81ae-110">Indicates that this cmdlet does not prompt you to confirm the removal of a previous network security group from the subnet.</span></span>

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

### <span data-ttu-id="b81ae-111">-이름</span><span class="sxs-lookup"><span data-stu-id="b81ae-111">-Name</span></span>
<span data-ttu-id="b81ae-112">이 cmdlet가 서브넷에 연결 하는 네트워크 보안 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b81ae-112">Specifies the name of the network security group that this cmdlet associates to a subnet.</span></span>

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

### <span data-ttu-id="b81ae-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b81ae-113">-PassThru</span></span>
<span data-ttu-id="b81ae-114">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b81ae-114">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="b81ae-115">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b81ae-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b81ae-116">-프로필</span><span class="sxs-lookup"><span data-stu-id="b81ae-116">-Profile</span></span>
<span data-ttu-id="b81ae-117">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b81ae-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="b81ae-118">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="b81ae-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b81ae-119">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="b81ae-119">-SubnetName</span></span>
<span data-ttu-id="b81ae-120">이 cmdlet이 네트워크 보안 그룹을 연결 하는 서브넷의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b81ae-120">Specifies the name of a subnet to which this cmdlet associates a network security group.</span></span>

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

### <span data-ttu-id="b81ae-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="b81ae-121">-VirtualNetworkName</span></span>
<span data-ttu-id="b81ae-122">가상 네트워크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b81ae-122">Specifies the name of a virtual network.</span></span>
<span data-ttu-id="b81ae-123">이 cmdlet은이 매개 변수에서 지정 하는 가상 네트워크의 서브넷에 네트워크 보안 그룹을 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="b81ae-123">This cmdlet associates a network security group to a subnet in the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="b81ae-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b81ae-124">CommonParameters</span></span>
<span data-ttu-id="b81ae-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b81ae-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b81ae-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b81ae-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b81ae-127">입력</span><span class="sxs-lookup"><span data-stu-id="b81ae-127">INPUTS</span></span>

## <span data-ttu-id="b81ae-128">출력</span><span class="sxs-lookup"><span data-stu-id="b81ae-128">OUTPUTS</span></span>

## <span data-ttu-id="b81ae-129">상속자</span><span class="sxs-lookup"><span data-stu-id="b81ae-129">NOTES</span></span>

## <span data-ttu-id="b81ae-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b81ae-130">RELATED LINKS</span></span>

[<span data-ttu-id="b81ae-131">Get-AzureNetworkSecurityGroupForSubnet</span><span class="sxs-lookup"><span data-stu-id="b81ae-131">Get-AzureNetworkSecurityGroupForSubnet</span></span>](./Get-AzureNetworkSecurityGroupForSubnet.md)

[<span data-ttu-id="b81ae-132">제거-AzureNetworkSecurityGroupFromSubnet</span><span class="sxs-lookup"><span data-stu-id="b81ae-132">Remove-AzureNetworkSecurityGroupFromSubnet</span></span>](./Remove-AzureNetworkSecurityGroupFromSubnet.md)


